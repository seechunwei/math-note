The history
1) system of linear equation
2) augmented matrix form
3) vector equation

from ref alone we can know the number of pivot and free variable

from rref we can get the particular solutions set

### 1.4 Spanning set
The motivation of the learning of spanning set is to able to study the properties of a set $v$ with $|v|=\infty$ using a small finite subset of $v$.

For example, the general form of $\mathbb{R}^{2}$ ^123

$$
\begin{align}
\mathbb{R}^{2}&=\{ \bigl( \begin{smallmatrix} a \\ b\end{smallmatrix} \bigr)| a,b \in \mathbb{R} \} \\
&= \{ a\bigl( \begin{smallmatrix} 1\\ 0\end{smallmatrix} \bigr)+b \bigl( \begin{smallmatrix} 0\\1\end{smallmatrix} \bigr)|a,n \in \mathbb{R} \}
\end{align}
$$

Notice that $e_{1}=\bigl( \begin{smallmatrix} 1\\0\end{smallmatrix} \bigr)$ and $e_{2}=\bigl( \begin{smallmatrix} 0\\1\end{smallmatrix} \bigr)$. $e_{1}$ and $e_{2}$ from the axes for a cartesian $xy-plane$. 

Thus, we can study the properties of linear combination of these 2 vector as the properties of $\mathbb{R}^{2}$. We cannot study the property of $\mathbb{R}^{2}$ directly because it has infinitely many solution.

If $\mathbb{R}^{n}$ then we need $n$ vectors such as $\{ e_{1},\dots e_{n} \}$ to span $\mathbb{R}^{n}$. Each vector act as one of the axis in $n$-dimensional matrix.

Consider the set below
$$
\begin{align}
A&=\{ \bigl( \begin{smallmatrix} a\\1\end{smallmatrix} \bigr)|a \in \mathbb{R} \} \\
&=\{ a\bigl( \begin{smallmatrix} 1\\0\end{smallmatrix} \bigr)+\bigl( \begin{smallmatrix} 0\\ 1\end{smallmatrix} \bigr) |a \in \mathbb{R}\}
\end{align}
$$

Notice that $A$ does not span whole $\mathbb{R}^{2}$ because it cannot express as linear combination of 2 linear independent vector.

==Remark==
The general solution for a non-invertible matrix is never a vector space because it is in the form

