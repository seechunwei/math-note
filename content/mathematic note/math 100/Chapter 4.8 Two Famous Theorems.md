This section contains proofs of two of the most famous theorems in mathematics: that $\sqrt{ 2 }$ is irrational and that there are infinitely many prime numbers


==Theorem Irrationality of== $\sqrt{ 2 }$
$\sqrt{ 2 }$ is irrational.
Proof:
Suppose,$\sqrt{ 2 }$ is rational. Then there are integers $m$ and $n$ with no common factors such that
$$
\sqrt{ 2 }=\frac{m}{n}
$$
Squaring both side of equation gives
$$
\begin{align}
2&=\frac{m^{2}}{n^{2}} \\
2n^{2}&=m^{2}
\end{align}
$$
Since $n^{2}$ is an integer because sum of integers are integers, it follow that $m^{2}$ is even. Thus, it follow that $m$ is even. By definition $m=2k$ for some integer k.

By substitution,
$$
m^{2}=(2k)^{2}=4k^{2}=2n^{2}
$$

Dividing both sides of the right-most equation by 2 gives
$$
n^{2}=2k^{2}
$$
Thus, $n^{2}$ is even and $n$ is even. Hence both m and n have a common factor of 2. But this contradicts the supposition that m and n have no common factors.


==Proposition==
$1+3\sqrt{ 2 }$ is irrational.
Proof:
Suppose $1+3\sqrt{ 2 }$ is rational. Thus there exists integers $m$ and $n$ such that 
$$
1+3\sqrt{ 2 }=\frac{m}{n} \text{ where }n \neq 0
$$
it follow that
$$
\begin{align}
3\sqrt{ 2 }&=\frac{m}{n}-1 \\
&=\frac{m-n}{n} \\
\sqrt{ 2 }&= \frac{m-n}{3n} 
\end{align}
$$
Note that $m-n$ and 3$n$ are integers because the difference and product of integers are integers and $3n \neq 0$ by the zero product property. Thus, by definition $\sqrt{ 2 }$ is rational. This contract the fact that $\sqrt{ 2 }$ is irrational.



Are There Infinitely Many Prime Numbers?
Euclid’s proof requires one additional fact we have not yet established: If a prime number divides an integer, then it does not divide the next successive integer.

==Proposition==
For any integer $a$ and any prime number p, if $p \mid a$ then $p \not\mid (a+1)$.

Understand intuitively. $p \mid a$ means $a=pk$ for some integer k. Since the smallest prime number is 2 , thus at least adding 2 is the condition for a to be divisible by p.

$$
a+1=pk+1
$$
if we are at $a$ (which is a multiple of $p$), the next multiple is at $a + p$.
 The previous multiple was at $a - p$.
Since the smallest prime is 2 ($p \ge 2$), the "gap" to the next multiple is always at least 2. Therefore, taking just one step ($+1$) lands you in the space _between_ multiples.




Proof: 
Suppose there exist an integer $a$ and a prime number $p$ such that $p\mid a$ and $p\mid(a+1)$. Then by definition of divisibility, there exists integers $r$ and $s$ such that $a=pr$ and $a+1=ps$ .It follow that 
$$
\begin{align}
1&=ps-a \\
&=ps-pr \\
&=p(s-r)
\end{align}
$$
and since ($s-r$) is an integer $p \mid 1$. But by Theorem, the only integer divisor of 1 are 1 and -1 and $p>1$ because p is prime. Thus, $p\leq 1$ and $p>1$, which is a contradiction. 


The idea of Euclid’s proof is this: Suppose the set of prime numbers were finite. Then you could take the product of all the prime numbers and add 1. By Theorem 4.4.4 this number must be divisible by some prime number. But by Proposition 4.8.3, this number is not divisible by any of the prime numbers in the set.
[[Basic number theory proof#^709f3d]]


$\mathbb{N}=\{ 1,2,3,4,\dots \}$
$\mathbb{Z}=\{ \dots,-3,-2,-1,0,1,2,3,\dots \}$

==Theorem Infinitude of the Primes==
The set of prime numbers is infinite.
Proof:
Suppose not. That is, suppose the set of prime number is finite.
Since it is a finite set, some prime number $p$ is the largest of all the prime numbers, hence we can list the prime numbers in ascending order:
$$
2,3,5,7,\dots,p
$$
Let N be the product of all the prime numbers plus 1:
$$
N=(2\cdot 3 \cdot 5 \cdot 7 \dots p)+1
$$
Then $N>1$%%Condition for it to be divisible by some prime number%%, and so, by Theorem 4.4.4, N is divisible by some prime number $q$. Because q is prime, q must equal one of the prime numbers 2, 3, 5, 7, 11,$\dots$, p. Thus, by definition of divisibility, q divides $2\cdot 3\cdot 5 \dots p$, and so, by Proposition 4.8.3, q does not divide $(2\cdot 3 \cdot 5 \cdot 7 \dots p)+1$, which equals N. Hence N is divisible by q and N is not divisible by q, and we have reached a contradiction.




Remark: To prove something that is infinite, prove by contradiction which is suppose it is a finite set, use the property of finite set(commutative, last term, finite sum) deduce that that exists some number belong to the set but not being listed in the set, which contradiction happened 


==Euclid's Lemma== tutorial 6 q8
If a prime number $p$ divides the product of two integers $a$ and $b$ (written as $p \mid ab$), then $p$ must divide $a$ or $p$ must divide $b$ (or both).

$$p \mid ab \implies p \mid a \quad \text{or} \quad p \mid b$$
![[Euclid lemma.png]]

Euclid's lemma is used to prove the [[Uniqueness of FTA]].



==Theorem==  (Tutorial 6 q5b)

FTA approach(We can also use Euclid's lemma to prove and we can use this to prove irrationality of any prime number)
For any prime p and any integer $m>1$, if $p\mid m^{2}$, then $p \mid m$
Proof: Suppose m is an arbitrary integer and p is an arbitrary prime and $p \mid m^{2}$. Thus, it follow that $m>1$
By unique factorization theorem
$$m = p_1^{e_1} \cdot p_2^{e_2} \cdot \dots \cdot p_k^{e_k}$$
Where $p_1, \dots, p_k$ are distinct prime numbers and $e_i \geq 1$.

Prime Factorization of $m^2$

To get $m^2$, we square the expression above:

$$m^2 = (p_1^{e_1} \cdot p_2^{e_2} \cdot \dots \cdot p_k^{e_k})^2$$

$$m^2 = p_1^{2e_1} \cdot p_2^{2e_2} \cdot \dots \cdot p_k^{2e_k}$$

Analysis
We are given that a prime $p$ divides $m^2$. For a prime to divide a number, that prime must appear in the number's unique factorization.

- Looking at the factorization of $m^2$, the only primes that exist in it are the set $\{p_1, p_2, \dots, p_k\}$.
- Therefore, $p$ must be one of these primes ($p = p_i$ for some $i$).
 Conclusion
If $p$ is one of the primes in the set $\{p_1, \dots, p_k\}$, and since $m = p_1^{e_1} \cdots p_k^{e_k}$, it follows by definition that $p \mid m$.

This proposition can be more general
1) $n^{th}$ power
2) Bi Conditional
For any prime $p$ and integer $m$:

$$p \mid m^n \iff p \mid m$$
1) The "Square-Free" Generalization
Let $k$ be an integer. The statement "$k \mid m^2 \implies k \mid m$" is true **if and only if** $k$ is a **square-free integer**.

