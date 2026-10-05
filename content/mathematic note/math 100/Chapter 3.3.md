#### Argument with Quantified Statement
1) Universal Instantiation Rule: If some property is true for everything in a set, then it is true of any particular thing in the set.
- $\forall x \in D$ such that $Q(x)$ 
- $x_{1} \in D$
- $Q(x)$ is true for $x_{1}$

- $\forall x, P(x)\to Q(x)$
- P(a), for a particular a
- $Q(a)$


Since... is ...., by the universal instantiation rule, Q(x)

what if a particular thing in the set is arbitrary , we can prove a universal statement by defined an arbitrary object in the domain. If we prove that the statement is true for the arbitrary object, then we can conclude that all the element in the set follow the conclusion .


Universal Modus Ponens (UMP)

Assume “ $\forall x \in D,P(x)\to Q(x)$” is true. If $a \in D$ and P(a) is true, then Q(a) is true

Since $a\in D$ , by universal instantiation, it follow that $P(a)\to Q(a)$ is true. Since, $P(a)$ is true by modus ponens $Q(a)$ is true.

Universal Modus Tollens (UMT)

Assume "$\forall x \in D,P(x)\to Q(x)$" is true, if  $\neg Q(a)$ is true for particular a, then $\neg P(a)$ is true.

[Use diagram to show validity of argument]

### Trivial proof
$$
\forall x \in S,Q(x)\implies P(x)
$$
Remember the truth table of a conditional statement, 

1) if $P(x)$ is true for all $x \in S$ then the whole statement is true regardless what is the truth value of $Q(x)$

### Vacuous proof
1) If $Q(x)$ is false for all $x \in S$, then the statement is true regardless what is the truth value of $P(x)$


Example
Let $x \in \mathbb{R}$. Prove that if $x^{3}-5x-1\geq 0$, then $(x-1)(x-3)\geq -2$
$$
\begin{align}
x^{2}-4x+3\geq -2 \\
x^{2}-4x+5 \geq 0 \\ \\
(-4)-4(1)(5)<0
\end{align}
$$
No real root 

$$
\begin{align}
(x-2)^{2}-(-2)^{2}+5=(x-2)^{2}+1> 0
\end{align}
$$
Thus, $(x-1)(x-3)\geq -2$ is true for all $x \in \mathbb{R}$. Thus, the implication statement is true.


Prove that if x, y and z are three real numbers such that $x^{2}+y^{2}+z^{2}<xy+xz+yz$, then $x+y+z> 0$.

To prove this statement we need to know a inequality call AM-GM inequality
$$
\frac{a+b}{2}\geq \sqrt{ ab }
$$

What is arithmetic mean and geometric mean

1) Suppose a arithmetic sequence $a, \dots,b$.

There exists a number between $a$ and $b$ which form a arithmetic sequence. To find that number, we need to find the average (Or what we call midpoint and mean) which is
$$
\frac{a+b}{2}
$$

But how this formula give us the number we want?

Since it is AP, we certainly know that we add or subtract a common difference 2 times to get b from a. Thus, to get the middle number we should add a with the common difference which get from 
$\dfrac{b-a}{2}$.


$$
\begin{align}
a+\frac{b-a}{2}&=\frac{a+b}{2} \\
\frac{2a+b-a}{2}&= \frac{a+b}{2} \\
\frac{a+b}{2}&=\frac{a+b}{2}
\end{align}
$$

2) Suppose a geometric sequence $a, \dots,b$.
How to find the middle number between $a$ and $b$.
We know that $a\times r^{2}=b$. Thus,

$$
\begin{align}
r^{2}&=\frac{b}{a} \\
r&=\pm\sqrt{ \frac{b}{a} }
\end{align}
$$
Thus, to get the middle number
$$
\begin{align}
a\times \pm \sqrt{ \frac{b}{a} }&=\pm\sqrt{ a^{2} \times \frac{b}{a} } \\
&=\pm \sqrt{ ab }
\end{align}
$$


Notice that $\frac{a+b}{2}\geq \sqrt{ ab }$ . Prove.

How to deduce something that result in $\sqrt{ ab }$ and $a+b$ ?
Proof:
Suppose $a$ and $b$ are arbitrary non negative real number

$$
\begin{align}
(\sqrt{ a }-\sqrt{ b })^{2}=a-2\sqrt{ ab }+b
\end{align}
$$

Since $\sqrt{ a }-\sqrt{ b }$ is real number, it follow that $(\sqrt{ a }-\sqrt{ b })^{2}\geq 0$. Thus, it follow that,

$$
\begin{align}
a-2\sqrt{ ab }+b&\geq 0 \\
a+b&\geq 2\sqrt{ ab } \\
\frac{a+b}{2}&\geq \sqrt{ ab }
\end{align}
$$
Q.E.D

==Continue to prove the statement==

Notice that 
$x^{2},y^{2},z^{2}\geq 0$ . Thus, we can apply the result above

$x^{2}+y^{2}\geq 2\sqrt{ x^{2}y^{2} }\geq 2xy$
$x^{2}+z^{2}\geq 2\sqrt{ x^{2}z^{2} }\geq 2xz$
$y^{2}+z^{2}\geq 2\sqrt{ y^{2}+z^{2} }\geq 2yz$

Notice that $\sqrt{ x^{2}y^{2} }=|xy|\geq xy$

Thus, it follow that
$$(x^2 + y^2) + (y^2 + z^2) + (z^2 + x^2) \ge 2xy + 2yz + 2xz$$

$$2x^2 + 2y^2 + 2z^2 \ge 2(xy + yz + xz)$$

$$x^2 + y^2 + z^2 \ge xy + yz + xz$$



Another way to prove from 3.59
Notice that
$$
\begin{align}
a^{2}+b^{2}&=(a-b)^{2}+2ab \\
\end{align}
$$
Since $(a-b)^{2}\geq 0$. It follow that $a^{2}+b^{2}\geq2ab$
