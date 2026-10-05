1.1
The invertible matrix has unique solution, while a singular matrix has no solution or infinitely many solution.

matrix $E$ for elimination and $P$ for row exchange. $L$ and $U$




1.2 The geometry of linear equations

Consider a 3 variables with 3 equation system.

$$
\begin{align}
2u+v+w&=5 \\
4u-6v&=-2 \\
-2u+7v+2w&=9
\end{align}
$$

Each equation describe a plane in three dimensions. Such plane is determine by 3 point that not lie on a line.

What if we change the right hand side?
Notice that $2u=v+w=10$ pass though $\left( \frac{5}{2},0,0 \right)$ and $(0,5,0)$ and $(0,0,5)$.

What is the change compare to $2u+v+w=10$. Thus, notice that this plane will pass though $(5,0,0)$ and $(0,10,0)$ and $(0,0,10)$, twice as far from the origin. 

![[Pasted image 20260415201747.png]]


In conclusion changing the right side move the plane in parallel way.

The second plane $4u-6v=-2$. 
Notice that it is line in 2 dimension because we have only $u$ and $v$. 

What happen if we add $w$ and $w$ can take any value?
 Thus, the line is extend though the 
 $w$-axis toward infinity.

---

To understand why a line requires $n-1$ equations in an $n$-dimensional space, it helps to think of equations not just as formulas, but as **constraints** that strip away "degrees of freedom."

1. The "Degrees of Freedom" Perspective

Think of a point in $n$-dimensional space as having $n$ different directions it can move ($x_1, x_2, \dots, x_n$).

- **0 Equations:** You have $n$ degrees of freedom. You can move anywhere in the entire $n$-dimensional volume.
    
- **1 Equation:** This acts as a single constraint. It locks one direction in terms of the others. You are left with $n - 1$ degrees of freedom. In 3D, $3 - 1 = 2$, which is a **plane** (a 2D surface).
    
- **2 Equations:** You now have two constraints. You are left with $n - 2$ degrees of freedom. In 3D, $3 - 2 = 1$, which is a **line**.
    

### The General Formula

The dimension of the resulting geometric object (the solution set) is generally:

$$\text{Dimension} = (\text{Ambient Dimensions}) - (\text{Number of Independent Equations})$$

To get a **line** (which is 1-dimensional), you set the Dimension to 1:

$$1 = n - (\text{Number of Equations})$$

$$\text{Number of Equations} = n - 1$$

Equation doesn't means a point , it is a set of point that satisfy the equation , it is a restriction to move along a direction.

### Column vectors and linear combinations

How about the column picture

$$
u\begin{bmatrix}
2 \\
4 \\
-2
\end{bmatrix}+v\begin{bmatrix}
1 \\
-6 \\
7
\end{bmatrix}+w\begin{bmatrix}
1 \\
0 \\
2
\end{bmatrix}=\begin{bmatrix}
5 \\
-2 \\
9
\end{bmatrix}=b
$$

Those are three dimensional column vectors

Every point in three-dimensional space is matched to a vector, and vice versa

Two important operation of vector is addition and multiplication by scalar

A point for example $b=\bigl( \begin{smallmatrix} 5 \\ -2 \\9\end{smallmatrix} \bigr)$ can be view as addiction along each axes

$$
\begin{bmatrix}
5 \\
0 \\
0
\end{bmatrix}+\begin{bmatrix}
0 \\
-2 \\
0
\end{bmatrix}+\begin{bmatrix}
0 \\
0 \\
9
\end{bmatrix}=\begin{bmatrix}
5 \\
-2 \\
9
\end{bmatrix}
$$

![[Pasted image 20260415205545.png]]

With n equations in n unknowns, there are n planes in the row picture. There are n vectors in the column picture, plus a vector b on the right side.

The equations ask for a linear com-bination of then columns that equals b.

---

### When will the elimination break down?

:Singular case

Suppose we are again in three dimensions, and the three planes in the row picture do not intersect.

One possibility is that two planes may be parallel. For example,
$$
\begin{align}
2u+v+w&=5 \\
4u+2v+2w&=11
\end{align}
$$
are inconsistent and parallel planes give no solution.

In two dimensions, parallel lines are the only possibility for breakdown.

But three planes in three dimensions can be in trouble without being parallel.

![[Pasted image 20260415211537.png]]


Each of them view from top.  Notice the $b$ graph represented by

$$
\begin{align}
u+v+w&=2 \\
2u+3w&=5 \\
3u+v+4w&=6
\end{align}
$$

The first two left sides add up to the third. One the right side $2+5\neq 6$.

Notice that if we change $6$ to $7$ which is move the third plane from $b$ to $c$. It will become consistent and have infinitely many solution.


#### What happen to the column picture?

For $b=(2,5,7)$ the point is outside the plane and $b=(2,5,6)$ is in the plane.

$$
\begin{align}
u\begin{bmatrix}
1 \\
2 \\
3
\end{bmatrix}+v\begin{bmatrix}
1 \\
0 \\
1
\end{bmatrix}+w\begin{bmatrix}
1 \\
3 \\
4
\end{bmatrix}
\end{align}
$$
Notice that the $Spam\{ a,b,c \}$ is in a plane but not $\mathbb{R}^{3}$. Because there exist linear dependent vectors.

Because $1.5\mathbf{v}_1 - 0.5\mathbf{v}_2 = \mathbf{v}_3$, the third vector lies entirely within the plane created by the first two. Adding $w\mathbf{v}_3$ to your combination doesn't allow you to reach any "new" height or depth in 3D space.

In other word , there exist a non zero linear combination that add to 0.

---

If then planes have no point in common, or infinitely many points, then then columns lie in the same plane. (linear dependent)

Both of your scenarios—having **no solution** or **infinitely many solutions**—are symptoms of the same underlying condition: the matrix $A$ is **singular** (its determinant is zero).

- **In the Row Picture:** This means the planes don't meet at a single, unique point. They might be parallel (no common point) or they might intersect along a line or a whole plane (infinitely many points).
    
- **In the Column Picture:** This means the columns are linearly dependent. They don't have enough "independent directions" to fill the entire $n$-dimensional space.