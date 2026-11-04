
Linear transformation is a function between 2 vector spaces over the same Field $F$ that preserve additivity and homogeneity.


# 3.2 Kernel and Image of a Linear Transformation

> [!theorem]  Proposition 3
> Let $T:V\to W$ be a linear transformation over $F$. Then $\ker(T)=\{ v\in V|T(v)=0 \}$, $\ker(T)$ is a subspace of $V$.

^a7467b

[[4.2 Nullspace Column space and row space#^bf7372]]

> [!theorem] Proposition 4
> Let $T:V\to W$ be a linear transformation over $F$. Then $\mathrm{Im}(T)=\{ T(v)\operatorname{|}v\in V \}$. $\mathrm{Im}(T)$ is a subspace of $W$.

Proof:
Suppose $T:V\to W$:
Since $V$ is a vector space, $0\in V$ and thus $T(0)=0\in \mathrm{Im}(T)$

Suppose $u\in \mathrm{Im}(T)$ and $w\in \mathrm{Im}(T)$. thus there exist $u_{1}\in V$ such that $T(u_{1})=u$ and $w_{1}\in V$ such that $T(w_{1})=w$. Hence, we have

$$
\begin{align}
u+w&=T(u_{1})+T(w_{1})=T(u_{1}+w_{1})
\end{align}
$$
Since $w_{1}+w_{2}\in V$, it follow that $u+w\in \mathrm{Im}(T)$.

For any $k\in F$, we have

$$
kw=kT(w_{1})=T(kw_{1})
$$
Since $kw_{1}\in V$, thus it follow that $kw\in \mathrm{Im}(T)$.

Hence it is a subspace. $\blacksquare$

> [!theorem] Theorem  ^cdce21
> 
> Let $V\to W$ be a linear transformation over $F$. Them $T$ is injective linear transformation iff $\ker(T)=\{ 0 \}$

Proof:
Forward direction:

> [!warning]
> Suppose $T$ is injective. Then for any $v_{1},v_{2}\in V$,  $T(v_{1})=T(v_{2})\implies v_{1}=v_{2}$. 
> $$
> \ker(T)=\{ v\in V| T(v)=0 \}
> $$
> Suppose $T(v_{1})=T(v_{2})$, then
> $$
> \begin{align}
> T(v_{1})-T(v_{2})&=0 \\ 
> T(v_{1}-v_{2})&= 0
> \end{align}
> $$
> Thus, by definition $v_{1}-v_{2}\in \ker(T)$. Since $v_{1}=v_{2}$, it follow that $v_{1}-v_{2}=0$. Hence $\ker(T)=\{ 0 \}$.

> [!question] What is the flaw of above proof?
> We suppose an element $v_{1},v_{2}$ such that $T(v_{1})=T(v_{2})$. It is unclear and not precise although they must me equal for us to compare. We must start with an element in $\ker(T)$ and show it must me 0.

The correct version should be 
Suppose $v_{1}\in \ker(T)$. Thus,
$$
\begin{align}
T(v_{1})&=0
\end{align}
$$
Since $T(0)=0$ we have
$$
T(v_{1})=T(0)
$$
And by injectivity it follow that $v_{1}=0$. Since any element $v_{1}\in \ker(T)$ must be 0, we conclude that $\ker(T)=\{ 0 \}$.$\blacksquare$

Backward direction:
Suppose $\ker(T)=\{ 0 \}$. Then, suppose $T(v_{1})=T(v_{2})$ for some $v_{1},v_{2}\in V$. Hence,
$$
\begin{align}
T(v_{1})-T(v_{2})&=0 \\
T(v_{1}-v_{2})&=0
\end{align}
$$
Thus, $v_{1}-v_{2}\in \ker(T)$. Since $\ker(T)=\{ 0 \}$. It follow that $v_{1}-v_{2}=0\implies v_{1}=v_{2}$.$\blacksquare$


> [!theorem]
> Let $T:V\to W$ be a linear transformation over $F$. Then $T$ is surjective linear transformation iff $\mathrm{Im}(T)=W$.

Proof:
Forward direction:
Suppose $T$ is surjective. Note that
$$
\mathrm{Im}(T)=\{ T(v)|v\in V \}
$$
It is clear that $\mathrm{Im}(T)\subseteq W$. Suppose $w_{1}\in W$ , then there exist $v_{1}\in V$ such that $T(v_{1})=w_{1}$. Hence, $w_{1}\in \mathrm{Im}(T)$. Hence, $W\subseteq \mathrm{Im}(T)$. Therefore, $\mathrm{Im}(T)=W$.

Backward direction:
Suppose $\mathrm{Im}(T)=W$. Assume $w_{1}\in W$, thus $w_{1}\in \mathrm{Im}(T)$. Hence, $w_{1}=T(v)$ for some $v\in V$. Hence, $T$ is surjective.$\blacksquare$

> [!theorem] Theorem (Inverse)
> Let $T:V\to W$ be an injective and surjective linear transformation over $F$. Then $T^{-1}$ exists and $T^{-1}$ is a linear transformation over $F$.

^0c422d

Proof:
We define $T(v)=w\iff T^{-1}(w)=v$.

Since $T$ is surjective, it follow that for every $w\in W$, there exist a $v\in V$ such that $T(v)=w\implies T^{-1}(w)=v$. 

Since $T$ is injective, it follow that for any $v_{1},v_{2}\in V$ $T(v_{1})=T(v_{2})\implies v_{1}=v_{2}$. Let $w_{1}=T(v_{1})\in W$ and $w_{2}=T(v_{2})\in W$. Hence $w_{1}=w_{2}\implies T^{-1}(w_{1})=T^{-1}(w_{2})$.
Hence, $T$ is a well defined function.

Closure under addition:
$$
\begin{align}
T^{-1}(w_{1}+w_{2})&=T^{-1}(T(v_{1}+v_{2})) \\
&=v_{1}+v_{2}\\
&=T^{-1}(w_{1})+T^{-1}(w_{2})
\end{align}
$$
Closure under scalar multiplication:
For any $k\in F$, we have
$$
\begin{align}
k(T^{-1}(w_{1}))&= kT^{-1}(T(v_{1})) \\
&=kv_{1} \\
&=T^{-1}(T(kv_{1})) \\
&= T^{-1}(kT(v_{1})) \\
&=T^{-1}(kw_{1})
\end{align}
$$
Thus $T^{-1}$ is a linear transformation $\blacksquare$

> [!theorem] Theorem 11
> Let $T:V\to W$ be a linear transformation over $F$. IF $V$ is finite dimensional, then $\dim(V)=\dim(\mathrm{Im}(T))+\dim(\ker(T))$.

Proof:
From Proposition 3 ![[Linear Transformation of Abstract Vector Spaces#^a7467b]]
We know that $\ker(T)$ is a subspace of $V$. Suppose $\{ v_{1},\dots,v_{k} \}$ is the basis for $\ker(T)$. Then $k\leq \dim(V)$. By Spanning Set Theorem, it can be extend to the basis for $V$ by adding $\{ u_{1},\dots,u_{m} \}$ so that $\{ v_{1},\dots,v_{k},u_{1},\dots,u_{m} \}$ forms a basis for $V$.

Hence for any $x\in V$, there exist some $c_{_{i}}$ and $d_{j}$ such that

$$
\begin{align}
x&=\sum_{i=1}^{k} c_{i}v_{i}+\sum_{j=1}^{m} d_{j}u_{j}
\end{align}
$$
We apply $T$ on both side:
$$
\begin{align}
T(x)&= T\left( \sum_{i=1}^{k} c_{i}v_{i}+\sum_{j=1}^{m} d_{j}u_{j} \right) \\
&=T\left( \sum_{i=1}^{k} c_{i}v_{i} \right)+ T\left( \sum_{j=1}^{m} d_{j}u_{j} \right) \\
\end{align}
$$

Note that $\sum_{i=1}^{k}c_{i}v_{i}\in \ker(T)$. Hence $T\left( \sum_{i=1}^{k}c_{i}v_{i} \right)=0$. Hence,

$$
\begin{align}
T(x)&=T \left( \sum_{j=1}^{m} d_{j}u_{j} \right) \\
&=\sum_{j=1}^{m} d_{j}T(u_{j})
\end{align}
$$

Note that $T(x)$ is an arbitrary element in $\mathrm{Im}(T)$ and it span by $\{ T(u_{1}),\dots,T(u_{j}) \}$. 

Check the linear dependency:
$$
\begin{align}
d_{1}T(u_{1})+\dots+d_{m}T(u_{m})&=0 \\
T(d_{1}u_{1}+\dots+d_{m}u_{m})&=0
\end{align}
$$
Hence, by definition $d_{1}u_{1}+\dots+d_{m}u_{m}\in \ker(T)$.  Since $\{ v_{1},\dots,v_{k} \}$ is a basis for $\ker(T)$. If follow that there exist some unique $c_{1},\dots,c_{k}$

$$
\begin{align}
d_{1}u_{1}+\dots+d_{m}u_{m}&=c_{1}v_{1}+\dots+c_{k}v_{k} \\
d_{1}u_{1}+\dots+d_{m}u_{m}- (c_{1}v_{1}+\dots+c_{k}v_{k})&=0
\end{align}
$$
Since $\{ v_{1},\dots,v_{k},u_{1},\dots,u_{m} \}$ is a basis for $V$. it follow that $d_{1}=\dots=d_{m}=c_{1}=\dots=c_{k}=0$. Hence, $\{ T(u_{1}),\dots,T(u_{m}) \}$ is linearly independent. 

Hence $\dim(\mathrm{Im}(T))=m$, $\dim(\ker(T))=k$ and $\dim(V)=k+m$. Therefore,

$$
\begin{align}
\dim(\mathrm{Im}(T))+\dim(\ker(T))=\dim(V) \tag*{$\blacksquare$}
\end{align}
$$


> [!remark]
> Think of $Ax=0$. The vector $x$ (each entry of $x$ is the weight of column of $A$) that being map to $0$ is a subspace, thus it can be express as linear span of some linearly independent vector set which is basis. (The basis is obtained by identifying the free variable )

Remark:

> [!question]  Why we cannot write $\{ u_{1},\dots,u_{m} \}$ is linearly independent implies that $\{ T(u_{1}),\dots,T(u_{m}) \}$ is linearly independent?
> 
> ![[4.4 Coordinate System#^65dae4]]
> 
> We need the condition that $T$ is one-to-one to write this argument. 
> 
> So what is the difference here? Why we still manage to prove that $\{ T(u_{1}),\dots,T(u_{m}) \}$ is linearly independent even though $T$ might not one-to-one?
> 
> The key is that we did not pick any arbitrary independent set- we picked the extension vector outside the kernel. Think about this, the theorem need one-to-one because given random linearly independent vector set, it might exist that  linear combination of some vectors in the set is in the kernel!!! For example,
> Let say $T(1,0,0)=0$ and $T(0,1,0)=0$. And 
> $$
> \ker(T)=Span\{ (1,0,0),(0,1,0) \}
> $$
> because it is always a subspace, and the smallest subspace that containing the vector is the spanning set of the vector.
> 
> Now, note that $\{ (2,5,0),(1,1,1) \}$ is linearly independent. Hence,
> 
> $$
> \begin{align}
> c_{1}(2,5,0)+c_{2}(1,1,1)&=0 \\
> c_{1}T(2,0,0)+c_{1}T(0,5,0)+c_{2}T(1,1,1)&=0
> \end{align}
> $$
> 
> Note that the first 2 term is in kernel of $T$. Hence, $c_{1}$ can be any real number!!!
> 
> In the theorem we prove earlier since $\{ v_{1},\dots,v_{k},u_{1},\dots,u_{m} \}$ is a basis of $V$, no non-trivial combination of $\{ u_{1},\dots,u_{m} \}$ can produce a vector in $\ker(T)$. In other words, $U\cap \ker(T)=\{ 0 \}$. So while $T$ is not one-to-one on the whole space $V$, it is strictly one-to-one when restricted to the subspace $U=\operatorname{span}\{ u_{1},\dots,u_{m} \}$. 

---

### Alternative Viewpoint: The Direct Sum ($\oplus$) Approach

We can understand the Theorem cleanly through the concept of an **internal direct sum**:

Let $U = \operatorname{span}\{u_1, \dots, u_m\}$ be the subspace spanned by the extension basis vectors. Because $\{v_1, \dots, v_k\}$ is a basis for $\ker(T)$ and $\{v_1, \dots, v_k, u_1, \dots, u_m\}$ is a basis for $V$:

1. **Spanning**: $V = \ker(T) + U$ (every $x \in V$ can be written as $x = v + u$ where $v \in \ker(T)$ and $u \in U$).
2. **Trivial Intersection**: $\ker(T) \cap U = \{0\}$ (because the combined basis vectors are linearly independent).

Therefore, $V$ decomposes into a direct sum:
$$V = \ker(T) \oplus U \implies \dim(V) = \dim(\ker(T)) + \dim(U)$$

Now examine the **restriction map** $T|_U : U \to \mathrm{Im}(T)$ (read as *"$T$ restricted to $U$"*):

> [!note] Notation: Function Restriction ($T|_U$)
> Normally, $T: V \to W$ accepts inputs from the whole space $V$. The notation $T|_U$ means we keep the exact same transformation rule, but **restrict its domain** strictly to inputs from the subspace $U$ (vectors from the kernel are not allowed as inputs).
> - While $T$ is not one-to-one on all of $V$, restricting its inputs to $U$ eliminates all non-trivial kernel vectors, making $T|_U$ strictly one-to-one!

- **Injective (one-to-one)**: $\ker(T|_U) = U \cap \ker(T) = \{0\}$.
- **Surjective (onto)**: For any $w = T(x) \in \mathrm{Im}(T)$, decomposing $x = v + u$ yields $T(x) = T(v) + T(u) = 0 + T(u) = T(u)$, so every image element is reached from $U$.

Since $T|_U$ is a linear bijection (an **isomorphism** between $U$ and $\mathrm{Im}(T)$), it preserves dimension:
$$\dim(U) = \dim(\mathrm{Im}(T))$$

Substituting $\dim(U) = \dim(\mathrm{Im}(T))$ into the direct sum formula immediately gives:
$$\dim(V) = \dim(\ker(T)) + \dim(\mathrm{Im}(T))$$

---

### Synthesis: Basis Approach vs. Direct Sum Approach

At their core, both approaches execute the **exact same fundamental strategy**: they split the domain $V$ into two non-overlapping pieces:
1. **The piece that collapses to $\mathbf{0}$**: the kernel ($\ker(T)$).
2. **The piece that survives with zero information loss**: the complementary part ($U = \operatorname{span}\{u_1, \dots, u_m\}$).

#### The Role of $U \cap \ker(T) = \{\mathbf{0}\}$ in Both Approaches:
The condition $U \cap \ker(T) = \{\mathbf{0}\}$ is the decisive linchpin in both proofs, viewed through two different lenses:

##### 1. Approach 1: Basis Extension (Bottom-Up)
- **Core Focus**: Vector & basis level ($\{v_i\}$ vs $\{u_j\}$).
- **How $U \cap \ker(T) = \{\mathbf{0}\}$ is used**:  
  Shows that if a linear combination lands in the kernel:
  $$d_1 u_1 + \dots + d_m u_m \in \ker(T) \implies d_1 u_1 + \dots + d_m u_m = \mathbf{0}$$
  which forces all coefficients $d_j = 0$, proving that $\{T(u_1), \dots, T(u_m)\}$ is **linearly independent**.
- **Matching the Dimension**: Counts basis elements: $m$ linearly independent vectors span $\mathrm{Im}(T) \implies \dim(\mathrm{Im}(T)) = m$.

##### 2. Approach 2: Direct Sum (Top-Down)
- **Core Focus**: Subspace & mapping level ($\ker(T)$ vs $U$).
- **How $U \cap \ker(T) = \{\mathbf{0}\}$ is used**:  
  Directly proves that the kernel of the restricted map is trivial:
  $$\ker(T|_U) = U \cap \ker(T) = \{\mathbf{0}\}$$
  which shows that $T|_U$ is **one-to-one (injective)**.
- **Matching the Dimension**: Uses the isomorphism: $T|_U : U \to \mathrm{Im}(T)$ is an isomorphism $\implies \dim(U) = \dim(\mathrm{Im}(T))$.

> [!important] The Unifying Principle
> One focuses on the **basis**, while the other focuses on the **isomorphism** to match the dimension. 
> These are two sides of the exact same theorem:
> $$\text{A linear map } T|_U: U \to \mathrm{Im}(T) \text{ is an isomorphism } \iff \text{it maps a basis of } U \text{ to a basis of } \mathrm{Im}(T).$$


---

### Why Orthogonality is NOT Needed (and Why It Is Overkill)

When studying matrices in $\mathbb{R}^n$, we often see the **Fundamental Theorem of Linear Algebra**:
$$\mathbb{R}^n = \ker(A) \oplus (\ker(A))^\perp = \ker(A) \oplus \mathrm{Row}(A)$$
where the null space and row space are **orthogonal complements** ($\ker(A) \perp \mathrm{Row}(A)$).

While this geometric picture works in Euclidean space $\mathbb{R}^n$, using orthogonality for general Theorem 11 is **overkill and conceptually insufficient**:

1. **No Inner Product Structure on General $V$**:
   Theorem 11 holds for **any** vector space $V$ over **any** field $F$ (e.g., function spaces, polynomial spaces, or finite fields $\mathbb{Z}_p$). An abstract vector space only defines vector addition and scalar multiplication—it does **not** have an inner product (dot product $\langle u, v \rangle$). Without an inner product, concepts like "angles", "lengths", and "orthogonal" ($u \cdot v = 0$) **do not exist**.
   
2. **Orthogonality is Unnecessary Extra Geometry**:
   To form a direct sum $V = \ker(T) \oplus U$, we do **not** need the complement $U$ to be *perpendicular* to $\ker(T)$. We only need:
   - $V = \ker(T) + U$
   - $\ker(T) \cap U = \{0\}$
   
   Any complementary subspace $U$ constructed via **basis extension** fulfills this using only linear independence.

> [!summary] Key Takeaway
> **Orthogonality** is a *metric/geometric* concept that requires an inner product space. **Rank-Nullity and Direct Sum** are purely *algebraic* concepts that hold across every abstract vector space over any field $F$.
 

> [!theorem] Theorem 12
> Let $T:V\to W$ be a linear transformation over $F$. Let $\dim V=\dim W$. Then $T$ is injective iff $T$ is surjective.

Proof:
Forward direction:
Suppose $\dim V=\dim W$ and $T$ is injective. Hence, by theorem above it follow that $\ker(T)= \{ 0 \}$. We need to show that $\mathrm{Im}(T)=W$. Form theorem 11 we know that
$$
\begin{align}
\dim V&=\dim( \ker(T))+\dim(\mathrm{Im}(T)) \\
\dim W&=0+\dim(\mathrm{Im}(T)) \\
\dim W&=\dim(\mathrm{Im}(T))
\end{align}
$$
We know that $\mathrm{Im}(T)\subseteq W$. We need to show $W\subseteq \mathrm{Im}(T)$. Suppose $B=\{ v_{1},\dots,v_{k} \}$ is a basis for $\mathrm{Im}(T)$. Since $v_{i}\in W$ for $i\in\{ 1,\dots,k \}$ and $\dim W=\dim(\mathrm{Im}(T))$, it follow that by The Basis Theorem $B$ is also a basis for $W$. Hence, for any $w_{1}\in W$, it follow that
$$
w_{1}\in Span(B)=\mathrm{Im}(T)
$$
Therefore, $W\subseteq \mathrm{Im}(T)\implies W=\mathrm{Im}(T)$. Hence, $T$ is surjective $\blacksquare$

Backward direction:
Suppose $T$ is surjective. Then, $\mathrm{Im}(T)=W$. By theorem 11, it follow that

$$
\begin{align}
\dim V &= \dim (\ker(T))+\dim(\mathrm{Im}(T)) \\
\dim W&= \dim(\ker(T))+\dim(\mathrm{Im}(T)) \\
\dim(\ker (T))&=0
\end{align}
$$
Hence $\ker(T)=\{ 0 \}$ and thus $T$ is injective.$\blacksquare$

> [!remark]
> It is easy to understand if we view $T$ as a matrix multiplication, suppose $A$ is a $n\times n$ matrix then by invertible theorem. the statement is true
>
>And we use theorem 11 here, because it link dimension of Image and Kernel together (Bridge surjective and injective)

# Some Operations with Linear Transformation

We can combine linear transformation to obtain new linear transformations.

Let $F:V\to W$ and $G:V\to W$ be linear transformations over $F$. (There must have same domain and codomain)

$F+G:V\to W$ is defined to be $(F+G)(v)=F(v)+G(v)$. Also $(kF)(v)=k(F(v))$ where $k\in \mathbb{F}$.

If $F,G$ linear, then $F+G$ and $kF$ also linear.

> [!theorem] Theorem 13
> Let $F,G:V\to W$ be linear transformation over $\mathbb{F}$ and $k,r\in \mathbb{F}$. Then $kF+rG:V\to W$ such that $(kF+rG)(v)=kF(v)+rG(v)$ is a linear transformation over $\mathbb{F}$.


Theorem
If we have composition of linear transformations
$$
V \overset{F}{\to} U \overset{G}{\to}W
$$
with $F:V\to U$ and $G:U\to W$. Then $G\circ F$ is the linear transformation from $V$ to $W$ defined by $(G\circ F)(v)=G(F(v))$

Proof:
Suppose $v,w\in V$ and $a,b\in \mathbb{F}$,

$$
\begin{align}
G\circ F(av+bw)&= G(F(av+bw)) \\
&=G(aF(v)+bF(w)) \\
&=aGF(v)+bG(F(w)) \\
&=a(G\circ F)(v)+b(G\circ F)(w)
\end{align}
$$

Therefore, $G\circ F$ is linear. $\blacksquare$

> [!definition] Definition 16
> A linear transformation $T$ from $V$ to $W$ is called invertible if there exist a mapping $U$ from $W$ to $V$ such that $UT$ is an identity mapping on $V$ and $TU$ is an identity mapping on $W$.
> 
> If $T$ is invertible, the mapping $U$ is unique and denoted as $T^{-1}$. Furthermore $T$ is invertible iff
> 
> a) $T$ is one to one
> b) $T$ is onto
> 
> Another wat to define:
> [[2.3 Characterizations of Invertible Matrices#^089f42]]

Since such inverse mapping is unique and linear transformation. We have the theorem below:

[[Linear Transformation of Abstract Vector Spaces#^0c422d]]


# Isomorphism of vector spaces over $\mathbb{F}$

If $V$ and $W$ are isomorphic $V\cong W$, it means that they are distinguishable in the sense of what is true about $V$ is also true for $W$ and vice versa.

> [!definition] Definition 17
> If a linear transformation $T$ is one to one and onto, then $T$ is called an isomorphism.

> [!definition] Definition 18
> Two vectors spaces $V,W$ over $\mathbb{F}$ are said to be isomorphic over $\mathbb{F}$, denoted $V\cong W$ if there exists an isomorphism $T$ from $V$ to $W$.

> [!remark]
> $V\cong W$ and $W\cong V$ are equivalent statement, since isomorphism $T$ is bijective, there exist $T^{-1}$ which is also a bijective linear transformation.

Exercise
a) Let $V=\mathbb{C}^{3}$ and $W=P_{2}(\mathbb{C})$ be vector spaces over $\mathbb{C}$. Define $T:V\to W$ such that $T(a_{0},a_{1},a_{2})=a_{0}+a_{1}x+a_{2}x^{2}$. Determine whether $V$ and $W$ are isomorphic.

To show $V\cong W$, we need to show there exist an isomorphism $T$. 
1) $T$ is linear transformation from $V\to W$
2) $T$ is bijective

Check additivity:
Let $v_{1}=(a_{1},b_{1},c_{1})\in V$ and  $v_{2}=(a_{2},b_{2},c_{2})\in V$. Hence,
$$
\begin{align}
T(v_{1}+v_{2})&=(a_{1}+a_{2})+(b_{1}+b_{2})x+(c_{1}+c_{2})x^{2} \\
&=(a_{1}+b_{1}x+c_{1}x)+(a_{2}+b_{2}x+c_{2}x^{2}) \\
&= T(v_{1})+T(v_{2})
\end{align}
$$

Check homogeneity:
Let $c\in \mathbb{C}$. Hence,

$$
\begin{align}
cT(v_{1})&=c(a_{1}+b_{1}x+c_{1}x^{2}) \\
&=ca_{1}+c b_{1}x+cc_{1}x^{2} \\
&=T(cv_{1})
\end{align}
$$
Hence, $T$ is a linear transformation.

Check if $T$ is one to one:
$$
\begin{align}
\ker(T)&=\{ v\in V\mid  T(v)=0 \} \\
&=\{ (a_{1},b_{1},c_{1})\mid  a_{1}+b_{1}x+c_{1}x^{2}=0 \} \\
&=\{ (0,0,0) \}
\end{align}
$$

Since $\ker(T)=\{ 0 \}$, then $T$ is one to one. 


Check if $T$ is onto:
$$
\begin{align}
\mathrm{Im}(T)&=\{ T(v)\in W \mid v\in V \} \\
&=\{ T((a_{1},b_{1},c_{1}))\mid (a_{1},b_{1},c_{1})\in V\} \\
&=\{a_{1}+b_{1}x+c_{1}x^{2}\mid a_{1},b_{1},c_{1}\in \mathbb{C}  \} \\
&= P_{2}(\mathbb{C})
\end{align}
$$

Hence, it is onto. Therefore, $T$ is bijective and thus it is isomorphism. Hence, $\mathbb{C}^{3} \cong P_{2}(\mathbb{C})$. $\blacksquare$

> [!remark] 
> If $V=\mathbb{C}^{3}$ over $\mathbb{R}$, then $V=\{ (a_{0}+a_{1}i,a_{2}+a_{3}i,a_{4}+a_{5}i) \mid a_{k}\in \mathbb{R}\text{ for }k=0,\dots,5\}$ 
> 
> Why we write like this?
> To reveal the standard basis $\{ (1,0,0),(i,0,0),(0,1,0),(o,i,0),(0,0,1),(0,0,i) \}$

# Linear Extension

^deab0e

> [!theorem] Theorem (Linear Extension Theorem)
> Let $V$ and $W$ be vector spaces over the same field $\mathbb{F}$.  
> Let $B = \{v_1, v_2, \dots, v_n\}$ be an ordered basis of $V$, and let $\{w_1, w_2, \dots, w_n\}$ be any arbitrary vectors in $W$.
> 
> Then there exists a **unique** linear transformation $T: V \to W$ such that:
> $$T(v_i) = w_i \quad \text{for all } i \in \{1, 2, \dots, n\}$$

> [!note] Why is it Called an "Extension"?
> In mathematics, if a function $f: B \to W$ is defined only on a subset $B \subset V$, an **extension** of $f$ to the larger set $V$ is a function $T: V \to W$ that agrees with $f$ on $B$ (that is, $T|_B = f$).
> 
> 1. **Start with a raw assignment on the basis:** $f: B \to W$ sends $v_i \mapsto w_i$. Notice that $f$ is just a set map—no linearity is required.
> 2. **Extend it to the entire space:** The theorem guarantees that this raw assignment can be uniquely **extended** to a full **linear transformation** $T$ defined on all of $V$.

> [!note] General Statement (Universal Property of a Basis)
> The theorem also holds when $V$ is infinite-dimensional:
> Let $B$ be any basis of $V$, and let $f: B \to W$ be any function. Then there exists a unique linear transformation $T: V \to W$ such that:
> $$T|_B = f$$

Given (Hypothesis):
1) $B=\{ v_{1},\dots,v_{n} \}$ is a ordered basis for $V$
2) $\{ w_{1},\dots,w_{n} \}$ are any order vectors set in $W$

To prove (Conclusion): There exists a map $T:V\to W$ such that:
1) $T(v_{i})=w_{i}$ for each $i$
2) $T$ is a linear transformation
3) $T$ is unique

