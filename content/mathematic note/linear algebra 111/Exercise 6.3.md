1)

Given $\{ u_{1},\dots,u_{4} \}$ is an orthogonal basis for $\mathbb{R}^{4}$ such that

$$
u_{1}=\begin{bmatrix}
0 \\
1 \\
-4 \\
-1
\end{bmatrix},u_{2}=\begin{bmatrix}
3 \\
5 \\
1 \\
1
\end{bmatrix},u_{3}=\begin{bmatrix}
1 \\
0 \\
1 \\
-4
\end{bmatrix},u_{4}=\begin{bmatrix}
5 \\
-3 \\
-1 \\
1
\end{bmatrix} \text{ and }x=\begin{bmatrix}
10 \\
-8 \\
2 \\
0
\end{bmatrix}
$$

Since $x\in \mathbb{R}^{4}$, it follow that $x\in Span\{ u_{1},..,u_{4} \}$. Thus, by theorem 5, 

$$
x= \frac{x\cdot u_{1}}{u_{1}\cdot u_{1}}u_{1}+ \frac{x\cdot u_{2}}{u_{2}\cdot u_{2}}u_{2}+ \frac{x\cdot u_{3}}{u_{3}\cdot u_{3}}u_{3}+ \frac{x\cdot u_{4}}{u_{4}\cdot u_{4}}u_{4} 
$$

Calculating first term:

$$
\begin{align}
\frac{x\cdot u_{1}}{u_{1}\cdot u_{1}}u_{1}&= \frac{-16}{18} \begin{bmatrix}
0 \\
1 \\
-4 \\
-1
\end{bmatrix} \\
&= \begin{bmatrix}
0 \\
-\frac{16}{18} \\
\frac{32}{9} \\
\frac{8}{9}
\end{bmatrix}
\end{align}
$$

Calculating second term:

$$
\begin{align}
\frac{x\cdot u_{2}}{u_{2}\cdot u_{2}}u_{2}&= -\frac{8}{36} \begin{bmatrix}
3 \\
5 \\
1 \\
1
\end{bmatrix} \\
&= \begin{bmatrix}
-\frac{2}{3} \\
-\frac{10}{9} \\
-\frac{8}{36} \\
-\frac{8}{36}
\end{bmatrix}
\end{align}
$$

Calculating third term:

$$
\begin{align}
\frac{x\cdot u_{3}}{u_{3}\cdot u_{3}}u_{3}&= \frac{12}{18} \begin{bmatrix}
1 \\
0 \\
1 \\
-4
\end{bmatrix} \\
&= \begin{bmatrix}
\frac{2}{3} \\
0 \\
\frac{2}{3} \\
-\frac{8}{3}
\end{bmatrix}
\end{align}
$$

Calculating fourth term:

$$
\begin{align}
\frac{x\cdot u_{4}}{u_{4}\cdot u_{4}}u_{4}&=  \frac{72}{36} \begin{bmatrix}
5 \\
-3 \\
-1 \\
1
\end{bmatrix} \\
&=\begin{bmatrix}
10 \\
-6 \\
-2 \\
2
\end{bmatrix}
\end{align}
$$
Notice that the sum of first 3 term is in $Span\{ u_{1},u_{2},u_{3} \}$ while the forth term is in $Span\{ u_{4} \}$.

5)
Check if $\{ u_{1},u_{2} \}$ is an orthogonal set:

$$
\begin{align}
u_{1}\cdot u_{2}&= \begin{bmatrix}
3 & -1 & 2
\end{bmatrix} \begin{bmatrix}
1 \\
-1 \\
-2
\end{bmatrix} \\
&=0
\end{align}
$$
Thus, $\{ u_{1},u_{2} \}$ is an orthogonal set.

Let $L=Span\{ u_{1},u_{2} \}$ and $\hat{y}=proj_{L}y$. Thus,

$$
\begin{align}
\hat{y}&= \frac{y\cdot u_{1}}{u_{1}\cdot u_{1}}u_{1}+ \frac{y\cdot u_{2}}{u_{2}\cdot u_{2}}u_{2} \\
&= \frac{7}{14}\begin{bmatrix}
3 \\
-1 \\
2
\end{bmatrix}+ -\frac{15}{6} \begin{bmatrix}
1 \\
-1 \\
-2
\end{bmatrix} \\
&= \begin{bmatrix}
\frac{3}{2} \\
-\frac{1}{2} \\
1
\end{bmatrix} + \begin{bmatrix}
-\frac{15}{6} \\
\frac{15}{6} \\
5
\end{bmatrix} \\
&= \begin{bmatrix}
-1 \\
2 \\
6
\end{bmatrix}
\end{align}
$$

