1)
Let $A=\begin{bmatrix}2 & 7 \\ 7 & 2\end{bmatrix}$. Thus,

$$
\begin{align}
\det \begin{bmatrix}
2-\lambda & 7 \\
7 & 2-\lambda
\end{bmatrix}&=(2-\lambda)(2-\lambda)-49 \\
&=\lambda^{2}-4\lambda-45 \\
&=(\lambda-9)(\lambda+5)
\end{align}
$$

Thus, the eigen value is $\lambda=9$ and $\lambda=5$.

3)
$$
\begin{align}
\det \begin{bmatrix}
3-\lambda & -2 \\
1 & -1-\lambda
\end{bmatrix}&=(3-\lambda)(-1-\lambda)-(-2) \\
&=\lambda^{2}-2\lambda-1 \\
\end{align}
$$

$$
\begin{align}
\lambda&= \frac{-b\pm \sqrt{ b^{2}-4ac }}{2a} \\
&= \frac{2\pm \sqrt{ 4-4(1)(-1) }}{2(1)} \\
&=\frac{2\pm \sqrt{ 8 }}{2} \\
&=1\pm \sqrt{ 2 }
\end{align}
$$

The characteristic polynomial is $\lambda^2 - 2\lambda - 1$, and its roots (the eigenvalues) are:

$$\lambda_1 = 1 + \sqrt{2}, \quad \lambda_2 = 1 - \sqrt{2}$$

5)

$$
\begin{align}
\det \begin{bmatrix}
2-\lambda & 1 \\
-1 & 4-\lambda
\end{bmatrix}&= (2-\lambda)(4-\lambda)-1(-1) \\
&=\lambda^{2}-6\lambda+9 \\
&=(\lambda-3)^{2}
\end{align}
$$

Thus, $\lambda=3$ is the eigenvalue.


6)

$$
\begin{align}
\det \begin{bmatrix}
1-\lambda & -4 \\
4 & 6-\lambda
\end{bmatrix}&=(1-\lambda)(6-\lambda)-(-16) \\
&=\lambda^{2}-7\lambda+22
\end{align}
$$

Since $b^{2}-4ac<0$, it follow that the characteristic polynomial don't have real root. Thus, the matrix don't have real eigenvalue.

9)

$$
\begin{align}
\det \begin{bmatrix}
1-\lambda & 0 & -1 \\
2 & 3-\lambda & -1 \\
0 & 6 & -\lambda
\end{bmatrix}& \xrightarrow[]{R_{2}\left( \frac{1-\lambda}{2} \right)} \begin{bmatrix}
1-\lambda & 0 & -1 \\
1-\lambda & \frac{(3-\lambda)(1-\lambda)}{2} & \frac{\lambda-1}{2} \\
0 & 6 & -\lambda
\end{bmatrix} \\
&\xrightarrow[]{R_{2}^{1}(-1)}\begin{bmatrix}
1-\lambda & 0 & -1 \\
0 & \frac{(3-\lambda)(1-\lambda)}{2} & \frac{\lambda+1}{2} \\
0 & 6 & -\lambda
\end{bmatrix}
\end{align}
$$

It is not a wise option because later we need to multiply $\frac{2}{1-\lambda}$ which is not valid if $1-\lambda=0$.

We should just do cofactor expansion across first column:

$$
\begin{align}
\det&=(-1)^{2}(1-\lambda)\det \begin{bmatrix}
3-\lambda & -1 \\
6 & -\lambda
\end{bmatrix}+(-1)^{3}(2)\det \begin{bmatrix}
0 & -1 \\
6 & -\lambda
\end{bmatrix} \\
&=(1-\lambda)[(-3\lambda+\lambda^{2})+6]+(-2)[0+6] \\
&=(-3\lambda+\lambda^{2}+6)+(3\lambda^{2}-\lambda^{3}-6\lambda)-12 \\
&=-\lambda^{3}+4\lambda^{2}-9\lambda-6
\end{align}
$$

The root is not rational root. 


