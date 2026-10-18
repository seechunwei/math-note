
> [!axiom] The Two Axioms of a Proper Riemann Integral
> To define a standard (proper) Riemann integral $\int_{a}^{b} f(x) \, dx$, two fundamental conditions must be satisfied:
> 1. **Finite Horizontal Span**: The domain $[a, b]$ must be a closed, bounded (finite) interval.
> 2. **Finite Vertical Span**: The function $f(x)$ must be **bounded** (no vertical asymptotes / infinite discontinuities) on $[a, b]$.
> 
> If either constraint is violated, the integral is **improper**:
> - **Type 1 (Horizontal Infinity)**: The interval of integration is unbounded (e.g., $[a, \infty)$).
> - **Type 2 (Vertical Infinity)**: The function itself is unbounded ($f(x) \to \pm\infty$) at some point in $[a, b]$.

Now Consider the area under the curve $y=\frac{1}{x^{2}}$ from $x=1$ to $b$:
$$
Area= \int_{1}^{b} \frac{1}{x^{2}} \, dx
$$

Question: How do we make sense of $\int_{1}^{\infty} \frac{1}{x^{2}} \, dx$ when the domain of integration is the unbounded interval $[1,\infty)$?


Now consider the type 1 improper integral. 
$$
\int_{a}^{\infty} f(x) \, dx
$$

We can obtain the area by partitioning the interval into infinitely many parts.

$$
\begin{align}
\int_{a}^{\infty} f(x) \, dx&=\int_{a}^{a+1}f(x)   \, dx+\int_{a+1}^{a+2} f(x) \, dx+\dots \\
&= \sum_{i=1}^{\infty} \int_{i}^{i+1}f(x)  \, dx
\end{align}
$$

The infinite sum is called series. And by definition it is equivalent to

$$
\int_{a}^{\infty} f(x) \, dx=\lim_{ b \to \infty }\int_{a}^{b} f(x) \, dx 
$$


## Convergent and divergent

> [!definition]
> if $\int_{a}^{t} f(x) \, dx$ exist for every number $t\geq a$, then
> 
> $$
> \int_{a}^{\infty} f(x) \, dx=\lim_{ t \to \infty } \int_{a}^{t} f(x) \, dx
> $$
> The improper integral $\int_{a}^{\infty} f(x) \, dx$ is called convergent provided this limit exist; otherwise it is called divergent

If $f$ is continuous on $[a, t]$, then $f$ is Riemann integrable (the converse is not true: discontinuity does not automatically prevent integrability).

Thus, if $f(x)$ is continuous on $[a, \infty)$, then $\int_{a}^{t} f(x) \, dx$ is guaranteed to exist for every $t \ge a$. 

### What if $f(x)$ is NOT Continuous on $[a, \infty)$? (Checking the Condition)

To determine whether $\int_{a}^{t} f(x) \, dx$ exists for all $t \ge a$, we check **whether the function remains bounded**:

#### Branch 1: $f(x)$ Remains Bounded on $[a, t]$ (No Vertical Asymptotes)
$\int_{a}^{t} f(x) \, dx$ **exists as a proper Riemann integral**.
- **Case 1.1: Smooth / Continuous**: Evaluate directly via the Fundamental Theorem of Calculus (FTC).
- **Case 1.2: Finite Jump Discontinuities (Step Functions)**:
  *Example*: The floor function $\lfloor x \rfloor$ or piecewise steps.
  Since each jump is finite, the vertical step has zero width ($dx = 0$). The proper integral still exists; we simply split the integral across the jump points:
  $$\int_{a}^{t} f(x) \, dx = \int_{a}^{c_1} f(x) \, dx + \int_{c_1}^{t} f(x) \, dx$$

#### Branch 2: $f(x)$ is Unbounded on $[a, t]$ (Singularity / Vertical Asymptote)
- If $f(x) \to \pm\infty$ at some finite point $c \in [a, \infty)$ (an **infinite discontinuity** / vertical asymptote):
  Then $\int_{a}^{t} f(x) \, dx$ **FAILS to exist as a proper Riemann integral** whenever $t > c$.
- **What this means**: The problem is **NOT a pure Type 1 integral**. It has a **Type 2 singularity** hidden inside the interval $[a, \infty)$.
- **Resolution**: You must split the domain at the singular point $c$:
  $$\int_{a}^{\infty} f(x) \, dx = \int_{a}^{c} f(x) \, dx + \int_{c}^{\infty} f(x) \, dx$$
  where $\int_{a}^{c} f(x) \, dx = \lim_{t \to c^-} \int_{a}^{t} f(x) \, dx$ is evaluated as a Type 2 improper integral.

