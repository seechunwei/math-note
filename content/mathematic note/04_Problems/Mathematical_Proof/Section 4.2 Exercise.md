==4.14==
Proof:
Suppose $a\equiv b \pmod n$. Thus, $a-b=nk$ for some $n \in \mathbb{Z}$. $a=b+nk$

$$
\begin{align}
a^{2}&=b^{2}+2bnk+n^{2}k^{2} \\
a^{2}-b^{2}&=n(2bk+nk^{2})
\end{align}
$$
Since $2bk+nk^{2}$ is an integer it follow that $n\mid (a^{2}-b^{2})$. Thus, $a^{2}\equiv b^{2} \pmod n$ Q.E.D

==4.15==
Proof:
Suppose $a\equiv b \pmod n$ and $a\equiv c \pmod n$.
$a-b=nx$ and $a-c=ny$ for some $x,y \in \mathbb{Z}$.
Then,$a=b+nx$ and $a=c+ny$.

Thus,
$$
\begin{align}
b+nx&=c+ny \\
b-c&=ny-nx \\
&=n(y-x)
\end{align}
$$
Since $y-x$ is an integer, it follow that $b\equiv c \pmod n$

4.16
Proof:
Suppose $a\equiv 0 \pmod 3$ and $b\equiv 0 \pmod 3$ (1) or $a,b\not\equiv 0 \pmod 3$ (2)

Case 1: $a\equiv 0 \pmod 3$ and $b\equiv 0 \pmod 3$
Thus, $a^{2}\equiv 0 \pmod 3$ and $b^{2}\equiv 0 \pmod 3$.
Thus,
$$
\begin{align}
a^{2}+2b^{2}\equiv 0 \pmod  3
\end{align}
$$
Case 2: $a,b \not\equiv 0 \pmod 3$
Thus $a,b$ is congruence to the element of $\{ 1,2 \}$.

Considering cases up to sign the quadratic residue modulo 3 is 1.
Thus,

$$
\begin{align}
a^{2}+2b^{2}&\equiv 1+2(1) \pmod  3 \\
&\equiv0 \pmod  3
\end{align}
$$
In either case $a^{2}+2b^{2}\equiv 0 \pmod 3$.

Conversely, suppose one of them congruence to 0 modulo 3 and one of them 
congruence to $\{ 1,2 \}$ modulo 3. If $x\equiv 0 \pmod 3$, then $x^{2} \equiv 0 \pmod 3$ while if $x \not\equiv 0 \pmod 3$ , then $x^{2}\equiv 1 \pmod 3$. Thus, 

Case 1: $a\equiv 0 \pmod 3$ and $b \not \equiv 0 \pmod 3$
$$
\begin{align}
a^{2}+2b^{2}&\equiv 0^{2}+2(1) \pmod  3 \\
&\equiv 2 \not\equiv 0 \pmod  3
\end{align}
$$
Thus, $a^{2}+2b^{2}\not\equiv 0 \pmod 3$

Case 2: $a\not\equiv 0 \pmod 3$ and $b\equiv 0 \pmod 3$
$$
\begin{align}
a^{2}+2b^{2}&\equiv (1)^{2}+2(0)^{2} \pmod  3 \\
&\equiv 1 \pmod  3
\end{align}
$$
Thus, $a^{2}+2b^{2} \not\equiv 0 \pmod 3$

In either case, $a^{2}+2b^{2}\not\equiv 0 \pmod 3$.

4.17
a)
Proof:
Suppose $a\equiv 1 \pmod 5$, thus $a-1=5k$ for some $k \in \mathbb{Z}$. Thus, $a=1+5k$. Hence,

$$
\begin{align}
a^{2}&=1^{2}+10k+25k^{2} \\
a^{2}-1^{2}&=5(2k+5k^{2})
\end{align}
$$
$a^{2}\equiv 1 \pmod 5$.Q.E.D


==4.18==^111
Proof:
Suppose $m\mid n$ and $a\equiv b \pmod n$ Thus, $n =mx$ and $a-b= ny$ for some $x,y \in \mathbb{Z}$. Hence, ^6e3b97

$$
\begin{align}
a-b=m(xy)
\end{align}
$$
Since $xy$ is an integer it follow that $a\equiv b \pmod m$.

4.19
Proof:
Suppose $a\equiv 5 \pmod 6$ and $b\equiv 3 \pmod 4$, . Thus, $a=5+6x$ and $b=3+4y$ for some $x,y \in \mathbb{Z}$. Hence,

$$
\begin{align}
4a+6b&=4(5+6x)+6(3+4y) \\
&=20+24x+18+24y \\
&=38+24x+24y \\
&=6+8(4+3x+3y)
\end{align}
$$
Since $4+3x+3y$ is an integer , thus it follow that $4a+6b\equiv 6 \pmod 8$

