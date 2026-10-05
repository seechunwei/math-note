1)
A set of vectors $\{ u_{1},\dots,u_{p} \}$ in $\mathbb{R}^{n}$ is said to be an **orthogonal set** if each distinct pair of vectors from the set is orthogonal, that is $u_{i}\cdot u_{j}=0$ whenever $i\neq j$.

Let $w_{1}=\begin{bmatrix}-1 \\ 4 \\ -3\end{bmatrix},w_{2}=\begin{bmatrix}5 \\ 2 \\ 1\end{bmatrix},w_{3}=\begin{bmatrix}3 \\ -4 \\ -7\end{bmatrix}$


$$
\begin{align}
w_{1}\cdot w_{2}&= w_{1}^{T}w_{2} \\
&=\begin{bmatrix}
-1 & 4 & -3
\end{bmatrix} \begin{bmatrix}
5 \\
2 \\
1
\end{bmatrix} \\
&=0
\end{align}
$$
$$
\begin{align}
w_{1}\cdot w_{3}&=w_{1}^{T}w_{3} \\
&=\begin{bmatrix}
-1 & 4 & -3
\end{bmatrix} \begin{bmatrix}
3 \\
-4 \\
-7
\end{bmatrix} \\
&=2
\end{align}
$$
Since $w_{1}\cdot w_{3}\neq 0$. Thus, the set $\{ w_{1},w_{2},w_{3} \}$ is not an orthogonal set.

> [!remark]
> If $\{ v_{1},\dots,v_{n} \}$ is a orthonormal set
> $$
> v_{i}\cdot v_{j}=\begin{cases}
> 0&i\neq j \\
> 1&i=j
> \end{cases}
> $$
> 

2)

Let $w_{1}=\begin{bmatrix}1 \\ -2 \\ 1\end{bmatrix},w_{2}=\begin{bmatrix}0 \\ 1 \\ 2\end{bmatrix},w_{3}=\begin{bmatrix}-5 \\ -2 \\ 1\end{bmatrix}$

$$
\begin{align}
w_{1}\cdot w_{2}&=w_{1}^{T}w_{2} \\
&=\begin{bmatrix}
1 & -2 & 1
\end{bmatrix}\begin{bmatrix}
0 \\
1 \\
2
\end{bmatrix} \\
&=0
\end{align}
$$

$$
\begin{align}
w_{1}\cdot w_{3}&=w_{1}^{T}w_{3} \\
&= \begin{bmatrix}
1 & -2 & 1
\end{bmatrix} \begin{bmatrix}
-5 \\
-2 \\
1
\end{bmatrix} \\
&=0
\end{align}
$$

$$
\begin{align}
w_{2}\cdot w_{3}&= w_{2}^{T}w_{3} \\
&=\begin{bmatrix}
0 & 1 & 2
\end{bmatrix} \begin{bmatrix}
-5 \\
-2 \\
1
\end{bmatrix} \\
&=0
\end{align}
$$

Since all distinct pair of vectors in the set $\{ w_{1},w_{2},w_{3} \}$ is orthogonal, it follow that it is an orthogonal set.


4)

Let $w_{1}=\begin{bmatrix}2 \\ -5 \\ -3\end{bmatrix},w_{2}=\begin{bmatrix}0 \\ 0 \\ 0\end{bmatrix},w_{3}=\begin{bmatrix}4 \\ 2 \\ 6\end{bmatrix}$

Notice that $w_{2}=0$, thus, $w_{1}\cdot w_{2}=0$ and $w_{2}\cdot w_{3}=0$, because zero vector in a vector space $V$ is orthogonal to every vector in $V$.

Thus. we only need to check $w_{1}\cdot w_{3}$:

$$
\begin{align}
w_{1}\cdot w_{3}&=w_{1}^{T}w_{3} \\
&=\begin{bmatrix}
2 & -5 & -3
\end{bmatrix} \begin{bmatrix}
4 \\
2 \\
6
\end{bmatrix} \\
&=-20
\end{align}
$$

