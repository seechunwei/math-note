
7)
### Diagonal Matrix

Before define what is diagonal matrix, we need to define what is diagonal first

Diagonal of $A$ is the entries $a_{ij}$ where $i=j$. Thus, even though the matrix is not square, it still have diagonal.

But notice that diagonal matrix is a square matrix where its entries $a_{ij}=0$ where $i \neq j$.. For example,

$$
\begin{bmatrix}
a_{11} & 0 & 0 \\
0 & a_{22} & 0 \\
0 & 0 & a_{33}
\end{bmatrix}
$$

Why diagonal matrix need to be square. Because of its algebraic properties.
1) Determinant 
- Only square matrix have determinant and for a diagonal matrix its determinant is just the product of its diagonal entries.
2) - **Invertibility:** A square diagonal matrix is invertible if and only if all its diagonal entries are non-zero. (Non zero Pivot)
- **Eigenvalues:** For square diagonal matrices, the entries on the diagonal _are_ the eigenvalues.

### Symmetrix matrix
A square matrix $A$ is **symmetric** if it is equal to its own transpose. Essentially, the matrix is a "mirror image" across its main diagonal.

- **Formal Definition:** $A = A^T$, which implies $a_{ij} = a_{ji}$ for all $i, j$.
- **Main Diagonal:** The entries on the main diagonal can be anything.

$$A = \begin{bmatrix} \mathbf{1} & 2 & 3 \\ 2 & \mathbf{5} & 4 \\ 3 & 4 & \mathbf{9} \end{bmatrix}$$

### Skew-Symmetric Matrix

A square matrix $A$ is **skew-symmetric** if its transpose is equal to its negative.

**Formal Definition:** $A^T = -A$, which implies $a_{ij} = -a_{ji}$ for all $i, j$.

But what happen to the diagonal?
$$
\begin{align}
a_{ii}&=-a_{ii} \\
2a_{ii}&=0 \\
a_{ii}&=0
\end{align}
$$

Thus, its diagonal entries is always equal to 0.

$$
\begin{bmatrix}
0 & 2 & 3 \\
-2 & 0 & 4 \\
-3 & -4 & 0
\end{bmatrix}
$$

### Upper triangle matrix

$a_{ij}=0$ if $i>j$

$$
\begin{bmatrix}
1 & 2 & 3 \\
0 & 5 & 6 \\
0 & 0 & 7
\end{bmatrix}
$$

10)
a) True
It because the $ab_{i}=Ab_{i}$ since $b_{{1}}=b_{3}$, it follow that $Ab_{1}=Ab_{3}$ and $ab_{1}=ab_{3}$.


b) False

Let $AB=$
$$
\begin{align}
\begin{bmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{bmatrix}\begin{bmatrix}
1 \\
2 \\
1
\end{bmatrix}= \begin{bmatrix}
a_{1}B \\
a_{2}B \\
a_{3}B
\end{bmatrix}
\end{align}
$$

Since $a_{1}B=(1,4,3)$ and $a_{3}B=(7,16,9)$. Thus, it follow that $a_{1}B=a_{3}B$

$B$ is fixed if we view the multiplication of matrix as combination of $B$, thus the entries of $B$ does not effect the equality of row of $AB$.

c) True
Argument same as a)

d)
$$
\begin{align}
(AB)^{2}&=(AB)(AB) \\
&\neq A^{2}B^{2}
\end{align}
$$

For example,

$$
\begin{align}AB&=
\begin{bmatrix}
1 & 1 & 1
\end{bmatrix}\begin{bmatrix}
1  \\
1 \\
1
\end{bmatrix}
\end{align}
$$
Note that $A^{2}$ and $B^{2}$ does not exist. Thus, $(AB)^{2} \neq A^{2}B^{2}$ it is a counterexample.

11)
The first row of $AB$ is 

$$
\begin{align}
a_{1}B&=\begin{bmatrix}
2 & 1 & 4
\end{bmatrix}\begin{bmatrix}
1 & 1 \\
0 & 1 \\
1 &  0
\end{bmatrix} \\
&=\begin{bmatrix}
6 & 3
\end{bmatrix}
\end{align}
$$

12)
Prove that the product of two lower triangular matrices is again lower triangular.

Proof:
Suppose 2 arbitrary lower triangle matrix $A$ and $B$ which $AB$ and $BA$ exist(square matrix). Let assume their size is $m\times m$ 

Thus, the $(i,j)$ entry of $AB$ is 
$$
ab_{ij}=\sum_{s=1}^{m} a_{is}b_{sj}
$$

We need to prove that $ab_{ij}=0$ when $i<j$. 

Assume $i<j$. Suppose $i\geq s$ and $s\geq j$. Note that it is a contradiction, thus $i<s$ or $s<j$. Since $a_{is}=0$ if $i<s$ and $b_{sj}=0$ if $s<j$. 
(or we can split in to 2 cases where $i<s$ or $s\leq i\to s<j$)

Therefore, in either case the term in the summation

$$
ab_{ij}=\sum_{s=1}^{m} a_{is}b_{sj}=0
$$

Thus, $ab_{ij}=0$ if $i<j$. Q.E.D

13)
a)
$A^{2}=-I$
$$
\begin{align}
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}&=\begin{bmatrix}
a^{2}+bc& ab+bd \\
ca+cd & bc+d^{2}
\end{bmatrix}
\end{align}
$$

$$
\begin{align}
a^{2}+bc&=-1 \\
ab+bd&=0 \\
ca+cd&=0 \\
bc+d^{2}&=-1
\end{align}
$$

$$
\begin{align}
b(a+d)&=0 \\
c(a+d)&=0
\end{align}
$$

if $b=0$ and $c=0$, then $a^{2}=-1$ and $d^{2}=-1$ which is contradiction. Thus, $(a+d)=0$ which means that $a$ and $d$ are addictive inverse.

and $a^{2}+bc=-1$



For example
$$
\begin{align}
A^{2}&=\begin{bmatrix}
-1 & -2 \\
1 & 1
\end{bmatrix}\begin{bmatrix}
-1 & -2 \\
1 & 1
\end{bmatrix} \\
&= \begin{bmatrix}
-1 & 0 \\
0 & -1
\end{bmatrix}
\end{align}
$$

b)
$B^{2}=0,B\neq 0$

Let 
$$
B=\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
$$

$$
\begin{align}
a^{2}+bc&=0 \\
b(a+d)&=0 \\
c(a+d)&=0 \\
bc+d^{2}&=0
\end{align}
$$

If $b=0$ and $c=0$ then $a=0$ and $d=0$. Since $B\neq 0$, thus contradiction. Thus $a=-d$ and $a^{2}+bc=0$.


$$
\begin{align}
B^{2}&=\begin{bmatrix}
1 & 1 \\
-1 & -1
\end{bmatrix} \begin{bmatrix}
 1 & 1 \\
-1 & -1
\end{bmatrix} \\
&=\begin{bmatrix}
0 &  0 \\
0 & 0
\end{bmatrix}
\end{align}
$$


==c)==

$CD=-DC$ and $CD \neq 0$

$$CD=\begin{bmatrix}
c_{11} & c_{12} \\
c_{21} & c_{22}
\end{bmatrix}\begin{bmatrix}
d_{11} & d_{12} \\
d_{21} & d_{22}
\end{bmatrix}
$$

$$
c_{11}d_{11}+c_{12}d_{21}=-()
$$


d)
$EF=0$ $(E)_{ij}\neq 0$ and $(F)_{ij} \neq 0$

$$
EF=\begin{bmatrix}
1 & 1 \\
1 & 1
\end{bmatrix}\begin{bmatrix}
1 & 1 \\
-1 & -1
\end{bmatrix}
$$


14)
$EA$
The first row of $EA$ form by first row of $A$ plus 7 times the second row of $A$.
The second row of $EA$ form by second row of $A$.

$AE$
The first column of $AE$ form by first column of $A$.
The second column form by 7 times the first column of $A$ plus second column of $B$.

15)
$$
\begin{align}
\begin{bmatrix}
a & 0 \\
c & 0
\end{bmatrix}=\begin{bmatrix}
a & b \\
0 & 0
\end{bmatrix}
\end{align}
$$

$b=0$ and $c=0$

$$
\begin{bmatrix}
0 & a \\
0 & c
\end{bmatrix}=\begin{bmatrix}
 c & d \\
 0 & 0
\end{bmatrix}
$$

$a=d$.


If $AB=BA$ for all matrices B, then A is a multiple of the identity.



==20)==


32）
a)
$x=2y\to x-2y=0$ 
$x+y=39$

$$
\begin{align}
\begin{bmatrix}
1 & -2 & 0 \\
1 & 1 & 39
\end{bmatrix} &\implies R^{1}_{2}(-1) \begin{bmatrix}
1 & -2 & 0 \\
0 & 3 & 30
\end{bmatrix} \\
&\implies R_{2}\left( \frac{1}{3} \right)\begin{bmatrix}
1 & -2 & 0 \\
0 & 1 & 13
\end{bmatrix} \\
&\implies R^{2}_{1}(2)\begin{bmatrix}
1 & 0 & 26 \\
0 & 1 & 13
\end{bmatrix}
\end{align}
$$
$x=26$ and $y=13$

---
### Block multiplication

**Block multiplication** (or partitioned matrix multiplication) is a method where you divide large matrices into smaller submatrices, called **blocks**, and treat these blocks as if they were individual elements when performing multiplication.

## How It Works

Imagine you have two matrices, $A$ and $B$, which are too large to handle conveniently. You can partition them into smaller submatrices:

$$A = \begin{bmatrix} A_{11} & A_{12} \\ A_{21} & A_{22} \end{bmatrix}, \quad B = \begin{bmatrix} B_{11} & B_{12} \\ B_{21} & B_{22} \end{bmatrix}$$

If the dimensions of the blocks are compatible (meaning the number of columns in the left-hand blocks matches the number of rows in the right-hand blocks), the product $C = AB$ is calculated using the standard "row-by-column" rule, but applied to the blocks themselves:

$$C = \begin{bmatrix} A_{11}B_{11} + A_{12}B_{21} & A_{11}B_{12} + A_{12}B_{22} \\ A_{21}B_{11} + A_{22}B_{21} & A_{21}B_{12} + A_{22}B_{22} \end{bmatrix}$$

---

## Critical Requirements: Conformability

For block multiplication to work, the "inner" dimensions of the blocks must align. Specifically:

- The number of columns in $A_{11}$ must equal the number of rows in $B_{11}$.
    
- The number of columns in $A_{12}$ must equal the number of rows in $B_{21}$.
    
- This pattern must hold for every block product in the resulting matrix.

## 1. The Matrices and the "Cut"

We will partition $A$ after the second column and $B$ after the second row.

$$A = \left[ \begin{array}{cc|c} 1 & 2 & 1 \\ 3 & 4 & 0 \end{array} \right], \quad B = \left[ \begin{array}{cc} 1 & 0 \\ 0 & 1 \\ \hline 2 & 3 \end{array} \right]$$

Now, let's name these blocks:

- **$A_{1}$:** The $2 \times 2$ identity-like block $\begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}$
    
- **$A_{2}$:** The $2 \times 1$ column vector $\begin{bmatrix} 1 \\ 0 \end{bmatrix}$
    
- **$B_{1}$:** The $2 \times 2$ identity block $\begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}$
    
- **$B_{2}$:** The $1 \times 2$ row vector $\begin{bmatrix} 2 & 3 \end{bmatrix}$
    

---

## 2. The Dimension Check (Conformability)

Before we multiply, we must ensure the "inner" dimensions match for every block product.

- **For $A_{1}B_{1}$:** $A_{1}$ is $(2 \times \mathbf{2})$ and $B_{1}$ is $(\mathbf{2} \times 2)$. They match! Result is $2 \times 2$.
    
- **For $A_{2}B_{2}$:** $A_{2}$ is $(2 \times \mathbf{1})$ and $B_{2}$ is $(\mathbf{1} \times 2)$. They match! Result is $2 \times 2$.
    

Since both results are $2 \times 2$, we can add them together. **If the vertical cut in $A$ did not match the horizontal cut in $B$, the multiplication would be impossible.**

## 3. The Calculation

Now we compute the product $C = A_{1}B_{1} + A_{2}B_{2}$:

**Step A: Calculate $A_{1}B_{1}$**

$$\begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}$$

**Step B: Calculate $A_{2}B_{2}$**

$$\begin{bmatrix} 1 \\ 0 \end{bmatrix} \begin{bmatrix} 2 & 3 \end{bmatrix} = \begin{bmatrix} 1(2) & 1(3) \\ 0(2) & 0(3) \end{bmatrix} = \begin{bmatrix} 2 & 3 \\ 0 & 0 \end{bmatrix}$$

**Step C: Add them together**

$$C = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} + \begin{bmatrix} 2 & 3 \\ 0 & 0 \end{bmatrix} = \mathbf{\begin{bmatrix} 3 & 5 \\ 3 & 4 \end{bmatrix}}$$

---

