---
tags: [math, calculus, derivatives, limits, differential-calculus]
date: 2026-04-25
aliases: [Derivative Definition, Limit Definition of Derivative, df/dt]
---

![[Pasted image 20260425112549.png]]

# The Limit Definition of the Derivative

&gt; [!INFO]
&gt; The **derivative** is calculus's way of measuring an ==instantaneous rate of change==.

$$\frac{df}{dt} = \lim_{h \to 0} \frac{f(t+h) - f(t)}{h}$$

In plain English: *How fast is $f(t)$ changing at this exact moment?*

---

## The Core Idea

Before calculus, we could only measure ==average rate of change== over an interval:

$$\frac{\Delta f}{\Delta t} = \frac{\text{change in quantity}}{\text{change in time}}$$

Calculus lets us ask a sharper question:

&gt; What is the rate of change at ==one exact instant==?

---

## Breaking Down the Formula

### Left Side: $\frac{df}{dt}$

**Leibniz notation** for the derivative.

| Symbol | Meaning |
|--------|---------|
| $f$ | The quantity being measured |
| $t$ | Independent variable (usually time) |
| $df$ | An infinitesimal change in $f$ |
| $dt$ | An infinitesimal change in $t$ |
| $\frac{df}{dt}$ | Instantaneous rate of change of $f$ with respect to $t$ |

&gt; [!EXAMPLE]
&gt; If $f(t)$ is position, then $\frac{df}{dt}$ is ==velocity==.

---

### Right Side: The Limit Expression

$$\lim_{h \to 0} \frac{f(t+h) - f(t)}{h}$$

| Symbol | Meaning |
|--------|---------|
| $\lim$ | The value being approached |
| $h \to 0$ | Time interval shrinks toward zero |
| $f(t)$ | Old value (at current time) |
| $f(t+h)$ | New value (after small interval $h$) |
| $f(t+h) - f(t)$ | Change in quantity |
| $h$ | Time interval |
| Fraction | Average rate of change over interval $h$ |

---

## The Logic: Average → Instantaneous

1. **Average rate**: $\frac{f(t+h) - f(t)}{h}$ is the slope of a ==secant line== through two points.
2. **Shrink the interval**: Let $h \to 0$. The two points merge into one.
3. **Instantaneous rate**: The secant becomes a ==tangent line==. The slope at that single point is the derivative.

&gt; [!IMPORTANT]
&gt; $h$ **approaches** zero but never equals zero. This avoids division by zero while capturing the behavior at a single instant.

---

## Concrete Example: $f(t) = t^2$

$$\frac{df}{dt} = \lim_{h \to 0} \frac{(t+h)^2 - t^2}{h}$$

**Step-by-step:**

$$\begin{aligned}
&= \lim_{h \to 0} \frac{t^2 + 2th + h^2 - t^2}{h} \\
&= \lim_{h \to 0} \frac{2th + h^2}{h} \\
&= \lim_{h \to 0} \frac{h(2t + h)}{h} \\
&= \lim_{h \to 0} (2t + h) \\
&= 2t
\end{aligned}$$

&gt; [!TIP]
&gt; Result: $\frac{df}{dt} = 2t$. At $t = 3$, the rate of change is ==6 units per unit time==.

---

## Why This Matters

The derivative turns **average change** over an interval into **instantaneous change** at a single point.

&gt; [!QUOTE]
&gt; A derivative measures how fast something is changing ==right now==.

**Applications:**
- #physics — velocity, acceleration, forces
- #economics — marginal cost, marginal profit
- #biology — population growth rates
- #engineering — system dynamics
- #machine-learning — gradient descent optimization

---

## Related Concepts

- [[Limits]]
- [[Continuity]]
- [[Tangent Line]]
- [[Secant Line]]
- [[Power Rule]]
- [[Chain Rule]]

#math #calculus #derivatives #limits #rate-of-change