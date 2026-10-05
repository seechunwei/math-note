
Sequence is a list of object which exist element one after another.

Since all the mathematic object is a set. A sequence is also a set which can be defined by:

An infinite sequence is a function whose domain is the set of positive integers.

For example $S=\{ (x,y) \in \mathbb{N}\times Y|(x,y)\in R \}$ 
$S=\{ (1,a_{1}),(2,a_{2}),\dots \}$

Formally, the sequence $a_{1},a_{2},a_{3},\dots$ is a function f with domain $\mathbb{Z}^{+}$ such that $f(i)=a_{i}$ for all $i\in \mathbb{Z}^{+}$.
$$
f:[n] \mapsto \mathbb{R}
$$
$$
[n]=\{ 1,2,3,\dots,n \}
$$

$\{ a_{1},\dots,a_{k} \}$: sequence
$a_{1}+a_{2}+\dots+a_{k}$ : real number

$\{ a_{1},\dots \}$ : sequence
$a_{1}+\dots$ : Series 
(series is the sum of infinitely many terms, one after the other)

$\sum_{i=0}^{99}i$ : the term change depend on the change of index
Total 100 terms because i start from 0

$\sum_{i=0}^{99}7$ : independent, the terms are independent form its index
Thus,
$$
\begin{align}
\sum_{i=0}^{99} 7&=\underbrace{7+7+\dots+7}_{\text{100 terms}} \\
&=100(7) \\
&=7 \\
&=7(1+1+\dots+1) \\
&=7\sum_{i=0}^{99} 1
\end{align}
$$

Principle of Mathematical Induction
To prove a statement of the form:“ For all positive integers n, property P(n) is true”, perform the following two steps:

Step 1 (basis step) Show that P(a) is true.
Step 2 (induction step) Suppose n is an arbitrary positive integer and suppose P(n) is true. Show that P(n+ 1) is true.

The supposition that P(n) is true is called the induction hypothesis.

To apply mathematical induction we need to have a starting point. The core part of the proof is to use the property of P(n) to prove P(n+1) so that we can keep the dice rolling. That is by induction hypothesis we need to show that P(n+1) is true.

If we need to show something is equal write in this form
$$
a=b=c
$$
==Theorem==
For all integers $n\geq{1}$ ^34da58
$$
1+2+3+\dots+n = \frac{n(n+1)}{2}
$$
Proof.:
We argue by mathematical induction. Let the property $P(n)$ be defined as follow:
$$
P(n):1+2+3+\dots+n = \frac{n(n+1)}{2}
$$

For the basis step, it is clear that P(1) is true because
$$
P(1)=1=\frac{1(1+1)}{2}
$$
For the induction step, suppose n is an arbitrary positive integer and suppose P(n) is true. We need to show that $P(n+1)$ is true.
$$
\begin{align}
1+2+3+\dots+n+(n+1)&=\frac{n(n+1)}{2}+(n+1) \text{ by IH} \\
&=\frac{n^{2}+n+2n+2}{2} \\
&=\frac{n^{2}+3n+2}{2} \\
&=\frac{(n+2)(n+1)}{2} \\
&=\frac{n+1((n+1)+1)}{2}
\end{align}
$$
Therefore $P(n+1)$ is true. Therefore, by the Principle of Mathematical Induction, we conclude that P(n) is true for all positive integers n.

What is the difference of derivation and proof?
Derivation is a sequence of step that construct a formula. It answers the question, **"Where did this formula come from?"**

A proof is a logical argument that establishes the truth of a statement beyond doubt. It answers the question, **"How do we know this is always true?"**

**Derivation** often involves spotting patterns or making "educated guesses" based on limited data. **Proof** is the safety net that ensures those patterns don't suddenly break when we aren't looking.

In mathematics, we call that a **conjecture**. It's a suspicion that something is true, but it's not a fact yet.

**Moser’s Circle Problem**.
Imagine you place distinct points on the edge of a circle and connect every point to every other point with a straight line. We want to count the maximum number of **regions** these lines create inside the circle.

| **Number of Points (n)** | **Number of Regions** |
| ------------------------ | --------------------- |
| 1                        | 1                     |
| 2                        | 2                     |
| 3                        | 4                     |
| 4                        | 8                     |
| 5                        | 16                    |
|                          |                       |

