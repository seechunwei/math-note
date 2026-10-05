1)
By theorem 13 the set of least-squares solution for $Ax=b$ is the set of solution for $A^{T}Ax=A^{T}b$.

$$
\begin{align}
A^{T}A&=\begin{bmatrix}
-1 & 2 & -1 \\
2 & -3 & 3
\end{bmatrix}\begin{bmatrix}
-1 & 2 \\
2 & -3 \\
-1 & 3
\end{bmatrix} \\
&= \begin{bmatrix}
6 & -11 \\
-11 & 22
\end{bmatrix}
\end{align}
$$

^109e1b

$$
\begin{align}
A^{T}b&=\begin{bmatrix}
-1 & 2 & -1 \\
2 & -3 & 3
\end{bmatrix} \begin{bmatrix}
4 \\
1 \\
2
\end{bmatrix} \\
&=\begin{bmatrix}
-4 \\
11
\end{bmatrix}
\end{align}
$$

Solve for $A^{T}Ax=A^{T}b$:

$$
\begin{align}
\begin{bmatrix}
6 & -11 \\
-11 & 22
\end{bmatrix} \begin{bmatrix}
x_{1} \\
x_{2}
\end{bmatrix}=\begin{bmatrix}
-4 \\
11
\end{bmatrix}
\end{align}
$$

Row reduce the augmented matrix below;

$$
\begin{align}
\begin{bmatrix}
6 & -11 & -4 \\
-11 & 22 & 11
\end{bmatrix} &\xrightarrow[R_{2}(\frac{1}{11})]{R_{1}\left( \frac{1}{6} \right)}\begin{bmatrix}
1 & -\frac{11}{6} & -\frac{2}{3} \\
-1 & 2 & 1
\end{bmatrix} \\
&\xrightarrow[]{R_{2}^{1}(1)}\begin{bmatrix}
1 & -\frac{11}{6} & -\frac{2}{3} \\
0 & \frac{1}{6} & \frac{1}{3}
\end{bmatrix} \\
&\xrightarrow[]{R_{2}(6)} \begin{bmatrix}
1 & -\frac{11}{6} & -\frac{2}{3} \\
0 & 1 & 2
\end{bmatrix} \\
&\xrightarrow[]{R_{1}^{2}(\frac{11}{6})}\begin{bmatrix}
1 & 0 & 3 \\
0 & 1 & 2
\end{bmatrix}
\end{align}
$$

Thus, $\hat{x}=\begin{bmatrix}3 \\ 2\end{bmatrix}$.

5)
Given 
$$
A=\begin{bmatrix}
1 & 1 & 0 \\
1 & 1 & 0 \\
1 & 0 & 1 \\
1 & 0 & 1
\end{bmatrix},b=\begin{bmatrix}
1 \\
3 \\
8 \\
2
\end{bmatrix}
$$

$$A^TA = \begin{bmatrix}
1 & 1 & 1 & 1 \\
1 & 1 & 0 & 0 \\
0 & 0 & 1 & 1
\end{bmatrix} \begin{bmatrix}
1 & 1 & 0 \\
1 & 1 & 0 \\
1 & 0 & 1 \\
1 & 0 & 1
\end{bmatrix}=\begin{bmatrix}
4 & 2 & 2 \\
2 & 2 & 0 \\
2 & 0 & 2
\end{bmatrix}$$

Compute $A^{T}b:$

$$A^Tb = \begin{bmatrix}
1 & 1 & 1 & 1 \\
1 & 1 & 0 & 0 \\
0 & 0 & 1 & 1
\end{bmatrix} \begin{bmatrix}
1 \\
3 \\
8 \\
2
\end{bmatrix} = \begin{bmatrix}
1(1) + 1(3) + 1(8) + 1(2) \\
1(1) + 1(3) + 0(8) + 0(2) \\
0(1) + 0(3) + 1(8) + 1(2)
\end{bmatrix} = \begin{bmatrix}
14 \\
4 \\
10
\end{bmatrix}$$

Solve for $A^{T}A\hat{x}=A^{T}b$ by row reduce the augmented matrix below:

$$
\begin{bmatrix}
4 & 2 & 2 & 14 \\
2 & 2 & 0 & 4 \\
2 & 0 & 2 & 10
\end{bmatrix} \sim \begin{bmatrix}
1 & 0 & 1 & 5 \\
0 & 1 & -1 & -3 \\
0 & 0 & 0 & 0
\end{bmatrix}
$$

