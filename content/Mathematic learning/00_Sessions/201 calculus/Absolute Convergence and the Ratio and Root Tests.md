
# Absolute Convergence

> [!definition]
> A series $\sum_{n=1}^{\infty}a_{n}$ is said to be absolutely convergent if the series of absolute values $\sum_{n=1}^{\infty}\lvert a_{n} \rvert$ is convergent.
> 
> A series $\sum_{n=1}^{\infty}a_{n}$ is said to be conditionally convergent if the series is convergent but not absolutely convergent.

2 cases 
1) $\sum a_{n}$ converges but $\sum \lvert a_{n} \rvert$ diverges (conditionally convergent)
2) $\sum \lvert a_{n} \rvert$ converges implies $\sum a_{n}$ converges (absolutely convergent) 
- We only need to check the convergence of $\sum \lvert a_{n} \rvert$ because the original series follow by the absolute value series
- In other word we are checking the stricter condition [[Limit Comparison test#^fac89d]]
- Suppose $\sum_{i=1}^{\infty}\lvert a_{i} \rvert$ is divergent, then $\sum_{i=1}^{\infty}a_{i}$ may still be conditionally convergent.

> [!remark]
> Sometimes it is easier to show absolutely convergent and thus deduce that the original series is convergent.

Determine the convergence of the series $\sum_{i=1}^{\infty} \frac{\cos i}{i^{2}}$.

Consider the series $\sum_{i=1}^{\infty} \left\lvert  \frac{\cos i}{i^{2}}  \right\rvert$. Note that

$$
0\leq \left\lvert  \frac{\cos i}{i^{2}}  \right\rvert\leq \frac{1}{i^{2}}
$$
for every $i\geq 1$.

Since $\sum_{i=1}^{\infty} \frac{1}{i^{2}}$ is a convergent p-series, by the Comparison Test, $\sum_{i=1}^{\infty} \left\lvert  \frac{\cos i}{i^{2}}  \right\rvert$ is convergent and thus $\sum_{i=1}^{\infty} \frac{\cos i}{i^{2}}$ is convergent.


## Rearrangement of a Series
One important property of finite sums is that we can rearrange their terms without changing the sum.

As we can see, absolute convergence ensures that this property also holds for infinite series.

> [!definition] Rearrangement
> A **rearrangement** of an infinite series $\sum_{i=1}^{\infty} a_{i}$ is a new series $\sum_{i=1}^{\infty} a_{\sigma(i)}$, where $\sigma: \mathbb{N} \to \mathbb{N}$ is a bijection (a permutation of the index set).
> Every single term from the original series appears in the new series exactly once, but the **order of the line-up** is altered.

> [!tip] Rearranging vs. Grouping (Parenthesizing)
> - **Grouping / Parenthesizing (Associative Law):** Deciding which terms to add together first without altering their order (e.g., $(a_{1} + a_{2}) + a_{3}$ vs. $a_{1} + (a_{2} + a_{3})$).
> - **Rearranging (Commutative Law for sequences):** Changing the queue/order in which terms arrive, which alters the sequence of partial sums $s_{n}' = a_{\sigma(1)} + \dots + a_{\sigma(n)}$.

### Example: Rearranging the Alternating Harmonic Series

The alternating harmonic series converges conditionally:
$$
1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \frac{1}{5} - \frac{1}{6} + \dots = \ln 2
$$

If we rearrange the queue to take **two positive terms followed by one negative term**:
$$
1 + \frac{1}{3} - \frac{1}{2} + \frac{1}{5} + \frac{1}{7} - \frac{1}{4} + \dots
$$
Every term of the original series is still present, but the new partial sums accumulate in a different order and actually converge to $\frac{3}{2}\ln 2$.

> [!important] Role of Absolute Convergence
> - **Absolutely Convergent Series:** Can be rearranged in **any arbitrary order** without altering the sum (finite commutativity extends safely; Dirichlet's Theorem).
> - **Conditionally Convergent Series:** The sum depends entirely on the order of summation. By the Riemann Rearrangement Theorem, a conditionally convergent series can be rearranged to sum to *any* real number, or even diverge.


> [!theorem]
> If $\sum_{i=1}^{\infty}a_{i}$ is an absolutely convergent series with sum $s$, then any rearrangement of $\sum_{i=1}^{\infty}a_{i}$ has the same sum $s$.

> [!theorem]
> If $\sum_{i=1}^{\infty}a_{i}$ is a conditionally convergent series and $r$ is any real number, then there is a rearrangement of $\sum_{i=1}^{\infty}a_{i}$ that has a sum equal to $r$.

---
# The Ratio Test

> [!theorem]
> Suppose $a_{i}\neq 0$ for all $i\geq 1$.
> 1) If $\lim_{ i \to \infty } \left\lvert  \frac{a_{i+1}}{a_{i}}  \right\rvert=L<1$, then the series $\sum_{i=1}^{\infty}a_{i}$ is absolutely convergent (and therefore convergent)
> 2) If $\lim_{ i \to \infty }\left\lvert  \frac{a_{i+1}}{a_{i}}  \right\rvert=L>1$ or $\lim_{ i \to \infty }\left\lvert  \frac{a_{i+1}}{a_{i}}  \right\rvert=\infty$, then the series $\sum_{i=1}^{\infty}a_{i}$ is divergent.
> 3) If $\lim_{ i \to \infty }\left\lvert  \frac{a_{i+1}}{a_{i}}  \right\rvert=1$, then the Ration Test is inconclusive; that is, no conclusion can be drawn about the convergence and divergence of the series $\sum_{i=1}^{\infty}a_{i}$.

