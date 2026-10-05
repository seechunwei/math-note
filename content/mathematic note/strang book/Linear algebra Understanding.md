First we want to solve a system of linear equation and we use gaussian elimination to solve. But it is too much to write can i ignore the variable and just write the coefficient. Then it become a mathematic object like this

$$
\begin{bmatrix}
1 & 2 & 3 \\
2 & 3 & 4 \\
4 & 5 & 6
\end{bmatrix}
$$
It is called matrix , thus we do our elimination process as we solve the system of linear equation. We want to reach something like this

$$
\begin{bmatrix}
a & * & *  \\
0 & b & * \\
0 & 0 & c
\end{bmatrix}
$$
We do elimination to reach until this form where $a,b,c\in \mathbb{R}$ and they represent the variable. We can see from the system of equation below

$$
\begin{align}
ax_{1}+*x_{2}+*x_{3}&=* \\
bx_{2}+*x_{3}&=* \\
cx_{3}&=*
\end{align}
$$

Thus, we just need to do the back substitution. Notice that back substitution can be done using matrix which is we try to make every pivot become 1 and eliminate each coefficient above pivot. Thus, we will reach this form

$$
\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix}
$$

And after that mathematician start to realize that a system of linear equation can be write in this form by collecting the same variable in each equation and form a vector which each entry determine the coefficient of equation

$$
c_{1}x_{1}+c_{2}x_{2}+\dots.+c_{n}x_{n}=b
$$
where $c_{n}$ is the $n-th$ column of the matrix $A$ and also is the column of the system of linear equation.  

Thus we will have the system of linear equation as the multiplication of matrix $Ax=b$

$$
\begin{bmatrix}
1 & 1 & 1 \\
 1 & 1 & 1 \\
1 & 1 & 1
\end{bmatrix}\begin{bmatrix}
x_{1} \\
x_{2} \\
x_{3}
\end{bmatrix}=\begin{bmatrix}
b_{1} \\
b_{2} \\
b_{3}
\end{bmatrix}
$$

From here we can define the multiplication of matrix with a vector denoted by $Ax$ as the linear combination of column of $A$ with entry of $x$ as weights.

It is equivalent of solving the augmented matrix as below:

$$
\begin{bmatrix}
x_{1} & x_{2} & \dots & x_{n} & b
\end{bmatrix}
$$


How about the multiplication of matrix?
Imagine the column is adjoint together and form a matrix. For example,

$$
\begin{bmatrix}
1 & 1 & 1 \\
1 & 1 & 1 \\
1 & 1 & 1
\end{bmatrix}\begin{bmatrix}
1 & 4 \\
2 & 5 \\
3 & 6
\end{bmatrix}=\begin{bmatrix}
1 & 1 & 1 \\
1 & 1 & 1 \\
1 & 1 & 1
\end{bmatrix}\begin{bmatrix}
1 \\
2 \\
3 \\
\end{bmatrix} \text{adjoint with}\begin{bmatrix}
1 & 1 & 1 \\
1 & 1 & 1 \\
1 & 1 & 1
\end{bmatrix} \begin{bmatrix}
4 \\
5 \\
6
\end{bmatrix}
$$

Thus, clearly we can see every column of $AB$ is the linear combination of $A$. and every row of $AB$ is the linear combination of row of $B$. 

And from here, notice that $a_{ij}$ is determine by the i row of $A$ and $j$ column of $B$, thus for the sake of computation we come out with the dot product and outer product.


Notice that if we multiply the whole system with 2, we still get the same solution set, but we cannot say they are equal because $A-A'\neq 0$, thus we come out with the row equivalent concept so that when we do row operation it preserve the solution set.


$$
\begin{bmatrix}
1 & 1 & 1 \\
1 & 1 & 1 \\
1 & 1 & 1
\end{bmatrix} \sim \begin{bmatrix}
2 & 2 & 2 \\
2 & 2 & 2 \\
2 & 2 & 2
\end{bmatrix}
$$

We say two matrix is equal iff each entry are the same.(it is like the set is determine by its element)

So the next question is the system can be no solution or infinitely many solution. Notice that it happened when there exist at least one row that don't have pivot and it is determined by the last entry of $c$. Let the elimination process be

$$
\begin{align}
Ax=b \\
EAx=Eb \\
Ux=c
\end{align}
$$
$E$ is a matrix that represent the sequence of row operation.

Notice that the final result of elimination is a Upper triangular matrix and a important concept come in which is the inverse matrix. We know that row operation is inversible, thus by performs the inverse of row operation we can get $U$ to $A$. And we notice that the inverse of $E$ is a Lower triangular matrix denoted by $L$. Thus, 

$$
A=LU
$$
and $U$ can have non 1 pivot and thus pivot can be factorize in to a $DU$. where $U$ now only have 1 in its diagonal

$$
A=LDU
$$
and in fact it something to do with the diagonalization and it link to the concept later on which if a matrix $A$ is invertible and symmetric, then 

$$
A=LDL^{T}
$$

