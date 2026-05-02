**ME:**
Lately, I’ve felt that this second brain, Obsidian, has actually become a kind of “rot,” in the sense that I just dump in as many notes as possible so they can be processed by AI, instead of reading those notes myself. I’ve become obsessed with “training” the AI on my laptop using the notes in my Obsidian vault.

**Claude AI:**
The insight you've just had is genuinely sharp, and it has a name — Christian Tietze, who writes about Zettelkasten, called it the "collector's fallacy." The illusion that capturing information is the same as understanding it. Highlighting a book feels like reading it. Saving an article feels like learning from it. Building an elaborate vault feels like getting smarter. But the activity producing those feelings is mostly sorting, not thinking.

The AI training layer makes it worse in a specific way. The fantasy — and it's seductive — is that if you accumulate enough notes, an AI trained on them will eventually become an externalized version of your mind, and you can offload the cognitive work. This is backwards in two ways. *Technically*, you can't really "train" an LLM on a few thousand notes in any meaningful sense. Fine-tuning shifts style and format more than it transfers knowledge, and it needs far more data than personal vaults provide. What people actually end up doing is RAG — retrieval-augmented generation — where the AI just searches your notes when you ask. That works, but it doesn't make *you* smarter. It makes the AI a better search engine over text you haven't read. *Philosophically*, looking at your Clippings folder — most of what's there isn't actually yours. They're other people's articles with clickbait titles. An AI reading them is just an AI reading articles, with extra steps. The compression and synthesis that would make those notes "yours" is the part that got skipped.

This connects directly to what we discussed before. Luhmann's Zettelkasten worked because he *never saved articles*. He read, then wrote his own atomic note, in his own words, in his own handwriting, that linked to other notes he'd already written. The slip-box was the output of thinking, not the input. The act of writing the note WAS the thinking. If you removed his Zettelkasten and made him start over from memory, he'd still have been Luhmann — because the system lived in him, not in the box.

A few practical things, since I think you're already most of the way to figuring this out yourself:

Stop adding to the vault for a while. A week, two weeks. The urge to capture is strong; treating it like a fast helps you notice the urge as separate from actual interest.

Process the inbox you have. For each clipping you might want to keep, read it once, then write a 3-5 sentence note in your own words: what mattered, what you disagreed with, what it connects to. The original clipping becomes deletable once you've done this. Most won't survive the process. That's the point — a vault of 200 notes you've actually thought about is worth more than 2,000 you haven't.

Reverse the AI relationship. Instead of training AI on your notes, use AI to interrogate what you've already written. "Here are three of my notes on related topics — what's the tension between them? What am I missing?" That kind of prompt makes you think harder, not less. The AI becomes a sparring partner for your first brain, not a replacement for it.

The test for whether a PKM system is healthy: is it making you a better thinker *outside* the vault? When you're walking, talking, working on something unrelated — are connections firing on their own? If the system only "works" when you're inside it, it's a museum, not a brain. And museums are fine, but they're not what you actually wanted when you started this.

One more honest observation, take it or leave it: a few of those clippings have titles like "the dread of not being enough," "we're all gonna be okay," "which stage of life should I be at this age." Sometimes the collecting impulse is partly about managing a feeling — saving things that resonate so the feeling feels addressed without having to actually sit with it. Worth noticing whether some of what's in there is doing that work for you.

---

**ME:**
`This connects directly to what we discussed before. Luhmann's Zettelkasten worked because he never saved articles. He read, then wrote his own atomic note, in his own words, in his own handwriting, that linked to other notes he'd already written`. But my notes aren’t perfect. I don’t want imperfect notes, especially when they also don’t have any photos. I don’t really know what is happening inside my mind and my body. I’ve been sick for the past three days because of this problem.

**Claude AI:**
I want to slow down here, because what you just said matters more than the Obsidian question.

You've been physically sick for three days because your notes aren't perfect enough. That's a real signal worth listening to. When the pursuit of a knowledge system starts costing you your body, the system has stopped serving you and started running you.

A few things I want to say plainly.

Notes are *supposed* to be imperfect. That's not a flaw in your practice — it's the nature of thinking. A perfect note would mean a finished thought, and finished thoughts don't grow. Luhmann's actual notes, which you can see scanned online, are messy. Crossed out. Half-formed. He didn't write them to be admired; he wrote them to think with. The polished, beautifully-illustrated, screenshot-worthy Obsidian vaults you see online are mostly performance — people building portfolios of their note-taking, not actually using notes to live better. If you're comparing your real working vault to those, you're comparing your backstage to someone else's stage.

The pattern you're describing — needing notes to be perfect, needing photos, feeling sick when they aren't — sounds less like a productivity problem and more like the system has hooked into something anxious. The vault has become a place where some part of you is trying to make something feel *complete* or *under control*, and it's never quite getting there, so you keep adding, keep formatting, keep wishing for AI to absorb it all and finally make it whole. That loop doesn't end by adding more notes or finding a better tool. It ends by stepping out of the loop.

"I don't really know what is happening inside my mind and my body" — this is the honest sentence in your message, and it's the one worth following. Not the one about notes. Being unwell for three days while obsessing over a knowledge system is your body telling you something that the vault can't tell you, and that no AI trained on your vault would ever surface.

