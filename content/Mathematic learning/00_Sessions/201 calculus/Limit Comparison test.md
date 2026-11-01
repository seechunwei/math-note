
## Comparison test

> [!theorem] Comparison Test
> Suppose $\sum_{i=1}^{\infty}a_{i}$ and $\sum_{i=1}^{\infty}b_{i}$ are series with nonnegative terms and $a_{i}\leq b_{i}$ for all $i\geq 1$.
> - If $\sum_{i=1}^{\infty}b_{i}$ is convergent, then $\sum_{i=1}^{\infty}a_{i}$ is convergent.
> - If $\sum_{i=1}^{\infty }a_{i}$ is divergent, then $\sum_{i=1}^{\infty}b_{i}$ is divergent

Proof:





> [!theorem] Limit Comparison Test
> Suppose $\sum_{i=1}^{\infty}a_{i}$ and $\sum_{i=1}^{\infty}b_{i}$ are series with positive terms. Suppose
> $$
> \lim_{ i \to \infty } \frac{a_{i}}{b_{i}}=c
> $$
> where $c$ is a finite number and $c>0$. Then either both series converge or both diverge. 

Proof:
Let $m$ and $M$ be any positive numbers such that $m<c<M$.
Since $\lim_{ i \to \infty } \frac{a_{i}}{b_{i}}=c$, the term $\frac{a_{i}}{b_{i}}$ is sufficient closed to $c$ for large i.

Thus, there exist a positive number $N$ such that if $i>N$, then
$$
m< \frac{a_{i}}{b_{i}}<M
$$
and so
$$
mbi<a_{i}<Mb_{i}
$$
if $\sum_{i=1}^{\infty}b_{i}$ is convergent, so $\sum_{i=1}^{\infty}Mb_{i}$. Thus, by Comparison Test, it follow that $\sum_{i=1}^{\infty}a_{i}$ is convergent.

If $\sum_{i=1}^{\infty}b_{i}$ is divergent, so $\sum_{i=1}^{\infty}mb_{i}$. Hence, $\sum_{i=1}^{\infty}a_{i}$ is divergent by the Comparison Test. $\blacksquare$

