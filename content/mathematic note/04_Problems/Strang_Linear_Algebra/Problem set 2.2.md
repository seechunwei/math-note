1)

$$
\begin{align}
\begin{bmatrix}
1 & 2 & 3 & 4 \\
0 & 0 &  1 & 2 \\
0 & 0 & 0 & 0
\end{bmatrix}\begin{bmatrix}
x_{1} \\
x_{2} \\
x_{3} \\
x_{4}
\end{bmatrix}=\begin{bmatrix}
0 \\
0 \\
1
\end{bmatrix}
\end{align}
$$

$$
\begin{align}
R=\begin{bmatrix}
1 & 2 & 0 & -2 \\
0 & 0 & 1 & 2 \\
0 & 0 & 0 & 0
\end{bmatrix}
\end{align}
$$
We can just ignore the right hand side because any combination of 0 is still 0.

The $x_{n}:$

$$
N= \begin{bmatrix}
-2 & -2 \\
1  & 0\\
0  & -2\\
0 & 1
\end{bmatrix}
$$

3)
$$
\begin{bmatrix}
0 & 1 & 0 & 3  & b_{1}\\
0 & 2 & 0 & 6 & b_{2}
\end{bmatrix}\to \begin{bmatrix}
0 & 1 & 0 & 3 & b_{1} \\
0 & 0 & 0 & 0 & b_{2}-2b_{1}
\end{bmatrix}
$$

$$
\begin{align}
N=\begin{bmatrix}
1  & 0 & 0\\
0  & 0 & -3\\
0  & 1 & 0\\
0 & 0 & 1
\end{bmatrix}
\end{align}
$$
$Ax=b$ is consistent when $b$ satisfies $b_{2}=2b_{1}$. Notice that the nullity is $3$, thus the dimension for nullspace is 3

$$
x_{p}=\begin{bmatrix}
0 \\
b_{1} \\
0 \\
0
\end{bmatrix}+x_{n}
$$

Thus

$$x = \underbrace{\begin{bmatrix} 0 \\ b_1 \\ 0 \\ 0 \end{bmatrix}}_{x_p} + x_1 \begin{bmatrix} 1 \\ 0 \\ 0 \\ 0 \end{bmatrix} + x_3 \begin{bmatrix} 0 \\ 0 \\ 1 \\ 0 \end{bmatrix} + x_4 \begin{bmatrix} 0 \\ -3 \\ 0 \\ 1 \end{bmatrix}$$


6)
$$
\begin{align}
\begin{bmatrix}
1 & 0  & b_{1}\\
0 & 1  & b_{2}\\
2 & 3 & b_{3}
\end{bmatrix}&\to \begin{bmatrix}
1 & 0  & b_{1}\\
0 & 1 & b_{2} \\
0 & 3 & b_{3}-2b_{1}
\end{bmatrix} \\
&\to \begin{bmatrix}
1 & 0 & b_{1} \\
0 & 1 & b_{2} \\
0 & 0 & b_{3}-2b_{1}-3b_{2}
\end{bmatrix}
\end{align}
$$

The system is consistent iff $b_{3}-2b_{1}-3b_{2}=0$.

rank=2

$$
x_{p}=\begin{bmatrix}
b_{1} \\
b_{2} \\
0
\end{bmatrix}
$$

Notice that this matrix have more row than column, it can only have solution if the last row is 0. $m=2$ , rank=2
 nullity=0.

8)

$b_{1}$ and $b_{2}$ can be any real number because the column space of $A$ span $\mathbb{R}^{2}$


Since $c_{2}$ and $c_{3}$ don't have pivot, we can ignore it to form the column space. Thus, 
$$
C(A)=x_{1}\begin{bmatrix}
1 \\
2
\end{bmatrix}+x_{4}\begin{bmatrix}
3 \\
7
\end{bmatrix}
$$

but since $x_{2},x_{3}$ is free variable it follow that it have infinity many solution for $Ax=b$ and $Ax=0$.

First we find the special solution.

$$
\begin{align}
\begin{bmatrix}
1 & 2 & 0 & 3 &  b_{1} \\
2 & 4 & 0 & 7 &  b_{2}
\end{bmatrix}&\to \begin{bmatrix}
1 & 2 & 0 & 3 & b_{1} \\
0 & 0 & 0 & 1 & b_{2}-2b_{1}
\end{bmatrix} \\
&\to \begin{bmatrix}
1 & 2 & 0 & 0 & 7b_{1}-3b_{2} \\
0 & 0 & 0 & 1 & b_{2}-2b_{1}
\end{bmatrix}
\end{align}
$$


$$
x_{n}=x_{2}\begin{bmatrix}
-2 \\
1 \\
0 \\
0
\end{bmatrix}+x_{3}\begin{bmatrix}
0 \\
0 \\
1 \\
0
\end{bmatrix}
$$

The nullspace is

$$
N=\begin{bmatrix}
-2 & 0 \\
1 & 0 \\
0 & 1 \\
0 & 0
\end{bmatrix}
$$

$$
\begin{align}
x&=x_{p}+x_{n} \\
&= \begin{bmatrix}
7b_{1}-3b_{2} \\
0 \\
0 \\
b_{2}-2b_{1}
\end{bmatrix}+x_{2}\begin{bmatrix}
-2 \\
1 \\
0 \\
0
\end{bmatrix}+x_{3}\begin{bmatrix}
0 \\
0 \\
1 \\
0
\end{bmatrix}
\end{align}
$$

The column space focus on column picture while nullspace focus on row picture. Because the column space is in $m$ dimensional space while nullspace is in $n$ dimensional space.

