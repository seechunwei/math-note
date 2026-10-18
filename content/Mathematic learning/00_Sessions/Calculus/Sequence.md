Infinite sequence: $a_{1},a_{2},a_{3},\dots$ (the ellipse mean so forth keep on going with non stop)

We use $\left\langle a_{1},a_{2},a_{3},\dots \right\rangle$ or $\langle a_{n} \rangle_{n=1}^{\infty}$ to denote the infinite sequence. A sequence can be viewed as the function
$$
\begin{align}
f(n)=a_{n} &&\text{for all }n\in Z^{+}
\end{align}
$$

> [!definition]
> An infinite sequence is a function whose domain is the set of positive integer

The Fibonacci sequence $\langle a_{n} \rangle_{n=1}^{\infty}$ is defined recursively by

$$
a_{1}=a_{2}=1 \text{ and }a_{n}=a_{n-1}+a_{n-2} \text{ for all }n\geq 3
$$

The first few terms are $1,1,2,3,5,8,13,21\dots$

Consider the sequence of ratios $\left\langle \frac{a_{n+1}}{a_{n}} \right\rangle^{\infty}_{n =1}$ derived from the Fibonacci sequence.

The first few terms are
$$
\frac{1}{1}, \frac{2}{1}, \frac{3}{2}, \frac{5}{3}, \frac{8}{5},\dots
$$
which is 
$$
1,2,1.5,1.667,1.6,1.625,\dots
$$


These terms are approaching the golden ratio, denoted by
$$
\phi= \frac{1+\sqrt{ 5 }}{2}=1.618033\dots
$$

We say that $\lim_{ x \to a }f(x)=L$ if we can make $f(x)$ arbitrarily close to $L$ by taking $x$ sufficiently close to $a$.

> [!definition]
> In other word, we say the sequence $\langle a_{n} \rangle_{n=1}^{\infty}$ converges to $L$ and write
> 
> $$
> \lim_{ n \to \infty } a_{n}=L 
> $$
> 
> By using $\epsilon-\delta$ definition, it is equivalent of saying for any $\epsilon>0$, there exist a number $M$ such that if $n>M$ then $|a_{n}-L|<\epsilon$

Prove that the sequence $\langle (-1)^{n} \rangle_{n=1}^{\infty}$ is divergent using definition.

Prove:
$$
(-1)^{n}=\begin{cases}
1&\text{when }n\in 2\mathbb{Z}^{+} \\
-1 &\text{when }n\in 2\mathbb{Z}^{+}-1
\end{cases}
$$

Their distance is exactly 2, if we choose $\epsilon<$ some number, then it fail. what is the number?

Assume the sequence converges and let $\lim_{ n \to \infty }(-1)^{n}=L$.
By definition, for any $\epsilon>0$ there exist a number $N>0$ such that if $n>N$, then $\lvert a_{n}-L \rvert<\epsilon$. 

$$
\begin{matrix}
-\epsilon<a_{n}-L<\epsilon \\
L-\epsilon<a_{n}<L+\epsilon
\end{matrix}
$$
Notice as long as we choose $\epsilon$ that make the interval less than 2, then we can lead to the contradiction. 

Let's choose $\epsilon= \frac{1}{2}$. Then $a_{n}\in\left(L-\frac{1}{2},L+\frac{1}{2} \right)$. Hence, both $1$ and $-1$ lies within the interval $\left( L-\frac{1}{2},L+\frac{1}{2} \right)$. 

However, the distance between 1 and -1 is 2, whereas the length of the interval is $1$. Thus, both point cannot lie in this interval -a contradiction. $\blacksquare$

> [!remark]
> Limit laws is also apply for sequence with the condition:
> - $\lim_{ n \to \infty }a_{n}$ and $\lim_{ n \to \infty }b_{n}$ exist.

---

> [!theorem]
> For any function $f$ of real variable and any real number $a$,
> $$
> \lim_{ x \to a } \lvert f(x) \rvert=0 \iff \lim_{ x \to a } f(x)=0
> $$

It is true for sequence:

> [!theorem]
> For any sequence $\langle a_{n} \rangle$ of real numbers,
> $$
> \lim_{ n \to \infty } \lvert a_{n} \rvert=0 \iff \lim_{ n \to \infty } a_{n}=0
> $$

