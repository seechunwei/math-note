%%
1)
division into case: n is odd or n is even
Case 1: n is even 
Example: Let  n=0 0=2(0)
But notice that if n is prime then n>1

Thus, we can just use counter example, cannot because we need to prove for all integer n, ...... cannot be prime, so it is not a counter example , it is a witness. It is not enough to prove a universal statement.

Prime
$\forall r,s \in \mathbb{Z},n =rs\to( r=n\lor s=n)$
Composite
$\exists r,s \in \mathbb{Z}, n =rs \land(1<r,s<n)$
where n>1

$\forall n, n \in \mathbb{Z}\to(n\lor n+2\lor n+4\lor n+6 \text{ is not prime})$
it means they have factor other than themselves ,prime cannot be divide by the prime number that less than themselves
%%

1)
Proof:
Suppose n is an arbitrary integer. We need to show that $\forall n, n \in \mathbb{Z}\to(n\lor n+2\lor n+4\lor n+6 \text{ is not prime})$. 

Case 1: Suppose $n\leq 1$
$n$ is not prime because by definition, if $n$ is prime,  then $n >1$. Since $n \not>1$, by Modus Tollens it follow that n is not prime.


Case 2: Suppose $n >1$

Case 2.1: Suppose n is even 
Then, $n+2,n+4,n+6$ are even because the sum of two even integer is even. Thus, by definition, all of them equal to the product of $2$ and some integer. Since 2 is the only even prime, and the integers $n, n+2, n+4, n+6$ are distinct, it follow that at most one of these integers can be equal to 2. Thus, it follow that at least one of $n,n+2,n+4,n+6$ is not prime.


Case 2.2: Suppose n is odd
Then, $n+2,n+4,n+6$ is odd because the sum of odd and even integer is odd. We need to show that at least one of them is not prime. 

Notice that the sum of two arbitrary integer denoted by $(k+s)$ is a multiple of an integer m iff $m \mid (k+s)$ which mean $k+s=mk$ for some integer k. 
Since the remainder is 0, thus $(r+s)\equiv 0(\text{ mod m})$. 

Let $m=3$. Thus, the residues of $n,n+2,n+4,n+6$ modulo 3 denoted by
$$
\begin{align}
n &\equiv r \text{ (mod 3)} \text{ where } r\in \{ 0,1,2 \}\\
n+2&\equiv r+2  \text{ (mod 3)}\\
n+4&\equiv r+1  \text{ (mod 3)}\\
n+6&\equiv r \text{ (mod 3)}
\end{align}
$$


Notice that the three residues $r,r+2,r+1$(mod 3) is just a permutation of $\{ 0,1,2 \}$ , Since $r,r+1,r+2$ are distinct so one of them must be equal to 0. Therefore, for every integer n at least one of $n,n+2,n+4,n+6$ is divisible by 3. 

Notice that, if one of them is 3, then being divisible by 3 does **not** imply composite. Let X denote the set of possible value $n,n+2,n+4,n+6$

$$
X=\{ n,n+2,n+4,n+6 \}
$$
Since $n > 1$, the only case where a multiple of 3 is prime is when the number _is_ 3. This can only happen when $n=3$ . It is because $n\leq1$ when $n+2=3$ or $n+4=3$ or $n+6=3$.

Suppose n=3. 
Thus, by substitution $X=\{ 3,5,7,9 \}$ where $9\neq 3$ and $3\mid 9$. 
Thus, it follow that at least one of $n,n+2,n+4,n+6$ is not prime.


%%
Case 2.2.2
if n+2=3. $X=\{ 1,3,5,7 \}$ where 1 is not prime

Case 2.2.3
if $n+4=3$ . $X=\{ -1,1,3,5 \}$ where -1 and 1 is not prime

Case 2.2.4
if $n+6$=3. $X=\{ -4,-1,1,3 \}$ where -4,-1 and 1 are not prime
%%
Since the cases above cover all the possibility of n. We can conclude that the four integers n, n +2, n+4, n+6 cannot all be prime, where n is any integer. Q.E.D


---

2)
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