Proof:
Step A: Define the candidate map
For any $v\in V$, there exist unique $c_{i}$ such that
$$
v=\sum_{i=1}^{n} c_{i}v_{i}
$$
Since $B$ is a basis. these coefficient $(c_{1},\dots,c_{n})$ exist (spanning) and are unique (linear independence). Therefore, we can legitimately define a function $T:V\to W$

$$
T(v)=\sum_{i=1}^{n} c_{i}w_{i}
$$
for some $\{ w_{1},\dots,w_{n} \}\in W$. t 

> [!question] Why it is a well defined function?
> Here is the reason why we need it to be a Basis in the domain $V$.
> 1) Total Assignment:
> Because $Span(B)=V$, every vector $v\in V$ can be written as:
> 
> $$
> v=\sum_{i=1}^{n} c_{i}v_{i}
> $$
> for some scalar $c_{1},\dots,c_{n}\in \mathbb{F}$. Since $W$ is closed under scalar multiplication and addition, $\sum_{i=1}^{n}c_{i}w_{i}$ is a vector in $W$. Therefore, every $v\in V$ has an image.
> 
> 2) Uniqueness: 
> Since $c_{1},\dots,c_{n}$ is unique, it follow that for any $v\in V$, the representation is unique and thus the case where $v$ have 2 representation and map to different image is impossible.

