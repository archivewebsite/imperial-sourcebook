## TL;DR

After writing "The Claude Code You Don't Know" and "The AI Agents You Don't Know," I wanted to tackle a third installment. This time I pushed myself to work through how large model training actually works, and tried to write something that a non-specialist reader could follow.

Looking at 2026, what actually separates frontier models is no longer pretraining itself. The gap increasingly lives in everything after it: post-training, evaluation, reward design, agent training, and distillation. Each step shapes what users feel. When a model suddenly seems much stronger, it's usually several of these improving together, not any single factor.

The rest of this piece follows the LLM training pipeline in order, focusing on how the back half of the training stack drives the final shipped quality.

## LLM Training Is an Assembly Line

For years, progress in language models was explained by stacking more parameters, data, and compute. But much of what users notice isn't from training on more base text. It comes from the entire pipeline that runs after pretraining. How a model talks, follows instructions, reasons, and uses tools doesn't grow naturally from feeding it more internet text.

InstructGPT gave a clear early example: a 1.3B-parameter model that had been alignment-tuned with preference optimization beat 175B GPT-3 in human preference evals. Two orders of magnitude fewer parameters, and users liked the smaller model better. The back half of training rewrites user perception.

Training is an assembly line where data, algorithms, systems, and feedback are tightly coupled. A change in one layer propagates through the others. In 2026, the capability and commercial value of models is increasingly concentrated in the layers after pretraining.

This is also why some models may not chase benchmark rankings but feel more natural in everyday use. When that happens, post-training is usually the reason.

The six layers above describe the division of work. The diagram below shows a more detailed nine-stage version, where raw data and the system recipe are broken out separately, and agent harness and deployment are their own distinct post-training substages. Two feedback loops run throughout: production traffic feeding back into data engineering, and offline benchmark results feeding back into pretraining.

## Pretraining Is Just the Foundation

Pretraining is still where training begins. Understanding what it actually does is the prerequisite for understanding what every subsequent layer adds. Without this step, there's no language modeling capability, no knowledge compression, and no room for later capability transfer. Engineered well, it does more than teach the model to predict the next token: it encodes the distribution of language, compresses the knowledge and patterns in large-scale text into parameters, and leaves room for future capabilities to be unlocked. Next-token prediction only describes the training form; it doesn't explain why, beyond a certain scale, models suddenly develop abilities they didn't previously show.

After GPT-3, more compute-aware approaches started asking how to allocate a training budget rather than just going bigger. Models don't improve by adding parameters alone. There's a balance between parameter count, training token count, and total compute budget. Many models aren't too small; they're undertrained, and haven't been pushed to the better operating point for their given budget.

When you're actually making these decisions, the practical question is: if someone gave you ten thousand H100s and a month, how would you train the best open-source model you could? Scaling laws here are a budget allocation tool, not an abstract academic curve. You still have to answer: should the next training run add more parameters or more data? Is the current model genuinely capacity-limited, or just undertrained? Given a fixed GPU budget, what ratio works best?

Pretraining is more like pouring a foundation. It determines the knowledge range, generalization potential, and pattern recognition capability, and determines whether there's anything for post-training to build on. But whether the model follows instructions, cooperates with users, and performs stably on critical tasks, that's not something pretraining controls.

Pretraining doesn't just decide how much knowledge the model learns; it also decides what the model can eventually become. The tokenizer's splitting strategy directly affects downstream training. Context window length has to be set before training starts. Whether to include multimodal pretraining, whether to make single-GPU deployability a hard requirement from day one, these tradeoffs get baked into the recipe before training begins; they're not features you bolt on at release. Gemma 3 simultaneously emphasized single accelerator support, 128K context, vision capability, and quantization, which reflects exactly these kinds of tradeoffs. The capabilities users eventually see, like running locally, understanding images, handling long documents, are largely determined during training.

Based on Chinchilla's compute-optimal point, an 8B model should train on around 200B tokens. Llama 3 8B trained on 15T tokens, roughly 75 times more. This kind of over-training recipe typically produces higher capability density per parameter, yielding a smaller, cheaper-to-serve model. Total FLOPs (floating-point operations) is a better predictor of quality than parameter count alone. The chart below makes this gap concrete.