Evaluate $\lim_{ n \to \infty } \frac{(-1)^{n}}{n}$

Since $\lim_{ n \to \infty } \left\lvert  \frac{(-1)^{n}}{n}  \right\rvert=\lim_{ n \to \infty } \frac{1}{n}=0$, by theorem, it follow that $\lim_{ n \to \infty } \frac{(-1)^{n}}{n}=0$.

> [!remark]
> The sequence look like this:
> $-1, \frac{1}{2},- \frac{1}{3}, \frac{1}{4}, -\frac{1}{5},\dots$ It is clear that it approach to 0

If $\lim_{ n \to \infty }a_{n}=-5$, then what can you say about $\lim_{ n \to \infty }\lvert a_{n} \rvert$? 
The limit is 5.

If $\lim_{ n \to \infty }\lvert a_{n} \rvert=5$, then what can you say about $\lim_{ n \to \infty }a_{n}$?
Cannot say anything, because it might be oscillating between -5 and 5. 

---
## Limit of Function and Sequence

We know that an infinite sequence $\langle a_{n} \rangle_{n=1}^{\infty}$ is a function $f(n)$whose domain is positive integer. $f:\mathbb{Z}^{+}\to \mathbb{R}$ such that
$$
f(n)=a_{n} \text{ for all }n\in \mathbb{Z}^{+}
$$

Thus, imagine the sequence is not discrete just like a normal function $f(x)$ whose domain is real number. 

We can say that $\langle a_{n} \rangle_{n=1}^{\infty}$ is the discrete point of $f(x)$, thus if $f(x)$ approach to $L$ when $x\to a$, then $\langle a_{n} \rangle_{n=1}^{\infty}$ must also approach to $L$.

But notice that since $\langle a_{n} \rangle_{n=1}^{\infty}$ is discrete, thus it cannot approach to some finite integer nor real number. Thus the limit only exist when we talk about $n\to \infty$.

But if $\lim_{ n \to \infty }a_{n}=L$ can we conclude that $\lim_{ n \to \infty }f(x)=L$? Consider the function below

$$
f(x)=\begin{cases}
\frac{x}{x+1} &\text{when }x\in \mathbb{Z}^{+} \\
\sin x &\text{when }x\not\in \mathbb{Z}^{+}
\end{cases}
$$
Notice that $\lim_{ n \to \infty }f(n)=1$ for $n\in \mathbb{Z}^{+}$. But $f(x)=\sin x$ is oscillates infinitely between $-1$ and $1$.

The $\lim_{ n \to \infty }$ doesn't give us any information about $[n,n+1]$. 

What if the function is continuous? Is the converse true? No. Consider the function
$$
f(x)=\sin(\pi x)
$$
Notice that when $x\in \mathbb{Z}^{+}$, $f(x)=0$. (Think about the unit circle). Thus, $\lim_{ n \to \infty }f(n)=0$
When $x\not\in \mathbb{Z}^{+}$ for example $x=n+\frac{1}{2}$, then

$$
f(x)=\sin\left( n\pi+ \frac{\pi}{2} \right)
$$
For $n =1$, $x= \frac{3}{2}\implies \sin\left(  \frac{3\pi}{2} \right)=-1$
For $n =2:$ $\sin\left( \frac{5\pi}{2} \right)=1$
(It oscillate between 1 and -1, thus the limit does not exist)

![[Pasted image 20261018091000.png]]

> [!theorem]
> Suppose $f$ is a function defined on the real numbers and $\langle a_{n} \rangle_{n=1}^{\infty}$ is a sequence such that
> 
> $$
> a_{n}=f(n)\text{ for all positive integers }n
> $$
> If $\lim_{ x \to \infty }f(x)=L$, then $\lim_{ n \to \infty }a_{n}=L$.

Proof:

