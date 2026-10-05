1)
$u=\begin{bmatrix}-1 \\ 2\end{bmatrix},v=\begin{bmatrix}2 \\ 3 \end{bmatrix},w=\begin{bmatrix}3 \\ -1 \\ -5\end{bmatrix},x=\begin{bmatrix}6 \\ -2 \\ 3\end{bmatrix}$

$$
\begin{align}
u\cdot u&=u^{T}u \\
&=\begin{bmatrix}
-1 & 2
\end{bmatrix}\begin{bmatrix}
-1 \\
2
\end{bmatrix} \\
&=5
\end{align}
$$

$$
\begin{align}
v\cdot u&=v^{T}u \\
&=\begin{bmatrix}
2 & 3
\end{bmatrix}\begin{bmatrix}
-1 \\
2
\end{bmatrix} \\
&=4
\end{align}
$$
$$
\frac{v\cdot u}{u\cdot u}=\frac{4}{5}
$$


4)

$$
\begin{align}
\frac{1}{u\cdot u}u&= \frac{1}{5}\begin{bmatrix}
-1 \\
2
\end{bmatrix} \\
&=\begin{bmatrix}
-\frac{1}{5} \\
\frac{2}{5}
\end{bmatrix}
\end{align}
$$

5)

$$
\begin{align}
v\cdot v&=v^{T}v \\
&=\begin{bmatrix}
2 & 3
\end{bmatrix}\begin{bmatrix}
2 \\
3
\end{bmatrix} \\
&=13
\end{align}
$$

Notice that $u\cdot v=v\cdot u= 4$ from question 1) (By theorem 1). Thus,

$$
\begin{align}
\left( \frac{u\cdot v}{v\cdot v} \right)v&= \left( \frac{4}{13} \right) \begin{bmatrix}
2 \\
3
\end{bmatrix} \\
&= \begin{bmatrix}
\frac{8}{13} \\
\frac{12}{13}
\end{bmatrix}
\end{align}
$$

> [!remark] 
> 
> Notice that this is $proj_{L}u$ where $L=Span\{ v \}$ which is the projection of $u$ onto the one dimensional subspace spanned by $v$.
> 
> Since $proj_{L}u\neq u$, it follow that $u \not\in Span\{ v \}$.
> 



7)

$$
\begin{align}
||w||&=\sqrt{ w\cdot w } \\
&=\sqrt{ w^{T}w } \\
&= \sqrt{ (9+1+25) } \\
&=\sqrt{ 35 }
\end{align}
$$
Remark: This is the length of $w$.

10)

Let $u=\begin{bmatrix}3 \\ 6 \\ -3\end{bmatrix}$ and $u'$ be the unit vector of $u$. Thus,

$$
\begin{align}
u'&=  \frac{u}{||u||} \\
&=\frac{u}{\sqrt{ u\cdot u }} \\
&= u \left( \frac{1}{\sqrt{ 54 }} \right) \\
&=\frac{1}{3\sqrt{ 6 }}\begin{bmatrix}
3 \\
6 \\
-3
\end{bmatrix} \\
&=\begin{bmatrix}
\frac{1}{\sqrt{ 6 }} \\
\frac{2}{\sqrt{ 6 }} \\
-\frac{1}{\sqrt{ 6 }}
\end{bmatrix}
\end{align}
$$

Verification:

$$
\begin{align}
||u'||^{2}&=u'\cdot u' \\
&=1 \\
||u||&=1
\end{align}
$$

> [!remark] 
> 
> Remark: This process is called normalizing $u$, and we say $u'$ is in the same direction as $u$.

13)
Given $x=\begin{bmatrix}10 \\ -3\end{bmatrix},y=\begin{bmatrix}-1 \\ -5\end{bmatrix}$

The distance between $x$ and $y$ denoted by $dist(x,y)$ is

$$
\begin{align}
dist(x,y)&=||x-y|| \\
&=\sqrt{ (x-y)\cdot(x-y) }
\end{align}
$$

Let's calculate $x-y$:
$$
x-y=\begin{bmatrix}
10 \\
-3
\end{bmatrix}-\begin{bmatrix}
-1 \\
-5
\end{bmatrix}=\begin{bmatrix}
11 \\
2
\end{bmatrix}
$$

Let's calculate $(x-y)\cdot(x-y)$:

$$
\begin{align}
(x-y)^{T}(x-y)&=\begin{bmatrix}
11 & 2
\end{bmatrix}\begin{bmatrix}
11 \\
2
\end{bmatrix} \\
&=125
\end{align}
$$

