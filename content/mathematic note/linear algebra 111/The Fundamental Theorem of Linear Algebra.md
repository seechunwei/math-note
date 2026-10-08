
The theorem describe the action of an $m$ by $n$ matrix. The matrix $A$ produces a linear transformation from $\mathbb{R}^{n}$ to $\mathbb{R}^{m}$.

The truth about $Ax=b$ is expressed in term of four subspaces (two of $\mathbb{R}^{n}$ and two of $\mathbb{R}^{m}$)

First we need to see $Ax$ as a combination of the columns of $A$. This step raise the view point to subspaces. Why?
1) because we could invent vector spaces and construct bases at random.
2) All algorithms and all application are understood by moving to subspaces.

We see $Ax$ as the **column space**. Solving $Ax=b$ means that finding all combination of the columns that produce $b$. (before this we only see entries in $A$ and $x$)

The column space is actually range $R(A)$, a subspace of $\mathbb{R}^{m}$.

The key algorithms in elimination. (elimination didn't change the **row space**). This subspace contains all combinations of the rows of $A$, which is the columns of $A^{T}$. Thus, $RowA=R(A^{T})$.

The third subspace is **nullspace** $N(A)$. It contains all solutions to $Ax=0$. Those solutions are not changed by elimination

Actually the elimination is a tool to reveal the dimension of the subspace which is the first part of this theorem. Because elimination to echelon form show the number of pivot and free variable.

The Fundamental Theorem of Linear Algebra
1) The dimensions of the subspaces.
2) The orthogonality of the subspaces.
3 and 4 in later section

#### The dimension

> [!NOTE] The Rank Theorem
> $$
> dim~R(A)=dim~R(A^{T}) \text{ and }dim~R(A)+dim~N(A)=n
> $$
> 

The column space has dimension of $r$ which implies that the row space has dimension $r$, the nullspace has dimension $n-r$

Elimination identifies $r$ pivot variable and $n-r$ free variables. (Why it is correspond to column? Because we want to explain dimension of row space and nullspace, row space is in $\mathbb{R}^{n}$ which is the number of columns) (Notice that the number of pivot form non zero row)

Thus,
$$
dimR(A)+dimN(A)=n
$$

Since the row of $A$ is the columns of $A^{T}$  and $dim~Col(A)=dim~Row(A)$ it follow that

$$
dim~R(A)=dim~R(A^{T})
$$
(This step emphasis viewing row space of $A$ as the range of $A^{T}$)

(Even though they live in different dimensional vector space but they have same dim)

#### The orthogonality

$Ax$ is the dot product of each row of $A$ and $x$, thus every $x\in N(A)$ is perpendicular to every row of $A$. Thus,

$$
N(A) \perp R(A^{T})
$$
The fourth subspace is the left nullspace $N(A^{T})$. What is that? If a matrix leads to $R(A)$ and $N(A)$, then its transpose must lead to $R(A^{T})$ and $N(A^{T})$.  

Since $R(A^{T})\perp N(A)$, by taking transpose $R(A)\perp N(A^{T})$.( The column space of $A$ is orthogonal to $N(A^{T})$). What is $N(A^{T})$? It is the solution set for $A^{T}y=0$.

![[Pasted image 20260629222257.png]]

Therefore, the left nullspace has dimension $m-r$, because $A^{T}$ is a $n\times m$ matrix.

$A^{T}y=0$ is the same as $y^{T}A=0^{T}$. $y^{T}A$ is a combination of the rows of $A$.

> [!cite] Remark:
> #### When you look at $A^T y = \mathbf{0}$:
> 
> Taking the transpose of $A$ turns its columns into rows. When you multiply $A^T$ by the column vector $y$, you are doing a series of row-by-column dot products:
> 
> $$A^T y = \begin{bmatrix} \text{— } c_1^T \text{ —} \\ \text{— } c_2^T \text{ —} \\ \vdots \\ \text{— } c_n^T \text{ —} \end{bmatrix} y = \begin{bmatrix} c_1 \cdot y \\ c_2 \cdot y \\ \vdots \\ c_n \cdot y \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \\ \vdots \\ 0 \end{bmatrix}$$
> 
> This is just a vertical list of instructions telling you: "$y$ is perpendicular to column 1, $y$ is perpendicular to column 2, etc."
> 
> #### When you look at $y^T A = \mathbf{0}^T$:
> 
> Now, keep $A$ exactly as it is (with its column vectors standing upright), but put the row vector $y^T$ on the left side:
> 
> $$y^T A = y^T \begin{bmatrix} | & | & & | \\ c_1 & c_2 & \dots & c_n \\ | & | & & | \end{bmatrix} = \begin{bmatrix} y \cdot c_1 & y \cdot c_2 & \dots & y \cdot c_n \end{bmatrix} = \begin{bmatrix} 0 & 0 & \dots & 0 \end{bmatrix}$$
> 
> This is a horizontal list of instructions telling you: "$y$ is perpendicular to column 1, $y$ is perpendicular to column 2, etc."
> 
> Thus, besides viewing matrix multiplication as linear combination of row or columns, we can view it as the dot product of each row or columns to the vector.
> #### Summary
> 
> The two equations are not doing two different jobs. They are compiling the **exact same list of dot products**.
> 
> - **$A^T y = \mathbf{0}$** writes that list of zeros as a vertical column.
>     
> - **$y^T A = \mathbf{0}^T$** writes that list of zeros as a horizontal row.
> 
> 

