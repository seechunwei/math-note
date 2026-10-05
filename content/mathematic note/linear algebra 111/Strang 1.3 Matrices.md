
why a matrix for system with infinity many solution is not invertible, we can just reverse the row operation from A to I right?

A matrix is invertible if it exist a inverse matrix $A^{-1}$ such that
$$
AA^{-1}=I \text{ or } A^{-1}A=I
$$

This require the existence of a sequence of row operation to reduce the $A$ to $I$ such that
$$
E_{1}E_{2}\dots E_{n}A=I
$$
Since row operation (elementary matrix) is invertible. Thus let $A^{-1}=E_{1}E_{2}\dots E_{n}$

$$
\begin{align}
A^{-1}A=I
\end{align}
$$


If a system have infinitely many solution, it cannot reduce the matrix in to identity matrix. Thus, it is not invertible.

Thus, for a matrix to be invertible, each row of coefficient must have pivot entry.

 In mathematics, we often look at the **Invertible Matrix Theorem**, which states that for a square $n \times n$ matrix $A$, the following are equivalent:

1. $A$ is **invertible**.
2. The RREF of $A$ is the **identity matrix** $I_n$.
3. $A$ has $n$ **pivots** (a pivot in every row/column).
4. The equation $Ax = 0$ has only the **trivial solution** ($x = 0$).

