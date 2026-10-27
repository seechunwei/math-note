1. Let $V = \mathbb { C } ^ { 3 }$ be the vector space over C, and consider the vectors 

$$
u = (1, 1, 0), \qquad v = (1, 0, 1), \qquad w = (2, 1, 1).
$$

A student claims that $S = \{ u , v , w \}$ is a basis for V. The student gives the following proof: 

Step 1: All three vectors are nonzero. 

Step 2: Since the vectors are nonzero and there are three vectors in V , they span V. 

Step 3: Therefore, S is a basis for V. 

(a) Evaluate the student's proof. Identify the first incorrect step and explain why the reasoning is invalid. 


---


(b) Construct a nontrivial linear combination of $u , v ,$ w that equals the zero vector. Explain how your result affects the student's conclusion. 

---


(c) The student revises the argument by replacing w with $p = ( 1 , - 1 , 1 )$ Determine whether u, v, p is a basis for V. Justify your evaluation. 


---


(d) Explain why the condition that a set contains exactly three nonzero vectors in V is insufficient to conclude that the set is a basis. State the additional condition needed. 


---

2. Let $A = \left( a _ { i j } \right)$ be an $n \times n$ matrix. The determinant of A is defined by 

$$
\det (A) = \sum_ {\sigma \in S _ {n}} \operatorname{sgn} (\sigma) \prod_ {i = 1} ^ {n} a _ {i, \sigma (i)}.
$$

Let B and C be two $n \times n$ matrices that differ only in their k-th rows. Suppose the k-th row of B is $( b _ { k 1 } , b _ { k 2 } , \ldots , b _ { k n } )$ , while the k-th row of C is $( c _ { k 1 } , c _ { k 2 } , \ldots , c _ { k n } )$ 

Let D be the matrix obtained from B by replacing its k-th row with the sum of the k-th rows of B and $C ,$ while keeping all other rows unchanged. 

We claim that 

$$
\det (D) = \det (B) + \det (C).
$$

(a) Since the determinant is defined as a sum over all permutations, evaluate the claim. Is it correct for all such matrices B and C? Explain your reasoning. 

Yes, the claim is correct for all such matrices $B$ and $C$.

**Reasoning:**
By the permutation definition (Leibniz formula), the determinant of an $n \times n$ matrix is given by:
$$
\det(D)= \sum_{\sigma \in S_n} \operatorname{sgn}(\sigma) \prod_{i=1}^n d_{i,\sigma(i)}
$$
In this expansion, each term consists of a product of $n$ matrix entries, with exactly one entry chosen from each row $i \in \{1, 2, \dots, n\}$. 

Because matrices $B$ and $C$ differ only in their $k$-th rows, matrix $D$ has the sum $(b_{kj} + c_{kj})$ in the $k$-th row, while all other $(n-1)$ rows are identical ($d_{ij} = b_{ij} = c_{ij}$ for $i \neq k$). Thus, in every permutation product $\prod_{i=1}^n d_{i,\sigma(i)}$, the addition $(b_{k,\sigma(k)} + c_{k,\sigma(k)})$ occurs in only a single factor.

By the distributive law of multiplication over addition, each product term splits into two separate products—one containing the factor from $B$ and the other from $C$. Since summation is splitable $\left( \sum(A+B)=\sum A+\sum B \right)$, summing these split terms over all $\sigma \in S_n$ yields $\det(B) + \det(C)$.

(This demonstrates the multilinearity of the determinant: the determinant is a linear function of each row individually, provided all other rows are held constant).

---

(b) Using the permutation definition of the determinant, determine whether the claim is valid when B and C have identical rows except for their k-th rows. Justify your conclusion by analyzing the terms in the permutation expansion. 

Solution:
Let $d_{ij}$ denote the $(i,j)$-entry of $D$. By construction, row $k$ satisfies $d_{kj} = b_{kj} + c_{kj}$, while all other rows $i \neq k$ satisfy $d_{ij} = b_{ij} = c_{ij}$.