Since $w_{1}\cdot w_{3}\neq 0$, it follow that the set $\{ w_{1},w_{2},w_{3} \}$ is not an orthogonal set.

6)
Let $w_{1}=\begin{bmatrix}5 \\ -4 \\ 0 \\ 3\end{bmatrix},w_{2}=\begin{bmatrix}-4 \\ 1 \\ -3 \\ 8\end{bmatrix},w_{3}=\begin{bmatrix}3 \\ 3 \\ 5 \\ -1\end{bmatrix}$

$$
\begin{align}
w_{1}\cdot w_{2}&=w_{1}^{T}w_{2} \\
&=\begin{bmatrix}
5 & -4 & 0 & 3
\end{bmatrix} \begin{bmatrix}
-4 \\
1 \\
-3 \\
8
\end{bmatrix} \\
&=0
\end{align}
$$

$$
\begin{align}
w_{1}\cdot w_{3}&=w_{1}^{T}w_{3} \\
&=\begin{bmatrix}
5 & -4 & 0 & 3
\end{bmatrix} \begin{bmatrix}
3 \\
3 \\
5 \\
-1
\end{bmatrix} \\
&=0
\end{align}
$$

$$
\begin{align}
w_{2}\cdot w_{3}&=w_{2}^{T}w_{3} \\
&=\begin{bmatrix}
-4 & 1 & -3 & 8
\end{bmatrix} \begin{bmatrix}
3 \\
3 \\
5 \\
-1
\end{bmatrix} \\
&=-32
\end{align}
$$

Since $w_{2}\cdot w_{3} \neq 0$, thus $\{ w_{1},w_{2},w_{3} \}$ is not an orthogonal set.


8)

> [!remark] Remark 1
> To show that a set is an orthogonal basis for $\mathbb{R}^{n}$:
> 
> a. It is an orthogonal set $\implies$ (linearly independent by Theorem 4)
> b.  If linearly independent set have $n$ element, then by The Basis Theorem, it is a basis for $\mathbb{R}^{n}$

Given $u_{1}=\begin{bmatrix}3 \\ 1\end{bmatrix},u_{2}=\begin{bmatrix}-2 \\ 6\end{bmatrix},x=\begin{bmatrix}-4 \\ 3\end{bmatrix}$

Show $S=\{ u_{1},u_{2} \}$ is an orthogonal set:

$$
\begin{align}
u_{1}\cdot u_{2}&=u_{1}^{T}u_{2} \\
&=\begin{bmatrix}
3 & 1
\end{bmatrix}\begin{bmatrix}
-2 \\
6
\end{bmatrix} \\
&=0
\end{align}
$$
Thus, $S=\{ u_{1},u_{2} \}$ is an orthogonal set. Since $S$ are linearly independent set that containing exactly 2 element, it follow that $S$ is a basis for $\mathbb{R}^{2}$(By The Basis Theorem) 

Since $x\in \mathbb{R}^{2}$, then $x \in Span(S)$. Thus, there exist unique $c_{1},c_{2}\in \mathbb{R}$ such that

$$
c_{1}u_{1}+c_{2}u_{2}=x
$$

By theorem 5:

$$
c_{1}= \frac{x\cdot u_{1}}{u_{1}\cdot u_{1}}= -\frac{9}{10}
$$
$$
c_{2}= \frac{x\cdot u_{2}}{u_{2}\cdot u_{2}}= \frac{13}{20}
$$


9)
Given

$$
u_{1}=\begin{bmatrix}
1 \\
0 \\
-1
\end{bmatrix},u_{2}=\begin{bmatrix}
1 \\
-4 \\
1
\end{bmatrix},u_{3}=\begin{bmatrix}
4 \\
2 \\
4
\end{bmatrix},\text{ and }x=\begin{bmatrix}
6 \\
4 \\
-2
\end{bmatrix}
$$

$$
\begin{align}
u_{1}\cdot u_{2}&=0 \\
u_{1}\cdot u_{3}&=0 \\
u_{2}\cdot u_{3}&=0
\end{align}
$$
(Verify by yourself)