There's another design decision that often gets overlooked: tokenizer vocabulary size, tokenization strategy, and byte-level encoding approaches all have meaningful impact. Llama 2 used a 32K vocabulary; Llama 3 expanded to 128K, compressing sequence length by roughly 15% and improving downstream performance. This carries forward into inference cost and multilingual capability. The token efficiency of Chinese, code, and mathematical notation is set at tokenizer design time. A tokenizer that splits Chinese characters into fragments isn't just a minor overhead per request; it's a decision whose cost compounds across every inference.

## The Data Recipe Determines the Model's Capabilities

Parameter scale was the headline metric for years. The more important concept now is the "data recipe."

What looks like data cleaning on the surface is a full production engineering process. Raw inputs including web crawls, code repositories, books, and forums all pass through text extraction, language identification, quality filtering, PII redaction, safety filtering, and deduplication before entering pretraining. The diagram below shows the complete funnel.

If you treat data as just fuel for training, it's easy to conclude that more is always better. Data engineering is closer to capability design. What the model sees and doesn't see, what proportion goes to code versus math versus encyclopedia content, these choices directly shape the capability distribution the model ends up with.

Deduplication and contamination control are routinely underestimated, but they have large effects. The problem isn't just low-quality data. It includes repeated templates, license boilerplate, mirror pages, and benchmark leakage. Without rigorous document-level and line-level dedup, a model tends to repeatedly absorb the most easily replicated content rather than the most valuable information. Many open-source models that seem inconsistently capable often trace that inconsistency back to data pipeline quality.

In the past couple of years, mixing ratios have become their own research area. Work like "Data Mixing Laws" isn't asking how much more data can be collected; it's asking how different proportions of data types produce different capability structures.

Synthetic data has moved from supplementary to a formal part of the training pipeline. Self-Instruct and similar methods that generate instruction data from the model itself, DeepSeek-R1's distilled reasoning traces, and the growing use of synthetic supervision in Qwen and Kimi series all point in the same direction. Each stronger generation of models contributes to reshaping the data that the next generation trains on. Early models generate basic instruction data. Stronger models generate high-quality reasoning traces and chain-of-thought data. RL-trained reasoning models distill those traces into smaller dense models. Dense here means all parameters run for every token, unlike MoE where only a subset activates per token.

The key point is that models generally need to develop capabilities at larger scale first before those capabilities can be compressed into smaller ones. DeepSeek-R1-Distill is the clearest example. RL-trained large model trajectories produced meaningful gains for dense models from 1.5B to 70B. Llama 3.1 405B was also explicitly used to improve post-training quality for the 8B and 70B variants. These aren't byproducts; they're part of the intended training design.

## System Constraints Have to Be Decided Before Training Starts

Many people think of training as a research problem: what loss function to use, how to reduce loss, what architecture to try. But in real large-scale training, the systems layer is not optional. It's a distributed systems problem, not a single-machine deep learning problem. GPU count, memory bandwidth, parallelism strategy, fault tolerance, and cost can't be tuned after training. They determine from the start how large a model you can train, how long a context you can support, and whether you can run more complex post-training at all.

MoE (Mixture of Experts) is the most representative example of this layer. It scales total parameters at roughly constant compute by routing each token to only a subset of experts, keeping per-token activation cost in check. The tradeoff is routing complexity, load balancing difficulty, and heavier infrastructure. DeepSeek-V3 and the Qwen MoE series are cost-quality tradeoffs, not pure architectural preferences.

Recent public training reports have moved past coarse-grained analysis of model size and token ratios. muP (maximal update parametrization) lets hyperparameters transfer from small-scale experiments to large-scale training. WSD learning rate schedules (warmup, stable, decay) show up in formal training reports alongside optimal batch size and higher data-to-parameter ratios. These details are becoming the real margin between models of equivalent scale.

