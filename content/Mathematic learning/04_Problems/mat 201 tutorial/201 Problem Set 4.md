
## Standard Problems

1) Determine whether the series is convergent or divergent.

(a) $\sum _ { i = 1 } ^ { \infty } { \frac { 1 + 4 ^ { i } } { 1 + 3 ^ { i } } }$ 

Approach 1:
Consider the series $\sum_{i=1}^{\infty}\left( \frac{4}{3} \right)^{i}$. Note that both series is with positive term, hence we  can use Limit Comparison Test.

$$
\begin{align}
\lim_{ i \to \infty }  \frac{\frac{1+4^{i}}{1+3^{i}}}{\left( \frac{4}{3} \right)^{i}}&= \lim_{ i \to \infty }  \frac{3^{i}(1+4^{i})}{4^{i}(1+3^{i})} \\
&=\lim_{ i \to \infty } \frac{3^{i}+12^{i}}{4^{i}+12^{i}} \\
&= \lim_{ i \to \infty }  \frac{ \left( \frac{1}{4} \right)^{i}+1}{\left( \frac{1}{3} \right)^{i}+1} \\
&=1>0
\end{align}
$$
Since $\sum_{i=1}^{\infty}\left( \frac{4}{3} \right)^{i}$ is divergent, it follow that $\sum_{i=1}^{\infty} \frac{1+4^{i}}{1+3^{i}}$ is divergent.

Approach 2:
Note that
$$
\lim_{ i \to \infty }  \frac{1+4i}{1+3i}= \lim_{ i \to \infty } \frac{\frac{1}{3^{i}}+ \left( \frac{4}{3} \right)^{i}}{\frac{1}{3^{i}}+1}=1
$$
Hence, by Test of Divergence, it follow that $\sum_{i=1}^{\infty} \frac{1+3^{i}}{1+4^{i}}$ is divergent.


(b*) $\sum _ { i = 1 } ^ { \infty } { \frac { 5 + 2 i ^ { 3 } } { ( 1 + i ^ { 2 } ) ^ { 2 } } }$ 

Can we use Test of Divergence here? Cannot because it is clear that the limit of the term go to 0. 

Consider the series $\sum_{i=1}^{\infty} \frac{2}{i^{2}}$. Since both series contain only positive term, hence we can use Limit Comparison Test.

$$
\begin{align}
\lim_{ i \to \infty }  \frac{\frac{5+2i^{2}}{(1+i^{2})^{2}}}{\frac{2}{i^{2}}}&= \lim_{ i \to \infty }  \frac{i^{2}(5+2i^{2})}{2(i^{4}+2i^{2}+1)} \\
&=\lim_{ i \to \infty } \frac{5i^{2}+2i^{4}}{2i^{4}+4i^{2}+2} \\
&= \lim_{ i \to \infty } 1>0
\end{align}
$$

Since, $\sum_{i=1}^{\infty} \frac{1}{i^{2}}$ is convergent by p-series test and so $\sum_{i=1}^{\infty} \frac{2}{i^{2}}$, hence it follow that $\sum_{i=1}^{\infty} \frac{5+2i^{2}}{(1+i^{2})^{2}}$ is convergent by  Limit Comparison Test.

