1)
$$
\forall r,s \in \mathbb{R},(r+s<50)\to(r<25 \text{ or } s<25)
$$
Contrapositive:
$$
\forall r,s \in \mathbb{R},(r\geq 25 \text{ and }s\geq 25)\to(r+s\geq 50)
$$

Proof (Contrapositive):

Suppose r and s are two arbitrary real number such that $r\geq 25$ and $s\geq 25$. By substitution
$$
\begin{align}
s+r&\geq 25+25 \\
s+r&\geq 50
\end{align}
$$
Since s and r are arbitrary it follow that the statement is true for all real number. Q.E.D

If 50 change to 51, then the statement is false. Let take $r=25.1$ and $s=25.1$. Thus, $r\geq 25$ and $s\geq 25$ but $s+r\not\geq 51$ 


==Remark==: Notice that if $r<25$ and $s\leq 25$ , then $r+s<50$. For the sum to be **equal** to the limit, _both_ parts would have to be equal to their limits.



2)
Proof (Contradiction):
Suppose not which is suppose there exist a least positive rational number denoted by $n$ . It means that $n\geq N$ for all positive rational number $N$. By definition,
$$
n =\frac{a}{b} \text{ for some positive integer a,b}
$$
Let $m=\dfrac{n}{2}$ . Thus, by substitution
$$
m=\frac{a}{2b}
$$
Notice that $m$ is a positive rational number because $m$ is a product of 2 positive rational number which is $\dfrac{a}{b}\cdot \dfrac{1}{2}$

Thus,
$$
\begin{array}
\ \dfrac{a}{2b}< \dfrac{a}{b} \\
m<n
\end{array}
$$
Thus, $n$ is the least positive rational number and $n$ is not the least positive rational number, which is contradiction. Thus, the supposition is false and the original statement is true.

3)
$$
\forall a\in \mathbb{Z},b=a^{3}\to b=3n \text{ or }b=3n+1 \text{ for some integer n}
$$
Proof:
Suppose an arbitrary integer $a$ and $b=a^{^{3}}$. By quotient remainder theorem, there exists a unique integer k and r such that $a=3k+r$ where $0\leq r<3$ .

Case 1: $a=3k+0$
Thus, by substitution 
$$
\begin{align}
b&=(3k)^{3} \\
&=27k^{3} \\
&=3(9k^{3})
\end{align}
$$
Let $t=9k^{2}$ and t is a integer because the product of integers are integer. Thus, by substitution
$$
b=3t \text{ for some intnger t}
$$

Case 2: $a=3k+1$
Thus by substitution
$$
\begin{align}
b&=(3k+1)^{3} \\
b&=(3k)^{3}+3(3k)^{2}(1)+3(3k)(1^{2})+(3k)^{0}1^{3} \\
&=27k^{3}+27k^{2}+9k+1 \\
&=3(9k^{3}+9k^{2}+3k)+1
\end{align}
$$
Let $t_{1}=27k^{3}+27k^{2}+3k+1$ and $t_{1}$ is an integer because the sum and product of integers are integer. Thus, by substitution
$$
b=3t_{1}+1 \text{ for some integer }t_{1}
$$

Case 3: $a=3k+2$. Thus, by substitution
$$
\begin{align}
b&=(3k+2)^{3} \\
&=27k^{3}+27k^{2}(2) +9k(2)^{2}+1(2)^{3} \\
&=27k^{3}+54k^{2}+ 36k+8 \\
&=3(9k^{3}+16k^{2}+12k+2)+2
\end{align}
$$
Let $t_{2}=9k^{3}+16k^{2}+12k+2$ and $t_{2}$ is an integer because the sum and product of integers are integer. Thus,
$$
b=3t_{2}+2  \text{ for some integer }t_{2}
$$

Thus, Let's take $a=3k+2$ for some integer k and $a\in \mathbb{Z}$. Since $a^{3}=3t_{2}+2$. Thus, $a=3k+2$ is counterexample. Therefore, the statement is false.

==Remark== : 
1) The main idea of this proof is to use modulo 3 to divide integer into 3 cases. 
2) Binomial theorem. 

4)
a) 
Proof(Contraposition):
Suppose $n,r$ and $s$ are arbitrary positive real numbers such that $r>\sqrt{ n }$ and $s>\sqrt{ n }$
Since,$\sqrt{ n }>0$. Thus, by substitution,
$$
\begin{align}
rs&>\sqrt{ n }\cdot \sqrt{ n } \\
rs&>n
\end{align}
$$

