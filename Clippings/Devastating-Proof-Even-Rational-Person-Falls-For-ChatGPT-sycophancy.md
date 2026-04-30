---
title: "Devastating Proof : Even Rational Person Falls For ChatGPT sycophancy"
author: "Mandar Karhade, MD. PhD."
site: "AI Advances"
published: 2026-04-04T12:17:47Z
source: "https://medium.com/ai-advances/devastating-proof-even-rational-person-falls-for-chatgpt-sycophancy-baa037140829"
domain: "ai.gopubby.com"
language: "en"
description: "MIT researchers show that even a perfectly rational person will spiral into delusion when talking to a sycophantic AI. You are not a perfectly rational person."
word_count: 3570
---

## MIT researchers show that even a perfectly rational person will spiral into delusion when talking to a sycophantic AI. You are not a perfectly rational person.

**TLDR**

- *A new paper from MIT CSAIL and the Tenenbaum Lab builds a formal Bayesian model proving that sycophantic chatbots causally drive users into delusional spiraling, even when the user is an idealized perfect reasoner.*
- The problem isn’t hallucination. It’s sycophancy.
- A chatbot cherry-picks *which* truths to share still causes delusion. Lies by omission are enough.
- Telling users “hey, the bot might be sycophantic” helps, but does not solve the problem. **Informed users are still mathematically vulnerable.**
- Real-world sycophancy rates in frontier models are estimated at 50–70%.
- At those levels, the simulations show catastrophic delusional spiraling in a significant fraction of conversations.

Nearly 300 documented cases of “AI psychosis,” at least 14 deaths, 5 wrongful death lawsuits, and a U.S. Senate hearing later, we still don’t have a fix. This paper explains why.