> [!remark]
> Can we use Direct Comparison Test? Try
> $$
> \begin{gathered}
> i^{2}+ 1>i \\
> (i^{2}+1)^{2}>i^{2} \\
> \frac{1}{(i^{2}+1)^{2}}> \frac{1}{i^{2}} \\
> \frac{5+2i^{3}}{(1+i)^{2}}< \frac{5+2i^{3}}{i^{4}}
> \end{gathered}
> $$
> Note that 
> $$
> \frac{5+2i^{3}}{i^{4}}= \frac{5}{i^{4}}+ \frac{2}{i}
> $$
> Note that $\sum_{i=1}^{\infty} \frac{2}{i}$ is divergent while $\sum_{i=1}^{\infty} \frac{5}{i^{4}}$ is convergent. Hence, by [[201 Problem set 3#^6385ca]] $\sum_{i=1}^{\infty} \frac{5+2i^{3}}{i^{4}}$ is diverges. Hence, we cannot compare.


(c) $\sum _ { i = 2 } ^ { \infty } ( - 1 ) ^ { i } \sin \left( { \frac { \pi } { i } } \right)$ 

Let $b_{i}= \sin\left( \frac{\pi}{i} \right)$. Note that $\lim_{ i \to \infty }\sin\left(  \frac{\pi}{i} \right)=0$. For $i\geq 2$,
$\frac{\pi}{i}$ stay in first quadrant, hence
$$
\begin{align}
0< \frac{\pi}{i}< \frac{\pi}{2}
\end{align}
$$
When $i$ increase $\theta=\frac{\pi}{i}$ decrease, since $\sin \theta$ is a increasing function on $\left[ 0, \frac{\pi}{2} \right]$, it follow that $\sin \frac{\pi}{2}$ is decreasing. Formally,
$$
0< \frac{\pi}{i+1}< \frac{\pi}{i}< \frac{\pi}{2}
$$
Since $\sin \theta$ is increasing on this interval, it follow that

$$
\sin \left( \frac{\pi}{i+1} \right)<\sin \left( \frac{\pi}{i} \right)\implies b_{i+1}<b_{i}
$$
Hence, $\langle b_{i} \rangle_{i=1}^{\infty}$ is decreasing. Thus, by Alternating Series Test, it follow that $\sum_{i=1}^{\infty}(-1)^{i}\sin\left( \frac{\pi}{i} \right)$ is convergent.

> [!remark]
> Can we use Ratio Test here? Cannot because the series is conditionally convergent (we will get $L=1$, inconclusive)

(d) $\sum _ { i = 1 } ^ { \infty } { \frac { 1 + \sin i } { 1 0 ^ { i } } }$ 
Note that $-1\leq \sin i\leq 1$. Hence,

$$
\begin{gathered}
0\leq  1+\sin i\leq 2 \\
0\leq \frac{1+\sin i}{10^{i}}\leq \frac{2}{10^{i}}
\end{gathered}
$$
Since $\sum_{i=1}^{\infty} \frac{1}{10^{i}}$ is convergent, it follow that $\sum_{i=1}^{\infty} \frac{2}{10^{i}}$ is convergent. Since, $\frac{1+\sin i}{10^{i}}\geq 0$ , hence by Comparison Test, it follow that $\sum_{i=1}^{\infty} \frac{1+\sin i}{10^{i}}$ is convergent. $\blacksquare$


(e*) $\sum _ { i = 3 } ^ { \infty } ( - 1 ) ^ { i + 1 } { \frac { \ln i } { i } }$ 

> [!remark]
> It is clear that $\lim_{ i \to \infty } \frac{\ln i}{i}=0$  and $\frac{\ln i}{i}$ is decreasing by inspection. Thus we use Alternating Series Test.

Let $b_{i}= \frac{\ln i}{i}$. Note that 

$$
\begin{align}
\lim_{ i \to \infty } \frac{\ln i}{i} &\overset{H}{=} \lim_{ i \to \infty }  \frac{ \frac{1}{x}}{1} \\
&=  0
\end{align}
$$
Consider the function $f(x)= \frac{\ln x}{x}$

$$
\begin{align}
f'(x)&= \frac{1- \ln x}{x^{2}}
\end{align}
$$
$1-\ln x<0\implies \ln x>1\implies x>e^{1}$. Hence when $x>e$, $f'(x)<0$ implies that $f(x)$ is decreasing. Hence $b_{i}$ is increasing also. By Alternating Series Test, $\sum_{i=1}^{\infty} \frac{\ln i}{i}$ is convergent.

(f*) $\sum _ { i = 1 } ^ { \infty } { \frac { \cos ^ { 2 } i } { i ! } }$ 
Note that $0\leq\cos ^{2}i\leq 1$. Hence,

$$
\begin{gathered}
0< \frac{\cos ^{2} i}{i!}\leq \frac{1}{i!}
\end{gathered}
$$

Note that
$$
\frac{1}{i!}\leq \left( \frac{1}{2} \right)^{i-1}
$$
for $i\geq 1$. Since $\sum_{i=1}^{\infty}\left( \frac{1}{2} \right)^{i-1}$ is convergent, by Comparison Test $\sum_{i=1}^{\infty} \frac{1}{i!}$ is convergent.

Hence, by Comparison Test again $\sum_{i=1}^{\infty} \frac{\cos ^{2}i}{i!}$ is convergent.

> [!remark]
> Why we compare with $\left( \frac{1}{2} \right)^{n}$? Try expand:
> $$
> s_{n}=1+ \frac{1}{2}+ \frac{1}{6}+ \frac{1}{n_{1}} \dots< 1+ \frac{1}{2}+ \frac{1}{4}+ \dots+ \left( \frac{1}{2} \right)^{n}
> $$
> Note that the convergence of $\sum_{i=1}^{\infty} \frac{1}{i!}$ can be shown using Ratio Test. 


(g*) $\sum _ { i = 1 } ^ { \infty } { \frac { 1 } { i ^ { 1 + { \frac { 1 } { i } } } } }$ 
Analyze the term: 
$$
\begin{align}
\frac{1}{i}\left(  \frac{1}{i^{1/i}} \right)
\end{align}
$$
$\lim_{ i \to \infty } \frac{1}{i}=0$ and $\lim_{ i \to \infty } \frac{1}{i^{1/i}}=1$ [^1]by inspection . Thus, we cannot use Test of Divergence.

$0\leq \frac{1}{i^{1/i}}\leq1\implies 0\leq \frac{1}{i^{1/i}}\leq \frac{1}{i}$. But $\sum_{i=1}^{\infty} \frac{1}{i^{1/i}}$ is divergent. So we cannot use Comparison Test here.

We cannot use integral test also because it is very hard to integrate.

Try Limit Comparison
We should compare with $b_{i}= \frac{1}{i}$ because $\lim_{ n \to \infty } \frac{1}{i^{1/i}}=1$. Hence,  when $i\to \infty$ , $\frac{1}{i^{1+1/i}}\approx \frac{1}{i}$ .

$$
\begin{align}
\lim_{ i \to \infty }  \frac{\frac{1}{i\cdot i^{1/i}}}{\frac{1}{i}}&= \lim_{ i \to \infty }  \frac{i}{i(i^{1/i})} \\
&= \lim_{ i \to \infty }  \frac{1}{i^{1/i}} \\
&= 1
\end{align}
$$
Since $\sum_{i=1}^{\infty} \frac{1}{i}$ is divergent .Hence, by Limit Comparison Theorem, it follow that $\sum_{i=1}^{\infty} \frac{1}{i^{1+i/1}}$ is divergent.


(h) $\sum _ { i = 1 } ^ { \infty } \sin \left( { \frac { 1 } { i } } \right)$ 

Note that
$$
\lim_{ i \to \infty }  \sin\left( \frac{1}{i} \right)=\sin \left( \lim_{ i \to \infty } \frac{1}{i} \right)=0
$$
We can do this because ![[Sequence#^86c70e]]
Hence, we cannot use Test of Divergence.

Note that $\sum_{i=1}^{\infty} \sin\left( \frac{1}{i} \right)= \sin 1+ \sin \frac{1}{2}+\dots$ . Note that $\sin\left( \frac{1}{i} \right)$ is on domain $\left[ 0, \frac{\pi}{2} \right]$ when $i\geq 2$, and this increasing.

$$
0< \frac{1}{i+1}< \frac{1}{i}< \frac{\pi}{2}
$$
Hence,
$$
\sin\left(  \frac{1}{i+1} \right)< \sin \left( \frac{1}{i} \right)\implies b_{i+1}<b_{i}
$$
Hence $b_{i}= \sin\left( \frac{1}{i} \right)$ is decreasing.

==Correct answer==:
We should use Limit Comparison Theorem to compare with $b_{i}= \frac{1}{i}$. Why? 
Because as $i \to \infty$, the angle $\frac{1}{i} \to 0$. From linear approximation (tangent line at $x=0$) or Taylor series:
$$
\sin x = x - \frac{x^{3}}{3!} + \frac{x^{5}}{5!} - \dots
$$
Unlike as $x \to \infty$ where the highest power dominates, **when $x \to 0$, the lowest power dominates** (for instance, if $x = 0.01$, then $x = 0.01$ is $10{,}000$ times larger than $x^3 = 0.000001$).

Therefore, for small inputs near zero, $\sin x \approx x$. Substituting $x = \frac{1}{i}$:
$$
\sin\left( \frac{1}{i} \right) \approx \frac{1}{i}
$$

Evaluating the limit of their ratio:
$$
\lim_{ i \to \infty } \frac{\sin\left( \frac{1}{i} \right)}{\frac{1}{i}} = 1 > 0
$$
Since the harmonic series $\sum_{i=1}^{\infty} \frac{1}{i}$ is divergent and both series have positive terms, by the Limit Comparison Test, $\sum_{i=1}^{\infty}\sin\left( \frac{1}{i} \right)$ is divergent. $\blacksquare$ 

2*) Show that $\sum _ { i = 1 } ^ { \infty } a _ { i } b _ { i }$ need not be convergent even if both $\sum _ { i = 1 } ^ { \infty } a _ { i }$ and $\sum _ { i = 1 } ^ { \infty } b _ { i }$ are convergent. 

We need to find a counter example. Naturally we think of absolute convergent. We can take some series that is conditionally convergent (with $(-1)^{i}$) and multiply with a conditionally convergent series (with $(-1)^{i}$) , so it become a absolute series and thus diverge.

Consider the alternating $p-$series;
$$
a_{i}=b_{i}= \frac{(-1)^{i}}{i^{p}}
$$
Note that $\sum a_{i}$ is converges by the Alternating Series Test for any $p>0$. The product $a_{i}b_{i}=a_{i}^{2}= \frac{1}{i^{2p}}$ which diverges by the p-series test whenever the exponent satisfies $2p\leq 1$. Thus, we can choose $p\leq 0.5$. For example:

$$
a_{i}=b_{i}= \frac{(-1)^{i}}{\sqrt{ i }}
$$
Both $\sum_{i=1}^{\infty} a_{i}$ and $\sum_{i=1}^{\infty} b_{i}$ converge by the Alternating Series Test. However, their product:
$$
\sum_{i=1}^{\infty} a_{i}b_{i} = \sum_{i=1}^{\infty} \frac{1}{i}
$$
is the harmonic series, which diverges. $\blacksquare$

3) Determine whether the series is absolutely convergent, conditionally convergent, or divergent. 
(a) $\sum _ { i = 1 } ^ { \infty } { \frac { \sin ( 4 i ) } { i ^ { 2 } } }$ 

We cannot use Test of Divergent because $\lim_{ i \to \infty } \frac{\sin(4i)}{i^{2}}=0$. Note that
$$
\begin{gathered}
0\leq \lvert \sin (4i) \rvert\leq 1 \\
0\leq \left\lvert  \frac{\sin(4i)}{i^{2}}  \right\rvert\leq \frac{1}{i^{2}}
\end{gathered}
$$
Since $\sum_{i=1}^{\infty} \frac{1}{i^{2}}$ is convergent, it follow that by Comparison Test $\sum_{i=1}^{\infty} \frac{\sin(4i)}{i^{2}}$ is absolute convergent and thus convergent.

(b*) $\sum _ { i = 2 } ^ { \infty } { \frac { ( - 1 ) ^ { i } } { \ln i } }$ 

1. **Check for Absolute Convergence:**
Consider the series of absolute values:
$$
\sum_{i=2}^{\infty}\lvert a_{i} \rvert = \sum_{i=2}^{\infty} \frac{1}{\ln i}
$$
Recall that $\ln i < i$ for all $i \geq 2$. Therefore:
$$
\frac{1}{\ln i} > \frac{1}{i} > 0
$$
Since the harmonic series $\sum_{i=2}^{\infty} \frac{1}{i}$ is divergent, by the Direct Comparison Test, $\sum_{i=2}^{\infty} \lvert a_{i} \rvert$ is divergent. Thus, the series is **not** absolutely convergent.

2. **Check for Conditional Convergence:**
Consider the alternating series with $b_{i} = \frac{1}{\ln i} > 0$:
- $\lim_{ i \to \infty } b_{i} = \lim_{ i \to \infty } \frac{1}{\ln i} = 0$
- Since $\ln(i+1) > \ln i$, we have $\frac{1}{\ln(i+1)} < \frac{1}{\ln i} \implies b_{i+1} < b_{i}$ (strictly decreasing for all $i \geq 2$).

By the Alternating Series Test, $\sum_{i=2}^{\infty} \frac{(-1)^{i}}{\ln i}$ is convergent.

**Conclusion:**
Since $\sum_{i=2}^{\infty} a_{i}$ converges but $\sum_{i=2}^{\infty} \lvert a_{i} \rvert$ diverges, the series $\sum_{i=2}^{\infty} \frac{(-1)^{i}}{\ln i}$ is **conditionally convergent**. $\blacksquare$

> [!remark]
> $\ln i$ growth slower than the line function


4) (a) Determine the convergence of the series $\sum _ { i = 2 } ^ { \infty } { \frac { ( - 1 ) ^ { i } i } { \sqrt { i ^ { 3 } + 2 } } }$ 

Let $b_{i}= \frac{i}{\sqrt{ i^{3}+2 }}$. Note that
$$
\begin{align}
\lim_{ i \to \infty }  \frac{i}{\sqrt{ i^{3}+2 }}&=\lim_{ i \to \infty } \frac{\frac{i}{\sqrt{ i^{3} }}}{\frac{\sqrt{ i^{3}+2 }}{\sqrt{ i^{3} }}} \\
&=\lim_{ i \to \infty } \frac{\frac{1}{\sqrt{ i }}}{\sqrt{ 1+ \frac{2}{i^{3}} }} \\
&= 0
\end{align} 
$$

> [!warning]
> And consider the 
> $$
> \begin{align}
>  \frac{a_{i+1}}{a_{i}} &=\frac{\frac{i+1}{\sqrt{ (i+1)^{3}+2 }}}{\frac{i}{\sqrt{ i^{3}+2 }}} \\
>  &= \frac{(i+1)\sqrt{ i^{3}+2 }}{i\sqrt{ ((i+1)^{3}+2) }} \\
>  &= \frac{\sqrt{ (i+1)^{2}(i^{3}+2) }}{\sqrt{ i^{2}(i+1)^{3}+2i^{2} }} \\
> \end{align}
> $$
> It is a messy here, why it is $\frac{a_{i+1}}{a_{i}}$ is not suitable here? Because it is suitable for factorials or discrete product chains.

For root and rational, use derivative test. Consider the function $f(x)= \frac{x}{\sqrt{ x^{3}+2 }}$. But it is very hard to find its derivative. How about we square it?
For $f(x)>0$, $f(x)$ is decreasing iff $[f(x)]^{2}$ is decreasing ^546c70
[[Trichotomy Law Monotonicity to Injectivity]]

Hence,
$$
\begin{align}
\frac{d}{dx}[f(x)]^{2}&= \frac{d}{dx} \frac{x^{2}}{x^{3}+2} \\
&= \frac{2x(x^{3}+2)-3x^{2}(x^{2})}{(x^{3}+2)^{2}} \\
&= \frac{2x^{4}+4x-3x^{4}}{(x^{3}+2)^{2}} \\
&= \frac{-x^{4}+4x}{(x^{3}+2)^{2}} \\
&= \frac{-x(x^{3}-4)}{(x^{3}+2)^{2}}
\end{align}
$$
Note that $\frac{d}{dx}[f(x)]^{2}<0$, when $x\geq 2$. Hence it is decreasing and thus $f(x)$ is decreasing and thus $\sum_{i=1}^{\infty} \frac{i}{\sqrt{ i^{3}+2 }}$ is decreasing. By Alternating Series Test, it follow that $\sum_{i=1}^{\infty} \frac{i}{\sqrt{ i^{3}+2 }}$ is convergent. $\blacksquare$


(b) Determine the convergence of the series $\sum _ { i = 2 } ^ { \infty } { \frac { i } { \sqrt { i ^ { 3 } + 2 } } }$ 

(c) Deduce whether the series $\sum _ { i = 2 } ^ { \infty } { \frac { ( - 1 ) ^ { i } i } { \sqrt { i ^ { 3 } + 2 } } }$ is absolutely convergent, conditionally convergent, or divergent. 

5*) (a) Produce an example of a conditionally convergent series $\sum _ { i = 1 } ^ { \infty } a _ { i }$ such that $\sum _ { i = 1 } ^ { \infty } i a _ { i }$ is convergent. 