column space focus on output which is b while nullspace focus on solution set. 

10)
One nullity 2 pivot
$$
\begin{align}
\begin{bmatrix}
1 & 0 &   -1 \\
0 & 1 &  -3 
\end{bmatrix}=\begin{bmatrix}
1 \\
2
\end{bmatrix}
\end{align}
$$

==Remark==
I would not know how to answer this question if i don't know how to get the answer directly from $R$ without doing algebraic 

12) c

==14== block matrix

15)
$$
\begin{align}N=
\begin{bmatrix}
-F \\
I
\end{bmatrix}
\end{align}
$$
It is completely normal to find block matrices abstract at first. Since you are diving into the rigor of **Pure Mathematics**, it helps to think of these blocks not just as symbols, but as **sub-systems** of equations.

Let’s break down the logic of why $N = \begin{bmatrix} -F \\ I \end{bmatrix}$ is the "magic key" that unlocks the nullspace of $R = \begin{bmatrix} I & F \\ 0 & 0 \end{bmatrix}$.

---

### 1. The Matrix Multiplication Proof

The definition of the nullspace matrix $N$ is that $RN = \mathbf{0}$. If we treat the blocks like single numbers and multiply them out, the logic becomes clear:

$$RN = \begin{bmatrix} I & F \\ 0 & 0 \end{bmatrix} \begin{bmatrix} -F \\ I \end{bmatrix}$$

Multiplying the "top row" of $R$ by the column $N$:

$$(I \times -F) + (F \times I) = -F + F = \mathbf{0}$$

Multiplying the "bottom row" of $R$ by the column $N$:

$$(0 \times -F) + (0 \times I) = 0 + 0 = \mathbf{0}$$

Because the result is a zero matrix, every column in $N$ must be a solution to $Rx = 0$.

### 2. What the Blocks Actually Represent

Think of the vector $\mathbf{x}$ as being split into two parts: **Pivots** ($x_p$) and **Free Variables** ($x_f$).

- **The Bottom Block ($I$):** This represents the **Free Variables**. In a special solution, we set one free variable to **1** and the others to **0**. By putting an Identity Matrix ($I$) here, we are systematically creating a list where every column "activates" exactly one free variable.
    
- **The Top Block ($-F$):** This represents the **Pivot Variables**. As we saw in the earlier examples, when you move a term from the left side of the equation to the right (to solve for the pivot), the sign must flip. This block tells the pivot variables exactly how to "react" to the free variables to keep the sum equal to zero.
    

### 3. A Concrete Example

Imagine a $2 \times 3$ matrix in RREF:

$$R = \begin{bmatrix} \mathbf{1} & 0 & \mathbf{5} \\ 0 & \mathbf{1} & \mathbf{6} \end{bmatrix}$$

Here, $I = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}$ (the pivots) and $F = \begin{bmatrix} 5 \\ 6 \end{bmatrix}$ (the free column).

Following the block formula $N = \begin{bmatrix} -F \\ I \end{bmatrix}$:

$$N = \begin{bmatrix} -5 \\ -6 \\ 1 \end{bmatrix}$$

- The **bottom 1** is the $I$ (setting the free variable $x_3 = 1$).
    
- The **top -5 and -6** are the $-F$ (the pivot variables $x_1$ and $x_2$ reacting).
    

---

==Remark==
We can view all the pivot column with one non pivot column as a block matrix as above. (more than 1 free variable, we just adjoint the column together) and it show that another way to understand it. The $I$ here means identity matrix , it means 1.

What is the identity matrix means in R?
It means the coefficient of pivot variable is 1, thus we can solve for

$$
\begin{bmatrix}
1 & 0 & 3 \\
0 & 1 & 2 \\
0 & 0 & 0
\end{bmatrix}=\begin{bmatrix}
0 \\
0 \\
0
\end{bmatrix}
$$

We suppose a square matrix with $r<m$, thus $R_{3}\in Span\{ R_{1},R_{2} \}$. Thus, the last row of rref will be zero. (we use the assumption that pivot column come first)

Thus, the $I=\begin{bmatrix}1 & 0 \\ 0 & 1\end{bmatrix}$, and $F=\begin{bmatrix}3 \\ 2\end{bmatrix}$. 

If we view as block matrix then it become our question

$$
\begin{align}
\begin{bmatrix}
I & F \\
0 & 0
\end{bmatrix}
\end{align}
$$

We need to solve for $Rx=0$. From result above we know that the answer is

$$
N=\begin{bmatrix}
-F \\
I
\end{bmatrix}
$$
But, what the identity matrix represent here?

If we have 2 free variable then the nullspace will be like

$$
\begin{bmatrix}
a & b \\
c & d\\
---  & ---\\
1 & 0 \\
0 & 1
\end{bmatrix}
$$
Because for first column we set the free variable $x_{3}=1$, $x_{4}=0$ 

the second column we set $x_{3}=0,x_{4}=1$. So it appear as the identity matrix below.

16)
This is a $m\times n$ block matrix

$$
R=\begin{bmatrix}
A & B \\
C & D
\end{bmatrix}
$$

Suppose all $r$ pivot variables come last. Since $B$ is $r\times r$ matrix, it follow that $B$ is an identity matrix. And notice that $m-r$ row are all zero thus, $C$ and $D$ are zero matrix. Thus,

$$
R=\begin{bmatrix}
A & I \\
0 & 0
\end{bmatrix}
$$
Thus, the nullspace is

$$
N=\begin{bmatrix}
I \\
-A
\end{bmatrix}
$$

$I$ come first as free variable come first in $R$.

17)

