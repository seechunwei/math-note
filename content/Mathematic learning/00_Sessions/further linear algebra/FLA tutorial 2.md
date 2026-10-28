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

Approach 2: Show the basis for $W_{1},W_{2},W_{3}$ is linearly dependent

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



(8.) Determine whether or not each of the following forms a basis for $\mathbb { C } ^ { 3 }$ over C: 
(a.) $( i , 1 , 1 ) , ( 1 , 0 , i )$ 
(b.) $( i , 1 , 1 ) , ( i , 2 , 3 ) , ( 2 , - 1 , i )$ 
(c.) $( 1 , 2 , 3 i ) , ( i , 3 , 5 ) , ( 1 , i , 1 ) , ( 2 , 3 i , 0 )$ 

(9.) Determine whether or not each of the following forms a basis for $\mathbb { C } ^ { 3 }$ over R: 

(a.) $( i , 1 , 1 ) , ( 1 , 0 , i ) , ( 0 , i , 0 )$ 

(b.) $( 1 , 1 , 1 ) , ( 1 , 2 , 3 ) , ( 2 , - 1 , 1 ) , ( 1 , 0 , 0 )$ 

(c.) $( i , 1 , 1 ) , ( 1 , 0 , i ) , ( 0 , i , 0 ) , ( 1 , 0 , 0 ) , ( 0 , 1 , 0 ) , ( 0 , 0 , 1 )$ 

(10.) Consider the complex field C, which contains the real field R. Thus, C is a vector space over R. Show that $\{ 1 , i \}$ is a basis of C over R and hence, C is a vector space of dimension 2 over R. 

(11.) Find a basis and dimension of the subspaces W of $\mathbb { C } ^ { 3 }$ over C where: 

(a.) $W = \{ ( a , b , c ) | a + b + c = 0 \}$ 

(b.) $W = \{ ( a , b , c ) | a = b = c \}$ 

(12.) [TEST] Let $P _ { 2 } ( \mathbb { C } )$ be the vector space over R with all complex polynomials of degree two or less. 

(a.) Let $S = \{ 1 , x , x ^ { 2 } \}$ be a subset of $P _ { 2 } ( \mathbb { C } )$ . Determine whether $\mathrm { s p a n } _ { \mathbb { R } } ( S )$ is a subspace of $P _ { 2 } ( \mathbb { C } )$ 

(b.) Determine whether span<sub>R</sub> $( S ) = P _ { 2 } ( \mathbb { C } )$ 

(c.) Give a basis for $P _ { 2 } ( \mathbb { C } )$ 

(13.) [TEST] Let V be the vector space $M _ { 2 \times 1 } ( \mathbb { C } )$ over R. 

(a.) Determine whether $W = { \left\{ \left( { \begin{array} { l } { 2 x } \\ { 0 } \end{array} } \right) { \Big | } x \in \mathbb { C } \right\} }$ is a subspace of V. 

(b.) Give a basis for V . 

(c.) Let 

$$
u = \binom{i}{1} \qquad \text { and } \qquad v = \binom{1}{0}
$$

be vectors in V. Determine whether span $( u , v ) = V$ 

(14.) [FE] Let $V = \mathbb { C } ^ { 2 }$ be the vector space over C and let $\alpha = \{ u _ { 1 } = ( i , 1 ) , u _ { 2 } =$ (1, 0)} be vectors in V. Show that α forms a basis for V. 