Step B: Verify the condition $T(v_{i})=w_{i}$

The coordinate vector $v_{1}$ has $c_{1}=1$ and all other $c_{j}=0$. By our definition:
$$
T(v_{1})=1w_{1}+0w_{2}+\dots+0w_{n}=w_{1}
$$
This holds for all $i=1,\dots,n$.

> [!question] Why can't we just declare $T(v_{i})=w_{i}$
> 1) Domain Mismatch (Points vs The Whole Space)
> A linear transformation must be a function defined on the entire domain:
> $$
> T:V\to W
> $$
> $\{ v_{1},\dots,v_{n} \}$ is just a set containing $n$ individual vectors. Writing $T(v_{i})=w_{i}$ only tells us what $T$ map those $n$ specific points. It does not tell you how to map any generic vector $v\in V$.
> 
> It only map a finite set $\{ v_{1},\dots,v_{n} \}$ rather than the whole vector space $V$.
> 
> 2) Why the Candidate formula $T(v)=\sum_{i=1}^{n}c_{i}w_{i}$?
> If a linear transformation $T$ were to exist satisfying $T(i)=w_{i}$ means that
> $$
> T(v)= T\left( \sum_{i=1}^{n} c_{i}v_{i} \right)=\sum_{i=1}^{n} c_{i}T(v_{i})=\sum_{i=1}^{n} c_{i}w_{i}
> $$
> 
> This show that if such $T$ exists, it is forced to have this exact formula. (It is like reverse engineering)