Thus, 
$$
dist(x,y)=\sqrt{ 125 }=5\sqrt{ 5 }
$$

> [!remark] 
> 
> Remark: Notice that the answer is same if we take $y-x$.


16)
By definition Two vectors $u$ and $v$ in $\mathbb{R}^{n}$ are orthogonal to each other iff $u\cdot v=0$

Given $x=\begin{bmatrix}4 \\ -2 \\ 5\end{bmatrix},y=\begin{bmatrix}11 \\ -1 \\ -9\end{bmatrix}$. Thus,

$$
\begin{align}
x\cdot y&=x^{T}y \\
&= \begin{bmatrix}
4 & -2 & 5
\end{bmatrix} \begin{bmatrix}
11 \\
-1 \\
-9
\end{bmatrix} \\
&=1
\end{align}
$$

Since $x\cdot y\neq 0$, thus, $x$ and $y$ is not orthogonal.

17)
Given $u=\begin{bmatrix}3 \\ 2 \\ -5 \\ 0\end{bmatrix},v=\begin{bmatrix}-4 \\ 1 \\ -2 \\ 6\end{bmatrix}$

$$
\begin{align}
u\cdot v&= u^{T}v \\
&=\begin{bmatrix}
3 & 2 & -5 & 0
\end{bmatrix}\begin{bmatrix}
-4 \\
1 \\
-2 \\
6
\end{bmatrix} \\
&=0
\end{align}
$$

Since $u\cdot v=0$, it follow that $u$ and $v$ are orthogonal.

29)

> [!theorem] 
> Let $u,v$ and $w$ be vectors in $\mathbb{R}^{n}$, and let $c$ be a scalar. Then
> 
> a. $u\cdot v=v\cdot u$
> b. $(u+v)\cdot w=u\cdot w+v\cdot w$
> c. $(cu)\cdot v=c(u\cdot v)=u\cdot(cv)$
> d. $u\cdot u\geq 0$, and $u\cdot u=0$ iff $u=0$

Proof b):

By transpose definition of inner product

$$
\begin{align}
(u+v)\cdot w&= (u+v)^{T}w \\
&=(u^{T}+v^{T})w &&(1)\\
&=u^{T}w+v^{T}w &&(2)\\
&=(u\cdot w)+(v\cdot w) && \blacksquare
\end{align}
$$

$(1)$ using the fact :$(A+B)^{T}=A^{T}+B^{T}$
$(2)$ using the fact: $C(A+B)=CA+CB$


Proof c):
$$
\begin{align}
(cu)\cdot v&= (cu)^{T}v \\
&=(cu^{T})v &&(1)\\
&=c(u^{T}v) &&(2)\\
&=c(u\cdot v)  &&\blacksquare
\end{align}
$$
(1) using the fact: $(cA)^{T}=cA^{T}$
(2) using the fact: $(cA)B=c(AB)$


31)
Given $u=\begin{bmatrix}3 \\ -4 \\ -1\end{bmatrix}, v=\begin{bmatrix}-8 \\ -7 \\ 4\end{bmatrix}$
$$
\begin{align}
u\cdot v&= u^{T}v \\
&=\begin{bmatrix}
3 & -4 & -1
\end{bmatrix} \begin{bmatrix}
-8 \\
-7 \\
4
\end{bmatrix} \\
&=0
\end{align}
$$

$$
\begin{align}
||u||^{2}&=u\cdot u \\
&=u^{T}u \\
&=\begin{bmatrix}
3 & -4 & -1
\end{bmatrix} \begin{bmatrix}
3 \\
-4 \\
-1
\end{bmatrix} \\
&=26
\end{align}
$$

$$
\begin{align}
||v||^{2}&=v\cdot v \\
&=v^{T}v \\
&=\begin{bmatrix}
-8 & -7 & 4
\end{bmatrix} \begin{bmatrix}
-8 \\
-7 \\
4
\end{bmatrix} \\
&=129
\end{align}
$$

$$
\begin{align}
||u+v||^{2}&=(u+v)\cdot(u+v) \\
&=(u+v)^{T}(u+v)
\end{align}
$$


$$
\begin{align}
u+v&=\begin{bmatrix}
3 \\
-4 \\
-1
\end{bmatrix}+\begin{bmatrix}
-8 \\
-7 \\
4
\end{bmatrix} \\
&=\begin{bmatrix}
-5 \\
-11 \\
3
\end{bmatrix}
\end{align}
$$

Thus,

