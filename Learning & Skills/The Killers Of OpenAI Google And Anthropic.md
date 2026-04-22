---
title: The Killers Of OpenAI Google And Anthropic
source: https://ai.gopubby.com/the-killers-of-openai-google-and-anthropic-524bdadf3c05
author:
- '[[Jose Crespo]]'
- '[[PhD]]'
published: 2026-04-10
created: 2026-04-17
tags:
- clippings
---

Democratizing access to artificial intelligence

## LLMs freeze after training. These new players have invented something awesomely different.

![](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*IOparWAxwsrfnygMIHbBoQ.gif)

Figures, animations, diagrams, and plots were created by the author using Stable Diffusion, Blender, and Python libraries.

## The LLM Era Is Over

The biggest names in AI have an aging problem, and they are trying to fix it by throwing more raw computation at it. Blatant mistake!

OpenAI, Google, Anthropic, and the rest have spent the last two years scaling inference-time compute: chain-of-thought prompting, search trees, verification loops, more tokens at test time. As I argued in previous articles, this approach has eliminated most of the surface hallucinations, the kind that embarrass you in a demo, while producing deeper structural errors that are far harder to detect and far more dangerous to trust.

And here is what most people are missing: the new LLMs sound smarter. They are not. They have simply learned to hallucinate with better grammar. And the data proves it: with every new release, the deeper hallucination rates are going up, not down.

One of OpenAI’s biggest recent models hit an almost mind-blowing 50% hallucination rate on their own SimpleQA benchmark. One in two answers, fabricated. The coherency is a mask. What is underneath is getting worse.

![](https://miro.medium.com/v2/resize:fit:2000/format:webp/1*x-xh4NKEAHG6CbesRIWi8Q.png)

The Four Mathematical Ingredients of the Killer AI Linear algebra provides operators. Geometry provides curvature and the Fisher metric. Topology provides structural invariants. Probability provides uncertainty and belief updating. The current paradigm bolts these together after the fact, stacking probability on top of flat linear algebra and hoping for the best. The architecture proposed here weaves them from the start: computation is movement through a space whose structure determines what can be preserved, what can be updated, and what will inevitably be lost.

So there you go: the companies that dominated the first era of AI are becoming its dinosaurs, and they are too busy scaling to notice what the new-kids-on-the-block competitors have already understood:

> ==intelligence is not a frozen function. It is a continuously updated probability distribution moving through a structured space. And in a real learning system, space is not the stage on which computation performs. Space is part of the script.==

In quieter times, this would be a technical debt problem. An expensive one, but manageable. These are not quiet times. The window is closing because the architecture itself is hitting a wall that compute cannot push through, and for the first time, there are credible alternatives waiting on the other side.

A new class of AI architecture is now positioned for a serious overtake of the entire industry. Not by building bigger transformers. Not by training longer. By changing the space in which computation happens. The approach has no single brand name yet, but the technical foundation is clear: **Fisher-Bayesian AI (see chart above)**. It replaces the flat Euclidean geometry that neural networks have assumed since the 1980s with the curved, information-theoretic geometry that probability distributions actually live in. It does not improve the existing paradigm. It obsoletes the mathematical surface on which that paradigm was built.

Let’s cut now the tech jargon and explore with a real-world example in an animation with two drones facing the same landscape with the same obstacles. However, one runs on a frozen AI trained like an LLM: it planned its route once before deployment and never updates, because for the LLM AI the world stops changing the moment you finish training. The other runs on a Bayesian brain: every sensor reading reshapes its map of the real world (you know, the one with mountains, valleys, and the kind of surprises that don’t care about your training data) in real time. Now watch what happens when a new obstacle appears mid-flight.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*YfOhtshPczkXnR2DWy69Sw.gif)