Thus, by substitution
$$
\begin{array}
\ \lfloor x \rfloor - \lceil x \rceil =-1  \\
\end{array}
$$

Case 1 if x is an integer, then
$$
\begin{array}
\ \lfloor x \rfloor =\lceil x \rceil 
\end{array}
$$

Thus,
$$
\begin{array}
\ \lfloor x \rfloor-\lceil x \rceil  = 0 \\
0\neq -1
\end{array}
$$
Therefore, the identity does not hold for any integer x


Case 2 if x is a non-integer, then 
$$
\lfloor x \rfloor =n  \Leftrightarrow n\leq x<n+1
$$
for some integer n.

Since $x$ is a non-integer, thus, $x \neq n$. Therefore,

$$n < x < n+1$$

By the definition of the ceiling function, $\lceil x \rceil$ is the smallest integer greater than or equal to $x$. It follow that  $\lceil x \rceil= n+1$.

Thus, 

$$
\begin{align}
\lfloor x \rfloor -\lceil x \rceil  &=n-(n-1) \\
&=-1
\end{align}
$$


Therefore, the statement only true if x is a non-integer. Thus, x is a non integer.

---


3)
Sophie Germain Identity:
$$
x^{4}+4y^{4}=(x^{2}+2xy+2y^{2})(x^{2}-2xy+2y^{2})
$$
Let $x=n$ and $y=1$
$$
n^{4}+4\times(1)^{4}=(n^{2}+2n+2)(n^{2}-2n+2)
$$
By definition, $n^{4}+4\times(1)^{4}$ is prime $\leftrightarrow$ either $(n^{2}+2n+2)=1$ or $(n^{2}-2n+2)=1$  .

Case 1 $(n^{2}+2n+2)=1$

$$
\begin{align}
(n^{2}+2n+2)&=1 \\
n^{2}+2n+1&=0 \\
(n+1)^{2}&=0 \\
n+1&=0  \text{ By Zero Product Property}  \\
n&=-1
\end{align}
$$
$(n^{2}-2n+2)=n^{4}+4$

Case 2 $(n^{2}-2n+2)=1$
$$
\begin{align}
(n^{2}-2n+2)&=1 \\
n^{2}-2n+1&=0 \\
(n-1)^{2}&=0 \\
n-1&=0 \text{ By Zero Product Property} \\
n&=1
\end{align}
$$
When $n =-1$, $(-1)^{4}+4=5$ where 5 is a prime.
When $n =1$, $(1)^{4}+4=5$ where 5 is a prime.
Therefore, $n =1$ or $n =-1$ are the only integers for $n^{2}+4$ is a positive prime.

---


4)
%%
Why $\alpha \neq a$ ?  We can prove the statement $a<r+\alpha<b$  by proving there exists a irrational number between two real number since $r+\alpha$ is irrational because it is a sum of irrational and rational.

My thought is insightful but not every irrational number looks like $r + \alpha$ for a fixed $\alpha$.  For example let $\alpha=\sqrt{ 2 }$ 
$r+\alpha=\sqrt{ 3 }$, $r+\sqrt{ 2 }=\sqrt{ 3 }$ , but $\sqrt{ 3 }-\sqrt{ 2 }$ is not a rational number.
%%

Proof:
Suppose $a$ and $b$ are arbitrary real number and $\alpha$ is an arbitrary irrational number such that $\alpha \neq a$ and $\alpha \neq b$. It is suffices to prove that $\exists r\in \mathbb{Q}$ such that $a<r+\alpha<b$.

Notice that
$$
a-\alpha<r<b-\alpha
$$
Let $x=a-\alpha$ and $y=b-\alpha$. Thus, it is suffices to prove that there exists a rational number $r$ strictly between two real numbers $x$ and $y$ (where $x < y$).
$$
a-\alpha<b-\alpha\implies x<y
$$

It means $y-x=(b-\alpha)-(a-\alpha)=b-a>0$