> [!remark]
> What is the difference of Integral Test and Limit Comparison Test? Integral test and limit comparison test no need to create an inequality to compare. 
> - Integral test, we know the limit value but also need strict condition
> - Use LCT when polynomial or roots or rational
> - Use Integral Test when a series contain logarithms alongside power of n
> - Integral Test compare with its own integration while Limit Comparison Test compare with a series that already know its convergence or divergence
> - [[201 Problem set 3#^2e3a60]]

Example
Determine the convergence of the series $\sum_{i=1}^{\infty} \frac{5}{2i^{2}-4i+3}$

Consider the series $\sum_{i=1}^{\infty} \frac{5}{2i^{2}}$, Note that the terms in these 2 series are positive, thus 

$$
\begin{align}
\lim_{ i \to \infty } \frac{\frac{5}{2i^{2}-4i+3}}{\frac{5}{2i^{2}}}&= \lim_{ i \to \infty }  \frac{2i^{2}}{2i^{2}-4i+3} \\
&=\lim_{ i \to \infty }  \frac{2}{2- \frac{4}{i}+ \frac{3}{i^{2}}} \\
&=1>0
\end{align}
$$
Since $\sum_{i=1}^{\infty} \frac{5}{2i}$ is divergent (Harmonic series), it follow that $\sum_{i=1}^{\infty} \frac{5}{2i^{2}-4i+3}$ is divergent by Limit Comparison Test.

Example
Determine whether the series $\sum_{i=1}^{\infty} \frac{i^{2}}{\sqrt{ 5+i^{3}+i^{6} }}$ is convergent or divergent.

When $i$ is large, $\frac{i^{2}}{\sqrt{ 5+i^{3}+i^{6} }}\approx \frac{i^{2}}{\sqrt{ i^{6} }}= \frac{1}{i}$. Hence we use Limit Comparison Test to compare with $\sum_{i=1}^{\infty} \frac{1}{i}$

$$
\begin{align}
\lim_{ i \to \infty }  \frac{\frac{i^{2}}{\sqrt{ 5+i^{3}+i^{6} }}}{\frac{1}{i}}&=  \lim_{ i \to \infty }   \frac{i^{3}}{\sqrt{ 5+i^{3}+i^{6} }} \\
&= \lim_{ i \to \infty }   \frac{1}{\frac{\sqrt{ 5+i^{3}+i^{6} }}{\sqrt{ i^{6} }}} \\
&=\lim_{ i \to \infty }  \frac{1}{\sqrt{ \frac{5}{i^{6}}+ \frac{1}{i^{3}}+1 }} \\
&= 1>0
\end{align}
$$
Since $\sum_{i=1}^{\infty} \frac{1}{i}$ is divergent, by the Limit Comparison Test, $\sum_{i=1}^{\infty} \frac{i^{2}}{\sqrt{ 5+i^{3}+i^{6} }}$ is divergent.

> [!remark]
> The key is to recognize a familiar series whose terms behave similarly to $a_{i}$. For example:
> - p-series $\sum_{i=1}^{\infty} \frac{1}{i^{p}}$
> - geometric series $\sum_{i=1}^{\infty} ar^{i-1}$

if $\lim_{ i \to \infty } \frac{a_{i}}{b_{i}}=0$, what can we say about the convergence of the series $\sum_{i=1}^{\infty}a_{i}$ and $\sum_{i=1}^{\infty}b_{i}$ where both series have positive terms?

Since $\lim_{ i \to \infty } \frac{a_{i}}{b_{i}}=0$, it follow that there exist a number $N$ such that if $i>N$
$$
\begin{gathered}
0< \frac{a_{i}}{b_{i}}<1 \\
0<a_{i}<b_{i}
\end{gathered}
$$
From here we can conclude that if $\sum_{i=1}^{\infty}a_{i}$ is divergent, then $\sum_{i=1}^{\infty}b_{i}$ is divergent. In other word, if $\sum_{i=1}^{\infty}b_{i}$ is convergent, then $\sum_{i=1}^{\infty}a_{i}$ is convergent. (Both statement need the condition that $a_{i}\geq 0$ and $b_{i}\geq 0$, precisely monotonic). This observation lead to the next theorem.
 

> [!theorem] Limit Comparison Theorem case 0
> Suppose $\sum_{i=1}^{\infty}a_{i}$ and $\sum_{i=1}^{oo}b_{i}$ consist of positive terms. If $\lim_{ i \to \infty } \frac{a_{i}}{b_{i}}=0$, then 
> 1) if $\sum_{i=1}^{\infty}a_{i}$ is divergent, then $\sum_{i=1}^{\infty}b_{i}$ is divergent
> 2) if $\sum_{i=1}^{\infty}b_{i}$ is convergent, then $\sum_{i=1}^{\infty}a_{i}$ is convergent
> 

> [!remark]
> Statement (1) and (2) are contrapositive of each other

Example of $\sum_{i=1}^{\infty}b_{i}$ is divergent and $\sum_{i=1}^{\infty}a_{i}$ is convergent

$$
\begin{align}
\lim_{ i \to \infty }  \frac{\frac{1}{i^{2}+1}}{\frac{1}{i}}&=  \lim_{ i \to \infty }  \frac{i}{i^{2}+1} \\
&=  \lim_{ i \to \infty }  \frac{\frac{1}{i}}{1+ \frac{1}{i^{2}}} \\
&=0
\end{align}
$$
But $\sum_{i=1}^{\infty}b_{i}=\sum_{i=1}^{\infty} \frac{1}{i}$ is divergent. while $\sum_{i=1}^{\infty}a_{i}=\sum_{i=1}^{\infty} \frac{1}{i^{2}+1}$ is convergent. 