By the permutation definition:
$$
\det(D) = \sum_{\sigma \in S_n} \operatorname{sgn}(\sigma) \prod_{i=1}^n d_{i,\sigma(i)}
$$
Each term in this expansion contains exactly one factor from each row $i \in \{1, 2, \dots, n\}$. In particular, row $k$ contributes $(b_{k,\sigma(k)} + c_{k,\sigma(k)})$, while all other factors satisfy $d_{i,\sigma(i)} = b_{i,\sigma(i)} = c_{i,\sigma(i)}$.

Thus, for row $i \neq k$, it follow that $\prod_{i=1, i \neq k}^n d_{i,\sigma(i)}=\prod_{i=1, i \neq k}^n b_{i,\sigma(i)}=\prod_{i=1, i \neq k}^n c_{i,\sigma(i)}$.

Applying the distributive law of multiplication over addition splits each product term into two parts:
$$
\begin{align}
\prod_{i=1}^n d_{i,\sigma(i)} &= \left(\prod_{i=1, i \neq k}^n d_{i,\sigma(i)}\right) (b_{k,\sigma(k)} + c_{k,\sigma(k)}) \\
&= \left(\prod_{i=1, i \neq k}^n b_{i,\sigma(i)}\right) b_{k,\sigma(k)} + \left(\prod_{i=1, i \neq k}^n c_{i,\sigma(i)}\right) c_{k,\sigma(k)} \\
&= \prod_{i=1}^n b_{i,\sigma(i)} + \prod_{i=1}^n c_{i,\sigma(i)}
\end{align}
$$
Substituting this back into the determinant sum and applying the linearity of summation:
$$
\begin{align}
\det(D) &= \sum_{\sigma \in S_n} \operatorname{sgn}(\sigma) \left( \prod_{i=1}^n b_{i,\sigma(i)} + \prod_{i=1}^n c_{i,\sigma(i)} \right) \\
&= \sum_{\sigma \in S_n} \operatorname{sgn}(\sigma) \prod_{i=1}^n b_{i,\sigma(i)} + \sum_{\sigma \in S_n} \operatorname{sgn}(\sigma) \prod_{i=1}^n c_{i,\sigma(i)} \\
&= \det(B) + \det(C)
\end{align}
$$
Since $B$ and $C$ are arbitrary, the claim is valid for all such $n \times n$ matrices. $\blacksquare$

---

(c) If the $k$-th row of a matrix $A$ is multiplied by a scalar $\lambda$, then its determinant becomes $\lambda \det(A)$. Evaluate this claim using the permutation definition. 

By the permutation definition of the determinant:
$$
\det(A) = \sum_{\sigma \in S_n} \operatorname{sgn}(\sigma) \prod_{i=1}^n a_{i,\sigma(i)}
$$
Let $A'$ be the matrix obtained by multiplying the $k$-th row of $A$ by $\lambda$. The entries of $A'$ satisfy $a'_{kj} = \lambda a_{kj}$ for row $k$, and $a'_{ij} = a_{ij}$ for all $i \neq k$.

