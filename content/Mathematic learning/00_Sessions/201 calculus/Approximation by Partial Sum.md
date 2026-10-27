
For a convergent series, we may also want to approximate its sum using a partial sum.

We will use the ideas from integral test to see how this can be done.

Suppose $\sum_{i=1}^{\infty}a_{i}$ is convergent, and let $s=\sum_{i=1}^{\infty}a_{i}$. Let $n\in \mathbb{Z}^{+}$, thus

$$
s=\sum_{i=1}^{n} a_{i}+\sum_{i=n+1}^{\infty}a_{i} =s_{n}+\sum_{i=n+1}^{\infty} a_{i}
$$

Thus,
$$
s-s_{n}= \sum_{i=n+1}^{\infty} =a_{n+1}+a_{n+2}+\dots
$$
which is sum of the tail of the series after $n-th$ term.

If we approximate the sum $s$ by the partial sum $s_{n}$, then the error of approximation is $s-s_{n}$.

We denote this error by $R_{n}$ and call it the $n-$th remainder.

> [!theorem] Remainder Estimate Theorem
> Suppose $f$ is a continuous. positive, decreasing function on $[1,\infty)$. Suppose $\sum _{i=1}^{\infty}f(i)$ is convergent and let $s$ be its sum.
> 
> For each positive integer $n$, if we approximate the sum $s$ by the partial sum $s_{n}=\sum_{i=1}^{n}f(i)$ and let $R_{n}=s-s_{n}$, then
> 
> $$
> \int_{n+1}^{\infty} f(x) \, dx \leq R_{n}\leq \int_{n}^{\infty} f(x) \, dx 
> $$


Geometric interpretation:

![[Pasted image 20261026163744.png]]

The error of estimation is $\sum_{i=n+1}^{\infty}a_{i}$, which can be view as the area of rectangle on $[n,\infty)$  using right end point (underestimate).Thus
$$
R_{n}\leq \int_{n}^{\infty} f(x) \, dx 
$$

From another perspective. It can be view as the area of rectangle on $[n+1,\infty)$ using left end point (overestimate). Thus,
$$
\int_{n+1}^{\infty} f(x) \, dx \leq R_{n}
$$

Hence, combining 2 inequality:
$$
\int_{n+1}^{\infty} f(x) \, dx \leq R_{n}\leq \int_{n}^{\infty} R_{n} \, dx 
$$

> [!remark] 
> The inequality is intuitively clear in the sense that left hand side is the actual area on $[n+1,\infty)$ and right hand side is $[n,\infty)$.

Example:
Approximate the sum $\sum_{i=1}^{\infty} \frac{1}{i^{3}}$ by using the partial sum $s_{10}$. Estimate the error involved in this approximation.

Approximating by the partial sum $s_{10}$ , we get

$$
\sum_{i=1}^{\infty} \frac{1}{i^{3}}\approx s_{10}=1.197532
$$

Let $f(x)= \frac{1}{x^{3}}$. Then, $f$ is a continuous, positive, and decreasing function on $[1,\infty)$.

By Remainder Estimate Theorem,
$$
\int_{11}^{\infty} f(x) \, dx \leq R_{10}\leq \int_{10}^{\infty} f(x) \, dx 
$$

$$
\begin{align}
\int_{11}^{\infty} f(x) \, dx&= \lim_{ t \to \infty } \int_{11}^{t} \frac{1}{x^{3}} \, dx \\
&=\lim_{ t \to \infty } \left[  \frac{1}{-2x^{2}} \right] ^{t}_{11} \\
&= \lim_{ t \to \infty } \left( \frac{1}{-2t^{2}}+ \frac{1}{2(11)^{2}} \right)  \\
&= \frac{1}{2(11)^{2}}
\end{align}
$$

Same as the upper bound
$$
\int_{10}^{\infty}f(x)   \, dx= \frac{1}{2(10)^{2}} 
$$

The the error is at most $\frac{1}{2(10)^{2}}$ or precisely $\frac{1}{2(11)^{2}}\leq R_{n}\leq \frac{1}{2(10)^{2}}$.

In fact we can improve our approximation by taking the midpoint.

$$
\begin{matrix}
\int_{10}^{\infty} \frac{1}{x^{3}} \, dx \leq s-s_{n}\leq \int_{11}^{\infty}  \frac{1}{x^{3}} \, dx \\
\frac{1}{2(10)^{2}}\leq s-s_{n}\leq \frac{1}{2(11)^{2}} \\
\frac{1}{2(10)^{2}}+1.1975532\leq s \leq \frac{1}{2(11)^{2}}+1.1975532 \\
1.201664\leq s\leq 1.202532
\end{matrix}
$$

Take its mid point we get
$$
s=\sum_{i=1}^{\infty}  \frac{1}{i^{3}}\approx 1.202098
$$
with error at most 0.000434 (half of the interval)

Example
How many terms are required to ensure that the approximation of the sum $\sum_{i=1}^{\infty} \frac{1}{i^{3}}$ by a partial sum is accurate to within 0.00001?

Note that the function $f(x)= \frac{1}{x^{3}}$ is a positive, decreasing and continuous function on $[1,\infty)$, thus By Remainder Estimate Theorem
$$
R_{n}\leq \int_{n}^{\infty}  \frac{1}{x^{3}} \, dx 
$$

Hence, we need to find $n$ large enough so that
$$
\begin{align}
\int_{n}^{\infty} \frac{1}{x^{3}}   \, dx &\leq 0.00001 \\
&=\lim_{ t \to \infty } \int_{n}^{t} \frac{1}{x^{3}} \, dx \\
&= \lim_{ t \to \infty } \left[ -\frac{1}{2x^{2}} \right]^{t}_{n} \\
&=\lim_{ t \to \infty } \left( -\frac{1}{2t^{2}}+ \frac{1}{2n^{2}} \right) \\
&= \frac{1}{2n^{2}}
\end{align}
$$

Hence,
$$
\begin{align}
\frac{1}{2n^{2}}&\leq 0.00001 \\
2n^{2}&\geq \frac{1}{0.00001} \\
n^{2}&\geq 50000 \\
n&\approx223.6
\end{align}
$$
Therefore we need 224 terms to ensure error at most $0.00001$.

