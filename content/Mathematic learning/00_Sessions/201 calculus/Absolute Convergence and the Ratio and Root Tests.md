
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

> [!theorem] The Ratio Test
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

Proof of part 2:
Since $\lim_{ i \to \infty }\left\lvert  \frac{a_{i+1}}{a_{i}}  \right\rvert=L>1$, by the definition of the limit, there exist an index $N$ such that for all $i\geq N$
$$
\begin{align}
\left\lvert  \frac{a_{i+1}}{a_{i}}  \right\rvert&>1 \\
\lvert a_{i+1} \rvert&> \lvert a_{i} \rvert
\end{align}
$$

Note that $\langle \lvert a_{i} \rvert \rangle_{i=1}^{\infty}$ is increasing and $\lvert a_{i} \rvert> 0$ for all $i\geq 1$. Hence $\lim_{ i \to \infty }\lvert a_{i} \rvert \neq 0\implies \lim_{ i \to \infty }a_{i} \neq 0$. Hence by Test of Divergence, the series $\sum_{i=1}^{\infty}a_{i}$ is divergent. $\blacksquare$

> [!remark]
> Don't let the expression scare you. The first part if the ratio is less than 1 , then after some term it will act like the geometric series and $\lvert a_{i} \rvert$ must converges, using the comparison test to show. To do this we need to construct a geometric series with $\lvert r \rvert<1$,  but greater than $L$ (to satisfy the inequality), it is possible by the definition of limit
> 
> If $r>1$ as in part 2, then it is increasing and limit of sequence will never be 0. By test of convergent the series is divergent.

Proof of part 3:
Suppose the series $\sum_{i=1}^{\infty}a_{i}=\sum_{i=1}^{\infty}(-1)^{i+1}$. Note that $\sum_{i=1}^{\infty}\lvert (-1)^{i+1} \rvert=\sum_{i=1}^{\infty}1^{i+1}=1+1+1+\dots$.. Note that the term of the sequence is the function value $f(n)=1$. Hence,
$$
\lim_{ i \to \infty } \left\lvert  \frac{a_{i+1}}{a_{i}}  \right\rvert=1
$$
and it is clear that $\sum_{i=1}^{\infty}a_{i}$ does not exist (diverges) because oscillating between -1 and 1. (Test of Divergence)

Now suppose the series $\sum_{i=1}^{\infty}a_{i}= \frac{1}{i^{2}}$. It is still the same
$$
\lim_{ i \to \infty } \left\lvert  \frac{a_{i+1}}{a_{i}}  \right\rvert= \lim_{ i \to \infty } \frac{i}{i+1}=1
$$

But $\sum_{i=1}^{\infty}a_{i}$ is convergent by p-series test. Hence, it is inconclusive. $\blacksquare$


> [!remark]
> The ratio is $1$, does it mean each term have same value? Constant function? The hypothesis want limit of the ratio, so after some term it act like the constant function, but not for all.

Example Determine whether the series $\sum_{i=1}^{\infty}(-1)^{i} \frac{i^{3}}{3^{i}}$ is convergent or divergent.

Approach 1:
Can we use alternating series?
Since $3^{i}$ growth faster than $i^{3}$, it follow that $\lim_{ i \to \infty } \frac{i^{3}}{3^{i}}=0$. 
Show it
$$
\begin{align}
\lim_{ i \to \infty } \frac{i^{3}}{3^{i}}&\overset{H}{=} \lim_{ i \to \infty } \frac{3i^{2}}{\ln 3 (3^{i})} \\
&\overset{H}{=} \lim_{ i \to \infty } \frac{6i}{\ln 3 \ln 3 (3^{i})} \\
&\overset{H}{=} \lim_{ i \to \infty } \frac{ 6}{(\ln 3)^{3} (3^{i})} \\
&= 0
\end{align}
$$

Check if it is decreasing:
Let $f(x)= \frac{x^{3}}{3^{x}}$
$$
\begin{align}
f'(x)&= \frac{3^{x}3x^{2}-\ln 3(3^{x})x^{3}}{3^{2x}} \\
&= \frac{3^{x}x^{2}(3- x\ln 3)}{3^{2x}} \\
&= \frac{x^{2}(3-x\ln 3)}{3^{x}}
\end{align}
$$

$3-x\ln 3<0\implies x> \frac{3}{\ln 3}$. Hence when $x> \frac{3}{\ln 3}$ , $f'(x)<0$.
Hence. by alternating series test, the series is convergent.

Approach 2:
Use the Ratio Test. Let $a_{i}=(-1)^{i} \frac{i^{3}}{3^{i}}$. 

$$
\begin{align}
\lim_{ i \to \infty } \left\lvert  \frac{a_{i+1}}{a_{i}}  \right\rvert&= \lim_{ i \to \infty }  \frac{\frac{(i+1)^{3}}{3^{i+1}}}{\frac{i^{3}}{3^{i}}} \\
&=\lim_{ i \to \infty } \frac{(i+1)^{3}}{3^{i+1}} \cdot \frac{3^{i}}{i^{3}} \\
&=\lim_{ i \to \infty } \frac{(i+1)^{3}}{3i^{3}} \\
&=\lim_{ i \to \infty } \frac{1}{3}\left( \frac{i+1}{i} \right)^{3} \\
&= \lim_{ i \to \infty } \frac{1}{3}\left(  1+ \frac{1}{i} \right)^{3} \\
&= \frac{1}{3}<1
\end{align}
$$
Therefore, by the Ratio Test, the series is absolutely convergent and thus convergent.

> [!tip] When to use Alternating Series Test vs. Ratio Test?
> The choice depends on how the terms behave under consecutive division $\left\lvert \frac{a_{i+1}}{a_{i}} \right\rvert$:
> 
> 1. **Use Ratio Test First:**
>    - Best whenever terms involve **factorials ($n!$)** or **exponentials ($c^n$)** (like $3^i$).
>    - Dividing $a_{i+1}$ by $a_{i}$ cancels them cleanly into constants, avoiding tedious derivatives and multiple rounds of L'Hôpital's Rule.
>    - Proves the stronger property of **absolute convergence** directly.
> 
> 2. **Use Alternating Series Test First:**
>    - Best whenever terms consist only of **algebraic powers ($n^p$), roots ($\sqrt{n}$), or logarithms ($\ln n$)** (such as $\sum \frac{(-1)^n}{\sqrt{n}}$ or $\sum \frac{(-1)^n}{n}$).
>    - Pure powers always yield a ratio limit of 1:
>      $$
>      \lim_{n \to \infty} \frac{(n+1)^p}{n^p} = 1
>      $$
>      which makes the Ratio Test completely **inconclusive ($L = 1$)**.

---
# The Root Test

> [!theorem] The Root Test
> 1) If $\lim_{ i \to \infty } \sqrt[i]{ \lvert a_{i} \rvert }=L<1$, then the series $\sum_{i=1}^{\infty}a_{i}$ is absolutely convergent (and therefore convergent).
> 2) If $\lim_{ i \to \infty }\sqrt[i]{ \lvert a_{i} \rvert }=L>1$ or $\lim_{ i \to \infty }\sqrt[i]{ \lvert a_{i} \rvert }=\infty$, then the series $\sum_{i=1}^{\infty}a_{i}$ is divergent.
> 3) If $\lim_{ i \to \infty }\sqrt[i]{ \lvert a_{i} \rvert }=1$, then the Root Test is incpnclusive.

> [!remark]
> For both Ratio and Root Test, it show that when the absolute series decreasing with some rate (both are geometric), then it is convergent.
> 
> One reveal the geometric factor and reveal the geometric base


Proof of Part 1:
Since $L<1$, there exist a number $N$ such that if $i>N$, then

$$
\sqrt[i]{ \lvert a_{i} \rvert }<r
$$
for some $L<r<1$. Hence,  Since $\lvert a_{i} \rvert\geq 0$, and $x^{n}$ is monotonic (or precisely increasing) for all $n\geq1$ in the domain $[0,\infty)$, thus it follow that

$$
\lvert a_{i} \rvert<r^{i}
$$
Since $\lvert r \rvert<1$, thus it follow that the geometric series $\sum_{i=1}^{\infty}r^{i}$ is convergent. By comparison test $\sum_{i=1}^{\infty} \lvert a_{i} \rvert$ is convergent and so $\sum_{i=1}^{\infty}a_{i}$.


Proof of Part 2:
Since $L>1$,  there exist a number $N$ such that if $i>N$, then

$$
\sqrt[i]{ \lvert a_{i} \rvert }>r
$$
for some $1<r<L$. Hence, by the same argument,

$$
\begin{align}
\lvert a_{i} \rvert>r^{i}
\end{align}
$$
Since $r>1$, we have $\lim_{ i \to \infty }r^{i}=\infty$. Hence, $\lim_{ i \to \infty }\lvert a_{i} \rvert \neq 0$ and thus $\lim_{ i \to \infty }a_{i} \neq 0$. Thus, by the Test of Convergence, it follow that $\sum_{i=1}^{\infty}a_{i}$ is divergent.