$$
\begin{align}
||u+v||^{2}&= \begin{bmatrix}
-5 &  -11 & 3
\end{bmatrix} \begin{bmatrix}
-5 \\
-11 \\
3
\end{bmatrix} \\
&=155 \\
&=||u||^{2}+||v||^{2}
\end{align}
$$
32)
Given parallelogram law is
$$
||u+v||^{2}+||u-v||^{2}=2||u||^{2}+2||v||^{2}
$$

Notice that,
$$
\begin{align}
||u+v||^{2} &= (u+v)\cdot(u+v) \\
&=u\cdot(u+v)+ v\cdot(u+v) \text{ (By Theorem 1)}\\
&= ||u||^{2}+||v||^{2}+2u\cdot v
\end{align}
$$

$$
\begin{align}
||u-v||^{2} 
&=(u-v)\cdot(u-v) \\
&=u\cdot(u-v)-v\cdot(u-v) \\
&=||u||^{2}+||v||^{2}-2u\cdot v
\end{align}
$$

Thus,

$$
\begin{align}
||u+v||^{2}+||u-v||^{2}=2||u||^{2}+2||v||^{2}
\end{align}
$$



> [!remark] 
> How to understand this intuitively?
> 
> ![[Pasted image 20260701141452.png]]
> 
> Thus, By Law of Cosine
> From 1)
> $$
> ||u+v||=||u||^{2}+||v||^{2}-2||v||||u||\cos \theta
> $$
> From 2)
> 
> $$
> ||u-v||=||u||^{2}+||v||^{2}-2||v||||u||\cos(180^\circ -\theta)
> $$
> 
> Since $\cos(180^\circ-\theta)=-\cos \theta$. It follow that
> 
> $$
> ||u-v||=||u||^{2}+||v||^{2}+2||v||||u||\cos \theta
> $$
> 
> Hence,
> 
> $$
> ||u+v||+||u-v||=2||u||^{2}+2||v||^{2}
> $$
> 
>  The law states that adding the squared lengths of these two changing diagonals always yields that constant sum of the four sides. (In fact it is related to geometry)
> 

^8e9e9d

33)
The general form of $H$ is 

$$
\begin{align}
H&=\left\{ \begin{bmatrix}
x \\
y
\end{bmatrix}\in \mathbb{R}^{2}:\begin{bmatrix}
x  & y
\end{bmatrix} \begin{bmatrix}
a \\
b
\end{bmatrix} =0\right\} \\
&=\left\{ \begin{bmatrix}
x \\
y
\end{bmatrix} \in \mathbb{R}^{2}:ax+by=0\right\}
\end{align}
$$

Case 1: $v=0$
Then,

$$
v=\begin{bmatrix}
a \\
b
\end{bmatrix}=\begin{bmatrix}
0 \\
0
\end{bmatrix}
$$
This implies that $a=0$ and $b=0$. Hence, $ax=0$ for all $a \in \mathbb{R}$ and $by=0$ for all $b \in \mathbb{R}$ (By Zero Product Property).

Hence,

$$
\begin{align}
H=\left\{  \begin{bmatrix}
x \\
y
\end{bmatrix} \in \mathbb{R}^{2}\right\}
\end{align}
$$


Case 2: $v\neq 0$.
Then,
$$
\begin{align}
H=\left\{ \begin{bmatrix}
x \\
y
\end{bmatrix}:ax+by=0  \right\}
\end{align}
$$
We need to solve for the system $ax+by=0$. 

$$
\begin{align}
ax+by&=0 \\
x&=-\frac{b}{a}y \tag*{(where y is free variable)}
\end{align}
$$

Thus, the solution set is

$$
\begin{align}
\begin{bmatrix}
-\frac{b}{a}y \\
y
\end{bmatrix} 
&= y\begin{bmatrix}
-\frac{b}{a} \\
1
\end{bmatrix} \\
&= c \begin{bmatrix}
-b \\
a
\end{bmatrix} where ~c=ya
\end{align}
$$
Thus, 

$$
\begin{align}
H&=\left\{ c \begin{bmatrix}
-b \\
a
\end{bmatrix} :c \in \mathbb{R} \right\} \\
&=Span \left\{   \begin{bmatrix}
-b \\
a
\end{bmatrix}  \right\}
\end{align}
$$

> [!remark] 
> How to understand this intuitively?
> the trivial common multiple of $a$ and $b$ is $ab$, thus, let $x=-b$ and $y=a$. Then
> 
> $$
> -ab+ab=0
> $$
> 

Case 2.2: $a=0$ and $b \neq 0$ 

Since $a=0$, it follow that $ax=0$ for all $x \in \mathbb{R}$. Since, $b\neq 0$, thus 

