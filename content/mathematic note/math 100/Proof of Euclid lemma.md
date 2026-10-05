Suppose $p$ is prime , $\forall a,b \in \mathbb{N}$, if $p\mid ab$ then $p\mid a$ or $p\mid b$.

Proof:
Suppose $p\not\mid a$ , we need to show that $p\mid b$. Since $p$ is prime and $p\neq a$, it follow that $gcd(p,a)=1$. Thus, by bezout identity, $\exists x,y \in \mathbb{Z}$ such that $px+ay=1$.

Since $p\mid ab$, it follow that $ab=pd$ for some $d \in \mathbb{Z}$. Thus,

$$
\begin{align}
b(px+ay)&=b \\
bpx+aby&=b \\
bpx+pdy&=b \\
p(bx+dy)&=b
\end{align}
$$
Since $bx+dy \in \mathbb{Z}$, it follow that $p\mid b$. Q.E.D.

==Remark==
Bezout's identity translate the coprimality to algebra. Thus, it tell us about what happen of p in one side (a or b) 

## Lemma 2 
The general version of Lemma 1

If $p\mid a_{1}\dots a_{n}$, then $p\mid a_{i}$ for some $1\leq i\leq n$ ($p$ is prime)

Proof:
We argue by mathematical induction. Let $P(n)$ defined as

$$
P(n): \text{the statement above}
$$
where $n \in \mathbb{N}$.

For basis step $P(1)$ is true and $P(2)$ is true because by Lemma 1 if $p\mid a_{1}a_{2}$, then $p\mid a_{1}$
or $p\mid a_{2}$.

For inductive step, suppose $P(n)$ is true for all $n \in \mathbb{N}$. Thus,

$$
\begin{align}
p\mid a_{1}a_{2}\dots a_{n+1}&=p\mid (a_{1}a_{2}\dots a_{n})(a_{n+1})
\end{align}
$$

By Lemma 1 we know that $p\mid a_{1}a_{2}\dots a_{n}$ or $p\mid a_{n+1}$. By IH, it follow that $p\mid a_{i}$ for $1\leq i\leq n$. Thus, it follow that $p\mid a_{i}$ for $1\leq i\leq n+1$.

Thus, $P(n+1)$ is true, by principle of induction, it follow that $P(n)$ is true for all $n \in \mathbb{N}$.

---
### Related Architecture
- [[Logical Architecture from WOP to FTA]] — Complete pipeline from WOP and Bézout's Identity to Euclid's Lemma and the uniqueness of FTA.