Q6 is the same as Q5

7)
Given $y=\begin{bmatrix}1 \\ 3 \\ 5\end{bmatrix},u_{1}=\begin{bmatrix}1 \\ 3 \\ -2\end{bmatrix},u_{2}=\begin{bmatrix}5 \\ 1 \\ 4\end{bmatrix}$

Let $L=Span\{ u_{1},u_{2} \}$ and let $\hat{y}=\text{proj}_{L}y$ . Thus,

$$
\begin{align}
\hat{y}&= \frac{y\cdot u_{1}}{u_{1}\cdot u_{1}}u_{1}+ \frac{y\cdot u_{2}}{u_{2}\cdot u_{2}}u_{2} \\
&= \frac{0}{14}u_{1}+ \frac{2}{3} \begin{bmatrix}
5 \\
1 \\
4
\end{bmatrix} \\
&= \begin{bmatrix}
\frac{10}{3} \\
\frac{2}{3} \\
\frac{8}{3}
\end{bmatrix}
\end{align}
$$

> [!remark]
> Notice that $y\cdot u=0$, thus it follow that $y$ and $u$ are orthogonal to each other.

Let $z=y-\hat{y}$. Thus,

$$
\begin{align}
z&= \begin{bmatrix}
1 \\
3 \\
5
\end{bmatrix}-\begin{bmatrix}
\frac{10}{3} \\
\frac{2}{3} \\
\frac{8}{3}
\end{bmatrix}= \begin{bmatrix}
-\frac{7}{3} \\
\frac{7}{3} \\
\frac{7}{3}
\end{bmatrix}
\end{align}
$$

By Orthogonal Decomposition Theorem,

$$
y=\hat{y}+z
$$
where $\hat{y}\cdot z=0$.

Verification:
$$\hat{y} \cdot z = \left( \frac{10}{3} \right) \left( -\frac{7}{3} \right) + \left( \frac{2}{3} \right) \left( \frac{7}{3} \right) + \left( \frac{8}{3} \right) \left( \frac{7}{3} \right)=0$$



9)
Given $y=\begin{bmatrix}4 \\ 3 \\ 3 \\ -1\end{bmatrix},u_{1}=\begin{bmatrix}1 \\ 1 \\ 0 \\ 1\end{bmatrix},u_{2}=\begin{bmatrix}-1 \\ 3 \\ 1 \\ -2\end{bmatrix},u_{3}=\begin{bmatrix}-1 \\ 0 \\ 1 \\ 1\end{bmatrix}$
Let $L=Span\{ u_{1},u_{2},u_{3} \}$ and let $\hat{y}=\text{proj}_{L}y$.

$$
\begin{align}
\hat{y}&= \frac{y\cdot u_{1}}{u_{1}\cdot u_{1}}u_{1}+ \frac{y\cdot u_{2}}{u_{2}\cdot u_{2}}u_{2}+ \frac{y\cdot u_{3}}{u_{3}\cdot u_{3}}u_{3} \\
&= \frac{6}{3}\begin{bmatrix}
1 \\
1 \\
0 \\
1
\end{bmatrix}+ \frac{10}{15}\begin{bmatrix}
-1 \\
3 \\
1 \\
-2
\end{bmatrix}- \frac{2}{3}\begin{bmatrix}
-1 \\
0 \\
1 \\
1
\end{bmatrix} \\
&= \begin{bmatrix}
2 \\
4 \\
0 \\
0
\end{bmatrix}
\end{align}
$$

Let $z=y-\hat{y}$. Thus, 

$$z = y - \hat{y} = \begin{bmatrix} 4 \\ 3 \\ 3 \\ -1 \end{bmatrix} - \begin{bmatrix} 2 \\ 4 \\ 0 \\ 0 \end{bmatrix} = \begin{bmatrix} 2 \\ -1 \\ 3 \\ -1 \end{bmatrix}$$

Thus, by The Decomposition Theorem

$$
y=\hat{y}+z
$$
where $\hat{y}\cdot z=0$

Verification:
$$\hat{y} \cdot z = (2)(2) + (4)(-1) + (0)(3) + (0)(-1)=0$$

 
12)
Let $W=Span\{ v_{1},v_{2} \}$ , by Best Approximation Theorem, the closest point to $y$ in the subspace $W$ is the orthogonal projection of $y$ onto $W$ which is $\hat{y}=\text{proj}_{W}y$ in the sense of 

