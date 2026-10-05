Proof:
We argue by mathematical induction. Let property $P(n)$ be defined as below.
$$
P(n):3^{n}>n^{2}
$$

For basis step, it is clear that $P(1)$ is true because $3^{1}=3>1=1^{2}$ .

For induction step, we suppose $n$ is arbitrary integer for which $n\geq{1}$ and suppose $P(n)$ is true.

$$
\begin{align}
3^{n+1}&=3^{n}\cdot{3} \\
&>n^{2}\cdot{3} \\
&>3n^{2}
\end{align}
$$

We need to show that $3n^{2}>(n+1)^{2}$.


$$
\begin{align}
3n^{2}-(n+1)^{2}&= 3 n^{2}-(n^{2}+2n+1)\\
&=2n^{2}-2n-1 \\
&=2n(n-1)-1
\end{align}
$$
Notice that this expression is less than 0 if $n =1$. Thus, we cannot prove $P(n+1)$ with $P(1)$. Noticed that $P(2)$ is true because $3^{2}=9>4=2^{2}$. Thus, $2n(n-1)-1>0$ when $n\geq 2$
Thus,
$$
3n^{2}>(n+1)^{2}
$$
Therefore,
$$
\begin{array}
\ 3^{n+1}>3n^{2}>(n+1)^{2} \\
3^{n+1}>(n+1)^{2}
\end{array}
$$

Since $P(1)$ and $P(2)$ is true and if $P(n)$ is true, then $P(n+1)$ is true for $n\geq{2}$. Thus, by Principle of Mathematic Induction, $P(n)$ is true for all positive integers.

==Remark==
	The main idea is you have a>b and you need to show a>c thus, you need to show that b>c. Then, you can prove that a>b>c which is a>c.

It is not a proper way to write like this. The proper way:

$$
\begin{align}
2n^{2}-2n-1&\geq 2(2n)-2n-1 \\
&\geq 2n-1\geq 3>0
\end{align}
$$
For basis step, it is clear that $P(1)$ and $P(2)$ are true because...... For induction step, suppose $n$ is an arbitrary integer with $n\geq 2$ 
and $P(n)$ is true. We need to show that...... for $n\geq 2$

The generalize mathematical induction
Question: show ...... for $n\geq 1$
Show $P(1),P(2),\dots,P(l)$ is true where $1\leq l\leq n$. Then assume $P(n)$ is true for $n\geq l$, then show that $P(n+1)$ is true.


==Another Approach==
We need to show the relationship $3^{n}$ between $n^{2}$
if we express $3^{n}$ as binomial term and we expand it using binomial theorem then the coefficient is $\dfrac{n!}{k(n-k)!}$



$$(a + b)^n = \sum_{k=0}^{n} \binom{n}{k} a^{n-k} b^k$$

Setting $a=1$ and $b=2$:

$$3^n = (1 + 2)^n = \binom{n}{0}2^0 + \binom{n}{1}2^1 + \binom{n}{2}2^2 + \dots + \binom{n}{n}2^n$$

Let's look at the first three terms of this sum (for $n \ge 2$):

1. **Term 0:** $\binom{n}{0} = 1$
2. **Term 1:** $\binom{n}{1}2 = 2n$
3. **Term 2:** $\binom{n}{2}2^2 = \frac{n(n-1)}{2} \cdot 4 = 2n(n-1) = 2n^2 - 2n$

### **The Comparison**

Since all terms in the binomial expansion are positive, we can say:

$$3^n > (\text{Term 1}) + (\text{Term 2})$$

$$3^n > 2n + (2n^2 - 2n)$$

$$3^n > 2n^2$$

Since $2n^2$ is obviously greater than $n^2$ for all $n \geq 1$, we have a very strong proof that:

$$3^n > 2n^2 > n^2$$
Q2
Proof:
We argue by mathematical induction. We suppose a sequence $$a_{1},a_{2},a_{3},\dots \text{ where }a_{1}=5
\text{ and } a_{n+1}=4+a_{n}$$

Let property $P(n)$ defined as follow.
$$
\begin{align}
P(n):a_{n}>4n 
\end{align}
$$

For basis step, it is clear that $P(1)$ is true because $a_{1}=5>4=4(1)$

For induction step, we suppose $n$ is an arbitrary positive integers and $P(n)$ is true. Thus,

$$
\begin{align}
a_{n+1}&=4+a_{n} \\
&>4+4n \text{ (By induction hypothesis)} \\
&>4(n+1)
\end{align}
$$
Thus, $P(n+1)$ is true. By principle of mathematical induction, $P(n)$ is true for all positive integer $n$.

Q3
Proof:
We argue by mathematical induction. Suppose a sequence $a_{0},a_{1},a_{2},\dots$ where $a_{0}=3$ and $a_{n}=(a_{n-1})^{2}$ .Let property $P(n)$ defined as follow.
$$
P(n):a_{n}=3^{2^{n}}
$$
For basis step, it is clear that $P(0)$ is true because $a_{0}=3=3^{2^{0}}$