> [!warning]
> Suppose $\lim_{ n \to \infty }f(x)=L$. By definition, for any $\epsilon>0$
> there exist a number $N$ such that if $x>N$, then $\lvert f(x)-L \rvert<\epsilon$.
> 
> Let $\langle a_{n} \rangle_{n=1}^{\infty}=\{ f(n)|n\in \mathbb{Z}^{+} \}\subseteq \{ f(x)|x\in \mathbb{R} \}$. Thus, if $a \in \langle a_{n} \rangle_{n=1}^{\infty}$, then $a\in \{ f(x)|x\in \mathbb{R} \}$.
> 
> [^1]Thus,  for any $\epsilon>0$, there exist a number $N$ such that if $x>N$, then $\lvert f(n)-L \rvert<\epsilon$.  Let $b=\lceil x \rceil$, thus $b\in \mathbb{Z}^{+}$, thus it follow that $b\geq x>N\implies \lvert f(n)-L \rvert<\epsilon$. $\blacksquare$
> 
> [^1]: This statement is wrong, because $f(n)$ is a function $f:\mathbb{Z}^{+}\to \mathbb{R}$. Thus, it cannot exist a $x\in \mathbb{R}$ as the candidate that satisfy the condition
> 
> Thus, there is nothing to do with the function value, instead the one we should concern is the domain $\mathbb{Z}^{+}\subseteq \mathbb{R}$. We need to show the existence of such integer.

The correct version:
Suppose $\lim_{ x \to \infty }f(x)=L$. Thus, by definition, for any $\epsilon>0$, there exist a number $N$ such that if $x>N$, then $\lvert f(x)-L \rvert<\epsilon$. 
Let $n\in \mathbb{Z}^{+}$ such that $n>N$. Since $\mathbb{Z}^{+}\subseteq \mathbb{R}$. It follow that $n\in \mathbb{R}$. Thus, it follow that if $n>N$, then $\lvert a_{n}-L \rvert=\lvert f(n)-L \rvert<\epsilon$. Hence $\lim_{ n \to \infty }a_{n}=L$. $\blacksquare$

> [!remark]
> Thus, we can find the limit of sequence by finding the corresponding limit of function and we can apply L'Hospital's Rule

Remark:
What if the function $f(x)$ is monotonic, then it won't oscillate, and since the limit of the sequence exist, it means that the function is bounded by the limit. Thus, the converse is true. (in other word it trap the real number in between the integer a region that strictly monotonic, no oscillate)

> [!theorem]
> If $f(x)$ is monotonic, then the converse is true

^2faa4a

Proof:
For any real number $x$, trap it between 2 consecutive integers: $\lfloor x \rfloor\leq x<\lfloor x \rfloor+1$. Since $f$ is non-decreasing, it follow that
$$
f(\lfloor x \rfloor )\leq f(x)\leq f(\lfloor x \rfloor +1)
$$

Let $n =\lfloor x \rfloor$. As $x\to \infty$, $n\to \infty$
- Left boundary: $f(n)\to L$
- Right boundary: $f(n +1)\to L$

By the Squeeze Theorem, $\lim_{ x \to \infty }f(x)=L$. $\blacksquare$.

> [!remark]
> Sequence monotonic cannot guarantee anything. 



---
## Uniqueness of limit

> [!theorem]
> The limit of a sequence , if it exists is unique

Proof:



----
## Limit of a Geometric Sequence

> [!theorem]
> The sequence $\langle r^{n} \rangle_{n=1}^{\infty}$ is convergent if $-1<r\leq 1$ and divergent for all other values of $r$. In fact,
> 
> $$
> \lim_{ n \to \infty } r^{n}= \begin{cases}
> 0 &\text{if }-1<r<1 \\
> 1&\text{if }r=1
> \end{cases}
> $$
> 

Proof:
When $r=1$. Then it is clear that $\lim_{ n \to \infty }1^{n}=1$.

If $r>1$, since $\lim_{ x \to \infty }r^{x}=\infty$, it follow that $\lim_{ n \to \infty }r^{n}=\infty$

When $0<r<1$, since $\lim_{ x \to \infty }r^{x}=0$, it follow that $\lim_{ n \to \infty }r^{n}=0$.

When $-1<r<0$. Then,  $0<\lvert r \rvert<1$ and thus,
$$
\lim_{ n \to \infty } \lvert r^{n} \rvert=\lim_{ n \to \infty } \lvert r \rvert^{n}=0
$$
Hence, $\lim_{ n \to \infty }r^{n}=0$. 

