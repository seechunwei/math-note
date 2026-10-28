## Complex number
Complex number are invented so that we can take square root of negative number.

> [!definition] 1.1 Complex numbers
> A complex number is an ordered pair $(a,b)$ where $a,b\in \mathbb{R}$, but we will write it as $a+bi$.
> 
> The set of all complex numbers is denoted by $\mathbb{C}$:
> $$
> \mathbb{C}=\{ a+bi|a,b\in \mathbb{R} \}
> $$
> Addition and multiplication are defined by
> $$
> \begin{align}
> (a+bi)+(c+di)&=(a+c)+(c+d)i \\
> (a+bi)(c+di)&=(ac-bd)+(ad+bc)i &&(1)
> \end{align}
> $$
> 

(1).The $ac$ and $(bi)(di)=-bd$ are the real part while $(aci+bci)$ is the imaginary part.

If the imaginary part is $0$ like $a+0i$, then it is a real number $a$. Thus, $\mathbb{R}\subseteq \mathbb{C}$.

> [!theorem] 1.3 Properties of complex arithmetic 
> - commutativity
> - associativity
> - identity (additive and multiplicative)
> - inverse (additive and multiplicative)
> - distributive property

^3dd2b8

Note that addition and multiplication we defined earlier can be shown by using 1.3 properties:

Addition:
$$
\begin{align}
(a+bi)+(c+di)&=  a+bi+c+di &&\text{(Associativity)}
 \\ 
 &= a+c+bi+di&&\text{(Commutativity)} \\
 &=(a+c)+(bi+di)&&\text{(Associativity)} \\
 &=(a+c)+(b+d)i&&(\text{Distributive})
\end{align}
$$

Multiplication:
$$
\begin{align}
(a+bi)(c+di)&=a(c+di)+bi(c+di) \\
&=ac+adi+bci-bd \\
&=(ac-bd)+(ad+bc)i
\end{align}
$$

We can define subtraction and division by inverse of complex numbers.

---
## List and length

> [!definition] Definition: List, length
> - Suppose $n$ is a nonnegative numbers. A list of length $n$ is a collection of ordered $n$ elements. 
> - Two lists are equal in the sense of they have same length and same element in same order.

Thus, a list of length two is an ordered pair denoted by $(a,b)$.
It can also be called n-tuple.

A list of length 0 look like $()$ for convenience. (The spanning set theorem and $Span(\emptyset)=\{ 0 \}$)

What is the difference of set and list?
[[Chapter 1-Speaking mathematically#^6f10f7]]. For list, the ordered ant number of element is important even though it is repeated. (it represent the dimension)

> [!definition] $F^{n}$, coordinate
> $F^{n}$ is the set of all lists of length $n$ of elements of $F$:
> 
> $$
> F^{n}=\{ (x_{1},\dots,x_{n}):x_{k}\in F\text{ for }k=1,\dots,n \}
> $$
> We say that $x_{k}$ is the $k^{th}$ coordinate of $(x_{1},\dots,x_{n})$

> [!definition] Addition in $F^{n}$
> Addition in $F^{n}$ is defined by adding corresponding coordinates
> $$
> (x_{1},\dots,x_{n})+(y_{1},\dots,y_{n})=(x_{1}+y_{1},\dots,x_{n}+y_{n})
> $$
> 

We usually use a letter like $x$ or $y$ to represent the list of $n$ number. And the subscript is being used to denote the corresponding coordinate.

If $0\in F^{n}$, then we usually means the list contain 0 as each coordinate: $0=(0,\dots,0)$. Thus $x+0=0$ in $F^{n}$.

> [!theorem] Commutativity of addition in $F^{n}$. 
> If $x,y\in F^{n}$, then $x+y=y+x$

Prove using properties of real number and definition above.


---
## Vector

We can use a point or arrow (vector) to represent $n-tuple$, but we usually only use $F^{2}$ as example. The position of a vector is not important, we can move an arrow parallel to itself (not changing length or direction) and still think they are same vector.

![[Pasted image 20261023153646.png]]

> [!remark]
> Consider an affine line
> $L_{0}=\{ av:a\in \mathbb{R} \}$ a line pass though the origin
> $L=\{ av+c:a\in \mathbb{R} \}$ is a parallel line shifted by $c$


Whenever we use pictures in $\mathbb{R}^{2}$ or use the somewhat vague language of points and vectors, remember that these are just aids to our understanding, not substitutes for the actual mathematics that we will develop.

How to connect it with addition of vector?
Recall that sum of 2 element of $F^{n}$ obtained by adding corresponding coordinates. 

It is simply a vector add at the end point of another vector. So the new vector connect initial point and endpoint of 2 vector.

It is clear that the additive inverse is the vector with same length but opposite direction.

> [!remark]
> The length of list and the length of vector is different thing.
> The length of vector is the norm of a vector $\lVert v \rVert=\sqrt{ v\cdot v }$
> And the direction is determine by the unit vector $\frac{v}{\lVert v \rVert}$
> A vector is identify by its displacement (ending point - starting point)

Scalar multiplication basically can be view as stretching or shrinking a vector by a number.   

---
## Fields
A fields is a set containing at least 2 distinct element called $0$ and 1, along with operation of addition and multiplication satisfying all properties listed in [[LADR Chapter 1#^3dd2b8]]

Thus, $\mathbb{R}$ and $\mathbb{C}$ are field as well as rational number. 

---

Exercise
1) Show that $\alpha+\beta=\beta+\alpha$