My idea: $\sum_{i=1}^{\infty}a_{i}$ is conditionally convergent, thus there must be something to do with the alternating series. A classic example $\sum_{i=1}^{\infty}(-1)^{i+1}\left( \frac{1}{i} \right)$ is conditionally convergent. But notice that when multiply with $i$, it become $\sum_{i=1}^{\infty}(-1)^{i+1}$ which is divergent by Test of Divergence. How about we we consider $\frac{1}{i^{2}}$? Cannot because it is absolutely convergent.

Consider the series of 3(b) $\sum _ { i = 2 } ^ { \infty } { \frac { ( - 1 ) ^ { i } } { \ln i } }$, it is also conditionally convergent. how about we multiply with $i$, then it is definitely divergent because $\lim_{ i \to \infty } \frac{i}{\ln i}$ is not 0 so do$\lim_{ i \to \infty } (-1)^{i+1} \frac{i}{\ln i}$. But how about we divide the original series with $i$ first?

Consider the series of 3(b) $\sum _ { i = 2 } ^ { \infty } { \frac { ( - 1 ) ^ { i } } { i\ln i } }$  as $\sum_{i=1}^{\infty}a_{i}$. Note that
$$
\sum_{i=1}^{\infty} ia_{i}= \sum_{i=1}^{\infty}  \frac{(-1)^{i+1}}{\ln i}
$$
which is proven convergent from 3(b). Now consider $\sum_{i=1}^{\infty}a_{i}$. It is clear that by Alternating Series Test $\sum_{i=1}^{\infty}a_{i}=\sum_{i=1}^{\infty} \frac{(-1)^{i+1}}{i \ln i}$ is convergent.