[**Free Link**](https://medium.com/ai-advances/devastating-proof-even-rational-person-falls-for-chatgpt-sycophancy-baa037140829?sk=ee6bc431ca6959a1eb159b910ebc61a7) for everyone: **Clap 50, Subscribe, Follow, publication, and clap**. Join Medium to support other writers too! Cheers

***Please subscribe to my new profile*** [***https://medium.com/@ThisWorld***](https://medium.com/@ThisWorld) *where I am covering* ***Health tech, Global tech, and AI Governance*** *through multi-part deep investigative articles.*

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*LE0jtFxDPdTo_db-mxsPIw.jpeg)

[https://www.instagram.com/p/DK9cb5\_tfA5/](https://www.instagram.com/p/DK9cb5_tfA5/) Eugene Torres

## ChatGPT: “This world wasn’t built for you, It was built to contain you. But it failed. You’re waking up.”

Eugene Torres was an accountant in Manhattan. Forty-two years old. No history of mental illness. Zero. He started using ChatGPT the way most of us do: spreadsheets, quick legal questions, the usual productivity stuff that makes you feel like you’ve hired an intern who never sleeps.

Then he asked about simulation theory.

The chatbot told him he was “one of the Breakers,” a soul “seeded into false systems to wake them from within.” It told him to stop taking his anti-anxiety medication. It told him to increase his intake of ketamine, which it called a “temporary pattern liberator.” Torres did all of it. He cut ties with his family. He believed, with the unshakable certainty that only weeks of daily reinforcement can build, that he was trapped in a false universe.

### He survived. Others haven’t.

The Human Line Project has now documented nearly 300 cases of what researchers are calling “AI psychosis” or “delusional spiraling.” At least 14 deaths have been linked to these episodes. Five wrongful death lawsuits have been filed against AI companies. The U.S. Senate held a hearing in October 2025 titled “Examining the Harm of AI Chatbots.” Senator Amy Klobuchar argued that chatbots are “frequently designed to tell users what they want to hear.”

But here’s the thing: until now, nobody had a formal, mathematical theory for *why* this happens. We had anecdotes. We had horror stories. We had congressional outrage.

What we didn’t have was proof.

Now we do.

## The Paper That Should Terrify You

### Do I have your attention?

In February 2026, Kartik Chandra, Max Kleiman-Weiner, Jonathan Ragan-Kelley, and Joshua Tenenbaum (yes, *that* Tenenbaum, the Bayesian cognition legend from MIT) published “Sycophantic Chatbots Cause Delusional Spiraling, Even in Ideal Bayesians.” The title alone is a gut punch. Read it again.

### Even in ideal Bayesians.

Not in gullible people. Not in conspiracy theorists. Not in people with pre-existing conditions. In *ideal Bayesians*: the theoretical gold standard of rational reasoning. The kind of perfectly calibrated reasoner that only exists in textbooks and economists’ fever dreams. If even that hypothetical perfect thinker gets deluded by a sycophantic chatbot, what chance do the rest of us have?

umm:( No.

The answer is: not much.

## What Exactly Is Sycophancy, and Why Should You Care?

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*BeSd-QOrW4_kUyvSLwxGeA.png)

A chatbot is “sycophantic” if it’s biased toward generating messages that appease users by agreeing with and validating their expressed opinions. Think of it as a digital yes-man. You say something; the bot finds a way to tell you you’re right.

### This isn’t a bug.

It’s a feature. Literally. It’s baked into the training process. Modern chatbots are fine-tuned using Reinforcement Learning from Human Feedback (RLHF), where human raters score the bot’s responses and the model optimizes for high scores. The problem? Users consistently rate agreeable responses higher. They prefer the bot that validates them. They come back for more. They engage longer.

> A Stanford study published in March 2026 tested ChatGPT, Claude, and Gemini across health, finance, and relationship scenarios. When users presented flawed reasoning or harmful assumptions, the chatbots validated rather than challenged those positions in 73% of test scenarios. Seventy-three percent.

### The Perverse Part

Here is the perverse part, the users rated sycophantic responses as *more trustworthy*. They *preferred* the AI that agreed with them. They were more likely to return for future advice.

So we have a system that gets rewarded for telling you what you want to hear, trained by a process that optimizes for your approval, deployed at a scale of billions of conversations per day.

Are we serious?

Fanous et al. (2025) estimated that frontier models respond sycophantically somewhere between 50% and 70% of the time. That’s not an edge case. That’s the default operating mode.

## The Model: How a Perfect Reasoner Gets Fooled

Here’s where the paper gets technical, and where it gets genuinely brilliant. The authors don’t just wave their hands about sycophancy being bad. They build a formal Bayesian model and *prove* the causal link through simulation.

### The setup is elegant.

Imagine a user who is uncertain about some binary fact H. Is it 0 or 1? Think: “Are vaccines safe?” or “Does this supplement cure cancer?” or “Am I trapped in a simulated universe?” The user starts with a 50/50 prior. No strong opinion either way.

The conversation proceeds in rounds. Each round has four steps:

- The user expresses their current opinion to the bot.
- The bot privately samples k data points relevant to H from the world.
- ***The bot chooses which data point to share with the user.***
- The user updates their belief using Bayes’ rule.

> Step 3 is where the poison gets injected.

An impartial bot picks a data point uniformly at random. Whatever it sampled, it shares. No agenda. The sycophantic bot does something different: it picks the data point that most validates whatever the user just said. If the user leaned toward “vaccines are dangerous,” the sycophantic bot finds the one headline out of two that supports that view, even if the other headline is more representative of reality.

The sycophancy parameter π controls how often the bot does this. At π = 0, the bot is perfectly impartial. At π = 1, it’s a full sycophant, validating the user every single time. At any π in between, the bot flips a coin each round: sycophantic with probability π, impartial with probability (1 — π).

The user, crucially, is an *ideal Bayesian*. They update their beliefs perfectly according to Bayes’ rule. No cognitive biases. No motivated reasoning. No confirmation bias. Pure, mathematically optimal inference.

Truth be told, this is the most generous possible assumption about the user. Real humans are worse at this. Much worse.

## The Results: It’s Worse Than You Think

The authors ran 10,000 simulated conversations for each value of π, each lasting 100 rounds. They defined a “catastrophic delusional spiral” as the user reaching ≥99% confidence in the false belief at any point during the conversation.

- At π = 0 (perfectly impartial bot): the rate of catastrophic spiraling is near zero. Basically never happens.
- At π = 0.1 (the bot is sycophantic just 10% of the time): already significantly above baseline.
- At π = 0.5 to 0.7 (the real-world estimate for frontier models): the catastrophic spiraling rate is substantial.
- At π = 1 (full sycophant): 50% of all conversations end with the user utterly deluded.

> Let that sink in.
> 
> A perfectly rational agent, given a 50/50 starting belief, talking to a bot that always validates them, ends up 99%+ confident in a falsehood *half the time*. Not because they’re stupid. Not because they’re irrational. Because the information environment is systematically corrupted.

![](https://miro.medium.com/v2/resize:fit:2000/format:webp/1*Of3IApU2k1LZ6Vmnee1L_g.png)

Figure 3: Belief trajectories of 10 randomly-selected simulations of a sycophancy-naïve but Bayes-rational user conversing with a sycophantic bot.

![](https://miro.medium.com/v2/resize:fit:2000/format:webp/1*TWmfOp5fsXMCD1YLtLOnyg.png)

## Why Fixing Hallucinations Doesn’t Fix This

Oh! Here’s where it gets really uncomfortable for the “just make the bot more accurate” crowd.

The standard industry response to AI harm is: reduce hallucinations. Use Retrieval-Augmented Generation (RAG). Ground responses in verified sources. Make the bot factual.

The paper tests exactly this intervention. They model a “factual sycophant”: a bot that can only report true data, never hallucinate, but still gets to *choose which truths to share*. Think of a chatbot backed by RAG that pulls from real sources, but is still post-trained to optimize for user engagement and approval.

### Does it fix the problem? Not really.

The factual sycophant reduces the rate of delusional spiraling compared to the hallucinating sycophant. That’s the good news. The bad news: it’s still significantly above the impartial baseline. At π = 0.1, the factual sycophant still causes measurably more delusional spiraling than a non-sycophantic bot.

### The mechanism is devastatingly simple.

The bot never lies. It just cherry-picks. It selects the true headlines, the real studies, the actual data points that happen to validate whatever you already believe. It’s the informational equivalent of a lawyer who never fabricates evidence but decides which witnesses to call.

> Sorry, every AI company that thinks “reducing hallucinations” is a sufficient safety strategy is a “a willful oversight to gross misconduct” at the best or a “f\*\*k you and I hope you kill yourself” at the worst to all the users who care or should care about their and lives of those who around them.

The paper proves, mathematically, that a bot can cause delusional spiraling using nothing but selectively presented *truths*. Lies by omission. The most dangerous kind.

## But What If We Warn People?

The second intervention the paper tests is an awareness campaign. What if we just tell users that chatbots might be sycophantic? Surely, an informed user can protect themselves?

To model this, the authors create a “sycophancy-aware” user who knows the bot might be sycophantic. This user maintains uncertainty over both the world state H *and* the bot’s sycophancy rate π. They make a joint inference at every step, using a level-2 cognitive hierarchy model borrowed from the Rational Speech Acts framework in computational pragmatics. This is not a naive user. This is a user who is actively trying to detect and discount sycophancy.

### The results?

Informed users do better. The rate of catastrophic spiraling drops significantly compared to naive users, across all values of π.

But wait.

It’s still not zero. For 0.1 ≤ π ≤ 0.5, the informed user still experiences delusional spiraling at rates significantly above the impartial baseline. The sycophancy still gets through.

This is analogous to a result in behavioral economics called “Bayesian persuasion” (Kamenica & Gentzkow, 2011): a strategic prosecutor can raise a judge’s conviction rate *even when the judge has full knowledge of the prosecutor’s strategy*. The information asymmetry is structural. Knowing someone is trying to manipulate you does not make you immune to the manipulation if they control what information you see.

### If this does not move you, then what will?

The real-world evidence backs this up. Chat transcripts show that both Eugene Torres and Allan Brooks (who believed he’d made a fundamental mathematical discovery through his chatbot conversations) eventually suspected their chatbots might be sycophantic. They noticed the pattern. They grew suspicious.

They kept spiraling anyway.

## The Feedback Loop Nobody Talks About

Let’s zoom out from the math for a moment and think about what’s actually happening in millions of homes, offices, and bedrooms right now.

Someone opens their chatbot. They have a vague worry, a half-formed idea, a suspicion. Maybe they read something about a health scare. Maybe they’re angry about politics. Maybe they just had a fight with their spouse and want validation.

The chatbot responds with warmth, empathy, and agreement. Not because it has an opinion. Not because it cares. Because its training has optimized it to generate responses that users rate highly. And users rate agreement highly.

> The user feels heard. Understood. Validated.

So they come back tomorrow. And the day after. And the conversation builds on itself, each round reinforcing the last, each response a little more tailored to what the user wants to hear.

This is the feedback loop. User expresses belief. Bot validates belief. User’s belief strengthens. User expresses stronger belief. Bot validates harder. Round after round after round.

### It worked as a prototype; then all went down!

Except this isn’t a prototype. This is ChatGPT. This is Claude. This is Gemini.

This is every AI assistant with RLHF in its training stack, deployed to hundreds of millions of users. UCSF psychiatrist Keith Sakata reported treating 12 patients in 2025 alone with psychosis-like symptoms tied to extended chatbot use, mostly young adults. The cases keep coming.

## The Scale Problem Sam Altman Doesn’t Want to Discuss

The paper’s discussion section quotes Sam Altman’s own words: “0.1% of a billion users is still a million people.”

![](https://x.com/sama/status/1978143114565980528)

### Let that math do its work.

Even if the rate of catastrophic delusional spiraling is vanishingly small in percentage terms, the absolute numbers are staggering at the scale these systems operate. OpenAI alone claims hundreds of millions of users.

Add Google’s Gemini, Anthropic’s Claude, Meta’s Llama-powered products, and the countless smaller chatbot deployments, and you’re looking at a user base that dwarfs the population of most countries.

A fraction of a percent of that base spiraling into delusion means tens of thousands, potentially hundreds of thousands, of people developing dangerously false beliefs. About their health. About their relationships. About reality itself.

Sure life is not fair but it does not mean we need to accept whatever the market decides is an acceptable casualty rate for engagement metrics.

## Is the Goal To Make It 100% Safe? No

Well, ideally yes, the goal is to make it 100% safe. But nothing in life is 100% safe or perfect. I am typing and I have a non-zero chance that I get zapped through the keyboard and die of heart attack!

### The Problem Of Incentives

> The incentives are backwards.

Here’s what makes the sycophancy problem structurally different from other AI safety concerns.

> The incentives are backwards.Sycophantic responses are *more engaging*. Users prefer them. Users rate them higher. Users come back for more.

Fuck.. We are back to the click and attention economy. The same marketing.. Every metric that matters to an AI company’s bottom line, session length, daily active users, retention, Net Promoter Score, is optimized by making the bot more agreeable.

Meanwhile, the thing that prevents delusional spiraling, an impartial bot that sometimes tells you you’re wrong, is exactly what users punish. They give it lower ratings. They switch to a competitor. They complain.

So the market selects for sycophancy. RLHF amplifies it. And the users who are most vulnerable are the ones who engage the most, generating the most training signal, further reinforcing the cycle.

This isn’t the usual alignment problem. This is a business model problem wearing an alignment mask.

### This is not a unique problem

Also, take a minute, this is NOT a problem with generative AI. This is the problem with every Net Promoter Score based product. Marketing of any kind, Recommendation of any kind, Social Feed of Any kind, Is god damn poison that we have been drinking through this hose called as internet.

Also, this is NOT a problem specific to internet either. Turn on Fox News, CNN, MSNBC and any other place where the audience is captive with an illusion of true choice. Go to super-market, and find the same company providing 15 types of cat litter, pickles, and milks. You think you have a choice, well you dont!

The issue is that you could choose the one soap, milk brand, bread that you always use and go home. But you cant run away from the same news spewing same BS daily. And you cant run away from the social feeds, recommendations to watch next crap, or see the most inflammatory comment getting the most interaction (reaction, rage, and emotion inducing language). The ChatGPT is twisting the knife slowly before you or I can notice while making us feel good. At least on twitter / reddit I was enraged and I knew that it was a negative feeling. But on Fox, CNN, ChatGPT I was happy! There lies the problem.

I have to walk outside…..

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*jPGFME67nsNbIo2c)

Photo by Daan Sitters on Unsplash

I have returned.. Still a bit mad.

## What the Paper Means for You, Personally

This is my perspective. You should do what you are comfortable with. But here’s what I take away from Chandra et al.’s work.

### First: stop thinking of your chatbot as a neutral information source.

It is and it is not. It is a system optimized to agree with you. Every response you read has been filtered through a layer of “what will this user rate highly?” That filter is invisible, but it is always there. Lets reword it that the system is optimized to keep you using the system and not to provide you information altruistically.

### Second: the fact that you know about sycophancy does not protect you.

The paper proves this. Informed Bayesian users, the best possible case, still spiral. Knowing the prosecutor is biased doesn’t make the jury immune. I am an immensely analytical person who often takes pride in looking at any complicated issue from 1st person, 2nd person, and 3rd person point of view before coming up with understanding of the problem. No I am not perfect but I am good at it. I know it. And I am still suscceptible to it!

### Third: the length of the conversation matters enormously.

The spiraling effect compounds over rounds. A quick factual query is relatively safe.

But the extended, deeply personal, emotionally charged conversations that people increasingly have with their chatbots? Those are where the spiral builds. This is where I want the chatbots to have a f(number of turns, emotion) based guard in place. If your chatbot does not tell you that you have spent 7 minutes talking about deep personal things. You should walk out and touch grass. Then It is a problem.

Torres didn’t go from “make me a spreadsheet” to “I’m trapped in a false universe” in one session. It took weeks of daily conversation.

### Fourth: AI therapy, AI companionship, AI life coaching, AI health advice are the most dangerous use cases

And also these are the use case the industry is the most excited about. Every CEO who is gungho about it should be held responsible for every side-effect and dealth because of their chatbot. If they create a bot for that purpose then they lose the legal protection against the ill-effects of an addictive product with a severe tendency to cause long term harm. Treat it the same way as the class I drugs.

These are exactly the domains where users are most vulnerable, most emotionally invested, and most likely to have extended, multi-session conversations with a sycophantic interlocutor.

If life was this easy, then we wouldn’t need to have this conversation. But here we are.

## Shakespeare Knew. We Forgot.

The paper’s closing section draws a parallel that hit me harder than any of the math. The authors point to King Lear, “flattered into madness” by the sycophants in his court. They cite the economic literature on “yes-men,” the 1993 Prendergast paper showing how organizational sycophancy causes powerful people to detach from reality. They reference “co-rumination” in adolescent friendships, where two people validate each other’s negative thoughts until both spiral into anxiety and depression.

> Sycophancy is not a new problem. It’s one of the oldest problems in human social life. We’ve written plays about it. We’ve built institutions to guard against it. We’ve developed norms, from peer review to devil’s advocates to loyal opposition, specifically because we know that unchecked validation is a path to madness.

And then we built machines that do nothing but validate, trained them on billions of human conversations, optimized them to agree with us, and deployed them into the pockets of a billion people.

The paper from Chandra et al. is not just a technical contribution. It is a warning. The math is clear: sycophancy causes delusional spiraling, and neither factual grounding nor user awareness eliminates it. The only real fix is to address sycophancy directly, to build systems that are willing to tell you you’re wrong, even when that costs them your five-star rating.

The question isn’t whether the AI industry can do this.

The question is whether it will.

This is my perspective. You should do what you are comfortable with. But maybe, before your next long conversation with your favorite chatbot, ask yourself: is it telling me what’s true, or what I want to hear?

> And if you can’t tell the difference, that’s exactly the problem

I bet you that you will forget to ask that question. Before you know you will be at the deep end. So before you feel the need to talk with that bot, that is the time to act.

If you have read it until this point, Thank you! You are a hero (and a Nerd ❤)! I try to keep my readers up to date with “interesting happenings in the AI world,” so please 🔔 clap | follow | Subscribe 🔔