> [!tip] Hypothesis Precision: "Continuous" vs. "$\int_{a}^{t} f(x)\,dx$ Exists"
> Why do many introductory textbooks state *"Suppose $f$ is continuous on $[a, \infty)$"* instead of the more general *"$\int_{a}^{t} f(x)\,dx$ exists"*?
> 
> 1. **Pedagogical Cleanliness (Single Antiderivative via FTC)**:
>    If $f$ is continuous, a single uninterrupted antiderivative $F(x)$ exists across the whole interval. The integral $\int_{a}^{t} f(x) \, dx = F(t) - F(a)$ evaluates in one direct algebraic step, leaving only the pure boundary limit $\lim_{t \to \infty} [F(t) - F(a)]$.
> 2. **Isolating the Single Pathology**:
>    It guarantees the problem deals with **only one challenge** (the infinite domain), without cluttering the definition with interior jump tracking or piecewise surgery.
> 3. **The Logical Nuance**:
>    - **"Continuous"** is a **stronger / more restrictive** hypothesis (cleanest for computation via FTC, but technically excludes step functions).
>    - **"$\int_{a}^{t} f(x)\,dx$ exists"** is a **weaker / more general** hypothesis (covers pulses and jump functions in advanced analysis).
>    - Both formulations are mathematically rigorous; "continuous" is simply chosen for maximum clarity in Calculus 101.

What if the unboundedness is at left end point? Then

$$
\begin{align}
\int_{-\infty}^{b} f(x) \, dx=\lim_{ t \to -\infty } \int_{t}^{b} f(x)  \, dx
\end{align}
$$


## The p-Test for Improper Integral

Theorem
Suppose $p$ is any real number. Then $\int_{1}^{\infty} \frac{1}{x^{p}} \, dx$ is convergent if $p>1$ and divergent if $p<1$.

Why?
When $p=1$ , $\frac{1}{x^{p}}=\frac{1}{x}$. And notice that $\frac{1}{x}$ is continuous on $[1,\infty)$. Thus,
$$
\begin{align}
\int_{1}^{\infty} \frac{1}{x} \, dx&= \lim_{ t \to \infty } \int_{1}^{t} \frac{1}{x}  \, dx \\
&=\lim_{ t \to \infty } [\ln |x|]^{t}_{1} \\
&=\lim_{ t \to \infty } (\ln t) \\
&=\infty
\end{align}
$$

Thus, when $p=1$, the improper integral is divergent.

When $p \neq 1$,

$$
\begin{align}
\int_{1}^{\infty} \frac{1}{x^{p}} \, dx  &= \lim_{ t \to \infty } \int_{1}^{t} \frac{1}{x^{p}} \, dx  \\
&=\lim_{ t \to \infty }  \left[ \frac{x^{-p+1}}{-p+1} \right]^{t}_{1} \\
&= \lim_{ t \to \infty } \left[ \frac{t^{-p+1}}{-p+1}- \frac{1}{-p+1} \right] \\
&= \frac{1}{1-p} \lim_{ t \to \infty } \left(  \frac{1}{t^{p+1}}-1 \right) \\
&= \frac{1}{1-p} (0-1) \\
&= \frac{1}{p-1} &&(1)
\end{align}
$$

(1) When $p>1$, it follow that $\frac{1}{p-1}> 0$ and $\lim_{ t \to \infty } \frac{1}{t^{p+1}}=0$. 

If $p<1$, then $\lim_{ t \to \infty } \frac{1}{t^{p+1}}=\infty$. Therefore

$$
\begin{align}
\int_{0}^{\infty} \frac{1}{x^{p}}   \, dx =\infty  &&\text{if }p<1
\end{align}
$$


### Example
Evaluate $\int_{-\infty}^{\infty} \frac{1}{1+x^{2}} \, dx$

We need to split into 2 interval. But what middle point should we choose?
Notice that there is no vertical asymptotes . Thus, we can choose random point.

![[Pasted image 20261017163805.png]]

By definition,

$$
\begin{align}
\int_{-\infty}^{\infty} \frac{1}{1+x^{2}} \, dx &= \int_{-\infty}^{0}  \frac{1}{1+x^{2}} \, dx+ \int_{0}^{\infty} \frac{1}{1+x^{2}} \, dx  \\
\end{align}
$$

$$
\begin{align}
\int_{-\infty}^{0} \frac{1}{1+x^{2}} \, dx &= \lim_{ t \to -\infty } \int_{t}^{0} \frac{1}{1+x^{2}} \, dx  \\
&=\lim_{ t \to -\infty } [\tan ^{-1}x]^{0}_{t} \\
&=\lim_{ t \to -\infty } (0-\tan ^{-1}t) \\
&= -\left( -\frac{\pi}{2} \right) \\
&=\frac{\pi}{2}
\end{align}
$$

Similarly,

$$
\begin{align}
\int_{0}^{\infty} \frac{1}{1+x^{2}} \, dx&= \lim_{ t \to \infty }\int_{0}^{t} \frac{1}{1+x^{2}} \, dx  \\
&=  \lim_{ t \to \infty } [\tan ^{-1}x]^{t}_{0} \\
&=\lim_{ t \to \infty } [\tan ^{-1}t] \\
&= \frac{\pi}{2}
\end{align}
$$

Therefore
$$
\int_{-\infty}^{\infty} \frac{1}{1+x^{2}} \, dx =\frac{\pi}{2}+\frac{\pi}{2}= \pi
$$