$$0x + by = 0 \implies y = 0$$

Thus the solution set is


$$\begin{bmatrix} x \\ 0 \end{bmatrix} = x \begin{bmatrix} 1 \\ 0 \end{bmatrix}$$

Thus ,

$$
\begin{align}
H&=\left\{  d\begin{bmatrix}
1 \\
0
\end{bmatrix} :d \in \mathbb{R} \right\} \\
&=Span\left\{  \begin{bmatrix}
1 \\
0
\end{bmatrix}  \right\}
\end{align}
$$



> [!remark] 
> What is the relation between the answer for Case 2.1 and Case 2.2?
> 
> If we let $a=0$, then
> 
> $$
> \begin{align}
> H&=\left\{  c\begin{bmatrix}
> -b \\
> 0
> \end{bmatrix} : c \in \mathbb{R}\right\} \\
> &=\left\{  e\begin{bmatrix}
> 1 \\
> 0
> \end{bmatrix}: e=-bc  \right\} \\
> &= \begin{bmatrix}
> e \begin{bmatrix}
> 1 \\
> 0
> \end{bmatrix}: e \in \mathbb{R}
> \end{bmatrix}
> \end{align}
> $$
> which is the answer for Case 2.2


34)
Let $u=\begin{bmatrix}5 \\ -6 \\ 7\end{bmatrix}$. We define $W$ as

$$
\begin{align}
W&=\left\{ x= \begin{bmatrix}
x_{1} \\
x_{2} \\
x_{3}
\end{bmatrix}:x\cdot u=0  \right\} \\
&= \left\{  x=\begin{bmatrix}
x_{1} \\
x_{2} \\
x_{3}
\end{bmatrix} : 5x_{1}-6x_{2}+7x_{3}=0 \right\}
\end{align}
$$
The system $5x_{1}-6x_{2}+7x_{3}=0$ has the same solution set as 

$$
\begin{bmatrix}
5 & -6 & 7
\end{bmatrix} \begin{bmatrix}
x_{1} \\
x_{2} \\
x_{3}
\end{bmatrix}=0
$$
We can solve this system by row reduce the augmented matrix below

$$
\begin{align}
\begin{bmatrix}
5 & -6 & 7 & 0
\end{bmatrix} \xrightarrow[]{R_{1}\left( \frac{1}{5} \right)}\begin{bmatrix}
1 & -\frac{6}{5} & \frac{7}{5} & 0
\end{bmatrix}
\end{align}
$$

Notice that $x_{2},x_{3}$ are free variables.
Thus, the solution set is

$$
x=\begin{bmatrix}
\frac{6}{5}x_{2}-\frac{7}{5}x_{3} \\
x_{2} \\
x_{3}
\end{bmatrix}=x_{2}\begin{bmatrix}
\frac{6}{5} \\
1 \\
0
\end{bmatrix}+x_{3} \begin{bmatrix}
\frac{7}{5} \\
0 \\
1
\end{bmatrix}
$$
where $x_{2},x_{3}\in \mathbb{R}$.

Let $w_{1}=\begin{bmatrix} \frac{6}{5} \\ 1 \\ 0 \end{bmatrix}$ and $w_{2}=\begin{bmatrix} \frac{7}{5} \\ 0 \\ 1 \end{bmatrix}$. Thus,

$$
W=Span\{ w_{1},w_{2} \}
$$

By Theorem 1 in chapter 4, it follow that $W$ is a subspace in $\mathbb{R}^{3}$. $W$ is a 2 dimensional subspace (plane) form by $w_{1}$ and $w_{2}$ in $\mathbb{R}^{3}$.

36)
Refer 37

37)
Let $W=Span\{ v_{1},\dots,v_{p} \}$. Show that if $x$ is orthogonal to each $v_{j}$ for $1\leq j\leq p$, then $x$ is orthogonal to every vector in $W$.

Proof:
Notice that for any $w \in W$, there exist scalar $c_{1},\dots c_{p}$ such that

$$
w=c_{1}v_{1}+\dots+c_{p}v_{p}
$$

Thus,

$$
\begin{align}
x\cdot w&=x\cdot(c_{1}v_{1}+\dots+c_{p}v_{p}) \\
&=c_{1}(x\cdot v_{1})+\dots+c_{p}(x\cdot v_{P})
\end{align}
$$
Since $(x\cdot v_{i})=0$ for $1\leq i\leq p$. Thus it follow that

$$
x\cdot w=0
$$
Thus, $x$ is orthogonal to every vector $w \in W$. $\blacksquare$.
