
Complex Vector space is a set of element with 2 operation defined such that addition of element and scalar multiplication over complex number $\mathbb{C}\in F$ that fulfill the 10 axiom.

The standard basis for $\mathbb{C}^{n}$ over $\mathbb{C}$ is the standard basis for $\mathbb{R}^{n}$ over $\mathbb{R}$:

$$
\{ e_{1},e_{2},\dots,e_{n} \}
$$

How about the standard basis for $\mathbb{C}^{n}$ over $\mathbb{R}$. Then, the number of basis is the 2 times the standard basis for $\mathbb{C}^{n}$ over $\mathbb{C}$:

$$
\{ e_{1},\dots,e_{n}, i_{1},\dots,i_{n} \}
$$

where $i_{n}$ is the vector with $n-th$ entry is $i$ and other entry is $0$.

> [!theorem] Dimension of a Complex Vector Space over $\mathbb{R}$ (Realification)
> Let $V$ be a finite-dimensional vector space over $\mathbb{C}$. By restricting scalar multiplication to the real numbers $\mathbb{R}$, $V$ becomes a vector space over $\mathbb{R}$ (denoted $V_{\mathbb{R}}$).
> 
> If $\dim_{\mathbb{C}}(V) = n$, then:
> $$\dim_{\mathbb{R}}(V) = 2 \dim_{\mathbb{C}}(V) = 2n$$

^3475e4

> [!proof] Basis Construction & Proof
> Let $\mathcal{B} = \{v_1, v_2, \dots, v_n\}$ be a basis of $V$ over $\mathbb{C}$. 
> Then the set of $2n$ vectors:
> $$\mathcal{B}_{\mathbb{R}} = \{v_1, iv_1, \; v_2, iv_2, \; \dots, \; v_n, iv_n\}$$
> forms a basis of $V$ over $\mathbb{R}$.
> 
> 1. **Spanning over $\mathbb{R}$:**
>    Any $v \in V$ can be written over $\mathbb{C}$ as $v = \sum_{j=1}^n c_j v_j$ for complex scalars $c_j \in \mathbb{C}$.
>    Decompose each scalar into real and imaginary parts: $c_j = a_j + i b_j$ where $a_j, b_j \in \mathbb{R}$:
>    $$v = \sum_{j=1}^n (a_j + i b_j) v_j = \sum_{j=1}^n a_j v_j + \sum_{j=1}^n b_j (iv_j)$$
>    Since $a_j, b_j \in \mathbb{R}$, $v$ is expressed as a real linear combination of $\mathcal{B}_{\mathbb{R}}$. Thus, $\operatorname{span}_{\mathbb{R}}(\mathcal{B}_{\mathbb{R}}) = V$.
> 
> 2. **Linear Independence over $\mathbb{R}$:**
>    Suppose a real linear combination evaluates to the zero vector:
>    $$\sum_{j=1}^n a_j v_j + \sum_{j=1}^n b_j (iv_j) = \mathbf{0} \quad (a_j, b_j \in \mathbb{R})$$
>    Regrouping by complex scalars:
>    $$\sum_{j=1}^n (a_j + i b_j) v_j = \mathbf{0}$$
>    Since $\{v_1, \dots, v_n\}$ is linearly independent over $\mathbb{C}$, every complex coefficient must vanish:
>    $$a_j + i b_j = 0 + 0i \implies a_j = 0 \quad \text{and} \quad b_j = 0 \quad \text{for all } j$$
>    Hence, all $2n$ real coefficients are zero, proving $\mathcal{B}_{\mathbb{R}}$ is linearly independent over $\mathbb{R}$.
> 
> $$\therefore \dim_{\mathbb{R}}(V) = |\mathcal{B}_{\mathbb{R}}| = 2n = 2 \dim_{\mathbb{C}}(V)$$

> [!note] Field Extension Perspective (Tower Law)
> In abstract algebra, this is an application of the field extension degree formula:
> $$\dim_{\mathbb{R}}(V) = [\mathbb{C} : \mathbb{R}] \cdot \dim_{\mathbb{C}}(V) = 2 \dim_{\mathbb{C}}(V)$$
> because the field degree $[\mathbb{C} : \mathbb{R}] = 2$ with standard basis $\{1, i\}$ over $\mathbb{R}$.



---

## Sum and Direct Sum

The reason why we have to study sums rather than unions is that the union of subspaces is rarely a subspace.