if $r<-1$, then when $n$ is even $r^{n}\geq 1$ and when $n$ is odd, $r^{n}\leq -1$. Therefore, $\lim_{ n \to \infty }r^{n}$ does not exist. $\blacksquare$.

---
## The Squeeze Theorem

> [!theorem]
> Suppose there exists $n_{0}$ such that
> $$
> a_{n}<b_{n}<c_{n} \text{ for all }n\geq n_{0}
> $$
> If $\lim_{ n \to \infty }a_{n}=\lim_{ n \to \infty }c_{n}=L$, then $\lim_{ n \to \infty }b_{n}=L$

How to prove?
Proof:
We need to show that for any $\epsilon> 0$, there exist a number $N$ such that $n>N\implies \lvert b_{n}-L \rvert<\epsilon$.  ^f7eca2

Hypothesis:
$\lim_{ n \to \infty }a_{n}=L$. there exist a number $N_{1}$ such that $n>N_{1}\implies \lvert a_{n}-L \rvert<\epsilon$. Hence,
$$
L-\epsilon<a_{n}<L+\epsilon
$$
$\lim_{ n \to \infty }c_{n}=L$. there exist a number $N_{2}$ such that $n>N_{2}\implies \lvert c_{n}-L \rvert<\epsilon$. Hence,
$$
L-\epsilon<c_{n}<L+\epsilon
$$
and $a_{n}<b_{n}<c_{n}$ for all $n\geq n_{0}$.

Argument:
Let $n>max(N_{1},N_{2},n_{0})$. (To let the hypothesis hold simultaneously ). Thus, since $b_{n}>a_{n}$. and $a_{n}>L-\epsilon$. By transitivity law, it follow that 
$$
L-\epsilon<b_{n}
$$
Since $b_{n}<c_{n}$ and $c_{n}<L+\epsilon$. By transitivity law, it follow that
$$
b_{n}<L+\epsilon
$$

Thus, by combining 2 inequality we get
$$
\begin{matrix}
L-\epsilon<b_{n}<L+\epsilon \\
-\epsilon<b_{n}-L<\epsilon \\ 
\lvert b_{n}-L \rvert<\epsilon
\end{matrix}
$$
$\blacksquare$


Determine whether the sequence $a_{n}= \frac{n!}{n^{n}}$, $n =1,2,3,\dots$ is convergent or divergent.

$$
\begin{align}
a_{n}= \frac{n!}{n^{n}}&= \frac{1\cdot 2 \cdot 3 \cdot \dots \cdot n}{n\cdot n\cdot n\cdot\dots \cdot n} \\
&= \frac{1}{n}\left( \frac{2\cdot 3\cdot 4\cdot\dots \cdot n}{n\cdot n\cdot n\cdot\dots \cdot n} \right)
\end{align}
$$
Hence, $0\leq a_{n}\leq \frac{1}{n}$ for all $n\geq 1$. Since $\lim_{ n \to \infty }0=\lim_{ n \to \infty } \frac{1}{n}=0$. It follow that by Squeeze Theorem, $\lim_{ n \to \infty }a_{n}=0$.

---

> [!theorem] _Sequential Criterion for Continuity_
> If $\lim_{ n \to \infty }a_{n}=L$ and the function $f$ is continuous at $L$, then
> $$
> \lim_{ n \to \infty } f(a_{n})=f(L)
> $$

Proof:
We need to show that for any $\epsilon>0$, there exists a number $N$ such that $n>N \implies \lvert f(a_{n})-f(L) \rvert < \epsilon$.

> [!tip] The Domino Chain ($\epsilon \implies \delta \implies N$)
> 1. $\epsilon > 0$ is given (the target error tolerance for the outputs).
> 2. Continuity of $f$ at $L$ translates $\epsilon$ into an input tolerance $\delta > 0$.
> 3. Convergence of $a_n \to L$ translates $\delta$ into a cutoff index $N$.

1. **Continuity of $f$ at $L$**: 
   Since $f$ is continuous at $L$, for the given $\epsilon > 0$, there exists $\delta > 0$ such that:
   $$
   \lvert x - L \rvert < \delta \implies \lvert f(x) - f(L) \rvert < \epsilon
   $$

