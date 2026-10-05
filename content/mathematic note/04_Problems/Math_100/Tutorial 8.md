Q1
a) $(-1)^{n}(n-1)$ for all integer $n\geq 1$

b)  $\dfrac{n}{(n+1)^{2}}$ for all integer $n\geq 1$

c) $\dfrac{1}{n}-\dfrac{1}{n+1}$ for all integer $n\geq 1$

Q2
a) $\sum_{i=1}^{7}(-1)^{i+1}(i)^{2}$ 

b) $\prod_{i=1}^{9} \dfrac{2i}{(i+1)!}$

c) $\prod_{i=1}^{11}(1-x^{i})$

d) $\sum_{i=1}^{99}(-1)^{i+1}(i^{3}-1)$

Q3
$$
\begin{align}
\sum_{k=1}^{99} [\sin(k+1)-\sin k] =&\sin(2)-\sin(1)\\
+&\sin(3)-\sin(2) \\
+&\dots \\
+&\sin(99)-\sin(98) \\
+&\sin(100)-\sin(99)  \\ \\

=&\sin(100)-\sin(1)
\end{align}
$$
Q4
a)
If we write out the terms of the left side, we get a series of pairs:

$$(a_1 + b_1) + (a_2 + b_2) + (a_3 + b_3) + \dots + (a_n + b_n)$$

Since addition is commutative (you can change the order) and associative (you can change the grouping), we can move all the $a$ terms to the front and all the $b$ terms to the back:

$$(a_1 + a_2 + \dots + a_n) + (b_1 + b_2 + \dots + b_n)$$

Each group is simply the definition of the individual summations:

$$\sum_{k=1}^{n} a_k + \sum_{k=1}^{n} b_k$$

Q4$a_{2}$ 
$$\sum_{k=1}^{n} (ca_k) = c \sum_{k=1}^{n} a_k$$

Let's expand the summation on the left:

$$(ca_1) + (ca_2) + (ca_3) + \dots + (ca_n)$$

Notice that every single term has a common factor of $c$. According to the distributive property (factoring), we can pull the $c$ out of the entire expression:

$$c(a_1 + a_2 + a_3 + \dots + a_n)$$

The expression inside the parentheses is exactly the definition of $\sum_{k=1}^{n} a_k$. Therefore:

$$c \sum_{k=1}^{n} a_k$$

b) 
$$
\begin{align}
\sum_{k=1}^{100} (k^{2}+4k+3)&=\sum_{k=1}^{100} k^{2}+\sum_{k=1}^{100} 4k+\sum_{k=1}^{100} 3 \\
&=\frac{100(100+1)[2(100)+1]}{6}+4\left( \frac{100(99)}{2} \right)+3(100) \\
&=338350+19800+300 \\
&=358450
\end{align}
$$

Q5
$$
\begin{align}
\prod_{k=1}^{99} \frac{k}{k+2}&=\frac{1}{3}\left( \frac{2}{4} \right)\left( \frac{3}{5} \right) \left( \frac{4}{6} \right)\left( \frac{5}{7} \right)\dots\left( \frac{97}{99} \right)\left( \frac{98}{100} \right)\left( \frac{99}{101} \right) \\
&=\frac{1(2)}{100(101)} \\
&=\frac{1}{50(101)} \\
&=\frac{1}{5050}
\end{align}
$$

6)
Proof:
Let property $P(n)$ defined as below:
$$
P(n):1+6+11+\dots+(5n-4)=\frac{n(5n-3)}{2}
$$
We argue by mathematical induction.

For basic step, it is clear that $P(1)$ is true because $[5(1)-4]=1=\dfrac{1(5(1)-3)}{2}$

For induction step, assume $n$ is arbitrary positive integer and assume $P(n)$ is true. Thus,
$$
\begin{align}
1+6+11+\dots+(5n-4)+(5(n+1)-4)&=\frac{n(5n-3)}{2}+(5n+1) \\
&=\frac{n(5n-3)+2(5n+1)}{2} \\
&=\frac{5n^{2}-3n+10n+2}{2} \\
&=\frac{5n^{2}+7n+2}{2} \\
&=\frac{(5n+2)(n+1)}{2} \\
&=\frac{(n+1)(5(n+1)-3)}{2}
\end{align}
$$
Therefore $P(n+1)$ is true. Therefore, by the Principle of Mathematical Induction, we conclude that P(n) is true for all positive integers n.

Q7
Proof:
We argue by mathematical induction. Let property $P(n)$ be defined as below:
$$
P(n):\sum_{k=1}^{n} k^{3}=\left[ \frac{n(n+1)}{2} \right]^{2}
$$
For basis step, it is clear that $P(2)$ is true because $2^{3}=8=\left[ \dfrac{2(2+1)}{2} \right]^{2}$


