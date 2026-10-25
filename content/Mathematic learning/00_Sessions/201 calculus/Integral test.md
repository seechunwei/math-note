Show that $\sum_{i=1}^{\infty}\ln\left( 1+ \frac{1}{i} \right)$ is divergent.

We cannot use divergence test here because $\lim_{ i \to \infty } (1+ \frac{1}{i})=1$. Thus, $\lim_{ i \to \infty }\ln\left( 1+ \frac{1}{i} \right)=0$. 

We consider the partial sums.

$$
\begin{align}
S_{n}&=\sum_{i=1}^{n} \ln\left(  1+\frac{1}{i} \right) \\
&=\sum_{i=1}^{n} \ln \left( \frac{i+1}{i} \right) \\
&= \sum_{i=1}^{n} (\ln(i+1)-\ln i)
\end{align}
$$

Hence, $s_{n}$ is a telescoping sum. Upon cancellation, we obtain $s_{n}=\ln(n+1)-\ln 1=\ln(n+1)$. Hence,

$$
\lim_{ n \to \infty } S_{n}=\lim_{ n \to \infty } \ln(n+1)=\infty
$$


The above example show test of divergent is inconclusive when we know $\lim_{ n \to \infty }a_{i}=0$.

This is the case for many important series like harmonic series or the generalize version which is p-series
$$
\sum_{i=1}^{\infty}  \frac{1}{i^{p}}
$$
## Geometric motivation

![[integral_test_convergence_case.png]]

We can interpret $\int_{1}^{\infty} \frac{1}{x^{2}} \, dx$ as the area under the graph of $y= \frac{1}{x^{2}}$ from $x=1$ to $\infty$.

Meanwhile $\sum_{i=2}^{\infty} \frac{1}{i^{2}}$ is the sum of the areas of the rectangles using right end point on interval $[1,\infty)$ with $\Delta x=1$.

From the diagram, we see that 
$$
\sum_{i=2}^{\infty}  \frac{1}{i^{2}}< \int_{0}^{\infty}  \frac{1}{x^{2}} \, dx 
$$

