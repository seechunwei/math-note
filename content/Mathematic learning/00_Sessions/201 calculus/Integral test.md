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


Proof:
![[integral_test_comparison.png]]
Comparing the areas of the shaded rectangles with the area under the graph $y=f(x)$ from $1$ to $n$, we see that

$$
\sum_{i=2}^{n} f(i)\leq \int_{1}^{n}f(x)   \, dx \leq \sum_{i=1}^{n-1} f(i)
$$

Backward direction:
Comparison Theorem approach:
Suppose $\int_{1}^{\infty} f(x) \, dx$ is convergent. We need to show that $\sum_{i=1}^{\infty}f(i)$ is convergent.

Note that
$$
s_{n}=f(1)+\sum_{i=2}^{n} f(i)\leq f(1)+\int_{1}^{n} f(x) \, dx 
$$
The inequality hold for $n\geq 2$. Since they are positive and $\sum_{i=1}^{n}f(i)$ is monotonic increasing and $f(1)+\int_{1}^{\infty} f(x) \, dx$ is convergent, it follow that by Comparison Theorem for Monotone Sequence $\sum_{i=1}^{\infty}f(i)$ is convergent.

MCT approach:
Then
$$
\begin{align}
s_{n}= f(1)+ \sum_{i=2}^{n} f(i)\leq f(1)+ \int_{1}^{n} f(x) \, dx \leq f(1)+\int_{1}^{\infty} f(x) \, dx 
\end{align}
$$

For every $n\geq 2$, implying that $\langle s_{n} \rangle_{n=1}^{\infty}$ is bounded above.
Since $f$ is positive, the sequence $\langle s_{n} \rangle_{n=1}^{\infty}$ is increasing. Hence, by MCT, $\lim_{ n \to \infty }s_{n}$ exist and this $\sum_{i=1}^{\infty}f(i)$ is convergent. $\blacksquare$

Forward direction: We prove its contrapositive, suppose $\int_{1}^{\infty} f(x) \, dx$ is divergent. We need to show $\sum_{i=1}^{\infty}f(i)$ is divergent.

Note that
$$
s_{n}=\sum_{i=1}^{n-1}f(i)+f(n)\geq\int_{1}^{n} f(x) \, dx  +f(n)
$$
for $n\geq 2$. Thus, by Comparison Theorem for Monotone Sequence, it follow that $\sum_{i=1}^{\infty}f(i)$ is divergent.



> [!remark]
> Notice that if we want to use Comparison Theorem for Monotonic Sequence then we need to compare it with a sequence $T(n)=f(1)+\int_{1}^{\infty}f(x)  \, dx$ rather then a real number $f(1)+\int_{0}^{\infty} f(x) \, dx$.


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
Comparison test approach:
Test  the convergence of the series $\sum_{i=1}^{\infty} \frac{1}{i^{2}+1}$.
$$
\frac{1}{i^{2}+1}\leq\frac{1}{i^{2}}
$$

By p-series test, it follow that $\sum_{i=1}^{\infty}\frac{1}{i^{2}}$ is convergent. Note that $\frac{1}{i^{2}+1}\geq 0$ and $\frac{1}{i^{2}}\geq 0$ for all $i\geq 1$.

By comparison test, it follow that $\sum_{i=1}^{\infty} \frac{1}{i^{2}+1}$ is convergent. 

Integral test approach:
In this approach we no need to create an inequality to compare or it is useful if we cannot create such inequality that can apply comparison test.

Note that function $f(x)= \frac{1}{1+x^{2}}$ is continuous, positive, and decreasing on $[1,\infty)$ and so we can use the Integral Test.

$$
\begin{align}
\int_{1}^{\infty}  \frac{1}{x^{2}+1} \, dx &=\lim_{ t \to \infty } \int_{1}^{t}  \frac{1}{x^{2}+1} \, dx  \\
&=\lim_{ t \to \infty } [\tan ^{-1}x]^{t}_{1} \\
&= \lim_{ t \to \infty } [\tan ^{-1}t-\tan ^{-1}1] \\
&= \frac{\pi}{2}-\frac{\pi}{4} \\
&= \frac{\pi}{4}
\end{align}
$$

By integral test, it follow that $\sum_{i=1}^{\infty} \frac{1}{i^{2}+1}$ is convergent.

> [!remark]
> By using integral test, we can know the limit or the sum if the function continuous, positive and decreasing on $[1,\infty)$


Determine whether the series $\sum_{i=1}^{\infty} \frac{\ln i}{i}$ converges or diverges.

Consider the function $f(x)=\frac{\ln x}{x}$, it is continuous and positive on $[1,\infty)$, but we don't know if it is decreasing. Let's consider its derivative.

$$
\begin{align}
f'(x)&= \frac{x\left( \frac{1}{x} \right)-\ln x}{x^{2}} \\
&= \frac{1-\ln x}{x^{2}}
\end{align}
$$
Hence, $f'(x)<0$ when $\ln x>1\implies x>e$.

It follow that $f$ is continuous, positive, decreasing on $[3,\infty]$. Therefore we can use the Integral Test.

$$
\begin{align}
\int_{3}^{\infty}  \frac{\ln x}{x} \, dx&= \lim_{ t \to \infty } \int_{3}^{t} \frac{\ln x}{x}   \, dx 
\end{align}
$$

Let $u=\ln x\implies du= \frac{1}{x}dx\implies dx=xdu$. 
When $x=3$, $u=e^{3}$ and when $x=t$, $u=e^{t}$
Thus,

$$
\begin{align}
\int_{3}^{\infty} \frac{\ln x}{x}   \, dx &= \lim_{ t \to \infty } \int_{e^{3}}^{e^{t}}{u}   \, du \\
&=\lim_{ t \to \infty } \left[ \frac{u^{2}}{2} \right]^{e^{t}}_{e^{3}} \\
&=\lim_{ t \to \infty } \left[ \frac{e^{2t}}{2}- \frac{e^{6}}{2} \right]  \\
&=\infty
\end{align}
$$

Thus, by integral test, it follow that $\sum_{i=3}^{\infty} \frac{\ln i}{i}$ is divergent. Therefore, $\sum_{i=1}^{\infty} \frac{\ln i}{i}$ is divergent.

