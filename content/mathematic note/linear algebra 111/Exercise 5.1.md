1)
let $A=\begin{bmatrix}3 & 2 \\ 3 & 8\end{bmatrix}$
To determine if $\lambda=2$ is an eigenvalue of $A$, we need to determine if $(A-\lambda I)x=0$ has non trivial solution or not. It is equivalent to determine the nullity.

$$
\begin{align}
(A-\lambda I)&= \begin{bmatrix}
3 & 2 \\
3 & 8
\end{bmatrix} -\begin{bmatrix}
2 & 0 \\
0 & 2
\end{bmatrix} \\
&= \begin{bmatrix}
1 & 2 \\
3 & 6
\end{bmatrix} \\
&\xrightarrow[]{R^{1}_{2}(-3)}\begin{bmatrix}
1 & 2 \\
0 & 0 
\end{bmatrix} &&(1)
\end{align}
$$
We know that the matrix in (1) have the same solution set as $(A-2I)$ [[4.3 Linearly Independent Sets, Bases#^313672]]. Thus, the null space is also the same. Thus, it follow that $(A-2I)$ have nullity of 1 implies that $(A-2I)x=0$ have non trivial solution. Thus, 2 is eigen value of $A$.


3)
Let $A=\begin{bmatrix}-3 & 1 \\ -3 & 8\end{bmatrix}$ and $v=\begin{bmatrix}1 \\ 4\end{bmatrix}$. By definition  $v$ is a eigen vector of $A$ if $Av=\lambda v$ for some $\lambda$. 

$$
Av=\begin{bmatrix}
-3 & 1 \\
-3 & 8
\end{bmatrix} \begin{bmatrix}
1 \\
4
\end{bmatrix}= \begin{bmatrix}
1 \\
29
\end{bmatrix}
$$

4)
Let $A=\begin{bmatrix}4 & 2 \\ 2 & 4\end{bmatrix}$ and $v=\begin{bmatrix}-1 \\ 1\end{bmatrix}$ . By definition  $v$ is a eigen vector of $A$ if $Av=\lambda v$ for some $\lambda$. 

$$
\begin{align}
Av=\begin{bmatrix}
4 & 2 \\
2 & 4
\end{bmatrix}\begin{bmatrix}
-1 \\
1
\end{bmatrix}= \begin{bmatrix}
-2 \\
2
\end{bmatrix}
\end{align}
$$

Notice that $\begin{bmatrix}-2 \\ 2\end{bmatrix}=2\begin{bmatrix}-1 \\ 1\end{bmatrix}$. Thus, it follow that $v$ is an eigenvector of $A$ corresponding to $\lambda=2$.

9）
Let $A=\begin{bmatrix}9 & 0 \\ 2 & 3\end{bmatrix}$, $\lambda=3,9$.

Find the eigenspace corresponding to each listed eigenvalue.

Row reduce $(A-3I)$:
$$
\begin{align}
\begin{bmatrix}
9 & 0 \\
2 & 3
\end{bmatrix}-\begin{bmatrix}
3 & 0 \\
0 & 3
\end{bmatrix}&=\begin{bmatrix}
6 & 0 \\
2 & 0
\end{bmatrix} \\
&\xrightarrow[]{R_{1}\left( \frac{1}{6} \right)} \begin{bmatrix}
1 & 0 \\
2 & 0
\end{bmatrix} \\
&\xrightarrow[]{R_{2}^{1}(-2)} \begin{bmatrix}
1 & 0 \\
0 & 0
\end{bmatrix}
\end{align}
$$

Thus, the solution $(A-3I)x=0$ is

$$
x= x_{2}\begin{bmatrix}
0 \\
1
\end{bmatrix}
$$
Thus, the eigenspace corresponding to $\lambda=3$ is $V_{3}=\text{Span}\{ \begin{bmatrix}0 \\ 1\end{bmatrix} \}$

Row reduce $(A-9I)$:

$$
\begin{align}
\begin{bmatrix}
9 & 0 \\
2 & 3
\end{bmatrix}-\begin{bmatrix}
9 & 0 \\
0 & 9
\end{bmatrix}&=\begin{bmatrix}
0 & 0 \\
2 & -6
\end{bmatrix} \\
&\xrightarrow[]{R_{1}^{2}} \begin{bmatrix}
2 & -6 \\
0 & 0
\end{bmatrix} \\
&\xrightarrow[]{R_{1}\left(  \frac{1}{2} \right)} \begin{bmatrix}
1 & -3 \\
0 & 0
\end{bmatrix}
\end{align}
$$

Thus, the solution $(A-3I)x=0$ is

$$
x=x_{2}\begin{bmatrix}
3 \\
1
\end{bmatrix}
$$
Thus, eigenspace corresponding to $\lambda=9$ is $V_{9}=\text{Span}\{ \begin{bmatrix}3 \\ 1\end{bmatrix} \}$