Each product in the Leibniz expansion contains exactly one entry from each row. In particular, row $k$ contributes the factor $a'_{k,\sigma(k)} = \lambda a_{k,\sigma(k)}$. By associativity and commutativity of multiplication:
$$
\prod_{i=1}^n a'_{i,\sigma(i)} = \left(\prod_{i=1, i \neq k}^n a_{i,\sigma(i)}\right) (\lambda a_{k,\sigma(k)}) = \lambda \prod_{i=1}^n a_{i,\sigma(i)}
$$
Substituting this into the expansion of $\det(A')$ and factoring out $\lambda$ by the distributive property of summation:
$$
\begin{align}
\det(A') &= \sum_{\sigma \in S_n} \operatorname{sgn}(\sigma) \prod_{i=1}^n a'_{i,\sigma(i)} \\
&= \sum_{\sigma \in S_n} \operatorname{sgn}(\sigma) \left( \lambda \prod_{i=1}^n a_{i,\sigma(i)} \right) \\
&= \lambda \sum_{\sigma \in S_n} \operatorname{sgn}(\sigma) \prod_{i=1}^n a_{i,\sigma(i)} \\
&= \lambda \det(A)
\end{align}
$$
Thus, $\det(A') = \lambda \det(A)$. $\blacksquare$

---

3. Let $V = P _ { 2 } ( \mathbb { C } )$ be the vector space of all polynomials of degree at most 2 with complex coefficients. Let 

$$
U = \{a + b x | a, b \in \mathbb {C} \} \quad \mathrm{and} \quad W = \{c x ^ {2} | c \in C \}.
$$

(a) Show that U and W are subspaces of V. 

$$
V=\{ a_{1}+a_{2}x+a_{3}x^{2}|a_{1},a_{2},a_{3}\in \mathbb{C} \}
$$

Show $U\subseteq V$ and $W\subseteq V$:
For any element $u_{1}\in U$ such that $u_{1}=a+bx$ for $a,b\in \mathbb{C}$, we have
$$
u_{1}=a+bx+0x^{2} \in V
$$
Thus, $U\subseteq V$.

To show that a subset of vector space $V$ is a subspaces, we must verify three criteria:
i) zero vector: $0 \in S$
ii) close under addition: if $a, b \in S$ then $a + b \in S$
iii) close under scalar multiplication: if $a \in S$ and $k \in \mathbb{C}$, then $ka \in S$

For $U = \{a + bx \mid a, b \in \mathbb{C}\}$:
i) Let $a$ and $b$ equal to zero.
Then,
$$
0 + 0x = 0 \in U
$$
Hence, $0 \in U$.

ii) Let $u_1(x), u_2(x) \in U$.
Thus, $u_1 = a_1 + b_1 x$ for some $a_1, b_1 \in \mathbb{C}$
$u_2 = a_2 + b_2 x$ for some $a_2, b_2 \in \mathbb{C}$
$$
\begin{align}
u_1 + u_2 &= (a_1 + b_1 x) + (a_2 + b_2 x) \\
&= (a_1 + a_2) + (b_1 x + b_2 x) \\
&= (a_1 + a_2) + (b_1 + b_2)x
\end{align}
$$
Since $a_1 + a_2 \in \mathbb{C}$ and $b_1 + b_2 \in \mathbb{C}$, $u_1 + u_2 \in U$.
Hence, $U$ is closed under addition.

iii) Suppose $u_1(x) = a + bx \in U$ for some $a, b \in \mathbb{C}$ and $k \in \mathbb{C}$.
$$
\begin{align}
k(u_1) &= k(a + bx) \\
&= ka + kbx
\end{align}
$$
Since $ka, kb \in \mathbb{C}$, $k u_1 \in U$.
Hence, $U$ is closed under scalar multiplication.

Therefore, $U$ is a subspace of $V$.

For $W = \{cx^2 \mid c \in \mathbb{C}\}$:
i) Let $c$ equal to zero.
Then,
$$
0x^2 = 0 \in W
$$
Hence, $0 \in W$.

ii) Let $w_1, w_2 \in W$.
Thus, $w_1 = c_1 x^2$ for some $c_1 \in \mathbb{C}$
$w_2 = c_2 x^2$ for some $c_2 \in \mathbb{C}$
$$
\begin{align}
w_1 + w_2 &= c_1 x^2 + c_2 x^2 \\
&= (c_1 + c_2)x^2
\end{align}
$$
Since $c_1 + c_2 \in \mathbb{C}$, $w_1 + w_2 \in W$.
Hence, $W$ is closed under addition.

