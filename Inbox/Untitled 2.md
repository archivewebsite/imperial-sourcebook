# What this calculus formula means

The image is explaining the **derivative**, which is calculus’s way of measuring an **instantaneous rate of change**.

The formula is:

\[
\frac{df}{dt} = \lim_{h \to 0} \frac{f(t+h) - f(t)}{h}
\]

In plain English:

> The derivative of \( f \) with respect to \( t \) tells you how fast \( f(t) \) is changing at one exact moment in time.

Humans, in their eternal quest to make “speed right now” sound like a legal contract, write it this way.

## The pieces

### \( f(t) \)

This means the value of some quantity \( f \) at time \( t \).

For example, \( f(t) \) might represent:

- position of a car at time \( t \)
- temperature at time \( t \)
- money in an account at time \( t \)
- population at time \( t \)

So \( f(t) \) is the **old value**.

## \( f(t+h) \)

This means the value of the same quantity a little later, at time \( t+h \).

Here, \( h \) is a small time interval.

So \( f(t+h) \) is the **new value**.

## \( f(t+h) - f(t) \)

This measures how much the quantity changed.

\[
f(t+h) - f(t)
\]

That is:

\[
\text{new value} - \text{old value}
\]

So this part gives the **change in the quantity**.

## \( h \)

The \( h \) represents the amount of time that passed.

So the fraction

\[
\frac{f(t+h) - f(t)}{h}
\]

means:

\[
\frac{\text{change in quantity}}{\text{change in time}}
\]

That is an **average rate of change** over the time interval \( h \).

For example, if distance changes by 20 meters over 4 seconds:

\[
\frac{20}{4} = 5
\]

So the average speed is 5 meters per second.

## The limit part

The important calculus move is this:

\[
\lim_{h \to 0}
\]

This means we let the time interval \( h \) get smaller and smaller, approaching zero.

Not actually equal to zero, because then we would divide by zero and mathematics would throw a chair.

Instead, \( h \) gets extremely close to zero.

So instead of asking:

> How fast is the quantity changing over a long interval?

we ask:

> How fast is the quantity changing at this exact instant?

That is the derivative.

## Final meaning

\[
\frac{df}{dt}
\]

means:

> the instantaneous rate of change of \( f \) with respect to time \( t \).

So the whole formula means:

\[
\frac{df}{dt} = \lim_{h \to 0} \frac{f(t+h)-f(t)}{h}
\]

or in words:

> The derivative is the value that the average rate of change approaches as the time interval becomes infinitely small.

## Simple example

Suppose:

\[
f(t) = t^2
\]

Then:

\[
f(t+h) = (t+h)^2
\]

Use the derivative formula:

\[
\frac{df}{dt} = \lim_{h \to 0} \frac{(t+h)^2 - t^2}{h}
\]

Expand:

\[
(t+h)^2 = t^2 + 2th + h^2
\]

So:

\[
\frac{df}{dt} = \lim_{h \to 0} \frac{t^2 + 2th + h^2 - t^2}{h}
\]

Cancel \( t^2 \):

\[
\frac{df}{dt} = \lim_{h \to 0} \frac{2th + h^2}{h}
\]

Factor out \( h \):

\[
\frac{df}{dt} = \lim_{h \to 0} \frac{h(2t+h)}{h}
\]

Cancel \( h \):

\[
\frac{df}{dt} = \lim_{h \to 0} (2t+h)
\]

Now let \( h \to 0 \):

\[
\frac{df}{dt} = 2t
\]

So if:

\[
f(t) = t^2
\]

then:

\[
\frac{df}{dt} = 2t
\]

This means the rate of change depends on the current value of \( t \).

At \( t = 3 \):

\[
\frac{df}{dt} = 2(3) = 6
\]

So at that exact moment, the quantity is changing at a rate of 6 units per unit time.

## Big idea

The derivative turns this:

\[
\text{average change over a time interval}
\]

into this:

\[
\text{instantaneous change at one exact point}
\]

That is the core idea behind differential calculus.