
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


## Alternating series test
