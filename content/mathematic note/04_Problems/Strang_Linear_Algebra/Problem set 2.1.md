1)
a) The plane of vector $(a_{1},a_{2})$ where $a_{1},a_{2}\geq0$

The plane of vector where $a_{1}\geq a_{2}$, it go out of the plane when it multiply with negative value.

The plane of vector where $a_{1},a_{2}\leq 0$

b)
The plane where the first quadrant and third quadrant.

==2==
For a subset of $\mathbb{R}^{3}$ to be a subspace, it need to satisfy these 3 condition
1) it must include zero vector
2) it is closed under addition
3) it is closed under multiplication

a) Yes,

b) No, it does not include zero vector

c) $b_{2}=0$ or $b_{3}=0$. 
It is not close under addition
$$
\begin{bmatrix}
1 \\
1 \\
0
\end{bmatrix}+\begin{bmatrix}
1 \\
0 \\
1
\end{bmatrix}=\begin{bmatrix}
1 \\
1 \\
1
\end{bmatrix}
$$
d) Yes, it a spanning set of these two vectors.

e) Yes, it is a solution set for homogeneous system. We just let the solution set become
$$
c \begin{bmatrix}
1 \\
-1 \\
3
\end{bmatrix}
$$


3)
$$
A=\begin{bmatrix}
1 & -1 \\
0 & 0
\end{bmatrix}
$$
$C(A)$: The column space of $A$ is a line pass though $(1,0)$ and $(0,0)$ in $\mathbb{R}^{2}$. 
Why the vector doesn't span $\mathbb{R}^{2}$? It is because the second vector is -1 multiply with first vector. Thus, they are actually in the same line (linearly dependent).

$N(A)$: The null space of $A$ is the solution set when $Ax=0$. Notice that 
$$
1\begin{bmatrix}
1 \\
0
\end{bmatrix}+1\begin{bmatrix}
-1 \\
0
\end{bmatrix}=0
$$
Thus, the spanning set of $(1,1)$ is the null space of $A$.

$$
B=\begin{bmatrix}
0 & 0 & 3 \\
1 & 2 & 3
\end{bmatrix}
$$
Notice that since each row of $B$ have pivot, it follow that $C(A)=\mathbb{R}^{2}$

Notice that there exist one free variable $x_{2}$. Thus, the solution set for $Ax=0$ is

$$
x=\begin{bmatrix}
-2x_{2} \\
x_{2} \\
0
\end{bmatrix}=x_{2}\begin{bmatrix}
-2 \\
1 \\
0
\end{bmatrix}
$$
which is the $N(A)$.

---

$C(B)$: 
If we can solve a matrix by Gaussian elimination$\implies$ nonsingular $\implies$$n$ pivot $\implies$ we can produce any $n$ dimensional vector $\implies$ span $\mathbb{R}^{n}$

This argument is wrong because:

1) The Shape of the Matrix

Your argument assumes the matrix is **square** ($n \times n$). If the matrix is rectangular, the logic of "$n$ pivots $\implies$ span $\mathbb{R}^n$" changes:

- **Tall Matrix ($m > n$):** Can have $n$ pivots (full column rank), but it can **never** span $\mathbb{R}^m$ because it doesn't have enough columns to cover all dimensions.
    
- **Wide Matrix ($n > m$):** Can span $\mathbb{R}^m$ if it has $m$ pivots, but it will **always** be singular (it has a non-trivial null space) because there are more variables than equations.
    

---
^111
 The Correct Logical Chain ^c692d6

If you want to reach the conclusion that the columns span $\mathbb{R}^n$, the argument should look like this:

1. The matrix $A$ is **$n \times n$ (square)**.
    
2. Gaussian elimination results in **$n$ pivots** (no zero rows in RREF).
    
3. $\implies$ The columns are **linearly independent**.
    
4. $\implies$ The matrix is **nonsingular** (invertible).
    
5. $\implies$ $A\mathbf{x} = \mathbf{b}$ has a unique solution for **any** $\mathbf{b} \in \mathbb{R}^n$.
    
6. $\implies$ The columns **span $\mathbb{R}^n$**.

Look at $B$, $2\times 3$, where $3>2$ (wide matrix), it follow that $B$ is singular, but does this tell anything? No

[[1.4 The Matrix Equation Ax=b#^b8d6b7]]

The theorem said if $A$ have pivot in every row, then its column span $\mathbb{R}^{n}$.


Singular and number of pivot in column, square matrix, unique solution, no free variable, one-to-one and onto.

column space, spanning set , pivot in every row, consistent

---

$$
C=\begin{bmatrix}
0 & 0 & 0 \\
0 & 0 & 0
\end{bmatrix}
$$

$C(A)=0$
$N(A)=\mathbb{R}^{2}$

$N(A)$ is wrong

. The Nullspace: $N(C) = \mathbb{R}^3$ (The Correction)

This is where the trap is. Remember that the nullspace lives in the **domain** (the "input" side), while the column space lives in the **codomain** (the "output" side).

For a $2 \times 3$ matrix:

- The columns have **2 components**, so $C(C)$ is a subspace of $\mathbb{R}^2$.
    
- The vectors $\mathbf{x}$ that you multiply by the matrix must have **3 components** to match the 3 columns. Therefore, $N(C)$ must be a subspace of **$\mathbb{R}^3$**.
    

**The calculation:**

We want to find all $\mathbf{x} \in \mathbb{R}^3$ such that $C\mathbf{x} = \mathbf{0}$.

$$\begin{bmatrix} 0 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \\ x_3 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \end{bmatrix}$$

Since $0x_1 + 0x_2 + 0x_3 = 0$ is always true for **any** values of $x_1, x_2, x_3$, every single vector in $\mathbb{R}^3$ is in the nullspace.

==Rank-Nullity Theorem==

4)
The smallest subspace is $0$. While the biggest subspace is linear combination of $3\times 3$ diagonal matrix.

It is because diagonal matrix is both symmetric and lower triangular.

The smallest subspace that contained all symmetric and lower triangular matrix is wrong.

If you take a symmetric matrix (which can fill the upper triangle) and add it to a lower triangular matrix (which can fill the lower triangle), you can eventually produce **any entry** in a $3 \times 3$ matrix.

- **The smallest subspace is all $3 \times 3$ matrices ($M_{3 \times 3}$).** * Its dimension is 9.

---
### 1. "Smallest Subspace containing $S$ and $L$" $\to$ The Sum ($S + L$)

You mentioned the **union**, and you are logically on the right track, but there is a subtle mathematical trap here.

In vector spaces, the union of two subspaces ($S \cup L$) is almost **never** a subspace itself. Think of it like two crossing lines in $\mathbb{R}^2$. The union is just the "X" shape. If you add a vector from one line to a vector from the other, the resulting vector lands in the "empty space" between the lines.

To fix this, we need the **Sum** ($S + L$). This is the set of all possible additions: every $s \in S$ added to every $l \in L$.

- It is the **"smallest"** because any subspace that tries to hold both $S$ and $L$ _must_ also hold all their sums to satisfy the closure property.
    
- As we found, for $3 \times 3$ matrices, this "box" has to grow to all 9 dimensions to fit both types.
    

---

### 2. "Largest Subspace contained in both" $\to$ The Intersection ($S \cap L$)

This one is much more straightforward. If a subspace is "contained in both," every vector in it must satisfy the rules of $S$ **and** the rules of $L$ simultaneously.

- The intersection of any two subspaces is **always** a subspace.
    
- It is the **"largest"** because it contains every single vector that manages to live in both worlds. There's no room to add anything else without breaking one of the two rules.
    
- For your problem, the only matrices that are both symmetric and lower triangular are **diagonal matrices**.
---

5)
a)
Rule 7 and 6 is broken because, 

$$
2(\begin{bmatrix}
3 \\
1
\end{bmatrix}+\begin{bmatrix}
5 \\
0
\end{bmatrix})=2\begin{bmatrix}
9 \\
2
\end{bmatrix}=\begin{bmatrix}
18 \\
4
\end{bmatrix}
$$

$$
2(\begin{bmatrix}
3 \\
1
\end{bmatrix}+\begin{bmatrix}
5 \\
0
\end{bmatrix})=(\begin{bmatrix}
6 \\
2
\end{bmatrix}+\begin{bmatrix}
10 \\
0
\end{bmatrix})=\begin{bmatrix}
17 \\
3
\end{bmatrix}
$$

b) 
We need to show that the set satisft all the condition.
1) addition is closed
$x+y=xy$ which $xy\geq 0$. Thus, $xy \in \mathbb{R}^{+}$.

2) Commutative under addition
$x+y=xy=yx=y+x$

3) Associative under addition
$(x+y)+z=(xy)+z=(xy)z=x(yz)=x+(yz)=x+(y+z)$
4) There exist additive identity
Let $y=1$. Thus for any $x$, $x+y=x(1)=x$

Thus, the 'zero vector' is 1.

5) There exist additive inverse
Let $y=\frac{1}{x}$. Thus, for any $x \in V$, $x+y=x\left( \frac{1}{x} \right)=1$

Notice that $1$ is zero vector which is the addictive identity

6) Multiplication is closed
$cx=x^{c}$ which $x^{c} \in V$.

7) Multiplicative identity
Let $c=1$. Thus, for any $x \in V$, $cx=x^{c}=x^{1}=x$

8) Associative of scalar multiplication
$c_{1}(c_{2}x)=(x^{c_{2}})^{c_{1}}=x^{c_{2}c_{1}}=(c_{1}c_{2})x$.


9) Distributivity of Scalar Multiplication over Vector Addition
$c(x+y)=(x+y)^{c}=(xy)^{c}=x^{c}y^{c}$

10) Distributivity of Scalar Multiplication over Scalar Addition
$(c+d)x=x^{c+d}$
$(cx+dx)=x^{c}+x^{d}=x^{c}x^{d}=x^{c+d}$


**The Zero Vector:** In this space, the "zero vector" is the number **1**. Note that in a vector space, the term "zero vector" refers to the additive identity element, not necessarily the numerical value $0$.

c) 
The commutativity of addition 
The associativity of addition
The existence of zero vector
The existence of additive inverse

6)
$x+2y+z=0$
$P$ is not subspace of $\mathbb{R}^{3}$ because it didn't pass though the origin. (non homogeneous)

$P_{o}$ is a subspaces of $\mathbb{R}^{3}$.

==7)==
a) Yes
b) 

8)
One free variable, thus it is a line and a subspace form by one vector in term of $x_{2}$

Besides, it is nullspace of $A$. b,d,e

9)

Show that the set of nonsingular 2 by 2 matrices is not a vector space.

$$
\begin{bmatrix}
1 & 9 \\
0 & 2
\end{bmatrix}+\begin{bmatrix}
1 & 1 \\
2 & 8
\end{bmatrix}=\begin{bmatrix}
2 & 10 \\
2 & 10
\end{bmatrix}
$$

Since the addition is singular matrix. It follow that the addition is not closed.

Show also that the set of singular2 by 2 matrices is not a vector space.

$$
\begin{bmatrix}
1 & 2 \\
2 & 4
\end{bmatrix}+\begin{bmatrix}
3 & 3 \\
4 & 4
\end{bmatrix}=\begin{bmatrix}
4 & 5 \\
6 & 8
\end{bmatrix}
$$

Since the addition is nonsingular, it follow that the addition is not closed.

==Remark==

A more fundamental reason why the set of all $2\times 2$ singular matrix is not a vector space.
 Failure of Additive Identity (The Zero Vector)

Every vector space must contain a "zero vector." For the space of $2 \times 2$ matrices, this is the zero matrix:

$$\mathbf{0} = \begin{bmatrix} 0 & 0 \\ 0 & 0 \end{bmatrix}$$

However, the determinant of the zero matrix is $0$. Since a nonsingular matrix must have a non-zero determinant, the zero matrix is **not** in the set. If the identity element isn't there, the set cannot be a vector space.

10)
Zero vectors is additive identity which is

$$
\begin{bmatrix}
0 & 0 \\
0 & 0
\end{bmatrix}
$$

$$
\frac{1}{2}A=\begin{bmatrix}
1 & -1 \\
1 & -1
\end{bmatrix}
$$
$$
-A=\begin{bmatrix}
-2 & 2 \\
-2 & 2
\end{bmatrix}
$$
The set of $2\times 2$ matrix where can be express in this form

$$
V=\begin{bmatrix}
-a & a \\
-a & a
\end{bmatrix}
$$
where $a \in \mathbb{R}$. or

$$
V=2\begin{bmatrix}
a & -a \\
a & -a
\end{bmatrix}
$$

The smallest subspace containing $A$ is the spanning set of $A$.

11)
a)
The set of $2\times 2$ matrix where $a_{ij}=0$ for $ij>1$.

b)
Yes, because $I$ is a linear combination of $A$ and $B$. ($I$ is in the spanning set)

c)
The set of $2\times 2$ **off-diagonal matrices**.

12,13 is about function

14)
a)
$$
\begin{bmatrix}
c & d \\
0 & 0
\end{bmatrix}
$$
where $c,d \in \mathbb{R}$

b)
$$
\begin{bmatrix}
c+d & 0 \\
0 & d
\end{bmatrix}
$$
where $c,d \in \mathbb{R}$

c)
$$
\begin{bmatrix}
c & c \\
0 & 0
\end{bmatrix}
$$
where $c \in \mathbb{R}$

d)
$$
\begin{bmatrix}
a+b & a+c \\
0 & b+c
\end{bmatrix}
$$
where $a,b,c \in \mathbb{R}$

Or 
$$
\begin{bmatrix}
x & y \\
0 & z
\end{bmatrix}
$$
set of upper triangular matrix.


15,16)
$A(x+x')=0$
$A(x+x')=b+b'$


18) 
a) plane, line
b) line, point
c) The intersection of 2 subspace is a subspace.

19. The Zero Vector

Since $S$ and $T$ are both subspaces of $\mathbb{R}^5$, they both must contain the zero vector $\mathbf{0}$.

- $\mathbf{0} \in S$ (because $S$ is a subspace)
    
- $\mathbf{0} \in T$ (because $T$ is a subspace)
    

Since $\mathbf{0}$ is in both sets, **$\mathbf{0} \in S \cap T$**.

---

2. Closure under Addition ($\mathbf{x} + \mathbf{y}$)

Suppose we have two vectors $\mathbf{x}$ and $\mathbf{y}$ that are both in the intersection $S \cap T$. We need to show that their sum $\mathbf{x} + \mathbf{y}$ is also in the intersection.

- Because $\mathbf{x}, \mathbf{y} \in S$ and $S$ is closed under addition, then **$\mathbf{x} + \mathbf{y} \in S$**.
    
- Because $\mathbf{x}, \mathbf{y} \in T$ and $T$ is closed under addition, then **$\mathbf{x} + \mathbf{y} \in T$**.
    

Since the sum $\mathbf{x} + \mathbf{y}$ belongs to both $S$ and $T$, it follows that **$\mathbf{x} + \mathbf{y} \in S \cap T$**.

---

3. Closure under Scalar Multiplication ($c\mathbf{x}$)

Suppose we have a vector $\mathbf{x} \in S \cap T$ and any scalar $c \in \mathbb{R}$. We must show that $c\mathbf{x}$ remains in the intersection.

- Because $\mathbf{x} \in S$ and $S$ is closed under scalar multiplication, then **$c\mathbf{x} \in S$**.
    
- Because $\mathbf{x} \in T$ and $T$ is closed under scalar multiplication, then **$c\mathbf{x} \in T$**.
    

Since $c\mathbf{x}$ belongs to both $S$ and $T$, it follows that **$c\mathbf{x} \in S \cap T$**.

 Conclusion

Because the intersection $S \cap T$ contains the zero vector and is closed under both addition and scalar multiplication, it is a **subspace** of $\mathbb{R}^5$.

---
19) plane or $\mathbb{R}^{3}$

20)
a) Yes because the addition of skew-symmetric is also skew-symmetric
Suppose $A^{T}=-A$ and $B^{T}=-B$
$(A+B)^{T}=(A^{T}+B^{T})=-(A+B)$

b) No, it is possible that the addition is symmetric matrix, and it does not have zero vector.

c) Let $v=(1,1,1)$ We are looking the set $\{ A \in M:Av=0 \}$

Suppose 2 matrix $Av=0$ and $Bv=0$
$$
(A+B)v=Av+Bv=0
$$
$cA(v)=c 0=0$

Thus, it is true.

21)