If we view the $Ax=b$ as a function (transformation), then the invertible matrix is the matrix that have uniquely solution $x$ for every $b$. (one to one and onto). Inverse matrix act like an inverse function!!!

==Existence==
And remember that if a system have at least one solution for each $b$ , then it must have pivot in every row (if not the right most column of the augmented matrix will have pivot)!!!!
==Uniqueness==
Each column have a pivot(it depend on the number of variable)


---

### The existence

But we didn't focus much in vector, which in fact is the heart of linear algebra. 

Notice that the linear combination of column of $A$ is called a spanning set of the vectors set. The main reason why we study the spanning set is to study infinite object in a set using finite object where the object hold the all property as other object in the set.

And it always span a vector space. In fact determine the existence of $b$ is equivalent of asking if $b$ is lying in the space that spanned by column vector of $A$.

All the $b$ that have solution is in the space. And the solution set for $Ax=0$ is always a vector space because it can be linear combination of zero vector(trivial solution) or at least 1 non zero vector (non trivial solution).


### The uniqueness

In fact if a vector set $\{ v_{1},\dots v_{n} \}$ span $\mathbb{R}^{m}$, it exist 2 cases

Case 1: For every $b\in \mathbb{R}^{m}$, there exist unique $a_{i}$ where $i\in \{ 1,\dots,n \}$ such that $b=a_{1}v_{1}+\dots+a_{n}v_{n}$  


Case 2: For every $b\in \mathbb{R}^{m}$, there exist non-unique $a_{i}$ where $i\in \{ 1,\dots,n \}$ such that $b=a_{1}v_{1}+\dots+a_{n}v_{n}$  


From here mathematician come out with the concept linear independent. Intuitively, linear independent is when each vector is being use in spanning the vector space. (no wasted vector, no vector is overlap).  


In fact a generating set of $\mathbb{R}^{n}$ is denoted as below:

$$
\begin{align}
\mathbb{R}^{n}&=Span\{ e_{1},\dots,e_{n} \} \\
&=\{ a_{1}e_{1}+\dots+a_{n}e_{n} \}
\end{align}
$$
A basis for $V$ is a sequence of vectors having  two properties at once:
1. The vectors are linearly independent (not too many vectors).
2. They span the space V (not too few vectors). 

Thus, notice that a set of linear independent vectors are determine by if there exist a $v \in \{ v_{1},\dots v_{p} \}$ such that $v\in Span\{ v_{1},\dots.v_{n-1} \}$. Why? [[Dr ang online class first may#^123]]

Thus, if this happen, there must exist at least one column of ref(A) that don't have pivot. In fact this is determine by the existence of free variable (Rank Nullity Theorem). This is because the general solution set for $Ax=0$ is 
$$
x=x_{p}+x_{n}
$$
This is why the definition of linearly independent link to the dimensional of nullspace.
Thus, and from definition we can deduce the column must have pivot in order for $Ax=0$ has only trivial solution.

==Theorem==
The column vector of $A$ is linearly independent iff the nullspace is a zero vector.

==Theorem==
Suppose  $Span\{ v_{1}\dots.v_{n} \}=\mathbb{R}^{n}$. A vector set $\{ v_{1},\dots.v_{n} \}$ is linearly independent over $\mathbb{R}$ and iff for every $b\in Span\{ v_{1},\dots,v_{n} \}$,  $b$ can be written uniquely as a linear combination of $\{ v_{1},\dots,v_{n} \}$.

Proof:
Forward direction:
Suppose a linearly independent vector set $\{ v_{1},\dots v_{n} \}$. Thus, by definition there exist only trivial solution for $a_{1},\dots a_{n}\in \mathbb{R}$ such that 
$$
a_{1}v_{1}+\dots.a_{n}v_{n}=0
$$

Suppose $b \in \mathbb{R}^{n}$ and 
$$
\begin{align}
b&=c_{1}v_{1}+\dots.+c_{n}v_{n} \\
b&=d_{1}v_{1}+\dots+d_{n}v_{n}
\end{align}
$$
such as $c_{i},d_{i}\in \mathbb{R}$ for every $i\in \{ 1,\dots ,n \}$. Thus,

$$
\begin{align}
(c_{1}-d_{1})v_{1}+\dots+(c_{n}-d_{n})v_{n}=0
\end{align}
$$
Thus, it follow that $(c_{i}-d_{i})=0$ for every $i$. Therefore, $c_{i}=d_{i}$. (Contradiction, we suppose there exist 2 linear combination that equal to b)

Backward direction:
Suppose for every $b\in Span\{ v_{1},\dots,v_{n} \}$,  $b$ can be written uniquely as a linear combination of $\{ v_{1},\dots,v_{n} \}$. Thus, since $0\in \mathbb{R}^{n}$, it follow that there exist unique $a_{1},\dots a_{n}\in \mathbb{R}$ such that

$$
a_{1}v_{1}+\dots+a_{n}v_{n}=0
$$
Q.E.D.
 
---
Vector space over $\mathbb{R}$.