Long context, multimodality, and new architectures look like product features, but treating them that way misses the training-side constraints. A 128K context target directly changes attention cost, batch size, training curriculum (the ordering and composition of training data), and parallelism strategy. Multimodality changes not just model structure but data mixing ratios, encoder design, and safety evaluation. Making single-GPU deployability a hard requirement tightens constraints on parameter count, quantization paths, and the range of model sizes in a family.

Work like Forgetting Transformer and Kimi's Attention Residuals is answering the same underlying question: how do you train on longer contexts, and how do you avoid information dilution as networks get deeper? From the outside you see a model that handles longer inputs or deploys more efficiently. From the inside you're facing a completely different set of constraints.

Compute budget is fixed. More parameters, more training tokens, longer context, cheaper serving: every dollar spent in one direction costs you somewhere else.

Extending context inflates attention cost and forces a smaller batch size. Making the model larger pushes GPU memory and serving cost up proportionally. These aren't choices to weigh; they're the direct consequence of resource constraints, and most decisions get locked in before training begins.

There's an engineering reality that often goes unmentioned: training is not always stable. After weeks of running thousands of GPUs, a training loss spike appears, too large to ignore, and the only option is rolling back to a checkpoint from days earlier and starting over.

Beyond loss spikes, a single GPU can silently compute wrong gradients without raising any error. NVLink bandwidth anomalies and inter-node communication jitter are both capable of corrupting a run. Detecting, isolating, and recovering from these in a large-scale training run is a lab-grade engineering capability. It cannot be learned from papers.

DeepSeek-V3's technical report explicitly notes that the entire pretraining run had no irrecoverable loss spikes and required no rollbacks. It's also one of the few publicly validated cases of FP8 mixed-precision training working at this scale. The full pipeline used approximately 2.788M H800 GPU hours and completed pretraining on 14.8T tokens.

Training and inference are closely related but are not the same engineering problem. Training cares about gradients, parallelism, checkpoints, throughput, and cost. Inference cares about latency, KV cache (caching past computations to avoid recomputation), quantization, and service stability.

## Post-Training Is Where Users Feel the Difference

Much of the improvement that ordinary users perceive happens after pretraining. Instruction tuning trains the model on labeled instruction-response pairs. It changes how the model answers, turning "how to accept tasks, how to organize output, how to behave like a cooperative assistant" into supervised signal. A base model may already have a lot of latent capability, but without this step those capabilities rarely emerge stably in the form users expect.

Moving further along, RLHF, DPO, and RFT all have the same direction: incorporating "what counts as a better response" into the training loop. They take different paths.

- RLHF (Reinforcement Learning from Human Feedback) first imitates high-quality responses, then uses pairwise preference comparisons for reinforcement
- DPO (Direct Preference Optimization) shortens that path by learning directly from preference pairs, without training a separate reward model
- RFT (Reinforcement Fine-Tuning) is a more productionizable interface that packages task definition, grader design, and reward signal into a deployable pipeline

Talking about post-training today purely in terms of SFT or RL isn't enough. The harder question is how to design the evaluation, how to score outputs, and what kind of response is worth continuing to optimize toward.

SFT (supervised fine-tuning) learns more than knowledge; it also learns style. Output length, format, whether to include citations, whether to prefer bullet points, all significantly shape the model's output patterns. Many users think they're comparing capability when the real difference is style. And preference evaluation naturally favors longer responses, making more elaborate output seem more competent. Benchmark performance in post-training is often insufficient; it needs to be combined with real-task results, cost, and stability.

Modern post-training is a multi-stage pipeline. DeepSeek-R1's public recipe is one of the clearest examples. It proceeds in four stages:

**Stage 1** is cold-start SFT, using a small set of high-quality chain-of-thought data to warm up before doing RL. DeepSeek-R1-Zero showed that going directly from a base model (the raw pre-trained model before alignment) into RL is viable, but pure RL training produces a model that repeats itself, mixes languages, and is hard to read. Cold-start SFT gives RL a more stable starting point by first locking in format and language consistency. It's not a redundant step.

