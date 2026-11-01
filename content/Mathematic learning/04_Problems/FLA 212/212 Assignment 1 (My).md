1. Let $V = \mathbb { C } ^ { 3 }$ be the vector space over C, and consider the vectors 

$$
u = (1, 1, 0), \qquad v = (1, 0, 1), \qquad w = (2, 1, 1).
$$

A student claims that $S = \{ u , v , w \}$ is a basis for V. The student gives the following proof: 

Step 1: All three vectors are nonzero. 

Step 2: Since the vectors are nonzero and there are three vectors in V , they span V. 

Step 3: Therefore, S is a basis for V. 

(a) Evaluate the student's proof. Identify the first incorrect step and explain why the reasoning is invalid. 

The student proof is incorrect in step 2. Consider the theorem below:

> [!theorem]
> If there exist a 0 vector in a subset of a vector space $V$ , then the vector set is a linearly dependent set in $V$

The student is trying to use the converse of this theorem to show that the vector set is linearly independent which is not true. Hence, the student cannot use the Basis Theorem to show that the 3 vectors span $V$.

---


(b) Construct a nontrivial linear combination of $u , v ,$ w that equals the zero vector. Explain how your result affects the student's conclusion. 
Given
$$
\begin{matrix}
u=(1,1,0) &v=(1,0,1) &w=(2,1,1)
\end{matrix}
$$
Consider the vector equation:
$$
c_1 u + c_2 v + c_3 w = \mathbf{0}
$$

Notice that, 
$$
u + v - w = \mathbf{0} 
$$

Since the scalars $(c_1, c_2, c_3) = (1, 1, -1) \neq (0, 0, 0)$, this is a nontrivial solution for the vector equation. By definition, the set $\{u, v, w\}$ is linearly dependent. 

A basis must be linearly independent, so $S$ cannot be a basis for $V = \mathbb{C}^3$, directly contradicting the student's conclusion in Step 3.

---


(c) The student revises the argument by replacing w with $p = ( 1 , - 1 , 1 )$ Determine whether u, v, p is a basis for V. Justify your evaluation. 

Consider the matrix $A=\begin{bmatrix}u^{T} & v^{T} & p^{T}\end{bmatrix}$, by invertible matrix theorem, $A$ is invertible iff $\det A \neq 0$.

Find $\det(A)$:
$$
\begin{align}
\det(A) &= \begin{vmatrix}
1 & 1 & 1  \\
1 & 0 & -1  \\
0 & 1 & 1 
\end{vmatrix} \\
&= \begin{vmatrix}
1 & 1 & 1  \\
0 & -1 & -2  \\
0 & 1 & 1 
\end{vmatrix} && (R^{1}_{2}(-1)) \\
&= \begin{vmatrix}
1 & 1 & 1 \\
0 & -1 & -2 \\
0 & 0 & -1
\end{vmatrix} && (R^{2}_{3}(1)) \\
&= (1)(-1)(-1) = 1
\end{align}
$$

Thus, it follow that $\det A=1(-1)(-1)=1 \neq 0$. Thus, by 
invertible matrix theorem, it follow that $A$ is invertible. Thus, the column of $A$ span $Col(A)$ which is $V=\mathbb{C}^{3}$ and the column of $A$ which is $\{ u^{T},v^{T},p^{T}\}$ are linearly independent. Hence, $\{ u,v,p \}$ is a basis for $V=\mathbb{C}^{3}$.

---


(d) Explain why the condition that a set contains exactly three nonzero vectors in V is insufficient to conclude that the set is a basis. State the additional condition needed. 

By definition, a subset of a vector space $V$ is a **basis** if and only if it satisfies two conditions:
1. It is linearly independent.
2. It spans $V$.

The condition is insufficient because it cannot deduce that the set of vector is linearly independent. We can see a counter example in (b).

When 3 vectors in $V=\mathbb{C}^{3}$ are linearly dependent, It cannot span $V$ by the Basis Theorem. 

The additional condition needed:
Since $dim(V)=dim(\mathbb{C}^{3})=3$  and the number of vectors in the set matches the dimension of the space,
By the Basis theorem, the required additional condition is the three vectors are linearly independent or they span $V$. Either condition will do.

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