For induction step, assume $n$ is an arbitrary positive integer and assume $P(n)$ is true. Thus,

$$
\begin{align}
\sum_{k=1}^{n+1} k^{3}&=\sum_{k=1}^{n}k^{3}+(n+1)^{3}   \\
&=\left[ \frac{n(n+1)}{2} \right]^{2}+(n+1)^{3} \\
&=\frac{n^{2}(n+1)^{2}}{4}+\frac{4(n+1)^{2}(n+1)}{4} \\
&= \frac{(n+1)^{2}[n^{2}+4(n+1)]}{4} \\
&=\frac{(n+1)^{2}(n^{2}+4n+4)}{4} \\
&=\frac{(n+1)^{2}(n+2)^{2}}{4} \\
&=\left[ \frac{(n+1)^{2}((n+1)+1)}{2} \right]^{2}
\end{align}
$$
Therefore $P(n+1)$ is true. Therefore, by the Principle of Mathematical Induction, we conclude that P(n) is true for all positive integers $n\geq 2$.

Q8
Proof:
We argue by mathematical induction, let property $P(n)$ be defined as follow:
$$
\begin{align}
P(n): \frac{4}{3}+\frac{9}{8}+\dots+\frac{n^{2}}{n^{2}-1}&=n -\frac{1}{4}- \frac{2n+1}{2n(n+1)} \\ 
\sum_{k=2}^{n} \frac{k^{2}}{k^{2}-1}&= n-\frac{1}{4}-\frac{2n+1}{2n(n+1)} \\
\end{align}
$$

For basis step, it is clear $P(1)$ is true because 
$$
\sum_{k=2}^{1} \frac{k^{2}}{k^{2}-1}=0=1-\frac{1}{4}-\frac{2(1)+1}{2(1)(1+1)} 
$$

For inductive step, suppose $n$ is an arbitrary positive integer and $P(n)$ is true. Thus,

$$
\begin{align}
\sum_{k=2}^{n+1} \frac{k^{2}}{k^{2}-1}&=\sum_{k=2}^{n} \frac{k^{2}}{k^{2}-1}+\frac{(n+1)^{2}}{(n+1)^{2}-1} \\
&=n-\frac{1}{4}-\frac{2n+1}{2n(n+1)}+\frac{(n+1)^{2}}{n(n+2)} \\
&=n-\frac{1}{4}-\frac{(2n+1)(n+2)+2(n+1)^{3}}{2n(n+1)(n+2)}  \\
&=n-\frac{1}{4}-\frac{(2n^{2}+5n+2)+2(n^{3}+3n^{2}+3n+1)}{2n(n+1)(n+2)} \\
&=n-\frac{1}{4}- \frac{2n^2 + 4n + 1}{2(n+1)(n+2)} \\
&=(n+1)-\frac{1}{4}-\frac{2n^{2}+4n+1-2(n^{2}+3n+2)}{2(n+1)(n+2)} \\
&= (n+1) - \frac{1}{4} - \frac{2n+3}{2(n+1)(n+2)} \\
&= (n+1) - \frac{1}{4} - \frac{2(n+1)+1}{2(n+1)(n+2)}
\end{align}
$$


Therefore $P(n+1)$ is true. Therefore, by the Principle of Mathematical Induction, we conclude that P(n) is true for all positive integers $n$.

9)
Proof:
We argue by mathematical induction. Let the property $P(n)$ be defined as follow.
$$
P(n):3^{2n}-1 \text{ is divisible by 8}
$$
For basis step, it is clear that $P(0)$ is true because $P(0)=0=3^{2(0)}-1$ is divisible by 8.

For induction step, assume $n$ is arbitrary nonnegative integer and assume $P(n)$ is true. Thus,
$$
\begin{align}
3^{2(n+1)}-1&=3^{2n}\cdot 3^{2}-1 \\
&= 3^{2}(3^{2n}-1)+8 \\
\end{align}
$$
By definition, $3^{2n}-1=8k$ for some integer k. Thus,

$$
\begin{align}
 3^{2}(3^{2n}-1)+8&=3^{2}(8k)+8 \\
&=8(9k+1)
\end{align}
$$
Since $9k+1$ is integer. Thus, $3^{2(n+1)}$ is divisible by 8. Hence $P(n+1)$ is true. Therefore by the Principle of Mathematical Induction, we can conclude that $P(n)$ is true for all positive integer.

10)
Proof:
We argue by mathematical induction