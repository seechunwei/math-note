
> [!definition] Intuitive Definition of a Limit at infinity
> Let $f$ be a function defined on some interval $(a,\infty)$. Then,
> 
> $$
> \lim_{ x \to \infty } f(x)=L
> $$
> Means that values of $f(x)$ can be made arbitrarily close to $L$ by requiring $x$ to be sufficiently large.

How about when $x\to-\infty$?
It is the same, thus one function can have at most $2$ different horizontal asymptotes.

But in this case $f$ defined on $(-\infty,b)$. 

We call $y=L$ as horizontal asymptotes. Formally:

> [!definition]
> The line $y=L$ is called a **horizontal asymptotes** of the curve $y=f(x)$ if either
> 
> $$
> \lim_{ x \to \infty }f(x)=L \text{ and }\lim_{ x \to -\infty } f(x)=L 
> $$
> 

Notice that horizontal asymptotes can cross horizontal asymptotes (oscillating) It is not the case for vertical asymptotes because of the definition of function. 


> [!info] Theorem
If $r>0$ is a rational number, then
>
>$$
\lim_{ x \to \infty } \frac{1}{x^{r}}=0$$
>
If $r>0$ is a rational number such that $x^{r}$ is defined for all $x$, then
>
>$$
\lim_{ x \to -\infty } \frac{1}{x^{r}}=0
$$

Why for negative infinity we need to suppose that $r$ is a rational number where $x^{r}$ is defined for all $x$.?

Because if $0<r<1$, then $x^{r}$  
$$
r= \frac{p}{q}
$$
where $p,q \in \mathbb{Z}$ and $q\neq 0$. where $x^r = x^{p/q} = \sqrt[q]{x^p}$

If $q$ is even. For example $\sqrt{ x }$ . then $x^{\frac{1}{2}}$
is not defined when $x\leq 0$,.

If $q$ is odd. Then, it is defined for all $x$.

![[Pasted image 20260621223005.png]]

> [!remark]
> This theorem is actually true for real number, but we haven't define the irrational power.
> 
> To rigorously define a real exponent like $x^\pi$, you first need to define the natural logarithm ($\ln x$) and the exponential function ($e^x$), allowing you to write $x^r = e^{r \ln x}$.
> 

## Infinite Limits at Infinity
The notation

$$
\lim_{ x \to \infty } f(x)=\infty
$$
is used to indicate that the values of $f(x)$ become large as $x$ becomes large. 



#### Precise Definitions of a Limit at infinity

> [!note] Definition
Let $f$ be a function defined on some interval $(a,\infty)$. Then
>
>$$
\lim_{ x \to \infty } f(x)=L$$
means that for every $\epsilon>0$ there is a corresponding number $N$ such that
>
if $x>N$ then $|f(x)-L|<\epsilon$.



Let $f$ be a function defined on some interval $(-\infty,a)$. Then

$$
\lim_{ x \to -\infty } f(x)=L
$$
means that for every $\epsilon>0$ there is a corresponding number $N$ such that 

if $x<N$ then $|f(x)-L|<\epsilon$.

Example
Prove that $\lim_{ x \to \infty } \frac{1}{x}=0$.

Preliminary step:

$$
\begin{align}
| \frac{1}{x}-0|&<\epsilon \\
x&< \frac{1}{\epsilon}
\end{align}
$$
(Since we are looking at the limit as $x \to \infty$, we can assume $x$ is positive. Therefore, $| \frac{1}{x} | = \frac{1}{x}$.)

Proof:
Let $N= \frac{1}{\epsilon}$ and suppose $\epsilon>0$. Then, we need to prove that for any $\epsilon>0$ there exist $N$ such that if $x>N$, then $|f(x)-0|<\epsilon$.

Since $\epsilon> 0$ it follow that $N> 0$, thus $x>0$. Starting with our inequality:

$$x > \frac{1}{\epsilon}$$

Since both sides are positive, taking the reciprocal reverses the inequality:

$$\frac{1}{x} < \epsilon$$
$$\frac{1}{x} < \epsilon$$
Because $x > 0$, we know that $\left| \frac{1}{x} - 0 \right| = \frac{1}{x}$. By direct substitution, we get:

$$\left| \frac{1}{x} - 0 \right| < \epsilon$$

Thus, let $N= \frac{1}{\epsilon}$. We have prove that $\lim_{ x \to \infty } \frac{1}{x}=0$

---

### Definition of an infinite limit at infinity

