---
title: "Do chess players know when to think (and when to just move)?"
source: "https://sciencespectrumu.com/do-chess-players-know-when-to-think-and-when-to-just-move-e56c80a7765e"
author:
  - "[[Bjbalas]]"
published: 2026-04-24
created: 2026-04-27
description: "Do chess players know when to think (and when to just move)? Some positions deserve a lot of thought and some don’t — but do players know which is which? There are always moments during a …"
tags:
  - "clippings"
---
## [Science Spectrum](https://sciencespectrumu.com/?source=post_page---publication_nav-9a1ae4e15408-e56c80a7765e---------------------------------------)

[![Science Spectrum](https://miro.medium.com/v2/resize:fill:76:76/1*GaJKIwMbuGzom2KJzJESFw.png)](https://sciencespectrumu.com/?source=post_page---post_publication_sidebar-9a1ae4e15408-e56c80a7765e---------------------------------------)

Science Spectrum is here to guide you on your personal path to understanding the fascinating world of science, mathematics, and related topics. Our goal is to make complex concepts accessible to everyone. We are happy to be a member of the Medium Boost family!

## Some positions deserve a lot of thought and some don’t — but do players know which is which?

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*2CWJW1fPOAZdU3nqeJ2JeQ.jpeg)

Image credit: Photo by Ralph Hutter on Unsplash

There are always moments during a top-level Classical tournament that I find striking. Sometimes it’s a brilliant move I know I’d never imagine making, other times it’s a blunder I know I **absolutely** could have made, and occasionally it’s a turn of events on or away from the board that’s some combination of funny, puzzling, and unique to playing chess competitively.

During the 2026 Candidates Tournament, the moment that stood out the most to me wasn’t actually a moment, though — it was a LOT of moments! Specifically, it was [Hikaru Nakamura thinking for just under 68 minutes during his Round 5 game with Javokhir Sindarov.](https://www.hola.com/us/entertainment/20260407893980/hikaru-nakamura-67-minute-chess-move-loss/) Besides living up to the jokes my wife usually makes when I’m watching live coverage of a tournament (”Did one of them shift in his seat? Did he start to reach for something??”) I can’t help but find this remarkable from a cognitive perspective. Partly this is because my own calculation abilities are very limited, so seeing a player spend so much time on a single move hints at how much more recall and computation they’re capable of. Even if Hikaru [ended up making a mistake after that deep think](https://www.reddit.com/r/chess/comments/1sbfnv2/67_minutes_44_seconds_hikarus_13th_move_today_was/), it’s still apparent that he’s got much more at his disposal than I do in terms of working memory, possibly visual imagery, and visuospatial processing.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*dJ2HRYXQ5WZFKv_kAhnqpw.jpeg)

Hikaru considering his options in a game against Magnus Carlsen (Sorry — no permission to use images from the Candidates!) Stefan64, CC BY-SA 3.0 < https://creativecommons.org/licenses/by-sa/3.0 >, via Wikimedia Commons

The other thing about this moment that I found interesting is that it highlights the role that **metacognition**, or thinking about thinking, plays in decision-making. Taking time to think something through carefully can be useful, but it also has its drawbacks: Thinking takes time, thinking uses metabolic resources, and depending on what you’re thinking about it may be more or less pleasant to keep turning your options over in your head. This trade-off between the benefits and the costs of having a long think means that not only do you have to make decisions out in the real world, you also have to decide how you’re deciding.

The constraints imposed by a game of chess make this trade-off especially stark. The time it takes to come to the best conclusion isn’t abstract, but is instead a very real resource that can decide the whole game. Those metabolic costs start to feel very real during a long game as well: Spending a lot of time on a single move may leave you feeling tired, hampering your ability to make good decisions later. Chess players thus have to engage in a process of thinking about the game, but also evaluating their own thinking: When should you dig deep and calculate carefully? When is it better to just **do something**?

Good metacognitive decisions over-the-board depend on knowing when it’s worth it to spend resources (your time and your energy) on extended thought. But can chess players tell when a position that they’re considering will benefit from more thinking? The study I want to tell you about here was designed to answer exactly this question: Do players of varying strength allocate their calculation time in ways that make sense given what’s on the board? Even though Hikaru ended up making a mistake after his awe-inspiring think, the time he spent might still have been the right call, after all.

## How do you objectively measure when a position deserves more thought?

The authors’ big goal in this study was to work out how well players of different abilities and across different time controls scaled their thinking time to the value of thinking more in real chess positions. That means they had two measurement problems to think about, one that’s quite easy and another that’s tougher. The easy part is measuring how long players think about a given position and the solution is fairly obvious: Let’s just use **move time!** Granted, this is not a perfect proxy for time spent thinking. [Mind-wandering is a very real phenomenon with its own interesting research literature](https://psycnet.apa.org/record/2013-07203-001) and players of all abilities certainly spend some time off-task even in crucial games. All the same, this is an easy thing to measure and certainly reflects players’ decision to consider a move more or less carefully.

The second thing the researchers had to measure was the value of thinking more in a particular position. This is a question about the state of the board rather than the players’ understanding of it (though hold that thought!) but requires a model of what outcomes you’d expect if you spent less vs. more time considering your options. Luckily, modern chess engines (in this case, Stockfish) are an excellent way to estimate this. Here, the authors used a simple means of quantifying the value of deeper thought using Stockfish assessments of the position at different depths of processing. If you’re not familiar with what this means, the classic definition of the term comes from algorithms that explored tree-like representations of how a game might proceed from a starting position. In these algorithms, depth specifically meant looking more possible steps ahead (or further down the tree) to more fully assess the potential consequences of each candidate move. The numbers associated with different depths in these models often referred specifically to a *ply*, or half-move, in a game.

![](https://miro.medium.com/v2/resize:fit:1280/format:webp/0*gGFSZkssUXFa3-QM.png)

An example of the full game tree for a much simpler game, namely Tic-Tac-Toe. In algorithms that do simple tree search, more depth means looking at outcomes that follow from more moves, moving you further down (here, across) the tree. A move that looks alright at a shallow depth might have negative consequences if you keep going. Image Credit: Mike like0708, CC0, via Wikimedia Commons

What depth means numerically in Stockfish and similar algorithms for assessing chess positions is not as simple as that, but it is still fair to say that a smaller (or we might say *shallower*) depth offers a less comprehensive look at possible outcomes than a greater (or *deeper*) search. In the current study, the authors used a fairly big difference in depth to estimate the value of extended thinking. First, they asked SF for the best move it could come up with using a depth-1 search. Next, they asked it to produce the best move at depth-15. With those two candidate moves in hand, they estimated the value of thinking more by asking depth-15 Stockfish (the harder thinker) to provide it’s usual numerical evaluation of each position. The difference between how well things turned out after making the higher depth move and the outcome from making the lower depth move is their final estimate of what thinking is worth.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*WxmuSQ6qHch4089K.png)

Figure 2 from Russek et al. (2025). The authors asked Stockfish to come up with the best move at Depth 1 and Depth 15, then evaluated the position after each move using the higher depth. The bigger the difference between those evals, the more value there is to spending time on the position. CC BY 4.0 License.

You can see in the figure above how this may shake out for different positions. On the left side of the figure, we see an example of a position in which the shallow move (Qxf2) leaves the position pretty much even while the deeper move (Qf5) gives Black a small advantage. On the right side, however, is a case where both the shallow and the deep search reveal the same best move: Take the horsey! In this case, there isn’t any value at all to thinking further because it doesn’t get better than the first thing you see.

I thought this approach to quantifying the value of deeper thought was a great choice and it also sounded rather familiar! [I’ve written before about a similar approach to estimating what moves deserve to be called “Brilliant.”](https://lichess.org/@/NDpatzer/blog/science-of-chess-what-makes-a-move-seem-brilliant/wtFdMXzO) The key difference between what’s happening here and using similar depth-differences to predict perceived brilliancy is that the current study is leveraging the full range of differences between shallow and deep search. “Brilliant” moves specifically look bad at a shallow depth but look good if you look deeper. Here, the authors are interested in all of the numerical differences between a brief think and thorough one to see if these predict how quickly players make choices.

## How does the time control affect players’ ability to choose when to think?

Give these two measurements, the time players take to move and the estimated value of thinking more, does the data suggest that players spend their time wisely? The researchers used a large-scale database of Lichess games (previously used to develop and test the [Maia chess engine](https://www.maiachess.com/)) that included half a billion moves from over 12 million games. These moves were taken from games at a wide range of time controls (which are reported in seconds rather than minutes in the text), from players spanning a wide range of playing strengths, and also limited to approximately the middlegame (between moves 7 and 37). This latter feature of the data used here is particularly important because it helps avoid any over-learned opening or endgame patterns that may contribute to very fast moves overall.

With all of this data in hand, the researchers were able to ask whether variance in move time was explained by their thinking-value variable. In the figure below (taken from their paper) you can see what this relationship looks like for different time controls, including Bullet, Blitz, and Rapid games with and without increment.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*RI_M-somJH4NlYnl.png)

Figure 3 from Russek et al. (2025). Each panel is a different time control (reported in seconds, so Bullet 1+0 is in the upper left) and the line graphs show the relationship between the average time players’ spent thinking about moves (y-axis) and the value in spending time thinking (x-axis). CC BY 4.0 License

I hope it’s evident that the main story from this figure is that players do indeed spend more time thinking when the position deserves it, or else these lines wouldn’t show such a clear increase in move time as the benefit to thinking increases. We can be a little more nuanced though and take note of some more granular features of the data. For one thing, there’s a statistically meaningful flattening to this curve as both variables increase, which signals that players appear to be most sensitive to the difference between no-advantage and some-advantage to further thought. I found this interesting as a vision scientist because it reminds me a little of the data we often get out of psychophysical experiments. In those tasks we often see evidence of a relationship called Weber’s Law which asserts that the smallest difference you can perceive between two stimuli gets bigger as the intensity of the stimuli increases. You can see a nice illustration of this in the figure below: In both the left and right half of the figure, there are 10 more dots in the bottom image. This is MUCH easier to see when we’re talking about 10 vs. 20 compared to when we’re talking about 110 vs. 120 however!

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*-uH-_E3OsrlpmOC1.png)

Image credit: By Д.Ильин: vectorization — File:Weber-Fechner law demo — dots.png by MrPomidor, CC0, https://commons.wikimedia.org/w/index.php?curid=113926988

The shape of the curves (which I’d call logarithmic) in the authors’ figure looks a lot like the kind of data we often get from sensory threshold experiments governed by this law, and it’s consistent with the idea that the benefit of thinking is working a bit like a perceptual variable. I’m not trying to argue that this is a real act of sensation or anything, but it’s still interesting to see the form of this relationship match data from other kinds of detection tasks. Another feature of the data I thought was striking was the dramatic increase in the width of the error bars as the time control lengthened, and especially when increment is available. In particular, the immense variability at the 30+20 time control relative to 30+0 is hard to ignore, and says a lot about how increment factors into players’ metacognition: Even a little time bonus every turn makes players much more willing to sometimes spend some resources on thinking.

## Does expertise lead to better decisions about deciding?

Besides examining the role of time control on the relationship between thinking benefit and move time, the authors were also able to slice their analysis up in terms of playing strength. This is especially interesting in that you could easily imagine that stronger players have better ideas about when it’s worth thinking through a position (estimating their own thinking-benefit variable) and thus are able to allocate time in a way that reflects what they might get out of thinking longer. By comparison, weaker players might not adequately sense the potential benefit (or potential peril!) that follows from spending more or less time on a particular move and thus show less sensitivity to thinking-benefit in their move times.

The figure below unpacks this for you, but it’s worth spending a little time explaining what’s being plotted. In essence, you’re about to look at graphs that show you a relationship between relationships. Let’s go back to the last graph for a moment — this included a curve for each time control that reflected how move time and thinking-benefit were related to one another. If we wanted to know what this curve looks like for players with different ratings, we could make separate lines for players of different strengths: One curve for the 1000–1200 ELO crowd, for example, and another one for the 1201–1400 ELO players, and so on. Instead of just looking at those, however, we can also measure the strength of the correlation between our two variables quantitatively. The authors did this using a value called Spearmann’s rho, which is a way of measuring correlations using the rank of each data point rather than it’s actual variable. This helps accommodate for non-linear shapes to our data like the logarithmic curves we saw in the authors’ Figure 2. Once we compute those values, we can make a new graph of how [Spearmann’s rho](https://en.wikipedia.org/wiki/Spearman%27s_rank_correlation_coefficient) changes with ELO as a function of each time control.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*o6hLUo4-dPd5bimc.png)

Figure 4 from Russek et al. (2025) — Spearmann’s rho values for the move time vs. thinking-benefit correlation as a function of playing strength (ELO rating) for the full range of time controls in the data set. CC BY 4.0 License.

Again, this is a case where the main story is pretty clear right away. As playing strength goes up, so does the strength of the relationship between move time and the objective value of thinking. That is, stronger players’ move times are more closely related to the possible benefit of thinking more. This graph gets a little depressing as you start scrutinizing what’s going on down at the low end of each graph honestly. At 1000 to 1200 ELO, player’s really don’t spend more time when they should (or less time when they don’t need to) very reliably at all! What I found remarkable, however, was how the strongest players in the data consistently were doing something better with their time even at the fastest time controls. Everything moves at breakneck speed during a Bullet game, but even when there’s 60 seconds total to work with, stronger players are spending those seconds on the positions that benefit from it (at least a little).

## Benefits vs. Costs to thinking?

I’ll close with an additional analysis that the authors carried out that I think is especially cool. Remember how I was kind of intrigued by the flattened curves on display in that initial look at the relationship between move time and the expected benefit of thinking? The authors were also intrigued by these and offer a nice perspective on where that shape may come from that’s based on an assessment of the **costs** to spending time thinking rather than just looking at the benefits.

The details of what they’re calculating are rather technical, but I want to try and give you the broad strokes. The starting point for their analysis is the observation that spending more time thinking obviously means you have less time to play, which increases the risk that you lose the game by running out of time. But how big is that risk? This is something the authors were able to estimate from the data! To do this, they sorted moves in their dataset according to the **amount of time left** and the **position evaluation** and then asked how often the active player actually won in those situations. What’s neat about this is that they’re getting all of this from the actual games, not from making many assumptions about the functions that might govern how games should turn out. The result is an empirical measurement of risk as a function of how much time you have left and how big your current advantage is: You can check out the left-most panel of their figure below to see what that looks like.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*lmpbnaezIZqBPKja.png)

Figure 8 from Russek et al. (2025) At left (a) is the 2D plot of winning probability (brighter squares indicate more likelihood of winning) as a function of the time you have left and the strength of your position advantage, determined from the games in the dataset. This plot makes it possible to estimate optimal strategies for allocating time based on the actual risk of losing (b-d). CC BY 4.0 License

From this counting exercise, the authors can start talking about optimal strategies for allocating time in light of how much risk and how much benefit you’re facing in different circumstances. The big insight I want to leave you with is in the two right-most panels of the figure just above: The 2D shape that the authors started with in the left panel leads to the relationship between how long it’s worth spending on calculating in ©. If you’re interested in the technical details regarding how you get between panel (a) and panel ©, I would very much encourage you to check out the paper for yourself for the full run-down. For my purposes here, the intuition I want to give you is that this way of estimating the risk of taking up time thinking implies data that’s shaped a little like what the authors actually saw from real people. While these curves don’t quite flatten out as much as the data we saw first, this is still a really neat example of using specific computational ideas about how people make decisions under uncertainty to explain why chess players may spend time the way they do over-the-board.

## What comes next?

This is one of those studies that has the potential to sound obvious to people: Oh, players spend more time thinking when there’s something worth thinking about? Big surprise. This is one of those cases in which, if you’re of that opinion, I’d encourage you examine that a little more: Why does it seem obvious? What are you assuming about what players can do during play? What do **you** do during a game to both manage your time and calculate as best you can? I suspect the more you consider it, the more you may realize that there is a lot you don’t really know about what makes you stop thinking and start moving.

What I like about the question the authors are asking (and answering) here is that it makes you think closely about the different kinds of decisions chess players have to make during a game. It’s easy to focus on identifying the best move as the primary goal for any player, but part of what we’re doing as real human beings playing this wonderful, complex game is try to understand other features of what’s happening on the board. For example, Julian from [Chess Engine Lab](https://chessenginelab.substack.com/) has a very fun post about the idea of sharpness in chess positions which I think about a lot: How well do we sense that a position is very volatile, with chances and missteps available for either player? When do we sense traps set for us or get the feeling that our opponent has unwittingly stepped into one of ours? When does a move or a whole game seem beautiful?

This rigorous look at one aspect of chess metacognition is a great example of how formalizing different aspects of what’s on the board with sophisticated models helps us understand more about how (and in this case, how fast) we make good and bad decisions during play. The vast amount of data we have about players of all strengths is truly remarkable, too, and I hope we see a lot more work that uses all those moves to tell us more about how the game works in the human mind.

## Support Science of Chess posts!

Thanks as always for reading! If you’re enjoying these Science of Chess posts and would like to send a small donation my way ($1-$5), you can visit my **Ko-fi page** here: [https://ko-fi.com/bjbalas](https://ko-fi.com/bjbalas) — Never expected, but always appreciated!

## References

Russek, E.M., Acosta-Kane, D., van Opheusden, B., Mattar, M.G. and Griffiths, T.L. (2025), Time Spent Thinking in Online Chess Reflects the Value of Computation. Cognitive Science, 49: e70119. [https://doi.org/10.1111/cogs.70119](https://doi.org/10.1111/cogs.70119)

McIlroy-Young, R., Sen, S., Kleinberg, J., & Anderson, A. (2020). Aligning superhuman AI with human behav-

ior: Chess as a model system. In Proceedings of the ACM SIGKDD International Conference on Knowledge

Discovery and Data Mining (pp. 1677–1687).

Osborne, H. (1964) Notes on the aesthetics of chess and the concept of intellectual beauty. British Journal of Aesthetics, 4, 160–164.

Zaidi, K. & Guerzhoy, M. (2024) Predicting User Perception of Move Brilliance in Chess. Arxiv, [https://arxiv.org/abs/2406.11895](https://arxiv.org/abs/2406.11895)