(1.) Show that $V = \mathbb { R } ^ { 2 }$ is not a vector space over R with respect to the following operations: $( a , b ) + ( c , d ) = ( a + c , b + d )$ and $\boldsymbol { k } ( a , b ) = ( k a , b )$ 

Check the distributive law:
Suppose $v_{1}=(x_{1},y_{1})\in V$ and $v_{2}=(x_{2},y_{2})\in V$ and $c\in \mathbb{R}$. Thus,

$$
\begin{align}
c(v_{1}+v_{2})&=(x_{1}+x_{2},y_{1}+y_{2}) \\
&=(c(x_{1}+x_{2}),y_{1}+y_{2})
\end{align}
$$
$$
\begin{align}
(cv_{1}+cv_{2})&= (cx_{1},y_{1})+(cx_{2},y_{2}) \\
&=(c(x_{1}+x_{2}),y_{1}+y_{2}) \\
&=c(v_{1}+v_{2})
\end{align}
$$

Check distributive over scalar:
Note that
$$
\begin{align}
(c_{1}+c_{2})v_{1}&=((c_{1}+c_{2})x_{1},y_{1})
\end{align}
$$
and
$$
\begin{align}
c_{1}v_{1}+c_{2}v_{1}&= (c_{1}x_{1},,y_{1})+(c_{2}x_{1},y_{1}) \\
&=((c_{1}+c_{2})x_{1}, 2y_{1}) \\
& \neq (c_{1}+c_{2})v_{1}
\end{align}
$$
Thus, $V$ is not a vector space.


> [!warning]
> Property $0u=0$:
> Note that $0v_{1}=(0,y_{1}) \neq 0$. Thus, it is not vector space.
> 
> 
> Additive inverse theorem: $u+(-u)=0$
> Note that for any $v\in V$, $-v=-1(v)$ is additive inverse of $u$. Thus,
> 
> $$
> \begin{align}
> v_{1}+(-v_{1})&= v_{1}-1(v_{1}) \\
> &=(x_{1},y_{1})+(-x_{1},y_{1}) \\
> &=(0,y_{1}) \\
> & \neq 0
> \end{align}
> $$
> Hence, $V$ is not a vector space.
> 
> Can we show like this? Cannot, because both of them are theorem derived from axiom rather then axiom.

> [!remark]
> How to know by inspection? 
> In $(c+d)v$, scalar multiplication occur once, keeping single copy of $y$.
> In $cv+dv$, two scaled vectors are created and then added together force to sum the second component to $2y$.

> [!example] Inspection Example: Modified Addition
> Consider $V = \mathbb{R}^2$ with standard scalar multiplication, but modified addition:
> $$(a, b) + (c, d) = (a + c, 0)$$
> **Axiom that fails: Additive Identity**
> An additive identity $\mathbf{0} = (e_1, e_2)$ must satisfy $v + \mathbf{0} = v$ for all $v = (x, y) \in V$:
> $$(x, y) + (e_1, e_2) = (x + e_1, 0)$$
> For this to equal $(x, y)$, we must have $0 = y$ for every vector, which is impossible whenever $y \neq 0$ (e.g., for $v = (0, 1)$).
> Hence, no additive identity exists, and $(V, +)$ fails to be an abelian group before scalar multiplication is even tested.

> [!tip] Quick-Inspection Cheat Sheet for Axiom Violations
> | Signature in Operation | What it looks like | Suspect Axiom to Test First | Why it breaks |
> | :--- | :--- | :--- | :--- |
> | **Ignored / Frozen Variable** | $k(x, y) = (kx, y)$ | $(c + d)v = cv + dv$ | $y$ (scaled once) vs $y + y = 2y$ (scaled twice and added) |
> | **Non-Linear Exponent** | $k(x, y) = (k^2 x, ky)$ | $(c + d)v = cv + dv$ | $(c + d)^2 \neq c^2 + d^2$ (cross-term $2cd$) |
> | **Constant / Shifted Term** | $u + v = (x_1 + x_2 + 1, \dots)$ | $c(u + v) = cu + cv$ | Shift gets scaled ($+c$) vs shift added unscaled ($+1$) |
> | **Swapped Coordinates** | $k(x, y) = (ky, kx)$ | $c(dv) = (cd)v$ or $1v = v$ | Scaling twice un-swaps coordinates; $1(x, y) = (y, x) \neq (x, y)$ |
> | **Absolute Value / Norm** | $k(x, y) = (\lvert k\rvert x, \lvert k\rvert y)$ | $(c + d)v = cv + dv$ | $\lvert c + d\rvert \neq \lvert c\rvert + \lvert d\rvert$ for opposite signs |
> | **Missing Identity Slot** | $u + v = (x_1 + x_2, 0)$ | $v + \mathbf{0} = v$ (Additive identity) | No fixed $(e_1, e_2)$ can output $y$ when $y \neq 0$ |



(2.) Determine whether the set of complex numbers $\mathbb { C } ^ { 2 }$ a vector space 
(a.) over C.  Yes
(b.) over R. Yes
(c.) over Z. No because the set of integer is not a field $\mathbb{F}$, because no multiplicative inverse.

> [!note] Why must scalars come from a Field $\mathbb{F}$?
> The defining property of a **field** $\mathbb{F}$ that general rings (like $\mathbb{Z}$) lack is that every non-zero scalar $c \neq 0$ has a **multiplicative inverse** $c^{-1}$ (allowing division by non-zero scalars).
> 
> Without multiplicative inverses:
> 1. **Cannot Solve Linear Combinations:** If $2v_1 + 3v_2 = \mathbf{0}$, we cannot isolate $v_1 = -\frac{3}{2}v_2$ over $\mathbb{Z}$ because $2^{-1} = \frac{1}{2} \notin \mathbb{Z}$.
> 2. **Basis & Dimension Collapse:** Over a field, every vector space has a basis, and all bases have the same cardinality (dimension). Over a ring, the structure is called a **module** (e.g. $\mathbb{Z}$-module), where sets can fail to have any basis at all.
> 3. **Gaussian Elimination Breaks:** You cannot scale a row by $\frac{1}{c}$ to obtain a leading $1$ pivot during row reduction.

(3.) Determine whether $W = \{ ( a , b , c ) | a \geq 0 \}$ is a subspace of $V = \mathbb { C } ^ { 3 } { \mathrm { ~ o v e r ~ } } \mathbb { R }$ 

No. Let $w_{1}=(1,0,0)\in W$, note that $-w_{1}=-1(1,0,0)=(-1,0,0)\not\in W$. Thus, it is not closed under scalar multiplication.

(4.) Let U and W be subspaces of a vector space V. Show that the intersection U ∩ W is also a subspace of V. 

[[4.1 Vector space#^cc5ea0]]

(5.) Show that W is not a subspace of V where $W = \{ f ( x ) \in F(S,C) | f ( 7 ) = 2 + f ( 1 ) \}$ 

Suppose 2 function $f$ and $g$ such that $f(7)=2+f(1)$ and $g(7)=2+f(1)$. Thus,

$$
\begin{align}
(f+g)(7)&=f(7)+g(7) \\
&=2+f(1)+2+g(1) \\
&=(f+g)(1)+4 \not\in W
\end{align}
$$

Since it is not closed under addition, it follow that it is not a subspace.


(6.) Suppose $W _ { 1 } , W _ { 2 } , W _ { 3 }$ are the $x , y$ axis and the line $y = x$ respectively on the $\mathbb { R } ^ { 2 }$ plane. Show that $\mathbb { R } ^ { 2 } \neq W _ { 1 } \oplus W _ { 2 } \oplus W _ { 3 }$  ^ea0d58

$$
\begin{align}
W_{1}&=\{ (a,0)| a\in \mathbb{R} \} \\
W_{2}&=\{ (0,b)| y\in \mathbb{R} \} \\
W_{3}&= \{ (c,d)|c=d, c\in \mathbb{R} \} \\
&=\{ (c,c)|c\in \mathbb{R} \}
\end{align}
$$

Approach 1 using definition:

Let $S=W_{1}\oplus W_{2} \oplus W_{3}$ . Suppose $v_{1}=(x,y)\in S$, then there exist  $c_{1},c_{2},c_{3}$ such that

$$
\begin{align}
(x,y)&= c_{1}(1,0)+c_{2}(0,1)+c_{3}(1,1) \\
&=(c_{1}+c_{3},c_{2}+c_{3})
\end{align}
$$

> [!question] Why we use $1$ here instead of $a,b,c$?
> It is because $(1,0),(0,1),(1,1)$ are basis for $W_{1},W_{2},W_{3}$ respectively. 

Thus, we can form the system below:
$$
\begin{align}
x&=c_{1}++0c_{2}+c_{3} \\
y&=0c_{1}+c_{2}+c_{3}
\end{align}
$$
The system have same solution set as the matrix equation below:
$$
\begin{bmatrix}
1 & 0 & 1 \\
0 & 1 & 1
\end{bmatrix} \begin{bmatrix}
c_{1} \\
c_{2} \\
c_{3}
\end{bmatrix}= \begin{bmatrix}
x \\
y
\end{bmatrix}
$$
Note that the coefficient matrix $A$ is $2\times 3$. Thus, the column of $A$ is linearly dependent. Thus, $c_{1},c_{2},c_{3}$ is not unique for any $(x,y)\in \mathbb{R}$.

> [!remark]
> Note the thing we did is actually showing the basis for $W_{1},W_{2},W_{3}$ are linearly dependent. This lead to the second approach using theorem and faster

Approach 2: Show the basis for $W_{1},W_{2},W_{3}$ is linearly dependent/ [^1]Trivial Zero Representation

> [!remark]
> By theorem to show $W_{1}+W_{2}+W_{3}$ is direct iff the zero vector can be written in only one way. (Intersection is empty set $\iff$ The basis of 3 vector space are linearly independent) [[Complex Vector space#^e822c9]]
> 
> Refer the second condition of  [[Complex Vector space#^0339db]]. If we want to show that  $\mathbb { R } ^ { 2 } \neq W _ { 1 } \oplus W _ { 2 } \oplus W _ { 3 }$ , then we only need to show one of them:
> 1) $W_{1}+W_{2}+W_{3} \neq \mathbb{R}^{2}$
> 2) $W_j \cap \sum_{i \neq j} W_i \neq \{0\}$ (e.g. $W_{3}\cap (W_{1}+W_{2}) \neq \{  0 \}$) $\iff$ Combined bases for $W_{1},W_{2},W_{3}$ are linearly dependent. *(Note: $W_1 \cap W_2 \cap W_3 = \{0\}$ is NOT the test for 3 subspaces!)*

We just need to identify
$$
1(1,0)+1(0,1)-1(1,1)=0
$$
is non-trivial solution for this vector equation. Thus, they are linearly dependent. By theorem it is not a direct sum.  $\blacksquare$

> [!tip] Which Method to Choose in Practice? (Trivial Zero vs. Combined Bases)
> - **To Disprove ($V \neq \bigoplus W_i$):** **Trivial Zero Representation** is faster because you only need to spot **one** non-zero counterexample $w_1 + w_2 + w_3 = \mathbf{0}$ (as done above: $(1,0)+(0,1)-(1,1)=\mathbf{0}$) without calculating full bases or matrices.
> - **To Prove ($V = \bigoplus W_i$):** **Combined Bases** is much better in practice because Trivial Zero requires proving for *all* arbitrary vectors (which ends up needing coordinate equations anyway). Combined Bases is 100% algorithmic: just put the bases as columns into a matrix and compute rank or determinant.
> 
> *(See full conceptual breakdown in [[Complex Vector space#^diff-zero-vs-bases]])*

(7.) Determine whether the vectors are linearly dependent and span the vector space. 

(a.) 

$$
\begin{array}{l} u = \left( \begin{array}{c c} 1 & 2 i \\ 5 & i \end{array} \right) \\ v = \left( \begin{array}{c c} i & 0 \\ 2 & 0 \end{array} \right) \end{array}
$$

and $u , v \in M _ { 2 \times 2 } ( \mathbb { C } )$ over R. 

Note that $dim(M_{2\times2}(\mathbb{C}))=4$ over $\mathbb{C}$. By [[Complex Vector space#^3475e4]], it follow that $dim(M_{2\times 2}(\mathbb{C}))=8$. Thus, it cannot span by 2 vector $u$ and $v$.


(b.) Let $\boldsymbol { u } = ( 2 , 0 ) , \boldsymbol { v } = ( i , 1 ) , \boldsymbol { w } = ( 0 , 2 i ) , \boldsymbol { y } = ( 1 , 1 )$ be the vectors of $\mathbb { C } ^ { 2 }$ over R. 

Identify $\mathbb{C}^2 \cong \mathbb{R}^4$ with the standard basis $\mathcal{B} = \{(1, 0), (i, 0), (0, 1), (0, i)\}$. 

Represent the vectors as coordinate column vectors:
$$
\boldsymbol{u} = \begin{bmatrix} 2 \\ 0 \\ 0 \\ 0 \end{bmatrix}, \quad 
\boldsymbol{v} = \begin{bmatrix} 0 \\ 1 \\ 1 \\ 0 \end{bmatrix}, \quad 
\boldsymbol{w} = \begin{bmatrix} 0 \\ 0 \\ 0 \\ 2 \end{bmatrix}, \quad 
\boldsymbol{y} = \begin{bmatrix} 1 \\ 0 \\ 1 \\ 0 \end{bmatrix}
$$

Form the coefficient matrix $A = [\boldsymbol{u} \mid \boldsymbol{v} \mid \boldsymbol{w} \mid \boldsymbol{y}]$:
$$
A = \begin{bmatrix}
2 & 0 & 0 & 1 \\
0 & 1 & 0 & 0 \\
0 & 1 & 0 & 1 \\
0 & 0 & 2 & 0
\end{bmatrix}
$$

Compute the determinant by expanding along the 4th row:
$$
\det(A) = -2 \begin{vmatrix} 
2 & 0 & 1 \\ 
0 & 1 & 0 \\ 
0 & 1 & 1 
\end{vmatrix} = -2 \cdot [2(1 \cdot 1 - 0 \cdot 1)] = -4 \neq 0
$$

**Conclusion:**
- Since $\det(A) \neq 0$, the vectors are **linearly independent** over $\mathbb{R}$.
- Since there are $4$ linearly independent vectors in a $4$-dimensional space ($\dim_{\mathbb{R}}(\mathbb{C}^2) = 4$), they also **span** $\mathbb{C}^2$ over $\mathbb{R}$ (and form a basis).


(c.) Let $\boldsymbol { u } = ( 2 , 0 ) , \boldsymbol { v } = ( i , 1 ) , \boldsymbol { w } = ( 0 , 2 i ) , \boldsymbol { y } = ( 1 , 1 )$ be the vectors of $\mathbb { C } ^ { 2 }$ over C. 

Check if linearly independent:
Identify $\mathbb{C}^{2}$ with ordered standard basis $B=\{ (1,0),(0,1) \}$. Thus, $\operatorname{dim}_{\mathbb{C}}(\mathbb{C}^{2})=2$. Since the given vector is more than 2, it follow that by theorem, $\{ u,v,w,y \}$ is linearly dependent.

> [!remark]
> Why we cannot write $\mathbb{C}^{2}\cong \mathbb{R}^{2}$ in this case?
> It is because in this question $\mathbb{C}^{2}$ is over $\mathbb{C}$ while $\mathbb{R}^{2}$ is a vector space over $\mathbb{R}$ (only with real scalar), thus they cannot be isomorphic.  

Check if span $\mathbb{C}^{2}$:

Approach 1: Using Matrix / Pivot Position
The coordinate vector of given vector with respect to $B$ is
$$
\begin{matrix}
u=\begin{pmatrix}
2 \\
0
\end{pmatrix}&,v= \begin{pmatrix}
i \\
1
\end{pmatrix}&,w=\begin{pmatrix}
0 \\
2i
\end{pmatrix}&,y=\begin{pmatrix}
1 \\
1
\end{pmatrix}
\end{matrix}
$$

> [!tip] Observation: Coordinate Vectors in $\mathbb{C}^n$ over $\mathbb{C}$ vs. over $\mathbb{R}$
> Why are the coordinate vectors $[\boldsymbol{u}]_{\mathcal{B}}, [\boldsymbol{v}]_{\mathcal{B}}, \dots$ literally just the given vectors written vertically?
> - **Over $\mathbb{C}$:** The scalar field is $\mathbb{C}$. Any vector $(z_1, z_2) = z_1(1, 0) + z_2(0, 1)$ uses complex scalars $z_1, z_2 \in \mathbb{C}$. Thus, with respect to the standard basis $\mathcal{B} = \{(1, 0), (0, 1)\}$, its coordinates are simply $\begin{pmatrix} z_1 \\ z_2 \end{pmatrix} \in \mathbb{C}^2$.
> - **Over $\mathbb{R}$ (Part b):** Scalars must be real ($c_i \in \mathbb{R}$). For $\boldsymbol{v} = (i, 1)$, we cannot write $i(1, 0)$ because $i \notin \mathbb{R}$. We had to use the $4$-element real basis $\{(1, 0), (i, 0), (0, 1), (0, i)\}$, yielding a $4 \times 1$ coordinate vector $\begin{pmatrix} 0 \\ 1 \\ 1 \\ 0 \end{pmatrix} \in \mathbb{R}^4$.
>
> In general, for any space $F^n$ over $F$, the coordinate vector with respect to the standard basis is always just the tuple turned into a column.

Let $A=\begin{bmatrix}u & v & w & y\end{bmatrix}$. We need to determine if $\operatorname{Col}(A)=\mathbb{C}^{2}$. 

$$
\begin{align}
A&= \begin{bmatrix}
2 & i & 0 & 1 \\
0 & 1 & 2i & 1
\end{bmatrix} \\
\end{align}
$$
Note that $A$ is already in REF form and every row of $A$ has a pivot position. Thus, by theorem it follows that $\operatorname{Col}(A)=\mathbb{C}^{2}$.

Approach 2: Faster Observation (Standard Basis Containment)
Notice that using just $\boldsymbol{u} = (2, 0)$ and $\boldsymbol{y} = (1, 1)$:
$$
(1, 0) = \frac{1}{2}\boldsymbol{u} \in \operatorname{span}_{\mathbb{C}}\{\boldsymbol{u}, \boldsymbol{v}, \boldsymbol{w}, \boldsymbol{y}\}
$$
$$
(0, 1) = \boldsymbol{y} - \frac{1}{2}\boldsymbol{u} \in \operatorname{span}_{\mathbb{C}}\{\boldsymbol{u}, \boldsymbol{v}, \boldsymbol{w}, \boldsymbol{y}\}
$$
Since both standard basis vectors belong to the subspace $W = \operatorname{span}_{\mathbb{C}}\{\boldsymbol{u}, \boldsymbol{v}, \boldsymbol{w}, \boldsymbol{y}\}$, by subspace closure any linear combination of them must also stay in $W$:
$$
\mathbb{C}^2 = \operatorname{span}\{(1, 0), (0, 1)\} \subseteq \operatorname{span}_{\mathbb{C}}\{\boldsymbol{u}, \boldsymbol{v}, \boldsymbol{w}, \boldsymbol{y}\} \subseteq \mathbb{C}^2
$$
Thus, $\operatorname{span}_{\mathbb{C}}\{\boldsymbol{u}, \boldsymbol{v}, \boldsymbol{w}, \boldsymbol{y}\} = \mathbb{C}^2$.


(8.) Determine whether or not each of the following forms a basis for $\mathbb { C } ^ { 3 }$ over C: 
(a.) $( i , 1 , 1 ) , ( 1 , 0 , i )$ 

By identifying that the standard basis for $\mathbb{C}^{3}$ over $\mathbb{C}$ is $\mathcal{B}=\{ (1,0,0),(0,1,0),(0,0,1) \}$, we have $\dim_{\mathbb{C}}(\mathbb{C}^{3})=3$. Since there are only $2$ vectors given ($2 < 3$), they cannot span $\mathbb{C}^{3}$ and thus do not form a basis for $\mathbb{C}^{3}$ over $\mathbb{C}$.

(b.) $( i , 1 , 1 ) , ( i , 2 , 3 ) , ( 2 , - 1 , i )$ 

From 7(c) we know that the coordinate vector with respect to ordered basis $B$ is just the vector itself (because it is over $\mathbb{C}$). Thus, consider the matrix $A$ below:

$$
\begin{align}
A&= \begin{bmatrix}
i & i & 2 \\
1 & 2 & -1 \\
1 & 3 & i
\end{bmatrix} 
\end{align}
$$
The determinant using cofactor expansion along row 1 give us
$$
\begin{align}
\det A&=i \begin{vmatrix}
2 & -1 \\
3 & i
\end{vmatrix}-i \begin{vmatrix}
1 & -1 \\
1 & i
\end{vmatrix}+2 \begin{vmatrix}
1 & 2 \\
1 & 3
\end{vmatrix} \\
&= i(2i+3)-i(i+1)+2(1) \\
&=-2+3i+1-i+2 \\
&=1+2i \neq 0
\end{align}
$$
Thus, by the Invertible Matrix Theorem, it follows that the columns of $A$ (which are the given vectors) form a basis for $\mathbb{C}^{3}$ over $\mathbb{C}$.


(c.) $( 1 , 2 , 3 i ) , ( i , 3 , 5 ) , ( 1 , i , 1 ) , ( 2 , 3 i , 0 )$ 

By the same reasoning from (a), the given vector form 4 vectors which is more than the number of  vector in basis. Thus, by theorem it is linearly dependent, thus not a basis for $\mathbb{C}^{3}$ over $\mathbb{C}$.

(9.) Determine whether or not each of the following forms a basis for $\mathbb { C } ^ { 3 }$ over R: 

(a.) $( i , 1 , 1 ) , ( 1 , 0 , i ) , ( 0 , i , 0 )$ 

By identifying the standard basis for $\mathbb{C}^{3}$ over $\mathbb{R}$ is $B=\{ (1,0,0),(0,1,0),(0,0,1),(i,0,0),(0,i,0),(0,0,i) \}$. We know that $\dim_{\mathbb{R}}(\mathbb{C}^{3})=2\dim_{\mathbb{C}}(\mathbb{C}^{3})=6$. Since the given vector only form 3 vector in $\mathbb{C}^{3}$, it follow that it is not a basis.

(b.) $( 1 , 1 , 1 ) , ( 1 , 2 , 3 ) , ( 2 , - 1 , 1 ) , ( 1 , 0 , 0 )$ 

Same argument from 8(a)


(c.) $( i , 1 , 1 ) , ( 1 , 0 , i ) , ( 0 , i , 0 ) , ( 1 , 0 , 0 ) , ( 0 , 1 , 0 ) , ( 0 , 0 , 1 )$ 

By [[Complex Vector space#^3475e4]], the dimension of $\mathbb{C}^3$ over $\mathbb{R}$ is $\dim_{\mathbb{R}}(\mathbb{C}^3) = 2\dim_{\mathbb{C}}(\mathbb{C}^3) = 2(3) = 6$.
The standard basis for $\mathbb{C}^{3}$ over $\mathbb{R}$ has $6$ vectors:
$$
\mathcal{B}_{\mathbb{R}} = \{(1, 0, 0), (0, 1, 0), (0, 0, 1), (i, 0, 0), (0, i, 0), (0, 0, i)\}
$$
Since the given set $S$ contains exactly $6$ vectors, by the Basis Theorem we only need to show that they either span $\mathbb{C}^3$ or are linearly independent over $\mathbb{R}$.

Method 1: Spanning via Standard Basis Containment
The last three vectors are already the real standard basis vectors:
$$e_1 = (1, 0, 0), \quad e_2 = (0, 1, 0), \quad e_3 = (0, 0, 1) \in \operatorname{span}_{\mathbb{R}}(S)$$

By subtracting these real vectors from the first two vectors in $S$, we can isolate the pure imaginary standard basis vectors:
$$
\begin{align*}
(i, 0, 0) &= (i, 1, 1) - (0, 1, 0) - (0, 0, 1) \in \operatorname{span}_{\mathbb{R}}(S) \\
(0, 0, i) &= (1, 0, i) - (1, 0, 0) \in \operatorname{span}_{\mathbb{R}}(S) \\
(0, i, 0) &= (0, i, 0) \in \operatorname{span}_{\mathbb{R}}(S)
\end{align*}
$$

Since all $6$ standard basis vectors of $\mathcal{B}_{\mathbb{R}}$ belong to $\operatorname{span}_{\mathbb{R}}(S)$, by subspace closure:
$$
\mathbb{C}^3 = \operatorname{span}_{\mathbb{R}}(\mathcal{B}_{\mathbb{R}}) \subseteq \operatorname{span}_{\mathbb{R}}(S) \subseteq \mathbb{C}^3 \implies \operatorname{span}_{\mathbb{R}}(S) = \mathbb{C}^3
$$
Since $S$ has $6$ vectors and spans a $6$-dimensional space, $S$ forms a **basis** for $\mathbb{C}^3$ over $\mathbb{R}$.

 Method 2: Linear Independence (Real vs. Imaginary Components)
Let $c_1, c_2, c_3, c_4, c_5, c_6 \in \mathbb{R}$ such that:
$$
c_1(i, 1, 1) + c_2(1, 0, i) + c_3(0, i, 0) + c_4(1, 0, 0) + c_5(0, 1, 0) + c_6(0, 0, 1) = (0, 0, 0)
$$
Collecting the real and imaginary parts of each coordinate:
$$
\begin{cases}
(c_2 + c_4) + c_1 i = 0 & \text{(1st coordinate)} \\
(c_1 + c_5) + c_3 i = 0 & \text{(2nd coordinate)} \\
(c_1 + c_6) + c_2 i = 0 & \text{(3rd coordinate)}
\end{cases}
$$
Equating the imaginary parts to zero immediately yields:
$$
c_1 = 0, \quad c_3 = 0, \quad c_2 = 0
$$
Substituting $c_1 = c_2 = c_3 = 0$ into the real parts:
$$
\begin{cases}
0 + c_4 = 0 \implies c_4 = 0 \\
0 + c_5 = 0 \implies c_5 = 0 \\
0 + c_6 = 0 \implies c_6 = 0
\end{cases}
$$
Thus, the only real solution is $c_1 = c_2 = c_3 = c_4 = c_5 = c_6 = 0$, meaning the $6$ vectors are **linearly independent** over $\mathbb{R}$.

Since $\dim_{\mathbb{R}}(\mathbb{C}^3) = 6$, any set of $6$ linearly independent vectors forms a **basis** for $\mathbb{C}^3$ over $\mathbb{R}$.


(10.) Consider the complex field C, which contains the real field R. Thus, C is a vector space over R. Show that $\{ 1 , i \}$ is a basis of C over R and hence, C is a vector space of dimension 2 over R. 

Consider the system below
$$
\begin{align}
c_{1}1+c_{2}i&=0
\end{align}
$$
Since $c_{1},c_{2}\in \mathbb{R}$, It is clear that by comparing real part and imaginary parts $c_{1}=c_{2}=0$.  Thus, $\{ 1,i \}$ is linearly independent. For any $v_{1}=a+bi\in \mathbb{C}$, we have

$$
c_{1}1+c_{2}i=a+bi
$$
Thus, $c_{1}=a$ and $c_{2}=b$. Hence, it follow that $\{ 1,i \}$ span $\mathbb{C}$
over $\mathbb{R}$. Therefore $\{ 1,i \}$ is a basis for $\mathbb{C}$ over $\mathbb{R}$. Thus, $\dim_{\mathbb{R}}(\mathbb{C})=2$.


(11.) Find a basis and dimension of the subspaces W of $\mathbb { C } ^ { 3 }$ over C where: 

(a.) $W = \{ ( a , b , c ) | a + b + c = 0 \}$ 

(b.) $W = \{ ( a , b , c ) | a = b = c \}$ 

(12.) [TEST] Let $P _ { 2 } ( \mathbb { C } )$ be the vector space over R with all complex polynomials of degree two or less.

(a.) Let $S = \{ 1 , x , x ^ { 2 } \}$ be a subset of $P _ { 2 } ( \mathbb { C } )$ . Determine whether $\mathrm { s p a n } _ { \mathbb { R } } ( S )$ is a subspace of $P _ { 2 } ( \mathbb { C } )$ 

By theorem if $S\subseteq P_{2}(\mathbb{C})$, then $Span(S)$ is a subspace of $P_{2}(\mathbb{C})$. [[2.8 Subspace#^5776a2]]


(b.) Determine whether span<sub>R</sub> $( S ) = P _ { 2 } ( \mathbb { C } )$ 

No because $\dim_{\mathbb{R}}(P_{2}(\mathbb{C}))=6$, but the given vector only form 3 vector. Thus, it does not span $P_{2}(\mathbb{C})$. 

We can give a counterexample like $P(x)=i\in P_{2}(\mathbb{C})$ can never be expressed as a real linear combination of $\{ 1,x,x^{2} \}$

(c.) Give a basis for $P _ { 2 } ( \mathbb { C } )$ 
$\{ 1,x,x^{2},i,ix,ix^{2} \}$
[[Complex Vector space#^3475e4]]. This directly follow by the theorem if $\{ v_{1},\dots,v_{n} \}$ is a basis over $\mathbb{C}$, then $\{ v,i\mathbf{v}..,v_{n},iv_{n} \}$ is a basis over $\mathbb{R}$ 

(13.) [TEST] Let V be the vector space $M _ { 2 \times 1 } ( \mathbb { C } )$ over R. 

(a.) Determine whether $W = { \left\{ \left( { \begin{array} { l } { 2 x } \\ { 0 } \end{array} } \right) { \Big | } x \in \mathbb { C } \right\} }$ is a subspace of V. 

(b.) Give a basis for V . 

(c.) Let 

$$
u = \binom{i}{1} \qquad \text { and } \qquad v = \binom{1}{0}
$$

be vectors in V. Determine whether span $( u , v ) = V$ 

(14.) [TEST] Let $V = \mathbb { C } ^ { 2 }$ be the vector space over C and let $\alpha = \{ u _ { 1 } = ( i , 1 ) , u _ { 2 } =$ (1, 0)} be vectors in V. Show that α forms a basis for V. 

[^1]: In this question, the **Trivial Zero Representation** (Statement 2) and the **Combined Bases Theorem** (Statement 4) are practically the same test. Because each subspace $W_1, W_2, W_3$ is $1$-dimensional ($\dim(W_i) = 1$), a basis for each subspace consists of just a single non-zero vector. Hence, picking one non-zero vector from each subspace to test for a zero sum ($w_1 + w_2 + w_3 = \mathbf{0}$) is identical to testing the linear independence of their combined bases.
