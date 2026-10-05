
==Definition Even==
An integer n is even if, and only if, n equals twice some integer. An integer n is odd if, and only if, n equals twice some integer plus 1.
Symbolically, for any integer, n
$$\begin{align}
\text{n is even} &\Leftrightarrow \text{n=2k} \\
\text{n is old} &\Leftrightarrow \text{2k+1 for some integer k}
\end{align}
$$
==Definition Prime==
An integer n is prime if, and only if, $n >1$ and for all positive integers r and s, if $n = rs$, then either r or s equals n. An integer n is composite if, and only if, $n >1$ and $n =rs$ for some integers r and s with $1<r<n$ and $1<s<n$.

In symbols: For each integer n with $n >1$,
$$
\text{n is prime} \Leftrightarrow \forall r,s \in \mathbb{Z}^{+} ,n =rs\to(r=n\lor s=n)
$$
$$
\text{n is composite} \Leftrightarrow \exists r,s \in \mathbb{Z}^{+},n =rs \land(1<r<n) \land(1<s<n)
$$
Note that prime and composite are mutually exclusive event and both are negation of each other. n is prime iff r=n and s=1
or s=n and r=1. 

Since that r and s are positive integer so , as a factor $r,s\leq n$ . Observe that, $r,s\neq 0$ , Thus, $r,s\geq 1$ . Therefore, $1\leq r,s \leq n$ 

Since the negation of prime means n and r not equal to 1, thus $1<r,s<n$.

Why n>1?
Originally, ancient mathematicians (like Euclid) also excluded 1 from the list of primes, because:

- Primes were seen as “building blocks” of all other numbers.
    
- 1 is not a “building block”; it’s a multiplicative identity for multiplication $1\times n = n$

The Fundamental Theorem of Arithmetic states that:
	Every integer greater than 1 can be written _uniquely_ (up to order) as a product of prime numbers. 
If n=1 and can be negative then the above statement is wrong because
$$
\begin{array}
\ 6=2\times 3 \\
6=1 \times 2\times 3 \\
6=-2\times -3
\end{array}
$$

Notice that $p$ is prime iff $p$ has only 2 divisor which is 1 and itself which is $p$ .


==Theorem 1.1.1== The sum of any two even integers is even.

$$
\forall n,m \in \mathbb{Z},\text{ if n and m are even then m+n=2k for some integer k}
$$
Proof:
Suppose m and n are particular arbitrarily chosen element in the set of positive integer. We need to prove that $m+n =2k$ for some integer k. By definition, $m=2r$ and $n =2s$ for some integer $r,s$
$$
\begin{align}
m+n &=2r+2s \text{ by substitution}\\
&=2(r+s) \text{ distrbutive property}
\end{align}
$$

Let $t=r+s$. Note that t is an integer because it is a sum of integers. Hence,
$$
m+n =2t \text{ where t is an integer}
$$
It follows by definition of even that $m+n$ is even.


==Theorem 1.1.2== The difference of any odd integer and any even integer is odd.
Proof:
Suppose $m$ is arbitrary even integer and $n$ is arbitrary odd integer. By definition, $m=2k$ and $n =2s+1$ for some integer $k,s$ . WLOG,
$$
\begin{align}
m-n &=2k-(2s+1) \text{ by substitution}\\
&= 2(k-s)-1 \\
&=2(k-s)-1+2-2 \\
&= 2(k-s-1)+1
\end{align}
$$
Let $t=k-s-1$ . By distributive property,
$$t=k-(s+1)$$. Let $a=s+1$ , a is an integer because it is a sum of integers. Hence,
$$
t=k-a
$$
Thus, t is an integer because it is a difference of integers. Hence, 
$$
m-n =2(t)+1 \text{ for some integer t}
$$
Therefore it follow by definition of odd that $m-n$ is odd.

==Theorem 1.1.3== 
If $p$ is a prime number and $p>2$, then p is odd
Proof: Suppose $p$ is an arbitrary prime number and $p>2$. It is suffices to show that $p$ is odd. (Notice that it is hard to use direct proof in this case.)

We prove by its contrapositive which is if $p$ is even, then p is composite number or $p\leq 2$. Suppose $p$ is an arbitrary even number. By definition, $p=2k,k \in \mathbb{Z}$. Suppose $p>2$, then $k>1$ and $p\neq k$ . None of which is p.
Thus, $p$ have divisor other than 1 and itself. Therefore, $p$ is composite.

We can prove by contradiction. Assume $p$ is even. Then by definition, $p=2k$ for some integer k. Since $p\neq 2$ and $p\neq k$, it follow that p is composite.