iii) Suppose $w_1 = cx^2 \in W$ for some $c \in \mathbb{C}$ and $k \in \mathbb{C}$.
$$
\begin{align}
k(w_1) &= k(cx^2) \\
&= (kc)x^2
\end{align}
$$
Since $kc \in \mathbb{C}$, $k w_1 \in W$.
Hence, $W$ is closed under scalar multiplication.

Therefore, $W$ is a subspace of $V$.

> [!remark]
> Since $U\subseteq V$ and $W\subseteq V$, it follow if an element is in $U$ or $W$ then it is also an element in $V$. Thus, the property above like associative, distributive, commutative and so on are justified by the axiom of vector space $V$  
> 
> Note that $\mathbb{C}$ is a field, thus it is closure under addition and scalar multiplication.


---


(b) Determine $U \cap W$
 Let $p(x) \in U \cap W$.
Then $p(x) = a + bx \in U$ and $p(x) = cx^2 \in W$.
Thus,
$$
\begin{align}
p(x) = a + bx &= cx^2 \\
a + bx - cx^2 &= 0
\end{align}
$$
Since this is the zero polynomial, all coefficient must be zero.
Then $a = b = c = 0$.
Hence, $p(x) = 0$.
Therefore,
$$
p(x) \in U \cap W \implies 0 \in U \cap W \implies U \cap W = \{0\}
$$


(c) Determine $U + W$ and hence decide whether $V = U + W$
By definition, $U + W = \{u + w \mid u \in U, w \in W\}$.
Let $u_1 = a + bx \in U$ for some $a, b \in \mathbb{C}$
$w_1 = cx^2 \in W$ for some $c \in \mathbb{C}$
$$
\begin{align}
u_1 + w_1 &= (a + bx) + cx^2 \\
&= a + bx + cx^2
\end{align}
$$
Since $a, b, c \in \mathbb{C}$, then $U + W = \{a + bx + cx^2 \mid a, b, c \in \mathbb{C}\}$.
$V = P_2(\mathbb{C}) = \{a + bx + cx^2 \mid a, b, c \in \mathbb{C}\}$.
Therefore, $V = U + W$.


(d) Determine whether $V = U \oplus W$ . Justify your answer. 

 By the theorem, the vector space $V$ is a direct sum of subspaces $U$ and $W$ iff
i) $V = U + W$
ii) $U \cap W = \{0\}$

Since both condition is show in (b) and (c).
Therefore,
$$
V = U \oplus W
$$

---

4. Let $V = { M } _ { 2 \times 2 } ( \mathbb { C } )$ be the vector space over $\mathbb{R}$. Define $T : V  \to V$ by 

$$
T (A) = A + \bar {A},
$$

where $\bar{A}$ denotes the matrix obtained by taking the complex conjugate of every entry of A. 

(a) Let $A=\begin{pmatrix}1+i & 2-i \\  3i & -2\end{pmatrix}$. Compute $T ( A )$.

$$
\bar{A}= \begin{pmatrix}
1-i & 2+i \\
-3i & -2
\end{pmatrix}
$$

Thus,
$$
\begin{align}
T(A)&= A+\bar{A} \\
&=\begin{pmatrix}
1+i & 2-i \\
3i & -2
\end{pmatrix}+ \begin{pmatrix}
1-i & 2+i \\
-3i & -2
\end{pmatrix} \\
&= \begin{pmatrix}
2 & 4 \\
0 & -4
\end{pmatrix}
\end{align}
$$

---


(b) Determine whether T is a linear transformation over $\mathbb{R}$. 

> [!theorem] Lemma:
> For any $A,B\in M_{2\times 2}(\mathbb{C})$,   $\overline{A+B}=\bar{A}+\bar{B}$ 

Proof:
Suppose $z=a+bi$ and $w=c+di$ are arbitrary entries of any matrix in $M_{2\times 2}(\mathbb{C})$. Thus,

