![[mcnugget.png]]==5.43==
[[Cardinality of set]]

5.45
Proof:
Suppose not. There exists nonzero real number $a$ and $b$ such that $\sqrt{ a^{2}+b^{2} }=\sqrt[3]{a^{3}+b^{3}  }$

$$
\begin{align}
(a^{2}+b^{2})^{3}&=(a^{3}+b^{3})^{2} \\
a^{6}+3a^{4}b^{2}+3a^{2}b^{4}+b^{6}&=a^{6}+2a^{3}b^{3}+b^{6} \\

\end{align}
$$
Thus, subtract $a^{6}+b^{6}$ from both side

$$
\begin{align}
3a^{4}b^{2}+3a^{2}b^{4}&=2a^{3}b^{3} \\
3a^{2}b^{2}(a^{2}+b^{2})&=2a^{2}b^{2}(ab) \\ 
\frac{3}{2}&= \frac{ab}{a^{2}+b^{2}} \\
2ab&=3(a^{2}+b^{2}) \\
3a^{2}-2ab+3b^{2}&=0 \\
2a^{2}+2b^{2}+(a^{2}-2ab+b^{2})&=0 \\
2a^{2}+2b^{2}+(a+b)^{2}&=0
\end{align}
$$
This equality only hold if $a=0$ and $b=0$. Contradiction.

5.46
Proof:
Let $f(x)=x^{3}+x^{2}-1$. Notice that $f$ is continuous over real number line, thus it is continuous over interval $\left[ \frac{2}{3},1 \right]$. $f(\frac{2}{3})=$

$$
\frac{8}{27}+\frac{4}{9}-1=-\frac{7}{27}
$$

$$
f(1)=1
$$
Since $f\left( \frac{2}{3} \right)<0<f(1)$, by intermediate value theorem of calculus it follow that there exists a real number $\frac{2}{3}<c<1$ such that $f(c)=0$. Q.E.D.

5.47
Proof:
$T\subset S$, thus all element in $T$ is in $S$, and there exists some element in $S$ that is not in $T$. Let set $W$ defined as below
$W=\{ x \in S\mid x \not\in T \}$
Let $x_{0}$ be the arbitrary element in the set  $W$. Thus, $x_{0} \in W$
Since $x_{0} \not\in T$, it follow that there exists an element in $S$ such that $R(x)$ is true. Thus,

$W=\{ x \in S\mid R(x) \}$.
Q.E.D

5.48
a) $\{ 1,2,3,6 \}$

b)
There exists $n$ distinct positive integers such that each integer divides the sum of the remaining integers.

Let $a$ be an arbitrary integer. Consider the set below
$$
\{ a,2a,3a,6a,12\mathbf{a}.. \}
$$
We can create a sequence which the succeeding term is the sum of terms before. 
Thus, we have $n^{th}$ term of sequence for which each integer is divides the sum of the remaining.

==Why?==
Let $S$ be the total sum of number , and let $a$ be an arbitrary positive integer.
$$
a\mid S-a
$$
It follow that $a\mid a$ and $a\mid S$. Thus, we need to find 4 distinct positive integers that each of them divide the total sum.

Notice that even plus even integer is even, thus we need to prevent using old integer since it will make the total sum become old, but we can use 2 old to become even. 

We can start with 1 since 1 divide every nonzero integer. if we start with 1, then we need another old , lets choose 3

The even integer that can divide 3 is 6, thus the total sum must divide 6, thus we add 2. Thus, we have $\{ 1,2,3 \}$ which $1+2+3=6$.

We need another number to make it divisible by 6, thus $\{ 1,2,3,6 \}$


5.49
Let $a,b,c$ be arbitrary integer in $S$. 
$P(S)=\{ \emptyset,\{ a \},\{ b \},\{ c \},\{ a,b \},\{ a,c \},\{ b,c \},\{ a,b,c \} \}$
We need to find 2 distinct non empty subset of $S$ such that $\sigma_{B}\equiv \sigma_{C}\pmod{ 6}$

The possible residue of modulo 6 is $\{0,1,2,3,4,5 \}$. Thus, there are 6 possible residue while there are 7 possible subset of $S$. Thus, by Pigeonhole principle , there exists 2 distinct subset say $B$ and $C$ such that $\sigma_{B}\equiv \sigma_{c}\pmod{6}$

[[Pigeonhole principle]] ^fa24af

5.51
Proof:
Suppose $n \in \mathbb{Z}$ such that $n\geq 8$. By QR theorem, it follow that $n =3q+r$ for some $q,r \in \mathbb{Z}$ and $0\leq r<3$

Case 1: $n =3q$
Since, $n\geq 8$, it follow that $q\geq 3$. Thus,
$$
\begin{align}
n =3q+5(0)
\end{align}
$$
Thus we can take $a=q$ and $b=0$


Case 2: $n =3q+1$
$$
\begin{align}
n&=3(q-3)+9+1 \\
&=3(q-3)+5(2)
\end{align}
$$
Thus, we can take $a=q-3$ (Notice that $a\geq 0$) and $b=2$

Case 3: $n =3q+2$
$$
\begin{align}
n =3(q-1)+5(1)
\end{align}
$$

Thus, we can take $a=q-1$ and $b=1$.

In every cases $n =3a+5b$ for some $a,b \in \mathbb{Z}$ such that $a,b\geq 0$. Q.E.D.


==Remark==
We cannot use bezou't identity  to prove because it involved negative integer for example
$$
3(2)+5(-1)=1
$$

