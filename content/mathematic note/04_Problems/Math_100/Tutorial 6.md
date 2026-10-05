1)
a) 
$$
\begin{align}
\ 6m(2m+10)=12m^{2}+60m \\
=4(3m^{2}+15m)
\end{align}
$$
$4(3m^{2}+15m)\mid{4}$ iff $3m^{2}+15m$ is integer

b)
$$
\begin{align}
n^{2}-1&=(4k+3)^{2}-1 \\
&=16k^{2}+24k+9-1 \\
&=16k^{2}+24k+8 \\
&=8(2k^{2}+3k+1)
\end{align}
$$
Let $t=2k^{2}+3k+1$ where t is integer because it a sum and product of integer. Thus,
$$
n^{2}-1=8t \text{ for some integer t}
$$

Therefore, by definition of divisibility, $8 \mid n^{2}-1$.

2)

$$\begin{array}
\ n \equiv 3 \text{ (mod 5)} \\
n =5q+3 \text{ for some integer q} \\
n^{2}=(5q+3)^{2} \\
n^{2}=25q^{2}+30q+9 \\
n^{2}=5(5q^{2}+6q+1)+4
\end{array}
$$
Let $t=5q^{2}+6q+1$ where t is an integer because it is a sum and product of integer. Thus,
$$
n^{2}=5t+4 \text{ for some integer t}
$$
Therefore, by definition $n^{2}$mod 5=4

3)
a-b is odd iff 
a is odd and b is even or,
a is even and b is odd

Thus, a and b have opposite parity

b-c is even iff
b and c are even or,
b and c are odd
Thus, b and c have same parity

Thus, a and c have opposite parity. Therefore, a-c is odd.

4)
$\forall n \in \mathbb{Z},6 \mid n  \to 2 \mid n$
Proof:

Suppose $n$ is an arbitrary integer and $6\mid n$. By definition, $n =6k$ for some integer k. Thus,
$$
n =2(3k) \text{ for some integer k}
$$
Let $t=3k$ where t is an integer because it is product of integers. Therefore,
$$
n =2t \text{ for some integer t}
$$
Thus, by definition of divisibility, $2 \mid n$ or n is divisible by 2. Q.E.D

5)
a)
Let $a=3$ and $b=3$.
Thus, by substitution
$$a+b=3+3=6$$
Notice that
$$
6=2(3)
$$

Thus, by definition $3 \mid 6$ 

 By substitution
 $$
a-b=3-3=0
$$
Thus, $3 \not\mid 0$ . 

%%
$\forall a,b\in \mathbb{Z},3 \mid(a+b)\to 3\mid(a-b)$
The negation of it:
$$
\exists a,b\in \mathbb{Z},3 \mid(a+b)\land 3 \not\mid (a-b)
$$
Proof:
Suppose 
%%

b)
Let a=4 and b=6. $4 \mid 36$ and $4\leq{6}$ but $4 \not\mid 6$.
The main idea is find a large number $b^{2}$ so it have many factor that divide $b^{2}$ but not divide b.
%%
i think i can prove by contradiction, to disprove this statement, it means that the negation of it is true and the original statement is false. Thus, we prove by contradiction by assuming the original statement is true.
$\forall a,b\in \mathbb{Z}^{+},(a \mid b^{2}) \land (a\leq b) \to a \mid b$

Suppose a and b are arbitrary positive integer and $a \mid b^{2}$ and $a\leq b$ . Thus, by definition,


$$\begin{array}
\ a\times n =b\times b \text{ for some integer n}\\
\end{array}
$$
Since $a>0$ and $b>0$ , it follow that $n >0$ 

Case 1: $a \mid b$  and $n \not\mid b$
Thus, by definition
$$
b=ak \text{ for some integer k}
$$
Thus, 
$$
\begin{align}
b^{2}&=(ak)^{2} \\
&=a^{2}k^{2} \\
&=a(ak^{2})
\end{align}
$$
Let $n=ak^{2}$ where n is an integer because $n$ is a product of integers. Therefore,
$$
b^{2}=an \text{ for some integer n}
$$
Thus, by definition $a \mid b^{2}$ 

Case 2: $a\not\mid b$ and $n\mid b$
Thus, by definition 
$$
b=ns \text{ for some integer s}
$$
Thus,
$$
\begin{align}
b^{2}&=(ns)^{2} \\
&=n(ns^{2})
\end{align}
$$
Let $a=ns^{2}$ where a is an integer because $a$ is a product of integers. Therefore,
$$
b^{2}=an \text{ for some integer a}
$$
Thus, by definition $a\mid b$ . Thus, $a\mid b$ and $a \not\mid b$ which lead to contradiction.
%%
it is true if the condition change to for all prime


