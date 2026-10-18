How Far can the tortoise go?
A tortoise is 1 meter from the finish line. At each step it walks half of the distance still remaining. (Intuitively it will never reach the finish line) but we learn that the distance traveled which is the geometric series below:

$$
\frac{1}{2}+\frac{1}{4}+\frac{1}{8}+\dots=1
$$

How? (Actually it is something to do with limit, the expression above omit the presence of limit)

> [!definition]
> A series is an expression of the form
> $$
> \sum_{i=1}^{\infty} a_{i}\text{ or }a_{1}+a_{2}+a_{3}+\dots
> $$
> The numbers $a_{1},a_{2},a_{3},\dots$ are called the terms of the series.

> [!remark]
> Series is also called infinite sum of a sequence
> The index $i$ need not to start from 1

> [!definition]
> Given a series $\sum_{i=1}^{\infty}a_{i}=a_{1}+a_{2}+a_{3}+\dots$. Let $s_{n}$ denote its $n-th$ partial sum (sum from first term to $n-th$ term):
> 
> $$
> s_{n}= \sum_{i=1}^{n} a_{i}=a_{1}+a_{2}+\dots+a_{n}
> $$
> [^1]If $\lim_{ n \to \infty }s_{n}=s$, then the series $\sum_{i=1}^{\infty}a_{i}$ is said to be convergent and we write $\sum_{i=1}^{\infty}a_{i}=s$ as the sum of the series.
> 
> Otherwise, if $\lim_{ n \to \infty }s_{n}$ does not exist, then the series is said to be divergent.

[^1]: We view it as a sequence $\langle s_{n} \rangle_{n=1}^{\infty}=s_{1},s_{2},\dots$

So go back the question, the distance travelled by the tortoise approach 1, but never reaches 1.

> [!question]
> So what does $\sum_{i=1}^{\infty}a_{i}=s$ means? It means:
> - The series is convergent (limit exist)
> - The sequence of partial sums $\left\langle s_{n} \right\rangle$ is convergent.
> - $s=\lim_{ n \to \infty }s_{n}$

> [!question]
> If the series $\sum_{i=1}^{\infty}a_{i}$ is convergent and $\sum_{i=1}^{\infty}a_{i}=s$, what is the sum $\sum_{i=3}^{\infty}a_{i}$?
> The answer is $s-a_{1}-a_{2}$ because $s$ is just a finite number.
> 
> what if $\sum_{i=1}^{\infty}a_{i}$ is divergent? Then, $\sum_{i=3}^{\infty}a_{i}$ is still divergent


Example
Show that the series $\sum_{i=1}^{\infty}(-1)^{i}$ is divergent using the definition.

$$
\begin{align}
\sum_{i=1}^{\infty} (-1)^{i}=\lim_{ n \to \infty } s_{n}
\end{align}
$$
where $s_{n}=\sum_{i=1}^{n}(-1)^{i}$.
Notice that
$$
s_{n}= \begin{cases}
0 &\text{if n is even} \\
-1& \text{if n is odd}
\end{cases}
$$

Hence, $\lim_{ n \to \infty }s_{n}$ does not exist because the term oscillate between $-1$ and $0$. Therefore, $\sum_{i=1}^{\infty}(-1)^{i}$ is divergent.

## Telescoping sum
[[The Consecutive Difference Principle (Telescoping Sums)]]

## Standard Laws for Series

If the series $\sum_{i=1}^{\infty}a_{i}$ and $\sum_{i=1}^{\infty}b_{i}$ are convergent, then the series 
$$
\sum_{i=1}^{\infty} ca_{i},\sum_{i=1}^{\infty} (a_{i}+b_{i}),\sum_{i=1}^{\infty} (a_{i}-b_{i})
$$
are convergent.

Furthermore,
1) $\sum_{i=1}^{\infty}ca_{i}=c\sum_{i=1}^{\infty}a_{i}$
2) $\sum_{i=1}^{\infty}(a_{i}+b_{i})=\sum_{i=1}^{\infty}a_{i}+\sum_{i=1}^{\infty}b_{i}$
3) $\sum_{i=1}^{\infty}(a_{i}-b_{i})=\sum_{i=1}^{\infty}a_{i}-\sum_{i=1}^{\infty}b_{i}$

## Geometric Series

> [!theorem]
> The geometric series $\sum_{i=1}^{\infty}ar^{i-r}=a+ar+ar^{2}+\dots$ with initial term $a(\neq 0)$ and common ratio $r$ is convergent if $\lvert r \rvert>1$ and its sum is
> 
> $$
> \begin{align}
> \sum_{i=1}^{\infty} ar^{i-1}= \frac{a}{1-r}, &&|r|<1
> \end{align}
> $$
> 
> If $\lvert r \rvert\geq 1$, the geometric is divergent

Is the series $\sum_{i=1}^{\infty}2^{2i}3^{1-i}$ convergent or divergent?
$$
\begin{align}
\sum_{i=1}^{\infty} 2^{2i}3^{1-i}= \sum_{i=1}^{\infty} 4^{i} \cdot\frac{3}{3^{i}}= 3\sum_{i=1}^{\infty} \left( \frac{4}{3} \right)^{i}= 4\sum_{i=1}^{\infty} \left( \frac{4}{3} \right)^{i-1}
\end{align}
$$
Hence, it is a geometric series with $a=4$ and $r=\frac{4}{3}$. Since $\lvert r \rvert>1$, the series diverge.

> [!remark]
> It need to be $i-1$

$0.5=0.4 \bar{9}$

---

## The Harmonic Series

> [!theorem]
> The harmonic series $\sum_{i=1}^{\infty} \frac{1}{i}$ is divergent

Proof:
Consider the partial sums $s_{2},s_{4},s_{8},s_{16},\dots$

$$
\begin{align}
s_{2}&= 1+ \frac{1}{2} \\
s_{4}&= 1+\frac{1}{2}+\left( \frac{1}{3}+\frac{1}{4} \right) \\
&>1+ \frac{1}{2}+\left( \frac{1}{4}+\frac{1}{4} \right) \\
&=1+ \frac{1}{2}+ \frac{1}{2}=1 +\frac{2}{2} \\
s_{8}&= 1+ \frac{1}{2}+ \left( \frac{1}{3}+\frac{1}{4} \right)+ \left( \frac{1}{5}+\frac{1}{6}+\frac{1}{7}+\frac{1}{8} \right) \\
&> 1+ \frac{1}{2}+ \left( \frac{1}{4}+ \frac{1}{4} \right)+ 4\left( \frac{1}{8} \right) \\
&>1+ \frac{3}{2}
\end{align}
$$

Therefore, by induction we can show that
$$
\begin{align}
s_{2^{k}}\geq 1+ \frac{k}{2} &&\text{for every }k\geq 1
\end{align}
$$

Since $\lim_{ k \to \infty }\left( 1+\frac{k}{2} \right)=\infty$, by comparison $\lim_{ k \to \infty }s_{2^{k}}=\infty$

Note that $\langle s_{n} \rangle_{n=1}^{\infty}$ is an increasing sequence because the series consists of nonnegative terms.

![[Pasted image 20261018212517.png]]

The reason why we need $\langle s_{n} \rangle_{n=1}^{\infty}$ is justified by  [[Sequence#^2faa4a]]

As $\langle s_{2^{k}} \rangle_{n=1}^{\infty}$ is a subsequence of $\langle s_{n} \rangle_{n=1}^{\infty}$ and the latter is increasing, while $\lim_{ k \to \infty }s_{2^{k}}=\infty$, it follow that $\lim_{ n \to \infty }s_{n}=\infty$.

> [!remark]
> If a sequence is convergent, then all its subsequences also converge to the same limit. In this case it is converse.
> 

---

> [!theorem]
> Theorem
> If a series $\sum_{i=1}^{\infty}a_{i}$ is convergent, then $\lim_{ i \to \infty }a_{i}=0$.