Example of  $\sum_{i=1}^{\infty}b_{i}$ is divergent and $\sum_{i=1}^{\infty}a_{i}$ is divergent

$$
\begin{align}
\lim_{ i \to \infty } \frac{ \frac{1}{i}}{\frac{1}{\sqrt{ i }}}&= \lim_{ i \to \infty }  \frac{\sqrt{ i }}{i} \\
&= 0
\end{align}
$$
. Both are divergent.

## Alternating series test

> [!Theorem] Alternating Series Test
> An alternating series $\sum_{i=1}^{\infty}(-1)^{i+1}b_{i}$ with $b_{i}>0$ for a;; $i\geq 1$ is convergent if it satisfies both the following properties:
> 1) $b_{1+1}\leq b_{i}$ for all $i\geq 1$ and
> 2) $\lim_{ i \to \infty }b_{i}=0$

> [!remark]
> Think of $b_{i}$ as the magnitude, the first condition make sure it is fluctuating smaller and smaller and get near to $y=0$. 
> 
> Why we need $\lim_{ i \to \infty }b_{i}=0$? (1) cannot imply (2)? 
> Cannot, it can be decrease forever without getting close to 0, for example it is getting close to $y=1$ and $y=-1$. Then, the limit still does not exist.

Geometric Integretation:
![[Pasted image 20261101163832.png]]

The figure shows that the partial sum go back and forth, but the amount by which they go back and forth gets smaller and smaller because of the hypotheses. 

Note that odd partial sum is always approaching the limit from the right and even partial sum always approaching the limit from left.

Proof:
Consider the even partial sums $s_{2n}$ group in adjacent pairs:
$$
s_{2n}=(b_{1}-b_{2})+(b_{3}-b_{4})+\dots+(b_{2n-1}-b_{2n})
$$
By condition (1) $b_{k}\leq b_{k-1}$ for all $k$, thus each pair in the series is positive. Hence $s_{2n}$ is increasing. 

Note that $s_{2n}$ is bounded above by $s_{1}=b_{1}$.
$$
\begin{align}
s_{2n}&= b_{1}-(b_{2}-b_{3})-(b_{4}-b_{5})-\dots-(b_{2n-2}-b_{2n-1})-b_{2n} \\
&\leq b_{1}
\end{align}
$$

So, the sequence $\langle s_{2k} \rangle_{k=1}^{\infty}$ is bounded above. By MCT, $\langle s_{2k} \rangle_{k=1}^{\infty}$ is convergent,.

Consider the odd partial sums,
$$
\lim_{ k \to \infty } s_{2k+1}=\lim_{ k \to \infty } (s_{2k}+b_{2k+1})=s+0=s
$$
Note that $\lim_{ k \to \infty }b_{2k+1}=0$ by hypothesis (2). $\langle s_{2k} \rangle_{k=1}^{\infty}$ and $\langle s_{2k+1} \rangle_{k=1}^{\infty}$ form the partition of $\langle s_{n} \rangle_{n=1}^{\infty}$, it follow that

$$
\lim_{ k \to \infty } s_{2k}=\lim_{ k \to \infty } s_{2k+1}=L\implies \lim_{ n \to \infty } s_{n}=L
$$
Therefore, $\sum_{i=1}^{\infty}(-1)^{i+1}b_{i}= \lim_{ n \to \infty }s_{n}=L$ is convergent. $\blacksquare$

> [!intuition] Core Architecture of the Proof
> 1. **Tame the Oscillation:** An alternating sequence bounces back and forth, so the Monotone Convergence Theorem cannot touch $s_n$ directly. Sampling at period 2 ($s_{2n}$) eliminates the directional flip, turning the bounce into a strictly one-directional crawl ($s_2 \leq s_4 \leq s_6 \leq \dots$).
> 2. **Anchor with MCT:** Monotone + Bounded forces $\{s_{2n}\}$ to lock onto an exact limit $L$.
> 3. **Pinch the Scissors Gap:** The distance between the odd peaks and even troughs is $|s_{2n+1} - s_{2n}| = b_{2n+1}$. Condition (2) forces that gap to vanish, pinching the entire sequence into that single anchor point $L$.

