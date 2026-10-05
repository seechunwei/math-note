
Elimination- success or failure (decide whether the matrix is the good one or has problem)
back substitution
matrix multiplication
express elimination as matrix operation
reverse matrix

---


Suppose we have a system of linear 2ith 3 variables
$$
\begin{align}
x+2y+z&=2 \\
3x+8y+z&=12 \\
0x+4y+z&=2
\end{align}
$$

Elimination is a process to eliminate one variable for each equation each times from top to down, until we get only one variable in the last equation.


We express the system of linear equation in matrix form $Ax=b$. But lets omit the variable part. Instead we adjoint the coefficient matrix with the right hand side column to become augmented matrix as below.

$$
\begin{bmatrix}
1 & 2 & 1  &2 \\
3 & 8 & 1  & 12\\
0 & 4 & 1 & 2
\end{bmatrix}
$$
Notice that the last column represent the right hand side of the equation. The pivot entry is the first non zero entry in a row. Thus, $a_{11}=1$ is the pivot entry for row 1.

So what is the first step of  our elimination, we eliminate the entry under the pivot entry which is 3,0 in first column. It is the same as we eliminate $x$ in 2rd and 3rd equation. 

So how we do that? For second row, we multiply $r_{1}$ with -3 and add to the second row denoted by $R^{1}_{2}(-3)$. Thus,

$$
\begin{bmatrix}
1 & 2 & 1 & 2 \\
0 & 2 & -2 & 6 \\
0 & 4 & 1 & 2
\end{bmatrix}
$$

Since the $(3,1)$ -entry is 0. Thus, we no need to eliminate. Now the pivot entry for $r_{2}$ is 2 and we want to eliminate all the entry below pivot entry. Thus, we multiply $r_{2}$ with -2 and add to $r_{3}$ denoted by $R^{2}_{3}(-2)$.

$$
\begin{bmatrix}
1 & 2 & 1 & 2 \\
0 & 2 & -2 & 6 \\
0 & 0 & 5 & -10
\end{bmatrix}
$$

Now notice that this is the upper triangle matrix denoted by $U$ . The entry below diagonal which is the entry with row subscript equal to column subscript are all 0. 

Now we transform it back to the system of linear equation:
$$
\begin{align}
x+2y+z&=2 \\
2y-2z&=6 \\
5z&=-10
\end{align}
$$
By using the back substitution we can get solution $(2,1,-2)$ . Beside we can also get the determinant which is $1\times 2\times 5=10$.

The process of elimination is from $E$  (elementary matrix) to $U$ (upper triangle matrix)

---


How do we express elimination matrix as matrix operation ? So far we only see column operation in matrix form which is $Ax=b$ is the linear combination of column for $A$.

$$
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
\begin{bmatrix}
x \\
y
\end{bmatrix}

=x\begin{bmatrix}
a \\
c
\end{bmatrix}+y
\begin{bmatrix}
b \\
d
\end{bmatrix}
$$
Thus, it effect the the column of matrix $A$. How about row operation? 

$$
\begin{bmatrix}
x & y
\end{bmatrix}
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}=
x\begin{bmatrix}
a & b
\end{bmatrix}+
y\begin{bmatrix}
c & d
\end{bmatrix}
$$
If we multiply a row vector in left hand side of the matrix , it is linear combination of the row of matrix $A$.

So to perform row operation, we need to multiply the matrix with a matrix in left hand side. Lets consider the operation $R^{1}_{2}(-3)$

$$
\begin{bmatrix}
 &  &  & &   \\
 \\
 \\

\end{bmatrix}
\begin{bmatrix}
1 & 2 & 1  &2 \\
3 & 8 & 1  & 12\\
0 & 4 & 1 & 2
\end{bmatrix}=
\begin{bmatrix}
1 & 2 & 1 & 2 \\
0 & 2 & -2 & 6 \\
0 & 4 & 1 & 2
\end{bmatrix}
$$
The answer is 

$$
\begin{bmatrix}
 1& 0 & 0 & 0  \\
 -3 & 1 & 0 & 0\\
 0 & 0 & 1 & 0\\

\end{bmatrix}
\begin{bmatrix}
1 & 2 & 1  &2 \\
3 & 8 & 1  & 12\\
0 & 4 & 1 & 2
\end{bmatrix}=
\begin{bmatrix}
1 & 2 & 1 & 2 \\
0 & 2 & -2 & 6 \\
0 & 4 & 1 & 2
\end{bmatrix}
$$

The first row of the matrix $\bigl( \begin{smallmatrix} 1&0&0&0\end{smallmatrix} \bigr)$ is the combination of row for matrix $A$. We since the first row remain unchanged , thus we just multiply the first row with 1 and other row with 0 and we add together become the first row of new matrix.


Notice that if we omit the last column it become a identity matrix denoted by $I$. How about $R_{3}^{2}(-2)$

$$\begin{bmatrix}
 1& 0 & 0 & 0  \\
 0 & 1 & 0 & 0\\
 0 & -2 & 1 & 0\\

\end{bmatrix}
\begin{bmatrix}
1 & 2 & 1 & 2 \\
0 & 2 & -2 & 6 \\
0 & 4 & 1 & 2
\end{bmatrix}=
\begin{bmatrix}
1 & 2 & 1 & 2 \\
0 & 2 & -2 & 6 \\
0 & 0 & 5 & -10
\end{bmatrix}
$$

What if the pivot entry is 0, then we want to interchange the row, we multiply the elementary matrix with permutation matrix on left hand side

$$
\begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix} 
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}=
\begin{bmatrix}
c & d \\
a & b
\end{bmatrix}
$$
The matrix on left hand side is called permutation matrix.

---
So far we only talk about row operation, how about column operation?


It is the same , but if we want to do column operation for matrix $A$, then we need to multiply with a matrix on right hand side. For example, the column interchange operation

$$
\begin{bmatrix}
a & b \\
c & d  
\end{bmatrix}
\begin{bmatrix} 
0 & 1 \\
1 & 0
\end{bmatrix}=
\begin{bmatrix}
b & a \\
d & c
\end{bmatrix}
$$
The first column of permutation matrix $\bigl( \begin{smallmatrix} 0 \\ 1\end{smallmatrix} \bigr)$ is the linear combination of column for matrix $A$ , we multiply 0 with first column and multiply 1 with second column add together become the first column of new matrix.

---
Notice that we perform 2 operation and reach $U$ denoted by $E_{1}(E_{2})A=U$. Actually we can find one matrix that perform only one times to reach $U$.

$$
\begin{align}
(E_{1}E_{2})A=U
\end{align}
$$
We find a new matrix by multiply the 2 operation matrix. (Associativity ). But there is a better way which is we consider how to change from $U$ to $E$. inverse matrix.

The matrix above is invertible because we can use elimination to find the solution set. Consider the matrix below
$$
\begin{bmatrix}
 &  &  &  \\
 &  &  &  \\

\end{bmatrix}
\begin{bmatrix}
1 & 0 & 0 \\
-3 & 1 &  0 \\
0 & 0 & 1
\end{bmatrix}=
\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix}
$$

The matrix is actually the operation $R_{2}^{1}(-3)$, how to we reverse the step, we simply multiply 1 with 3 and add to 2

$$
\begin{bmatrix}
 1& 0 &0   \\
 3&  1& 0  \\
0 & 0 & 1
\end{bmatrix}
\begin{bmatrix}
1 & 0 & 0 \\
-3 & 1 &  0 \\
0 & 0 & 1
\end{bmatrix}=
\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix}
$$
$$