$$
||y-\hat{y}||\leq||y-v||
$$
for any $v\in W$.

Thus, 

$$
\begin{align}
\hat{y}&= \frac{y\cdot v_{1}}{v_{1}\cdot v_{1}}v_{1}+ \frac{y\cdot v_{2}}{v_{2}\cdot v_{2}}v_{2} \\
&= \frac{10}{10} \begin{bmatrix}
2 \\
1 \\
-2 \\
1
\end{bmatrix}+ \frac{4}{4} \begin{bmatrix}
1 \\
1 \\
1 \\
-1
\end{bmatrix} \\
&= \begin{bmatrix}
3 \\
2 \\
-1 \\
0
\end{bmatrix}
\end{align}
$$

13)
Let $W=Span\{ v_{1},v_{2} \}$, the question want us to find the closest point to $z$ in $W$. By Best Approximation Theorem, this point is $\hat{z}=\text{proj}_{W}z$. Thus,

$$
\begin{align}
\hat{z} &= \frac{z \cdot v_1}{v_1 \cdot v_1} v_1 + \frac{z \cdot v_2}{v_2 \cdot v_2} v_2 \\
&= \frac{10}{15}\begin{bmatrix}
2 \\
-1 \\
-3 \\
1
\end{bmatrix}- \frac{7}{3}\begin{bmatrix}
1 \\
1 \\
0 \\
-1
\end{bmatrix} \\
&= \begin{bmatrix}
-1 \\
-3 \\
-2 \\
3
\end{bmatrix}
\end{align}
$$


16）
The distance from  $y$ to the subspace $W$ is $||y-\hat{y}||$:

Calculate $y-\hat{y}$:

$$
y-\hat{y}=\begin{bmatrix}
4 \\
3 \\
4 \\
7
\end{bmatrix}- \begin{bmatrix}
3 \\
2 \\
-1 \\
0
\end{bmatrix}= \begin{bmatrix}
1 \\
1 \\
5 \\
7
\end{bmatrix}
$$

Thus,

$$
\begin{align}
||y-\hat{y}||&= \sqrt{ (y-\hat{y})^{T}(y-\hat{y}) } \\
&= \sqrt{ 76 }
\end{align}
$$

18)
Let $y=\begin{bmatrix}7 \\ 9\end{bmatrix},u_{1}=\begin{bmatrix} \frac{1}{\sqrt{ 10 }} \\ -\frac{3}{\sqrt{ 10 }}\end{bmatrix}$ and $W=\text{Span}\{ u_{1} \}$ 

a) 
$$
\begin{align}
U^{T}U=1
\end{align}
$$
$$
\begin{align}
UU^{T}&= \begin{bmatrix}
\frac{1}{\sqrt{ 10 }} \\
-\frac{3}{\sqrt{ 10 }}
\end{bmatrix} \begin{bmatrix}
\frac{1}{\sqrt{ 10 }} & -\frac{3}{\sqrt{ 10 }}
\end{bmatrix} \\
&=\begin{bmatrix}
\frac{1}{10} & -\frac{3}{10} \\
-\frac{3}{10} & \frac{9}{10}
\end{bmatrix}
\end{align}
$$
b)

Calculate $\text{proj}_{W}y$:

$$
\begin{align}
\text{proj}_{W}y&= \frac{y\cdot u_{1}}{u_{1}\cdot u_{1}}u_{1} \\
&=-\frac{2\sqrt{ 10 }}{1} \begin{bmatrix}
\frac{1}{\sqrt{ 10 }} \\
-\frac{3}{\sqrt{ 10 }}
\end{bmatrix} \\
&= \begin{bmatrix}
-2 \\
6
\end{bmatrix}
\end{align}
$$

Calculate $(UU^{T})y$:

$$
\begin{align}
(UU^{T})y&= \begin{bmatrix}
\frac{1}{10} & -\frac{3}{10} \\
-\frac{3}{10} & \frac{9}{10}
\end{bmatrix}\begin{bmatrix}
7 \\
9
\end{bmatrix} \\
&= \begin{bmatrix}
-2 \\
6
\end{bmatrix}
\end{align}
$$

> [!remark]
> This is the verification of theorem 10 because $u_{1}$ is an orthogonal unit vector.

19)