Case 1: $x$ and $y$ are rational number
Since $x<y$ , it follow that
$$
\begin{array}
\ x+y<y+y \\ 
x+y<2y \\
\dfrac{x+y}{2}<y \\
\end{array}
$$
it also follow that
$$
\begin{array}
\ x+x<x+y \\
2x<x+y \\
x< \dfrac{x+y}{2}
\end{array}
$$
Therefore,
$$
x< \frac{x+y}{2} <y
$$


Let $r=\dfrac{x+y}{2}$  and $r$ is a rational number because $x+y$ is rational since it is sum of rational numbers and dividing a rational by a non-zero integer yields a rational. Thus, there exists a rational number such that $x<r<y$.


Case 2. One of them is rational number and the other is irrational number

WLOG, assume that $x$ is rational and $y$ is irrational. By Archimedean Principle, for any real number $Z > 0$, there exists a natural number $n \in \mathbb{N}$ such that $n > Z$ . In other word, there exists a natural number $n \in \mathbb{N}$ such that $\frac{1}{n} < Z$. 

Since $y-x$ is real number and $y-x>0$, it follow that there exists a natural number $n$ such that 
$$
\begin{array} 
\ \dfrac{1}{n}<y-x   \\
\ x<x+\dfrac{1}{n}<y
\end{array}
$$


Let $r=x+\dfrac{1}{n}$ . Thus,
$$
x<r<y
$$

$r$ is a rational number because it is a sum of rational numbers. Thus, it follow that there exists a rational number $r$ such that $x<r<y$.



Case 3: $x$ and $y$ are irrational number

We need to find a rational number which is smaller than $y-x$ and greater than 0 so that the multiple of that rational number will lies between $(x,y)$.


By Archimedean Principle, for any real number $Z > 0$, there exists a natural number $n \in \mathbb{N}$ such that $n > Z$ . In other word, there exists a natural number $n \in \mathbb{N}$ such that $\frac{1}{n} < Z$. 

Since $y-x$ is real number and $y-x>0$, it follow that there exists a natural number $n$ such that 

$$
\begin{array}
\ \dfrac{1}{n}<y-x    \text{ (By substitution) }   \\
n > \dfrac{1}{y-x}
\end{array}
$$
%%Since we want to solve for $n$ to use the Archimedean Principle (which talks about finding large integers), we take the reciprocal of both sides. Remember that taking the reciprocal reverses the inequality sign:%%

Multiplying by $(y - x)$, we get:

$$n(y - x) > 1 \quad \text{or} \quad ny - nx > 1$$
We need to find an integer $m$ such that $nx<m<ny$. Let $m = \lfloor nx \rfloor + 1$. Thus, it is suffices to prove that $m>nx$ and $m<ny$.

By definition of the floor function
$$\lfloor nx \rfloor \le nx < \lfloor nx \rfloor + 1$$
Since $m = \lfloor nx \rfloor + 1$, it follow that $m>nx$.

Notice that 
$$\begin{array}
\ ny - nx > 1 \\
ny>nx+1
\end{array}
$$
From the floor definition,
$$
\begin{array}
\ \lfloor nx \rfloor \le nx < \lfloor nx \rfloor + 1 \\ \lfloor nx \rfloor +1\leq nx+1<\lfloor nx \rfloor +2
\end{array}
$$
Since, $ny>nx+1$, it follow that $ny>\lfloor nx \rfloor+1$. Thus, by substitution, $ny>m$ or $m<ny$.

$$
nx<m<ny
$$

Dividing the entire inequality by $n$ (where $n > 0$):

$$x < \frac{m}{n} < y$$

Let $r = \dfrac{m}{n}$. Since $m$ is an integer ($m \in \mathbb{Z}$) and $n$ is a natural number ($n \in \mathbb{N}$), $r$ is a rational number ($r \in \mathbb{Q}$).

Thus, by substitution
$$
\begin{array}
\ a-\alpha<r<b=\alpha \\
a<r+\alpha<b
\end{array}
$$
Thus, there exists an $r \in \mathbb{Q}$ such that $a < r + \alpha < b$.


Since the cases above cover all the possibility, it follow that $\exists r\in \mathbb{Q}$ such that $a<r+\alpha<b$ for all real number $a$ and $b$
**Q.E.D.**


---