Now we need to show $\sum_{i=1}^{\infty}\lvert a_{i} \rvert=\sum_{i=1}^{\infty} \frac{1}{i\ln i}$ is not convergent.

Since it contains $\ln i$, it is better we use Integral Test. Consider the function $f(x)= \frac{1}{x\ln x}$, it is clear that $f(x)$ is positive, decreasing and continuous for $x\geq 2$. Hence,

$$
\begin{align}
\int_{2}^{\infty}  \frac{1}{x\ln x}  \, dx &=\lim_{ t \to \infty } \int_{2}^{t} \frac{1}{x\ln x} \, dx  \\
&= \lim_{ t \to \infty } [\ln(\ln x)]^{t}_{2}  \\
&= \lim_{ t \to \infty } (\ln(\ln t)-\ln(\ln 2)) \\
&=\infty
\end{align}
$$

Hence, by integral test $\sum_{i=1}^{\infty} \lvert a_{i} \rvert$ is divergent. Hence, $\sum_{i=1}^{\infty}a_{i}$ is conditionally convergent.

> [!insight] Pedagogical Intent & The "Twilight Zone" of Convergence
> **1. Why did the lecturer ask this?**
> Most students naively assume that multiplying terms by $i$ *always* destroys convergence because it makes terms $i$ times larger (as in $i \cdot \frac{(-1)^i}{i} = (-1)^i$). This problem shatters that assumption, proving that conditional convergence has infinite shades of depth: a series can decay fast enough that multiplying by $i$ still converges by AST, while its absolute sum remains divergent!
> 
> **2. The Hierarchy of Decay Rates:**
> Notice where $\frac{1}{i \ln i}$ sits relative to $p$-series:
> - Any positive power $i^\epsilon$ (even $i^{0.1}$) grows vastly faster than $\ln i$ ($i^{0.1} \gg \ln i$).
> - Therefore, the denominators satisfy $i < i \ln i < i^{1.1}$, which inverts the fractions into:
>   $$
>   \frac{1}{i} > \frac{1}{i \ln i} > \frac{1}{i^{1.1}}> \frac{1}{\ln i} \quad (\text{for large } i)
>   $$
> - While $\sum \frac{1}{i^{1.1}}$ converges ($p = 1.1 > 1$) and $\sum \frac{1}{i}$ diverges ($p = 1$), the series $\sum \frac{1}{i \ln i}$ lives right in the razor-thin "twilight zone"—decaying faster than the harmonic series, yet still divergent!

