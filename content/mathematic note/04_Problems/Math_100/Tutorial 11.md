1)
$S_{2}=\{ (a,b),(a,c),(b,c) \}$. Yes because  $S_{0}\cup S_{1}\cup S_{2}\cup S_{3}=P(S)$ and $S_{i}$ are mutually disjoint

2)
a) 
$S_{1}=\{ \emptyset,\{  b\},\{ c \},\{ d \},\{ b,c \},\{ b,d \},\{ c,d \},\{ b,c,d \} \}$

$S_{2}=\{ \{ a \},\{ a,b \},\dots ,\{ a,b,c,d \}\}$

b) $|S_{1}|=|S_{2}|$

c) Yes

3)
$$
\begin{align}
(A-B)\cap(C-B)&=(A\cap B^{c})\cap(C\cap B^{c}) \text{ (by set diffrence law)}\\ 
&=B^{c}\cap(A\cap C) \text{ (by distributive law)} \\
&=(A\cap C)\cap B^{c} \text{ (by comutative law)} \\
&=(A\cap C)-B \text{ (by set difference law)}
\end{align}
$$

4)
We argue by contradiction. Suppose not which is if $A\cap C=\emptyset$ then $(A\times B)\cap(C\times D)\neq \emptyset$.

We suppose $(x,y)$ is an arbitrary element in $(A\times B)$ and $(x_{0},y_{0})$ is an arbitrary element in $(C\times D)$. Thus, $x \in A$ and $x_{0} \in C$. Since, $(A\times B)\cap(C\times D)\neq \emptyset$. 
Thus, there exists an element $x_{1} \in A\cap C$  which contradict the supposition $A\cap C=\emptyset$. Q.E.D

5)
Proof:
Suppose $A,B$ are arbitrary set. 
Part 1
Suppose $x$ is an arbitrary element in $P(A\cap B)$. By definition, $x \subseteq A\cap B$ . Thus, $x \subseteq A$ and $x\subseteq B$. BY definition $x \in P(A)$ and $x \in P(B)$. Thus $x \in P(A) \cap P(B)$.
Thus, $P(A\cap B)\subseteq P(A)\cap P(B)$.

Part 2
Suppose $x$ is an arbitrary element in $P(A)\cap P(B)$. Thus, $x \in P(A)$ and $x \in P(B)$. By definition, $x \subseteq A$ and $x \subseteq B$. Thus, $x\subseteq A\cap B$. By definition, $x \in P(A\cap B)$. Hence, $P(A)\cap P(B)\subseteq P(A\cap B)$.

Since, $P(A\cap B)\subseteq P(A)\cap P(B)$ and $P(A)\cap P(B)\subseteq P(A\cap B)$. Thus, $P(A\cap B)=P(A)\cap P(B)$

6)
Proof:
$$
\begin{align}
A-(A-B)&=A\cap(A\cap B^{c})^{c} \text{ (by set difference law)} \\
&= A\cap(A^{c}\cup B) \text{ (by De Morgan Law)} \\
&=(A\cap A^{c})\cup(A\cap B) \text{ (by distributive law)} \\
&= \emptyset \cup(A\cap B) \text{ (by complement law)} \\
&=A\cap B \text{ (by identity law)}
\end{align}
$$

7)
a)
$$
\begin{align}
A\cap((B\cup A^{c})\cap B^{c})&=A\cap((B^{c}\cap B)\cup(B^{c}\cap A^{c})) \text{ (distributive law)}\\
&=A\cap(\emptyset \cup(B^{c}\cap A^{c})) \text{ (idempotent law)}\\
&=A\cap(B^{c}\cap A^{c}) \text{ (identity law)} \\
&= (A\cap A^{c})\cap B^{c} \text{ (associative law)} \\
&=\emptyset \cap B^{c} \text{ (idempotent law)} \\
&=B^{c} \text{ (identity law)}
\end{align}
$$

b)
$$
\begin{align}
(A-(A\cap B))\cap(B-(A\cap B))&=(A\cap(A\cap B)^{c})\cap(B\cap(A\cap B)^{c}) \text{ (set difference law)}\\
&=(A\cap(A^{c}\cup B^{c}))\cap(B\cap(A^{c}\cup B^{c})) \text{ (De Morgan Law)}\\
&=((A\cap A^{c})\cup (A\cap B^{c}))\cap ((B\cap A^{c})\cup(B\cap B^{c})) \text{ (Distributive law)} \\
&=(\emptyset \cup(A\cap B^{c}))\cap((B\cap A^{c})\cup \emptyset) \text{ (idempotent law)} \\
&=(A\cap B^{c})\cap(A^{c}\cap B) \text{ (identity law)} \\
&= (A\cap B^{c}) \text{ (identity law)}
\end{align}
$$

8)
Suppose $C=\{ 1 \}$ and $A=\{ 1,2 \}$, $B=\{ 2 \}$
$A-(B-C)=\{  1\}$
$(A-B)-C=\{  \emptyset\}$ 
Thus, $A-(B-C)\neq(A-B)-C$

How to construct general counter exmaple?
Method 1: 
![[Untitled.png]]
We do some analysis based on vein diagram. And we can found some general counter example:

1)
![[tutorial 11.png]]
Let $A=B \cup C$, $B$ and $C$ nonempty, $B\cap C=\emptyset$, then $A-(B-C)=A-B=C$ ,
but $(A-B)-C=C-C=\emptyset$

Since $C \neq \emptyset$, we have $A-(B-C)\neq(A-B)-C$. Counterexamples :
Let $B=\mathbb{Q}, C=\mathbb{Q}^{c}$, $A=\mathbb{Q}\cup \mathbb{Q}^{c}=\mathbb{R}$.
Let $B=2\mathbb{Z}$ , $C=2\mathbb{Z}+1$ , $A=\mathbb{Z}$ 

Method 2:
![[tutorial 11 2.png]]

==Lemma==: $X=Y$ iff $X-Y=\emptyset$ and $Y-X=\emptyset$ 
Consider $A,B,C \neq \emptyset$
Then $A-(B-C)-[(A-B)-C]=C \neq \emptyset$
By above lemma $A-(B-C)\neq(A-B)-C$

Counter example: $A=\mathbb{R}$ $B=\mathbb{Q}$ $C=\mathbb{Z}$.


9)
Suppose  $A=\{ 1,2,3,4\}$ and $B=\{ 1,2 \}$ and $C=\{ 2,3 \}$

$B\cap C\subseteq A$ and $(A-B)\cap(A-C)=\{ 4 \}\neq \emptyset$


General counter example:
![[tutorial 11 3.png]]