Thus, $S=\{ u_{1},u_{2} ,u_{3}\}$ is an orthogonal set. Since $S$ are linearly independent set that containing exactly 3 element, it follow that $S$ is a basis for $\mathbb{R}^{3}$(By The Basis Theorem) 

Since $x\in \mathbb{R}^{3}$, then $x \in Span(S)$. Thus, there exist unique $c_{1},c_{2}.c_{3}\in \mathbb{R}$ such that

$$
c_{1}u_{1}+c_{2}u_{2}+c_{3}u_{3}=x
$$

By theorem 5:

$$
\begin{align}
c_{1}&= \frac{x\cdot u_{1}}{u_{1}\cdot u_{1}}=4 \\
c_{2}&= \frac{x\cdot u_{2}}{u_{2}\cdot u_{2}}= -\frac{2}{3} \\
c_{3}&= \frac{x\cdot u_{3}}{u_{3}\cdot u_{3}}= \frac{2}{3}
\end{align}
$$



11)
Let $u=\begin{bmatrix}1 \\ 7\end{bmatrix}$  ,$w=\begin{bmatrix}-4 \\ 2\end{bmatrix}$ and $Span\{ w \}=L$.

Find the orthogonal projection of $u$ onto $L$ which is $\hat{u}$

$$
\begin{align}
\hat{u}&=proj_{L}u \\
&= \frac{u\cdot w}{w\cdot w}w \\
\end{align}
$$
Calculate $u\cdot w$:

$$
\begin{align}
u\cdot w&=u^{T}w \\
&=\begin{bmatrix}
1 & 7
\end{bmatrix} \begin{bmatrix}
-4 \\
2
\end{bmatrix} \\
&=10
\end{align}
$$

Calculate $w\cdot w$:

$$
\begin{align}
w\cdot w&=w^{T}w \\
&= \begin{bmatrix}
-4 & 2
\end{bmatrix} \begin{bmatrix}
-4 \\
2
\end{bmatrix} \\
&=20
\end{align}
$$
Thus, by substitution

$$
\begin{align}
\hat{u}&= \frac{10}{20} \begin{bmatrix}
-4 \\
2
\end{bmatrix} \\
&= \begin{bmatrix}
-2 \\
1
\end{bmatrix}
\end{align}
$$

> [!remark]
> 
>Notice that we can take any vector $w'\in L$ to calculate $proj_{L}u$, 
refer to question 39) for more information which is not in the exercise

14)

Given $y=\begin{bmatrix}2 \\ 6\end{bmatrix}$ and $u=\begin{bmatrix}6 \\ 1\end{bmatrix}$.

We need to write $y$ as the sum of 2 orthogonal vector , one in Span$\{ u \}$ and one orthogonal to $u$.

> [!question]
> 
> Why we can do that? It is by the Orthogonal Decomposition Theorem in 6.3.
> 
> Let $L=Span\{ u \}$ which is a subspace in $\mathbb{R}^{2}$ (By theorem 1 in Chapter 4), hence by Orthogonal Decomposition Theorem
> 
> $y\in \mathbb{R}^{2}$ can be written unique in the form 
> $$
> y=\hat{y}+z
> $$
> where $\hat{y}=proj_{L}y$ and $z=y-\hat{y}$.

Find $\hat{y}$:

$$
\begin{align}
\hat{y}&= \frac{y\cdot u}{u\cdot u}u
\end{align}
$$

Calculate $y\cdot u$:

$$
\begin{align}
y\cdot u&=y^{T}u \\
&= \begin{bmatrix}
2 & 6
\end{bmatrix} \begin{bmatrix}
6 \\
1
\end{bmatrix} \\
&=18
\end{align}
$$

Calculate $u\cdot u:$

$$
\begin{align}
u\cdot u&= u^{T}u \\
&=\begin{bmatrix}
6 & 1
\end{bmatrix} \begin{bmatrix}
6 \\
1
\end{bmatrix} \\
&=37
\end{align}
$$
Thus, by substitution,