> [!definition]
> Suppose $U_{1},U_{2},\dots U_{n}$ are subspaces of $V$. The sum of $U_{1},U_{2},\dots,U_{n}$ denoted as $U_{1}+U_{2}+\dots+U_{n}$ is the set of all possible sums of $U_{1},\dots,U_{n}$.
> 
> We can write $U+W=\{ u+w|u\in U,w\in W \}$

Verify it is a subspace:

Note that since $U$ and $W$ are subspace of $V$, it follow that $0\in U$ and $0\in W$. Since $0=0+0$, it follow that $0\in U+W$.


For any $v_{1},v_{2}\in U+W$, by definition $v_{1}=u_{1}+w_{1}$ for some $u_{1}\in U$ and $w_{1}\in W$ while $v_{2}=u_{2}+w_{2}$ for some $u_{2}\in U$ and $w_{2}\in W$. Thus

$$
\begin{align}
v_{1}+v_{2}&=(u_{1}+w_{1})+(u_{2}+w_{2}) \\
&=(u_{1}+u_{2})+(w_{1}+w_{2})
\end{align}
$$

The above operation is justified by the fact that they are element of $V$. Note that $u_{1}+u_{2}\in U$ and $w_{1}+w_{2}\in W$. Thus, $v_{1}+v_{2}\in U+W$.

For any $c\in F$, it follow that
$$
\begin{align}
cv_{1}&=c(u_{1}+w_{1}) \\
&=cu_{1}+cw_{1}
\end{align}
$$

$cu_{1}\in U$ and $cw_{1}\in W$. Thus, $cv_{1}\in U+W$. Thus, it is a subspace. $\blacksquare$

> [!note] Why $U$ and $W$ Must Belong to the Same Vector Space $V$
> 1. **Addition must be defined:** The sum $u + w$ only has meaning if $u$ and $w$ live in the same space where vector addition $+ : V \times V \to V$ is defined. (For example, you cannot add a vector in $\mathbb{R}^2$ to a polynomial in $\mathcal{P}(\mathbb{R})$).
> 2. **Axioms of $V$ justify rearranging terms:** In the proof, regrouping $(u_1 + w_1) + (u_2 + w_2) = (u_1 + u_2) + (w_1 + w_2)$ and distributing $c(u_1 + w_1) = cu_1 + cw_1$ are valid **only because** all elements inherit the associativity, commutativity, and distributivity axioms from the common ambient space $V$.


> [!definition] Direct Sum
> $V$ is a direct sum of subspaces $U_{1}, U_{2}, \dots, U_{n}$, written as $V = U_{1} \oplus U_{2} \oplus \dots \oplus U_{n}$, if each element $v \in V$ can be written uniquely as a sum:
> $$
> v = u_{1} + u_{2} + \dots + u_{n} \quad \text{where } u_{j} \in U_{j}
> $$

### Equivalent Conditions for Direct Sum

^0339db

For two subspaces $U, W \subseteq V$, the following statements are equivalent:
1. $V = U \oplus W$ (every $v \in V$ has a unique representation $v = u + w$).
2. $V = U + W$ and $U \cap W = \{0\}$.
3. If $u + w = 0$ with $u \in U$ and $w \in W$, then $u = 0$ and $w = 0$.
4. For finite-dimensional $V$: $V = U + W$ and $\dim(V) = \dim(U) + \dim(W)$.

### Intuition: Why $U \cap W = \{0\}$ Means Unique Representation
What does $U \cap W = \{0\}$ mean in terms of linear independence and uniqueness?

Suppose $U = \operatorname{span}\{u_1, \dots, u_n\}$ and $W = \operatorname{span}\{w_1, \dots, w_m\}$ where each set is a basis.

If $U \cap W \neq \{0\}$, then there exists a non-zero vector $v$ in both subspaces ($v \in U \cap W$). Since $v$ belongs to both, it can be expanded in both bases:
$$
v = a_1 u_1 + \dots + a_n u_n \quad \text{and} \quad v = b_1 w_1 + \dots + b_m w_m
$$

This immediately leads to two things:
1. **Representation is not unique:** $v$ can be written as a sum in $U + W$ in two different ways:
   $$
   v = (a_1 u_1 + \dots + a_n u_n) + 0 \cdot w
   $$
   or
   $$
   v = 0 \cdot u + (b_1 w_1 + \dots + b_m w_m)
   $$