That is the most logical guess! If we look at the sequence $1, 2, 4, 8, 16$, it looks exactly like the powers of 2 ($2^{n-1}$). Most people would bet money on the next number being 32.

Here is the twist: If you actually draw the circle with 6 points and count the regions, the answer is **31**.

The pattern breaks! The actual formula for the number of regions is much more complex:

$$\text{Regions} = \binom{n}{4} + \binom{n}{2} + 1$$



==Theorem==
Any sum of n even integers is even
Suppose n is arbitrary even integer. $n_{1}+n_{2}+n_{3}+\dots+n_{n}$ where $n_{i}=2k$ where $0<i\leq n$.

$$
\sum_{i=1}^{n} 2k=2\times \sum_{i=1}^{n} k
$$
Since $\sum_{i=1}^{n}k$ is an integer because it a sum of integers. Thus by definition, Any sum of n even integers is even.

Why we cannot prove like this?
Distributive property:
$$n_1 + n_2 + \dots + n_n = 2k_1 + 2k_2 + \dots + 2k_n = 2(k_1 + k_2 + \dots + k_n)$$
In standard algebra, the distributive property is defined for **two** numbers: $a(b+c) = ab + ac$.

While this seems obvious, strictly speaking, moving from "2 numbers" to "$n$ numbers" **is** a jump that requires Induction. You cannot just say "..." and assume the rules of algebra don't break when the list gets infinitely long.

1) The core idea of this formal proof is:
Addition is Binary. To compute the sum, there is a last addition and the final sum is of the form $L + R$..."

Consider their sum when parentheses are arbitrarily but validly inserted (it means that no matter how you insert the parenthesis, the last addiction must be only 2 summands)

2) Why strong Induction
When there is $n+1$ terms, we cannot show that $n+1$ is true by using the property of n . When we split a sum of $n+1$ integers into $L + R$, we don't know how big $L$ and $R$ are.
But we know that $L$ and $R$ is a sum $\leq n$ ,thus we need to assume that $P(a),P(a+1),\dots P(n)$ is true because it is rely on several previous step.

When to use Mathematical Induction

Use this when the statement for number $100$ depends on the statement for number $99$ being true.

**The Signs:**

- **The "..." (Ellipsis):** If the problem has "..." (like $1+2+\dots+n$), it is a huge red flag for Induction. The "..." hides a growing chain of operations.
    
- **Recursive Definitions:** If a sequence is defined as $a_{n} = a_{n-1} + 5$.
- N+1 is depend on N
    
- **$n$ is in the Exponent:** Proving $2^n > n^2$.
    
- **"For all integers $n \geq 1$":** Especially if proving it for a specific huge number (like $n=1000$) would require doing the same step 1000 times.

the argument is made that each term among those indicated by the ellipsis(···)has such-and-such an appearance and when these are cancelled such-and-such occurs. But it is impossible actually to see each such term and each such cancellation, and so the accuracy of these claims cannot be fully checked. With mathematical induction it is possible to focus exactly on what happens in the middle of the ellipsis and verify without doubt that the calculations are correct.

Why it is suitable to use mathematical induction when n is exponent. it is because exponent function where domain is $[n]$ is a recursive sequence where $n+1$ is just multiple of $n$ with some number(base). 

For example,
For all nonnegative integers n, $2^{2n}-1$ is divisible by 3
Proof: Let the
$$P(n):2^{2n}-1 \text{  is divisible by 3}$$
We argue by mathematical induction.
For the basis step, it is clear that $P(0)$ is true because $P(0)=2^{2(0)}-1=0$ is divisible by 3.

For induction step we suppose n is arbitrary integer with $n\geq 0$  and $P(n)$ is true. (We need to show that P(n+ 1) is true, that is, $2^{2n+1}-1$ is divisible by 3.)
$$
\begin{align}
2^{2(n+1)}-1&=2^{2n+2}-1 \\
&=2^{2n}\cdot 2^{2}-1 \\ 
&=2^{2n}(3+1)-1 \\ 
&=2^{2n}(3)+2^{2n}-1 \\
\end{align}
$$
By definition $2^{2n}-1=3k$ for some integer k. Thus,
$$
\begin{align}
2^{2(n+1)}-1&=2^{2n}(3)+3k\\
&=3(2^{2n}+k)
\end{align}
$$
Thus, $2^{2(n+1)}$ is divisible by 3. Hence, $P(n+1)$ is true.
Therefore, by the Principle of Mathematical Induction, we conclude that $P(n)$ is true for all nonnegative integers n.

==Remark==
Why in the first step, we can write like this?
$2^{2n+1}-1=2^{2n+1}-1$
Actually this statement include 2 property one is $2^{2n+1}-1$ the formula for sequence itself and $2^{2n}-1$ is divisible by 3. For the formula the statement didn't state that it is a summation or product of sequence thus it is just a number in this form, thus we no need to use mathematical induction to prove $2^{2n+1}-1$. Thus, we can straight away substitute the $n+1$ in the formula.


==Theorem==
For all integers $n\geq 3$, $2^{n}>2n+1$
Proof: Let the property $P(n)$ be defined as follows:
$$
P(n):2^{n}>2n+1
$$
We argue by mathematical induction.
For basis step, it is clear that $P(3)$ is true because $2^{3}=8>7=2(3)+1$.

For induction step, suppose n is an arbitrary integer with $n\geq 3$ and suppose $P(n)$ is true.
$$
\begin{align}
2^{n+1}&=2(2^{n}) \\
2^{n+1}&>2(2n+1) \\
2^{n+1}&>4n+2 \\
&>2n+2n+2 \\
&>2n+1+2 (\text{ since }n\geq 3 \text{ implies }2n>1) \\
&>2n+3 \\
&>2(n+1)+1
\end{align}
$$
Since, $2^{n+1}>2(n+1)+1$, Hence $P(n+1)$ is true. Therefore, by the Principle of Mathematical Induction, we conclude that P(n) is true for all integers n≥3.


==Example==
Suppose $a_{1},a_{2},a_{3},\dots$ is defined (recursively) by
$$
a_{1}=2 \text{ and } a_{n}=\frac{a_{n-1}}{n} \text{ for all integers }n\geq 2
$$
Prove that for all positive integers $n$, $a_{n}=\frac{2}{n!}$ where $n!=1\cdot{2}\cdot{3}\cdot\dots \cdot n$.
Proof: Let the property $P(n)$ defined as follows.
$$
P(n):a_{n}=\frac{2}{n!}
$$
We argue by mathematical induction.
For the basis step, it is clear that $P(1)$ is true because $a_{1}=2=\dfrac{2}{1!}$.

For the induction step, suppose n is an arbitrary positive integer and $P(n)$ is true, Thus,
$$
\begin{align}
a_{n+1}&=\frac{a_{n}}{n+1} \\
&=\left( \frac{2}{n!} \right)\left( \frac{1}{n+1} \right) \\
&=\frac{2}{(n+1)!}
\end{align}
$$
Therefore, $P(n+1)$ is true. Therefore, by the Principle of Mathematical Induction, we conclude that P(n) is true for all positive integers n.

==Example of non-numerical puuzle==
**Golomb's Tromino Theorem**.

Given a $2^{n}\times 2^{n}$ square checkerboard we can use tromino to fill the checkerboard but leave one corner uncovered.

The main idea is 
$$
\begin{align}
2^{n+1}\times 2^{n+1}&=2(2^{n})\times 2(2^{n}) \\
&=(2^{n}+2^{n})\times(2^{n}+2^{n})
\end{align}
$$
Thus, the $2^{n+1}\times 2^{n+1}$ checkerboard is just four $2^{n}\times 2^{n}$ checkerboard assemble together. Thus, we can use the property of $P(n)$ to prove $P(n+1)$.

==Question==
Prove by mathematical induction that for every positive integer n,
$$
\frac{1}{3}=\frac{1+3+5+\dots+(2n-1)}{(2n+1)+(2n+3)+(2n+5)+\dots[2n+(2n-1)]}
$$
Proof: 
Let the property $P(n)$ be defined as follows.
$$
P(n):(2n+1)+(2n+3)+(2n+5)+\dots+[2n+(2n-1)]=3[1+3+5+\dots+(2n-1)]
$$

