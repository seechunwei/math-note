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

> [!remark]
> Since we have $\lim_{ n \to \infty }s_{n}$ convergent implies $\sum_{i=1}^{\infty}a_{i}$ is convergent and $\lim_{ n \to \infty }s_{n}$ divergent implies $\sum_{i=1}^{\infty}a_{i}$ is divergent. (Thus it is a biconditional statement)
> 

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

^80f337

If the series $\sum_{i=1}^{\infty}a_{i}$ and $\sum_{i=1}^{\infty}b_{i}$ are convergent, then the series 
$$
\sum_{i=1}^{\infty} ca_{i},\sum_{i=1}^{\infty} (a_{i}+b_{i}),\sum_{i=1}^{\infty} (a_{i}-b_{i})
$$
are convergent.

Furthermore,
1) $\sum_{i=1}^{\infty}ca_{i}=c\sum_{i=1}^{\infty}a_{i}$
2) $\sum_{i=1}^{\infty}(a_{i}+b_{i})=\sum_{i=1}^{\infty}a_{i}+\sum_{i=1}^{\infty}b_{i}$
3) $\sum_{i=1}^{\infty}(a_{i}-b_{i})=\sum_{i=1}^{\infty}a_{i}-\sum_{i=1}^{\infty}b_{i}$

> [!remark]
> The converse is not true. For example, let's consider the statement: if $\sum(a_{i}+b_{i})$ converge, then $\sum a_{i}$ and $\sum b_{i}$ must both converge individually.
> 
> Let $b_{i}=-a_{i}$ and say $a_{i}=1$, it is clear that $\sum_{i=1}^{\infty}a_{i}=\infty$ while $\sum_{i=1}^{\infty}b_{i}=-\infty$. But notice that
> 
> $$
> \sum_{i=1}^{\infty} (a_{i}+b_{i})=0
> $$
> which is reveal that the converse is not true.

^e95560

> [!remark]
> But the scalar multiplication part is biconditional provided $c  \neq 0$. [[201 Problem set 3#^eea206]]

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

^4a9158

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
## Necessary condition for convergence

What can we know about the term $\lim_{ n \to \infty }a_{n}$ provided the series is convergent?

When the series is convergent, it means that it converge to one value, it means that it is adding or subtracting a term that get smaller when $n\to \infty$, thus we can say $\lim_{ i \to \infty }a_{n}=0$ provided the series is convergent.

> [!theorem]
> If a series $\sum_{i=1}^{\infty}a_{i}$ is convergent, then $\lim_{ i \to \infty }a_{i}=0$.

Proof:
A series $\sum_{i=1}^{\infty}a_{i}$ is convergent iff the partial sum $S_{n}=\sum_{i=1}^{n}a_{i}$ is converge. By definition, there exist a number $L$ such that
$$
\begin{align}
\lim_{ n \to \infty } S_{n}&=\lim_{ n \to \infty } \sum_{i=1}^{n} S_{n}=L
\end{align}
$$
Notice that $\lim_{ n \to \infty }S_{n}=\lim_{ n \to \infty }S_{n-1}$. And note that $a_{n}=S_{n}-S_{n-1}$. Thus,
$$
\begin{align}
\lim_{ n \to \infty } a_{n}&=\lim_{ n \to \infty } (S_{n}-S_{n-1}) \\
&=L-L \\
&=0 \tag*{$\blacksquare$}
\end{align}
$$

The following useful test is the contrapositive of the theorem. and thus is immediate as a corollary.

> [!theorem] Test for Divergence
> If $\lim_{ i \to \infty }a_{i}$ does not exist or $\lim_{ i \to \infty }a_{i} \neq 0$, then the series $\sum_{i=1}^{\infty}a_{i}$ is divergent.

Example:
Is the series $\sum_{i=1}^{\infty} \frac{i^{2}}{5i^{2}+4}$ convergent or divergent?

Since $\lim_{ i \to \infty } \frac{i^{2}}{5i^{2}+4}=\lim_{ i \to \infty } \frac{1}{5+ \frac{4}{i^{2}}}= \frac{1}{5} \neq 0$. By the Test for Divergence, $\sum_{i=1}^{\infty} \frac{i^{2}}{5i^{2}+4}$ is divergent. 

Example:
Suppose that $\sum_{i=1}^{\infty}a_{i}$ is a convergent series, where $a_{i}\neq 0$ for all $i\geq 1$. Prove that $\sum_{i=1}^{\infty} \frac{1}{a_{i}}$ is a divergent series.

> [!warning]
> Suppose $\sum_{i=1}^{\infty}a_{i}$ is a convergent series, where $a_{i}\neq 0$ for all $i\geq 1$. It follow that $\lim_{ i \to \infty }a_{i}=0$. Note that
> $$
> \begin{align}
> \sum_{i=1}^{\infty} \frac{1}{a_{i}}=\lim_{ n \to \infty } S_{n}= \lim_{ n \to \infty } \sum_{i=1}^{n} \frac{1}{a_{i}} \\
> \end{align}
> $$
> 
> Since $\lim_{ i \to \infty } \frac{1}{a_{i}}=\infty \neq 0$. Thus, by test of divergent it follow that $\sum_{i=1}^{\infty} \frac{1}{a_{i}}$ is divergent.
> 
> There is one flaw in this solution:
> What if $\sum_{i=1}^{\infty}a_{i}$ is a alternating convergent series where it oscillates like $a_{i}= \frac{(-1)^{i}}{i}$. [[Sequence#^9a4c78]].
> 
> 
> Even though $\lim_{ i \to \infty }a_{i}=0$ but we do not know $\lim_{ i \to \infty } \frac{1}{a_{i}}$.
> 

Corrected version:
Assume, for contradiction, that $\lim_{ i \to \infty } \frac{1}{a_{i}}$ exists. Then

$$
1= \lim_{ i \to \infty } \left( \frac{1}{a_{i}}\cdot a_{i} \right)=\lim_{ i \to \infty } a_{i}\cdot \lim_{ i \to \infty } \frac{1}{a_{i}}=0
$$

a contradiction. Hence, $\lim_{ i \to \infty } \frac{1}{a_{i}}$ does not exist. Therefore, by the test for Divergence, $\sum_{i=1}^{\infty} \frac{1}{a_{i}}$ is divergent.

Question
Conversely, if a series $\sum_{i=1}^{\infty}a_{i}$ is divergent, what can you say about the convergence of the sequence $\langle a_i \rangle_{i=1}^{\infty}$?

The sequence can be converge to 0 while the series is divergent. For example,  harmonic series .

The sequence can be of course divergent as well. Or it can be the limit of sequence does not exist like $\lim_{ n \to \infty }(-1)^{n}$.

So we cannot tell anything.