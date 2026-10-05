5.16
Proof:
Suppose $a,b \in \mathbb{Z}$ such that $a\geq 2$ and $a|b$ and $a\mid (b+1)$.

$$
b=ac \text{ for some } c \in \mathbb{Z}
$$
and 
$$
b+1=ad \text{ for some }d \in \mathbb{Z}
$$

Thus, 
$$
\begin{align}
ac+1&=ad \\
ac-ad=&-1 \\
a(c-d)&=-1 \\
a&=\frac{1}{d-c}
\end{align}
$$
Since $d-c \in \mathbb{Z}$, it follow that $a\leq 1$ which contradict the supposition.

Cleaner way:
Since $a(d-c)=1$ and $d-c \in \mathbb{Z}$. Thus, $a \mid 1$ , it follow that $a=1$ or $a=-1$. Thus, it contradict the supposition.


5.18
Proof:
Suppose the product of an irrational number $s$ and a nonzero rational number $m$ is rational.
Thus,
$$
m=\frac{c}{d} \text{ for some }c,d \in \mathbb{Z}
$$


$$
\begin{align}
s\left( \frac{c}{d} \right)&=\frac{a}{b} \text{ for some }a,b \in \mathbb{Z}\\
s&=\frac{ad}{bc}
\end{align}
$$

Since $ad$ and $bc$ are integer, it follow that $s$ is a rational number which contradict our supposition.

5.19
Proof:
Suppose an $z \in \mathbb{Q}$ where $\frac{s}{m}=z$ for $s \in \mathbb{Q}^{c}$ and $m \in \mathbb{Q}$ and $m\neq 0$. Thus,

$$
z=\frac{a}{b} \text{ for some }a,b \in \mathbb{Z}
$$
and
$$
m=\frac{c}{d} \text{ for some }c,d\in \mathbb{Z}
$$
Thus,

$$
\begin{align}
\frac{s}{m}&=z \\
\frac{s}{\left( \frac{c}{d} \right)}&=\frac{a}{b} \\
s&=\frac{ac}{bd}
\end{align}
$$
Since $ac$ and $bd$ are integer ,it follow that s is a rational number which contradict our supposition.


5.20
Proof:
Suppose not which is $a \in \mathbb{Q}^{c}$ and $r \in \mathbb{Q}$ and $s \in \mathbb{R}$, $ar+s$ and $ar-s$ is rational.

Since $ar+s$ and $ar-s$ are rational .It follow that their sum is rational. Thus,

$$
\begin{align}
(ar+s)+(ar-s)&=\frac{c}{d} \text{ for some }c,d \in \mathbb{Z} \\
2ar&=\frac{c}{d} \text{ for some }c,d \in \mathbb{Z} \\
a&=\frac{c}{2dr} 
\end{align}
$$
Since $dr$ is rational and $c$ is integer, it follow that a is a rational number which contradict our supposition.

==Remark==
Rational is close, it is a group with arithmetic operation

Thus, rational+ rational=rational , contradiction either one is irrational (question given), thus the sum is irrational to make the contradiction (question) true.

5.21
Proof:
Suppose not $\sqrt{ 3 }$ is rational. Thus,
$$
\begin{align}
\sqrt{ 3 }&=\frac{a}{b} \text{ for some }a,b \in \mathbb{Z} \text{ where }gcd(a,b)=1 \\
3&= \frac{a^{2}}{b^{2}} \\
3b^{2}&=a^{2}
\end{align}
$$

Since $b^{2}\in \mathbb{Z}$ it follow that $3\mid a^{2}$ , thus $3\mid a$. Thus, $a=3c$ for some $c \in \mathbb{Z}$
$$
\begin{align}
3b^{2}&=(3c)^{2} \\
b^{2}&=3c^{2}
\end{align}
$$
$3\mid b^{2}$ thus $3\mid b$. It follow that $gcd(a,b)\neq 1$. Which contradict our supposition.

==square free integer==
$a\mid b^{m}$ iff $a\mid b$ is true iff $a$ is square free integer(more narrow: prime number). square free is the strictest condition.

$2^{2}\cdot3^{2}=36$
$2^{2}\cdot 3=12$
2cdot 3=6
Thus, $12\mid 36$ but $12\not\mid 6$