$$
\hat{y}= \frac{18}{37} \begin{bmatrix}
6 \\
1
\end{bmatrix}= \begin{bmatrix}
\frac{108}{37} \\
\frac{18}{37}
\end{bmatrix}
$$

Thus,

$$
\begin{align}
z&=y-\hat{y} \\
&= \begin{bmatrix}
2 \\
6
\end{bmatrix}-\begin{bmatrix}
\frac{108}{37} \\
\frac{18}{37}
\end{bmatrix} \\
&= \begin{bmatrix}
-\frac{34}{37} \\
\frac{204}{37}
\end{bmatrix}
\end{align}
$$
Verification:

$$\hat{y} + z = \begin{bmatrix} \frac{108}{37} \\ \frac{18}{37} \end{bmatrix} + \begin{bmatrix} -\frac{34}{37} \\ \frac{204}{37} \end{bmatrix} = \begin{bmatrix} \frac{74}{37} \\ \frac{222}{37} \end{bmatrix} = \begin{bmatrix} 2 \\ 6 \end{bmatrix} = y \quad \checkmark$$

$$z \cdot u = \begin{bmatrix} -\frac{34}{37} \\ \frac{204}{37} \end{bmatrix} \cdot \begin{bmatrix} 6 \\ 1 \end{bmatrix} = \left(-\frac{34}{37}\right)(6) + \left(\frac{204}{37}\right)(1) = -\frac{204}{37} + \frac{204}{37} = 0 \quad \checkmark$$

16)

Given $y=\begin{bmatrix}-1 \\ 7\end{bmatrix}$ and $u=\begin{bmatrix}1 \\ 3\end{bmatrix}$

> [!remark]
> 
> We need to find the distance from $y$ to the subspace $L=Span\{ u \}$. How to define the distance?
> 
> The distance from $y$ to $L$ is the length of the perpendicular line segment from $y$ to the orthogonal projection $\hat{y}$.
> 
> This line segment is actually the $z$ in The Orthogonal Decomposition Theorem (We will prove that the point identified with $\hat{y}$ is the closest point of $L$ to $y$ in  Theorem 9, 6.3)

The distance is denoted by $||y-\hat{y}||$ (which is the length of $z$)

First we need to find the orthogonal projection of $y$ onto $L$:
$$
\begin{align}
\hat{y}&= \frac{y\cdot u}{u\cdot u}u
\end{align}
$$
Calculate $y\cdot u$:

$$
\begin{align}
y\cdot u&= \begin{bmatrix}
-1 & 7
\end{bmatrix} \begin{bmatrix}
1 \\
3
\end{bmatrix} \\
&=20
\end{align}
$$

Calculate $u\cdot u$:

$$
\begin{align}
u\cdot u&=\begin{bmatrix}
1 & 3
\end{bmatrix}\begin{bmatrix}
1 \\
3
\end{bmatrix} \\
&=10
\end{align}
$$
Thus, by substitution

$$
\begin{align}
\hat{y}&= \frac{20}{10}\begin{bmatrix}
1 \\
3
\end{bmatrix} \\
&=\begin{bmatrix}
2 \\
6
\end{bmatrix}
\end{align}
$$
Thus, 

$$
y-\hat{y}=\begin{bmatrix}
-1 \\
7
\end{bmatrix}-\begin{bmatrix}
2 \\
6
\end{bmatrix}= \begin{bmatrix}
-3 \\
1
\end{bmatrix}
$$

Calculate $||y-\hat{y}||$:

$$
\begin{align}
||y-\hat{y}||&=\sqrt{ (y-\hat{y})\cdot(y-\hat{y}) } \\
&= \sqrt{ \begin{bmatrix}
-3 & 1
\end{bmatrix}\begin{bmatrix}
-3 \\
1
\end{bmatrix} } \\
&=\sqrt{ 10 }
\end{align}
$$

17)