Step C: Prove that $T$ is a linear transformation 
Let $u=\sum_{i=1}^{n}a_{i}v_{i}$ and $v=\sum_{i=1}^{n}b_{i}v_{i}$. Then,

$$
u+av=\sum_{i=1}^{n} (a_{i}+\alpha b_{i})v_{i}
$$

Hence,
$$
\begin{align}
T(u+av)&=T\left( \sum_{i=1}^{n} (a_{i}+\alpha b_{i}) v_{i}\right) \\
&= \sum_{i=1}^{n} (a_{i}+\alpha b_{i})w_{i} \\
&= \sum_{i=1}^{n} a_{i}w_{i}+ \alpha\sum_{i=1}^{n} b_{i}w_{i} \\
&= T(u)+\alpha T(v)
\end{align}
$$
Therefore $T$ is linear.

Step D: Prove that $T$ is unique
Suppose there exist another linear transformation $S:V\to W$ such that
$$
\begin{gathered}
S(v_{i})=w_{i} &&\text{for all }i\in \{ 1,2,\dots,n \}
\end{gathered}
$$

For any $v\in V$, 
$$
v=\sum_{i=1}^{n} c_{i}v_{i}
$$
Hence,
$$
\begin{align}
S(v)&=S\left( \sum_{i=1}^{n} c_{i}v_{i} \right) \\
&= \sum_{i=1}^{n} c_{i}w_{i} \\
&= T(v) \tag*{$\blacksquare$}
\end{align}
$$


