You wouldn't run a company where you check revenue once a year and someone says "looks normal." You wouldn't deploy code with no monitoring, no alerts, no logs. Just a PDF someone emails you every 12 months that says "all systems operational" while your infrastructure is quietly on fire.

But that's exactly how most people manage their health.

I know because I did the same thing. I'm a product designer. I've built systems, pipelines, dashboards. Except, apparently, the one system that actually kills me if it goes down. I found out I was prediabetic at 35. My labs had said "normal" for years.

Turns out "normal" is a lie. And fixing it is an engineering problem nobody's bothered to solve properly.

## 1\. The monitoring is broken

Your annual blood panel checks about 15 biomarkers. Your body has thousands. That's not a monitoring system. That's checking whether the building is on fire by looking at it from across the street once a year.

Lab "normal" ranges are the central 95% of the tested population. That population is 88% metabolically unhealthy. You're being benchmarked against a sick cohort and told you're fine. My fasting glucose was 99. "Normal." Threshold is 100. I was one point from a flag, but cardiovascular risk starts climbing above 85. I was 14 points into the danger zone and my doctor said I was fine.

The test that would've caught me a decade earlier, fasting insulin, wasn't even ordered. It's not on the standard panel. 96 million Americans are prediabetic. 80% don't know. Not because the signal isn't there. Because nobody's reading it.

## 2\. The visualization layer doesn't exist

Here's what bothers me as an designer. Every complex system in the world has a dashboard. Datadog for your servers. Grafana for your infrastructure. Bloomberg terminal for markets. Even your car lights up when something is off.

Your body, the most complex system you'll ever operate, gives you a PDF. Rows of numbers. Maybe a flag if something is wildly out of range. No hierarchy. No severity weighting. No visual signal of what actually matters.

So I built one. BioMap is a treemap of your biomarkers, the same visualization used for stock market sectors, disk usage, and code coverage. Each block is a biomarker. Size equals clinical significance. Color equals status. Critical markers are large and red. Optimal ones are small and green. Glance at it and you know instantly where you're failing. No parsing a table. No Googling reference ranges. Two seconds and you see the shape of your health.

## 3\. There's no feedback loop

Even with a great dashboard, monitoring is useless without a feedback loop. In product development: you detect an anomaly > you investigate > you deploy a fix > you verify the fix worked. Detect > Intervene > Measure > Iterate. In health: you get a blood report, you feel vaguely concerned, you Google some supplements, you take them randomly for six months, you get another report, and you can't connect any input to any output.

There's no version control for your interventions. No way to diff your health between commits. That's the gap nobody's built for. In Otto, after you see your BioMap, you build your health stack: every supplement, protocol, and intervention you're running, each mapped to the specific biomarkers it targets. It's like declaring your dependencies.

Stacks are social. You can see what other people with similar flags are running. Follow their stacks. Watch their biomarkers move over time. It's GitHub for health interventions: transparent, forkable, outcome-tracked. When you upload your next labs, you see the delta. What improved. What didn't. What you were taking during that window. The feedback loop closes.

## 4\. The interface layer

Two more things that matter.

**Context-aware AI**. Tap any biomarker on your BioMap and ask Otto questions about it. Not generic chatbot answers. It knows your full panel, your stack, your history, your trends. "My ferritin is 280, I'm taking iron, and my CRP is rising. Are these connected?" It answers with your data, not WebMD's.

**Privacy controls**. Your profile shows your BioMap and stack publicly so the community can learn from each other. But if you don't want your numbers visible, flip a switch and your profile shows only the shape of your health. The treemap without the values. You decide what's public.

## 5\. The protocol

If you do nothing else, do this. Save it. Get real data.

- Add these to your next blood draw: fasting insulin, fasting glucose, ApoB, Lp(a), hs-CRP, full thyroid, vitamin D, homocysteine. (With fasting insulin and glucose, you can calculate HOMA-IR — a score that catches insulin resistance years before glucose alone does.)
- Benchmark against optimal, not population averages. Fasting glucose under 90, not under 100. Fasting insulin under 6. Vitamin D over 40. If your lab says normal, verify it yourself.
- If your bio age is higher than your calendar age, you have a problem no amount of "feeling fine" will fix. Track it quarterly.
- Every supplement should map to a biomarker. No biomarker target equals no reason to take it. Be as rigorous with your health stack as you are with your tech stack.
- Retest in 90-180 days. Diff the results. Attribute changes to interventions. Iterate. This is how you turn a static annual checkup into a continuous deployment pipeline for your body.

We build alerting for everything except the system that matters most. Upload your labs at ottolab.com. See what your doctor isn't showing you.