$$
\begin{align}
\overline{z+w}&=\overline{(a+c)+(b+d)i} \\
&=(a+c)-(b+d)i
\end{align}
$$
and
$$
\begin{align}
\bar{z}+\bar{w}&= a-bi+c-di \\
&=(a+c)-(b+d)i
\end{align}
$$
Hence, it follow that
$$
\overline{z+w}=\bar{z}+\bar{w}
$$

Therefore, it follow that $\overline{(A+B)_{ij}}=\overline{(A)_{ij}}+\overline{(B)_{ij}}$ which implies  $\overline{A+B}=\bar{A}+\bar{B}$. $\blacksquare$

For any $A,B\in V$, it follow that
$$
\begin{align}
T(A+B)&=A+B+ \overline{A+B} \\
&=A+B+\bar{A}+\bar{B} \\
&=A+\bar{A}+B+\bar{B} \\
&=T(A)+T(B)
\end{align}
$$

For any $k\in \mathbb{R}$, note that $\bar{k}=k$. So,

$$
\begin{align}
T(kA)&= kA+ \overline{kA} \\
&=kA+ \bar{k}\bar{A} \\
&=kA+k\bar{A} \\
&=k(A+\bar{A}) \\
&=kT(A)
\end{align}
$$

Thus, $T$ is a linear transformation over $\mathbb{R}$.

---

(c) Consider the scalar i and a suitable non-zero matrix. Determine whether T is also a linear transformation over $\mathbb{C}$.

When $V = M_{2\times 2}(\mathbb{C})$ is considered as a vector space over $\mathbb{C}$, for any scalar $k \in \mathbb{C}$ and matrix $A \in V$:
$$
\begin{align}
T(kA) &= kA + \overline{kA} \\
&= kA + \bar{k}\bar{A}
\end{align}
$$
and
$$
\begin{align}
kT(A) &= k(A + \bar{A}) \\
&= kA + k\bar{A}
\end{align}
$$

Since $\bar{k} = k$ if and only if $k$ is purely real, $T(kA) \neq kT(A)$ in general over $\mathbb{C}$.

**Example:**  
Let $k = i$, and let $A = \begin{pmatrix} 1+i & 2-i \\ 3i & -2 \end{pmatrix}$ (the non-zero matrix from part (a)).  
From part (a), we already have $T(A) = \begin{pmatrix} 2 & 4 \\ 0 & -4 \end{pmatrix}$.

Computing $T(kA)$:
$$
\begin{align}
T(kA) &= kA + \overline{kA} \\
&= kA + \bar{k}\bar{A} \\
&= i\begin{pmatrix} 1+i & 2-i \\ 3i & -2 \end{pmatrix} - i\begin{pmatrix} 1-i & 2+i \\ -3i & -2 \end{pmatrix} \\
&= i \left[ \begin{pmatrix} 1+i & 2-i \\ 3i & -2 \end{pmatrix} - \begin{pmatrix} 1-i & 2+i \\ -3i & -2 \end{pmatrix} \right] \\
&= i \begin{pmatrix} 2i & -2i \\ 6i & 0 \end{pmatrix} \\
&= \begin{pmatrix} -2 & 2 \\ -6 & 0 \end{pmatrix}
\end{align}
$$

On the other hand, computing $kT(A)$:
$$
kT(A) = i T(A) = i \begin{pmatrix} 2 & 4 \\ 0 & -4 \end{pmatrix} = \begin{pmatrix} 2i & 4i \\ 0 & -4i \end{pmatrix}
$$

Since:
$$T(kA) = \begin{pmatrix} -2 & 2 \\ -6 & 0 \end{pmatrix} \neq \begin{pmatrix} 2i & 4i \\ 0 & -4i \end{pmatrix} = kT(A)$$

$T$ fails the scalar multiplication property over $\mathbb{C}$.

Therefore, we conclude that $T$ is not a linear transformation over $\mathbb{C}$. $\blacksquare$