Improper Integral of Type 2
What if the unboundedness is at function itself? For example
$$
\int_{0}^{1} \frac{1}{x^{2}} \, dx 
$$
Notice that $\lim_{ x \to 0 } \frac{1}{x^{2}}=\infty$. Thus, the integrand becomes inbounded at the endpoint $x=0$.

> [!definition]
> Suppose $f$ is continuous on $[a, b)$ and
> $$
> \lim_{ x \to b^{-} } f(x)=\pm \infty 
> $$
> Then, 
> $$
> \int_{a}^{b} f(x) \, dx =\lim_{ t \to b^{-} } \int_{a}^{t} f(x) \, dx 
> $$
> 
> Notice if $f(x)$ is unbounded at right end point, then it approaches from the left, and vice versa.


What if the unboundedness or vertical asymptotes is between the interval? For example

$$
\begin{align}
\int_{2}^{3} \frac{1}{x-1} \, dx 
\end{align}
$$

Notice that $x=1$ is a vertical asymptotes. Thus, we need to split into 2 and approach to $1$ form both side.

> [!definition]
> Suppose $f$ is continuous on $[a,b]$, except at $c$, where $a<c<b$, and 
> 
> $$
> \begin{align}
> \lim_{ x \to c^{-} } f(x)=\pm \infty \text{ and } \lim_{ x \to c^{+} } f(x)=\pm \infty
> \end{align}
> $$
> Then,
> 
> $$
> \int_{a}^{b} f(x) \, dx =\lim_{ t \to c^{-} } \int_{a}^{t} f(x) \, dx  + \lim_{ t \to c^{+} } \int_{t}^{b} f(x) \, dx  
> $$
>
>The improper integral is convergent if both of them are convergent otherwise it is divergent


> [!question] What if both endpoints are vertical asymptotes? 
> Then we use the same method to split it into 2 integration with any point $c\in[a,b]$ as middle point.

## The p-Test for Improper Integral type 2

> [!theorem]
> Suppose $p$ is any real number. Then $\int_{0}^{1} \frac{1}{x^{p}} \, dx$ is convergent if $p<1$ and divergent if $p\geq 1$.

It is because $0<x<1$. For example $x=0.5$. Then, $(0.5)^{2}=0.025$ and $\frac{1}{0.025}> \frac{1}{0.5}$ (increasing) and vice versa. The condition for convergence is reversed.

![[Pasted image 20261017180741.png]]

Notice that  $\frac{1}{x^{0.5}}<\frac{1}{x^{2}}$ on the interval $(0,1)$. Thus the graph $\frac{1}{x^{0.5}}$ is below $\frac{1}{x^{2}}$. Thus, the area must be smaller. (It is reverse after $x=1$)

It is like 2 reverse $\frac{1}{x}$ reverse one time and the interval $[0,1]$ reverse one time so $p$ is big implies that the area is big

Proof:

When $p=1$. Then,
$$
\begin{align}
\int_{0}^{1} \frac{1}{x} \, dx &=\lim_{ t \to 0^{+} }\int_{t}^{1} \frac{1}{x} \, dx  \\
&=\lim_{ t \to 0^{+} } [\ln \lvert x \rvert]^{1}_{t} \\
&= \lim_{ t \to 0^{+} } (0-\ln t) \\
&= \infty
\end{align}
$$
Thus, the improper integral is divergent.
When $p \neq 1$. Then,

$$
\begin{align}
\int_{0}^{1} \frac{1}{x^{p}} \, dx &= \lim_{ t \to 0^{+} } \int_{t}^{1} x^{-p} \, dx  \\
&=\lim_{ t \to 0^{+} } \left[ \frac{x^{-p+1}}{1-p} \right]^{1}_{t} \\
&= \frac{1}{1-p}\lim_{ t \to 0^{+} }   (1-t^{-p+1}) \\
\end{align} 
$$

When $p> 1$, then $\lim_{ t \to 0^{+} } t^{-p+1}= \infty$. (Because $p>1\implies 1-p<0$, thus we are dividing a very small number). Therefore, the improper integral is divergent.

When $p<1$, then $\lim_{ t \to 0^{+} } t^{1-p}=0$. (0 raise to a very small positive number is still 0). Thus,

$$
\int_{0}^{1} \frac{1}{x^{p}} \, dx = \frac{1}{1-p} 
$$
which is convergent. $\blacksquare$.

## Comparison Theorem

> [!theorem]
> Suppose that $f$ and $g$ are continuous on $[a,\infty)$ with $f(x)\geq g(x)\geq 0$ for all $x\geq a$.
> - If $\int_{a}^{\infty} f(x)   \, dx$ is convergent, then $\int_{a}^{\infty} g(x) \, dx$ is convergent
> - If $\int_{a}^{\infty} g(x) \, dx$ is divergent, then $\int_{a}^{\infty} f(x) \, dx$ is divergent


Determine whether $\int_{1}^{\infty} \frac{1+e^{-x}}{\sqrt{ x }} \, dx$ is convergent or divergent.

Show that $\int_{0}^{\infty} e^{-x^{2}} \, dx$ is convergent.