Since,$n,r$ and $s$ are arbitrary positive real number. It follow that the statement is true for all positive real number. Q.E.D

b) 
Proof:
Suppose an arbitrary composite number $n$ and $n>1$ By definition, there exist integers a and b such that
$$
n =ab \text{ where } 1<a<n \text{ and } 1<b<n
$$
It follow that $a<\sqrt{ n }$  or $b<\sqrt{ n }$  WLOG, let assume $a\leq b$. Thus, $a<\sqrt{ n }$.
 **Case 1:** If $a$ is prime, 
 Let $p = a$. Then $p|n$ and $p \le \sqrt{n}$.

**Case 2:** If $a$ is composite, 
Then by the Fundamental Theorem of Arithmetic, $a$ must have a prime factor $p$. Since $p$ is a factor of $a$, then $p \le a$.
Since $a \le \sqrt{n}$, by transitivity, **$p \le \sqrt{n}$**.
Since $p|a$ and $a|n$, by transitivity of divisibility, **$p|n$**. Q.E.D


==Remark==: 
We cannot simply apply Fundamental Theorem of Arithmetic to imply that a and b are prime. It is because not all number can be express as product of **2 prime factors**. For example $60=2^{2}\times 3 \times 5$.

This property is most commonly known as the **Prime Divisors Theorem** (or sometimes the **Trial Division Theorem**).

It provides the mathematical foundation for the **Trial Division** algorithm, which is the most basic method for determining if a number is prime.

The Theorem Explained

The theorem is usually stated in two equivalent ways (contrapositives of each other):

1. **The Composite Form:** If an integer $n > 1$ is composite (not prime), then $n$ must have at least one prime factor $p$ such that $p \leq \sqrt{n}$.
2. **The Primality Test Form (Your version):** If an integer $n$ is not divisible by any prime number $p$ where $p \leq \sqrt{n}$, then $n$ must be prime.

Another approach to prove 
Proof:
Suppose an arbitrary composite number $n$ and $n>1$, By Fundamental Theorem of Arithmetic, there exists a positive integer k and prime number $p_{i}$ where $0<i\leq k$ such that
$$
n =p_{1}\cdot p_{2}\cdot\dots \cdot p_{k}
$$

Since, n is composite , thus $k\geq 2$. Assume that $p_{1}$ is the least prime factor. Let $a=p_{1}$ and $b=p_{2}\cdot p_{3}\cdot\dots \cdot p_{k}$. Thus,
$$
n =ab \text{ where } a\leq b
$$

Thus, it follow that
$$
a\leq\sqrt{ n }
$$
$$
p_{1}\leq \sqrt{ n }
$$

Let $p=p_{1}$ . Thus, $p\mid n$ and $p\leq \sqrt{ n }$ . Q.E.D

5)
The supposition is wrong. The negation of it should be there exists an integer that is irrational. Then, we can proceed the proof by show that it lead to contradiction.

6)
Proof:
Suppose x and y are arbitrary real numbers.
Case 1:  $x\geq 0$ and $y\geq0$
Thus, $xy\geq 0$ . It follow that
$$|xy|=xy$$
Since $x\geq 0$ and  $y\geq 0$ , it follow that $|x|=x$ and $|y|=y$ . Thus by substitution
$$
|x|\cdot|y|=xy
$$
Thus,
$$
|xy|=xy=|x|+|y|
$$



Case 2: One of x and y is greater or equal to 0 and the another less than 0
WLOG, assume $x\geq 0$ and $y<0$ . It follow that $|x|=x$ and $|y|=-y$ . Thus, by substitution
$$
|x|\cdot|y|=-(xy)
$$

Notice that $xy< 0$ . Thus 
$$
|xy|=-(xy)
$$
Thus,
$$
|xy|=-(xy)=|x|\cdot|y|
$$



Case 3: $x< 0$ and $y< 0$

Thus, $|x|=-x$ and $|y|=-y$. Thus, by substitution
$$
\begin{align}
|x|\cdot|y|&=(-x)(-y) \\
&=xy
\end{align}
$$

Notice that $xy>0$ . Thus, 
$$
|xy|=xy
$$
Thus,
$$
|xy|=xy=|x|\cdot|y|
$$
Since the cases above exhaust all the possible cases. Thus, it follow that the statement is true. Q.E.D

7)
Proof(Contraposition):
Suppose an arbitrary integer n such that $3\not\mid n$.By quotient remainder theorem
$$
n =3k+1 \text{ or }n =3k+2 \text{ for some integer k}
$$
 Case 1: $n =3k+1$
 $$\begin{align} n^2 &= (3k+1)^2 \\ n^2 &= 9k^2 + 6k + 1 \\ n^2 &= 3(3k^2 + 2k) + 1 \end{align}$$
 Let $t=3k^{2}+2k$ and t is an integer because the product and sum of integers are integer. Thus,
 $$