> [!remark]
> 
> A set $\{ u_{1},\dots,u_{p} \}$ is an orthonormal set if it is an orthogonal set of unit vectors.


Let $u_{1}=\begin{bmatrix} \frac{1}{3} \\ \frac{1}{3} \\ \frac{1}{3}\end{bmatrix}$ and $u_{2}=\begin{bmatrix}-\frac{1}{2} \\ 0 \\ \frac{1}{2}\end{bmatrix}$

Check if $u_{1},u_{2}$  is orthogonal:

$$
\begin{align}
u_{1}\cdot u_{2}&= u_{1}^{T}u_{2} \\
&= 0
\end{align}
$$

Check if  $u_{1},u_{2}$ is orthonormal:

$$
\begin{align}
||u_{1}||^{2}&= u_{1}\cdot u_{1} \\
&= \frac{1}{3} \\
||u||&= \sqrt{ \frac{1}{3} }\neq 1
\end{align}
$$

$$
\begin{align}
||u_{2}||^{2}&=u_{2}\cdot u_{2} \\
&= \frac{1}{2} \\
||u_{2}||&=\frac{1}{\sqrt{ 2 }} \neq 1
\end{align}
$$


. Thus, the $\{ u_{1},u_{2} \}$ is not an orthonormal set. We need to normalize the vectors to produce orthonormal set.

Normalizing $u_{1}$:

$$
u_{1}'=\frac{u_{1}}{||u_{1}||}= \begin{bmatrix}
\frac{\sqrt{ 3 }}{3} \\
\frac{\sqrt{ 3 }}{3} \\
\frac{\sqrt{ 3 }}{3}
\end{bmatrix}
$$
Normalizing $u_{2}$:

$$
u_{2}'=\frac{u_{2}}{||u_{2}||}=\begin{bmatrix}
-\frac{\sqrt{ 2 }}{2} \\
0 \\
\frac{\sqrt{ 2 }}{2}
\end{bmatrix}
$$
Verification:

$$
\begin{align}
||u_{1}'||&= 3\left( \frac{\sqrt{ 3 }}{3} \times \sqrt{ \frac{3}{3} }\right) \\
&=1
\end{align}
$$

$$
\begin{align}
||u_{2}||&=\left( -\frac{\sqrt{ 2 }}{2}\times-\frac{\sqrt{ 2 }}{2} \right)+\left( \frac{\sqrt{ 2 }}{2}\times \frac{\sqrt{ 2 }}{2} \right) \\
&=1
\end{align}
$$



Q19 and Q22 is the same as Q17

34)

Suppose $W$ is a subspace of $\mathbb{R}^{n}$ spanned by $n$ nonzero orthogonal vectors, say $S=\{ u_{1},\dots,u_{n} \}$. By theorem 4, $S$ is linearly independent set that has exactly $n$ element. Since $dim\mathbb{R}^{n}=n$, by The Basis Theorem, $S$ is the basis for $\mathbb{R}^{n}$. Thus,

$$
W=Span(S)=\mathbb{R}^{n} ~~\blacksquare
$$

> [!remark]
> The nonzero orthogonal vector is important, because if there exist a zero vector then $S$ is linearly dependent

35)

Suppose $U$ is a square matrix with orthonormal columns. Then, by Theorem 4, the columns of $U$ is  linearly independent. Thus, by Invertible Matrix Theorem, $U$ is invertible. $\blacksquare$

Extra 36)

Suppose $U$ is a $n\times n$ orthogonal matrix. By definition, the columns of $U$ is orthonormal. By exercise 35, we know that $U$ is invertible and by Theorem 6 we know that $U^{T}U=I$. Notice that $U^{T}$ is the left inverse of $U$. Since the inverse is unique it follow that $UU^{T}=I$. $\blacksquare$