From here we can see that
1) $R(A^{T})$ and $N(A)$ is a subspace in $\mathbb{R}^{n}$
2) $R(A)$ and $N(A^{T})$ is a subspace in $\mathbb{R}^{m}$

By rank theorem, it follow that $dim~N(A)=n-r$ while $dim~N(A^{T})=m-r$

## The First Picture: Linear Equations

With $b \in R(A)$, $Ax=b$ can be solved. There is a particular solution $x$, in the row space. The homogeneous solutions $x_{n}$ form the nullspace. The general solution is $x_{r}+x_{n}$. (Notice that it is the application of Unique Decomposition Theorem )

> [!question]
> Since there are infinitely many $x_{n}$, does it violate the Unique Decomposition Theorem?
> 
> The answer is no, because 
> - If you pick **Solution A** ($x_A$), the theorem guarantees it has a unique split:
>     
>     $$x_A = x_r + x_{nA}$$
>     
>     For $x_A$, you can never find any other nullspace piece besides $x_{nA}$ that works.
>     
> - If you pick **Solution B** ($x_B$), it has its own unique split:
>     
>     $$x_B = x_r + x_{nB}$$
>     
> - If you pick **Solution C** ($x_C$), it has its own unique split:
>     
>     $$x_C = x_r + x_{nC}$$
> Notice that $x_{A}\neq x_{B}\neq x_{C}$. Thus, it is not violating the theorem.

![[Pasted image 20260629231227.png]]

> [!question]
> Why Row Space is connected to Null Space but the number of pivot column is the one determine the dimension of nullspace?
> It is because the number of pivot column is constraint by the row space dimension which is in $\mathbb{R}^{n}$.
> But why the number of pivot indicate the linearly dependency of column vector? Because pivot work for both Row and Column, that's why $dim(Row)=dim(Col)$

## The Second Figure: Least Squares Equations

^177ee1

If $b$ is not in the column space, $Ax=b$ cannot be solve. When it will happen?
When we have more equations than unknowns (overdetermined system)

Thus, we need to choose the closest point to $b$ in that subspace. This point is the projection $b$ onto the columns space. The error vector is $e=b-p$ has minimal length. (This implies that $e$ is perpendicular to the subspace by Theorem 9).

> [!NOTE]
> Let $p=Ax$ for some $x$ and $e=b-Ax$. $e=b-Ax$ is in the left nullspace;
> 
> $$
> A^{T}(b-Ax)=0\implies A^{T}Ax=A^{T}b
> $$
> This is called the normal equation.

> [!cite] Remark
> We can use this to find $x$ for $p=Ax$.
> When you are handed a real-world data problem where $Ax = b$ has no solution, you find $p$ using this exact two-step sequence:
> 
> - **Step 1: Solve for $\bar{x}$.** You take your messy matrix $A$ and vector $b$, calculate the squared matrix $A^TA$ and the squeezed vector $A^Tb$, and solve the normal equations. This gives you the vector $\bar{x}$.
>     
> - **Step 2: Construct $p$.** Once you have $\bar{x}$ in your hands, you plug it right back into your column combination machine:
>     
>     $$p = A\bar{x}$$
> 

> [!question]
> What is the relation between normal equation and Theorem 10 $(UU^{T}y)$?
> 
> . **Theorem 10** told you that _if_ you have a matrix $U$ with **orthonormal columns**, then the projection is incredibly easy to find:
> 
> $$p = UU^T b$$
> Let's see what happens to Strang's Normal Equation $(A^{T}Ax=A^{T}b)$ if the columns of the matrix happen to be perfectly orthonormal, we replace $A$ with $U$:
> 
> $$
> U^{T}Ux=U^{T}b
> $$
> 
> Notice that $U^{T}Ux=x$. Thus,
> 
> $$
> x=U^{T}b
> $$
> Substitute into $p=Ux$. 
> 
> $$
> p=U(U^{T}b)
> $$
> Thus, the theorem 10 is a special case of the normal equations (when $A$ has orthonormal columns)

^06adea


The normal equations show that we start with a rectangular $A$ ($m>n$) end up computing with the square symmetric matrix $A^{T}A$.

> [!tip]
> This matrix is invertible if $A$ has independent columns.

Proof:
Suppose $A$ has independent columns , then $N(A)=\{ 0 \}$. Then

$$
\begin{align}
A^{T}Ax&=0 \\
x^{T}A^{T}Ax&=0 \\
(Ax)^{T}Ax&=0 \\
||Ax||^{2}&=0 \\
Ax&=0
\end{align}
$$
Thus, by our assumption $x=0$. $\blacksquare$

Another approach:
We can use [[6.2 Orthogonal Sets#^fe7f6f]]. Instead the first method come from the proof that $N(A)=N(A^{T}A)$.

> [!question]
> What is the consequence of $A^{T}A$ is invertible?
> We can unique $x$ for each $A^{T}b$, which is the unique part of the decomposition 
> $$
> b=p+e
> $$
> 

^88d74f

![[Pasted image 20260630113659.png]]

## The Third Figure: Orthogonal Bases



Why he propose this? what is the consequences? Is that any relation with the thing i have learnt? 
