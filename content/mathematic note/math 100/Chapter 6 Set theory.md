What is universal set 
Universal set is the set containing all the object and of which All other set are subset of it. (Under certain context)


Suppose A and B are subsets of universal set U.
Elementary Set Operation
$A \cup B=\{x \in U \mid  x \in A  \text{ or }x \in B \}$

$A \cap B= \{ x \in U \mid x \in A \text{ and } x \in B \}$

$A\setminus B=\{ x \in U \mid x \in A \text{ and }x \not\in B \}$ (A delete B)

$A^{c}=\{  x \in U \mid x \not\in A \}$
$\bar{A}=U-A=\{ x: x \in U \text{ and }x \not\in A\}$

The set operation can be defined by the logical operation.


Notation for interval of Real number

Noticed that $(a,b)=\{  x \in \mathbb{R} \mid a<x<b \}$ is a infinite set because it contain infinitely many element and it does not have the least element 

$A=(-1,0]$ and $B=[0,1)$

$A \cup B=(-1,1)$
$A \cap B= \{ 0 \}$
$B \\\setminus A=(0,1)$

Notice that $B \setminus A=B\cap(A\cap B)^{c}$

Power set
Suppose $A$ is a set. The power set of $A$, denoted $P(A)$ , is the set of all subset of $A$.

Example: $A=\{ 0,2,4 \}$
$P(A)=P(\{ 0,2,4 \})$
$P(A)=\{\emptyset, \{ 0 \},\{ 2 \},\{ 4 \},\{ 0,2 \},\{ 0,4 \},\{ 2,4 \},\{ 0,2,4 \} \}$

$|A|=3$ Thus, $|P(A)|=2^{|A|}=8$

==Theorem==
Suppose E is a set with no elements and A is any set. Then $E\subseteq A$.

### 1. Direct Proof (Vacuous Truth)

The formal definition of a subset is as follows:

$$X \subseteq Y \iff \forall x, (x \in X \implies x \in Y)$$

To prove $E \subseteq A$, we must show that the statement **"If $x \in E$, then $x \in A$"** is true for every possible $x$.

- By definition, the empty set $E$ has **no elements**.
    
- Therefore, the statement "$x \in E$" is **always false**, regardless of what $x$ is.
    
- In logic, a conditional statement ($P \implies Q$) is considered **true** whenever the antecedent ($P$) is false. This is known as a **vacuous truth**.
    
- Since the premise "$x \in E$" is never met, the implication "$x \in E \implies x \in A$" is true for all $x$.

Why the contradiction proof valid because it is a existential statement, for a existential statement to be true, there must first exist one element, then only we check the condition.


==Uniqueness of the empty set==
There is a unique set with no elements.

==Disjoint==
Two sets A and B are disjoint iff they have no elements in common, that is, $A\cap B=\emptyset$

==Mutually Disjoint==
A finite collection of sets $A_{1},A_{2},A_{3},\dots,A_{n}$ is said to be mutually disjoint iff for all $i,j \in \{ 1,2,3,\dots,n \}$
$$
A_{i}\cap A_{j}=\emptyset \text{ where }i\neq j
$$
==Partition==
Suppose A is a set. A collection of nonempty sets {A1,A2,A3,...,An} is a partition of A iff

$$\bigcup_{i}^{n} A_i = A$$
and

the sets A1,A2,A3,...,An are mutually disjoint.

A partition $S$ of $A$ is a collection of non empty subsets of $A$ such that each element in $A$ belong to exactly one subset in $S$.

A partition of A can be defined as a collection S of subsets of A satisfying the three properties:
1) $X \neq \emptyset$ for all $X \in S$
2) for every two set $X,Y \in S$, either $X=Y$ or $X\cap Y=\emptyset$
3) $\bigcup_{X \in S}X=A$

Let $A=\{ 1,2,3,4,5,6 \}$
$S=\{ \{ 1,2,3 \},\{ 4,5 \},\{ 6 \} \}$
$A$ is said to be partitioned into 3 set which is $\{ 1,2,3 \}$, $\{ 4,5 \},\{ 6 \}$
Thus, $|S|=3$

What is the subset $T$ of the partition $S$ such that $|T|=2$
$T=\{ \{ 1,2,3 \},\{ 6 \} \}$

What is the element $B$ in the partition $S$  such that $|B|=2$
$\therefore B=\{ 4,5 \}$

Element in the partition $S$ is a subsets of $A$ while the subset of $S$ is the collection of subsets of $A$.