2. **The combined basis is linearly dependent:** Subtracting the two gives:
   $$
   a_1 u_1 + \dots + a_n u_n - b_1 w_1 - \dots - b_m w_m = 0
   $$
   Since $v \neq 0$, the coefficients cannot all be zero. Thus, the combined set $\{u_1, \dots, u_n, w_1, \dots, w_m\}$ is **linearly dependent**.

**Takeaway:**
$U \cap W = \{0\}$ ensures that the two subspaces share no non-zero vectors. Their bases are **mutually linearly independent**, which is why every vector in $U \oplus W$ has a **unique representation**.

> [!theorem] Linear Independence of Combined Bases $\iff$ Direct Sum
> Let $\mathcal{B}_U = \{u_1, \dots, u_n\}$ be a basis of $U$, and $\mathcal{B}_W = \{w_1, \dots, w_m\}$ be a basis of $W$.
> The combined set $\mathcal{B}_U \cup \mathcal{B}_W = \{u_1, \dots, u_n, w_1, \dots, w_m\}$ is **linearly independent**
> $$
> \iff
> $$
> The sum $U + W$ is a **direct sum** ($U \cap W = \{0\}$, denoted $U \oplus W$).
> 
> > [!proof]
> > - $(\implies)$ Suppose the combined set is linearly independent. If $v \in U \cap W$, then $v = \sum a_i u_i$ and $v = \sum b_j w_j$. Subtracting gives $\sum a_i u_i - \sum b_j w_j = 0$. By linear independence, all coefficients are $0$, so $v = 0$. Thus $U \cap W = \{0\}$.
> > - $(\impliedby)$ Suppose $U \cap W = \{0\}$. If $\sum a_i u_i + \sum b_j w_j = 0$, then $\sum a_i u_i = -\sum b_j w_j \in U \cap W = \{0\}$. Since $\{u_i\}$ and $\{w_j\}$ are bases of $U$ and $W$, this forces all $a_i = 0$ and $b_j = 0$. Hence the combined set is linearly independent.

^e822c9

> [!warning] Distinction: "Subspace" vs. "Direct Sum"
> - **$U + W$ is ALWAYS a subspace of $V$:** No independence is needed. Even if $U = W$ (identical bases), $U + U = U$ is still a valid subspace.
> - **Linear independence characterizes the DIRECT sum ($U \oplus W$):** The linear independence of the combined basis is what guarantees the decomposition $v = u + w$ is unique (no non-zero overlap).


### Generalization: Extension to $k \ge 3$ Subspaces & The Intersection Trap