The solution set is:
$$\hat{x} = \begin{bmatrix}
5 \\
-3 \\
0
\end{bmatrix} + x_3 \begin{bmatrix}
-1 \\
1 \\
1
\end{bmatrix}, \quad x_3 \in \mathbb{R}$$

> [!question]
> Why this happen?
> Because by theorem 14 the $\hat{x}$ is not unique implies that the columns of $A$ is linearly dependent. Conversely is true.

9)
Given 

$$
A=\begin{bmatrix}
1  & 5 \\
3 & 1 \\
-2 & 4
\end{bmatrix}.b=\begin{bmatrix}
4 \\
-2 \\
-3
\end{bmatrix}
$$

Let $\hat{b}=\text{proj}_{\text{Col}A}b$ and $a_{1},a_{2}$ be the column of $A$. Thus,

$$
\begin{align}
\hat{b}&= \frac{b\cdot a_{1}}{a_{1}\cdot a_{1}}a_{1}+ \frac{b\cdot a_{2}}{a_{2}\cdot a_{2}} a_{2} \\
&= \frac{4}{14}\begin{bmatrix}
1 \\
3 \\
-2
\end{bmatrix}+ \frac{6}{42} \begin{bmatrix}
5 \\
1 \\
4
\end{bmatrix} \\
&=\begin{bmatrix}
1 \\
1 \\
0
\end{bmatrix}
\end{align}
$$

Notice that $\{ a_{1},a_{2} \}$ is an orthogonal set, thus the solution set of $Ax=\hat{b}$ is

$$
\hat{x}=\begin{bmatrix}
\frac{4}{14} \\
\frac{1}{7}
\end{bmatrix}
$$
by theorem 5.

13)
Given

$$
A=\begin{bmatrix}
2 & 1 \\
-3 & -4 \\
3 & 2
\end{bmatrix},b=\begin{bmatrix}
5 \\
4 \\
4
\end{bmatrix},u=\begin{bmatrix}
4 \\
-5
\end{bmatrix},v=\begin{bmatrix}
6 \\
-5
\end{bmatrix}
$$

Compute $Au$:

$$
Au= \begin{bmatrix}
2 & 1 \\
-3 & -4 \\
3 & 2
\end{bmatrix} \begin{bmatrix}
4 \\
-5
\end{bmatrix}=\begin{bmatrix}
3 \\
8 \\
2
\end{bmatrix}
$$
Compute $Av:$

$$
Av=\begin{bmatrix}
2 & 1 \\
-3 & -4 \\
3 & 2
\end{bmatrix} \begin{bmatrix}
6 \\
-5
\end{bmatrix}= \begin{bmatrix}
7 \\
2 \\
8
\end{bmatrix}
$$

Compute $||b-Au||:$

$$
b-Au=\begin{bmatrix}
5 \\
4 \\
4
\end{bmatrix}-\begin{bmatrix}
3 \\
8 \\
2
\end{bmatrix}=\begin{bmatrix}
2 \\
-4 \\
2
\end{bmatrix}
$$

$$
\begin{align}
||b-Au||&=\sqrt{ (b-Au)\cdot(b-Au) } \\
&= \sqrt{ 24 }
\end{align}
$$

Compute $||b-Av||:$

$$
b-Av=\begin{bmatrix}
5 \\
4 \\
4
\end{bmatrix}-\begin{bmatrix}
7 \\
2 \\
8
\end{bmatrix}=\begin{bmatrix}
-2 \\
2 \\
-4
\end{bmatrix}
$$

$$
\begin{align}
||b-Av||&= \sqrt{ 24 }
\end{align}
$$

Since the columns of $A$ is linearly independent, by theorem 14, the least square solution is unique. 

Suppose $u$ or $v$ is the least square solution then for the sake of contradiction , since $||b-Au||=||b-Av||$ 
it follow that both of them are least square solution. (contradict theorem 14)

31)
The normal equation: ^caf71f

$$
\begin{align}
A^{T}Ax&=A^{T}b \\
x&=(A^{T}A)^{-1}A^{T}b
\end{align}
$$

$$
\begin{align}
\hat{b}&=A(A^{T}A)^{-1}A^{T}b \\
\end{align}
$$

> [!question]
> Why ?
> $$
> (A^{T}A)^{-1}\neq A^{-1}(A^{T})^{-1}
> $$
> It is because $A$ is not a square matrix. If $A$ is a square matrix, then $\hat{b}=b$
> 
> Why? It is because $A$ is a square matrix with linearly independent columns, thus Col $A=\mathbb{R}^{n}$ given $A$ is $n\times n$.
>
>Since the supposition is the columns of $A$ is linearly independent, thus $m\geq n$.