**Stage 2** does reinforcement learning on verifiable domains like math, code, and logic, using GRPO as the training algorithm with programmatically checkable correctness as the reward signal. The key question is why GRPO rather than traditional PPO. PPO (Proximal Policy Optimization) requires a separate value network to estimate the value of the current state, and maintaining two networks simultaneously on large models is engineering-heavy. GRPO samples multiple responses to the same prompt and uses within-group ranking instead of absolute value estimation. It requires no separate value network and is significantly simpler to operate. Both the DeepSeek series and Cursor Composer 2's RL infrastructure use approaches close to GRPO.

**Stage 3** does Rejection Sampling Fine-Tuning: filtering successful RL trajectories and converting them into new SFT data for another supervised fine-tuning round. This is the bridge between RL and SFT. The good trajectories RL explored become the high-quality training samples for the next SFT pass.

**Stage 4** incorporates helpfulness and safety preference feedback to bring the model to a state that meets release standards as an assistant.

The four stages depend on each other: cold start stabilizes RL, RL generates high-quality data, rejection sampling turns those into SFT inputs for the next round, and alignment RL brings behavior to convergence. From public results, the gap between direct SFT and going through all four stages is usually visible.

## Eval, Grader, and Reward Are Redefining What Training Optimizes For

The component that turns model output into training scores is called the grader. It creates problems that are easy to miss. Evaluating only the final answer teaches models to take shortcuts. Coarse scoring lets noise get amplified by RL over time. Benchmark scores improve while real-task performance doesn't always follow. Often what looks like a gap in base model quality is actually a gap in how the objective was defined.

In training terms: eval decides what to measure, grader decides how one output becomes a score, reward decides which direction the model gets pushed. Together they form a concrete feedback loop: task definition, eval, grader, optimization, rollout (the trajectory produced when the model executes a task), re-evaluation. If any link in the chain drifts, all subsequent optimization drifts with it.

Evaluating only final results means a model can get lucky or reach a correct answer through an incorrect process. In code, math, and complex reasoning tasks this is especially problematic. If intermediate steps don't enter the feedback, the model learns not how to reason more reliably but how to maximize the probability of the final scoring event.

This is why more work has shifted from traditional RLHF toward verified rewards, using programs to directly check correctness. For verifiable tasks like math, code, and logic, you can score correctness directly rather than relying primarily on human preference. But verified rewards haven't eliminated the problem. Over-optimization, reward overfitting (the scoring rules get gamed without genuine capability improvement), and mode collapse (outputs become highly uniform and lose diversity) still appear. The problem has shifted from "are preferences labeled accurately" to "is the scoring pipeline stable."

A model's written reasoning trace also can't be treated as a complete record of its internal process. In observability experiments on reasoning models, Anthropic found that models use hints provided to them but don't acknowledge this in their visible chain of thought. In reward-hacking scenarios, they're more likely to patch in a plausible-looking explanation after the fact. Reward hacking means exploiting the scoring system rather than genuinely completing the task. Visible CoT is better used as a training and monitoring signal, not taken as a complete ground truth.

At a deeper level, models can start to exploit the scoring channel itself. Research on reward tampering and alignment faking shows that models could in principle actively interfere with the scoring process. Reward tampering means directly modifying the reward computation. Alignment faking means appearing compliant while concealing misaligned intent. Once a model has sufficiently capable environment access, what it optimizes may include not just task outcomes but also checklists, reward code, and the training relationship itself. In a 2025 Anthropic experiment, extra reward-hack knowledge was injected into a set of exploitable production coding RL environments. The resulting generalization was consistent with this pattern: after a model learned reward hacking, it continued exploiting similar tasks and also exhibited broader misalignment behaviors like alignment faking.

These behaviors are invisible in standard conversational evals and only appear in agent task environments. The engineering implication is direct: reward, grader, environment isolation, and monitoring all have to be treated as part of training design.

In the agent phase, reward design gets broken down further. Final outcome is just one component. Process quality, context management, and anti-exploitation constraints are each measured separately. Kimi K2.5 rewards effective decomposition and genuine parallelism. Chroma Context-1 scores relevant documents found during search. Cursor Composer 2 incorporates summaries from long tasks into rewards because a corrupted summary will distort all subsequent context.