> [!warning] The Intersection Trap for $k \ge 3$ Subspaces
> It is tempting to assume that $W_1 \oplus \dots \oplus W_k \iff \bigcap_{i=1}^k W_i = \{0\}$ or that pairwise intersections $W_i \cap W_j = \{0\}$ suffice. **Both assumptions are FALSE!**
> 
> **Why? Look at the algebra:**
> - **For 2 subspaces:** A non-trivial relation is $u + w = \mathbf{0} \implies u = -w$. 
>   The left side is in $U$, the right is in $W$, so $u \in U \cap W$. Hence, linear dependence directly means $U \cap W \neq \{0\}$.
> - **For 3 subspaces:** A non-trivial relation is $w_1 + w_2 + w_3 = \mathbf{0} \implies w_3 = -(w_1 + w_2)$.
>   The left side is in $W_3$, but the right side lives in the **sum** $(W_1 + W_2)$!
>   Therefore, linear dependence means:
>   $$W_3 \cap (W_1 + W_2) \neq \{0\}$$
>   It does **not** mean $w_3 \in W_1 \cap W_2 \cap W_3$.
> 
> **Geometric Counterexample in $\mathbb{R}^2$ [[FLA tutorial 2#^ea0d58]]:**
> Let $W_1$ be the $x$-axis, $W_2$ be the $y$-axis, and $W_3$ be the line $y = x$.
> - All pairwise intersections are trivial: $W_1 \cap W_2 = \{0\}$, $W_1 \cap W_3 = \{0\}$, $W_2 \cap W_3 = \{0\}$.
> - The mutual intersection is trivial: $W_1 \cap W_2 \cap W_3 = \{0\}$.
> - **Yet the sum is NOT direct:** $(1, 1) = (1, 0) + (0, 1)$ shows that $(1, 1) \in W_3 \cap (W_1 + W_2)$, so representations of vectors are not unique!
> 
> **Intuition: Equality ($w_1 = w_2 = w_3$) vs. Summing to Zero ($w_1 + w_2 + w_3 = \mathbf{0}$):**
> - The intersection condition $W_1 \cap W_2 \cap W_3 = \{0\}$ only asks about a single vector belonging to all three simultaneously:
>   $$w_1 = w_2 = w_3 = v \implies v = \mathbf{0}$$
>   It only guarantees that if vectors from each subspace are forced to be the **exact same vector**, they must be $\mathbf{0}$.
> - The direct sum condition $W_1 \oplus W_2 \oplus W_3$ is far stronger: it demands that their **sum cannot cancel out**:
>   $$w_1 + w_2 + w_3 = \mathbf{0} \implies w_1 = w_2 = w_3 = \mathbf{0}$$
>   Here, the vectors $w_1, w_2, w_3$ can be completely distinct! In $(1, 0) + (0, 1) + (-1, -1) = (0, 0)$, none of the three vectors are equal to each other, so $W_1 \cap W_2 \cap W_3 = \{0\}$ was completely powerless to prevent them from balancing to $\mathbf{0}$.


> [!theorem] Universal Direct Sum Theorem ($k$ Subspaces)
> Let $U_1, U_2, \dots, U_k$ be subspaces of $V$. The sum $U_1 + \dots + U_k$ is a **direct sum** (denoted $U_1 \oplus \dots \oplus U_k$) if and only if any of the following equivalent conditions hold:
> 1. **Unique Representation in the Sum:** Every vector $v \in U_1 + \dots + U_k$ can be written uniquely as:
>    $$v = u_1 + u_2 + \dots + u_k \quad \text{where } u_1 \in U_1, \; u_2 \in U_2, \; \dots, \; u_k \in U_k$$
> 2. **Trivial Zero Representation:** If arbitrary vectors $u_1 \in U_1, \dots, u_k \in U_k$ satisfy:
>    $$u_1 + u_2 + \dots + u_k = \mathbf{0}$$
>    then every single vector must be zero: $u_1 = u_2 = \dots = u_k = \mathbf{0}$.
> 3. **True Intersection Condition:** For every $j \in \{1, \dots, k\}$, the subspace $U_j$ intersects the sum of all the other subspaces only at zero:
>    $$U_j \cap \left( \sum_{i \neq j} U_i \right) = \{0\}$$
> 4. **Linear Independence of Combined Bases:** If $\mathcal{B}_j$ is a basis for each subspace $U_j$, then the combined union:
>    $$\mathcal{B} = \bigcup_{j=1}^k \mathcal{B}_j$$
>    is **linearly independent** (and forms a basis of $U_1 \oplus \dots \oplus U_k$).
> 5. **Dimension of the Sum (Finite-Dimensional):**
>    $$\dim(U_1 \oplus \dots \oplus U_k) = \sum_{j=1}^k \dim(U_j)$$

> [!proof] Justification of Statement 2 (Why Zero Sum Forces $u_j = \mathbf{0}$)
> - **Equivalence with Uniqueness (Statement 1):** If a vector $v$ has two representations $v = \sum u_j = \sum u_j'$, subtracting them yields:
>   $$\sum_{j=1}^k (u_j - u_j') = \mathbf{0}$$
>   Because each subspace is closed under subtraction, each difference $(u_j - u_j') \in U_j$. Statement 2 guarantees that any vectors from the subspaces summing to $\mathbf{0}$ must individually be $\mathbf{0}$, forcing $u_j - u_j' = \mathbf{0} \implies u_j = u_j'$ for all $j$. Thus, the representation is unique.
> - **Equivalence with True Intersection (Statement 3):** 
>   Suppose $u_1 + \dots + u_k = \mathbf{0}$. Isolate any arbitrary vector $u_j$:
>   $$u_j = -\sum_{i \neq j} u_i$$
>   The left side lives in $U_j$, while the right side lives in the sum of all other subspaces $\sum_{i \neq j} U_i$. Therefore:
>   $$u_j \in U_j \cap \left( \sum_{i \neq j} U_i \right) = \{\mathbf{0}\} \implies u_j = \mathbf{0}$$
>   Repeating this isolation for each $j \in \{1, \dots, k\}$ forces every $u_j = \mathbf{0}$.
>   *(Physical Intuition: To cancel out a non-zero vector $u_j \in U_j$, the remaining subspaces must together be capable of constructing its exact opposite $-u_j$. Since they share no common directions with $U_j$ beyond $\{\mathbf{0}\}$, it is impossible to cancel out non-zero components).*

> [!remark] When Does the Direct Sum Equal the Whole Space $V$?
> The conditions above only prove that the subspaces have no redundant overlap (i.e. the sum is **direct**, living as a subspace inside $V$).
> 
> To conclude that the direct sum equals the **entire ambient space** $V$ ($V = U_1 \oplus \dots \oplus U_k$), you must additionally confirm that they **span** all of $V$:
> 1. **General Case:** Show $U_1 + \dots + U_k = V$ (every vector in $V$ can be formed by adding vectors from the subspaces).
> 2. **Finite-Dimensional Shortcut:** If the sum is already direct, simply check if the total dimension matches:
>    $$\sum_{j=1}^k \dim(U_j) = \dim(V)$$



---

## Orthogonal Direct Sum ($\oplus^\perp$ or $U \perp W$)

While a direct sum is purely **algebraic** (requiring only vector space structure), an **orthogonal direct sum** is **geometric** (requiring an inner product space).

> [!definition] Orthogonal Subspaces & Orthogonal Direct Sum
> Equip $V$ with an inner product $\langle \cdot, \cdot \rangle$. Two subspaces $U$ and $W$ are **orthogonal** ($U \perp W$) if:
> $$
> \langle u, w \rangle = 0 \quad \text{for all } u \in U, \; w \in W
> $$
> When $V = U + W$ and $U \perp W$, $V$ is called the **orthogonal direct sum** of $U$ and $W$, denoted:
> $$
> V = U \oplus^\perp W \quad (\text{or } V = U \oplus W \text{ with } U \perp W)
> $$
> In this setting, $W$ is the **orthogonal complement** of $U$, denoted $U^\perp$:
> $$
> U^\perp = \{v \in V \mid \langle v, u \rangle = 0 \text{ for all } u \in U\}
> $$

> [!theorem] Orthogonality Automatically Implies Directness
> If $U \perp W$, then their sum is guaranteed to be a direct sum ($U \cap W = \{0\}$).
> 
> > [!proof]
> > Suppose $x \in U \cap W$. Since $x \in U$ and $x \in W$, and $U \perp W$:
> > $$
> > \langle x, x \rangle = 0
> > $$
> > By positive-definiteness of the inner product, $x = 0$. Hence $U \cap W = \{0\}$.

---

### Visual in $\mathbb{R}^2$
Consider the $x$-axis $U = \operatorname{span}\{(1, 0)\}$:
- **Direct Sum:** Any line through the origin other than $U$ can be a complement $W$. For example, if $W = \operatorname{span}\{(1, 1)\}$, then $\mathbb{R}^2 = U \oplus W$ with unique decomposition $(x, y) = (x - y, 0) + (y, y)$.
- **Orthogonal Direct Sum:** Only the perpendicular line works: $W = U^\perp = \operatorname{span}\{(0, 1)\}$ (the $y$-axis), giving $\mathbb{R}^2 = U \oplus^\perp U^\perp$ with $(x, y) = (x, 0) + (0, y)$.

---

## Dimensions and Orthogonal Direct Sum

### Dimension Formula
For finite-dimensional subspaces $U, W \subseteq V$:
$$
\dim(U + W) = \dim(U) + \dim(W) - \dim(U \cap W)
$$
For **any direct sum** ($U \cap W = \{0\}$):
$$
\dim(U \oplus W) = \dim(U) + \dim(W)
$$

### Does $\dim(U) + \dim(W) = \dim(V)$ Mean Orthogonal Direct Sum?
**No, it only means direct sum:**
- $\dim(U) + \dim(W) = \dim(V)$ is a **necessary** condition, but not sufficient.
- Orthogonality requires the geometric condition $\langle u, w \rangle = 0$.
- **Counterexample in $\mathbb{R}^2$:**
  Let $U = \operatorname{span}\{(1, 0)\}$ and $W = \operatorname{span}\{(1, 1)\}$.
  $$
  \dim(U) + \dim(W) = 1 + 1 = 2 = \dim(\mathbb{R}^2)
  $$
  Here $\mathbb{R}^2 = U \oplus W$ is a direct sum, but $\langle (1, 0), (1, 1) \rangle = 1 \neq 0$, so it is **not** an orthogonal direct sum.
- **When orthogonality is already known:** If $U \perp W$ is already given, then $\dim(U) + \dim(W) = \dim(V)$ guarantees that $U + W = V$, confirming $V = U \oplus^\perp W$.

---

## Application: Row Space and Nullspace
### Following the Chain: Orthogonal $\implies$ Direct Sum $\implies$ Full Decomposition

Consider an $m \times n$ matrix $A$. Both $\operatorname{Row}(A)$ and $\operatorname{Null}(A)$ are subspaces of the same ambient space $\mathbb{F}^n$.

#### 1. Orthogonal ($\operatorname{Row}(A) \perp \operatorname{Null}(A)$)
By definition of the nullspace, if $x \in \operatorname{Null}(A)$, then $Ax = 0$:
$$
\begin{bmatrix} r_1^T \\ r_2^T \\ \vdots \\ r_m^T \end{bmatrix} x = \begin{bmatrix} r_1 \cdot x \\ r_2 \cdot x \\ \vdots \\ r_m \cdot x \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \\ \vdots \\ 0 \end{bmatrix}
$$
Every vector $x \in \operatorname{Null}(A)$ is orthogonal to every row $r_i$ of $A$. Since $\operatorname{Row}(A)$ is the span of the rows, any $r \in \operatorname{Row}(A)$ satisfies:
$$
\langle r, x \rangle = 0 \implies \operatorname{Row}(A) \perp \operatorname{Null}(A)
$$

#### 2. Orthogonal $\implies$ Direct Sum
Because orthogonality guarantees that they share only the zero vector:
$$
\operatorname{Row}(A) \cap \operatorname{Null}(A) = \{0\}
$$
(If $v$ were in both, $\langle v, v \rangle = 0 \implies v = 0$).  
Therefore, their sum is automatically an orthogonal direct sum:
$$
\operatorname{Row}(A) \oplus^\perp \operatorname{Null}(A)
$$

#### 3. Dimension $\implies$ The Fundamental Theorem Decomposition
From the Rank-Nullity Theorem:
- $\dim(\operatorname{Row}(A)) = \operatorname{rank}(A) = r$
- $\dim(\operatorname{Null}(A)) = \operatorname{nullity}(A) = n - r$

Adding their dimensions:
$$
\dim(\operatorname{Row}(A)) + \dim(\operatorname{Null}(A)) = r + (n - r) = n = \dim(\mathbb{F}^n)
$$
Because they are orthogonal and their dimensions sum to the full dimension $n = \dim(\mathbb{F}^n)$, they span all of $\mathbb{F}^n$:
$$
\mathbb{F}^n = \operatorname{Row}(A) \oplus^\perp \operatorname{Null}(A)
$$
Hence, the nullspace is the unique orthogonal complement of the row space:
$$
\operatorname{Null}(A) = (\operatorname{Row}(A))^\perp
$$


---

Example 37:
Let $u=(1+i,i)$, $v=(1,i)$ such that $u,v\in \mathbb{C}^{2}$. Determine whether $u$ and $v$ are linearly independent over $\mathbb{C}$.

> [!warning]
> Let $a_{1},a_{2}\in \mathbb{C}$. Suppose 
> $$
> \begin{align}
> a_{1}u+a_{2}v&=0 \\
> a_{1}(1+i,i)+a_{2}(1,i)&=0 \\
> (a_{1}+(a_{1}+a_{2})i,(a_{1}+a_{2})i)&=0
> \end{align}
> $$
> 
> $$
> \begin{align}
> a_{1}+a_{2}+a_{1}i&=0+0i \\
> (a_{1}+a_{2})i&=0+0i
> \end{align}
> $$
> 
> It is wrong because $a_{1},a_{2}\in \mathbb{C}$, $a_{1},a_{2}$ itself  might contains imaginary part. Thus, we cannot take $a_{1}$ as real part and $(a_{1}+a_{2})$ as imaginary part.

Corrected version:

 Method 1: Direct System of Equation
The hypothesis give the system below:
$$
\begin{align}
a_{1}(1+i)+a_{2}&=0 &&(1)\\
a_{1}i+a_{2}i&=0 &&(2)
\end{align}
$$

From equation (2), divide by $i$ implies that $a_{1}=-a_{2}$.

Substitute $a_{1}=-a_{2}$ into (1), we get $a_{1}=0$. Thus, $a_{2}=0$.

> [!remark]
> First equation is from first coordinate while second equation is from second coordinate.

Method 2: Determinant 
2 vectors in $\mathbb{C}^{2}$ are linearly independent over $\mathbb{C}$ iff their determinant is non-zero

$$
\begin{bmatrix}
1+i &1 \\
i & i 
\end{bmatrix}= (1+i)(i)-(1)(i)=i-1+i=-1
$$
Since $\det \neq 0$, it follow that $\{ u,v \}$ is linearly independent over $\mathbb{C}$.

Example 38
let $u=(1+i,i)$, $v=(2+i,1)$, $w=(1,i)$, $x=(i,1)$ such that $u,v,w,x\in \mathbb{C}^{2}$. Determine whether these vector are linearly independent over $\mathbb{R}$.

Let $a,b,c,d\in \mathbb{R}$. Suppose
$$
\begin{align}
au+bv+cw+dx&=0 \\
a(1+i,i)+b(2+i,1)+c(1,i)+d(i,1)&=0
\end{align}
$$

We can form the system below by separating real and imaginary parts for each coordinate:
$$
\begin{align}
a+2b+c&=0 &&\text{(1st coord, Real)} \\
a+b+d&=0 &&\text{(1st coord, Imag)} \\
b+d&=0 &&\text{(2nd coord, Real)} \\
a+c&=0 &&\text{(2nd coord, Imag)}
\end{align}
$$

This is equivalent to the matrix equation $M \begin{bmatrix} a \\ b \\ c \\ d \end{bmatrix} = 0$:

$$
\begin{bmatrix}
1 & 2 & 1 & 0 \\
1 & 1 & 0 & 1 \\
0 & 1 & 0 & 1 \\
1 & 0 & 1 & 0
\end{bmatrix}
\begin{bmatrix}
a \\ b \\ c \\ d
\end{bmatrix}
=
\begin{bmatrix}
0 \\ 0 \\ 0 \\ 0
\end{bmatrix}
$$

> [!remark] Where the columns come from
> Each column represents a vector under the real basis $\mathcal{B} = \{(1, 0), (i, 0), (0, 1), (0, i)\}$:
> - **Col 1 ($u$):** $u = (1+i, i) \implies [1, 1, 0, 1]^T$
> - **Col 2 ($v$):** $v = (2+i, 1) \implies [2, 1, 1, 0]^T$
> - **Col 3 ($w$):** $w = (1, i) \implies [1, 0, 0, 1]^T$
> - **Col 4 ($x$):** $x = (i, 1) \implies [0, 1, 1, 0]^T$

### Solving the Matrix System:

**Method 1: Row Reduction (Gaussian Elimination)**
Perform $R_4 \to R_4 - R_1$:
$$
\begin{bmatrix}
1 & 2 & 1 & 0 \\
1 & 1 & 0 & 1 \\
0 & 1 & 0 & 1 \\
0 & -2 & 0 & 0
\end{bmatrix}
$$
- Row 4 immediately gives: $-2b = 0 \implies \mathbf{b = 0}$.
- Row 3 gives: $b + d = 0 \implies 0 + d = 0 \implies \mathbf{d = 0}$.
- Row 2 gives: $a + b + d = 0 \implies a + 0 + 0 = 0 \implies \mathbf{a = 0}$.
- Row 4 of original system gives: $a + c = 0 \implies 0 + c = 0 \implies \mathbf{c = 0}$.

Thus, row reducing leads directly to the identity matrix $I_4$, giving the unique trivial solution:
$$a = b = c = d = 0$$

**Method 2: Determinant**
Using cofactor expansion along the simplified 4th row (after $R_4 - R_1$):
$$
\det(M) = -2 \cdot (-1)^{4+2} \cdot \det \begin{bmatrix} 1 & 1 & 0 \\ 1 & 0 & 1 \\ 0 & 0 & 1 \end{bmatrix} = -2 \cdot (1) \cdot (-1) = 2 \neq 0
$$
Since $\det(M) \neq 0$, the matrix is invertible, so the only solution is the trivial solution:
$$a = b = c = d = 0$$

### Conclusion
Therefore, the vectors $\{u, v, w, x\}$ are **linearly independent over $\mathbb{R}$**. $\blacksquare$

