$\forall a,b \in \mathbb{Z},\exists x,y \in \mathbb{Z}\,s.t.\,ax+by=gcd(a,b)$

Example $gcd(432,126)=18$

We can obtained this number by using Euclid's Algorithms.

$$
\begin{align}
432&=3(126)+54 \\
126&=2(54)+18 \\
54&=3(18)+0
\end{align}
$$
Thus, $gcd(432,126)=18$

How to find $x$ and $y$ ? Notice that 
$$
\begin{align}
18&=126-2(54) \\
18&=126-2[432-3(126)] \\
18&=126-2(432)+6(126) \\
18&=7(126)-2(432)
\end{align}
$$

Thus $x=-2$ and $y=7$. Is there any other solution?
$$
18=126(7[])+432(-2[])
$$

We need to fill in the blank $[]$ to make the equality true.

What is the LCM for 432 and 126?
Notice that 
$432=18(24)$
$126=18(7)$

Since $7$ and 24 are coprime 
Thus , $LCM(432,126)=18\cdot 24\cdot 7=3024$

Thus,
$$
18=126(7-24m)+432(-2+7m)
$$

Thus, $x=-2+7m$ and $y=7-24m$

How to think of it intuitively?
 $d\mid(ax+by)$ if $d$  divide $ax$ and $d$ divide $by$ , why?

$ax=dm$ for some $m \in \mathbb{Z}$
$by=dn$ for some $n \in \mathbb{Z}$
$ax+by=d(n+m)$. Thus, $d\mid ax+by$

thus it is obvious that the d can be the $gcd(a,b)$.


----
Lets look at Euclid's algorithms, notice that each remainder is linear combination of 2 number. Thus, the gcd which is the last remainder must able to express as linear combination.
$gcd(a,b)=ax+by$. (Bezout's identity) 

The $gcd(a,b)$ is the min($ax+by$), and it is divisible by a and b. (Notice that other remainder is not divisible by $a$ and $b$ but they are multiple of gcd). 

How to prove this?
Use WOP to prove the existence of min($ax+by$), and we prove that this min($ax+by$) divide $a$ and $b$. 

We prove by contradiction. which we suppose it not divide a or b, and at the end we show that the $r$(remainder) is in the set and it is smaller than min($ax+by$).

---
$\forall a,b \in \mathbb{N},\exists x,y \in \mathbb{Z}\,s.t.\,ax+by=gcd(a,b)$
Proof:
Suppose $a,b \in \mathbb{N}$.
Let S defined as 
$$
S=\{ ax+by\mid x,y \in \mathbb{Z} \land ax+by>0 \}
$$
(Why>0, because the linear combination can be negative but in fact we just concern about the positive part)

Notice that for any $a,b \in \mathbb{N}$, $ax+by\in S$ if
$x=1$ and $y=1$. Thus, $S$ is non empty set. Since $S \subseteq \mathbb{N}$, by WOP it follow that there exists a minimum natural number say min(S)=d.
Notice that $d=ax_{0}+by_{0}$
We need to show that $d\mid a$ and $d\mid b$.(it is equal to show if $d=ax_{0}+by_{0}$ then $d\mid a$ and $d\mid b$ which is only true for min(S). For the sake of contradiction, suppose $d\not\mid a$. Thus, by QR Theorem, $a=dq+r$ for some $q \in \mathbb{Z}$ and $0<r<d$.

$$
\begin{align}
dq&=aqx_{0}+bqy_{0} \\
a-r&=aqx_{0}+bqy_{0} \\
r&=(1-qx_{0})a-(qy_{0})b
\end{align}
$$
Thus, it follow that $r \in S$ and $r<d$ which lead to a contradiction. We use the same method to show that $d\mid b$. Thus, $d\mid a$ and $d\mid b$.

We need to show that $gcd(a,b)=d$. Suppose there exist an common divisor for $a$ and $b$ say $d_{1}$. Thus, $d_{1}\mid a$ and $d_{1}\mid b$. Therefore it follow that $d_{1}\mid(ax+by)$ for all $x,y \in \mathbb{Z}$ (simple result from divisibility). Thus, it follow that $d_{1}\mid (ax_{0}+by_{0})$. Thus, $d_{1}\mid d$. Therefore, $gcd(a,b)=d$.

---
### Related Architecture
- [[Logical Architecture from WOP to FTA]] — How Bézout's Identity is derived via WOP / Euclidean Algorithm, and how it proves Euclid's Lemma and FTA.

QR Theorem change not divisibility to algebra while Bezout's identity change coprimality to algebra.  