6)
a)
Proof:
Suppose two arbitrary even integer a and b. Thus, by definition $a=2k$ and $b=2r$ for some integer k and r.
By substitution,
$$
\begin{align}
 a\times b&=2k\times 2r \\
&=4(kr)
\end{align}
$$
Let $t=kr$ where t is an integer because it is a sum of integers
Thus,
$$
a\times b=4t \text{ for some integer t}
$$
Therefore, it follow that $4 \mid ab$. Q.E.D.

b)
Proof:
Suppose a, b and c are arbitrary integer such that $a\mid b$ and $a \mid c$.
By definition, $b=ak_{1}$ and $c=ak_{2}$ for some integers $k_{1}$ and $k_{2}$
Thus,
$$
\begin{align}
2b-3c&=2(ak_{1})-3(ak_{2}) \\
&=a(2k_{1}-3k_{2})
\end{align}
$$
Let $t=2k_{1}-3k_{2}$ where t is an integer because it is a sum and product of integers. Thus,
$$
2b-3c=a\times t \text{ for some integer t}
$$
Therefore, by definition, $a \mid (2b-3c)$. Q.E.D

7)
Suppose  a and b are arbitrary integer and $ab \mid c$. Thus, by definition
$$
c=abk \text{ for some integer k}
$$
Thus, by associative law
$$
c=a(bk) \text{ and } c=b(ak)
$$
Let $t=bk$ and $r=ak$ where t and r are integer because t and r are product of integers. 
Thus, by substitution
$$
c=at \text{ and } c=br \text{ for some integer t and r}
$$
Thus, by definition $a\mid c$ and $b\mid c$


8)
$$
\forall a,b,c \in \mathbb{Z}, a\mid bc \to a \mid b \text{ or }  a\mid c
$$
Suppose a, b and c are arbitrary integers and $a\mid bc$. Thus,
by definition 
$$
\begin{align}
bc=ak \text{ for some integer k} \\
b=a\left( \frac{k}{c} \right) \text{ and } c=a\left( \frac{k}{b} \right)
\end{align}
$$
When $k<c$ and $k<b$ , $\dfrac{k}{c}$  and $\dfrac{k}{b}$is not an integer

Let $a=6$ and $b=2$ and $c=3$ and $bc=6$
Thus, $6 \mid 6$ but $6\not \mid 3$ and $6 \not\mid 2$. (Note this is true for all prime a which is Euclid Lemma)


9)
a)
Proof:
Suppose an arbitrary integer n. Thus, $n,n+1,n+2$ are 3 consecutive integers. By quotient remainder theorem, $n =3k+r$ where $r\in \{ 0,1,2 \}$

Case1: **$n = 3k$+0**
Since $3k$ is a multiple of 3, **$n$ is divisible by 3.**

Case 2: $n =3k+1$
$n+1=3k+2$ , thus $(n+1) \not\mid 3$
$n+2=3k+3$, thus  $n+2=3(k+1)$ , thus $(n+2)\mid 3$

Case 3: $n =3k+2$
$n+1=3k+3$, thus $n+1=3(k+1)$ , thus $(n+1)\mid 3$

Since Case 1,2 and 3 cover all the possibility. We can conclude that three consecutive integers, one of them is divisible by 3.





b)
Suppose an arbitrary integer n. Let
$$P = n \times (n+1) \times (n+2)$$
Since, three consecutive integers, one of them is divisible by 3, it follow that,
- Case 1 ($3\mid n$ ):
$$\begin{align}
P &= (3k)(n+1)(n+2)  \text{ for some integer k}\\
&= 3[k(n+1)(n+2)]
\end{align}
$$
Thus, $3 \mid P$

- Case 2 ( $3 \mid n+1$ ):
$$\begin{align}
P &= n(3k)(n+2)  \text{ for some integer k}\\
&= 3[nk(n+2)]
\end{align}
$$
Thus, $3 \mid P$

- Case C ($3 \mid n+2$ ):
$$
\begin{align}
P &= n(n+1)(3k)  \text{ for some integer k} \\
&= 3[n(n+1)k]
\end{align}
$$
Thus, $3\mid P$


10)
$$
3^{5}\cdot 5^{3} \cdot
$$
$m=3,$

11)
a)
$a^{2}=p_{1}^{2e_{1}} \cdot p_{2}^{2e_{2}}\cdot\dots \cdot p_{k}^{2e_{k}}$
b)
