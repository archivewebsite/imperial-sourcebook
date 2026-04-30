![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*jjmSpvftw6IzEuXtugegRg.png)

AI has a problem, particularly when you want to do something hard.

If you don’t know about the subject that you are trying to build, you don’t even know how to prompt. You don’t know what is possible.

Before you to try to one shot and build the hard thing, I reckon it’s better to take a pause and build a sandbox environment first.

Let me show you how I do that.

Let’s imagine you want to learn about computer vision and how to do tennis tracking.

I’ve seen some cool tennis trackers like this.

*Not a Medium member? Keep reading by clicking* [***here***](https://medium.com/@chrisdunlop_37984/before-you-build-anything-hard-with-claude-code-or-cursor-do-this-first-85156ae9a0ed?sk=167d6924537c7309140026212bda1652)*.*

![](https://x.com/mirrash7/status/2046685871739433172)

But for the sake of argument, let’s imagine you knew absolutely nothing about how to solve the problem.

The first step is to ask ChatGPT to recommend you a good library that has tutorials. We will use OpenCV for this.

Going to their website they have a list of tutorials.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*JEcDPttldpMDSm1HoIbYdw.png)

I just paste this into the chat window, asking for it to build a sandbox.

![](https://miro.medium.com/v2/resize:fit:1318/format:webp/1*Qt24sZkM2wEu1qRwIjh7eQ.png)

The AI will build you a series of modules. Each tutorial now gets its own folder. This makes it easy to keep the code clean and separated.

![](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*2Mf0zC0MVdRD-H5U1zovnw.png)

When this builds, I get a list of tutorials on the left hand menu.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*HUAqy9nE0k2yUwrArKra0Q.png)

Clicking through them, you can quickly see what the library is capable of.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*HEjyQCq9Km_2hGE0acCvNg.png)

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*FpRC-M8enCEYvWl4shqRBg.png)

Not only are you learning the specific language and words that the library uses, but you are also getting exposed to the art of the possible.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*bkyCgfavS8ttGGjwNo4NjA.png)

Why this is great is that now if you want to solve a particular problem, you have a bunch of modules that are already built that you can use to put together to solve your problem.

Back to our tennis example.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*55dpBkeJgXaEob-qL3FOlg.png)

Now that we have the sandbox set up it’s time for the next step.

So what you do is you paste the image into Cursor/Claude Code and ask it to playback potential ways it could use the various libraries in your sandbox to solve problems that you might have.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*VMcblly0FTCAzZETjxSoqQ.png)

I like doing it this way because I haven’t told the AI what I want yet, I have asked it what is possible.

The AI has provided me with 8 scenarios of problems that it can solve.

The first thing it made for me is a line detector that it said was good for detecting the outside of a court. That’s pretty cool.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*mkwzSDPpqo0rb10q0Ry5Tw.png)

It gives me a bunch of sliders, so I can adjust the type of line that it detects.

![](https://miro.medium.com/v2/resize:fit:1192/format:webp/1*Fe4HyXyUqMZ8jBCgWRdY4A.png)

The next idea it has was for a ball detector that uses colour inversion.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*xFcrrE2qCBuCsUNm4V1iUg.png)

The next one is a scoreboard extractor. On the right below you can see that it has picked out the scoreboard, I thought it was quite cool that it just automatically cropped to the correct area.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*WXz1d4siZySR7FQLvwkP5A.png)

You get the idea, there is all sorts of strange ideas that it surfaces. Like this one where it remapped the perspective. That’s quite cool.

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*J6E-y_73H7ylw_y49aOTMw.png)

You can see why this is helpful. You are getting served up ideas and so it might open your mind to new ways of doing things.

## The trick works for anything you’re new to

Audio processing. 3D modelling. Geospatial work. Financial libraries. Anywhere there’s a mature library with a tutorials page, you can sandbox it the same way.

I’ve done this with librosa for audio. Pasted the tutorials, got a sandbox, clicked through. Within an hour I knew that the library could do beat detection, pitch shifting, spectrograms, onset detection. I had no idea any of that existed before. Now when a problem comes up that touches audio, I have a mental map of what’s available.

I find that the pattern is always the same. I Find the library, find the tutorials page, paste it into Cursor or Claude Code and ask for a sandbox. The cool thing is that even if there isn’t listed tutorials, Cursor can make up it’s own ones from the documentation.

What you’re really building is a vocabulary. Once you know that “onset detection” is a thing, you can ask for it. Once you know “homography” exists in OpenCV, you can use it. The sandbox gives you the words.

And I find that the words are the bottleneck. You can’t prompt your way to something you don’t know exists. You can’t search for a solution if you don’t know what category it sits in. At this stage, most of being good with AI is just knowing what to ask for, and the fastest way to learn what to ask for is to see the menu.

So before you try to build the hard thing, build the sandbox. Spend an hour clicking around. Then go back to your real problem with a head full of options.

## Before you go

Subscribe to my **free** Substack [newsletter](https://chrisdunlop.substack.com/) **because** you get the following:

- A brand-new article for executives on Sunday that’s only posted on Substack.
- Links to every Medium post I’ve written in the past week
- Book recommendations every week for you to spend your Audible credits on