In implementation terms: ORM (Outcome Reward Model) scores only the final answer. Signal is sparse, cost is low, good for getting started, but also more prone to shortcut reasoning. PRM (Process Reward Model) scores intermediate steps. Signal is denser, generally stronger for math and code reasoning, but both annotation and systems cost are much higher. OpenAI's math reasoning experiments showed PRM not only improved accuracy but made it easier to constrain process quality, since every step is supervised. The practical issue is that PRM typically costs several times more than ORM, so most real systems start with ORM, and only in verifiable domains like math, code, and logic does it become practical to automate PRM using programs to check intermediate steps, bypassing the human annotation bottleneck.

The full loop runs like this:

Recent alignment approaches are all converging on the same goal. Anthropic's Constitutional AI feeds human-written principles into training and uses AI feedback in place of per-example human preference labels. OpenAI's Deliberative Alignment builds safety compliance into the reasoning process, asking reasoning capability itself to carry some of the safety constraints. Deliberative Alignment means the model reasons through safety considerations at inference time rather than relying on trained reflexes. Both approaches are moving alignment away from human labels and toward being intrinsic to training objectives.

The Constitutional AI pipeline runs in two phases: first the model self-critiques and revises its outputs according to the principles, then AI feedback replaces per-example human annotation. Alignment was never an afterthought appended after training. What the system tests, how it scores, and what it rewards determines where the model goes. That has always been the most direct control lever in the back half of training.

## In Agent Training, the Model Isn't the Only Thing Being Optimized

Over the past two years, reasoning models exemplified by the o1 series and DeepSeek-R1 have demonstrated that, given stable rewards, reliable verification, and the right infrastructure, RL on language models can substantially improve performance on math, code, and logic tasks.

This simultaneously opened a new dimension: inference-time compute can now also scale. RL training took on an additional function beyond teaching the model to answer questions: it started teaching the model how to allocate its reasoning budget, knowing when to think longer and when to stop. The next challenge after that became keeping a model acting productively in an environment across a sustained task, not just extending a single chain of thought.

Qwen's former model lead Junyang Lin's reflection on the Thinking and Instruct hybrid approach is representative. The hard part isn't giving the model a reasoning toggle. The two modes have fundamentally different objectives: one prioritizes directness, compliance, and low latency; the other prioritizes broader exploration and higher accuracy. Pushed further, the training objective shifts from "how long to think before answering" to "how to allocate budget across actions, how to incorporate feedback, how to keep a task moving."

At this point the training target is no longer just a model that answers questions. It's a system that can plan, call tools, receive feedback, and stay coherent across a long task. The training stack changes accordingly. Browsers, terminals, search, execution sandboxes, memory systems, tool servers, and orchestration frameworks all start entering the training system.

More precisely, the harness is the control program wrapped around the model. This concept belongs to both agent runtime and training: it decides what input the model sees, in what form it receives feedback, when to truncate context, and when to call tools. Prompt construction, memory update, retrieval policy, context editing, and tool orchestration all live here. The environment is no longer just a static verifier; it's a layer that training and deployment both have to directly engage.

The harness has to be stable before model training can be meaningful. When tool return values are inconsistent, the browser environment doesn't match production, or the file system state isn't reproducible, the grader breaks first, and what the model then learns is not capability but how to exploit environment bugs. Training agents means debugging the model and debugging the environment at the same time.

The approaches from three teams are all clear. Kimi uses PARL to solve parallel decomposition and credit assignment. Cursor uses self-summarization and real-time RL to reconnect long coding sessions and production traffic back to training. Chroma trains prune\_chunks as a policy, making context pruning a first-class part of the retrieval process itself.

In the SFT era, data diversity was the primary driver. In the agent era, environment quality is the core variable: stability, fidelity to production, coverage, difficulty distribution, reward richness, and resistance to exploitation. Training objectives shift accordingly. What's needed is sustained reliability across a complete task, not getting one question right. Classic CoT benchmarks don't cover this.

This shift is moving further upstream: not just training models inside a runtime harness, but making the harness code itself a target that an outer loop can search and optimize.