5.22
Proof:
Suppose not. Thus
$$
\begin{align}
\sqrt{ 2 }+\sqrt{ 3 }&=r \text{ where }r \in \mathbb{Q} \\
\sqrt{ 3 }&=r-\sqrt{ 2 } \\
3&=r^{2}-2\sqrt{ 2 }+2 \\
1&=r^{2}-2\sqrt{ 2 } \\
r^{2}-1&=2\sqrt{ 2 } \\
\sqrt{ 2 }&=\frac{r^{2}-1}{2}
\end{align}
$$
Since $r^{2}-1\in \mathbb{Q}$, it follow that $\sqrt{ 2 }\in \mathbb{Q}$ which contradict the fact.

1) irrational $\times$ rational = irrational? (wrong)
$\sqrt{ 2 }\times 0=0$
it is only true if we exclude the zero.

2) irrational + rational = irrational 

5.24
Proof:
Suppose not. There exist an element $x \in S\cap T$ such that $x \in \mathbb{Q}^{c}$. Since $p \in \mathbb{Q}$ and $r \in \mathbb{Q}$, it follow that $q\sqrt{ 2 }\in \mathbb{Q}^{c}$ and $s\sqrt{ 3 }\in \mathbb{Q}^{c}$. Thus, $x=p+q\sqrt{ 2 }$ and $x=r+s\sqrt{ 3 }$
$$
\begin{align}
p+q\sqrt{ 2 }&=r+s\sqrt{ 3 } \\ 
p-r&=s\sqrt{ 3 }-q\sqrt{ 2 } \\
(p-r)^{2}&=3s^{2}-qs\sqrt{ 6 }+2q^{2} \\
(p-r)^{2}-3s^{2}-2q^{2}&=-qs\sqrt{ 6 } \\
\sqrt{ 6 }&=\frac{(p-r)^{2}-3s^{2}-2q^{2}}{-qs} \text{ where }q,s\neq 0
\end{align}
$$

(if $q=0$, $q\sqrt{ 2 } \in \mathbb{Q}$ contradiction)
(if $s=0$, $s\sqrt{ 3 }\in \mathbb{Q}$ contradiction)


$\frac{(p-r)^{2}-3s^{2}-2q^{2}}{-qs}$ is a rational number which contradict the fact that $\sqrt{ 6 }$ is irrational.

5.25
Proof:
Suppose there exist an integer $a$ such that $a\equiv 5 \pmod{14}$ and $a\equiv 3 \pmod{21}$. Thus,
$a=14b+5$ and $a=21c+3$ for some $b,c \in \mathbb{Z}$.Therefore,

$$
\begin{align}
14b+5&=21c+3 \\
14b-21c&=-2 \\
7(2b-3c)&=-2 \\
2b-3c&=\frac{-2}{7}
\end{align}
$$
Notice that $2b-3c$ is an integer which is a contradiction.

5.26
Proof:
Suppose there exists positive integer $x$ such that $2x<x^{2}<3x$.

$$
\begin{align}
2<x<3
\end{align}
$$
which is a contradiction.

5.27
Proof:
Suppose not. WLOG, suppose 
$$
a<b<c
$$

$$
c\mid |b-a|
$$
 Since, $c$ and $|b-a|$ is positive it follow that $c\leq|b-a|$.
 $$
c\leq b-a
$$
Notice that,
$$
b>b-a
$$
Thus,
$$
c<b
$$
Which is a contradiction.

5.28
Proof Analysis:
We know that the product of 2 odd integer is odd. Thus , the sum of 2 square of odd integers is even. is there any even square? yes (4,16,36,...) Thus, we cannot narrow the possibility in modulo 2.

(The core idea)
Notice that, $2\mid x^{2}$, iff $2\mid x$. Thus. $x=2k$ for some integer $k$. Thus, $x^{2}=4k^{2}$., we can conclude that $4\mid x^{2}$. Let's try work under modulo 4

$a=2s+1$ , thus, $a^{2}=4(s^{2}+s)+1$ same as $b$. Thus, $a^{2}\equiv 1 \pmod{ 4}$ and $b^{2}\equiv 1 \pmod{ 4}$. Thus, $a^{2}+b^{2}\equiv 2 \pmod{ 4}$. (Contradiction)

(Thus, Pythagorean triples one of height or width must be even. )

