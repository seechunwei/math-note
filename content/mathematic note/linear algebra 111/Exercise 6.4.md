1)

Let $u_{1}=\begin{bmatrix}3 \\ 0 \\ -1\end{bmatrix},u_{2}=\begin{bmatrix}8 \\ 5 \\ -6\end{bmatrix}$. Given $\{ u_{1},u_{2} \}$ is a basis for a subspace $W$. We need to construct an orthogonal basis $\{ v_{1},v_{2} \}$ for $W$. 

Let $v_{1}=u_{1}$ and let 

$$
\begin{align}
v_{2}&=u_{2}- \frac{u_{2}\cdot v_{1}}{v_{1}\cdot v_{1}}v_{1} \\
&= \begin{bmatrix}
8 \\
5 \\
-6
\end{bmatrix}- \frac{30}{10}\begin{bmatrix}
3 \\
0 \\
-1
\end{bmatrix} \\
&=\begin{bmatrix}
8 \\
5 \\
-6
\end{bmatrix}- \begin{bmatrix}
9 \\
0 \\
-3
\end{bmatrix} \\
&= \begin{bmatrix}
-1 \\
5 \\
-3
\end{bmatrix}
\end{align}
$$

Thus, By theorem 14 $\{ v_{1},v_{2} \}$ is an orthogonal basis for $W$.

3)

Let $u_{1}=\begin{bmatrix}2 \\ -5 \\ 1\end{bmatrix},u_{2}=\begin{bmatrix}4 \\ -1 \\ 2\end{bmatrix}$. Given $\{ u_{1},u_{2} \}$ is a basis for a subspace $W$. We need to construct an orthogonal basis $\{ v_{1},v_{2} \}$ for $W$. 

Let $v_{1}=u_{1}$ and let 

$$
\begin{align}
v_{2}&=u_{2}- \frac{u_{2}\cdot v_{1}}{v_{1}\cdot v_{1}}v_{1} \\
&= \begin{bmatrix}
4 \\
-1 \\
2
\end{bmatrix}- \frac{15}{30} \begin{bmatrix}
2 \\
-5 \\
1
\end{bmatrix} \\
&=\begin{bmatrix}
4 \\
-1 \\
2
\end{bmatrix} -\begin{bmatrix}
1 \\
-\frac{5}{2} \\
\frac{1}{2}
\end{bmatrix} \\
&=\begin{bmatrix}
3 \\
\frac{3}{2} \\
\frac{3}{2}
\end{bmatrix}
\end{align}
$$
Thus, By theorem 14 $\{ v_{1},v_{2} \}$ is an orthogonal basis for $W$.

6)
It is the same as Q1 and Q3

7)
Since $\{ v_{1},v_{2} \}$ is the orthogonal basis for $W$, we just need to normalize each vector in the set to get orthonormal basis for $W$.

To simplify the arithmetic , scale $v_{2}$ by letting $v_{2}'=2v_{2}$ 

$$
v_{2}'=2v_{2}=\begin{bmatrix}
6 \\
3 \\
3
\end{bmatrix}
$$

Normalizing $v_{1}$:

$$
\begin{align}
\frac{v_{1}}{||v_{1}||}&=\frac{1}{\sqrt{ 30 }} \begin{bmatrix}
2 \\
-5 \\
1
\end{bmatrix} \\
&= \begin{bmatrix}
 \frac{2}{\sqrt{ 30 }} \\
-\frac{5}{\sqrt{ 30 }} \\
\frac{1}{\sqrt{ 30 }}
\end{bmatrix}
\end{align}
$$

Normalizing $v_{2}'$:

$$
\begin{align}
\frac{v_{2}'}{||v_{2}||}&= \frac{1}{3\sqrt{ 6 }} \begin{bmatrix}
6 \\
3 \\
3
\end{bmatrix} \\
&=\begin{bmatrix}
\frac{2}{\sqrt{ 6 }} \\
\frac{1}{\sqrt{ 6 }} \\
\frac{1}{\sqrt{ 6 }}
\end{bmatrix}
\end{align}
$$

Thus, Let $w_{1}= \frac{u_{1}}{||u_{1}||}$ and $w_{2}= \frac{u_{2}'}{||u_{2}'||}$. Hence, $\{ w_{1},w_{2} \}$ is the orthonormal basis for $W$.


10)
Let
$$
A=\begin{bmatrix}
-1 & 6 & 6 \\
3 & -8 & 3 \\
1 & -2 & 6 \\
1 & -4 & -3
\end{bmatrix}
$$

Let $a_{i}$ denote the $i-th$ columns of $A$. Thus, $\{ a_{1}.a_{2}.a_{3} \}$ is the basis for $\text{Col}A$. 

We need to find an orthogonal basis $\{ v_{2},v_{2},v_{3} \}$ for $\text{Col}A$ using Gram-Schmidt Process.

Let $v_{1}=a_{1}$, and

$$
\begin{align}
v_{2}&= a_{2}- \frac{a_{2}\cdot v_{1}}{v_{1}\cdot v_{1}} v_{1}\\
&= \begin{bmatrix}
6 \\
-8 \\
-2 \\
-4
\end{bmatrix}- \frac{-36}{12}\begin{bmatrix}
-1 \\
3 \\
1 \\
1
\end{bmatrix} \\
&=\begin{bmatrix}
6 \\
-8 \\
-2 \\
-4
\end{bmatrix}+3\begin{bmatrix}
-1 \\
3 \\
1 \\
1
\end{bmatrix} \\
&=\begin{bmatrix}
3 \\
1 \\
1 \\
-1
\end{bmatrix}
\end{align}
$$

$$
\begin{align}
v_{3}&= a_{3}- \frac{a_{3}\cdot v_{1}}{v_{1}\cdot v_{1}}v_{1}- \frac{a_{3}\cdot v_{2}}{v_{2}\cdot v_{2}}v_{2} \\
&=\begin{bmatrix}
6 \\
3 \\
6 \\
-3
\end{bmatrix}- \frac{6}{12} \begin{bmatrix}
-1 \\
3 \\
1 \\
1
\end{bmatrix}- \frac{30}{12} \begin{bmatrix}
3 \\
1 \\
1 \\
-1
\end{bmatrix} \\
&=\begin{bmatrix}
6 \\
3 \\
6 \\
-3
\end{bmatrix}- \begin{bmatrix}
-\frac{1}{2} \\
\frac{3}{2} \\
\frac{1}{2} \\
\frac{1}{2}
\end{bmatrix}- \begin{bmatrix}
\frac{15}{2} \\
\frac{5}{2} \\
\frac{5}{2} \\
-\frac{5}{2}
\end{bmatrix} \\
&= \begin{bmatrix}
-1 \\
-1 \\
3 \\
-1
\end{bmatrix}
\end{align}
$$
Verification:

$v_3 \cdot v_1 = 1 - 3 + 3 - 1 = 0$ 
$v_3 \cdot v_2 = -3 - 1 + 3 + 1 = 0$


Extra exercise
13) ^330bf0

Given $$
A=\begin{bmatrix}5 & 9 \\ 1 & 7 \\ -3 & -5 \\ 1 & 5\end{bmatrix},Q=\begin{bmatrix}
\frac{5}{6} & -\frac{1}{6} \\
\frac{1}{6} & \frac{5}{6} \\
-\frac{3}{6} & \frac{1}{6} \\
\frac{1}{6} & \frac{3}{6}
\end{bmatrix}
$$
where the columns of $Q$  obtained by applying the Gram Schmidt process to the columns of $A$. 

Thus, the columns of $Q$ is orthogonal implies that $Q^{T}A=R$. Thus,

$$
\begin{align}
R&=\begin{bmatrix}
\frac{5}{6} & \frac{1}{6} & -\frac{3}{6} & \frac{1}{6} \\
-\frac{1}{6} & \frac{5}{6} & \frac{1}{6} & \frac{3}{6}
\end{bmatrix} \begin{bmatrix}
5 & 9 \\
1 & 7 \\
-3 & -5 \\
1 & 5
\end{bmatrix} \\
&= \begin{bmatrix}
6 & 12 \\
0 & 6
\end{bmatrix}
\end{align}
$$

27)

Suppose $A=QR$ is a factorization of an $m\times n$ matrix $A$ (with linearly independent columns). Partition $A$ as $\begin{bmatrix}A_{1} & A_{2}\end{bmatrix}$, where $A_{1}$ has $p$ columns. Show how to obtain a $QR$ factorization of $A_{1}$, and explain why your factorization has the appropriate properties.

Partition $A$ as $\begin{bmatrix}A_{1} & A_{2}\end{bmatrix}$ means that the union of this 2 matrix is the columns of $A$ (with the condition that $A_{1}\cap A_{2}=0$). This only guarantee they are different matrix, so the question add on another condition (the columns of $A$ is linearly independent).

Assume that $A_{1}$ has $p$ columns and $A_{2}$ has $n-p$ columns. 

To match this structure, we partition $Q$ and $R$ based on their columns and rows:

- Partition $Q$ by columns into $Q_1$ (first $p$ columns) and $Q_2$ (remaining $n-p$ columns):
    
    $$Q = \begin{bmatrix} Q_1 & Q_2 \end{bmatrix}$$
    
- Partition $R$ into blocks such that the dimensions match the multiplication:
    
    $$R = \begin{bmatrix} R_{11} & R_{12} \\ 0 & R_{22} \end{bmatrix}$$
    
    where $R_{11}$ is a $p \times p$ matrix, $R_{12}$ is $p \times (n-p)$, the bottom-left block is a $(n-p) \times p$ zero matrix (since $R$ is upper triangular), and $R_{22}$ is $(n-p) \times (n-p)$.

By the rules of block multiplication, we multiply the rows of the first matrix by the columns of the second:

$$\begin{bmatrix} A_1 & A_2 \end{bmatrix} = \begin{bmatrix} Q_1 R_{11} + Q_2 (0) & Q_1 R_{12} + Q_2 R_{22} \end{bmatrix}$$

$$\begin{bmatrix} A_1 & A_2 \end{bmatrix} = \begin{bmatrix} Q_1 R_{11} & Q_1 R_{12} + Q_2 R_{22} \end{bmatrix}$$

By equating the first block on both sides, we get:

$$A_1 = Q_1 R_{11}$$

This gives us our candidate QR factorization for $A_1$.

### 3. Verification of Appropriate Properties

To prove that $A_1 = Q_1 R_{11}$ is a valid QR factorization, we must check that $Q_1$ and $R_{11}$ satisfy the formal definitions:

- **Dimensions match:** $A_1$ is $m \times p$. $Q_1$ is $m \times p$, and $R_{11}$ is $p \times p$. The dimensions are perfectly appropriate for a QR factorization of an $m \times p$ matrix.
    
- **Orthonormal columns of $Q_1$:** Since the columns of $Q$ are orthonormal, any subset of its columns must also be orthonormal. Mathematically, since $Q^T Q = I_n$, we have:
    
    $$Q^T Q = \begin{bmatrix} Q_1^T \\ Q_2^T \end{bmatrix} \begin{bmatrix} Q_1 & Q_2 \end{bmatrix} = \begin{bmatrix} Q_1^T Q_1 & Q_1^T Q_2 \\ Q_2^T Q_1 & Q_2^T Q_2 \end{bmatrix} = \begin{bmatrix} I_p & 0 \\ 0 & I_{n-p} \end{bmatrix}$$
    
    Looking at the top-left block, $Q_1^T Q_1 = I_p$, which confirms that the columns of $Q_1$ are orthonormal.
    
- **Upper triangular structure of $R_{11}$:** Since $R$ is an upper triangular matrix, its submatrix $R_{11}$ (which lies entirely on and above the main diagonal of $R$) must also be upper triangular.
    
- **Invertibility / Positive diagonal entries:** The diagonal entries of $R_{11}$ are exactly the first $p$ diagonal entries of $R$. Since $A$ has linearly independent columns, all diagonal entries of $R$ are strictly positive (and non-zero), meaning $R_{11}$ is invertible with strictly positive diagonal entries.

> [!question]
> How to we determine the partition of $Q$ and $R$?
> ### 1. Why $Q$ is partitioned into $\begin{bmatrix} Q_1 & Q_2 \end{bmatrix}$
> 
> We are told that $A$ is partitioned by columns into $A = \begin{bmatrix} A_1 & A_2 \end{bmatrix}$, where $A_1$ has $p$ columns.
> 
> When you multiply two matrices $Q$ and $R$ to get $A$, the columns of the result are combinations of the columns of $Q$. To make the blocks line up directly with $A_1$ and $A_2$:
> 
> - $A_1$ has $p$ columns, so the first block of $Q$ ($Q_1$) must look at the first $p$ columns.
>     
> - $A_2$ has the remaining $n-p$ columns, so the second block of $Q$ ($Q_2$) takes the remaining $n-p$ columns.
>     
> 
> Because we only split $Q$ vertically along its columns, it looks like a single row of blocks:
> 
> $$Q = \begin{bmatrix} Q_1 & Q_2 \end{bmatrix}$$
> 
> ### 2. Why $R$ must be partitioned into 4 blocks
> 
> To multiply $Q$ and $R$ using block multiplication, the **horizontal splitting of $R$ (rows) must perfectly match the vertical splitting of $Q$ (columns)**.(This follow by the dimension of multiplication of matrix)
> 
> Since $Q$ was split vertically after $p$ columns, $R$ **must** be split horizontally after $p$ rows.
> 
> Additionally, because $R$ is an $n \times n$ square matrix, splitting its rows after $p$ rows means we generally split its columns after $p$ columns as well to keep the diagonal structures intact. This cuts $R$ into a $2 \times 2$ grid of blocks:
> 
> $$R = \begin{bmatrix} R_{11} & R_{12} \\ R_{21} & R_{22} \end{bmatrix}$$
> 
> ### 3. Finding the Dimensions of $R$'s Blocks
> 
> Since $R$ is $n \times n$, and we cut it after $p$ rows and $p$ columns:
> 
> - **Rows:** The top blocks have $p$ rows; the bottom blocks have $n - p$ rows.
>     
> - **Columns:** The left blocks have $p$ columns; the right blocks have $n - p$ columns.
>     
> 
> Combining rows $\times$ columns gives us the exact dimensions:
> 
> - $R_{11}$ is $(\text{top rows}) \times (\text{left columns}) = p \times p$
>     
> - $R_{12}$ is $(\text{top rows}) \times (\text{right columns}) = p \times (n-p)$
>     
> - $R_{21}$ is $(\text{bottom rows}) \times (\text{left columns}) = (n-p) \times p$
>     
> - $R_{22}$ is $(\text{bottom rows}) \times (\text{right columns}) = (n-p) \times (n-p)$
>     
> 
> ### 4. Why the bottom-left block ($R_{21}$) is $0$
> 
> The original matrix $R$ is **upper triangular**, meaning every entry strictly below the main diagonal is zero.
> 
> Let's look at where the block $R_{21}$ sits. It occupies rows $p+1$ down to $n$, and columns $1$ down to $p$.
> 
> - For any element $R_{ij}$ inside this block, its row index $i$ is always greater than $p$ ($i \ge p+1$).
>     
> - Its column index $j$ is always less than or equal to $p$ ($j \le p$).
>     
> 
> Since $i > p \ge j$, we have $i > j$ for every single entry in this block. By definition of an upper triangular matrix, any entry where the row index is greater than the column index ($i > j$) must be $0$.
> 
> Therefore, the entire $R_{21}$ block is filled with zeros, allowing us to write it definitively as:
> 
> $$R = \begin{bmatrix} R_{11} & R_{12} \\ 0 & R_{22} \end{bmatrix}$$

> [!remark]
> If we equate the second block, we get:
> 
> $$A_2 = Q_1 R_{12} + Q_2 R_{22}$$
> 
> ### Why this isn't a QR factorization for $A_2$
> 
> A standard QR factorization requires a matrix to equal an orthogonal matrix multiplied by _one_ upper triangular matrix ($A = QR$).
> 
> For $A_2$, the expression $Q_1 R_{12} + Q_2 R_{22}$ is a sum of two different matrix products. You can factor out the $Q$ terms by writing it back in a block form:
> 
> $$A_2 = \begin{bmatrix} Q_1 & Q_2 \end{bmatrix} \begin{bmatrix} R_{12} \\ R_{22} \end{bmatrix} = Q \begin{bmatrix} R_{12} \\ R_{22} \end{bmatrix}$$
> 
> While $Q$ has orthonormal columns, the matrix $\begin{bmatrix} R_{12} \\ R_{22} \end{bmatrix}$ is a tall rectangular matrix ($n \times (n-p)$). Because the top block $R_{12}$ is generally full of non-zero entries, this combined matrix is **not upper triangular** in the standard sense.
> 
> ### How do you actually get a QR factorization for $A_2$?
> 
> If you explicitly need the QR factorization of $A_2$ alone, you cannot just slice up the QR factorization of $A$. Instead, you have two options:
> 
> 1. **Run Gram-Schmidt from scratch:** Treat the columns of $A_2$ as a brand-new set of vectors and run the Gram-Schmidt process directly on them.
>     
> 2. **Permute the columns first:** If you want to use the overall QR property, you would have to rearrange the columns of $A$ so that the columns of $A_2$ come first, forming a new matrix $A' = \begin{bmatrix} A_2 & A_1 \end{bmatrix}$, and then compute a brand-new QR factorization for $A'$.

    