> [!remark]
> 
> From exercise 35 and 36 we know that if $U$ is a square matrix with orthonormal columns, then $U$ is invertible and $U^{T}=U^{-1}$.
> 
> Thus, this is why we define an orthogonal matrix is a square invertible matrix such that $U^{-1}=U^{T}$ or equivalently
> 
> $$
> \begin{align}
> U^{T}U&=I ~~(1)\\
> UU^{T}&=I~~(2)
> \end{align}
> $$
> Notice that $(1)$ only require $U$ has orthonormal columns while $(2)$ require $U$ to be square and has orthonormal columns
> 

^9571cf

41)
Given $u\neq 0$ in $\mathbb{R}^{n}$, let $L=Span\{ u \}$. Show that the mapping $x\mapsto proj_{L}x$ is a linear transformation.

Let $T:x\mapsto proj_{L}x$. Thus,

$$
T(x)= \frac{x\cdot u}{u\cdot u}u
$$
We need to show for linearity

L1: $T(x_{1}+x_{2})=T(x_{1})+T(x_{2})$

L2: $T(cx_{1})=cT(x_{1})$

Show L1:
Suppose 2 arbitrary vector $x_{1},x_{2}\in \mathbb{R}^{n}$, we have

$$
\begin{align}
T(x_{1}+x_{2})&=\frac{(x_{1}+x_{2})\cdot u}{u\cdot u}u \\
&=\frac{(x_{1}\cdot u)+ (x_{2}\cdot u)}{u\cdot u}u  \text{ (By theorem 1 in 6.1)}\\
&= \frac{x_{1}\cdot u}{u\cdot u}u+ \frac{x_{2}\cdot u}{u\cdot u}u \\
&= T(x_{1})+T(x_{2})
\end{align}
$$

Show L2:
Suppose arbitrary vector $x_{1}\in \mathbb{R}^{n}$ and any real scalar $c$, we have 
$$
\begin{align}
T(cx_{1})&=\frac{(cx_{1})\cdot u}{u\cdot u}u \\
&=c\left( \frac{x_{1}\cdot u}{u\cdot u} \right)u  \text{ (By theorem 1)} \\
&=cT(x_{1}) &&\blacksquare
\end{align}
$$



> [!remark]
> 
> How to understand this intuitively?
> Orthogonal projection is the shadow when cast a perpendicular light onto the subspace. Thus, add the vector together and cast a shadow is the same as we cast the shadow and add them together.

42)
Given $u\neq 0$ in $\mathbb{R}^{n}$, let $L=Span\{ u \}$. For $y\in \mathbb{R}^{n}$, the reflection of $y$ in $L$ is the point $reft_{L}y$ denoted by

$$
reft_{L}y=2proj_{L}y-y
$$
Why? see from the graph

![[Pasted image 20260702154619.png]]

The point $reft_{L}y$ is define as 

$$
\begin{align}
\hat{y}-(y-\hat{y})&=2\hat{y}-y \\
&=2proj_{L}y-y
\end{align}
$$

We need to show that $T:x\mapsto reft_{L}y$ is a liner transformation. 

Thus, We need to show for linearity

L1: $T(x_{1}+x_{2})=T(x_{1})+T(x_{2})$

L2: $T(cx_{1})=cT(x_{1})$

Show L1:
Suppose 2 arbitrary vector $x_{1},x_{2}\in \mathbb{R}^{n}$ , we have
$$
\begin{align}
T(x_{1}+x_{2})&= 2proj_{L}(x_{1}+x_{2})+(x_{1}+x_{2}) \\
&=2(proj_{L}x_{1}+proj_{L}x_{2})+(x_{1}+x_{2}) \text{ (By Q41)} \\
&=(2proj_{L}x_{1}+x_{1})+(2proj_{L}x_{2}+x_{2}) \\
&=T(x_{1})+T(x_{2})
\end{align}
$$

Show L2:
Suppose arbitrary vector $x_{1}\in \mathbb{R}^{n}$ and any real scalar $c$, we have 

$$
\begin{align}
T(cx_{1})&= 2proj_{L}(cx_{1})+cx_{1} \\
&=c (2proj_{L}x_{1}+x_{1}) \text{ (By Q41)}\\
&=cT(x_{1}) &&\blacksquare
\end{align}
$$