5.29
Proof:
Suppose not. There exist positive real number $x$ and $y$ such that
$$
\begin{align}
\sqrt{ x+y }&=\sqrt{ x }+\sqrt{ y } \\
x+y&=x+2\sqrt{ xy }+y \\
2\sqrt{ xy }&=0 \\
xy&=0
\end{align}
$$
Thus, $x=0$ or $y=0$. (Contradiction)

5.30
Proof:
Suppose not. There exists positive integers $m$ and $n$ such that $m^{2}-n^{2}=1.$

$$
\begin{align}
(m-n)(m+n)&=1 \\
\end{align}
$$
Thus, $(m-n)=1$ and $(m+n)=1$ or $(m-n)=-1$ and $(m+n)=-1$.

Case 1: $(m-n)=1$ and $(m+n)=1$
$$
\begin{align}
2m=2 \\
m=1
\end{align}
$$
Thus, $n =0$ (contradiction)

Caser 2: $(m-n)=-1$ and $(m+n)=-1$
$$
\begin{align}
2m&=-2 \\
m&=-1
\end{align}
$$
(Contradiction)

**The Intuition:** 
$$
m^{2}=n^{2}+1
$$
Since the smallest gap between positive squares is 3 (between 1 and 4), it is obviously impossible to find two squares with a gap of 1.


5.31:
Proof:
Suppose not which is assume $m=2s$ where $s \in 2\mathbb{Z}+1$ and there exists integer $x$ and $y$ such that $x^{2}-y^{2}=m$
$m=2(2r+1)$ for some $r \in \mathbb{Z}$
$m=4r+2$

Thus, $m\equiv 2\pmod{4}$.
Lemma 1:
For $a \in \mathbb{Z}$, if $a\equiv 0 \pmod{2}$ , then $a^{2}\equiv 0 \pmod{ 4}$ 
Lemma 2:
For $a \in \mathbb{Z}$, if $a\equiv 1 \pmod{2}$, then $a^{2}\equiv 1 \pmod{ 4}$.

Case 1: $x\equiv 0 \pmod{2}$ and $y\equiv 0 \pmod{ 2}$
Thus, $x^{2}\equiv 0 \pmod{ 4}$ $y^{2}\equiv 0 \pmod{4}$. Thus, $x^{2}-y^{2}\equiv 0 \pmod{ 4}$. Contradiction

Case 2:  $x\equiv 1 \pmod{2}$ and $y\equiv 0 \pmod{2}$
Thus, $x^{2}\equiv 1 \pmod{4}$ and $y^{2} \equiv 0 \pmod{ 4}$. Thus, $x^{2}-y^{2}\equiv 1 \pmod{ 4}$. Contradiction.

Case 3: $x\equiv 0 \pmod{ 2}$ and $y \equiv 1 \pmod{2}$
Thus, $x^{2}-y^{2}\equiv 3 \pmod{ 4}$. Contradiction


Case 4: $x\equiv 1 \pmod{ 2}$ and $y\equiv 1 \pmod{2}$
Thus, $x^{2}-y^{2}\equiv 0 \pmod{4}$. Contradiction.

Since every cases above leads to contradiction it follow that there do not exists integers $x$ and $y$ such that $x^{2}-y^{2}=m$

==Another way to prove==
#### **Alternative Proof: The Parity of Factors**

**Proposition:** Let $m$ be an integer such that $m \equiv 2 \pmod 4$. There are no integers $x, y$ such that $x^2 - y^2 = m$.

**Proof:**

Assume for the sake of contradiction that $x^2 - y^2 = m$.

We can factor the left side:

$$(x - y)(x + y) = m$$

Let $A = x - y$ and $B = x + y$.

Thus, $AB = m$.

Consider the sum of these two factors:

$$A + B = (x - y) + (x + y) = 2x$$

Since $2x$ is always an even integer, the sum $A + B$ is **even**.

For the sum of two integers to be even, they must have the **same parity**.

- Case 1: Both $A$ and $B$ are **odd**.
    
- Case 2: Both $A$ and $B$ are **even**.
    

Now let's look at the product $AB = m$:

**Case 1: $A$ and $B$ are both odd.**

The product of two odd numbers is odd.

Therefore, $AB$ is odd.

But we are given that $m \equiv 2 \pmod 4$, which implies $m$ is **even**.

Contradiction ($m$ cannot be both odd and even).

**Case 2: $A$ and $B$ are both even.**

Let $A = 2k$ and $B = 2j$ for some integers $k, j$.