The Frozen AI Drone vs. the Bayesian AI Drone The frozen AI drone (left) flies with a flat map printed before takeoff. No contour lines, no elevation data. Nothing that appeared after training exists on that map. When a new obstacle shows up mid-flight, the drone flies straight into it and explodes. The Bayesian AI drone (right) draws its own map as it flies. Every sensor reading warps the grid: tight where danger is high, loose where the path is clear. It curves around every obstacle and reaches the goal. One drone had a map. The other builds the map as it flies.

Yup, this is not a surprise: frozen AI drones crash because their maps are frozen too.

The nasty surprise, though, is realizing that this deficient AI is what the industry has been scaled and built around.

Chatbots are answering questions about a world that has already moved on after their training cutoff. Autonomous systems are navigating cities that have changed since the last model update. Financial models are pricing risk in market regimes that did not exist in their training data. Medical AIs are diagnosing with knowledge that stopped evolving the day the product left the factory. I could keep going, but you get the point: every single one of these domains is screaming for an AI that can retrain itself by doing.

The companies building the Bayesian alternative are not just tweaking the old architecture. They are replacing the static map with something alive. Their drones do not crash because they were never flying blind in the first place. They build the terrain as they move through it, reshaping their internal space with every new observation, tightening certainty where the evidence is strong and relaxing it where the world is still unclear.

This is not a minor technical improvement. It is the difference between ==intelligence that stays in contact with reality and intelligence that expires the moment reality changes.==

You can be sure of one thing: you had better take a serious look at the Bayesian companies that already understand that difference and are building the new products, instead of focusing too much on LLM solutions that are already outdated.

## A Deeper Look at the Core of the New AI Engines

You see, the old AI industry is still running every major production model by keeping its core parametric machinery frozen at inference time.

That means the learned parameters do not update in real time from your stream of interactions. Yes, the industry now wraps those frozen weights with retrieval layers, memory stores, tool use, agent loops, and every kind of prosthetic scaffolding. But peel that scaffolding away and the situation is always the same: a static set of learned parameters that has not changed since the last retraining cycle.

The smoking gun The latest GPT models were described by OpenAI as a Transformer pre-trained to predict the next token and then post-trained, not as a system that continuously rewrites its own core beliefs during use. **Read that again. The most advanced AI system** on the planet was described by its own creators as a machine that learns once, ships, and then freezes.

That is not a bug. That is the architecture.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*wbKa2tQVGPansdmhpYggrw.gif)

Gradient Descent vs. Bayesian Inference Gradient descent (left) The current AI approach converges to the nearest local minimum and stays trapped. Bayesian inference (right) the new kid on the block maintains a posterior over the full landscape, reshaping with each observation until it finds the basin the data actually supports. The difference is not only compute. It is mainly the space where that computation is running.

Let’s take a closer look, because this trap goes deeper than the update problem alone.

A frozen LLM does not just refuse to learn after training. It also lives in the wrong space altogether: a flat geometry with no intrinsic way to tell which parameters carry real information and which are only noise.

Flat architectures cannot preserve the structural invariants that real cognition depends on, the kind that tell you when two beliefs are genuinely close and when they only seem close because the coordinate system is misleading you.

And once that freeze-and-serve model is deployed, the bad geometry is locked in place. What you get is a machine that can interpolate brilliantly inside a sealed statistical landscape, yet cannot revise a single belief in real time without breaking something else in the process.

Still skeptical Then look at the cracks that are no longer hypothetical. In September 2025, OpenAI’s own researchers published a paper arguing that language models hallucinate because standard training and evaluation procedures reward guessing instead of acknowledging uncertainty. On the PersonQA benchmark, their most advanced reasoning models showed hallucination rates of 33% and 48%. One answer in three was fabricated. For the flagship model, nearly one in two.

That is not some cosmetic bug flickering at the edge of an otherwise healthy system. It is a structural failure. The model has been optimized to keep producing answers, not to represent, in any deep way, the boundary between what it knows and what it does not know.

But that boundary is exactly what real reasoning under uncertainty depends on. And uncertainty requires curvature. But you now know that the flat architectures on which our LLMs are built throw that away before training even begins.

