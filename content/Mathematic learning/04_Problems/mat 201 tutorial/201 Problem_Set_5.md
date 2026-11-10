
## Standard Problems

1) A series $\sum _ { i = 1 } ^ { \infty } a _ { i }$ is defined recursively by the equations: $a _ { 1 } = 1$ , and $a _ { i + 1 } = { \frac { 2 + \cos i } { \sqrt i } } a _ { i }$ for all $i \geq 1$ 

Determine whether the series is convergent or divergent. 

The given series $\sum_{i=1}^{\infty}a_{i}$ look like a geometric series with $a=1$ and $r= \frac{2+\cos i}{\sqrt{ i }}$. We know that $-1\leq \cos i\leq 1$ implies that
$$
\frac{1}{\sqrt{ i }}\leq \frac{2+\cos i}{\sqrt{ i }}\leq \frac{3}{\sqrt{ i }}
$$
Note that $\lim_{ i \to \infty } \frac{1}{\sqrt{ i }}=0$ and $\lim_{ i \to \infty } \frac{3}{\sqrt{ i }}=0$. Hence, $\lim_{ i \to \infty } \frac{2+\cos i}{\sqrt{ i }}=0$ by Squeeze Theorem. Hence, there exist a number $N$ such that if $i\geq N$, then

$$
\frac{2+\cos i}{\sqrt{ i }}<r
$$
where $0<r< 1$. Hence, it is clear that $\sum_{i=n}^{\infty}a_{i}$ is convergent. Note that

$$
\sum_{i=1}^{\infty} a_{i}=\sum_{i=1}^{n-1}a_{i}+\sum_{i=n}^{\infty} a_{i} 
$$
Since the second term is convergent adding a finite term $\sum_{i=1}^{n-1}a_{i}$ doesn't change the convergent behavior. Hence, $\sum_{i=1}^{\infty}a_{i}$ is convergent. $\blacksquare$

> [!remark]
> It is not rigorous, because claim that it is a geometric series is not formally correct, since ratio is not a constant. It is better to use ratio test since 
> $$
> \left\lvert  \frac{a_{i+1}}{a_{i}}  \right\rvert= \frac{2+\cos i}{\sqrt{ i }}
> $$
> and we have prove that $\lim_{ i \to \infty } \frac{2+\cos i}{\sqrt{ i }}=0$. Hence, by Ratio Test the series $\sum_{i=1}^{\infty}a_{i}$ converges. $\blacksquare$.  

Note that $\sum_{i=1}^{\infty} \frac{3}{\sqrt{ i }}$ is convergent, since $\frac{2+\cos i}{\sqrt{ i }}\geq 0$ and $\frac{3}{\sqrt{ i }}\geq 0$, it follow that by Direct Comparison Test. $\frac{2+\cos i}{\sqrt{ i }}$

2) Determine whether the series is convergent or divergent using the Ratio or the Root Test. 
(a*) $\sum _ { i = 1 } ^ { \infty } ( - 1 ) ^ { i + 1 } { \frac { i ^ { 2 } 2 ^ { i } } { i ! } }$ 

Let $a_{i}=(-1)^{i+1} \frac{i^{2}2^{i}}{i!}$. Note that $a_{i} \neq 0$ for all $i\geq 1$. Hence, 

$$
\begin{align}
\lim_{ i \to \infty } \left\lvert  \frac{a_{i+1}}{a_{i}}   \right\rvert&= \lim_{ i \to \infty }  \frac{(i+1)^{2}2^{i+1}}{(i+1)!} \cdot \frac{i!}{i^{2}2^{i}} \\
&=\lim_{ i \to \infty }   \frac{2\left(  1+ \frac{2}{i}+ \frac{1}{i^{2}} \right)}{i+1} \\
&=0
\end{align}
$$
Hence, by Ratio Test it follow that $\sum_{i=1}^{\infty}\lvert a_{i} \rvert$ is convergent and thus $\sum_{i=1}^{\infty}a_{i}$ is convergent. $\blacksquare$

(b*) $\sum _ { i = 1 } ^ { \infty } \left( { \frac { i ^ { 2 } + 1 } { 2 i ^ { 2 } + 1 } } \right) ^ { i }$ 
(c) $\sum _ { i = 1 } ^ { \infty } \left( 1 + { \frac { 1 } { i } } \right) ^ { i ^ { 2 } }$ 
(d) $\sum _ { i = 2 } ^ { \infty } { \frac { ( - 1 ) ^ { i - 1 } } { 3 \cdot 5 \cdot 7 \cdot \cdots \cdot ( 2 i - 1 ) } }$ 

3) Determine whether the series is convergent or divergent.
(a*) $\sum _ { i = 1 } ^ { \infty } { \frac { \sin 2 i } { 1 + 2 ^ { i } } }$ 
(b) $\sum _ { i = 1 } ^ { \infty } i \sin ( 1 / i )$ 
(c) $\sum _ { i = 1 } ^ { \infty } ( - 1 ) ^ { i } { \frac { \ln i } { \sqrt { i } } }$ 
(d) $\sum _ { i = 1 } ^ { \infty } { \frac { i ! } { e ^ { i ^ { 2 } } } }$ 

4*) (Not hard) Is it possible to find a power series whose interval of convergence is $\lbrack 0 , \infty ) ?$ Explain your answer. 

5) Determine the interval of convergence of the power series. (a) $\sum _ { i = 1 } ^ { \infty } { \frac { ( - 1 ) ^ { i } x ^ { i } } { i ^ { 3 } } }$ (b*) $\sum _ { i = 0 } ^ { \infty } ( - 1 ) ^ { i } { \frac { i ^ { 2 } x ^ { i } } { 2 ^ { i } } }$ (c*) $\sum _ { i = 0 } ^ { \infty } ( - 1 ) ^ { i } { \frac { x ^ { 2 i + 1 } } { ( 2 i + 1 ) ! } }$ (d) $\sum _ { i = 0 } ^ { \infty } i ! ( 2 x - 1 ) ^ { i }$ (e*) $\sum _ { i = 0 } ^ { \infty } ( - 1 ) ^ { i } \frac { ( x - 3 ) ^ { i } } { 2 i + 1 }$ 

## Non-standard Problems

6) Suppose that the power series $\sum _ { i = 0 } ^ { \infty } c _ { i } ( x - a ) ^ { i }$ satisfies $c _ { i } \neq 0$ for all $i \geq 1$ . Show that if $\operatorname* { l i m } _ { i \to \infty } \left| { \frac { c _ { i + 1 } } { c _ { i } } } \right| > 0$ , then the radius of convergence of the power series is $\operatorname* { l i m } _ { i \to \infty } \left| { \frac { c _ { i } } { c _ { i + 1 } } } \right|$ 7*) (Optional) Suppose the series $\sum _ { i = 1 } ^ { \infty } a _ { i }$ is conditionally convergent. Prove that the series $\sum _ { i = 1 } ^ { \infty } i ^ { 2 } a _ { i }$ is divergent. Note: This proof requires a brief moment of insight, but the solution is very short—just five lines! 