If you multiply this entire equation by $n$, you get:

$$n = 3(2n) + 5(-n)$$

But notice that $-1< 0$. In fact this we can use non negative integer to form the linear combination of $n$ iff $n\geq 8$. Thus, $n\geq 8$ is the core condition here.

But notice that we can trade term which $3(5)=15$ and $(5)(3)=15$.

Thus,
the coefficient of a: $a=2n-5k$
the coefficient of b: $b=-n+3k$

- **Condition 1 ($a \ge 0$):**

$$2n - 5k \ge 0 \implies 5k \le 2n \implies k \le \frac{2n}{5}$$
- **Condition 2 ($b \ge 0$):**
$$-n + 3k \ge 0 \implies 3k \ge n \implies k \ge \frac{n}{3}$$
**So, the proof boils down to this:**

Does there always exist an integer $k$ in the interval $[\frac{n}{3}, \frac{2n}{5}]$?

The length of this interval is $\frac{2n}{5} - \frac{n}{3} = \frac{6n - 5n}{15} = \frac{n}{15}$.

For an interval to guarantee containing at least one integer, its length usually needs to be close to 1.

When $n =1$
![[mcnugget.png]]

when $n =3$
![[mcnugget1.png]]

Since $n =3$ work , why the minimum number is $8$. Because $n =4$ does not work , in fact this equality work for all $n$ when $n\geq 8$

When given a $n$ , to find such $k$ that make the equality hold, we need to let the coefficient of a $\geq 0$. and create an interval to see if an integer exist or not within the interval.

This largest impossible number is called the **Frobenius Number**, denoted as $g(x, y)$.

Proof for Chicken McNuggets Theorem:
The largest impossible number to get from linear combination of 2 coprime number $a,b$ is $ab-a-b$.


First part: prove that $xy-x-y$ cannot be made for $a,b\geq 0$. We argue by contradiction
$xy-x-y=ax+by$  for $a,b\geq 0$
$xy=(a+1)x+(b+1)y$

Since $xy\equiv 0 \pmod{x}$ and $(a+1)x\equiv 0 \pmod{x}$ it follow that $(b+1)y\equiv 0 \pmod{ x}$


$$
b+1\equiv 0 \pmod{x} 
$$

Since $b\geq 0$ and $b+1\equiv 0 \pmod{ x}$, it follow that the smallest possible number is $x$.  

We apply the same argument to $(a+1)x$ and we get $(a+1)\geq y$

Thus, by substitution we get
$$
xy\geq 2xy
$$
which is a contradiction (why? since $x=0$ or $y=0$ make the inequality true.) It is because for $ax+by=1$ , $x \neq 0$ and $y\neq 0$. Because if $x=0$ , then $gcd(x,y)\neq 1$. In other word this theorem is only true iff $x,y> 0$.

Part 2: We prove that for $n>xy-x-y$ , we can find nonnegative integers $a,b$ such that $n = ax+by$

Assume $a\geq 0$ and $b< 0$. Since $xy=yx$ it follow that we can add b with $x$ and eventually become positive
$n =(a-y)x+(b+x)y$

If we keep on minus $y$ from a, the last number is remainder when divide $y$ which is
$\{ 0,\dots y-1 \}$
This is exactly why, for _any_ values of $x$ and $y$, we can always shift our coins around until $a$ is securely trapped in the range:

$$0 \le a \le y - 1$$
Since we forced $a$ to be non-negative, we just need to prove that its partner, $b$, **must also be non-negative** ($\ge 0$). We argue by contradiction which is assume $b\leq 1$.

We plugged both of those maximum limits into our equation to see what the highest possible value for $n$ could be:

$$
\begin{align}
n &\le x(y - 1) + y(-1) \\
n&\leq xy-x-y
\end{align}
$$
which is a contradiction. Thus, $b\geq 0$.

5.53
Let $p$ be an arbitrary prime number in the set $s$ where $s$ is the sum of every 3 prime number.
It cannot be even number and we have 3 prime number thus, 2 must not in the set $S$.

Let try 3,5,11,13
How many combination? $^{4}C_{3}=4$.

Notice that 3+5+7=21=$3(7)$
Notice that $11+13+3=27=3(9)$
Notice that each of them is divisible by 3, thus the core idea is to check the sum in modulo 3.

Notice that we have 3 prime number, and notice that the prime number that have following residue work: $\{ 1,1,2,2 \}$

Because each combination is not divisible by 3. For example $\{ 7,13,5,17 \}$

But notice that $7+13+5=25=5(5)$

if $\{ 7,19,5,17 \}$
$7+19+5=31$
$19+5+17=41$
$5+17+7=29$
$17+7+19=43$

5.54
Proof:
Let $K=\{ x \in \mathbb{N}\mid \neg P(x) \}$. Since, $K \subseteq \mathbb{N}$. Since $|K|=k$, it follow that $K$ is finite.
Furthermore, because the statement $\forall n \in \mathbb{N}, P(n)$ is known to be false, there is at least one counterexample, meaning $K$ is non-empty.
By mathematical induction it follow that there exists an element $x_{1}$ in $K$ such that $\forall x \in K,x_{1}\geq x$. 
Lets define $m=x_{1}+1$
Thus, let's define the set $S=\{ n \in \mathbb{N}\mid n\geq m \}$. Thus, it is clear that $n \not\in K$. Thus, it follow that $\forall n \in S,P(n)$ is true.


