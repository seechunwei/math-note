14b)

$$
\begin{bmatrix}
0 & 3 & 4 \\
 1 & 5 & 6 \\
0 & 6 & 8
\end{bmatrix}
$$

15)
If rows 1 and 2 are the same, when we do the elimination the first and second entry will be zero. Thus, we need to interchange with another row where its second entry is not zero. If whole column is zero then it is not singular.

If column 1 and 2 are the same, then pivot 2 is missing

16)
$$
\begin{bmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
3 & 6 & 9
\end{bmatrix}
$$

Thus,  it will become 
$$
\begin{bmatrix}
1 & 2 & 3 \\
0 &0&0\\
0 & 0 & 0
\end{bmatrix}
$$

for $b=(1,10,100)$, it has no solution. for $b=(0,0,0)$ , it has infinity many solution (2 free variable with homogeneous system).

17
$t=0$ 

18)
It is because if 2 line pass though same 2 point, they are the same line, so there are infinitely many solution

 1. The Algebraic Proof

Suppose you have a system of linear equations represented by $Ax = b$. Let's assume there are two distinct solutions, $x_1$ and $x_2$, such that:

$$Ax_1 = b \quad \text{and} \quad Ax_2 = b$$

Now, consider a new vector $x$ that is a **weighted average** (or convex combination) of these two solutions:

$$x = (1 - c)x_1 + cx_2$$

_(where $c$ is any real number)_

If we multiply this new vector by $A$, we get:

$$Ax = A[(1 - c)x_1 + cx_2]$$

$$Ax = (1 - c)Ax_1 + cAx_2$$

Substituting our known values ($Ax_1 = b$ and $Ax_2 = b$):

$$Ax = (1 - c)b + cb$$

$$Ax = b - cb + cb$$

$$Ax = b$$


Why $1-c$ and c because $1-c+c=1$.

b) the line that pass though the 2 points