Then their product is:

$$AB = (2k)(2j) = 4kj$$

This implies that $AB$ is divisible by 4 (i.e., $AB \equiv 0 \pmod 4$).

However, we are given that $m \equiv 2 \pmod 4$.

Contradiction ($m$ cannot be congruent to both 0 and 2 modulo 4).

**Conclusion:**

Since both cases lead to a contradiction, no such integers $x$ and $y$ exist.

5.32
Proof:
Suppose there exists three distinct real numbers $a,b,c$ such that all of the numbers $a+b+c$, $ab$, $ac$, $bc$, $abc$ are equal. Thus, 

WLOG, $a<b<c$. (There is nothing to do with this).

We know that the only possibility is $a,b,c=0$. Thus, we show all of them must equal to 0 by using $ab=ac=bc$.

$$
\begin{align}
a(b-c)=0
\end{align}
$$
$b-c \neq 0$, thus, $a=0$. $ac=bc\to bc=0$. Thus, $b=0$ or $c=0$. Contradiction

5.33
Proof:
[[Euclid lemma.png]]
We argue by contradiction. Suppose $x,y \in \mathbb{Z}$,  $5\not\mid xy$ and $5\mid x$ or $5\mid y$. 

Case 1: $5\mid x$
Thus, $x=5k$ for some $k \in \mathbb{Z}$.Therefore,
$$
\begin{align}
xy=5(ky)
\end{align}
$$
Since $xy \in \mathbb{Z}$, it follow that $5\mid xy$.

Case 2: $5\mid y$
Thus, $y=5s$ for some $s \in \mathbb{Z}$. Therefore,
$$
\begin{align}
xy=5(xs)
\end{align}
$$
Since $xs \in \mathbb{Z}$, it follow that $5\mid xy$.

In every cases, $5\mid xy$ which lead to contradiction.

==Remark==
Notice that this is converse of Euclid lemma, which is trivial:
Suppose $a,b,c \in \mathbb{Z}$, if $a\mid b$ or $a\mid c$, then $a\mid bc$.

Euclid lemma:
Suppose $a$ is a prime number and $x,y \in \mathbb{Z}$, if $a\mid xy$, then $a\mid x$ or $a\mid y$.

We need to use Bézout's Identity to prove Euclid lemma, and we use Euclid lemma to prove the unique part if FTA.

5.34
To prove this we need to know about Bounding between consecutive squares.
There is not perfect square between $k^{2}$
and $(k+1)^{2}$.

Proof:
For the sake of contradiction, suppose $m,n \in \mathbb{Z}^{+}$ such that $m^{2}+m+1=n^{2}$

Since $m>0$, thus $m+1>0$, and $m^{2}>0$. Therefore, $m^{2}+m+1>m^{2}$ implies that $n^{2}>m^{2}$.

Notice that $(m+1)^{2}=m^{2}+2m+1>m^{2}+m+1$. Thus, $n^{2}<(m+1)^{2}$

Thus, 
$$
m^{2}<n^{2}<(m+1)^{2}
$$
Contradiction.


**Practice:** Try proving that $n^4 + 2n^3 + 2n^2 + 2n + 1$ is never a perfect square for large enough $n$. (Hint: Compare it to $(n^2+n)^2$ and $(n^2+n+1)^2$).

We need to guess the root. What if it is a perfect square?

$$
\begin{align}
(n^{2}+n)^{2}=n^{4}+2n^{3}+n^{2}
\end{align}
$$

Is it greater or smaller?

$$
\begin{align}
n^{4}+2n^{3}+2n^{2}+2n+1-(n^{2}+n)^{2}&=n^{2}+2n+1 \\
&=(n+1)^{2}
\end{align}
$$
Since $(n+1)^{2}>0$, it follow that $n^{4}+2n^{3}+2n^{2}+2n+1>(n^{2}+n)^{2}$

Let's look at the next perfect square
$$
(n^{2}+n+1)^{2}=n^{4}+2n^{3}+3n^{2}+2n+2
$$

The difference between them is $-n^{2}$.Thus,

$$(n^2+n)^2 < P(n) < (n^2+n+1)^2$$
Which is never a perfect square.

==5.35==
a)
Proof:
$b^{2}-4ac=(-3)^{2}-4=5$ , since $5$ is not a perfect square, it follow that the solution is irrational.

Proof:
