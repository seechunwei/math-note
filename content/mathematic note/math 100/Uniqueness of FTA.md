Statement:
For any integer $n>1$, there exist an unique representation

$$
n =p_{1}^{e_{1}}p_{2}^{e_{2}}\dots p_{k}^{e_{k}}
$$
where $p_{k}$ is some distinct prime number and $k$ is some positive integer. (Why positive integer? Because $a^{0}=1$ for all $a$, thus it will have infinitely many representation)

Proof of uniqueness by WOP:
Suppose the statement is wrong for the sake of contradiction. Thus, by WOP there exist a smallest number say $n$ that have 2 different prime factorization representation. 
$$
n =p_{1}p_{2}\dots p_{k}=q_{1}q_{2}\dots q_{s}
$$
where $p_{k}$ and $q_{s}$ are prime number and $p_{1}\leq p_{2}\leq\dots\leq p_{k}$ and $q_{1}\leq q_{2}\leq\dots\leq q_{s}$.  (Why we need this? Because order is the only  thing that can make difference).

We know that $p_{1}| n\implies p_{1}| (q_{1}q_{2}\dots q_{s})$.  By Euclid lemma, it follow that $p_{1}| q_{m}$ for some $m$. Since $p_{1}$ and $q_{m}$ are prime numbers, it follow that $p_{1}=q_{m}$. From the order, we know that $q_{1}\leq q_{m}=p_{1}$.

Same deduction, we will get $q_{1}|p_{m_{1}}$ for some integer $m_{1}$ which implies that $q_{1}=p_{m_{1}}$. From the order, we know that $p_{1}\leq p_{m_{1}}=q_{1}$. Thus, combine with 2 condition, it follow that $p_{1}=q_{1}$.

Let $n'=\frac{n}{p_{1}}$. Since $p_{1}=q_{1}$, it follow that
$$
n'=p_{2}p_{3}\dots p_{k}=q_{2}q_{3}\dots q_{s}
$$
Notice that $p_{1}>1$, thus $n'<n$, and $n'$ have 2 different representation which contradict our supposition that $n$ is the smallest number that hold this statement. $\blacksquare$


Proof by induction: 
Let $P(k)$ defined as $$ n =p_{1}p_{2}\dots p_{k}=q_{1}q_{2}\dots q_{k} $$ where $p_{i}=q_{i}$ for $1\leq i\leq k$.  What is the problem with the property we defined above?
1) we assume same length, it should be $q_{s}$
2) n is an arbitrary integer that have fixed number of prime factor, but the $k$ here can be any natural number

There are actually 2 ways to define the statement. 
1) For a fixed number $n$, the first $k$ prime factors match $p_{1}=q_{1},\dots,p_{k}=q_{k}$
2) Any integer that has a total of $k$ prime factor has a unique representation. Exp:

> [!example]
> 
> Let $P(k)$ be the statement below:
> 
> If an integer $n$ has a prime factorization with $k$ prime factors $p_{1},\dots p_{k}$ and also equals $q_{1},\dots,q_{s}$, then $k=s$ and $p_{i}=q_{i}$ for $1\leq i\leq k$.

We are actually using the first one. Let $P(k)$ defined as
$$
P(k):p_{i}=q_{i} \text{ for all }1\leq i\leq k 
$$

For basis step, we already prove $P(1)$ is true in WOP proof.

For induction step, assume $k$ is an arbitrary integer where $k\geq 1$ and $P(k)$ is true. Thus,

$$
\begin{align}
p_{1}\dots p_{k}p_{k+1}&= q_{1}\dots q_{s}
\end{align}
$$
Since $p_{1}=q_{1}$, thus we divide both side by $p_{1}$
$$
p_{2}\dots p_{k}p_{k+1}=q_{2}\dots q_{s}
$$
Notice that they $p_{2}\dots p_{k+1}$ have $k$ terms, this by IHP, it follow that
$$
p_{i}=q_{i}\text{ for }2\leq i\leq k+1
$$
Thus, $P(k+1)$ is true. 

Proof using power notation:
Suppose 
$$
p_{1}^{a_{1}}p_{2}^{a_{2}}\dots p_{k}^{a_{k}}=p_{1}^{b_{1}}p_{2}^{b_{2}}\dots p_{k}^{b_{3}}
$$
where $p_{i}$ is distinct prime number for $1\leq i\leq k$ and $k\in \mathbb{Z}$ where $k\geq 1$ and $p_{1}<p_{2}<\dots<p_{k}$.

Why? suppose $n =ab$ and $n =bc$ (different representation), how to compare them? Notice that $abc^{0}=a^{0}bc$, now we have all the possible prime factor but with different power.

If we can prove that every exponent must match $(a_{i}=b_{i})$, then since $a_{i}\geq 1$ and $b_{i}\geq 1$, they turn out to be the same representation.

Now suppose $a_{i}\geq b_{i}$ for some $1\leq i\leq k$ for the sake of contradiction and we divide both side by $p_{i}^{b_{i}}$. Thus,

$$
\begin{align}
\prod_{n=1}^{k} p_{n}^{a_{n}}&=\prod_{n=1}^{k} p_{n}^{b_{n}} \\
\prod_{n=1,n\neq i}^{k}p_{n}^{a_{n}}\cdot p_{i}^{a_{i}-b_{i}}&=\prod_{n=1,n\neq i}^{k} p_{n}^{b_{n}} 
\end{align}
$$

Since $a_{i}>b_{i}$, it follow that $a_{i}-b_{i}\geq 1$. (To make sure $p_{i}^{a_{i}-b_{i}}\neq 1$). 
Notice that $p_{i}|LHS$. Since $LHS=RHS$, it follow that $p_{i}|RHS$. By Euclid lemma, it follow that $p_{i}|p_{n}$ for some $1\leq n\leq k$ and $n\neq i$. But $p_{1},\dots,p_{k}$ are all distinct primes number, thus $p_{i} \nmid RHS$ which lead to contradiction.

---
### Related Architecture & Vault Links
- **Existence of Factorization:** [[Chapter 5 Sequences and Mathematical Induction#^fta-existence|Chapter 5: Strong Induction Proof]]
- **Master Pipeline:** [[Logical Architecture from WOP to FTA]] — Complete pipeline from WOP, Bézout's Identity, and Euclid's Lemma to FTA Existence & Uniqueness.
- **Divisibility Precursor:** [[Basic number theory proof#^709f3d|Divisibility by a Prime]]

