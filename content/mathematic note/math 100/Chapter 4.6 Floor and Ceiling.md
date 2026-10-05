
==Definition==
Given any real number x, the floor of $x$, denoted $\lfloor x \rfloor$, is defined as follows:
$$
\lfloor x \rfloor =n \Leftrightarrow n\leq x<n+1 \text{ for some integer n}
$$
Substitute the $\lfloor x \rfloor=n$ 
$$
\lfloor x \rfloor \leq  x  <\lfloor x \rfloor+1
$$
We can get one property which is $x < \lfloor x \rfloor+1$
From the inequality we know that the floor of x is the greatest integer that less than or equal to x. The greatest integer $n$ here means if $n+1$ which is the next integer will be more than $x$.

==Definition==
Given any real number $x$, the ceiling of $x$, denoted $\lceil x \rceil$, is defined as follows:
$$
\lceil x \rceil =n \Leftrightarrow n-1<x\leq n \text{ for some integer n}
$$
By substitution,

$$
x>\lceil x \rceil -1
$$
From the inequality we know that the floor of x is the smallest integer that greater than or equal to x.

![[Pasted image 20251205145240.png]]


the floor and ceiling will only change when the changed value is an integer. Thus,
$$
\lfloor x+y \rfloor \neq \lfloor x \rfloor +\lfloor y \rfloor 
$$
It is because when the fractional part of x and y is at least 1 then $\lfloor x+y \rfloor>\lfloor x \rfloor+\lfloor y \rfloor$


==Theorem==
For every real number $x$ and every integer $m$, $\lfloor x+m \rfloor=\lfloor x \rfloor+m$


 if m is an integer, then $\lfloor m \rfloor=m=\lceil m \rceil$.


==Theorem 4.6.2 The Floor of $\dfrac{n}{2}$==
For any integer n
$$
\left\lfloor  \frac{n}{2}  \right\rfloor \begin{cases}
\dfrac{n}{2} \text{ if n is even}\\
\dfrac{n-1}{2} \text{ if n is odd}
\end{cases}
$$
Proof:
Suppose n is an arbitrary integer. By quotient remainder theorem, n is either odd or even.

Case 1 (n is odd): In this case, $n =2k+1$ for some integer k. We must show that $\left\lfloor  \dfrac{n}{2}  \right\rfloor=\dfrac{n-1}{2}$ .
$$
\begin{align}
\left\lfloor  \frac{n}{2}  \right\rfloor &=\left\lfloor  \frac{2k+1}{2}  \right\rfloor  \\
&=\left\lfloor  k+\frac{1}{2}  \right\rfloor  \\
&=k
\end{align}
$$
because $k$ is an integer and $k\leq k+\frac{1}{2}<k+1$.
$$
\begin{align}
\frac{n-1}{2}&=\frac{2k+1-1}{2} \\
&=\frac{2k}{2} \\
&=k
\end{align}
$$
Thus, $\left\lfloor  \dfrac{n}{2}  \right\rfloor=k=\dfrac{n-1}{2}$

Case 2 ($n$ is even): In this case, $n =2k$ for some integer k. We must show that $\left\lfloor  \frac{n}{2}  \right\rfloor=\frac{n}{2}$. 
$$
\begin{align}
\frac{n}{2}&=\frac{2k}{2} \\
&=k
\end{align}
$$
$$
\begin{align}
\left\lfloor \frac{n}{2}  \right\rfloor &=\lfloor k \rfloor \\
&=k
\end{align} 
$$
Thus, $\left\lfloor  \dfrac{n}{2}  \right\rfloor=k=\dfrac{n}{2}$. Since, the cases above cover all the possibility, thus we can conclude that the statement is true.


==Theorem==
For all real number x, $\lfloor -x \rfloor=-\lceil x \rceil$
Let $\lceil x \rceil=y$. By definition,
$$
\begin{align}
\ &y-1<x\leq y \\
&=-y+1>-x\geq-y \\
&=-y\leq-x<-y+1 \\
\end{align}
$$

It follow that,
$$
\begin{align}
\ \lfloor -x \rfloor &=-y \\
  \lfloor -x \rfloor  &=-\lceil x \rceil   \text{ by substitution}\\
\end{align}
$$

==Theorem==
For all non-integer x, $\lceil x \rceil=\lfloor x \rfloor+1$

Proof:
if x is a non-integer, then 
$$
\lfloor x \rfloor =n  \Leftrightarrow n\leq x<n+1
$$
for some integer n.

Since $x$ is a non-integer, thus, $x \neq n$. Therefore,

$$n < x < n+1$$

By the definition of the ceiling function, $\lceil x \rceil$ is the smallest integer greater than or equal to $x$. It follow that  $\lceil x \rceil= n+1$.

Thus, by substitution, it follow that $\lceil x \rceil=\lfloor x \rfloor+1$ or $\lfloor x \rfloor=\lceil x \rceil-1$.