Why it is a space, because the solution set of homogeneous system is a subspace of $\mathbb{R}^{n}$ iff $A-\lambda I$ is a $n\times n$ matrix. (Nullspace live in domain)

"The vectors obtained from the free variables in the solution to $(A - \lambda I)x = 0$ are **linearly independent** and **span the eigenspace**; therefore, they form a **basis for the eigenspace** corresponding to the eigenvalue $\lambda$. [[2.8 Subspace#^6c5471]]

17)

$$
A=\begin{bmatrix}
0 & 0 & 0 \\
0 & 2 & 5  \\
0 & 0 & -1
\end{bmatrix}
$$
Find the eigen value

$$
\begin{align}
(A-\lambda I)= \begin{bmatrix}
-\lambda & 0 & 0 \\
0 & 2-\lambda & 5 \\
0 & 0 & -1-\lambda
\end{bmatrix}
\end{align}
$$

Notice that it is already in its ref form. Thus, for the system to have non trivial solution,

The $a_{33}$ entry:
$$
\begin{align}
-1-\lambda&=0 \\
\lambda&=-1
\end{align}
$$

The $a_{22}$ entry:

$$
\begin{align}
2-\lambda&=0 \\
\lambda&=2
\end{align}
$$

The $a_{11}$ entry:

$$
\begin{align}
-\lambda&=0 \\
\lambda&=0
\end{align}
$$

> [!remark]
> Since $\lambda=0$ , it follow that $Ax=0$ has non trivial solution


19)
Let $A=\begin{bmatrix}1 & 2 & 3 \\  1 & 2 & 3 \\ 1 & 2 & 3\end{bmatrix}$.

Let $c_{i}$ denote the $i-th$ columns of $A$. Notice that $c_{3}\in\text{Span}\{ c_{1},c_{2} \}$. Thus, the columns of $A$ is linearly dependent. It follow that $Ax=0$ has non trivial solution.

==31)==
> [!theorem] Statement:
An $n\times n$ matrix can have at most $n$ distinct eigenvalues.

It is because the system $(A-\lambda I)x=0$ have non trivial solution iff there exist free variable in any columns. Since there is only $n$ columns, it follow that the system can have at most 5 distinct free variable. 


> [!warning]
> The number of free variables is a property as a whole when we try to row reduce $(A-\lambda I)x$ for any $\lambda$. And each pivot is the condition for the system to have free variable, since $A$ can only have maximum of $n$ pivot, it follow that it can has at most 5 distinct eigenvalue. 
> (It is wrong because by definition the existence of free variable only assure the existence of eigen value.)
> 
> But what i meant was when we want to find eigenvalue, one of the way is row reduce $(A-\lambda I)$ to ref and set each pivot to 0 right? Because the $\lambda$ value that can make the pivot become 0$\implies$ free variable $\implies$ eigenvalue


> [!question]
> 1) The statement the system $(A-\lambda I)x=0$ have non trivial solution iff there exist free variable in any columns. Is it equivalent of saying that the _number of eigenvalues_ is bounded by the _number of columns_?
> 
> No, it only state that the existence of eigenvalue is equivalent to the existence of  free variable of the system. 
> 
> 2) A matrix can have a limited number of free variables, but how does the number of free variables in restrict the number of _distinct values? (The quantitative relationship)
> 

Consider the example $A=\begin{bmatrix}2 & 0 \\ 0 & 3\end{bmatrix}$.  Since it is a triangular matrix the eigenvalue are $2$ and $3$. And the matrix

$$
A-2I=\begin{bmatrix}
0 & 0 \\
0 & 1
\end{bmatrix}
$$
has 1 pivot and 1 free variable. Thus, the geometric multiplicity is 1. It is the same as $A-3I$.  Now consider the algebraic multiplicity:

$$
\det \begin{bmatrix}
2-\lambda & 0 \\
0 & 3-\lambda
\end{bmatrix}=(2-\lambda)(3-\lambda)
$$
Thus, the algebraic multiplicity is 1 for both eigenvalue. (This is typical of diagonalizable matrices)

Now consider the matrix:
$$
A=\begin{bmatrix}
2 & 1 \\
0 & 2
\end{bmatrix}
$$
$$
\det \begin{bmatrix}
2-\lambda & 1 \\
0 & 2-\lambda
\end{bmatrix}=(2-\lambda)^{2}
$$
Thus, the algebraic multiplicity of $\lambda=2$ is 2. Now we row reduce $A-2I$ 