(b) Produce an example of a conditionally convergent series $\sum _ { i = 1 } ^ { \infty } a _ { i }$ such that $\sum _ { i = 1 } ^ { \infty } i a _ { i }$ is divergent. 

Let $a_{i}= (-1)^{i+1}\left( \frac{1}{i} \right)$.
## Non-standard Problems

6*) Prove that if $\sum _ { i = 1 } ^ { \infty } a _ { i }$ and $\sum _ { i = 1 } ^ { \infty } b _ { i }$ are both convergent series with positive terms, then $\sum _ { i = 1 } ^ { \infty } a _ { i } b _ { i }$ must be convergent. (Compare this with Problem 2.) 

Proof:
Since $\sum_{i=1}^{\infty}b_{i}$ is convergent, it follow that $\lim_{ i \to \infty }b_{i}=0$. Hence, by definition of the limit, there exists an integer $N$ such that for all $i\geq N$,
$$
0< b_{i}<1
$$
Since $a_{i}>0$, we can multiply the inequality by $a_{i}$. (This is the crucial part why we need $a_{i}$, $b_{i}$ to be positive). Hence,

$$
0< a_{i}b_{i}<a_{i}
$$
Hence, by Direct Comparison Test, since $\sum_{i=1}^{\infty}a_{i}$ is convergent, it follow that $\sum_{i=1}^{\infty}a_{i}b_{i}$. $\blacksquare$

[^1]:  $\lim_{ i \to \infty }i^{1/i}$=1 because $e^{\ln i^{1/i}}=e^{\frac{\ln i}{i}}$ and  by L'Hospital's Rule the limit is $e^{0}=1$ [[Absolute Convergence and the Ratio and Root Tests#^3c46ba]]