%%Every integer that >2 and not equal to 2 is composite because is divisible by 2 which is not itself and 1.%%

==Corollary== 2 is the unique prime number that is even
Proof: By definition 2 is prime and even. By Theorem 4.3.1, no prime number greater than 2 is even. Thus, 2 is the only prime number that is even.


==Definition== A real number r is rational if, and only if, it can be expressed as a quotient of two integers with a nonzero denominator. A real number that is not rational is irrational. More formally, if r is a real number, then
$$
\text{r is rational }\Leftrightarrow\exists \text{ integers a and b such that }r=\frac{a}{b} \text{ and }b\neq 0
$$
Zero Product Property
If neither of two real numbers is zero, then their product is also not zero.

==Theorem 1.2.1==
Every integer is a rational number.

==Theorem 1.2.3== The sum of any two rational numbers is rational
Proof:
Suppose r and s are arbitrary rational numbers.. Then, by definition of rational, $r=\dfrac{a}{b}$ and $s=\dfrac{c}d{}$ for some integer a, b, c and d where $b,d\neq 0$
$$
\begin{align}
r+s&=\frac{a}{b}+\frac{c}{d} \text{ by substitution} \\
&= \frac{ad+bc}{bd}
\end{align}
$$
Let $p=ad+bc$ and $q=bd$ . p and q are integers because products and sums of integers are integers. Also $q\neq 0$ by zero product property.

Thus,
$r+s=\dfrac{p}{q}$ where p and q are some integers and $q\neq 0$

Therefore, $r+s$ is rational number by definition of rational number.

==Corollary 4.3.2== 
The double of a rational number is rational.

Thought( The double of a rational number is rational because it is a sum of itself)

Proof:
Suppose r is an arbitrary rational number, by definition $r=\dfrac{a}{b}$ where a and b are integers and $b\neq 0$. Noted that $2r=r+r$ . Thus, by Theorem 4.3.2, 2r is rational.

==Theorem 1.2.4== The negative of a rational number is rational
Proof: Suppose r is an arbitrary rational number. We need to prove that $-r$ is rational. By definition, $r=\dfrac{a}{b}$ for some integer a, b and $b\neq 0$. Then, $-r=\dfrac{-a}{b}$ . Since $-a$ is integer, it follow that $-r$ is rational.

==Theorem 1.2.5== If a is any even integer and b is any odd integer, then 
$$
\frac{a^{2}+b^{2}+1}{2} \text{ is an integer.}
$$



==Definition== Divisibility
If n and d are integers then n is divisible by d if, and only if, n equals d times some integer and $d\neq 0$.

Instead of “n is divisible by d,” we can say that
n is a multiple of d, or
d is a factor of n, or
d is a divisor of n, or
d divides n

$$
d \mid n \Leftrightarrow \exists k\in \mathbb{Z}, n =dk \land d\neq 0
$$
Why $d\neq 0$ ? It is because if $d=0$ , then $n$ must equal to 0.
Why k must be integer? It is because if k can be rational number, then it is possible that $n<d$ . Thus, it is consider as division instead of multiplication.

==Divisor of Zero==
$$
\forall a \in \mathbb{Z}, a\neq 0 \to a \mid 0
$$
$0=k \times a$ for any integer a and k. By zero product property, it is either $k=0$ or $a=0$ . By definition, $a\neq 0$ . Thus, $k=0$ .Therefore, $0=0 \times a$. Since a is any integer, thus the statement is true.

==Theorem 4.4.1== A Positive Divisor of a Positive Integer ^123

Extra knowledge
If $a<b$ and $c>0$, then $ac<bc$.

Proof:
For all integers a and b, if a and b are positive and a divides b then $a\leq b$.
Proof:
Suppose a and b are arbitrary positive integer and $a\mid b$. By definition $b=ak$ for some integer k. Since, a and b are positive, k must be positive. It follow that,
$$\begin{array}
\ k\geq 1 \\
\dfrac{b}{a}=k \\
\dfrac{b}{a} \geq 1 \\
b\geq a
\end{array}
$$



==Theorem 4.4.2== Divisors of 1
The only divisors of 1 are 1 and $-1$.

Extra knowledge:
1) If $ab>0$, then both a and b are positive or both are negative.
2) $(-m)(-n)=mn$


Proof:
$$
\forall n \in \mathbb{Z},n = 1\to n =rs \text{ such that }r,s=\pm 1
$$
Suppose s and r are arbitrary integers and $n =1$ and $n =rs$. By Theorem (Extra knowledge),  $r,s>0$ or $r,s<0$. By Theorem 4.4.1  $r,s\leq 1$ 