$$
x=x_{p}+x_{n}
$$
where $x_{p}$ is the particular solution for certain $b$. (it didn't pass though the origin) and cannot express as linear combination of $n$ vectors in $\mathbb{R}^{n}$.

But $x_{n}$ itself form a subspace of $\mathbb{R}^{n}$(nullspace).


---
How a spanning set look?

What is the spanning set of one vector $v \in \mathbb{R}^{n}$.

Case 1: $v= 0$. Then 

$$
\begin{align}
Span\{ v \}&=\{ av|a \in \mathbb{R} \} \\
&=\{ a0|a \in \mathbb{R} \} \\
&=\{ 0 \}
\end{align}
$$

So $Span\{ 0 \}=0$.

Case 2: $v \neq 0$. Then
$$
Span\{ v \}=\{ kv|v \in \mathbb{R} \}
$$
It is a line by expanding $v$.

Why?
Because $v$ is a point in $\mathbb{R}^{n}$ and it form a line by connecting the origin. Thus, the linear combination of it is just the line expanding in 2 direction.


### How about spanning set of 2 vectors

WLOG Let $v_{1}=0$, $v_{2}\neq 0$. Then $Span\{ v_{1},v_{2} \}=Span\{ v_{2} \}$. Why?

$$
\begin{align}
Span\{ v_{2},v_{2} \}&=\{ av_{1}+bv_{2}|a,b \in \mathbb{R} \} \\
&=\{ a(0)+bv_{2}|a,b \in \mathbb{R} \} \\
&=\{ bv_{2}|b \in \mathbb{R} \} \\
&=Span\{ v_{2} \}
\end{align}
$$


What happen if $v_{1}=cv_{2}$ for some $c \in \mathbb{R}\setminus\{ 0 \}$. Or we can say that 

Case 1: $v_{1}\in Span\{ v_{2} \}$ 

Then ,

$$
\begin{align}
Span\{ v_{1},v_{2} \}&=\{ a_{1}v_{1}+a_{2}v_{2}|a_{1},a_{2}\in \mathbb{R} \} \\
&=\{ a_{1}(cv_{2})+a_{2}v_{2}|a_{1},a_{2}\in \mathbb{R} \} \\
&=\{ (a_{1}c+a_{2})v_{2}|a_{1},a_{2}\in \mathbb{R} \} \\
&=\{ bv_{2}|b \in \mathbb{R} \} \\
&=Span\{ v_{2} \}
\end{align}
$$

$v_{1}\in Span\{ v_{2} \}$ iff $v_{2} \in Span\{ v_{1} \}$. Thus, it follow that ^123

$$
Span\{ v_{1},v_{2} \}=Span\{ v_{1} \}=Span\{ v_{2} \}
$$

The spanning set is still a line.

Case 2: $v_{1} \not\in Span\{ v_{1} \}$.
Then


$$
Span\{ v_{1},v_{2} \}=\{ a_{1}v_{1}+a_{2}v_{2}|a_{1}.a_{2} \in \mathbb{R} \}
$$

![[Pasted image 20260503153506.png]]
![[Pasted image 20260503153606.png]]

In this case $v_{1},v_{2}$ vectors form the axes of a plane and any point lies in the plane can be express as the linear combination of $v_{1},v_{2}$.

---
The next section talk about the existence of free variable make the number solution set of some $b$ is infinity many iff $Ax=0$ has solution set.

It is because we can take any value of free variable. (The existence of $x_{n}$)

---
1.5
If one of the column vector in $A$ is in spanning set of the other vector. Then in rref. there exist a column that represent the certain free variable in this form

$$
\begin{bmatrix}
a_{1} \\
a_{2} \\
\dots \\
0
\end{bmatrix}
$$
(linearly dependent)

If there is 2, then there exist 2 column like this with last $m-r$ row of 0

![[Pasted image 20260503200620.png]]


A vector $v \in \text{Span}\{v_{1}, \dots, v_{n}\}$ can be written **uniquely** as a linear combination **if and only if** no vector in the set is a linear combination of the vectors that came before it.

For example

$$
\begin{bmatrix}
1 & 0 & 2 \\
0 & 1 & 3 \\
0 & 0 & 0
\end{bmatrix}
$$
Since $c_{1},c_{2}$ is linearly independent. Thus, it follow that if $c_{3}\in Span\{ c_{1},c_{2} \}$, then $c_{3}$ can be express uniquely as the linear combination of $c_{1},c_{2}$, which is

$2c_{1}+3c_{2}=c_{3}$.

What if $v_{1} \in Span\{ v_{2} \}$? Then the rref form will be like this

$$
\begin{align}
\begin{bmatrix}
1 & 1 & 2 \\
0 & 0 & 0 \\
0 & 0 & 0
\end{bmatrix}
\end{align}
$$

Thus,
$c_{3}=(2-c_{2})c_{1}+c_{2}$ where $c_{2} \in \mathbb{R}$. Thus, it has infinity way to express.
 
==Remark==
This is not what lecturer trying to say but it is true also

Lecturer is trying to say 
$c_{3}=2c_{1}+1c_{2}+0c_{3}$ or
$c_{3}=0c_{1}+0c_{2}+1c_{1}$

Thus, in general if $b \in Span\{ v_{1},v_{2},\dots,v_{n} \}$, then $b$ can be written uniquely as the linear combination of $v_{1},v_{2},\dots,v_{n}$ iff $v_{i+1}\not\in Span\{ v_{1},v_{2},\dots,v_{i} \}$ for every $i \in \{ 1,2,\dots n-1 \}$. ==The uniqueness Theorem==


---
The last section use the concept of block matrix, we can ignore some column in the augmented matrix to find different solution set. 

![[Pasted image 20260503155554.png]]

In fact the column of nullspace matrix form by solving the pivot matrix as $A$ and one of the non-pivot column in $x$, and solve for $Ax=0$.