Example
Consider the alternating harmonic series $\sum_{i=1}^{\infty} \frac{(-1)^{i+1}}{i}$ again. Let $b_{i}= \frac{1}{i}$ for every $i\geq 1$.

Since $\frac{1}{i+1}< \frac{1}{i}$ for every $i\geq 1$, hence it follow that $b_{i+1}<b_{i}$ and $\lim_{ i \to \infty }b_{i}= \lim_{ i \to \infty } \frac{1}{i}=0$.

Therefore, by the Alternating Series Test, the series is convergent.

> [!remark]
> Notice that this is alternating harmonic series. 
> $$
> \sum_{i=1}^{\infty} \left\lvert  \frac{(-1)^{i+1}}{i}  \right\rvert=\sum_{i=1}^{\infty} \frac{1}{i}
> $$
> Hence, we might think that $\sum_{i=1}^{\infty}\lvert a_{i} \rvert$ is convergent is stricter than $\sum_{i=1}^{\infty}a_{i}$ (Absolute Convergence implies Convergence).
> 
> Since $-\lvert a_{i} \rvert \leq a_{i} \leq \lvert a_{i} \rvert$, adding $\lvert a_{i} \rvert$ gives non-negative terms:
> $$
> 0 \leq a_{i} + \lvert a_{i} \rvert \leq 2\lvert a_{i} \rvert
> $$
> Since $\sum_{i=1}^{\infty} 2\lvert a_{i} \rvert = 2\sum_{i=1}^{\infty}\lvert a_{i} \rvert$ converges and all terms are non-negative, by the Direct Comparison Test, the series $\sum_{i=1}^{\infty} (a_{i} + \lvert a_{i} \rvert)$ is convergent.
> 
> Finally, by the difference law of series (subtracting the convergent series $\sum_{i=1}^{\infty} \lvert a_{i} \rvert$):
> $$
> \sum_{i=1}^{\infty} a_{i} = \sum_{i=1}^{\infty} (a_{i} + \lvert a_{i} \rvert) - \sum_{i=1}^{\infty} \lvert a_{i} \rvert
> $$
> Since both series on the right side converge, their difference $\sum_{i=1}^{\infty} a_{i}$ must also be convergent.

^fac89d

> [!question] What if $\lim_{ i \to \infty }b_{i}\neq 0$?
> Then we can use Test of Divergence to deduce that the series is divergent.

---

# Approximation by Partial Sums

If an alternating series fulfill all the condition of Alternating Series Test, then if the sum $s$ is approximated by the $n-$th partial sum $s_{n}$, then the error, namely, the remainder $R_{n}=s-s_{n}$, satisfies 

$$
\lvert R_{n} \rvert<b_{n+1}
$$

Proof:
We know that
$$
\begin{gathered}
s_{2n}\leq L\leq s_{2n+1} &&\text{for all }k\geq 1
\end{gathered}
$$

Since $L$ is trapped between 2 consecutive term, it follow that, the error $\lvert L-s_{n} \rvert$ cannot be larger than the distance between 2 consecutive term
$$
\lvert L-s_{n} \rvert\leq \lvert s_{n+1}-s_{n} \rvert=b_{n+1}
$$

> [!question] Why bound by the forward term $b_{n+1}$ instead of the previous term $b_{n}$?
> Notice that $L$ is also trapped between $s_{n}$ and the previous partial sum $s_{n-1}$, which would give an error bound of $\lvert s_{n} - s_{n-1} \rvert = b_{n}$.
> 
> However, because condition (1) guarantees that the terms are decreasing ($b_{n+1} \leq b_{n}$), the forward interval $[s_{n}, s_{n+1}]$ has a smaller width than the backward interval $[s_{n-1}, s_{n}]$. Choosing the forward step $b_{n+1}$ guarantees a strictly tighter (sharper) error bound with less error.