It suffices to show P(n) is true for all positive integers n. We argue by mathematical induction. 
For the basis step, it is clear that P(1) is true because 2(1) + 1 = 3 = 3(1).
For the induction step, suppose n is an arbitrary positive integer and suppose P(n) is true. We need to show that P(n+ 1) is true, that is,

$$
\begin{align}
&(2(n+1)+1)+(2(n+1)+3)+(2(n+1)+5)+\dots+[2(n+1)+(2(n+1)-1)] \\
&=3[1+3+5+\dots+[2(n+1)-1]]\\
\end{align}
$$

Left hand side of equation
$$
\begin{align}
&=(2n+3)+(2n+5)+(2n+7)+\dots+(2n+2+2n+2-1) \\
&=(2n+3)+(2n+5)+(2n+7)+\dots+(4n-1)+(4n+1)+(4n+3) \\
&=(2n+1)+(2n+3)+(2n+5)+\dots+(4n-1)+(4n+1)+(4n+3)-(2n+1) \\
&=3[1+3+5+\dots+(2n-1)]+(4n+1)+(4n+3)-(2n+1)  \text{ by IH}\\ 
&=3[1+3+5+\dots+(2n-1)]+6n+3 \\
&=3[1+3+5+\dots+(2n-1)+2n+1] \\
&=3[1+3+5+\dots+(2n-1)+[2(n+1)-1]] \\
&=\text{ Right hand side}
\end{align}
$$

Thus, $P(n+1)$ is true. Therefore, by the Principle of Mathematical Induction, we conclude that P(n) is true for all positive integers n.


==question==
Cannot understand the property, don't know which one is definition and which one is formula. What if i exchange the equation?

So the answer is actually there are 3 things: the original sequence, the sequence definition , the sequence formula. Usually, sequence formula is more compact and simple while sequence definition is the thing to represent the sequence. In this case the more complicated sequence is LHS and the simple one is RHS. But we can just exchange it in this case.

$P(n+1)=(2n+1)+(2n+3)+(2n+5)+\dots+[2n+(2n-1)]+[2(n+1)+(2(n+1)-1)]$
It is not the case, noticed that each term of the summation is depend on the n which is the number of term. Thus, when n change to n+1 every term will change.


The sequence can be view as this:
$$
\sum_{k=1}^{n} 2n+(2k-1)
$$
This mean that the n here is actually playing 2 different role at the same time.
1) $2n$ is a constant because the n here is the number of term. It determines the starting point of the sequence. if $n$ change to $n+1$. The sequence will move 1 term from the starting point and add a last term

2) $2k-1$ or $2n-1$ is the variable term that keep on changing depending on the index $n$. When $n$ change to $n+1$ the new sequence will extend one term +2.

Combining effect
his explains why the difference between the "Old Last Term" and "New Last Term" is 4.

This explain why there exist a missing term $4n+1$ 

1. **Shift in Base:** $+2$ (because $n \to n+1$)
2. **Shift in Index:** $+2$ (because $k$ steps forward)
3. **Total Change:** $2 + 2 = \mathbf{4}$



Principle of Strong Mathematical Induction
Suppose a is an integer and P(n) is a property that is defined for all integers n≥a. Suppose the following two statements are true.
1. P(a) is true.
2. For all integers $n\geq a$, if  P(a), P(a+ 1), P(a+ 2), . . ., and P(n) are true, then P(n+ 1) is true. Then P(n) is true for all integers n≥a.


Method of Proof by Strong Mathematical Induction
Suppose a is an integer.  To prove a statement of the form:“ For all integers n≥a, property P(n) is true”, perform the following two steps:
Step 1 (basis step) Show that P(a) is true.
Step 2 (induction step)  Suppose n is an arbitrary integer with n≥a and suppose P(k) is true for every a≤k≤n.  Show that $P(n+1)$ is true.


The main difference of strong mathematical induction and ordinary mathematical induction is the induction hypothesis. 

To prove $P(n+1)$, not only you have the truth of $P(n)$ at your supposition, you have the stronger induction hypothesis that supposes that P(k) is true for every a≤k≤n.


==Theorem== Every integer $n\geq 2$ is divisible by a prime number.
[[Basic number theory proof#^709f3d]]
Alternative proof:
Let the property $P(n)$ be defined as follow.
$$
P(n): \text{ n is divisible by a prime number}
$$
We argue by strong mathematical induction.

For the basis step, it is clear that $P(2)$ is true because 2 is divisible by a prime number which is itself.

For the induction step, suppose n is an arbitrary integer with $n\geq 2$ and suppose $P(k)$ is true for every $2\leq k\leq n$. (We need to show that $P(n+1)$ is true, that is, $n+1$ is divisible by a prime number.)

Case 1. $n+1$ is a prime number.
Then $n+1$ is certainly divisible by a prime number, namely itself.

Case 2. $n+1$ is not a prime number.
By definition, $n+1=ab$ for some integer $ab$ where $1<a<n+1$ and $1<b<n+1$. Since, $2\leq a\leq n$, by the induction hypothesis, $P(a)$ is true. Hence a is divisible by a prime number, say p. Since $p\mid a$ and $a \mid (n+1)$ , by transitivity $p \mid (n+1)$. Thus, $n+1$ is divisible by a prime number.

In either case, $P(n+1)$ is true. Therefore, by the Principle of Strong Mathematical Induction, we conclude that P(n) is true for all integers n≥2.


==Remark==
Why we need to separate into cases which is prime and not prime(composite), it is because by using the definition we can write $n+1$ as a product of some integer, let alone if $n+1$ is prime then the proof is done. So we can only focus on composite case.


### ==Theorem== (Fundamental Theorem of Arithmetic) ^fta-existence
Suppose $n>1$ is any integer. Then there exist a positive integer k, distinct prime numbers  $p_{1},p_{2},\dots,p_{k}$,  and positive integers $e_{1},e_{2},\dots{e}_{k}$, such that:
1. $n =p_{1}^{e_{1}}p_{2}^{e_{2}}\dots p_{k}^{e_{k}}$
2. Any other expression for n as a product of prime numbers is identical to this except, perhaps, for the order in which the factors are written.

*(For the Uniqueness proof via Euclid's Lemma, see [[Uniqueness of FTA]]. For the full pipeline, see [[Logical Architecture from WOP to FTA]].)*

Proof of existence. Let the property $P(n)$ be defined as follows.
$$
P(n): \text{the statement}
$$
We argue by strong mathematical induction.
For the basis step, it is clear that $P(2)$ is true because 2 is prime and so $2=2^{1}$ , where $k=1$, $p_{1}=2$ and $e_{1}=1$.

Case 1: $n+1$ is prime.
Similarly as in the basis step, $P(n+1)$ is true trivially.

Case 2: $n+1$ is composite
Then by definition $n+1=ab$ for some integer $a,b$ such that $2\leq a\leq n$ and $2\leq b\leq n$. Thus, by induction hypothesis, $P(a)$ is true. Hence, $a=p_{1}^{e_{1}}p_{2}^{e_{2}}\dots p_{k}^{e_{k}}$ for some integer k and distinct prime numbers  $p_{1},p_{2},\dots,p_{k}$,  and positive integers $e_{1},e_{2},\dots{3}_{k}$ . Similarly $P(b)$ is true. Hence, $b=q_{1}^{f_{1}}q_{2}^{f_{2}}\dots q_{i}^{f_{i}}$ for some...... Now $n+1=p_{1}^{e_{1}}p_{2}^{e_{2}}\dots p_{k}^{e_{k}}q_{1}^{f_{1}}q_{2}^{f_{2}}\dots q_{i}^{f_{i}}$. Note that some $p_{k}$ may be identical with some $q_{i}$. By combining the identical primes, it follows that $P(n+1)$ is true.

In either case, $P(n+1)$ is true. Therefore, by the Principle of Strong Mathematical Induction, we conclude that P(n) is true for all integers n≥2.

==Remark==
These 2 proof use the same idea that is analysis into cases and write it as a product of 2 integer (composite definition). The similarity of these proof is both of them is talking about product, divisibility.




