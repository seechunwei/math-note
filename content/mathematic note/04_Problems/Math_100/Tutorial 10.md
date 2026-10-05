1)
a) $A\cup B=(0,4)$
b) $B\cap C=[3,4)$
c) $A^{c}=(-\infty,0]\cup(2,\infty)$
d) $A\cap C^{c}=(0,2]$
e) $B\setminus A=(2,4)$

2)
a) No. Let $i=0$, $|A_{i}|=1$

b) 
$\bigcup_{i=0}^{3}A_{i}=\{ 0,-1,-2,-3,1,2,3 \}$ 

$\bigcap_{i=0}^{3}A_{i}=\emptyset$

c) yes
d) $\mathbb{Z}=\{ \dots,-2,-1,0,1,2,\dots \}$

e) Is the set of integer

3)
a)
Yes, because $E$ and $O$ is mutually disjoint and $E\cup O=\mathbb{Z}$

b)
$\{ 1 \}$ because 1 is not prime and not composite number.

4)
Proof:
Suppose $x$ in an arbitrary element in $A$ and $A\subseteq B$. Suppose $x$ is in $A \cap C$, it follow that $x \in A$ and $x \in C$. Since $A\subseteq B$, it follow that $x \in B$.

Thus, combine the result, we know that $x \in C$ and $x \in B$. Thus, $x \in B\cap C$.

Since we chose $x$ arbitrarily from $A \cap C$ and showed it must exist in $B \cap C$ with the assumption of $A\subseteq B$, we have proven that $A \cap C \subseteq B \cap C$.

5)
Proof:
Suppose $x$ is an arbitrary element in $A$ and $A\subseteq B$. Thus, if $x \in A$ , then $x \in B$. Suppose $x \in B^{c}$, thus $x\not\in B$ ,
by Modus Tollens, $x \not\in A$. Since $x$ is an arbitrary element, the statement is true for all element in $A$. Q.E.D

6)
Proof:
Suppose $x$ is an arbitrary element in $A$ and suppose $A\subseteq B$ and $A\subseteq C$. Thus, if $x$ is in $A$ , then $x$ is in $A$ and $x$ is in $C$. Thus, if $x \in A$ then $x \in A\cap B$. It follow that, $A\subseteq A\cap B$. Since $x$ is an arbitrary element, the statement is true for all element in $A$. Q.E.D

7)
a)
Proof:
Suppose $x$ is an arbitrary element in $A$. Thus,
$$
x \in \mathbb{Z} \text{ such that }x=6k^{2}-5 \text{ for some positive integer k}
$$
 By QR Theorem, there exists a unique integer $q$ and unique integer r such that $k=3q+r$ for $0\leq r<3$.
 By definition of Modulo, we can conclude that 
 $k\equiv r \text{ (mod 3)}$ for $0\leq r<3$.
Since $k>0$, thus $x>0$. It follow that $q\geq0$

Case 1: $x=3q$
$$
\begin{align}
x&=6(3q)^{2}-5 \\
&=6(9q^{2})-5 \\
&=3(18q^{2})-2
\end{align}
$$
Thus,
$$
\begin{align}
x&\equiv-2 \text{ (mod 3)} \\
x&\equiv 1  \text{ (mod 3)}
\end{align}
$$

----
Suppose $x$ is an arbitrary element in $A$. Thus,
$$
x \in \mathbb{Z} \text{ such that }x=6k^{2}-5 \text{ for some positive integer k}
$$
Thus, 
$$
x=3(2k^{2}-2)+1
$$
Notice that $k\geq 1$, Thus, 
$$
\begin{align}
k^{2}&\geq 1 \\
2k^{2}&\geq 2 \\
2k^{2}-2&\geq 0
\end{align}
$$
Since, $2k^{2}-2$ is nonnegative integer $k$, it follow that $x \in B$. Thus, $A\subseteq B$

b)
We need to disprove that $B\subseteq A$.  Why? Notice that set the $k^{2}$ in set A will be the key things.

There exists an element in $B$ that is not in $A$. Let $x=4$
Why? it is because 4 is the smallest element in $B$ and consider the set of A
$$
A=\{ 1,19,\dots \}
$$
Clearly there exists an element between 1 and 19 that is in the form of $1+3k$ . For example, 4,7,10,13,16

Thus, $4 \in B$ and $4 \not\in A$. Q.E.D

8)
a)
Proof:
Part one:
We need to show $A\subseteq B$
Suppose $x$ is an arbitrary element in $A$. Thus, $x=3k-2$ for some even positive integer $k$.
By definition, $k=2a$ for some integer $a$, Since $k\geq 2$ , it follow that $a\geq1$

Thus,
$$
\begin{align}
x&=3(2a)-2 \\
&=6a-2 \\
&=1+6a-3 \\
&=1+3(2a-1) \\
&=1-3(1-2a)
\end{align}
$$

Since $a\geq 1$, it follow that $2a$ is an even integer which $2a\geq 2$ Thus, $-2a\leq -2$ 
$1-2a\leq -1$ is an odd negative integer because $1-2a$ and $-2a$ are consecutive integer, since $-2a$ is negative even integer it follow that $1-2a$ is odd negative integer. Thus, $x \in B$, hence, $A\subseteq B$. Q.E.D

Part 2
We need to show that $B\subseteq A$
Suppose $x$ is an arbitrary element in $B$. Thus, $x=1-3k$ for some odd negative integer $k$.
By definition, $k=2b+1$ for some integer b. Since $k\leq -1$, it follow that $b\leq-1$.

Thus,
$$
\begin{align}
x&=1-3(2b+1) \\
&=1-6b-3 \\
&=-6b-2 \\
&=3(-2b)-2
\end{align}
$$

Since $b\leq-1$ , it follow that $-2b\geq 2$ for which $-2b$ is even positive integer. Thus, $x \in A$ hence $B\subseteq A$. Q.E.D

9)
a) $B\subseteq A$
Suppose $x$ is an arbitrary element in $B$. Thus, $x<3$ and $x>1$ .Hence , $(x-3)< 0$ and $(x-1)> 0$. Thus, $(x-3)(x-1)< 0$ which is $x^{2}-4x+3<0$.

Thus, $x \in A$, it follow that $B\subseteq A$.

b)
We need to show that $A\subseteq B$. 
We argue by contraposition which is we need to show $B^{c}\subseteq A^{c}$. Suppose $x$ is an element in $B^{c}$ which is $x\geq3$ or $x\leq1$ . We need to show that $x \in A^{c}$ which is $x^{2}-4x+3\geq 0$.

Case 1 $x\geq 3$
Thus, $(x-3)\geq 0$ and $(x-1)\geq 0$. Thus, $(x-3)(x-1)\geq 0$ which is $x^{2}-4x+3\geq 0$. Thus, $x \in A^{c}$

Case 2 $x\leq 1$
Thus, $(x-3)\leq 0$ and $(x-1)\leq 0$. Thus, $(x-3)(x-1)\geq 0$ which is $x^{2}-4x+3\geq 0$. Thus, $x \in A^{c}$.

In either case $x \in A^{c}$. Thus, we can conclude that $B^{c}\subseteq A^{c}$ which implies that $A\subseteq B$.

c)

10)
i) False
ii) 
iii) True
iv) True

b)
$A_{m}=\left[ 1,1+\frac{1}{i} \right]$
$A_{1}=\{ 1 \}$

11)
a)