> [!note]
Let $f$ be a function defined on some interval $(a,\infty)$. Then
>
>$$
\lim_{ x \to \infty } f(x)=\infty$$
means that for every positive number $M$ there is a corresponding positive number $N$ such that
>
if $x>N$ then $f(x)>M$

Similar definitions apply when the symbol $\infty$ is replaced by $-\infty$ .

Example 
Prove $\lim_{ x \to \infty }(3x-5)=\infty$ 

Preliminary step:

$$
\begin{align}
3x-5&>M \\
3x&>M+5 \\
x&> \frac{M+5}{3}
\end{align}
$$
Thus we choose
$N= \frac{M+5}{3}$

Proof:
Suppose $M>0$ and let $N= \frac{M+5}{3}$. We need to show that if $x> \frac{M+5}{3}$, then $3x-5>M$. 

$$
\begin{align}
x&> \frac{M+5}{3} \\
3x&>M+5 \\
3x-5&>M
\end{align}
$$
$\blacksquare$.

> [!question]
> Contents
How to define $\lim_{ x \to \infty }f(x)=-\infty$?
>
For any $M<0$, there exists an $N>0$ such that if $x>N$, then $f(x)<M$.

Suppose we want to prove $\lim_{x \to -\infty} x^3 = -\infty$. Given a negative number $M < 0$, what condition must $x$ satisfy to guarantee $x^3 < M$?

Ans: $x< \sqrt[3]{M  }$

> [!question]
> To formally prove $\lim_{x \to \infty} (x^2 - x) = \infty$, a common technique is to bound the expression from below. For $x > 2$, which inequality is valid and helpful for the proof?
Let's break down **Question 8** step-by-step. It's a classic trick used in calculus proofs to handle messy polynomials.

The goal is to prove that:

$$\lim_{x \to \infty} (x^2 - x) = \infty$$

According to the formal definition, we need to show that $x^2 - x$ gets larger than any arbitrary giant number $M$. The algebraic challenge is solving the inequality $x^2 - x > M$ directly for $x$, because dealing with a quadratic inequality with two different powers of $x$ is messy.

To make our lives easier, we use a technique called **bounding from below**. We want to find a simpler function that is _always smaller_ than $x^2 - x$, but still goes to infinity.

### Step 1: The "Half-Share" Strategy

Think about the two terms: $x^2$ (which grows massive) and $-x$ (which subtracts from it). As $x$ gets very large, $x^2$ completely dominates $x$.

We want to show that subtracting $x$ doesn't hurt $x^2$ that much. Specifically, we can show that $x$ takes away _less than half_ of $x^2$.

Let's test when $x$ is less than half of $x^2$:

$$x < \frac{1}{2}x^2$$

If we divide both sides by $x$ (assuming $x > 0$), we get:

$$1 < \frac{1}{2}x \implies x > 2$$

So, **as long as $x > 2$**, the statement $x < \frac{1}{2}x^2$ is absolutely true.

### Step 2: Substituting into the Proof

Now, let's look at our original expression $x^2 - x$.

Since we know that $x < \frac{1}{2}x^2$ (for $x > 2$), if we multiply that inequality by $-1$, the sign flips:

$$-x > -\frac{1}{2}x^2$$

Now, add $x^2$ to both sides:

$$x^2 - x > x^2 - \frac{1}{2}x^2$$

$$x^2 - x > \frac{1}{2}x^2$$

### Why is this the correct answer?

By establishing that $x^2 - x > \frac{1}{2}x^2$, we have bounded our function from below with a much simpler function ($\frac{1}{2}x^2$).

Now, instead of solving the difficult inequality $x^2 - x > M$, we can just solve the much simpler inequality:

$$\frac{1}{2}x^2 > M$$

$$x^2 > 2M \implies x > \sqrt{2M}$$

If we make $x$ larger than both $2$ and $\sqrt{2M}$, then:

$$x^2 - x > \frac{1}{2}x^2 > M$$

This proves that $x^2 - x$ successfully shoots off to infinity!

- **Why the other options fail:** Bounding _above_ (like $x^2 - x < x^2$) doesn't help us prove something goes to infinity. Knowing a function is smaller than something big doesn't mean the function itself is big! We must prove it is _larger_ than a lower boundary that goes to infinity.

> [!question]
> If we use the lower bound $x^2 - x > \frac{1}{2}x^2$ (for $x > 2$) to prove $\lim_{x \to \infty} (x^2 - x) = \infty$, what is a safe choice for $N$ given $M > 0$?

Ans: $N=max(2,\sqrt{ 2M })$, we need $x>2$ for our lower bound to be true, and we need $x> \sqrt{ 2M }$ to make sure $\frac{1}{2}x^{2}>M$.