> [!remark]
> This have shown that if $S(v_{i})=T(v_{i})$ for all basis vectors $v_{i}$, then $S=T$ 
> 
> Whenever we need to prove that 2 complicated linear transformation are identical, we just need to check where it sends a basis. **A linear transformation is uniquely determined by where it sends a basis**.
> 
> This is also the reason why a matrix $A=\begin{bmatrix}T(v_{1}) & \dots & T(v_{n})\end{bmatrix}$ only represent one and only one linear transformation $T$. See remark below for more detail on matrix

---

### Purpose of the Linear Extension Theorem

The Linear Extension Theorem is the backbone of linear algebra. Its practical and theoretical purposes include:

#### 1. Compressing Infinite Information into Finite Data
A vector space $V$ over $\mathbb{R}$ or $\mathbb{C}$ contains **infinitely many vectors**. 
Normally, specifying an arbitrary function $f: V \to W$ requires describing what happens to infinitely many points.

The Linear Extension Theorem says:
> **Linear maps are rigid.** You do not need to describe what $T$ does to infinitely many vectors. You only need to choose the destinations of the $n$ basis vectors $\{v_1, \dots, v_n\}$, and the behavior on the entire infinite space is completely and uniquely fixed.

#### 2. Absolute Freedom of Choice (No Contradictions)
Can you pick *any* targets $w_1, \dots, w_n \in W$?
* Do the $w_i$'s need to be linearly independent? **No.**
* Do the $w_i$'s need to span $W$? **No.**
* Can all $w_i = \mathbf{0}$? **Yes** (that yields the zero transformation).
* Can $w_1 = w_2$? **Yes.**