The new killer AI companies are using exactly the metric that gives that curvature back: the Fisher metric.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*dufaiUHrCMCR61aqWO1mVQ.gif)

The Fisher Metric as the Geometry of Bayesian Learning The green path is the Bayesian–Fisher AI: it follows the curved surface, bending with the geometry the data creates. The red path is the current frozen AI, trained once and retrieving forever: it flies straight through flat space, ignoring the curvature entirely. The dashed drop lines show the gap between where the flat optimizer thinks it is and where the actual landscape lies. That gap is not a rounding error. It is the cost of running computation in the wrong space.

Look at the red line in the animation above. That is what every large language model does when it trains: flat Euclidean gradient descent, treating every direction in parameter space as equivalent, like planning a flight from Vienna to Tokyo on a flat map. You will arrive somewhere, for sure **it will not be Tokyo.**

The Fisher metric tells you the map is curved. Some directions are highly informative, others are inert. Shun-ichi Amari formalized this in the 1990s with the natural gradient: F⁻¹∇L. One operation that turns a flat step into a step that follows the surface. The green path is what that looks like. The red path is what the entire industry ships instead.

Why Because the Fisher information matrix for a 70-billion-parameter model has 4.9 × 1⁰²¹ entries. You cannot realistically compute it, store it, or invert it. So the big players in AI chose scale over geometry, they are in that red line in the animation above that gets longer, gets faster, but it is still pointing in the wrong direction.

And inference-time compute does not fix that. It only carries you farther across the same flat map.

Why Because the Fisher information matrix for a 70-billion-parameter model has 4.9 × 1⁰²¹ entries. You cannot realistically compute it, store it, or invert it. So the big players in AI chose scale over geometry. They are like the red line in the animation above: getting longer, getting faster, but still pointing in the wrong direction.

And inference-time compute does not fix that. It only carries you farther across the same flat map. **You are still no closer to Tokyo.**

So what does the alternative actually look like when you put it all together The animation below shows a complete Fisher-Bayesian system in operation: reconfigurable probability graphs instead of hardcoded neural connections, all living on a curved surface governed by the Fisher metric field. No tricks. No black boxes. Just a system that learns by changing its own shape when confronted with new perceptions and new information.

That is a real, refreshing, and hopeful alternative to the dead-end path the big names in AI are following, burning enormous amounts of money on brute-force compute instead of using geometry to simplify the problem.

![](https://miro.medium.com/v2/resize:fit:2000/format:webp/1*UK1HVVgtr1dooXHGP4gKYA.gif)

The Engine That Learns by Changing Shape What if AI did not retrieve answers from a frozen database, but actually changed its own geometry every time new evidence arrived This is what a Fisher–Bayesian engine looks like: a living probability field where the space of belief itself deforms before any computation happens. Geometry moves first. Then the graph retrains. The model you use today cannot do this.

## The Heroes of the New AI Land

The companies that will force this transition are not coming. They are already here. They are the dark horses trying to escape the freeze-and-serve paradigm itself. They treat uncertainty, belief revision, causality, and structure as first-class architectural objects, not as afterthoughts bolted onto a frozen generator. And the mathematical traditions behind these attempts, probabilistic updating, causal graphical models, information geometry on statistical manifolds, active inference, sit far outside the mathematical center of gravity that built today’s AI empire.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*M7C7_N61mi5mf4KrSM8MlA.gif)

The Dark Horses Five companies building outside the freeze-and-serve paradigm. What they replace, and what they have already delivered.

Not all of them are equally close to the full Fisher-Bayesian architecture our story describes. But each one has built at least one load-bearing pillar of it, and together they form the outline of a paradigm that the flat-space incumbents cannot replicate by scaling alone.