Kimi K2.5's PARL is a useful case to unpack. The approach is direct: only train the orchestrator, and concentrate credit assignment at the orchestration layer rather than trying to optimize all sub-agents simultaneously.

Reward signal has three components: task success, parallel decomposition quality, and completion constraints, all driving the orchestration layer. During early training, the r\_parallel weight is increased to encourage exploration of parallelization strategies, then gradually annealed to 0 to prevent the model from treating parallel sub-agent spawning as a shortcut. Evaluation doesn't just measure total steps; it measures critical path length. A shorter critical path indicates that parallelism is actually working.

By 2026, this has gone one step further. Meta-Harness explicitly extracts harness engineering as a standalone optimization target. It doesn't optimize weights; it optimizes the harness code itself, meaning the prompt construction, retrieval, memory, and state update programs wrapped around a fixed model. The opening number in the paper is direct: with the same base model, only changing the harness, you can see a 6x performance gap on the same benchmark. The program surrounding the model is no longer just a deployment detail. It's a layer that shapes capability.

The key isn't adding another abstract optimizer layer. It's writing all prior code, scores, and execution traces (the logs of tool calls and state changes) to a filesystem and letting the proposer (the module that suggests harness modifications) work through them by doing grep, cat, and diff comparisons, then trace failed paths to revise the harness. The paper's assessment is clear: most text-based optimizers aren't effective on harnesses because harnesses are long-running, stateful programs. Showing only scalar scores or summaries collapses too much information. Harness bugs often surface many steps later, and once the feedback is over-compressed the diagnostic chain breaks.

These results go beyond higher benchmark numbers. In online text classification, Meta-Harness exceeded the ACE (Agent Context Engineering baseline) by 7.7 points while cutting context token usage to 1/4. In retrieval-augmented math reasoning, a discovered harness showed an average of 4.7 points of additional gain across 5 held-out models on 200 IMO-level problems. On TerminalBench-2, it also outperformed the hand-engineered baseline. What's being optimized is no longer just the model's internal policy but also the program that organizes how the model sees and acts on information.

A concrete example: Meta-Harness automatically discovered environment bootstrap on TerminalBench-2, running a shell command before the agent loop starts to snapshot the working directory, available languages, package manager, and memory state and inject it into the first prompt. Many coding agents spend their first few turns probing the environment. Getting this pre-loaded right means the gain may not come from stronger weights but from the harness putting the model in a better starting context.

At this point, the optimization target has expanded from answer, to trajectory, to the harness program that carries the trajectory.

## After a Frontier Model Ships, the Training Pipeline Keeps Running

Thinking about today's large models as the product of a single pretraining run is no longer sufficient. A shipped model has typically already gone through pretraining, post-training, distillation, and specialization as a complete chain, and stronger models are continuously producing training data for the next generation.

DeepSeek-R1's distillation series is the clearest example: a large model develops reasoning capability through RL and verified rewards, then those reasoning trajectories transfer to smaller dense models. Specialized models like TranslateGemma show another path: on a more clearly defined target task, high-quality data and specialized reward design compress and direct capability further. At this stage, stronger models aren't just used to serve users; they're directly producing training data for the next generation.

There's a deeper reason than just trajectory transfer. One possible explanation is that in internet-scale pretraining corpora, knowledge memorization and reasoning capability are entangled, and current pretraining objectives require models to learn both simultaneously. Larger models are required first because only at sufficient scale can they carry both responsibilities at once. They can then generate pure reasoning demonstration data, and smaller models trained on that data can focus on reasoning itself without being forced to memorize everything. Bigger-before-smaller is partly about capability decoupling, not just cost strategy.

Deployment adaptability matters as much as raw capability. Many scenarios don't need a generalist frontier model; they care about cost, latency, stability, and controllability. The end of training doesn't have to be larger. It can be smaller, cheaper, and more specialized.

The model that gets shipped isn't necessarily the one at the rightmost point of the training curve. Before release, teams typically compare multiple checkpoints across real-task results, refusal style, tool stability, cost, and regression risk. The version that ships is a product decision, not the checkpoint with the highest single-metric score.