How about the partition of partition of $A$?
Use the example above and let $S_{2}$ denoted as the partition of $S$
Thus, $S_{2}=\{ \{ \{ 1,2,3 \},\{ 4,5 \} \},\{ 6 \} \}$
Thus, notice that $|S_{2}|<|S|<|A|$
(Exercise 1.54)

A set that containing the set itself is a partition of the set itself. Example
$S_{3}=\{ A \}$ is a partition of $A$ because $A\subseteq A$.
### Subset and the Element Method of Proof
==Definition Subset==
$$
A\subseteq B \iff \forall x, x \in A\implies x \in B
$$

Proper subset
$$
A \subset B \iff \forall x, x \in A\implies x \in B \land A\neq B
$$

[Element Method of Proof] Suppose A and B are sets. To prove that A is a subset of B, we suppose x is an arbitrary element of A and then we show that x is an element of B

Element method of prove is similar to the prove of universal biconditional statement. 

==Example==
![[Pasted image 20260104122747.png]]

Equality Between Sets
Two sets A and B are equal if and only if A ⊆ B and B ⊆ A. (It is like a biconditional statement ,we need prove with 2 direction)

![[Pasted image 20260104123026.png]]

Indexed Collection of Sets
$$
\{ A_{i} \}_{i\in I}=\{ A_{1},A_{2},A_{3},\dots \}
$$
if $I$ is the set of $\mathbb{Z}$
$\{ A_{1},A_{2},A_{3},\dots \}$ is an indexed collection of sets, where $A_{i}$ are sets for $i=1,2,3,\dots$

![[Pasted image 20260104135833.png]]

Notice that $\cup$ is for some and $\cap$ is for all.

Nested set. (assignment 3)

### What if the index set is different but the union is still same?

$A=\{ a,b,c,d, \dots z \}$. Let $\alpha \in A$ and $A_{a}=\{ a,b,c \}$, $A_{b}=\{ b,c,d \}$
Therefore, $\bigcup_{\alpha \in A}A_{\alpha}=A$

What if we change the index set to be
$$
B=\{ a,d,g,j,m,p,s,v,y \}
$$
Then $\bigcup_{\alpha \in B}A_{\alpha}=A$

### Different way of writing the collection of set
Let $I=\{ 1,2,3 \}$ and $J=\{ S_{1},S_{2},S_{3} \}$
$$
S=S_{1}\cup S_{2}\cup S_{3}=\bigcup_{i \in I}S_{i}=\bigcup_{i=1}^{3}S_{i}=\bigcup_{X \in J}X
$$

### We use the logical operation to represent the set definition. (Characterization) 

![[Pasted image 20260104140438.png]]

==Theorem==
Suppose $A$ and $B$ are sets. Then,
$$
\begin{array}
\ A \cap B\subseteq A \\
A\subseteq A\cup B
\end{array}
$$

Proof of 1:
Suppose $x$ is an arbitrary element in $A\cap B$. Thus, $x \in A$ and $x \in B$. Thus, $x \in A$.
Therefore, $A\cap B\subseteq A$

Proof of 2:
Suppose $x$ is an arbitrary element in $A$. Thus, by generalization  $x \in A$ or $x \in B$. Thus, $x \in A\cup B$. Therefore, $A\subseteq A\cup B$.

==Transitivity==
Suppose A, B, and C are sets. Then if A ⊆ B and B ⊆ C, then A ⊆C.

==Theorem==
For all set $A$ and $B$, if $A\subseteq B$, then 
$$
A\cap B=A
$$
$$
A\cup B=B
$$
Proof :
Suppose  $x$ is an arbitrary element in $A$ and $A\subseteq B$ and $A \cap B$. 
We already know that $A\cap B\subseteq A$. Thus it remain to show $A\subseteq A\cap B$. Since $A\subseteq B$ and $x \in A$ , it follow that $x \in B$. Hence, $x \in A$ and $x \in B$ implying that $x \in A\cap B$. Therefore, $A\subseteq A\cap B$. 

#### Set identities
1) Identity law 
$A\cup \emptyset=A$ and $A\cap U=A$

2) Complement law
$A\cup A^{c}=U$ and $A\cap A^{c}=\emptyset$

3) Double Complement law
$(A^{c})^{c}=A$

4) Idempotent Law
$A\cup A=A$ and $A\cap A=A$


==Theorem==
Set Difference Law
For all sets A and B
$$
A \setminus B=A \cap B^{c}
$$
Suppose $A$ and $B$ are arbitrary sets. Suppose x is an arbitrary element in $A \setminus B$. 
Then, $x \in A$ and $x \not\in B$.
hence, $x \in A$ and $x \in B^{c}$
Thus, $x \in A \cap B^{c}$
Therefore, $A\setminus B\subseteq A \cap B^{c}$

