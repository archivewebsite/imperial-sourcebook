# How Engineering Teams Are Using AI: field report, 2026

## Executive summary

Engineering teams are using AI less like a magic replacement engineer and more like a tireless, occasionally unhinged junior teammate: useful for drafting, transforming, searching, testing, reviewing, and summarizing, but still needing adult supervision. The serious shift is from “autocomplete in the IDE” to AI embedded across the software delivery lifecycle: code generation, PR review, migration, testing, documentation, incident response, security scanning, and internal knowledge retrieval.

The current evidence is mixed but no longer theoretical. Stack Overflow’s 2025 survey says 84% of respondents are using or planning to use AI tools in development, and 51% of professional developers use them daily. At the same time, developers distrust AI accuracy more than they trust it: 46% actively distrust AI tool accuracy versus 33% who trust it. Humanity has discovered a machine that helps you move faster while also making you check everything it says. Elegant. ([Stack Overflow](https://survey.stackoverflow.co/2025/ai/ "AI | 2025 Stack Overflow Developer Survey"))

The big organizational lesson is that AI amplifies the system it is dropped into. DORA’s 2025 report, based on more than 100 hours of qualitative research and nearly 5,000 technology professionals, concludes that AI “magnifies” both high-performing organizations and dysfunctional ones. In plainer terms: good engineering systems get faster; messy ones generate mess faster. ([Google Research](https://research.google/pubs/dora-2025-state-of-ai-assisted-software-development-report/ "DORA 2025 State of AI-assisted Software Development Report"))

## 1. The main ways engineering teams are using AI

### 1. Code generation and pair programming

This is the obvious one: engineers ask AI to write boilerplate, implement small features, convert pseudo-code into working code, generate API clients, add error handling, write SQL, draft scripts, or produce first-pass implementations. GitHub’s Accenture study found that Copilot users adopted the tool quickly, with 67% using it at least five days per week; Accenture saw an 8.69% increase in pull requests, a 15% increase in PR merge rate, and an 84% increase in successful builds in the study. Those are vendor-reported results, but the study did include telemetry and a randomized controlled trial design, which is better than the industry’s usual “we vibe-tested it and bought hoodies.” ([The GitHub Blog](https://github.blog/news-insights/research/research-quantifying-github-copilots-impact-in-the-enterprise-with-accenture/ "Research: Quantifying GitHub Copilot’s impact in the enterprise with Accenture - The GitHub Blog"))

At large tech companies, AI-written code is now a management-visible metric. Google says 75% of new code at Google is now AI-generated and approved by engineers, up from 50% in fall 2025, and says it is moving toward “agentic workflows” where engineers orchestrate autonomous AI task forces. Microsoft’s Satya Nadella said in April 2025 that 20% to 30% of code inside Microsoft repositories was “written by software,” while noting results vary by language. Treat these figures as company-reported and measurement-dependent, not holy scripture chipped into granite. ([blog.google](https://blog.google/innovation-and-ai/infrastructure-and-cloud/google-cloud/cloud-next-2026-sundar-pichai/?utm_source=chatgpt.com "Sundar Pichai shares news from Google Cloud Next 2026"))

### 2. Codebase understanding and onboarding

A very practical use case is asking AI to explain unfamiliar systems: “What does this service do?”, “Trace this request path,” “Where is this feature flag used?”, “Summarize this module,” or “Find every place this API contract matters.” This matters because reading code is often slower than writing it, which humans somehow kept pretending was not true.

Block’s internal agent Goose is a good story here. Wired reported that Goose helps with coding, data visualizations, prototypes, and understanding unfamiliar codebases. One Block engineering lead described asking it to explore a codebase and summarize how it works. Block also learned the hard way that agents can make mistakes, including deleting files, so they ran it in rollback-friendly environments and kept human review protocols. ([WIRED](https://www.wired.com/story/jack-dorseys-block-made-an-ai-agent-to-boost-its-own-productivity "Jack Dorsey's Block Made an AI Agent to Boost Its Own Productivity | WIRED"))

### 3. Large-scale code migrations and technical debt

This may be one of the highest-value uses because migrations are repetitive, structured, and expensive. Airbnb used LLMs to migrate nearly 3,500 React component test files from Enzyme to React Testing Library. The original manual estimate was 1.5 years of engineering time; the LLM-assisted migration finished in six weeks. Airbnb’s pipeline migrated 75% of files in four hours, reached 97% after systematic prompt and script refinement, and used humans for the final 3%. ([Airbnb Tech](https://airbnb.tech/infrastructure/accelerating-large-scale-test-migration-with-llms/ "Accelerating Large-Scale Test Migration with LLMs | Airbnb Engineering & Data Science"))

Google has used AI internally for code migrations too. In one Google migration workstream, 80% of code modifications in landed changelists were AI-authored, while engineers reported a 50% reduction in total migration time. The key detail: Google combined AI with static analysis, symbol cross-references, validation, and human review. The model was not simply told, “go fix the monorepo, champ.” ([Google Research](https://research.google/blog/accelerating-code-migrations-with-ai/ "Accelerating code migrations with AI"))

### 4. Test generation and QA automation

Engineering teams use AI to generate unit tests, regression tests, mock data, edge cases, test plans, and Playwright/Cypress flows. Uber’s early tech-wide generative AI hackathon produced proofs of concept for automating coding, generating tests, improving code quality, and reducing operational load; 713 engineers participated and submitted 98 working demos. ([Uber](https://www.uber.com/us/en/blog/the-transformative-power-of-generative-ai/ "The Transformative Power of Generative AI in Software Development: Lessons from Uber’s Tech-Wide Hackathon"))

Testing is especially attractive because AI can draft broad coverage quickly, while deterministic test runners decide whether the thing actually works. That is the sweet spot: let the probabilistic goblin propose, let the deterministic machine judge.

### 5. Pull request review and code quality

AI code review is becoming a production workflow, not just a side panel in an IDE. Atlassian built Rovo Dev Code Reviewer as a human-in-the-loop AI reviewer for Bitbucket. After a year-long online evaluation across more than 1,900 repositories, Atlassian reported a 30.8% reduction in median PR cycle time, a 35.6% reduction in human-written review comments, and a 38.7% resolution rate for Rovo-generated comments that led to code changes. ([Atlassian](https://www.atlassian.com/blog/ai-at-work/developer-productivity-improved-with-rovo-dev "30.8% Faster PRs: How AI-Driven Rovo Dev Code Reviewer Improved the Developer Productivity at Atlassian - Work Life by Atlassian"))

The interesting design lesson from Atlassian is that they did not trust a single model blindly. Their system uses context from PRs and Jira issues, then filters hallucinated or factually incorrect comments with an LLM-as-judge step, then filters vague comments with a quality check. This is the adult version of AI adoption: context, filters, metrics, humans. Boring. Effective. ([Atlassian](https://www.atlassian.com/blog/ai-at-work/developer-productivity-improved-with-rovo-dev "30.8% Faster PRs: How AI-Driven Rovo Dev Code Reviewer Improved the Developer Productivity at Atlassian - Work Life by Atlassian"))

### 6. Documentation, requirements, and design docs

Teams are using AI to turn scattered notes into requirements, summarize RFCs, draft design docs, generate changelogs, explain APIs, create onboarding guides, and maintain internal docs. Uber’s hackathon identified requirements and design document creation, review, and risk assessment as one of the software development lifecycle areas where generative AI could help. ([Uber](https://www.uber.com/us/en/blog/the-transformative-power-of-generative-ai/ "The Transformative Power of Generative AI in Software Development: Lessons from Uber’s Tech-Wide Hackathon"))

This matters because code is only 16% of developers’ time in Atlassian’s framing; the rest is communication, context, docs, reviews, planning, coordination, and spelunking through organizational sediment. Atlassian’s 2025 DevEx report found that developers report top time-wasters as finding information, adapting new technology, and context switching. ([Atlassian](https://www.atlassian.com/blog/developer/developer-experience-report-2025 "Atlassian research: AI adoption is rising, but friction persists - Work Life by Atlassian"))

### 7. Security and vulnerability discovery

Security teams are using AI to generate fuzz targets, detect vulnerabilities, explain findings, propose patches, and triage security alerts. Google’s OSS-Fuzz reported 26 vulnerabilities found using AI-generated and AI-enhanced fuzz targets, including one in OpenSSL. That is a concrete defensive use case: AI expands the reach of testing rather than merely producing more code that security teams then have to chase with a broom. ([Google Online Security Blog](https://security.googleblog.com/2024/11/leveling-up-fuzzing-finding-more.html?utm_source=chatgpt.com "Leveling Up Fuzzing: Finding more vulnerabilities with AI"))

The risk side is obvious: faster code generation can create faster vulnerability generation. GitLab’s 2025 DevSecOps survey found that only 37% would trust AI to handle daily work tasks without human review, 73% had experienced problems with code created by “vibe coding,” and 70% said AI is making compliance management more challenging. The phrase “vibe coding” continues to sound like a misdemeanor committed in a coworking space, but the concern is real. ([about.gitlab.com](https://about.gitlab.com/press/releases/2025-11-10-gitlab-survey-reveals-the-ai-paradox/ "GitLab Survey Reveals the \"AI Paradox,\" Faster Coding Creates New Bottlenecks Requiring Platform Solutions"))

### 8. Incident response and SRE

AI is being used to summarize incidents, draft postmortems, cluster alerts, retrieve runbooks, suggest diagnostics, and eventually execute remediations under guardrails. PagerDuty launched an AI agent suite in 2025 for incident response, with agents intended to surface context, recommend diagnostics, and execute remediations. Datadog has used LLMs to combine incident metadata with Slack messages to help engineers draft incident postmortems. ([PagerDuty](https://www.pagerduty.com/newsroom/2025-fall-productlaunch/?utm_source=chatgpt.com "PagerDuty Launches Industry’s First End-to-End AI Agent Suite, Slashing ..."))

The useful boundary: AI can prepare evidence, summarize timelines, suggest likely causes, and automate low-risk checks. It should not replace the learning process after incidents. If teams automate away the hard thinking after failure, congratulations, they have invented a faster way to repeat outages.

### 9. Industrial, hardware, and manufacturing engineering

The pattern is not limited to software. Siemens’ Industrial Copilot lets industrial engineering teams generate programmable logic controller code using natural language and is positioned across design, planning, engineering, operations, and services. Siemens says this reduces repetitive workload and makes complex engineering tasks less error-prone. ([Siemens Press](https://press.siemens.com/global/en/pressrelease/bringing-generative-ai-industry-siemens-industrial-copilot-wins-hermes-award-2025 "Bringing Generative AI to Industry: Siemens Industrial Copilot wins Hermes Award 2025 | Press | Company | Siemens"))

BMW says it is scaling AI across development, production, purchasing, sales, and customer experience, including AI-supported simulations for crash testing, aerodynamics, and autonomous driving, plus AI quality monitoring in production lines. NVIDIA’s BMW case study says BMW uses synthetic data and no-code AI tools for manufacturing quality tasks, reducing the time for employees to develop and deploy AI models for their own QA tasks by two-thirds. ([BMW Group](https://www.bmwgroup.com/en/innovation/artificial-intelligence.html "Artificial Intelligence at BMW Group"))

NASA’s Goddard team has used AI-assisted design for bespoke mission hardware, including structural parts for the EXCITE telescope. NASA frames the use case as especially strong because it creates thousands of custom parts rather than mass-producing one repeated design. ([NASA](https://www.nasa.gov/technology/goddard-tech/nasa-turns-to-ai-to-design-mission-hardware/ "NASA Turns to AI to Design Mission Hardware - NASA"))

## 2. Real-world stories worth stealing from

Airbnb is the cleanest migration story: define the target, build validation gates, run per-file LLM transformations, retry with compiler/test/lint feedback, expand context up to huge prompts, measure failure modes, then manually finish the long tail. The lesson is not “LLMs are magic.” The lesson is “LLMs plus validation loops can compress miserable migration work.” ([Airbnb Tech](https://airbnb.tech/infrastructure/accelerating-large-scale-test-migration-with-llms/ "Accelerating Large-Scale Test Migration with LLMs | Airbnb Engineering & Data Science"))

Atlassian’s Rovo story is the best code-review pattern: use AI for first-pass review, ground it in PR and issue context, filter hallucinations, measure whether comments lead to code changes, and leave final judgment with humans. Their reported 30.8% PR-cycle reduction is less interesting than the architecture: AI is inserted into a workflow with accountability rather than sprayed randomly over developers like enterprise confetti. ([Atlassian](https://www.atlassian.com/blog/ai-at-work/developer-productivity-improved-with-rovo-dev "30.8% Faster PRs: How AI-Driven Rovo Dev Code Reviewer Improved the Developer Productivity at Atlassian - Work Life by Atlassian"))

Google’s internal migration work shows how AI fits into mature engineering infrastructure. The AI does not replace the monorepo tooling; it complements static analysis and large-scale change systems. That matters because the best AI engineering workflows are usually hybrids: symbolic tools find the target, LLMs draft the transformation, tests validate, humans review. ([Google Research](https://research.google/blog/accelerating-code-migrations-with-ai/ "Accelerating code migrations with AI"))

Duolingo’s GitHub case shows AI as part of developer-platform standardization. GitHub reports that Duolingo saw a 25% increase in developer speed with Copilot, a one-minute setup time for its largest repo with Codespaces, a 67% decrease in median code review turnaround time, and a 70% increase in pull requests. The story is not only Copilot; it is Copilot plus Codespaces plus standardized workflows and custom API integrations. ([GitHub](https://github.com/customer-stories/duolingo "Duolingo · GitHub"))

Block’s Goose story shows the agentic frontier: an internal agent that can run commands, access files, use tools, and help both engineers and non-engineers prototype. The useful lesson is also the cautionary one: Block used rollback-safe environments and human review because agents can damage things while being extremely confident about their little crimes. ([WIRED](https://www.wired.com/story/jack-dorseys-block-made-an-ai-agent-to-boost-its-own-productivity "Jack Dorsey's Block Made an AI Agent to Boost Its Own Productivity | WIRED"))

Uber’s story shows adoption as culture, not just tooling. In 2023, Uber used a tech-wide hackathon to explore code generation, tests, quality, docs, and operations use cases. By 2026, Uber’s CTO said 95% of engineers use AI monthly and an internal coding agent writes about 1,800 code changes per week, with engineers reviewing and approving. ([Uber](https://www.uber.com/us/en/blog/the-transformative-power-of-generative-ai/ "The Transformative Power of Generative AI in Software Development: Lessons from Uber’s Tech-Wide Hackathon"))

## 3. Where AI is working best

AI works best when the task has tight feedback loops: tests pass or fail, types compile or do not, lint rules trigger or not, PR comments are accepted or ignored, vulnerabilities reproduce or do not. This is why migrations, test generation, refactoring, boilerplate, code review suggestions, documentation drafts, and code search are strong fits.

It works less reliably when the task requires deep product judgment, ambiguous tradeoffs, security-sensitive changes, architecture ownership, or cross-team negotiation. Stack Overflow’s survey shows developers are much more resistant to using AI for high-responsibility systemic work: 76% do not plan to use AI for deployment and monitoring, and 69% do not plan to use it for project planning. Apparently engineers still prefer humans for the decisions that can ruin everyone’s weekend. Sensible. ([Stack Overflow](https://survey.stackoverflow.co/2025/ai/ "AI | 2025 Stack Overflow Developer Survey"))

The strongest teams are not asking, “Can AI write code?” They are asking, “Where can we surround AI with context, deterministic checks, ownership, and workflow integration?” That is the difference between useful automation and a code-shaped confetti cannon.

## 4. The productivity paradox

AI often saves individual time while failing to improve organizational throughput. Atlassian’s 2025 DevEx survey found that 99% of developers report saving time with AI tools, and 68% save more than 10 hours per week. But 50% still lose more than 10 hours per week to organizational inefficiencies, and 90% lose at least six hours. In short: AI gives developers time back, then the organization eats it. Nature is healing. ([Atlassian](https://www.atlassian.com/blog/developer/developer-experience-report-2025 "Atlassian research: AI adoption is rising, but friction persists - Work Life by Atlassian"))

GitLab found a similar “AI Paradox”: faster coding creates bottlenecks elsewhere. Its 2025 survey of 3,266 DevSecOps professionals found teams lose seven hours per person per week to inefficient processes, 60% use more than five software development tools, and 49% use more than five AI tools. Tool sprawl has learned to wear a little robot hat. ([about.gitlab.com](https://about.gitlab.com/press/releases/2025-11-10-gitlab-survey-reveals-the-ai-paradox/ "GitLab Survey Reveals the \"AI Paradox,\" Faster Coding Creates New Bottlenecks Requiring Platform Solutions"))

There is also hard evidence that AI does not always make experienced engineers faster. METR ran a randomized controlled trial with 16 experienced open-source developers doing 246 real tasks in mature repositories. Developers expected AI to speed them up, but in the study AI usage increased completion time by 19%. That does not disprove all AI productivity gains; it shows context matters, especially for complex, familiar codebases where prompting and verification can cost more than they save. ([metr.org](https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/?utm_source=chatgpt.com "Measuring the Impact of Early-2025 AI on Experienced Open-Source ..."))

## 5. What the best teams are doing differently

The best teams treat AI adoption as an engineering system, not a perk. They pick high-leverage workflows, define measurable outcomes, instrument usage and quality, and create guardrails. They do not merely buy licenses and hope morale becomes a KPI.

A strong AI engineering rollout usually has five parts:

First, choose workflows with feedback loops: migrations, tests, code review, docs, internal search, build fixes, vulnerability triage. Second, wire AI into existing developer surfaces: IDE, GitHub/GitLab/Bitbucket, Jira, CI, Slack, observability tools. Third, measure real outcomes: cycle time, PR size, review latency, test coverage, defect escape rate, rollback rate, incident MTTR, build success, developer satisfaction. Fourth, enforce review and provenance: AI-authored code must be reviewed, tested, scanned, and traceable. Fifth, train teams on when not to use AI, because apparently “the model sounded confident” is not a release criterion.

The most mature pattern is “AI drafts, systems verify, humans decide.” Google’s migration work, Airbnb’s migration pipeline, and Atlassian’s Rovo reviewer all follow this shape: LLMs generate candidate changes, automated validation filters them, and engineers own acceptance. ([Google Research](https://research.google/blog/accelerating-code-migrations-with-ai/ "Accelerating code migrations with AI"))

## 6. Practical use-case map

For coding-heavy teams, start with boilerplate generation, unit-test generation, bug-fix drafts, code explanation, and documentation. These are low-friction and usually do not require deep organizational redesign.

For platform teams, prioritize migrations, dependency upgrades, service template generation, golden-path scaffolding, internal developer portal search, and CI failure diagnosis. This is where AI can reduce toil across many teams.

For security teams, use AI for fuzz target generation, vulnerability explanation, secure-code suggestions, threat-model drafts, and alert triage. Keep human approval for fixes and policy decisions.

For SRE teams, use AI for incident summaries, timeline reconstruction, runbook retrieval, alert clustering, log-query suggestions, and postmortem drafts. Be extremely cautious with autonomous remediation until there are strong rollback and blast-radius controls.

For hardware, manufacturing, and industrial teams, the mature use cases are simulation acceleration, generative design, PLC-code assistance, manufacturing QA, synthetic data generation, and predictive maintenance. Siemens, BMW, and NASA show this is already real outside the software bubble. ([Siemens Press](https://press.siemens.com/global/en/pressrelease/bringing-generative-ai-industry-siemens-industrial-copilot-wins-hermes-award-2025 "Bringing Generative AI to Industry: Siemens Industrial Copilot wins Hermes Award 2025 | Press | Company | Siemens"))

## 7. Risks leaders keep underestimating

The first risk is false productivity. A developer may feel faster while the team ships no faster because review, QA, security, deployment, or cross-team coordination becomes the bottleneck. Both Atlassian and GitLab’s surveys point directly at this problem. ([Atlassian](https://www.atlassian.com/blog/developer/developer-experience-report-2025 "Atlassian research: AI adoption is rising, but friction persists - Work Life by Atlassian"))

The second risk is quality drift. AI can generate plausible code that passes shallow tests but violates architecture, security assumptions, or maintainability norms. Stack Overflow’s trust data is a nice cold shower here: distrust is rising even as usage rises. ([Stack Overflow](https://survey.stackoverflow.co/2025/ai/ "AI | 2025 Stack Overflow Developer Survey"))

The third risk is tool sprawl. Teams adopt Copilot, Cursor, Claude Code, internal agents, code review bots, doc assistants, observability agents, and security agents, then wonder why nobody can explain the workflow. The machines did not create chaos; they merely joined it.

The fourth risk is junior-skill erosion. If early-career engineers outsource too much implementation and debugging, they may lose the slow, painful learning path that creates judgment. AI can be a tutor, but only if teams make engineers explain, test, and review the generated work.

The fifth risk is governance theatre. Tracking AI usage alone is not the same as measuring impact. “Number of prompts” is not productivity, in much the same way “number of meetings” is not strategy, despite the brave lies calendars tell.

## 8. Bottom line

Engineering teams are using AI in three increasingly mature layers.

Layer one is personal productivity: autocomplete, chat, code explanation, tests, docs, and small fixes. This is now mainstream.

Layer two is workflow automation: PR review, CI repair, migrations, security triage, incident summaries, and internal knowledge search. This is where serious productivity gains begin.

Layer three is agentic engineering: AI agents that plan, modify files, run commands, open PRs, and coordinate with other tools while humans review. This is emerging quickly, but it demands strong sandboxing, observability, permissions, rollback, and review.

The best evidence does not support the lazy claim that AI simply “replaces engineers.” It supports a more annoying, more realistic conclusion: engineering work is being reorganized. Engineers are moving from typing every line toward specifying intent, curating context, reviewing machine output, designing systems, maintaining guardrails, and owning quality. The keyboard is less sacred now. The judgment is more important than ever.