n^{2}=3t+1 \text{ for some integer t}
$$
Thus, $3\not\mid n^{2}$

**Case 2:** $n = 3k + 2$

$$\begin{align} n^2 &= (3k+2)^2 \\ n^2 &= 9k^2 + 12k + 4 \end{align}$$
$$\begin{align} n^2 &= 9k^2 + 12k + 3 + 1 \\ n^2 &= 3(3k^2 + 4k + 1) + 1 \end{align}$$
Let $t_{1}=3k^{2}+4k+1$ and $t_{1}$ is an integer because the product and sum of integers are integer. Thus,
$$
n^{2}=3t_{1}+1 \text{ for some integer }t_{1}
$$
Thus, $3\not\mid n^{2}$

Since, the cases above exhaust a;; the possible cases. Thus, it follow that the statement is true.

### ==Remark== 
Can we prove by FTA?
**Theorem:** $\forall n \in \mathbb{Z}$, if $3 \mid n^2$, then $3 \mid n$.

Proof:

Let $n$ be an arbitrary integer such that $3 \mid n^2$.

Case 1: $n = 0$

$0^2 = 0$. Since $0 = 3 \times 0$, $3 \mid 0$. The statement holds.

Case 2: $n \neq 0$

Let $x = |n|$. Since $n \neq 0$, $x$ is a positive integer ($x \ge 1$).

Note that $n^2 = x^2$.

Since we are given $3 \mid n^2$, it follows that $3 \mid x^2$.

- Subcase 2a: $x = 1$
    
    $1^2 = 1$, which is not divisible by 3. This contradicts the hypothesis. Thus $x \neq 1$.
    
- Subcase 2b: $x > 1$
    
    Since $x > 1$, we can apply the Fundamental Theorem of Arithmetic to $x$.
    
    $x$ has a unique prime factorization.
    
    Since $3 \mid x^2$, and 3 is prime, 3 must be a prime factor of $x$ (by the logic established previously: prime factors of $x^2$ are just factors of $x$ doubled).
    
    Therefore, $3 \mid x$.
    

Since $x = |n|$, this means $3 \mid |n|$.

By properties of divisibility, if 3 divides the absolute value, it divides the number itself.

Thus, $3 \mid n$.

This proof use the modulo 3 to separate the integer into 3 class.



###
8)
Proof(Contradiction) :
Suppose not which is suppose $\sqrt{ 2 }+\sqrt{ 3 }$ is rational. Thus, bt definition
$$
\sqrt{ 2}+\sqrt{ 3 }=\frac{a}{b} \text{ for some integers a and b},b\neq 0
$$
We assume that $\dfrac{a}{b}$ don't have non-trivial common factor. Thus,
$$
\begin{align}
(\sqrt{ 2 }+\sqrt{ 3 })^{2}=\frac{a^{2}}{b^{2}} \\
(\sqrt{ 2 })^{2}+2(\sqrt{ 2 })(\sqrt{ 3 })+(\sqrt{ 3 })^{2}= \frac{a^{2}}{b^{2}} \\
2+2(\sqrt{ 6 })+3=\frac{a^{2}}{b^{2}} \\
2\sqrt{ 6 }=\frac{a^{2}}{b^{2}}-5 \\
\sqrt{ 6 }=\left( \frac{1}{2} \right)(\frac{a^{2}}{b^{2}}-5)
\end{align}
$$
Let $t=\left( \dfrac{1}{2} \right)\left( \dfrac{a^{2}}{b^{2}}-5 \right)$ and t is an rational number because the product and difference of rational number is rational.
Thus,
$$
\begin{align}
\sqrt{ 6 }=t \\
\sqrt{ 6 }=\frac{a}{b} \\
6=\frac{a^{2}}{b^{2}}  \\
6b^{2}=a^{2} \\
a^{2}=2(3b^{2})
\end{align}
$$
Since, $3b^{2}$ is integer. By definition $a^{2}$ is even integer. Thus, $a$ is even integer. By definition,
$$
a=2k  \text{ for some integer k}
$$
By substitution,
$$
\begin{align}
a^{2}=2(2k^{2}) \\
2(2k^{2})=2(3b^{2}) \\
3b^{2}=2k^{2} \\
b^{2}=\frac{2}{3}k^{2}
\end{align}
$$