And conversely....

==Theorem==
Commutative law
Associative law
De Morgan's Laws


==Theorem==
Distributive laws
For all sets $A,B$ and $C$,
$$
\begin{array}
\ a) A\cup(B\cap C)=(A\cup B)\cap(A\cup C) \\
b) A\cap (B\cup C)=(A\cap B)\cup(A\cap C)
\end{array}
$$
Proof 1:
Suppose $A,B$ and $C$ are arbitrary set. We need to prove $A\cup(B\cap C)\subseteq(A\cup B)\cap(A\cup C)$.

Suppose $x$ is an arbitrary element in $A\cup(B\cap C)$. Then, $x \in A$ or $x \in B\cap C$

Case 1: $x \in A$
Thus, $x \in A \cup B$ and $x \in A \cup C$. Hence, $x \in(A\cup B)\cap(A\cup C)$

Case 2: $x \in B\cap C$
Thus, $x \in B$ and $x \in C$. Thus, $x \in B\cup A$ and $x \in C \cup A$. Thus, $x \in(A\cup B)\cap(A\cup C)$.

In either case, $x \in(A\cup B)\cap(A\cup C)$. Therefore, $A\cup(B\cap C)\subseteq(A\cup B)\cap(A\cup C)$


Conversely, we need to show that $(A\cup B)\cap(A\cup C)\subseteq A\cup(B\cap C)$
Suppose $x$ is an arbitrary element in $A\cup B$ and $A\cup C$.
Then, $x \in A\cup B$ and $x \in A \cup C$

Case 1: $x \in A$
Thus, $x \in A \cup(B \cap C)$.

Case 2: $x \not\in A$
Then, $x \in B$ and $x \in C$. Hence, $x \in B\cap C$.
Therefore, $x \in A\cup(B\cap C)$.

in either case .......
Since..... 

==Generalized Distributive Laws==

For any set A and for every positive integer n and any sets $B_{1},B_{2},B_{3},\dots B_{n}$,

$$
A\cup \bigcap_{i=1}^{n}B_{i}=\bigcap_{i=1}^{n}(A\cup B_{i})
$$
We argue by mathematical induction. Let the property $P(n)$ be defined as follows.
$$
P(n):A\cup \bigcap_{i=1}^{n}B_{i}=\bigcap_{i=1}^{n}(A\cup B_{i})
$$

For basis step, $P(1)$ is true because 
$$
A\cup\bigcap_{i=1}^{1}B_{i}=A\cup B_{1}=\bigcap_{i=1}^{1}(A\cup B_{i})
$$

For the induction step, suppose $n$ is an arbitrary positive integer and suppose $P(n)$ is true.

$$
\begin{align}
A\cup \bigcap_{i=1}^{n+1}B_{i}&=A\cup \bigcap_{i=1}^{n}B_{i}\cap B_{n+1} \\
&=\bigcap_{i=1}^{n}(A\cup B_{i})\cap B_{n+1} \text{ (By IH)} \\
&= \bigcap_{i=1}^{n}(A\cup B_{i}) \cap(A\cup B_{n+1}) \\
&=\bigcap_{i=1}^{n+1}(A\cup B_{i})
\end{align}
$$
Hence, P(n +1) is true. Therefore, by the Principle of Mathematical Induction, we conclude that P(n) is true for all positive integers n

How about direct proof? (In text book)

==Example==
$$
(A\cap B)-C=(A-C)\cap B
$$
==Example==
$$
(A\cap B)\cup(A\cap B^{c})=A
$$
(Absorption law)
We can use algebraic method of proof.

#### Contradiction
To prove that a set A is equal to the empty set ∅, we argue by contradiction. 
Assume A is nonempty and suppose a ∈ A. Then we derive a contradiction.

==Example==
Prove the complement law: for all sets $A$, $A\cap A^{c}=\emptyset$

Proof:
We argue by contradiction. Suppose $A$ is an arbitrary set. Assume $A\cap A^{c}\neq \emptyset$ . Suppose $x \in A \cap A^{c}$. Thus, $x \in A$ and $x \not\in A$, a contradiction.

==Example==
Prove that for all sets A, A ∩ ∅ = ∅.

==Example==
Prove that for all sets A, B, and C, if A ⊆ B and $B\subseteq C^{c}$, then A∩C =∅.

==Example==
Prove that for all sets A, B, and C, if C ⊆ B −A, then A∩C = ∅.

#### Cardinality of Power Set