Proof of Part 3:
Consider the p-series $\sum_{i=1}^{\infty}a_{i}=\sum_{i=1}^{\infty} \frac{1}{i^{2}}$. We have
$$
\lim_{ i \to \infty } \sqrt[i]{ \lvert a_{i} \rvert }=\lim_{ i \to \infty }  \sqrt[i]{ \frac{1}{i^{2}} }=\lim_{ i \to \infty }  \frac{1}{i^{2/i}}=1
$$

Note that $\lim_{ x \to \infty } \frac{1}{x^{2/x}}=\lim_{ x \to \infty }x^{-2/x}$ is an indeterminate form of type $\infty^{0}$. Use the techniques of L'Hospital's Rule.

> [!question] Why it go to 1? (Intuitively)
> $x^{2/x}=e^{\ln}(x^{2/x})=e^{\frac{2\ln x}{x}}$. Hence, since $x$ increase faster than $\ln x$, it follow that limit is $e^{0}=1$

^3c46ba

Also, consider the harmonic series $\sum_{i=1}^{\infty}b_{i}=\sum_{i=1}^{\infty} \frac{1}{i}$. We have, 

$$
\lim_{ i \to \infty } \sqrt[i]{ \frac{1}{i} }=1
$$
However, $\sum_{i=1}^{\infty} \frac{1}{i^{2}}$ is convergent but $\sum_{i=1}^{\infty} \frac{1}{i}$ is divergent. Therefore, the Root Test is inconclusive when the limit is 1. $\blacksquare$

Example 
Determine the convergence of the series $\sum_{i=1}^{\infty} \frac{(-1)^{i}2^{2i}}{i^{i}}$.

We use the root test. Let $a_{i}= \frac{(-1)^{i}2^{2i}}{i^{i}}$. 

$$
\begin{align}
\lim_{ i \to \infty } \sqrt[i]{ \lvert a_{i} \rvert }&=\lim_{ i \to \infty } \sqrt[i]{ \frac{2^{2i}}{i^{i}} } \\
&= \lim_{ i \to \infty }  \sqrt[i]{ \left( \frac{4}{i} \right)^{i}  } \\
&= \lim_{ i \to \infty }  \frac{4}{i} \\
&=0<1
\end{align}
$$

Hence, $\sum_{i=1}^{\infty} \frac{1}{i^{2}}$ is absolutely convergent and thus convergent. $\blacksquare$

> [!remark]
> If $a_{i}$ is in the for $(b_{i})^{i}$, then Root Test is useful

---
# Cesaro Sum

> [!definition]
> The Cesaro sum of a series $\sum_{i=1}^{\infty}a_{i}$ is defined to be
> $$
> \lim_{ k \to \infty }  \frac{1}{k} \sum_{n=1}^{k}s_{n} 
> $$
> where $s_{n}=\sum_{i=1}^{n}a_{i}$ is the $n-$th partial sum.

> [!remark]
> It is like sum the sum and take the average?
> Yes, it is the running arithmetic average of the first $k$ partial sums:
> $$
> \sigma_{k} = \frac{1}{k}\sum_{n=1}^{k} s_{n} = \frac{s_{1} + s_{2} + \dots + s_{k}}{k}
> $$
> 

### Example: Grandi's Series
Consider the oscillating series $\sum_{i=1}^{\infty}(-1)^{i+1} = 1 - 1 + 1 - 1 + \dots$

Its partial sums bounce forever:
$$
s_{1} = 1, \quad s_{2} = 0, \quad s_{3} = 1, \quad s_{4} = 0, \quad \dots
$$

The first few running averages are:
- $\sigma_{1} = \frac{1}{1} = 1$
- $\sigma_{2} = \frac{1+0}{2} = \frac{1}{2}$
- $\sigma_{3} = \frac{1+0+1}{3} = \frac{2}{3}$
- $\sigma_{4} = \frac{1+0+1+0}{4} = \frac{1}{2}$

In general:
- Even terms ($k = 2m$): $\sigma_{2m} = \frac{m}{2m} = \frac{1}{2}$
- Odd terms ($k = 2m+1$): $\sigma_{2m+1} = \frac{m+1}{2m+1} \to \frac{1}{2}$ as $m \to \infty$

Therefore, while Grandi's series diverges in the ordinary sense, its **Cesàro sum is $\frac{1}{2}$**:
$$
\lim_{ k \to \infty } \frac{1}{k}\sum_{n=1}^{k} s_{n} = \frac{1}{2}
$$