The theorem guarantees that **no matter what choices you make for $\{w_1, \dots, w_n\}$**, you will never create a mathematical contradiction with linearity. A unique, valid linear map is guaranteed to exist.

#### 3. It Justifies the Existence of Matrices
Whenever you write down an $m \times n$ matrix $A$ to represent a linear map, the columns of $A$ are simply the coordinates of the target vectors:
$$
A = \begin{bmatrix} | & | & & | \\ T(v_1) & T(v_2) & \cdots & T(v_n) \\ | & | & & | \end{bmatrix}
$$

^fceb18

Why are we allowed to associate any arbitrary grid of numbers with a legitimate linear transformation? 
**Because of the Linear Extension Theorem.** It guarantees that specifying the image of the basis vectors gives a legitimate, globally consistent linear transformation on the whole space.

![[1.9 The Matrix of a Linear Transformation#^22baa7]]

Combine these 2 we have 1 linear transformation $\iff$ 1 unique matrix.

---
## Biconditional statement for Surjective and Injective 

> [!theorem] Proposition 5
> Let $\{ v_{1},\dots,v_{n} \}$ be vectors in the vector space $V$. Let $e_{1},\dots,e_{n}\in \mathbb{R}^{n}$ be the standard basis and $T:\mathbb{R}^{n}\to V$ the linear extension of $T(e_{i})=v_{i}$, for $i=1,2,\dots,n$. Then $\{ v_{1},\dots,v_{n} \}$ are linearly independent iff $\ker(T)=\{ 0 \}$

Proof:
Forward direction:
Suppose $\{ v_{1},\dots,v_{n} \}$ is linearly independent. Then 
$$
c_{1}v_{1}+\dots+c_{n}v_{n}=0
$$
implies that $c_{1}=\dots=c_{n}=0$. 
$$
\begin{align}
\ker(T)&=\{ r\in \mathbb{R}^{n}\mid T(r)=0 \} \\
&=\{ (c_{1},\dots,c_{n})\in \mathbb{R}^{n}\mid  c_{1}v_{1}+\dots+c_{n}v_{n}=0 \} \\
&=\{ 0 \}
\end{align}
$$

Backward direction:
Suppose $\ker(T)= \{ 0 \}$. Assume
$$
\begin{align}
c_{1}v_{1}+\dots+c_{n}v_{n}&=0 \\
T(r)&=0
\end{align}
$$
Since $r=(c_{1},\dots,c_{n})\in \ker(T)$, thus it follow that $c_{1}=\dots=c_{n}=0$. Hence, $\{ v_{1},\dots,v_{n} \}$ is linearly independent. $\blacksquare$

> [!remark]
> From earlier theorem we chose random vector in codomain but this time we choose a linearly independent set and it result in one to one because $\ker(T)$ is depend on the vector set in $V$

> [!theorem] Proposition 6
> Let $\{ v_{1},\dots,v_{n} \}$ be vectors in the vector space $V$. Let $e_{1},\dots,e_{n}\in \mathbb{R}^{n}$ be the standard basis and $T:\mathbb{R}^{n}\to V$ the linear extension of $T(e_{i})=v_{i}$, for $i=1,2,\dots,n$. Then $\{ v_{1},\dots,v_{n} \}$ span $V$ iff $\mathrm{Im}(T)=V$

Proof:
Suppose $\{ v_{1},\dots,v_{n} \}$ span $V$. Thus, 
$$
\begin{align}
\mathrm{Im}(T)&=\{ T(r)\mid r\in \mathbb{R}^{n} \} \\
&=\{ c_{1}v_{1}+\dots+c_{n}v_{n}\mid  (c_{1},\dots,c_{n})\in \mathbb{R}^{n} \} \\
&= Span \{ v_{1},\dots,v_{n} \} \\
&=V
\end{align}
$$
The backward direction will be since $\{ v_{1},\dots,v_{n} \}$ span $\mathrm{Im}(T)$ and $\mathrm{Im}(T)=V$, it follow that $\{ v_{1},\dots,v_{n} \}$ span $V$.$\blacksquare$

> [!remark]
> $\{ v_{1},\dots,v_{n} \}$ is basis for $V$ iff $T$ is bijective, this require their dimension are the same

### Example
Using Linear Extension method, show that vector spaces $\mathbb{C}^{2}$ over $\mathbb{C}$ and $M_{2\times1}(\mathbb{C})$ over $\mathbb{C}$ are isomorphic.

Step 1: Choose Bases for Both Spaces
For the domain $V=\mathbb{C}^{2}$ over $\mathbb{C}$, consider the standard basis
$$
B=\{ e_{1},e_{2} \}
$$
where $e_{1}=(1,0)$ and $e_{2}=(0,1)$.

For the codomain $W=M_{2\times 1}(\mathbb{C})$ over $\mathbb{C}$, consider the standard basis
$$
B'=\{ E_{1},E_{2} \}
$$
where $E_{1}=\begin{pmatrix}1 \\  0 \end{pmatrix}$ and $E_{2}=\begin{pmatrix}0 \\  1\end{pmatrix}$.

Step 2: Construct Linear Map via Linear Extension
By the Linear Extension Theorem, given the basis $B=\{ e_{1},e_{2} \}$ of $\mathbb{C}^{2}$ and arbitrary vectors set $\{ E_{1},E_{2} \}\in M_{2\times 1}(\mathbb{C})$, there exist a unique linear transformation $T:V\to W$ such that
$$
\begin{gathered}
T(e_{1})=E_{1} &&T(e_{2})=E_{2}
\end{gathered}
$$

For any $z=(z_{1},z_{2})\in \mathbb{C}^{2}$, we have unique representation with respect to $B$:
$$
z=z_{1}e_{1}+z_{2}e_{2}
$$
Applying $T$ gives the explicit formula:

$$
\begin{align}
T(z)&=T(z_{1}e_{1}+z_{2}e_{2}) \\
&=z_{1}T(e_{1})+z_{2}T(e_{2}) \\
&= z_{1} \begin{pmatrix}
1 \\
0 
\end{pmatrix}+z_{2} \begin{pmatrix}
0 \\
1
\end{pmatrix} \\
&= \begin{pmatrix}
z_{1} \\
z_{2}
\end{pmatrix}
\end{align}
$$
By Linear Extension Theorem, $T$ is well defined and linear.

Step 3: Show that $T$ is an isomorphism (Bijective)

Injectivity:
Suppose $T(z_{1},z_{2})=\begin{pmatrix}0 \\  0\end{pmatrix}$. Thus, 

$$
\begin{pmatrix}
z_{1} \\
z_{2}
\end{pmatrix}= \begin{pmatrix}
0 \\
0
\end{pmatrix}\implies z_{1}=0,z_{2}=0
$$

Hence, $\ker(T)=\{  0 \}$, $T$ is injective.

Surjectivity:
$$
\begin{align}
\mathrm{Im}(T)&=\{ T(z)\mid z\in \mathbb{C}^{2} \} \\
&=\{ \begin{pmatrix}
z_{1} \\
z_{2}
\end{pmatrix}\mid  (z_{1},z_{2})\in \mathbb{C}^{2} \} \\
&= \{ z_{1}\begin{pmatrix}
1 \\
0
\end{pmatrix}+z_{2} \begin{pmatrix}
0 \\
1
\end{pmatrix}\mid  z_{1},z_{2}\in \mathbb{C} \} \\
&= Span \{ E_{1},E_{2} \} \\
&= V
\end{align}
$$
Thus, $T$ is surjective. Hence, $\mathbb{C}^{2}\cong M_{2\times 1}(\mathbb{C})$ over $\mathbb{C}$. $\blacksquare$

---

### Practical Use vs. Formal Proof: Why the Order Flips

> [!insight] The Contrast: Practice vs. Theory
> Notice what we just did in **Step 2** of the example above:
> - **In Practice (Forward Construction):** We started with where we wanted the basis to land:
>   $$T(e_1) = E_1, \quad T(e_2) = E_2$$
>   and then **extended** it to the entire space via linearity:
>   $$T(z_1 e_1 + z_2 e_2) = z_1 T(e_1) + z_2 T(e_2) = \begin{pmatrix} z_1 \\ z_2 \end{pmatrix}$$
>   We specified only $2$ basis outputs, and automatically unlocked the explicit formula for **all infinitely many vectors** in $\mathbb{C}^2$!
> 
> - **In the Formal Proof (Reverse Verification):** The order was completely flipped:
>   1. We first proposed the candidate formula $T(v) = \sum_{i=1}^n c_i w_i$ out of nowhere for all $v \in V$.
>   2. Then we verified that it satisfies $T(v_i) = w_i$.

#### Why can't the formal proof do it the practical way?
If a formal proof simply stated:
> *"Let $T(v_i) = w_i$, and now extend it to all $v$ by linearity: $T(\sum c_i v_i) = \sum c_i T(v_i)$..."*

A mathematician would object:
> 🚫 **Logical error (Begging the question):** You cannot invoke the *linearity* of $T$ yet, because $T$ does not even legally exist as a well-defined function on $V$! You cannot use a property of an object before defining the object itself.


> [!summary] Key Takeaway
> The **Linear Extension Theorem is the legal permit** that justifies the practical method:
> Because the theorem has already been rigorously proven once and for all, in practice and applications we are **legally allowed** to specify just the basis targets $T(v_i) = w_i$, confident that a unique, well-defined linear transformation on the entire space is guaranteed to exist.

> [!remark]
> This problem can be shown easily without using Linear Extension Theorem with following theorem 

---

> [!theorem] Theorem 16
> Suppose $V$ and $W$ are finite dimensional vector spaces. If $\dim V=\dim W$ then $V$ and $W$ are isomorphic.

Proof:
Let $\{ v_{1},\dots,v_{n} \}$ be a basis for $V$ and $\{ w_{1},\dots,w_{n} \}$ be basis for $W$. Note that they the same number of elements.

By Linear Extension Theorem, there exist a unique linear transformation $T:V\to W$ such that $T(v_{i})=w_{i}$ for $i=1,\dots,n$.a

Note that $\mathcal{L}(v_{1},\dots,v_{n})=V$ and $T(\mathcal{L}(v_{1},\dots,v_{n}))=\mathcal{L}T(v_{1},\dots,v_{n})$. Therefore,
$$
\begin{align}
\mathrm{Im}(T)&= T(\mathcal{L}(v_{1},\dots,v_{n})) \\
&=\mathcal{L}T(v_{1},\dots,v_{n}) \\
&=\mathcal{L}(T(v_{1}),\dots,T(v_{n})) \\
&=\mathcal{L}(w_{1},\dots,w_{n}) \\
&= W
\end{align}
$$

Then, By Theorem 11
$$
\begin{align}
\dim(V)&=\dim(\ker(T) )+\dim(\mathrm{Im}(T)) \\
n&=\dim(\ker(T))+\dim(W) \\
&=\dim(\ker(T))+n \\
\dim(\ker(T))&=0
\end{align}
$$

Hence, $\ker(T)=\{  0 \}$. Hence $T$ is an isomorphism and $V\cong W$. $\blacksquare$

> [!remark]
> Or we can straight away use Theorem 12

> [!theorem] Corollary 1
> If a vector space $V$ has finite dimension $n$ then $V$ is isomorphic to $\mathbb{R}^{n}$

