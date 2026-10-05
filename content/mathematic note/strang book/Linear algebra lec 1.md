
The most fundamental question in linear algebra is to solve the system of equation. We will introduce the important concept which is 
1) row picture 
2) column picture.
3) matrix form

Suppose 2 linear equation 
$$
\begin{align}
2x-y&=0 \\
-x+2y&=3
\end{align}
$$
The matrix is a rectangular array of number. In this case we will construct the coefficient matrix and the column vector to represent the variable.

$$
\begin{bmatrix}
2&-1 \\
-1&2
\end{bmatrix}
\begin{bmatrix}
x \\
y
\end{bmatrix}
=\begin{bmatrix}
0 \\
3
\end{bmatrix}
$$
We will write $Ax=b$ to denote the multiplication of a matrix and column vector (It the matrix form of a system of linear equation). So any system equation can be write in this form., 

Or in other way, it can be express as the vector equation
$$
b=c_{1}v_{1}+c_{2}v_{2}+\dots+c_{n}v_{n}
$$



The row picture is the graph of 2 row equation in cartesian plane.

![[Pasted image 20260401174104.png]]

The solution for this system of equation is the point where 2 line intersect each other which is $(1,2)$. 

Column picture
Notice that the system of equation can be write as 
$$
x\begin{bmatrix}
2 \\
-1 
\end{bmatrix}
+y\begin{bmatrix}
-1 \\
2
\end{bmatrix}=
\begin{bmatrix}
0 \\
3
\end{bmatrix}
$$
We pack the thing together with same variable, and denote the coefficient as a column vector. 

Why we can do that? From the property of vector ^134

$$
\begin{bmatrix}
2x & -y \\
-x & 2y
\end{bmatrix}=
\begin{bmatrix}
2x \\
-x
\end{bmatrix}+\begin{bmatrix}
-y \\
2y
\end{bmatrix}=x\begin{bmatrix}
2 \\
-1
\end{bmatrix}+y\begin{bmatrix}
-1 \\
2
\end{bmatrix}
$$


In a vector $\bigl( \begin{smallmatrix} x \\ y\end{smallmatrix} \bigr)$ , x means horizontal movement and y means vertical movement. We need to find the linear combination of column vector to produce $\bigl( \begin{smallmatrix} 0\\3\end{smallmatrix} \bigr)$. Thus the column picture is depend on the vector

![[Screenshot 2026-04-01 180627.png]]

When $x=1$ and $y=2$. We can cleary see that after add 2 linear combination of column vector the end point is $(0,3)$.


==Question==
Does the linear combination of these 2 column vector fill up the whole 2d space? The answer is yes. When it work, and when it does not work?



Now suppose a 3x3 system of linear equation

$$
\begin{align}
2x-1y+0z&=0 \\
-x+2y-z&=-1 \\
0x-3y+4z&=4
\end{align}
$$
The matrix form of this system equation.
$$\begin{bmatrix} 2 & -1 & 0 \\ -1 & 2 & -1 \\ 0 & -3 & 4 \end{bmatrix} \begin{bmatrix} x \\ y \\ z \end{bmatrix} = \begin{bmatrix} 0 \\ -1 \\ 4 \end{bmatrix}$$


It is very hard to see the intersection in row picture. The solution for any system of linear equation is a plane.

How to visualize $2x-1y+0z=0$ as a plane?
How to Visualize It

1. **Start in 2D:** Draw the line $y = 2x$ on a piece of paper (the $xy$-plane).
2. **Go to 3D:** Imagine that paper is the floor of a room.
3. **Build the Plane:** Imagine a giant, flat glass wall rising straight up from that line toward the ceiling. (can pick any z)

How about the column picture?
$$
x
\begin{bmatrix}
2 \\
-1 \\
0 
\end{bmatrix}+y \begin{bmatrix}
-1 \\
2 \\
-3
\end{bmatrix} +z \begin{bmatrix}
0 \\
-1 \\
4 
\end{bmatrix}= \begin{bmatrix}
0 \\
-1 \\
4
\end{bmatrix}
$$
Notice that $(0,0,1)$ can produce the solution.

By remaining the left side and we change the right side can we fill up the 3d space with the linear combination?

Not always t work only if it is a non-singular matrix. An invertible matrix and vice versa. It is depend on the independence between column. 

Let say the 3rd column is the sum of first column and second column. Then the linear combination is just lie in the certain plane.

$Ax=b$ is a multiplication of matrix and a vector.
1) dot product
2) combination of column 
