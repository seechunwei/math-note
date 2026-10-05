$PP^{T}=I$. Why?

$$
\begin{align}
PP^{T}&=\begin{bmatrix}
0 & 1 & 0 \\
1 & 0 & 0 \\
0 & 0 & 1
\end{bmatrix}\begin{bmatrix}
0 & 1 & 0 \\
1 & 0 & 0 \\
0 & 0 & 1
\end{bmatrix} \\
&=\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix}
\end{align}
$$
$$
\begin{align}
PP^{T}&=\begin{bmatrix}
0 & 1 & 0 \\
0 & 0 & 1 \\
1 & 0 & 0
\end{bmatrix}\begin{bmatrix}
0 & 0 & 1 \\
1 & 0 & 0 \\
0 & 1 & 0
\end{bmatrix} \\
&=\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix}
\end{align}
$$
The critical part is the diagonal act as a mirror, the row of $PP^{T}$ is linear combination of row of $P^{T}$ with entry $P$ as weights. Thus, see the first row of $P=(0,1,0)$, it determine the first row of $PP^{T}$ , Thus , the second row of $P^{T}$ must equal to $(1,0,0)$. Thus, $a_{12}=a_{21}$. The subscript $(1,2)$ and $(2,1)$ is the exchange of row 1 and 2.


Thus，
$$
P^{-1}=P^{T}
$$

In MATLAB, it will exchange the row which is reasonable in respect of numerical value. For example, if we have a very small pivot like 0.000002334... and it take a lot of cost to divide the whole row with that coefficient. 

For any invertible matrix $A$ that need to perform row exchange can be express in this way

$$
PA=LU
$$

### Transpose 

[[1.6 Inverse and Transposes]]

### Vector space and subspace

The main operation of vector is scalar multiple and addiction. We create space using this 2 operation with some rule.

The addiction of vectors with real number as multiple scalar is called linear combination of column vector. 

For example $\mathbb{R}^{2}$
$$
\begin{bmatrix}
3 \\
2
\end{bmatrix},\begin{bmatrix}
0 \\
0
\end{bmatrix},\begin{bmatrix}
\pi \\
e
\end{bmatrix}
$$
The vector usually represented by an arrow in $\mathbb{R}^{2}$. The vector in $\mathbb{R}^{2}$ means its 2 component are real number.

$\mathbb{R}^{2}$ is a 2 dimensional figure which is plane.

Any linear combination of 3 such vector are still in $\mathbb{R}^{2}$. It is closed. Thus, zero vector is crucial (it must be included) because any vector with 0 as multiple scalar will become 0.

$\mathbb{R}^{3}$ is all the vector with 3 real component. For example,
$$
\begin{bmatrix}
3 \\
2 \\
0
\end{bmatrix}
$$

Notice that 
$$
\begin{bmatrix}
3 \\
2 \\
0
\end{bmatrix} \neq \begin{bmatrix}
3 \\
2
\end{bmatrix}
$$

One is a vector in $\mathbb{R}^{3}$ where it happened that the third component is 0 and one is in $\mathbb{R}^{2}$.


$\mathbb{R}^{n}$ is all column vectors with $n$ real component. $\mathbb{R}^{n}$ is closed same as $\mathbb{R}^{2}$. any linear combination of vector in $\mathbb{R}^{n}$ is still in $\mathbb{R}^{n}$.

When it is not a vector space?
Suppose the first quadrant of $\mathbb{R}^{2}$, Any addition of the vector come from the space are still in the space, no problem. 

But what about scalar multiple, what if we multiply negative real number, then it will go out of this space. Thus, it is not closed under multiplication by all real numbers.

So the question is does it exist a subspace in a vector space $\mathbb{R}^{n}$ ?

Vector space that follow the rule but no need all the vector

$\mathbb{R}^{2}$
1) a line pass though $(0,0)$
for example a line pass though $(1,1)$ and $(0,0)$ is a subspace of $\mathbb{R}^{2}$, because any linear combination of $(1,1)$ is still lying on the line 

Notice that it require the line to pass though $(0,0)$ to allow for multiplication with 0.

2) a point which is zero vector alone

How about $\mathbb{R}^{3}$
1) a plane pass though $(0,0,0)$
2) a line pass though $(0,0,0)$
3) zero vectors

How to construct subspace from column of a matrix?

$$
A=\begin{bmatrix}
1 & 3 \\
2 & 3 \\
4 & 1
\end{bmatrix}
$$

The linear combination of 2 column vectors in $\mathbb{R}^{3}$
$$
a\begin{bmatrix}
1 \\
2 \\
4
\end{bmatrix}+b\begin{bmatrix}
3 \\
3 \\
1
\end{bmatrix}
$$

form 2 axis of a plane and its spanning set is a plane in $\mathbb{R}^{3}$.