Given $u_{1}=\begin{bmatrix}1 \\ 1 \\ 1\end{bmatrix},u_{2}=\begin{bmatrix}1 \\ -2 \\ 1\end{bmatrix}$ and $u_{3}=\begin{bmatrix}0 \\ 0 \\ 1\end{bmatrix}$ such that $u_{1}\cdot u_{2}=0$ but $u_{3}$ is not orthogonal to $u_{1}$ or $u_{2}$. 

Besides $u_{3}\not\in\text{Span}\{ u_{1},u_{2} \}$. (This fact tell us that $\{ u_{1},u_{2},u_{3} \}$ is a linearly independent set)

Let $W=\text{Span}\{ u_{1},u_{2} \}$. By Orthogonal Decomposition Theorem, $u_{3}$ can be written uniquely as the sum of  2 orthogonal vector:

$$
u_{3}=\hat{u}_{3}+z
$$
where $\hat{u}_{3}=\text{proj}_{W}u_{3}$ and $z=u_{3}-\hat{u}_{3}$.

Thus, find $\hat{u}_{3}$

$$
\begin{align}
\hat{u}_{3}&= \frac{u_{3}\cdot u_{1}}{u_{1}\cdot u_{1}}u_{1}+ \frac{u_{3}\cdot u_{2}}{u_{2}\cdot u_{2}}u_{2} \\
&= \frac{1}{3} \begin{bmatrix}
1 \\
1 \\
1
\end{bmatrix} + \frac{1}{6} \begin{bmatrix}
1 \\
-2 \\
1
\end{bmatrix} \\
&= \begin{bmatrix}
\frac{1}{2} \\
0 \\
\frac{1}{2}
\end{bmatrix}
\end{align}
$$

Thus, 

$$
\begin{align}
z= \begin{bmatrix}
0 \\
0 \\
1
\end{bmatrix}-\begin{bmatrix}
\frac{1}{2} \\
0 \\
\frac{1}{2}
\end{bmatrix}=\begin{bmatrix}
-\frac{1}{2} \\
0 \\
\frac{1}{2}
\end{bmatrix}
\end{align}
$$

> [!remark]
> Notice that this question is the example of Gram-Schmidt process. 
> 
> Notice that $\{ u_{1},u_{2},z \}$ is an orthogonal set, thus by theorem 4 it follow that it is a linearly independent set that containing  3 vector. Thus, by The Basis Theorem, it is a basis for $\mathbb{R}^{3}.$ Since it is orthogonal set, it follow that $\{ u_{1},u_{2},z \}$ is an orthogonal basis for $\mathbb{R}^{3}$.

31)
Proof:
let $A$ be an $m\times n$ matrix. Thus $\text{Row}A\in \mathbb{R}^{n}$ and Nul $A\in \mathbb{R}^{n}$. Since 
$$
\text{Row}A\perp\text{Nul}A
$$
it follow that by Orthogonal Decomposition any $x\in \mathbb{R}^{n}$ can be written in the form of 
$$
x=p+u
$$
where $p\in\text{Row}A$ and $u\in \text{Nul}A$. 

Suppose $Ax=b$ is consistent, by first part $x$ can be written unique as

$$
x=p+u
$$
where $p\in\text{Row}A$ and $u\in \text{Nul}A$. Thus,

$$
\begin{align}
A(p+u)&=b \\
Ap+Au&=b \\
Ap&=b
\end{align}
$$
We need to show for the uniqueness of $p$. Suppose there exist another vector $p_{1}\in\text{Row}A$ such that $Ap_{1}=b$  Thus,

$$
\begin{align}
A(p-p_{1})&=b-b \\
A(p-p_{1})&=0 &&(1)
\end{align}
$$

Since $p\in\text{Row}A$ and $p_{1}\in\text{Row}A$, hence it follow that $p-p_{1}\in\text{Row}A$. From (1) we know that $p-p_{1}\in\text{Nul}A$. 

Since $\text{Row } A$ and $\text{Nul } A$ are orthogonal complements $(\text{Row } A \perp \text{Nul } A)$, the only vector they share in common is the zero vector:

$$\text{Row } A \cap \text{Nul } A = \{0\}$$
Therefore, it must be true that:

$$\begin{align}
p - p_1 = 0 \implies p = p_1 &&\blacksquare
\end{align}$$

> [!question]
> Why the Orthogonal Decomposition Theorem doesn't guarantee the uniqueness of $p$ ?
> 
> Because the Orthogonal Decomposition Theorem guarantee for each fixed $x$, there exist a unique $p$ such that $x=p+u$ but it didn't guarantee that the $p$ is unique for the solution set for $Ax=b$.(x can be infinitely many)

32)