For induction step, we assume $n$ is an arbitrary integer where $n\geq 0$ and assume $P(n)$ is true. Thus,
$$
\begin{align}
a_{n+1}&=(a_{n+1-1})^{2} \\
&=(a_{n})^{2} \\
&=(3^{2^{n}})^{2} \\
&=3^{2^{n}}\cdot 3^{2^{n}} \\
&=3^{2^{n}+2^{n}} \\
&=3^{2(2^{^{n}})} \\
&=3^{2^{(n+1)}}
\end{align}
$$
Thus, $P(n+1)$ is true. By principle of mathematical induction, $P(n)$ is true for all integer $n\geq 0$.

Q4
Proof:
We argue by mathematical induction. Suppose $x$ is an arbitrary real number for which $x\geq 0$ . Let property $P(n)$ defined as follow.
$$
P(n):(1+x)^{n}\geq 1+nx
$$

For basis step, we need to show that $P(2)$ is true.

---

%% We argue by mathematical induction. Let property $Q(x)$ defined as follow:
$$
(1+x)^{2}\geq 1+2x
$$

For basis step, it is clear that $Q(0)$ is true because $(1+0)^{2}=1\geq 1=1+2(0)$.

For induction step, we assume $Q(x)$ is true. Thus,
$$
\begin{align}
(1+(x+1))^{2}&=x^{2}+4x+4 \\
&=x^{2}+2x+1+2x+3 \\
&=(1+x)^{2}+2x+3 \\
&\geq (1+2x)+2x+3 \text{ (By Induction Hypothesis)} \\
&\geq 4+4x \\
\end{align}
$$
Since $x\geq 0$. Thus, $4+4x\geq 2x+3=1+2(x+1)$. Thus,
$$
(1+(x+1))^{2}\geq 4+4x\geq 1+2(x+1)
$$
It follow that
$$
(1+(x+1))^{2}\geq 1+2(x+1)
$$
Thus, $Q(x+1)$ is true and by Principle of Mathematical Induction, $Q(x)$ is true for $x\geq 0$ %%

==Remark==
We cannot use mathematical induction for real number because we cannot count the next term

--- 

$$
\begin{array}
\ (1+x)^{2}\geq 1+2x \\
1+2x+x^{2}\geq 1+2x
\end{array}
$$
Since $x^2 \ge 0$ for any real number $x$, it follows that $1 + 2x + x^2 \ge 1 + 2x$. Therefore, $(1+x)^2 \ge 1 + 2x$, and the base case holds.


Thus, we show that $P(2)$ is true. For induction step, we assume $n$ is an arbitrary integer for which $n\geq 2$ and assume $P(n)$ is true. Thus,