$$
A-2I= \begin{bmatrix}
0 & 1 \\
0 & 0
\end{bmatrix}
$$
Notice that there is one pivot and 1 free variable. Thus, the geometric multiplicity is $1$. Notice that $GM<AM$. (in fact [[5.3 Diagonalization#^7ac6fb]])

> [!question] Challenge:
> 1. Since the GM of $\lambda=2$ is **1**, how many linearly independent eigenvectors does this $2\times 2$ matrix have in total? 
> Ans:1
> 2. To "diagonalize" a matrix, you need a full set of linearly independent eigenvectors to form a basis for the space (in this case, ). Do we have enough eigenvectors to form a basis for  using this matrix?
> Ans: No 
> 3. If we don't have enough eigenvectors, what does that tell you about the "diagonalizability" of this matrix?
> Ans: The matrix is not diagonalizable because we don't have enough number of linearly independent eigenvector to form the basis for $\mathbb{R}^{n}$.

Go back to the question, the qualitative relationship between the free variable and number of eigenvalue is 
The total sum of all free variable (geometric multiplicity) across all distinct eigenvalues is the total number of linearly independent eigenvectors the matrix possesses.

$$
\sum(\text{Free variables for each }\lambda_{i})\leq \text{Total number of eigenvalue (counter with AM)} 
$$

(Why?)

and
This inequality only tell about any eigenvalue. How about distinct eigenvalue?

For any distinct $\lambda_{i}$, $GM_{i}\geq 1$.

Thus,

$$
\begin{align}
1\leq GM\leq AM && (1)
\end{align}
$$
for each $\lambda_{k}$.

The $AM$ represent the number of root of the characteristic polynomial of a matrix $A$. If $A$ is a $n\times n$ matrix, then the polynomial can have at most $n$ root, thus from inequality above we know that $A$ can have at most $n$ distinct eigenvalue and linearly independent eigenvector.


> [!warning]
> The simpler answer:
> We need to consider the Characteristic Polynomial for an $n\times n$ matrix.
> 
> $$
> p(\lambda)=\det(A-\lambda I)
> $$
> where $p(\lambda)$ is a degree $n$ polynomial. By Fundamental Theorem of Algebra, a polynomial of degree $n$ have exactly $n$ complex root. Since we only concern about the real eigenvalue, thus an $n\times n$ matrix can has at most $n$ eigenvalues.
> 
> (This is wrong it doesn't tell us about the uniqueness of eigenvalues)
> 

> [!question] The final challenge
> If you have a $3\times 3$ matrix and you find that it has **three distinct eigenvalues**, what does that automatically tell you about:
> 
> 1. The Algebraic Multiplicity of each eigenvalue? 
> 
> From FTA, we know that the characteristic polynomial of a $3\times 3$ matrix have at most $n$ root. Thus, $AM\leq 3$. Since there 3 distinct eigenvalues, each of them must have at least 1 algebraic multiplicity. Thus, $AM\geq 3$. Combining these 2 inequality, we have $AM=3$. Thus, each of the distinct eigenvalue will have exactly 1 algebraic multiplicity.
> 
> 2. The Geometric Multiplicity of each eigenvalue? 
> We have $1\leq GM\leq AM$. We just prove that $AM=1$, thus $GM=1$.
> 
> 3. The diagonalizability of the matrix? (yes because have 3 linearly independent eigenvectors)

> [!remark]
> Let $A\in M_{n\times n}$ and $\lambda_{1},\lambda_{2},\dots,\lambda_{k}$ for $k\leq n$ be the distinct eigenvalues of $A$.
> Case 1: If  $k=n$, then $A$ is diagonalizable. (The challenge above)
> 
> Case 2: if $k<n$, then $A$ can be diagonalized iff the geometric multiplicity and algebraic multiplicity is the same for every eigenvalue. 
> 
> Why? because the total algebraic multiplicity represent the number of root (and the geometric multiplicity is the number of linearly eigenvector for each $\lambda_{i}$ ) Since $1\leq GM\leq AM$, it follow that $GM=AM$ to have enough linearly eigenvector. 
> 
> Combine this two we only need to check one thing: $A$ is diagonalizable iff $AM_{i}=GM_{i}$ for every $\lambda_{i}$ (This verify the observation from challenge)

==33)==

> [!theorem]
> Let $\lambda$ be an eigenvalue of an invertible matrix $A$. Show that $\lambda^{-1}$ is an eigenvalue of $A^{-1}$. (Hint: Suppose a nonzero $x$ satisfies $Ax=\lambda x$).

Proof:
Since $A$ is invertible matrix, it cannot have eigenvalue of $0$. Thus, $\lambda^{-1}$ is well-defined. (An inverse of a real number is its multiplicative inverse).

Suppose a nonzero $x$ satisfies $Ax=\lambda x$. Thus,

$$
\begin{align}
A^{-1}(Ax)&=A^{-1}(\lambda x) \\
x&=\lambda(A^{-1}x) \\
\lambda^{-1}x&=A^{-1}x
\end{align}
$$

Thus, $\lambda^{-1}$ is the eigenvalue of $A^{-1}$. $\blacksquare$


(Notice that $0$ has no multiplicative inverse)


34)
Suppose $A^{2}$ is 0, then it implies that $A=0$.Thus, by theorem 1, the only eigenvalue of $A$ is 0.