2. **Convergence of $a_n$**: 
   Since $\lim_{n \to \infty} a_n = L$, for this specific $\delta > 0$, there exists $N$ such that:
   $$
   n > N \implies \lvert a_n - L \rvert < \delta
   $$

3. **Chaining**: 
   For any $n > N$, letting $x = a_n$, we have $\lvert a_n - L \rvert < \delta$, which immediately implies:
   $$
   \lvert f(a_n) - f(L) \rvert < \epsilon
   $$

Thus, by definition, $\lim_{n \to \infty} f(a_n) = f(L)$. $\blacksquare$

> [!warning] Failure Boundary: What if $f$ is discontinuous at $L$?
> The ability to pass the limit inside **fails** if $f$ is not continuous at $L$:
> $$
> \lim_{n \to \infty} f(a_n) \neq f\left(\lim_{n \to \infty} a_n\right)
> $$
> 
> *Counterexample*:
> Let $f(x) = \begin{cases} 1 &\text{if } x > 0 \\ 0 &\text{if } x \leq 0 \end{cases}$ and let $a_n = \frac{1}{n}$.
> 
> 1. **Inner limit**: $\lim_{n \to \infty} a_n = 0$, so $L = 0$.
> 2. **Function at the limit**: $f(L) = f(0) = \mathbf{0}$.
> 3. **Limit of the sequence of outputs**: For all $n \geq 1$, $a_n = \frac{1}{n} > 0 \implies f(a_n) = 1$.
>    $$
>    \lim_{n \to \infty} f(a_n) = \lim_{n \to \infty} 1 = \mathbf{1}
>    $$
> 4. **The Mismatch**: $\lim_{n \to \infty} f(a_n) = 1 \neq 0 = f(L)$.
> 
> *Why did it break down?*
> The sequence limit $\lim_{n \to \infty} f(a_n)$ DOES exist ($=1$), but the function's two-sided limit does NOT exist:
> $$
> \lim_{x \to 0^+} f(x) = 1 \quad \neq \quad \lim_{x \to 0^-} f(x) = 0
> $$
> Because $f$ is **discontinuous at $L = 0$**, the domino chain ($\epsilon \implies \delta$) is broken at the first step.



Find $\lim_{ n \to \infty }\sin\left( \frac{\pi}{n} \right)$.

Since $\sin x$ is continuous everywhere,
$$
\lim_{ n \to \infty } \sin\left( \frac{\pi}{n} \right)=\sin\left( \lim_{ n \to \infty } \frac{\pi}{n} \right)=\sin 0 =0
$$

---

## Monotonicity and Boundedness

> [!definition]
> A sequence $\langle a_{n} \rangle_{n=1}^{\infty}$ is increasing (or non-decreasing) if 
> $$
> a_{n+1}>a_{n}\text{ for all }n\geq 1
> $$
> and vice versa
> 

> [!definition]
> A sequence $\langle a_{n} \rangle_{n=1}^{\infty}$ is bounded above if there exists a number $M$ such that 
> $$
> a_{n}\leq M \text{ for all }n\geq 1
> $$
> and vice versa

If a sequence is bounded above and below, then the sequence is a bounded sequence.


> [!theorem] Monotone Convergence Theorem, MCT
> Every bounded monotonic sequence is convergent

> [!Theorem] Corollary
> a) Every increasing sequence bounded above is convergent
> b) Every decreasing sequence bounded below is convergent

To prove this theorem we need the following Completeness Axiom.

> [!theorem]  Completeness Axiom
> Is $S$ is any nonempty set of real numbers that is bounded above, (i.e. there exist an upper bound $M$ such that $x\leq M$ for all $x\in S$), then $S$ has a least upper bound.

Example
Consider the set $S=\{ x\in \mathbb{R}:x<2 \}$. Every number $M\geq 2$ is an upper bound for $S$. Among all these upper bounds, 2 is the least upper bound.