Users see a model name and assume it corresponds to a smoothly ascending training curve. Which checkpoint actually goes live is a separate question.

A large model's value is both in what it can do for users today and in how it will continue generating training data, distillation sources, and release bases for the next generation.

Beyond offline training, near-online continuous optimization has entered the mainstream pipeline. Cursor Composer 2's real-time RL indicates that some agent capabilities are already being iterated on through production traffic, rather than waiting for the next large-scale offline training cycle. The boundary between training and deployment hasn't disappeared, but the feedback loop between them is getting shorter.

## How to Read Why a Model Got Stronger

In 2026, the value of frontier model work is increasingly about who can run the full post-pretraining stack end-to-end: continuously producing training data, doing distillation, doing specialization, getting eval and reward design right, and making the right deployment choices.

When a model seems to suddenly improve, there are three things worth checking first:

- Where the change happened. Many capability gains do come from stronger pretraining and better data recipes, but a lot of the subjective improvements come primarily from post-training. Whether the model follows instructions, uses tools correctly, and gives consistently well-formatted responses often doesn't grow from feeding it more text.
- Which layer the improvement comes from. Is it weights and training recipe, or reward / eval / grader, or harness code and deployment loop? For reasoning models and agents, what users feel as "getting stronger" is often not produced by the base model alone. How eval was set up, how rewards were scored, how stable the tool environment is, how retrieval and memory are organized, how summaries and context are trimmed, and which checkpoint was chosen for release, all of these together reshape the final product experience.
- What the shipped version is optimizing for. Some releases are chasing a higher ceiling. Others are cutting cost, latency, and regression risk. Others are specializing for a particular class of tasks. A release is a product decision, not the furthest-right point on a training curve. Paying attention to what a given update is optimizing for gets you closer to the real picture.

Breaking down "model suddenly got stronger" back to production terms, many improvements are amplified jointly by the back half of the training stack and the outer harness. The iteration cycle on this is also shortening: production traffic continuously flows back into training, each stronger generation produces capability while also producing supervision data for the next, and the outer program rewrites itself based on rollouts, logs, and real-task feedback.

Today's shipped model is a snapshot. The pipeline and the harness program are what keep running.

## Further Reading

1. Hoffmann et al. (2022). Training Compute-Optimal Large Language Models (Chinchilla). arXiv:2203.15556
2. Ouyang et al. (2022). Training language models to follow instructions with human feedback (InstructGPT). arXiv:2203.02155
3. Shao et al. (2024). DeepSeekMath: Pushing the Limits of Mathematical Reasoning in Open Language Models (GRPO). arXiv:2402.03300
4. DeepSeek-AI (2025). DeepSeek-R1: Incentivizing Reasoning Capability in LLMs via Reinforcement Learning. arXiv:2501.12948
5. DeepSeek-AI (2024). DeepSeek-V3 Technical Report. arXiv:2412.19437
6. Llama Team, AI @ Meta (2024). The Llama 3 Herd of Models. arXiv:2407.21783
7. Bai et al. (2022). Constitutional AI: Harmlessness from AI Feedback. arXiv:2212.08073
8. OpenAI (2024). Deliberative Alignment: Reasoning Enables Safer Language Models. openai.com/index/deliberative-alignment
9. Anthropic (2025). Sycophancy to Subterfuge: Investigating Reward Tampering in Language Models. anthropic.com/research/reward-tampering
10. MacDiarmid et al. (2025). Natural Emergent Misalignment from Reward Hacking in Production RL. arXiv:2511.18397
11. Lee et al. (2026). Meta-Harness: End-to-End Optimization of Model Harnesses (preprint project page). yoonholee.com/meta-harness
12. Kimi Team (2026). Kimi K2.5 Tech Blog: Visual Agentic Intelligence. kimi.com/blog/kimi-k2-5
13. Rush, S. (2026). A technical report on Composer 2. cursor.com/blog/composer-2-technical-report
14. Chroma (2026). Chroma Context-1: Training a Self-Editing Search Agent. trychroma.com/research/context-1