5)
The set of integers $\{1, 2, \ldots, 3n\}$; $n \in \mathbb{Z}^+$ is partitioned into three residue classes modulo $3$.

a) The first class consists of integers congruent to $1 \pmod{3}$ which are of the form $\{1, 4, 7, \ldots, 3n-2\} = \{3i-2 : 1 \le i \le n\}$ which can be defined as follows:

$$\prod_{i=1}^{n} (3i-2)$$

b) The second class consists of integers congruent to $2 \pmod{3}$, which are of the form $\{2, 5, 8, \ldots, 3n-1\} = \{3i-1 : 1 \le i \le n\}$ which can be defined as follows:

$$\prod_{i=1}^{n} (3i-1)$$

c) The third class consists of integers congruent to $0 \pmod{3}$, which are of the form $\{3, 6, 9, \ldots, 3n\} = \{3i : 1 \le i \le n\}$ which can be defined as follows:

$$\prod_{i=1}^{n} (3i)$$

Then, the product of all integers in the set $\{1, 2, 3, 4, \ldots, 3n\}$ is $(3n)!$ which is given by

$$(3n)! = \left(\prod_{i=1}^{n} (3i-2)\right) \left(\prod_{i=1}^{n} (3i-1)\right) \left(\prod_{i=1}^{n} (3i)\right)$$

Notice that:
$$
\begin{align}
\prod_{i=1}^{n} (3i)&=3(1)\cdot 3(2)\cdot 3(3) \cdot \dots \cdot3(n) \\
&=(3^{n})(n!)
\end{align}
$$
Thus, by substitution


$$ \quad (3n)! = \left(\prod_{i=1}^{n} (3i-2)(3i-1)\right) \left((3^n)(n!)\right)$$
$$\left(\prod_{i=1}^{n} (3i-2)\right) \left(\prod_{i=1}^{n} (3i-1)\right) = \frac{(3n)!}{(3^n)(n!)}$$





Thus, 
$$
\begin{align}
\prod_{i=1}^{n} \left( \frac{(3i-2)(3i-1)}{3i} \right)&= \left(\prod_{i=1}^{n} (3i-2)(3i-1)\right) \times \frac{1}{\prod_{i=1}^{n}(3i) }\\
&=\frac{(3n)!}{(3^n)(n!)} \times \frac{1}{(3^{n})(n!)} \\
&=\frac{(3n)!}{(3^{2n})(n!)^{2}}
\end{align}
$$

The proof is completed by showing that
$$
\prod_{i=1}^{n} \left( \frac{(3i-2)(3i-1)}{3i} \right)=\frac{(3n)!}{(3^{2n})(n!)^{2}}
$$

Q.E.D



---



6)
a) The claim is 'If $x$ is an **irrational** number and $y$ is a **rational** number, then $z=x-y$ is **irrational**.'

Then, the proof assumes $x=\sqrt{2}$ specifically. This is not valid because we cannot take a witness such as $x=\sqrt{2}$ to prove a universal statement. For other irrational numbers $x$, the argument does not hold.


**b)** Suppose $x$ is an arbitrary irrational number and $y$ is an arbitrary rational number, we need to show $z=x-y$ is irrational.

We argue by contradiction. 
Assume $z=x-y$ is rational number.
By the definition of rational number, $z=\dfrac{a}{b}$ and $y=\dfrac{c}{d}$ for some integers $a, b, c$ and $d$ with $c \ne 0$ and $d \ne 0$.

Then $z=x-y$ (by substitution)

$$x = z+y$$

$$x = \frac{a}{b} + \frac{c}{d}$$

$$x = \frac{ad + cb}{bd}$$

for some integers $ad, cb$ and $bd$ with $bd \ne 0$.

Since $b \ne 0$ and $d \ne 0$, so $bd$ is nonzero.

Clearly, $ad+cb$ and $bd$ are integers because the products and sum of integers is an integer.


Hence, $x$ is ratio of integers with a non-zero denominator and $x$ is rational number by definition of rational.
This contradicts the supposition that $x$ is irrational. Thus, $z=x-y$ must be irrational. Q.E.D