Prove using modulo arithmetic using result 
4.18
Proof:
Suppose $a\equiv 5 \pmod 6$

$$
\begin{align}
4a\equiv 20 \pmod {24}
\end{align}
$$
By result 4.18, since $8\mid 24$ and $4a\equiv 20 \pmod{24}$. it follow that $4a\equiv 20 \pmod{ 8}$. Thus,
$$
\begin{align}
4a\equiv 4 \pmod{ 8} \\ 
\end{align}
$$

Suppose $b\equiv 3 \pmod{4}$
Thus,
$$
\begin{align}
6b\equiv 18 \pmod{ 24} \\
6b\equiv 18 \pmod{ 8} \\
6b\equiv  2 \pmod{ 8}   
\end{align}
$$
Thus,
$$
4a+6b\equiv 6 \pmod{ 8} 
$$
Q.E.D

==Remark==
Why this can happen ?
Notice that $a\equiv 5 \pmod{ 6}$. That mean if we multiply the whole statement it become $4a=20+4(6)(nx)$ Since $(4)(6)=24$ and $8\mid 24$, we can just factor out 8. 

4.21
Proof: 
Case 1: $a \equiv 0 \pmod{ 3}$
$$
\begin{align}
a^{3}\equiv 0^{3}\equiv 0\equiv a \pmod{3} 
\end{align}
$$
Thus, $a^{3}\equiv a \pmod{3}$

Case 2: $a\equiv 1 \pmod{ 3}$
$$
\begin{align}
a^{3}\equiv 1^{3}\equiv 1\equiv a  \pmod{ 3} 
\end{align}
$$
Thus, $a^{3}\equiv a \pmod{ 3}$

Case 3: $a\equiv 2 \pmod{3}$
$$
\begin{align}
a^{3}\equiv 8\equiv 2 \equiv a \pmod{3} 
\end{align}
$$
Thus, $a^{3}\equiv a \pmod{3}$.

In either case $a^{3}\equiv a \pmod{ 3}$.

==Remark==
Notice that $a^{3}-a=a(a-1)(a+1)$ which is three consecutive integer.

4.23
$a\equiv 0 \pmod{ 6}$ even
$a+1\equiv 1 \pmod{ 6}$  $a+1\equiv 1 \pmod{2}$
$a+2\equiv 2 \pmod{6}$ even
$a+3\equiv 3 \pmod{ 6}$ odd
$a+4\equiv 4 \pmod{ 6}$ even
$a+5\equiv 5 \pmod{ 6}$ odd

Let us denote the set of these odd integers as $O$:

$$O = \{a+1, a+3, a+5\}$$

Notice that since $24 = 3 \times 8$ and $\gcd(3, 8) = 1$ , thus, $24\mid(x^{2}-y^{2})$ can be shown by
1) $8\mid(x^{2}-y^{2})$
2) $3\mid(x^{2}-y^{2})$

Since $x$ and $y$ are odd, it follow that $8\mid(x^{2}-1)$ and $8\mid(y^{2}-1)$
$$
\begin{align}
8\mid[(1)(x^{2}-1)+(-1)(y^{2}-1)] \\
8\mid(x^{2}-y^{2})
\end{align}
$$
We determine $k^2 \pmod 3$ for each odd integer $k \in O$. Since $3\mid 6$ , it follow that 

Case 1: $k=a+1$
$a+1\equiv 1 \pmod{ 3}$ $\implies$ $(a+1)^{2}\equiv 1 \pmod{ 3}$

Case 2: $k=a+3$
$a+3\equiv 3\equiv 0 \pmod{ 3}$ $\implies$ $(a+3)^{2}\equiv 0 \pmod{ 3}$

Case 3: $k=a+5$
$a+5\equiv 2 \equiv-1 \pmod{3}$  $\implies$$(a+5)^{2}\equiv 1 \pmod{ 3}$


Notice that $3 \mid(x^{2}-y^{2})$ is true iff one of $x$ and $y$ is congruent to 1 modulo 6 while the other is congruent to 5 modulo 6.

herefore, $x^2 - y^2 \equiv 0 \pmod 3$ if and only if we choose the pair $\{a+1, a+5\}$.

- If we choose $\{a+1, a+3\}$, residues are $1$ and $0 \implies 1 - 0 \neq 0$.
    
- If we choose $\{a+3, a+5\}$, residues are $0$ and $1 \implies 0 - 1 \neq 0$.
    
- If we choose $\{a+1, a+5\}$, residues are $1$ and $1 \implies 1 - 1 = 0$.
    

Thus, $24 \mid (x^2 - y^2)$ if and only if $x$ and $y$ correspond to the elements $a+1$ and $a+5$. As established at the start, these are precisely the integers congruent to **1** and **5** modulo 6.