Note that $\lim_{ i \to \infty }\left\lvert  \frac{a_{i+1}}{a_{i}}  \right\rvert=L$, thus at some point the ratio will approach close enough to $L$ that the tail of the series start behaving like a geometric series whose consecutive ratio is roughly $L$.

Since a geometric series $\sum r^{i}$ converges when whenever $\lvert r \rvert<1$, we expect the series to converges also.

Proof of Part 1:
Since $L<1$, we can choose a fixed constant  $r$ strictly between $L$ and 1:
$$
L<r<1
$$
By the definition of the limit, there exist an index $N$ such that if $i\geq N$, then
$$
\left\lvert  \frac{a_{i+1}}{a_{i}}  \right\rvert<r\implies \lvert a_{i+1} \rvert<r\lvert a_{i} \rvert
$$
Starting $i=N$, 
$$
\left\lvert  \frac{a_{N+1}}{a_{N}}  \right\rvert<r\implies \lvert a_{N+1} \rvert<r\lvert a_{N} \rvert
$$
When $i=N+1$
$$
\begin{align}
\lvert a_{N+2} \rvert<r\lvert a_{N+1} \rvert<r^{2}\lvert a_{N} \rvert
\end{align}
$$
When $i=N+k$
$$
\begin{align}
\lvert a_{N+k+1} \rvert<r\lvert a_{N+k} \rvert< r^{k+1}\lvert a_{N} \rvert \tag*{(1)}
\end{align}
$$
By induction, we have $\lvert a_{N+k} \rvert<r^{k}\lvert a_{N} \rvert$ for every $k\geq 1$. Hence

$$
\sum_{k=1}^{\infty} \lvert a_{N+k} \rvert< \lvert a_{N} \rvert \sum_{k=1}^{\infty} r^{k}
$$
Since $\lvert r \rvert<1$, the RHS is a convergent geometric series multiplied by a fixed constant $\lvert a_{N} \rvert$. Hence, by comparison theorem $\sum_{k=1}^{\infty}\lvert a_{N+k} \rvert$ is convergent and thus $\sum_{i=1}^{\infty}\lvert a_{i} \rvert$ is also convergent.

> [!remark] 
> (1) is easy to understand because the ratio is keep on decreasing, hence the real series must less than the geometric series with fixed ratio $r$. 
> Not only the series, we show the inequality in sequence first then only deduce to series

Proof  of part 2: