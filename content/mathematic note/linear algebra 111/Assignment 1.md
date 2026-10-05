1)
a)
First Method (By Matrix Multiplication)

$$
\begin{align}
A&=\begin{bmatrix}
1 & 2 & 3 \\
1 & 1 & 1 \\
2 & 2 & 3
\end{bmatrix} \\
&\xrightarrow[R^{1}_{3}(-2)]{R^{1}_{2}(-1)}\begin{bmatrix}
1 & 2 & 3 \\
0 & -1 & -2 \\
0 & -2 & -3
\end{bmatrix} \\
&\xrightarrow[]{R^{2}_{3}(-2)}\begin{bmatrix}
1 & 2 & 3 \\
0 & -1 & -2  \\
0 & 0 & 1
\end{bmatrix}
\end{align}
$$

Thus, there exist a sequence of elementary matrix such that

$$
E^{2}_{3}(-2)E^{1}_{3}(-2)E^{1}_{2}(-1)A=U
$$

Since $[E^{i}_{j}(\alpha)]^{-1}=E^{i}_{j}(-\alpha)$, from the book we know that 

$$
\begin{align}
L&=[E^{2}_{3}(-2)E^{1}_{3}(-2)E^{1}_{2}(-1)]^{-1} \\
&=E^{1}_{2}(1)E^{1}_{3}(2)E^{2}_{3}(2)
\end{align}
$$


Thus,

$$
\begin{align}
L&=\begin{bmatrix}
1 & 0 & 0 \\
1 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix}\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
2 & 0 & 1
\end{bmatrix}\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 2 & 1
\end{bmatrix} \\
&=\begin{bmatrix}
1 & 0 & 0 \\
1 & 1 & 0 \\
2 & 0 & 1
\end{bmatrix}\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 2 & 1
\end{bmatrix} \\
&=\begin{bmatrix}
1 & 0 & 0 \\
1 & 1 & 0 \\
2 & 2 & 1
\end{bmatrix}
\end{align}
$$


> [!info] Observation
"Let the multiplier $l_{ij}$ be defined as the scalar used to eliminate the entry in the $i$-th row and $j$-th column. Specifically, if we perform $R^{i}_{j}(-\alpha)$, we define $l_{ij} = \alpha$
>
Notice that each multiplier is the correspond $(i,j)$-entry of $L$. It is because the inverse of row operation doesn't interfere with each other. 
>
This lead to the second method.

<div class="page-break" style="page-break-before: always;"></div>


Second Method (By Multiplier)


We perform a sequence of row replacement operation (add multiple of row to another row) to reduce $A$ to $U$ and each of the multiplier is the correspond  $(i,j)$-entry of $L$ under diagonal.

Since $A$ has 3 rows, it follow that $L$ is a $3\times 3$ matrix.

$$L = \begin{bmatrix} 1 & 0 & 0 \\ l_{21} & 1 & 0 \\ l_{31} & l_{32} & 1 \end{bmatrix}$$


From first method, the elementary row operation implies that $l_{12}=1$, $l_{13}=2$ and $l_{23}=2$. 

Notice that there is another way to obtained this multiplier (Textbook approach) . From method 1, we know that


$$
\begin{align}
A&=\begin{bmatrix}
1 & 2 & 3 \\
1 & 1 & 1 \\
2 & 2 & 3
\end{bmatrix} \\
&\sim\begin{bmatrix}
1 & 2 & 3 \\
0 & -1 & -2 \\
0 & -2 & -3
\end{bmatrix} \\
&\sim\begin{bmatrix}
1 & 2 & 3 \\
0 & -1 & -2  \\
0 & 0 & 1
\end{bmatrix}
\end{align}
$$
The $j=th$ column of $L$ is the $j-th$ column of $A$ divided by the top pivot entry. It is because each entry we get is actually the scalar multiplier used to eliminate the entry.

Thus, 
The first column of $L$ is
$$
÷(1)\begin{bmatrix}
1 \\
1 \\
2
\end{bmatrix}= \begin{bmatrix}
1 \\
1 \\
2
\end{bmatrix}
$$
The second column of $L$ is

$$
÷(-1)\begin{bmatrix}
-1 \\
-2
\end{bmatrix}=\begin{bmatrix}
1 \\
2
\end{bmatrix}
$$

The third column of $L$ is

$$
\begin{bmatrix}
1
\end{bmatrix}
$$


Thus,

$$
L=\begin{bmatrix}
1 & 0 & 0 \\
1 & 1 & 0 \\
2 & 2 & 1
\end{bmatrix}
$$

---
<div class="page-break" style="page-break-before: always;"></div>

b)
The given system of linear equation can be express as $Ax=b$ defined as

$$
\begin{bmatrix}
1 & 2 & 3 \\
1 & 1 & 1 \\
2 & 2 & 3
\end{bmatrix}\begin{bmatrix}
x \\
y \\
z
\end{bmatrix}=\begin{bmatrix}
1 \\
2 \\
3
\end{bmatrix}
$$

Notice that from $1)a)$ , $A=LU$ such that


$$
\begin{align}
\begin{bmatrix}
1 & 2 & 3 \\
1 & 1 & 1 \\
2 & 2 & 3
\end{bmatrix} &= \begin{bmatrix}
1 & 0 & 0 \\
1 & 1 & 0 \\
2 & 2 & 1
\end{bmatrix}\begin{bmatrix}
1 & 2 & 3 \\
0 & -1 & -2 \\
0 & 0 & 1
\end{bmatrix}
\end{align}
$$

Thus,

$$
\begin{align}
Ax&=b \\
(LU)x&=b \\
L(Ux)&=b
\end{align}
$$

Let $Ux=c$ and we need to solve
1) $Lc=b$
2) $Ux=b$.


Step 1: Solve $Lc=b$

Let $L_{i}$ denote the $i-th$ column of $L$. By Theorem 3 in section 1.4. It follow that this equation has the same solution set as

$$
\begin{bmatrix}
L_{1} & L_{2} & L_{3} & b
\end{bmatrix}
$$

Thus,

$$
\begin{align}
\begin{bmatrix}
1 & 0 & 0  & 1\\
1 & 1 & 0  & 2\\
2 & 2 & 1 & -3
\end{bmatrix} &\xrightarrow[R^{1}_{3}(-2)]{R^{1}_{3}(-1)} \begin{bmatrix}
1 & 0 & 0 & 1 \\
0 & 1 & 0 & 1 \\
0 & 2 & 1 & -5
\end{bmatrix} \\
&\xrightarrow[]{R^{2}_{3}(-2)} \begin{bmatrix}
1 & 0 & 0 & 1 \\
0 & 1 & 0 & 1 \\
0 & 0 & 1 & -7
\end{bmatrix}
\end{align}
$$

It follow that

$$
c=\begin{bmatrix}
1 \\
1 \\
-7
\end{bmatrix}
$$

<div class="page-break" style="page-break-before: always;"></div>

Step 2: Solve for $Ux=c$

Let $U_{i}$ denote the $i-th$ column of $U$. By Theorem 3 in section 1.4. It follow that this equation has the same solution set as

$$
\begin{bmatrix}
U_{1} & U_{2} & U_{3} & c
\end{bmatrix}
$$

Thus,

$$
\begin{align}
\begin{bmatrix}
1 & 2 & 3 & 1 \\
0 & -1 & -2 & 1 \\
0 & 0 & 1 & -7
\end{bmatrix}&\xrightarrow[R^{3}_{1}(-3)]{R^{3}_{2}(2)} \begin{bmatrix}
1 & 2 & 0 & 22 \\
0 & -1 & 0 & -13 \\
0 & 0 & 1 & -7
\end{bmatrix} \\
&\xrightarrow[]{R_{2}(-1)} \begin{bmatrix}
1 & 2 & 0 & 22 \\
0 & 1 & 0 & 13 \\
0 & 0 & 1 & -7
\end{bmatrix} \\
&\xrightarrow[]{R^{2}_{1}(-2)} \begin{bmatrix}
1 & 0 & 0 & -4 \\
0 & 1 & 0 & 13 \\
0 & 0 & 1 & -7
\end{bmatrix}
\end{align}
$$

Thus, it follow that

$$
x=\begin{bmatrix}
-4 \\
13 \\
-7
\end{bmatrix}
$$

Hence, $x=-4,y=13,z=-7$.

<div class="page-break" style="page-break-before: always;"></div>

2)
Let $A$ be an $n\times n$ matrix such that the sum of the entries of each row equals zero. Thus, 

The $i-th$ row of $A$ has the property as below:
$$
\sum_{j=1}^{n}(A)_{ij} =0
$$

This implies that

$$
\begin{align}
\begin{bmatrix}
\sum_{j=1}^{n}(A)_{1j} \\
\vdots  \\
\sum_{j=1}^{n} (A)_{nj} 
\end{bmatrix}&= 0 \\
\begin{bmatrix}
a_{11}+\dots+a_{1n} \\
\vdots  \\
a_{n_{1}}+\dots+a_{nn}
\end{bmatrix}&= 0 \\
\end{align}
$$

By definition of addition of matrices page 123

$$
\begin{align}
\begin{bmatrix}
a_{11} \\
\vdots  \\
a_{n_{1}}
\end{bmatrix}+\dots+\begin{bmatrix}
a_{1n} \\
\vdots  \\
a_{nn}
\end{bmatrix} = 0
\end{align}
$$

Thus, Let $a_{n}$ denote the $n-th$ column vector of $A$ , the equation above implies that 

$$
a_{1}+\dots a_{n}=0
$$

where 

$$
a_{n}=\begin{bmatrix}
a_{1n} \\
\vdots  \\
a_{nn}
\end{bmatrix}
$$


Thus, this implies that the system $Ax=0$ denoted by

$$
\begin{bmatrix}
a_{1} & \dots & a_{n} & 0
\end{bmatrix}
$$

has a non trivial solution which is

$$
1a_{1}+\dots+1a_{n}=0
$$
Thus, by fact (equation 3 page 85), it follow that the column of $A$ are linearly dependent.

Thus, by The Invertible Matrix Theorem page 145, it follow that $A$ is not invertible.










