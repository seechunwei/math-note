1*) Apply the Comparison Theorem above for improper integrals of Type 2 to determine whether the improper integral $\int _ { 0 } ^ { \pi } { \frac { \sin ^ { 2 } x } { \sqrt { x } } } d x$ is convergent or divergent. 

Since $0\leq\sin ^{2}x\leq 1$. It follow that $0\leq\frac{\sin ^{2}x}{\sqrt{ x }}\leq \frac{1}{\sqrt{ x }}$. 

$$
\begin{align}
\int_{0}^{\pi} \frac{1}{\sqrt{ x }} \, dx &= \int_{0}^{1} \frac{1}{\sqrt{ x }} \, dx +\int_{1}^{\pi} \frac{1}{\sqrt{ x }} \, dx  \\
\end{align}
$$

Notice that by theorem ![[Improper integral#^13e611]]
it follow that $\int_{0}^{1} \frac{1}{\sqrt{ x }} \, dx$ is convergent. Since $\int_{1}^{\pi} \frac{1}{\sqrt{ x }} \, dx$ is also convergent. It follow that $\int_{0}^{\pi} \frac{1}{\sqrt{ x }} \, dx$ is also convergent. By Comparison Theorem, it follow that $\int_{0}^{\pi} \frac{\sin ^{2}x}{x} \, dx$ is convergent.

2) Determine whether the sequence $\langle a _ { n } \rangle _ { n = 1 } ^ { \infty }$ converges or diverges, where 

(a) $a _ { n } = { \sqrt { \frac { n + 1 } { 9 n + 1 } } }$ 

$$
\begin{align}
\lim_{ n \to \infty } a_{n}&= \lim_{ n \to \infty }  \sqrt{ \frac{n+1}{9n+1} } \\
&= \lim_{ n \to \infty }  \sqrt{ \frac{1+\frac{1}{n}}{9+ \frac{1}{n}} } \\
&= \sqrt{ \frac{1}{9} } \\
&= \frac{1}{3}
\end{align}
$$

> [!remark]
> We can also consider the function, and show that it is decreasing and bounded below by 0, thus by MCT it is convergent. And the sequence is convergent
> 
> But it that necessary? 
> The answer is no, we just treat it like normal limit and substitute. We only use theorem when it is hard to find its limit

oscillate use squeeze or comparison

(b) $a _ { n } = { \frac { 3 ^ { n + 2 } } { 5 ^ { n } } }$ 

$$
\begin{align}
\lim_{ n \to \infty } \frac{3^{n+2}}{5^{n}}&= \lim_{ n \to \infty }9  \left( \frac{3}{5} \right)^{n} \\ 
&=0
\end{align}
$$
[[Sequence#^7c95fd]]

(c) $a _ { n } = { \frac { \sin 2 n } { 1 + { \sqrt { n } } } }$ 
Notice that $-1\leq\sin 2n\leq1$. Thus, it follow that 
$$
-\frac{1}{1+\sqrt{ n }}< \frac{\sin 2n}{1+\sqrt{ n }}\leq \frac{1}{1+\sqrt{ n }}
$$
Since $\lim_{ n \to \infty } \frac{1}{1+\sqrt{ n }}=0$ and $\lim_{ n \to \infty } -\frac{1}{1+\sqrt{ n }}$.Thus, by Squeeze Theorem it follow that $\lim_{ n \to \infty }a_{n}=0$.

==(d*)== $a _ { n } = \cos { \frac { n \pi } { 2 } }$ 

Note that 
$$
\cos \frac{n\pi}{2}=\begin{cases}
-1 &\text{if n/2 is odd}\\
0 &\text{if n is odd}\\
1& \text{if n/2 is even}
\end{cases}
$$
Since the sequence is oscillating infinitely between 3 number, it follow that the sequence is divergent. [[Sequence#^d343bf]]

(Ask about the theorem)

(e*) $a _ { n } = { \frac { n ! } { 2 ^ { n } } }$  ^b60f3d

$$
\begin{align}
\frac{n!}{2^{n}}&= \frac{1\cdot 2\cdot 3\cdot \dots \cdot n}{2\cdot 2\cdot 2\cdot\dots \cdot 2} \\
&= \left( \frac{1}{2} \right)\left( \frac{2}{2} \right)\left( \frac{3}{2} \right)\dots\left( \frac{n}{2} \right) \\
&> \left( \frac{1}{2} \right)(1)(1)\dots\left( \frac{n}{2} \right) \\
&> \left( \frac{n}{4} \right)
\end{align}
$$

Since $\lim_{ n \to \infty } \frac{n}{4}=\infty$ and $0< \frac{n}{4}<a_{n}$. Thus by Comparison Theorem it follow that $\langle a_n \rangle_{n=1}^{\infty}$ is divergent.
[[Improper integral#^96cfa0]]

Remark:
For factorial and power sequence we expand first


(f*) $a _ { n } = \left( \frac { 1 + n } { 3 n } \right) ^ { n }$ 

$$
\begin{align}
\lim_{ n \to \infty } a_{n}&= \left( \frac{1}{3n}+\frac{1}{3} \right)^{n}  \\
=0
\end{align}
$$

But it is not rigorous, because basic limit law only allow to take limits of;
1. $b^{n}$ when the base $b$ is a fixed constant 
2. $[f(n)]^{p}$ when the exponent $p$ is a fixed constant.

Because both of them are continuous thus we can do this by substitution, but we don't know about function $x^{x}$ . Actually there is one trick using natural logarithm:

$$
[f(x)]^{g(x)}e^{g(x)\ln f(x)}
$$
Because the exponential function $e^{u}$ is continuous everywhere, we can pass the limit directly inside the exponent. (Proof?)

Go back to the question:
$$
\begin{align}
\lim_{ n \to \infty } a_{n}&=\lim_{ n \to \infty } \left( \frac{1}{3n}+\frac{1}{3} \right)^{n} \\
&=\lim_{ n \to \infty } e^{n\ln\left( \frac{1}{3n}+ \frac{1}{3} \right)} \\
\end{align}
$$
Since it is continuous, we can push the $\lim$it inside [[1)a) The limit laws#^a2a6d3]]. Thus, $\lim_{ n \to \infty }\left( \frac{1}{3n}+\frac{1}{3} \right)=\frac{1}{3}$ and $\ln \frac{1}{3}< 0$. and $\lim_{ n \to \infty }n =\infty$. Thus $e^{-\infty}=0$ . Hence

$$
\lim_{ n \to \infty } a_{n}=0
$$

Another approach by squeeze theorem:
[^1]For any $n\geq 1$, $1+n\leq 2n$. Thus,
$$
\frac{1+n}{3n}< \frac{2n}{3n}=\frac{2}{3}
$$

Since $0<\left(  \frac{1+n}{3n} \right)^{n}< \left( \frac{2}{3} \right)^{n}$ for all $n\geq 1$.  Note that $\lim_{ n \to \infty }0=0$ and $\lim_{ n \to \infty } (\frac{2}{3})^{n}=0$ by [[Sequence#^7c95fd]] 
. Therefore by Squeeze Theorem, it follow that $\lim_{ n \to \infty }a_{n}=0$.

> [!remark]
> Cannot use L'Hospital's Rule here, because the base approach to $\frac{1}{3}$

[^1]: It work for 2 reason:
	- The sequence start from positive integer
	- The limit approach to infinity, by definition we only need to find a number $N$ such that the limit exist for $n>N$

(g) $a _ { n } = \left( 1 + { \frac { 2 } { n } } \right) ^ { n }$ 

Notice that $\lim_{ n \to \infty }a_{n}$ is very close to 
$$
\lim_{ n \to \infty } \left( 1+\frac{1}{n} \right)^{n}=e
$$

How to eliminate the 2?
Let $m=\frac{n}{2} \implies n = 2m$. Thus, $n\to \infty\implies m\to \infty$. Therefore,

$$
\begin{align}
\lim_{ n \to \infty } a_{n}&= \lim_{ m \to \infty } \left( 1+ \frac{1}{m} \right)^{2m} \\
&= \left[ \lim_{ m \to \infty } \left( 1+ \frac{1}{m} \right)^{m} \right]^2 \\
&=e^{2}
\end{align}
$$

> [!remark] Real-World Meaning: Continuous Compound Growth
> This is the continuous compounding formula $\lim_{n \to \infty} P\left(1 + \frac{r}{n}\right)^{nt} = P e^{rt}$:
> - It corresponds to a **200% growth rate ($r = 2$)** compounded continuously for **1 year** ($t = 1$): $e^{2 \times 1} = e^2 \approx 7.389$.
> - Or a **100% growth rate ($r = 1$)** compounded continuously for **2 years** ($t = 2$): $e^{1 \times 2} = e^2$.
> 
> General formula for any constant $x \in \mathbb{R}$:
> $$
> \lim_{ n \to \infty } \left( 1 + \frac{x}{n} \right)^{n} = e^x
> $$

> [!warning]
> Note that
> $$
> a_{n}=\left( 1+ \frac{2}{n} \right)^{n}= \left( \frac{n+2}{n} \right)^{n}
> $$
> 
> Observe that for any $n\geq 1$, $\frac{n+2}{n}>1$, thus by ![[Sequence#^fcd59a]]
> it follow that $\langle a_n \rangle_{n=1}^{\infty}$ is divergent.
>
>It is wrong because when $n\to \infty$, $1+\frac{2}{n}\to 1$. It is a tug of war indeterminate form $1^{\infty}$. From the theorem the base $r$ must be a fixed constant!

> [!remark]
> We can use L'Hospital's Rule to solve this problem

3)
Determine whether the sequence is monotonic. 

(a) $a _ { n } = { \frac { 2 n - 3 } { 3 n + 4 } }$ 

Consider the function $f(x)= \frac{2x-3}{3x+4}$

$$
\begin{align}
f'(x)&= \frac{2(3x+4)-3(2x-3)}{(3x+4)^{2}} \\
&= \frac{-1}{(3x+4)^{2}}
\end{align}
$$

Since $(3x+4)^{2}\geq 0$. Thus, it follow that $f(x)$ is decreasing implies that the sequence $\langle a_n \rangle_{n=1}^{\infty}$ is decreasing.

(b*) $a _ { n } = n e ^ { - n }$ 

It is a exponential sequence. Thus, we use the third method (ratio):

$$
\begin{align}
\frac{a_{n+1}}{a_{n}}&= \frac{(n+1)e^{-(n+1)}}{ne^{-n}} \\
&= \frac{n+1}{n} \cdot e^{-n-1+n} \\
&= \frac{n+1}{n}\cdot e^{-1} \\
&= \frac{n+1}{ne} \\
\end{align}
$$

For $n\geq 1$, $0<n+1<2n<ne$. Thus,
$$
\frac{a_{n+1}}{a_{n}}<1
$$

Thus, $a_{n}$ is monotonic (decreasing).

(c) $a _ { n } = \tan ^ { - 1 } n$ 

Consider the function $f(x)=\tan ^{-1}x$. Note that

$$
\begin{align}
f'(x)&= \frac{1}{1+x^{2}} \\
&\geq 0
\end{align}
$$

Since $f'(x)\geq 0$, it follow that $f(x)$ is increasing. Thus, the sequence is monotonic (increasing).

A sequence $\langle a _ { n } \rangle _ { n = 1 } ^ { \infty }$ is recursively defined by 

$$
a _ {1} = \sqrt {2} \quad \text { and } \quad a _ {n + 1} = \sqrt {2 + a _ {n}} \text {   for   all   } n \geq 1.
$$

(a) Show that $\langle a _ { n } \rangle _ { n = 1 } ^ { \infty }$ is increasing. 

(b) Show that $a _ { n } < 2$ for all $n \geq 1$ 

(c) Deduce that $\langle a _ { n } \rangle _ { n = 1 } ^ { \infty }$ is convergent and find its limit. 

5*) A sequence $\langle a _ { n } \rangle _ { n = 1 } ^ { \infty }$ is recursively defined by 

$$
a _ {1} = 2 \quad \text { and } \quad a _ {n + 1} = \frac {1}{3 - a _ {n}} \text {   for   all   } n \geq 1.
$$

(a) Show that $0 < a _ { n } \le 2$ for all $n \geq 1$ 

We show using mathematical induction. Let $P(n)$ be property defined as
$$
P(n):0<a_{n}\leq 2
$$

For base step, $P(1)$ is true because $0<2\leq 2\implies 0< a_{1}\leq 2$.

For induction step. suppose $n$ is an arbitrary positive integer and $P(n)$ is true. Thus,

$$
\begin{align}
a_{n+1}&= \frac{1}{3-a_{n}}
\end{align}
$$
By IH, it follow that 
$$
\begin{matrix}
0<a_{n}< 2 \\
-2<-a_{n}<0 \\
1<3-a_{n}<3 \\
\frac{1}{3}< \frac{1}{3-a_{n}}< 1 \\
\frac{1}{3}<a_{n+1}<1 \\
0<a_{n+1}<2
\end{matrix}
$$
Thus,  $P(n+1)$ is true.

Therefore, $P(n)$ is true for all $n\in \mathbb{Z}^{+}$.

(b) Show that $\langle a _ { n } \rangle _ { n = 1 } ^ { \infty }$ is decreasing. 

We argue by mathematical induction. Let $P(n)$ be the property that
$$
P(n): a_{n} \text{ is decreasing}
$$

For basis step, $a_{2}= \frac{1}{3-a_{1}}= 1$. Thus, $a_{2}=1<2=a_{1}$. Hence, $P(2)$ holds. 

For induction step, suppose $n$ is arbitrary positive integer and $P(n)$ is true. By IH, we know that
$$
\begin{matrix}
a_{n-1}>a_{n} \\
-a_{n}>-a_{n-1} \\
3-a_{n}>3-a_{n-1} \\
\frac{1}{3-a_{n}}< \frac{1}{3-a_{n-1}} \\
a_{n+1}<a_{n}
\end{matrix}
$$
Thus, $P(n+1)$ is true. Hence, $P(n)$ is true for all $n\in \mathbb{Z}^{+}$.

> [!remark]
> Since $a_{n+1}$ is depend on $a_{n}$ and $a_{n}$ is depend on $a_{n-1}$. Thus, we can use the inequality of $a_{n}<a_{n-1}$ to deduce $a_{n+1}<a_{n}$


(c) Deduce that $\langle a _ { n } \rangle _ { n = 1 } ^ { \infty }$ is convergent and find its limit. 


6) Suppose the n-th partial sum $s _ { n }$ of a series $\sum _ { i = 1 } ^ { \infty } a _ { i }$ is given by $s _ { n } = 3 - { \frac { n } { 2 ^ { n } } }$ . Determine the sequence $\langle a _ { i } \rangle _ { i = 1 } ^ { \infty }$ and the sum of the series $\sum _ { i = 1 } ^ { \infty } a _ { i }$ if it is convergent. 

7) (* ) Suppose a series $\sum _ { i = 1 } ^ { \infty } a _ { i }$ has nonnegative terms (that is, $a _ { i } \geq 0$ for all $i \geq 1 )$ and its partial sums satisfy the inequality $s _ { n } \leq 1 0 0 0$ for all $n \geq 1$ . Justify why the series $\sum _ { n = 1 } ^ { \infty } a _ { n }$ is convergent. 

## Non-standard problems

8) Prove that $\operatorname* { l i m } _ { n \to \infty } { \frac { n } { n + 1 } } = 1$ using the definition. 

9) ==Prove== that if $\langle a _ { n } \rangle _ { n = 1 } ^ { \infty }$ is bounded and $\operatorname* { l i m } _ { n \to \infty } b _ { n } = 0$ , then $\operatorname* { l i m } _ { n \to \infty } ( a _ { n } b _ { n } ) = 0$ 

10) Suppose f is continuous on $[ 0 , \infty )$ and $\operatorname* { l i m } _ { x \to \infty } f ( x ) = 1$ . Is it possible that $\int _ { 0 } ^ { \infty } f ( x ) d x$ is convergent? Justify your answer. 