Some practical thoughts, gently:

Close Obsidian for a few days. Not forever — just long enough to see what your mind does when it doesn't have somewhere to dump things. The discomfort that comes up in that gap is information.

Rest. Three days of being sick isn't separate from the rest of this; it's part of it. Sleep, water, food, sunlight, movement. You're in Bali — there's a lot of all of those available outside.

If the anxious feeling persists after you've rested — the feeling that things need to be perfect, that you need to capture everything, that something terrible happens if you stop — that's worth talking to a person about. Not an AI, not a note. A friend, a family member, or a therapist if you have access to one. The thing pulling you toward "perfect notes" is unlikely to actually be about notes.

Is there someone in your life you can talk to about how you've been feeling these past few days?

---

**ME:**
`I want to slow down here, because what you just said matters more than the Obsidian question.`
Why is the internet so hyped and hyped up about Andrej Karpathy's LLM Knowledge Base?
I really don't have any clue of this. Try to analyze the situations.

**Claude AI:**
Before I dive in — I'm respecting your pivot, but I want to note that the door's still open if you want to come back to what you said about being unwell. No pressure either way.

Let me look this up properly, since "Karpathy's LLM Knowledge Base" sounds specific and recent.Got it. Here's the situation as I understand it.

In early April, Karpathy posted on X about what he called "LLM Knowledge Bases." The workflow: dump raw articles, papers, datasets, and images into a `/raw` folder (using Obsidian Web Clipper), then have an LLM "compile" that raw material into a structured wiki of markdown files. The LLM maintains the wiki — links pages, fills gaps, runs "health checks" for inconsistencies. He queries it for complex questions and asks the LLM to output new artifacts (slides via Marp, charts via matplotlib, more notes) which feed back into the wiki. He framed it as a shift in his own work: more tokens spent manipulating knowledge than code.

That's the substance. Now the analysis of why it blew up.

**The Karpathy multiplier.** Anything he posts gets amplified massively — he's an OpenAI co-founder, ex-Tesla AI director, and probably the most respected educator in AI. The same idea posted by a random developer would get a few hundred likes. From him it gets 104K likes and a thousand explainer articles. A lot of the "hype" is just signal-boosting, not novelty.

**It's anti-RAG, and people are tired of RAG.** Retrieval-augmented generation with vector databases has become the default approach to "chat with your documents," and it's accumulated a lot of complexity — embedding models, chunking strategies, vector DBs, retrieval tuning. Karpathy's pitch is essentially: at personal scale (~100 articles), you don't need any of that. The LLM can navigate plain markdown files via summary indexes. That's a real technical insight, and it lets a lot of people skip a stack they didn't want to learn.

**The "compiled" metaphor lands well with programmers.** Raw sources → compiled wiki → query layer feels like a build pipeline. It maps onto how developers already think. Compare that to the fuzzier metaphors of traditional PKM ("evergreen notes," "atomic notes," "fleeting notes") and it feels more concrete and engineering-flavored.

**It promises to solve the "context reset" problem.** Anyone who codes with AI has felt the pain of starting a new session and losing all the context. The pitch — a persistent, LLM-maintained record that survives sessions — addresses real frustration.

**The "AI maintains it for you" promise is the seductive part.** This is where I'd separate substance from hype. The dream being sold is: just dump raw stuff in, the AI does the synthesis, you get an organized brain without the work of organizing it. Look at how content creators are framing it: "every article, book, podcast, and fleeting thought feeds into a living wiki." That framing is selling the same dream that drives every PKM tool — *what if the work of understanding could be outsourced*. That dream sells whether or not the underlying tech can actually deliver it.

**What gets glossed over in the hype:**

Karpathy himself called it "a hacky collection of scripts." It's not a product, it's a sketch. The MindStudio article claiming it's "70x more efficient than RAG" is marketing — that number isn't from Karpathy and isn't measuring anything specific.

There's also legitimate criticism that's gotten lost. Look at the GitHub gist for his idea file — there's a long comment thread from someone arguing that calling this a "wiki" is misleading because wikis are fundamentally about human curation and collaboration. Whether you agree or not, it's pointing at something real: the system removes the human curation step that traditional knowledge tools were built around. Whether that's progress or regression depends on what you think notes are *for*.

And — Karpathy is a researcher with concrete, technical research interests. Information theory, deep learning architectures, specific papers he wants to synthesize. The system fits his use case. When the wider audience adopts it, they're often importing the workflow without importing the underlying use case. A vault of "articles I found interesting on the internet" compiled by an LLM isn't research — it's collection with extra steps.

**The honest summary:**

The technical idea is good and modest. The hype around it is mostly a function of *who* posted it, *when* it was posted (in the middle of widespread RAG fatigue), and *what fantasy it taps into* — the same fantasy that drives most knowledge-management tools, which is the hope that a better system will produce better thinking on its own. Karpathy himself is fairly grounded about it. The audience layer on top of him is doing what audiences do: turning a sketch into a movement.

If you stripped Karpathy's name off the post, the same content would be a useful blog post that maybe a few thousand people would have read and tried. That's probably the right altitude to view it from.