For any element $w_{1}\in W$ such that $w_{1}=cx^{2}$ for some $c\in \mathbb{C}$, it follow that
$$
w_{1}=0+0x+cx^{2}\in V
$$
Thus, $W\subseteq V$

Check 0 vector:
Let $a=0$ and $b=0$. Thus,
$$
u_{1}=0+0x=0\in U
$$
and let $c=0$. Thus,
$$
\begin{align}
w_{1}&=0x^{2}=0\in W
\end{align}
$$

Closure under addition:
For any $u_{1}=a+bx\in U$ and $u_{2}=c+dx\in U$, we have 

$$
\begin{align}
u_{1}+u_{2}&=(a+bx)+(c+dx) \\
&=(a+c)+(bx+dx) \\
&=(a+c)+(b+d)x 
\end{align}
$$

Since $a+c\in \mathbb{C}$ and $b+d\in \mathbb{C}$, it follow that $u_{1}+u_{2}\in U$.

For any $w_{1}=ax^{2}\in W$ and $w_{2}=bx^{2}\in W$. We have
$$
\begin{align}
w_{1}+w_{2}&=ax^{2}+bx^{2} \\
&=(a+b)x^{2} 
\end{align}
$$
Since $a+b\in \mathbb{C}$, it follow that $w_{1}+w_{2}\in W$.

Closure under multiplication:
For any $u_{1}=a+bx\in U$ and $c\in \mathbb{C}$. It follow that
$$
\begin{align}
cu_{1}&=c(a+bx) \\
&=ca+ bc x 
\end{align}
$$

Since $ca\in \mathbb{C}$ and $bc\in \mathbb{C}$, it follow that $cu_{1}\in U$.

For any $w_{1}=ax^{2}\in W$ and $c\in \mathbb{C}$, it follow that
$$
\begin{align}
cw_{1}&=cax^{2}
\end{align}
$$
Since $ca\in \mathbb{C}$, it follow that $cw_{1}\in W$.

Thus, $U$ and $W$ are subspace of $V$.

> [!remark]
> Since $U\subseteq V$ and $W\subseteq V$, it follow if an element is in $U$ or $W$ then it is also an element in $V$. Thus, the property above like associative, distributive, commutative and so on are justified by the axiom of vector space $V$  

---


(b) Determine $U \cap W$

Let $p(x) \in U \cap W$. Since $p(x) \in U$, $p(x) = a + bx$ for some $a, b \in \mathbb{C}$. Since $p(x) \in W$, $p(x) = cx^2$ for some $c \in \mathbb{C}$.
Equating the two:
$$
\begin{align}
a + bx &= cx^2
\end{align}
$$

It follow that $a=b=c=0$. Thus, $u_{1}=0+0x+0cx^{2}$ which is the 0 vector in $V$. Hence, $U\cap W=\{ 0 \}$.

(c) Determine $U + W$ and hence decide whether $V = U + W$

$$
\begin{align}
U+W&=\{ u+w| u\in U,w\in W \} \\
&=\{ (a+bx)+cx^{2}|a,b,c\in \mathbb{C} \} \\
&= \{ a+bx+cx^{2}|a,b,c\in \mathbb{C} \}
\end{align}
$$
Comparing this with the definition of $V$:
$$
V=\{ a_{1}+a_{2}x+a_{3}x^{2}|a_{1},a_{2},a_{3}\in \mathbb{C} \}
$$

By identifying $a_{1}=a,a_{2}=b$ and $a_{3}=c$, every element $V$ can be written as an element of $U+W$ and vice versa. Hence, $V=U+W$. $\blacksquare$


(d) Determine whether $V = U \oplus W$ . Justify your answer. 

Yes, $V = U \oplus W$. By theorem, a vector space is the direct sum $V = U \oplus W$ if and only if $V = U + W$ and $U \cap W = \{ 0 \}$. Since both conditions were shown in (b) and (c), it follows that $V = U \oplus W$. $\blacksquare$ 


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
