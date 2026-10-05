
# The substitution rule

Observe that if $F'=f$, then

$$
\int F'(g(x))g'(x) \, dx=F(g(x))+c
$$
because, by the Chain Rule,

$$
\frac{d}{dx}[F(g(x))]=F'(g(x))g'(x)
$$
If we make the "substitution" $u=g(x)$, then 
we have

$$
\int F'(g(x))g'(x) \, dx=F(g(x))+c=F(u)+c= \int F'(u) \, du
$$

Thus, we have proved the following rule

> [!NOTE] The Substitution Rule
> If $u=g(x)$ is a differentiable function whose range is an interval $I$ and $f$ is continuous on $I$, then
> 
> $$
> \int f(g(x))g'(x) \, dx=\int f(u) \, du
> $$
> 



Example
Find $\int x^{3}\cos(x^{4}+2) \, dx$

Notice that $\frac{d}{dx}(x^{4}+2)=x^{3}$. It is in the form of $\int F'(g(x))g'(x) \, dx$

Let $u=x^{4}+2$. Thus, $\frac{du}{dx}=4x^{3}$. 

We can treat the $\frac{du}{dx}$ as differential for $\frac{\triangle u}{\triangle x}$. Thus, it becomes a quotient of 2 number. Hence,

$$
du=4x^{3}dx
$$

Thus, 
$$
\frac{du}{4}=x^{3} dx
$$

Thus, by substitution 

$$
\begin{align}
\int x^{3}\cos(x^{4}+2) \, dx&= \int \cos u \, \frac{du}{4} \\
&= \frac{1}{4} \int \cos u \, du \\
&=\frac{1}{4}\sin u+c \\
&=\frac{1}{4} \sin (x^{4}+2)+c
\end{align}
$$



### How about evaluating definite integrals?

First method: Evaluate integral first and then use the Fundamental Theorem

Second method: Change the limits of integration when the variable is changed.

> [!NOTE] The Substitution Rule for Definite Integrals
> If $g'$ is continuous on $[a,b]$ and $f$ is continuous on the range of $u=g(x)$, then
> 
> $$
> \int_{a}^{b} f(g(x))g'(x) \, dx= \int_{g(a)}^{g(b)}f(u)  \, du  
> $$

Why we need the condition that $g'$ is continuous on $[a,b]$ and $f$ is continuous on the range of $u=g(x)$

, before you can evaluate an integral, you must prove it is actually integrable.

- If $g'$ is continuous, then $g$ is continuous
- If $f$ is continuous on the range of $g(x)$ and $g$ is continuous, then $f(g(x))$ is also continuous.
- Multiplying two continuous functions ($f(g(x)) \cdot g'(x)$) gives a brand new continuous function.

Because continuous functions on a closed interval are always Riemann-integrable, demanding that $g'$ be continuous guarantees that the left-hand side of your equation is mathematically valid and doesn't bounce around chaotically.

> [!question]  Why the condition is different for indefinite integral and definite integral?
> 
> Let's look at the indefinite integral
> **Why the condition is weaker here:** Look closely at the Chain Rule step. To write down $\frac{d}{dx}[F(g(x))]$, what do we actually need from $g$? We _only_ need the derivative $g'(x)$ to exist at that point. The Chain Rule doesn't care if $g'(x)$ varies smoothly or jumps around chaotically across an interval; it only cares that the derivative **exists right now** (i.e., that $g$ is differentiable).
> 
>  
>  The Definite Rule Has to Deal with Riemann Sums
> 
> The moment you put boundaries on the integral ($\int_{a}^{b}$), you are no longer just looking for a derivative match. You are now invoking the machinery of **Riemann sums**—slicing up an entire physical interval, drawing rectangles, and taking a limit.

Here is the exact hierarchy of strictness for a function $g$:

$$\text{Continuously Differentiable } (C^1) \implies \text{Differentiable} \implies \text{Continuous}$$

- **Differentiable (Weaker):** This just means the derivative $g'(x)$ _exists_ at every point.
    
- **Continuously Differentiable (Strict):** This means the derivative $g'(x)$ exists **AND** that the derivative function $g'(x)$ itself is perfectly smooth and continuous (no sudden jumps or wild oscillations).

If $g(x)$ is merely differentiable, its derivative $g'(x)$ can actually be deeply pathological—it can oscillate infinitely fast and have massive amounts of discontinuities (like the famous function $x^2 \sin(1/x^2)$). If $g'(x)$ is that chaotic, the product $f(g(x))g'(x)$ might completely break the Riemann sum machinery, meaning you can't draw the rectangles or take the limit safely.

---

### Symmetry
Integrals of Symmetric Functions
Suppose $f$ is continuous on $[-a,a]$

a) If $f$ is even $[f(-x)=f(x)]$, then $\int_{-a}^{a} f(x) \, dx=2 \int_{0}^{a} f(x) \, dx$

b) If $f$ is odd $[f(-x)=-f(x)]$, then $\int_{-a}^{a} f(x) \, dx=0$

---