Since $\int_{1}^{\infty}  \frac{1}{x^{2}} \, dx$ is convergent (p-test) [[Improper integral#^4f99a4]] it follow that the series $\sum_{i=2}^{\infty} \frac{1}{i^{2}}$ with positive terms cannot diverge to $\infty$.

(It is something like the generalization of Comparison Theorem, the positive term here guarantee the monotonic)

![[Improper integral#^bf6817]]


![[integral_test_divergence_case.png]]

We can interpret $\int_{1}^{\infty} \frac{1}{\sqrt{ x }} \, dx$ as the area under the graph of $y= \frac{1}{\sqrt{ x }}$ from $x=1$ to $\infty$.

Meanwhile, $\sum_{i=1}^{\infty} \frac{1}{\sqrt{ x }}$ is the area of the rectangles using lest end point on interval $[1,\infty)$ with $\Delta x=1$. From the diagram we see that

$$
\sum_{i=1}^{\infty}  \frac{1}{\sqrt{ i }}> \int_{1}^{\infty} \frac{1}{\sqrt{ x }} \, dx 
$$
By p-test, it follow that $\int_{1}^{\infty} \frac{1}{\sqrt{ x }} \, dx$ is divergent. Thus, by the generalize version of Comparison Theorem, it follow that the series $\sum_{i=1}^{\infty} \frac{1}{\sqrt{ i }}$ is divergence.

> [!remark]
> We choose right end point of left end point based on our need to make it above or below the graph (overestimate or underestimate)

From 2 example above somehow it suggest that for there is a strong relation with the series and integration. 

> [!theorem] The Integral Test
> Suppose $f$ is continuous , positive, and decreasing function on $[1,\infty)$. Then the series $\sum_{i=1}^{\infty}f(i)$ is convergent iff the improper integral $\int_{1}^{\infty} f(x) \, dx$ is convergent.


> [!remark]
> Suppose $f$ is continuous (sufficient condition for Riemann integrable), positive (to ensure the integration/series is monotonic), and decreasing function (so that it squeeze between left end point and right end point).
> 
> What if it is increasing function? Then it is clear that it is divergent. We only concern about convergent since we cannot conclude anything from $\lim_{ i \to \infty }a_{i}=0$
> 
> Proof:
> Because $f(x)$ is positive and increasing for all $n\geq 1$:
> $$
> a_{n}=f(n)\geq f(1)> 0
> $$
> As $n\to \infty$ the terms $a_{n}$ cannot approach to 0. Thus, by the divergence test $\sum_{i=1}^{\infty}a_{i}$ is divergent. As well as the integral $\int_{1}^{\infty} f(x) \, dx$

> [!remark]
> The integral test is the bridge from p-test to p series test but not only this. (it is very useful for series containing rational function)

## Application of the Integral Test on p-Series

> [!theorem] P-series test
> The p-series $\sum_{i=1}^{\infty}  \frac{1}{i^{p}}$ is convergent if $p>1$ and divergent if $p\leq 1$.

In particular the harmonic series is a p-series for $p=1$ and it is divergent by the theorem.


Proof:
By p-test $\int_{1}^{\infty} \frac{1}{x^{p}} \, dx$ is convergent when $p> 1$ and divergent when $p\leq1$. Since $\frac{1}{x^{p}}$ is positive decreasing and continuous over $[1,\infty)$ when $p>0$, it follow that by integral test $\sum_{i=1}^{\infty} \frac{1}{i^{p}}$ is convergent if $p> 1$ and divergent if $0<p\leq1$. $\blacksquare$ 

Since we can only use integral test for $p>0$. Thus, we can use the divergence test for $p\leq 0$.

Case 1: $p<0$:
$$
\lim_{ i \to \infty } \frac{1}{i^{p}}=\infty
$$
Case 2: $p=0$
$$
\lim_{ i \to \infty }  \frac{1}{i^{p}}=1
$$
Hence, by the Test of Divergence, $\sum_{i=1}^{\infty} \frac{1}{i^{p}}$ diverges if $p\leq 0$. $\blacksquare$.

> [!remark]
> It is the sequence version of p-test for improper integral ![[Improper integral#^4c03e8]]

Example
Test the convergence of the series $\sum_{i=6}^{\infty} \frac{1}{(i-3)^{\pi}}$.

Note that $\sum_{i=1}^{\infty} \frac{1}{(i-3)\pi}= \sum_{i=1}^{\infty} \frac{1}{i^{\pi}}$.
Hence, it is a p-series with $p=\pi>1$, thus it is convergent.

> [!remark]
> Omitting or adding finitely many initial terms does not change the convergence of a series

Example
Test the series $\sum_{i=1}^{\infty} \frac{1}{\left( i- \frac{5}{2} \right)^{3}}$ for convergence or divergence.

Note that it is a polynomial or rational function. Thus, we can try compare with p-series:

$$
\begin{align}
\sum_{i=1}^{\infty}  \frac{1}{\left( i- \frac{5}{2} \right)^{3}}=\frac{1}{\left( -\frac{3}{2} \right)^{3}}+ \frac{1}{\left( -\frac{1}{2} \right)^{3}}+ \frac{1}{\left( \frac{1}{2} \right)^{3}}+\dots
\end{align}
$$

Note that start from $i=3$ the terms is positive. Since the function $f(x)= \frac{1}{\left( x-\frac{5}{2} \right)^{3}}$ is continuous, positive, and decreasing on $[3,\infty]$, we can use integral test

$$
\begin{align}
\int_{3}^{\infty}  \frac{1}{\left( x- \frac{5}{2} \right)^{3}} \, dx &= \lim_{ t \to \infty } \int_{3}^{t} \frac{1}{\left( x- \frac{5}{2} \right)^{3}} \, dx  \\
&= -\frac{1}{2}\lim_{ t \to \infty } \left[ \left( x- \frac{5}{2} \right)^{-2} \right]^{t}_{3} \\
&=-\frac{1}{2}\left( \left( t-\frac{5}{2} \right)^{-2}-\left( \frac{1}{2} \right)^{-2} \right) \\
&=-\frac{1}{2}(-4) \\
&=2
\end{align}
$$

Since $\int_{3}^{\infty} \frac{1}{\left( x- \frac{5}{2} \right)^{3}} \, dx$ is convergent, by the Integral Test. $\sum_{i=3}^{\infty} \frac{1}{\left( i- \frac{5}{2} \right)^{3}}$ is convergent.

> [!remark]
> We cannot compare with $\frac{1}{i^{3}}$ because $\frac{1}{\left( i-\frac{5}{2} \right)^{3}}> \frac{1}{i^{3}}$ while $\sum_{i=1}^{\infty} \frac{1}{i^{3}}$ is convergent which tell us nothing.

Example 
Test  the convergence of the series $\sum_{i=1}^{\infty} \frac{1}{i^{2}+1}$