A "square-free" integer is a number not divisible by any perfect square other than 1 (e.g., 6, 10, 30 are square-free; 12, 18, and 4 are not).

Why it is square free integer. Let  look at one counter example let $k=12$ and $m=6$. Thus $12\mid 6^{2}$ which is 36 but $12 \not\mid 6$ Why? The power is the key point. Let see the prime factor of each number:
$12=2^{2}\cdot{3}$
$6=2\cdot 3$
$36=2^{2}\cdot 3^{2}$
$12\mid 36$ because the power of factor 2 for 12 is $\leq$ 36. But since the factor of 2 for 6 is less than 12 thus $12\not\mid 6$. Thus square free integer $k$ assure that the highest power of each of the prime factor is 1. Thus, $m^{2}$ is just the square of $m=p_{1}\cdot p_{2}\cdot\dots \cdot p_{i}$ which is $p_{1}^{2} \cdot p_{2}^{2}\dots p_{i}^{2}$ . Thus, k divide $m^{2}$ means that the prime factor of k is the subset of prime factor of $m^{2}$ and since k is square free integer thus it must divide m.


==Exercise==
Prove that for any prime number $p$ and integer $n \ge 2$, $\sqrt[n]{p}$ is irrational.
Proof:
Prove by contradiction. Suppose $\sqrt[n]{p  }$ is rational such that  $p$ is an arbitrary prime and $n$ is an arbitrary integer and $n \geq 2$
Thus, by definition,
$$
\begin{align}
\sqrt[n]{p }&=\frac{a}{b} \text{ for some integer a and b} \\
p&=\frac{a^{n}}{b^{n}} \\
p\cdot b^{n}&=a^{n}
\end{align}
$$
Thus, $p\mid a^{n}$ and by theorem $p\mid a$ . Thus, by definition
$$
a=pk \text{ for some integer k}
$$
By substitution,
$$
\begin{align}
p\cdot b^{n}=(pk)^{n} \\
p\cdot b^{n}=p^{n}\cdot k^{n} \\
b^{n}=p^{n-1}\cdot k^{n} \\
\end{align}
$$
Look at the new equation $b^n = p^{n-1} \cdot k^n$.

Since $n \ge 2$, the term $p^{n-1}$ contains at least one factor of $p$. Therefore, the right side is divisible by $p$, which means the left side ($b^n$) must also be divisible by $p$.

$$p \mid b^n$$
Thus, by the proposition $p\mid b$. Thus, $p\mid a$ and $p\mid b$ . Thus, a and b have common factor p which contradict the supposition that $\frac{a}{b}$ have no common non-trival factor.


$12=2^{2}\cdot{3}$
$6=2\cdot 3$
$36=2^{2}\cdot 3^{2}$


==Question==
Suppose a,b, and c are odd integers and suppose z is a solution of $ax^{2}+bx+c=0$. Prove that z is irrational.

$ap^{2}+bpq+cq^{2}=0$

### Conclusion of the Proof

We have now shown a complete contradiction:

1. We assumed $z$ was a rational number $p/q$.
2. This implied that $ap^2 + bpq + cq^2 = 0$.
3. However, if $a, b, c$ are odd, the expression $ap^2 + bpq + cq^2$ is **always odd**, regardless of the integers $p$ and $q$ (as long as they aren't both even).
4. Since 0 is an even number, an odd sum cannot equal 0.
Therefore, our initial assumption was false. **$z$ must be irrational.**

Why we use modulo 2 as the main idea of proof, because the condition state that a, b, c are odd, so since parity of coefficient is fixed and the sum of it is even thus we can manipulate the parity of z to lead to a contradiction.

Besides, we always use proof by contradiction to prove irrationality, with the assumption of $z=\frac{a}{b}$ for some integer a, b and $b\neq{0}$ and both of them don't have common nontrivial factor. This also imply that a and b are not even.  