is the closest to the complete vision. Their engine runs on Karl Friston’s free energy principle, the same mathematical framework that neuroscience uses to describe how biological brains learn. The weights do not freeze after training. Beliefs update continuously at deployment time, every observation reshaping the posterior in real time. This is not an approximation of the Fisher-Bayesian paradigm. This is the paradigm, running in production. Their AXIOM model outperformed Google DeepMind’s DreamerV3 by 60% while being 97% more efficient and 39 times faster. That efficiency is not an engineering trick. It is what happens when you stop fighting the geometry and start following it.

builds the causal pillar. Causal graphs encode interventions and counterfactuals, not pattern correlations. A causal graph defines a family of probability distributions indexed by what you could do, not just what you have seen, and the Fisher information over that family tells you which interventions actually matter. Geometry applied to causation. Their $50M in funding, their partnership with Google Cloud, And clients like Cisco and Scotiabank tell you that the enterprise market is now seizing the opportunity.

builds the topological pillar. $33M from Khosla Ventures backing a team of PhD mathematicians and former Tesla engineers who are applying category theory to machine learning. They co-authored a paper with Google DeepMind on categorical deep learning that lays the theoretical foundation. Category theory is another beast that gives you something no neural network can: compositional guarantees. If two modules are correct individually, their composition is correct by construction. **Where the Fisher metric gives you local curvature, category theory gives you global structural invariants**, the scaffolding that ensures the whole system holds together and not just each isolated piece.

is the proof that the mathematics survives contact with reality. Acquired by TD Bank Group and now operating as their AI centre of excellence, Layer 6 publishes at ICML and NeurIPS while serving around 30 million banking customers. Their CausalPFN holds the best average rank across standard causal inference benchmarks by combining Bayesian causal inference with transformer-based amortization: raw observations in, calibrated causal effects out, with uncertainty estimates baked in from the start. This is Fisher-Bayesian mathematics running at institutional scale in one of the most unforgiving domains on the planet: financial decision-making, where being wrong costs real money and where most LLM-based AI has been off-limits, but not this new Bayesian-Fisher kind.

**Microsoft** occupies a peculiar position here. Infer.NET already gives it the right mathematical foundation by compiling probabilistic programs directly into inference algorithms, and it has the cloud infrastructure to deploy that foundation at a scale almost nobody else can match. What has held it back is not the math but the difficulty of automating models that are still too hand-built to scale cleanly in production. That is a serious limitation, but it is an engineering limitation, not a conceptual one. If Microsoft chooses to act, we all know that it does not need to pivot. It needs to ship.

**So, summig up.**

> VERSES builds the brain. causalLens builds the “why.” Symbolica builds the structural scaffolding. Layer 6 proves it works with real customers and real money. Microsoft has the cloud to deploy it everywhere. Nobody has put all the pieces together yet. But the pieces exist, and none of them run on flat space.

**These five killers** share one property that OpenAI, Google, and Anthropic do not possess and cannot acquire by scaling. Their computation already lives on the curved surface. Four of them are dark horses: small, underfunded, mathematically correct. The fifth is Microsoft, which is not a dark horse but something potentially more dangerous: a sleeping giant with the right foundation already built, waiting for a reason to wake up.

They did not start in flat space and bolt on corrections. They started in the right geometry. Everything they build from here compounds on a mathematical foundation that the flat-space optimizers cannot reach no matter how many GPUs they stack, because the problem was never compute. The problem was the space.

![](https://miro.medium.com/v2/resize:fit:2000/format:webp/1*CJ9NRlDgBF4C0wlTzRF-Qg.png)

The AI Battlefield Nobody Is Mapping The x-axis is the only axis that matters: how close is the architecture to real-time Bayesian belief updating on a curved statistical manifold The left side trains once and serves forever. The right side never stops learning. The arrows tell you which direction the industry is moving. The incumbents have not noticed yet.Artificial IntelligenceProgrammingTechnologyBusinessMathematics

## Related Clippings
<!-- managed-by-linking-obsidian-clippings:start -->
- [[AI Will Destroy The Economy]]
- [[Teslas Lifeline Is Failing]]
<!-- managed-by-linking-obsidian-clippings:end -->
