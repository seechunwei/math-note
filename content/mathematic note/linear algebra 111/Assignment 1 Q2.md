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