Case 1: $r,s>0$
Since $r,s\leq 1$ and $r,s>0$ . Thus, $0<r,s\leq 1$ . Thus, the only possibility of r, s is 1

Case 2: $r,s<0$
By Theorem (Extra knowledge 2) $(-r)(-s)=rs=1$.  In this case, $-r$ and $-s$ are positive divisor of 1 thus $-r,-s=1$ . It follow that $r,s=-1$ .


==Question==
1) Prove that there exist irrational numbers a and b such that $a^{b}$ is rational.



2) Prove that for every positive integer k, $k^{2}+2k+1$ is composite.
Proof:
Suppose $k \in \mathbb{Z}$ such that $k> 0$. Notice that, $k^{2}+2k+1=(k+1)^{2}$
We need to show that $1<k+1<k^{2}+2k+1$
Since $k> 0$, hence
$$
k+1>1
$$
Thus, since $k+1> 1$, thus it follow that $k+1<(k+1)^{2}=k^{2}+2k+1$
Therefore, it follow that $1<k+1<k^{2}+2k+1$. Thus, it follow that $k^{2}+2k+1$ is composite.


==Definition==
For all integers *n* and *d* , $d\not\mid n \Leftrightarrow \dfrac{n}{d}$ is not an integer


==Theorem== Transitivity of Divisibility
For all integer a, b, and c, if $a\mid b$ and $b\mid c$ then $a\mid c$

==Theorem== Divisibility by a Prime
Any integer $n >1$ is divisible by a prime number.
Proof:
Suppose n is an arbitrary integer and $n >1$. if n is prime, then n is divisible by a prime number(namely itself), and we are done. If n is not prime,

$n =r_{0}s_{0}$ where $r_{0}$ and $s_{0}$ are integers and 
$1<r_{0}<n$ and $1<s_{0}<n$.

It follows by definition of divisibility that $r_{0}\mid n$ .(We introduce the definition of divisibility here to use the transitivity of divisibility)
Noticed that $r_{0}$ can be prime or composite. If $r_{0}$ is prime , then $r_{0}$ is divisible by a prime number(namely itself) and $r_{0}\mid n$ .Thus, we are done. If $r_{o}$ is not prime, then

$r_{0} =r_{1}s_{1}$ where $r_{1}$ and $s_{1}$ are integers and 
$1<r_{1}<r_{0}$ and $1<s_{1}<r_{0}$.

it follow by definition of divisibility $r_{1}\mid r_{0}$ and by transitivity of divisibility $r_{1}\mid n$ . If $r_{1}$ is prime then $r_{1}$ is divisible by a prime number namely itself and we are done. If $r_{1}$ is not prime, then 

$r_{1} =r_{2}s_{2}$ where $r_{2}$ and $s_{2}$ are integers and 
$1<r_{2}<r_{1}$ and $1<s_{2}<r_{1}$.

We may continue in this way, factoring successive factors of n until we find a prime factor. We must succeed in a finite number of steps because each new factor is both less than the previous one (which is less than n) and greater than 1, and there are fewer than n integers strictly between 1 and n.* Thus we obtain a sequence

$$
r_{0},r_{1},r_{2},\dots,r_{k}
$$
where $k\geq 0$ , $1\leq r_{k}\leq r_{k-1}\leq\dots\leq r_{2}\leq r_{1}\leq r_{0}\leq n$ and $r_{i} \mid n$ for each $i=0,1,2,\dots,k$. The condition for termination is that $r_{k}$ should be prime. Hence $r_{k}$ is a prime number that divides n.
^709f3d

%%* this statement is justified by an axiom for the integers called the well-ordering principle, which is discussed in Section 5.4. Theorem 4.4.4 can also be proved using strong mathematical induction, as shown in Example 5.4.1.%%


==Theorem== Unique Factorization of Integers Theorem (Fundamental Theorem of Arithmetic) ^fta-statement

Given any integer $n >1$, there exist a positive integer k, distinct prime numbers $p_{1},p_{2},\dots,p_{k}$, and positive integers $e_{1},e_{2},\dots,e_{k}$ such that
$$
n =p_{1}^{e_{1}}\dots p_{k}^{e_{k}}
$$
and any other expression for n as a product of prime numbers is identical to this except, perhaps, for the order in which the factors are written.

*(For the Existence proof via Strong Induction, see [[Chapter 5 Sequences and Mathematical Induction#^fta-existence|Chapter 5]]. For the Uniqueness proof via Euclid's Lemma, see [[Uniqueness of FTA]]. For the complete structural chain, see [[Logical Architecture from WOP to FTA]].)*

%%Exercises for Sections 5.4 and 8.4.%%