$$
\begin{align}
(1+x)^{n+1}&=(1+x)^{n}(1+x) \\
&\geq (1+nx)(1+x) \\
&\geq (1+x+nx+nx^{2}) \\
&\geq (1+x(1+n+x)\\
&\geq (1+x(n+1))
\end{align}
$$
Thus, $P(n+1)$ is true and by Principle of Mathematical Induction, $P(n)$ is true for all integer $n$, $n\geq 2$.

==Remark==
This statement is known as **Bernoulli's Inequality** ($n\geq 0$). This inequality is used to prove that the sequence $e_n = (1 + 1/n)^n$ is increasing

We can prove Bernoulli inequality using binomial expansion with the condition of $x\geq 0$. 
Notice that  ^018e17
$$
\begin{align}
(1+x)^{n}=\binom{n}{0}x^{0}+\binom{n}{1}x^{1}+\dots
\end{align}
$$
Notice that the first 2 term of the expansion is $1+nx$ 

Since we assumed $x \ge 0$, then $x^2, x^3, \dots, x^n$ are all non-negative . Since binomial coefficients $\binom{n}{k}$ count combinations, they are always positive integers for $n \ge k$.

Thus we can conclude that 
$$
(1+x)^{n}=1+nx+\dots\geq 1+nx
$$
==Remark==
But notice that Bernoulli inequality is true for $x\geq -1$. Thus, if $x=-1$ the term of binomial expansion will have alternating sign(we cannot say the remaining term is positive in a simple way). 

### Geometric Interpretation

Visually, this inequality describes the relationship between a curve and a line.

- **The Curve:** $y = (1+x)^n$
    
- **The Line:** $y = 1 + nx$
    

For $n \ge 2$, the function $f(t) = (1+t)^n$ is **convex** (it curves upwards). The expression $1+nx$ represents the tangent line to this curve at $x=0$. Because the curve is convex, it always stays **above** its tangent line.

Q5
Proof:
We prove by mathematical induction. Let property $P(n)$ defined as follow.
$$
P(n): \frac{1}{\sqrt{ 1 }}+\frac{1}{\sqrt{ 2 }}+\frac{1}{\sqrt{ 3 }}+\dots+ \frac{1}{\sqrt{ n }}> \sqrt{ n }
$$

==Remark==
$$
P(n):\sum_{k=1}^{n} \frac{1}{\sqrt{ k }}>\sqrt{ n } 
$$

For basis step, $P(2)$ is true because $\frac{1}{\sqrt{ 1 }}+ \frac{1}{\sqrt{ 2 }}> \sqrt{ 2 }$.

For induction step, suppose $n$ is an arbitrary integer with $n\geq 2$ and suppose $P(n)$ is true. Thus,
$$
\begin{align}
\sum_{k=1}^{n+1} \frac{1}{\sqrt{ k }}&=\sum_{k=1}^{n}  \frac{1}{\sqrt{ k }}+ \frac{1}{\sqrt{ n+1 }}  \\
&> \sqrt{ n } + \frac{1}{\sqrt{ n+1 }} \text{ (By Induction Hypothesis)}
\end{align}
$$
We need to show that
$$
\begin{align}
\sqrt{ n }+ \frac{1}{\sqrt{ n+1 }}&> \sqrt{ n+1 } \\
\end{align}
$$
Thus,
$$
\begin{align}
\sqrt{ n }+ \frac{1}{\sqrt{ n+1 }}- \sqrt{ n+1 } &=\sqrt{ n(n+1) }+1-(n+1) \\
&=
\end{align}
$$
But notice that if we make it into a equality we cannot simplify it by square the expression. Thus, we suspect the inequality is true:

$$
\begin{align}
\sqrt{ n }+ \frac{1}{\sqrt{ n+1 }}&\stackrel{?}{>} \sqrt{ n+1 } \\ 
\sqrt{ n(n+1) }+1 & \stackrel{?}{>} n+1 \\
\sqrt{ n^{2}+n }&\stackrel{?}{>}n \\
n^{2}+n&\stackrel{?}{>}n^{2}
\end{align}
$$
Since $n\geq 2$. Thus, $n^{2}+n>n^{2}$. Thus, by the reversing process we can say that 
$$
\begin{align}
\sqrt{ n }+ \frac{1}{\sqrt{ n+1 }}&> \sqrt{ n+1 } \\
\end{align}
$$
Thus,
$$
\begin{align}
\sum_{k=1}^{n+1} \frac{1}{\sqrt{ k }}> \sqrt{ n } + \frac{1}{\sqrt{ n+1 }}> \sqrt{ n+1 } \\
\sum_{k=1}^{n+1} \frac{1}{\sqrt{ k }}>\sqrt{ n+1 }
\end{align}
$$
Thus $P(n+1)$ is true.

==The formal way==
![[Screenshot 2025-12-24 122856.png]]

Alternative method
![[Screenshot 2025-12-24 123147.png]]

Q6
Proof:
We argue by mathematical induction. Suppose a sequence $a_{1},a_{2},a_{3},\dots$ with $a_{1}=1$, $a_{2}=3$  and $a_{n}=a_{n-1}+a_{n-2}$ for positive integer $n\geq 3$

Let property $P(n)$ defined as 
$$
P(n):a_{n}\leq \left( \frac{7}{4} \right)^{n}
$$
For basis step, it is clear that $P(1)$ is true because $1\leq \left( \frac{7}{4} \right)^{1}$  and $P(2)$ is true because $3\leq \left( \frac{7}{4} \right)^{2}$.

For induction step we suppose n is an arbitrary positive integer and $P(k)$ is true for $1\leq k\leq n$. Thus,

$$
\begin{align}
a_{n+1} &=a_{n}+a_{n-1} \\
&\leq \left( \frac{7}{4} \right)^{n}+\left( \frac{7}{4} \right)^{n-1} \\
&\leq \left( \frac{7}{4} \right)^{n}\left( 1+\frac{4}{7} \right) \\
&\leq \left( \frac{7}{4} \right)^{n}\left( \frac{11}{7} \right)
\end{align}
$$
Notice that $\left( \frac{11}{7} \right)  \leq\left( \frac{7}{4} \right)$ Thus,

$$
\begin{align}
a_{n+1}&\leq\left( \frac{7}{4} \right)^{n}\left( \frac{7}{4} \right) \\
&\leq\left( \frac{7}{4} \right)^{n+1}
\end{align}
$$

Thus, $P(n+1)$ is true. By principle of strong mathematical induction. $P(n)$ is true for all positive integer $n\geq 1$.

==Remark==
$a<b$ and $b<c$ thus $a<c$
Why we use strong mathematical induction, because the recursive sequence is depend on previous 2 term.
Why, we need to prove $P(1)$ and $P(2)$ because $n\geq 3$ for the sequence (The tool we use to prove)

7)


