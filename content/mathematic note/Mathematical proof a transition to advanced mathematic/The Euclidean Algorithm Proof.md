Suppose $a,b \in \mathbb{N}$, if we repeated perform the division algorithms :
$$
\begin{align}
a&=bq_{1}+r_{1} \\
b&=r_{1}q_{2}+r_{2} \\
r_{1}&=r_{2}q_{3}+r_{4} \\
\dots \\ 
r_{n-3}&=r_{n-2}q_{n-1}+r_{n-1} \\
r_{n-2}&=r_{n-1}q_{n}+0
\end{align}
$$
then $r_{n-1}=gcd(a,b)$


==Analysis==
we want to find greatest common divisor of $a,b$. Thus, we take a divide by b to see the left out part which is the remainder. To find the gcd we need to find a factor that divide $a,b,r_{1}$ , thus, we take $b$ divide by $r_{1}$ and find the remainder. We keep on repeat the process until the remainder is 0. 

Notice that it is a chain reaction, $r_{n-1}\mid r_{n-2}$ and $r_{n-1}\mid r_{n-1}$. Thus, it follow that $r_{n-1}\mid r_{n-3}$. It goes on until $r_{n-1}\mid  a$ and $r_{n-1}\mid b$.

In plain word, we want to find $gcd(a,b)$, and we form a equation $a=bc+d$, notice that there are 3 part (a, bc, d), $d$ is the left over that is not divisible by $b$, but what if $d | b$? Then 
since $d|bc$, then $d |b$. 
$$
\begin{align} \\
gcd(a,b)&=gcd(b,r) \\
gcd(b,r)&=gcd(r,r_{1}) \\
\dots \\
gcd(r_{n-2},r_{n-1})&=gcd(r_{n-1},0)
\end{align}
$$



Proof:
First part we need to show that it will reach to an end. 
Notice that the sequence $\{ r_{1},r_{2},r_{3},\dots \}\subseteq \mathbb{N}$. and is decreasing. Thus, by WOP there exist a minimum natural number in the set say $r_{n-1}$.

Second part we need to show that $r_{n-1}\mid a$ and $r_{n-1}\mid b$.
Notice that $r_{n-1}\mid r_{n-2}$ and $r_{n-1}\mid r_{n-1}$. Thus, it follow that $r_{n-1}\mid r_{n-3}$. Thus, by Finite Induction,  $r_{n-1}\mid a$ and $r_{n-1}\mid b$.

Formal using induction:

Let $r_{n-1}$ be the last non-zero remainder. Then $r_{n-1} \mid r_{n-k}$ for all integers $k$ such that $1 \le k \le n+1$.

Let $P(k)$ defined as
$$
P(k): \text{For all k, }r_{n-1}\mid r_{n-k} 
$$

We need to defined what is k. Let k represent how many steps back from the end we are
$k=0$ corresponding to $r_{n}$ (the last remainder, which is 0).
$k=1$ corresponding to $r_{n-1}$ (the GCD candidate).
...
$k=n$ correspond to $r_{0}=b$
$k=n+1$ corresponding to $a$

For basis step $P(1)$ is true because  $r_{n-1} \mid r_{n-1}$. $P(2)$ is true because $r_{n-2}=r_{n-1}q_{n}+0$, thus $r_{n-1}\mid r_{n-2}$.


For inductive hypothesis,
Suppose $j$ is an arbitrary integer. Assume $P(j)$ is true for all $1 \le j \le k$.
This means we assume $r_{n-1}$ divides **both** $r_{n-(k-1)}$ and $r_{n-k}$. We must show $P(k+1)$ is true, i.e., show that $r_{n-1} \mid r_{n-(k+1)}$.

Consider the division algorithm equation involving these terms:

$$r_{n-(k+1)} = r_{n-k} \cdot q_{n-k+1} + r_{n-(k-1)}$$

Rearranging for the term we want ($r_{n-(k+1)}$):
$$r_{n-(k+1)} = r_{n-k} \cdot q + r_{n-(k-1)}$$

- By our inductive hypothesis, $r_{n-1} \mid r_{n-k}$ (so it divides the first term).
    
- By our inductive hypothesis, $r_{n-1} \mid r_{n-(k-1)}$ (so it divides the second term).
    
- Since $r_{n-1}$ divides both terms on the RHS, it must divide the LHS.
    

Therefore, $r_{n-1} \mid r_{n-(k+1)}$.

Thus $P(k+1)$ is true.


==Remark==
Ladder analogy:
We need to climb the ladder until $n+1$, thus in inductive hypothesis we cannot assume $P(j)$ is true for $1\leq j\leq n+1$. (We assume what we need to prove). Since $1\leq k\leq n+1$. Think of $k$ as the step in middle, assume $P(k)$ is true and show that $P(k+1)$ is true, then by mathematical induction we can show that we can reach $n+1$.


Why we need to prove 2 cases in basis step. Because to start the sequence we need the first 2 term because the term is determined by the previous 2 terms. Why?

$$
r_{n-3}=r_{n-2}q_{n-1}+r_{n-1}
$$
Notice that to prove $r_{n-1}\mid r_{n-3}$ we need to show $r_{n-1}\mid r_{n-1}$ and $r_{n-1}\mid r_{n-2}$.

or
$$
r_{n-(k+1)}=r_{n-k}q_{n-(k-1)}+r_{n-(k-1)}
$$

To prove that $r_{n-1}$ divides the term on the left ($r_{n-(k+1)}$), we need to assume it divides **both** terms on the right:

1. It must divide $r_{n-k}$ (the "current" term).
    
2. It must divide $r_{n-(k-1)}$ (the "previous" term).


This is also the reason why we use strong induction


Third part we need to show that $r_{n-1}=gcd(a,b)$. Suppose there exists an natural integer $d$ such that $d\mid a$ and $d\mid b$. (We need to show that $d\mid r_{n-1}$) Thus, it follow that $d\mid (a-bq_{1})$ , thus, $d\mid r_{1}$. Therefore it follow that $d\mid (b-r_{1}q_{2})$ , thus $d\mid r_{2}$ . Thus we repeat the process and $d\mid r_{n-1}$

Formal induction:
Suppose there exists an natural integer $d$ such that $d\mid a$ and $d\mid b$. Let $P(k)$ defined as
$$
P(k):d\mid r_{k}
$$
$-1\leq k\leq n-1$.
$a=r_{-1}$
$b=r_{0}$

For basis step,$P(-1)$ and $P(0)$ are true by assumption. $P(1)$ is true because $d\mid (a-bq_{1})$ which is $d\mid r_{1}$.

For inductive step, suppose $P(j)$ is true for all $1\leq j\leq  k$.

Notice that 
$$
r_{k+1}=r_{k-1}-r_{k}q
$$
By IH $d\mid r_{k}$ and $d\mid r_{k-1}$. Thus, $d\mid r_{k+1}$. Thus, $P(k+1)$ is true. 


==Question==
Is there only one set of solution? No, there have infinitely many solution.

### Dividing the polynomial
Long division and Synthetic division

---
### Related Architecture
- [[Logical Architecture from WOP to FTA]] — Termination by WOP, proof by Strong Induction, and connection to Bézout's Identity.