> [!note] Completeness Axiom vs. Well-Ordering Principle (WOP)
> Both principles serve as foundational "boundary guarantees", but they operate on fundamentally different fabrics:
> 
> | Dimension | Well-Ordering Principle (WOP) | Completeness Axiom (LUB Property) |
> | :--- | :--- | :--- |
> | **Domain** | Discrete realm: Positive integers $\mathbb{Z}^+$ | Continuous realm: Real numbers $\mathbb{R}$ |
> | **Membership** | **Must belong to the set**: $\min(S) \in S$ | **Can live outside the set**: $\sup(S)$ or $\inf(S) \notin S$ |
> | **What it heals** | Prevents infinite descending chains of steps | Fills all "holes" (irrational gaps) in the number line |
> 
> 1. **Inside vs. Outside Membership**:
>    - In WOP, every non-empty $S \subseteq \mathbb{Z}^+$ contains its own bottom: $\min(S) \in S$.
>    - In $\mathbb{R}$, the open interval $S = (0, 1)$ has no minimum element, but has an infimum $\inf(S) = 0 \notin S$. Completeness guarantees the horizon exists as a real number even if the set never reaches it.
> 2. **Discrete Floor vs. Continuous Hole-Filling**:
>    - WOP provides a discrete floor that powers Mathematical Induction and Infinite Descent.
>    - Completeness asserts that $\mathbb{R}$ has no gaps, ensuring that bounded monotonic sequences actually arrive at a destination in $\mathbb{R}$.
> 3. **What about Rationals $\mathbb{Q}$? (Fails Both)**:
>    - **WOP fails (density)**: $S = \left\{\frac{1}{n} \;\middle|\; n \in \mathbb{Z}^+\right\}$ has no minimum element in $\mathbb{Q}^+$.
>    - **Completeness fails (holes)**: $S = \{q \in \mathbb{Q} \mid q^2 < 2\}$ is bounded above, but has no least upper bound in $\mathbb{Q}$ because $\sqrt{2} \notin \mathbb{Q}$.
> 
> | System | WOP? | Completeness? | Nature |
> | :--- | :--- | :--- | :--- |
> | $\mathbb{Z}^+$ | **YES** | N/A | Discrete steps (induction) |
> | $\mathbb{Q}$ | **NO** | **NO** | Dense, but full of holes |
> | $\mathbb{R}$ | **NO** | **YES** | Continuum (calculus & limits) |

Proof of MCT Corollary (a):

Candidate generation via completeness:
Assume $\langle a_{n} \rangle_{n=1}^{\infty}$ is increasing and bounded above. Let $S=\{ a_{n}|n\in \mathbb{Z}^{+} \}$. By Completeness Axiom it follow that there exist a least upper bound $sup(S)$. Let $L=sup(S)$.

To prove $\lim_{ n \to \infty }a_{n}=L$, we need to show for any $\epsilon>0$, there exist a number $N$ such that $n>N\implies \lvert a_{n}-L \rvert<\epsilon$.
Thus,
$$
L-\epsilon<a_{n}<L+\epsilon
$$
Since $L-\epsilon<L$ is not the least upper bound of $S$. It follow that, there exist a number $N$ such that $a_{N}>L-\epsilon$. Since $n>N$, it follow that $a_{n}>a_{N}>L-\epsilon$. And note that $a_{n}<L<L+\epsilon$. Thus, chain the inequality together, it follow that

$$
\begin{matrix}
L-\epsilon<a_{n}<L+\epsilon \\
\lvert a_{n}-L \rvert<\epsilon
\end{matrix}
$$
Thus, $\lim_{ n \to \infty }a_{n}=L=sup(S)$. $\blacksquare$

> [!remark]
> From the proof we know that 
> $\lim_{ n \to \infty }a_{n}=sup \{ a_{n}|n\in \mathbb{Z}^{+} \}$ (for increasing sequences)
> $\lim_{ n \to \infty }a_{n}=inf\{ a_{n}|n\in \mathbb{Z}^{+} \}$ (for decreasing sequences)
>
>But we no need to find least upper bound to use MCT, instead upper bound $\implies$ existence of sup $\implies$ it is convergent 

Example Assignment Question 2 (b) and (c) 

---

> [!theorem] Order Limit Theorem
> Let $\left\langle a_{n} \right\rangle$ and $\left\langle b_{n} \right\rangle$ be convergent sequences with $\lim_{ n \to \infty }a_{n}=A$ and $\lim_{ n \to \infty }b_{n}=B$. If there exist an integer $N_{0}$ such that for all $n\geq N_{0}:a_{n}\geq b_{n}$ then $A\geq B$.
