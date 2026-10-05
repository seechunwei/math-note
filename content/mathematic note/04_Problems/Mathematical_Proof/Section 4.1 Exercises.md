4.1
Proof:

Suppose $a$ and $b$ are arbitrary integer such that $a\mid b$. Thus, $b=ac$ for some integer $c$.

$$
\begin{align}
b^{2}&=(ac)^{2}=a^{2}(c^{2})
\end{align}
$$
Since $c^{2}$ is an integer, it follow that $a^{2}\mid b^{2}$.

4.2
Proof:
Suppose $a$ and $b$ are arbitrary integer such that $a\mid b$ and $b\mid a$. Thus, $a=bc$ and $b=ad$ for some integer $c$ and $d$.

Thus,
$$
\begin{align}
a&=adc \\
1&=dc
\end{align}
$$
(Since $a\neq 0$ we can divide a)
. Since the only divisor of 1 is -1 and 1. 

Case 1: $d$ and $c$ are both equal to 1
Thus, $a=b$

Case 2: $d$ and $c$ are both equal to -1
Thus, $a=-b$

4.4
Proof:

Suppose $x$ and $y$ are arbitrary integer such that $3 \not\mid x$ and $3 \not\mid y$. Thus, $3\mid(x^{2}-1)$ and $3\mid(y^{2}-1)$. Thus, by result 4.3

$$
\begin{align}
3\mid[(1)(x^{2}-1)+(-1)(y^{2}-1)] \\
3\mid (x^{2}-y^{2})
\end{align}
$$
Q.E.D

4.5
Proof:
Suppose $a,b,c$ are arbitrary integer which $a \neq 0$. Suppose $a\mid b$ or $a\mid c$

Case 1: $a\mid b$
$b=ax$ for some $x \in \mathbb{Z}$. Thus,
$$
bc=ax(c)=a(xc)
$$

Since $xc$ is an integer, it follow that $a\mid bc$

Case 2: $a\mid c$
$c=ay$ for some $y \in \mathbb{Z}$. Thus,
$$
bc=b(ay)=a(by)
$$
Since $by$ is an integer, it follow that $a\mid bc$.

4.6 ==Euclid lemma==

4.7 
Proof:
Suppose $n$ is an arbitrary integer such that $3\not\mid n$. 
Since $n$ is not a multiple of 3, we know $n \equiv \pm 1 \pmod 3$, which implies $n^2 \equiv 1 \pmod 3$. Therefore  $3\mid(n^{2}-1)$ and $3\mid(n^{2}+2)$.
Thus, it follow that
$$
3\mid[(1)(n^{2}-1)+(1)(n^{2}+2)]
$$
$$
3\mid(2n^{2}+1)
$$

Conversely, suppose $3\mid n$. Since $n\mid n^{2}$, by transitivity it follow that $3\mid n^{2}$. Thus by definition, $n^{2}=3k$ for some $k \in \mathbb{Z}$. 

$$
\begin{align}
2n^{2}+1&=2(3k)+1 \\ 
&=3(2k)+1
\end{align}
$$
Since $3(6k^2)$ is divisible by 3, the expression leaves a remainder of 1. Thus, $3 \nmid (2n^2 + 1)$
Q.E.D

4.9
Can we conclude if $2\mid x$, then $8\mid x$?
No

4.11
if $n$ is an odd integer such that $3\not\mid n$, then $24\mid(n^{2}+3)$

Proof:
Since 3 and 8 are coprime factor of 24. We need to show $3\mid (n^{2}-1)$ and $8\mid(n^{2}-1)$.

Since $3\not\mid n$.  We know that $n \equiv\pm 1 \pmod 3$ , thus $n^{2} \equiv 1 \pmod 3$
We can conclude that $3\mid(n^{2}-1)$.

Since $n$ is odd, $n =2k+1$ for some integer $k$. 
$$
\begin{align}
n^{2}-1&=(2k+1)^{2}-1 \\
&=4k^{2}+4k+1-1 \\
&=4k^{2}+4k \\
&=4k(k+1)
\end{align}
$$
Since $k(k+1)$ is consecutive integer, it means that one of them is even. Thus, $k(k+1)=2s$ for some integer $s$.

Thus,
$$
\begin{align}
4k(k+1)&=4(2s) \\
&=8s
\end{align}
$$
Since $s$ is am integer it follow that $8 \mid(n^{2}-1)$

Since $3\mid (n^{2}-1)$ and $8\mid(n^{2}-1)$. it follow that $24\mid(n^{2}-1)$

4.12
Proof:
Since $x$ and $y$ are both old. By result 4.6(b)
it follow that $8\mid(x^{2}-1)$ and $8\mid(y^{2}-1)$. Thus, it follow that 
$$
\begin{align}
8\mid[(1)(x^{2}-1)+(-1)(y^{2}-1)] \\
8\mid (x^{2}-y^{2})
\end{align}
$$

4.13
Proof:
Prove by contradiction. Suppose $a,b,c$ are arbitrary integer such that if $a^{2}+b^{2}=c^{2}$ then $3\not\mid a$ and $3\not\mid b$. 
Thus,
$$
\begin{array}
\ a^{2}\equiv 1 \pmod  3 \\
b^{2} \equiv 1 \pmod  3
\end{array}
$$
Thus
$$
a^{2}+b^{2}\equiv 2 \pmod 3
$$

$c\equiv r \pmod 3$ where $r\in\{ 0,1,2 \}$
$c^{2}\equiv r^{2} \pmod 3$ where $r^{2}\in \{ 0,1 \}$
Thus, it follow that 
$$
a^{2}+b^{2}\neq c^{2}
$$
which contradict our supposition.

Extra question
For any Pythagorean triple $a^2 + b^2 = c^2$, do you think it is always true that **one** of the numbers ($a, b,$ or $c$) must be divisible by 5?

 0 
$n^{2} \equiv 0 \pmod 5$
Pair 1 and 4
$n^{2}\equiv 1 \pmod 5$
Pair 2 and 3
$n^{2}\equiv 4 \pmod 5$

For any integer $n$, the square $n^2$ is congruent to one of the elements in the set $\{0, 1, 4\}$ modulo $5$

Since $a^{2}+b^{2}=c^{2}$. We assume that 
$a,b,c$ all are not divisible by 5. Thus, a$a^{2},b^{2},c^{2}$ are congruence to one of the element in the set $\{ 0,1,4 \}$ modulo 5.

Case 1: WLOG $a^{2}\equiv 1$ and $b^{2}\equiv 4$
$$
1+4 \equiv 0 \pmod  5
$$
In this case, $a^{2}+b^{2}=c^{2}$ hold and $5\mid c^{2}$. It also follow that $5 \mid c$ which contradict our supposition.

Case 2: $a^{2}\equiv 1$ and $c^{2} \equiv 1$
$$
1+1\equiv 2 \pmod  5
$$
However, $c^2$ must be in $\{1, 4\}$. Since $2 \notin \{1, 4\}$, this is a contradiction.

Case 3: $a^2 \equiv 4$ and $b^2 \equiv 4$

$$4 + 4 = 8 \equiv 3 \pmod 5$$
However, $c^2$ must be in $\{1, 4\}$. Since $3 \notin \{1, 4\}$, this is a contradiction.

Since all possible cases for non-divisible integers lead to a contradiction, the assumption must be false. Therefore, at least one of $a, b,$ or $c$ must be divisible by $5$.

