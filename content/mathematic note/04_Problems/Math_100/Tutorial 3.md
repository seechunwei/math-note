1)
a) There exists an integer x such that x is prime and x is even.
It is true
Let x=2(witness)
- n is prime iff $\forall \text{ positive integer }r$ and s, if $n = rs$  then either r=1 and s=n or r=n and s=1
	2=1(2) , thus 2 is prime number
- n is even iff n=2k for some integer k
	2=2(1) . Since, 1 is particular integer, thus 2 is even

b) All integer x, if x is prime, then x is not a perfect square
It is true
By definition
- n is prime iff $\forall \text{ positive integer }r$ and s, if $n = rs$  then either r=1 and s=n or r=n and s=1
- x is a perfect square iff $x=k^{2}$ for particular integer k
$$
\text{n is a perfect square }\Leftrightarrow \exists k \in \mathbb{Z} \text{ such that }n =k^{2}
$$
Let x be an arbitrary prime number which denoted by $x=r\cdot s$ such that $r,s \in \mathbb{Z}^{+}$ and it follow that $r=1$ and $s=x$ or $r=x$ and $s=1$ 

Since x can be only defined as the product of 1 and itself and it follow that $1\neq x$. Thus, x is not a perfect square. Since x is an arbitrary prime number, it follow that the conclusion is true for all prime number.

c) There exists an integer x such that x is odd and x is a perfect square
It is true
Let x=9
- 9=2(4)+1, thus 9 is odd
- $9=3^{2}$ , thus 9 is a perfect square

2)
a) All band has won less than ten Grammy awards.
b) There exists a real number that are not positive not negative and not zero.
c) All odd integer is not a perfect square 
d) $\exists x \in \mathbb{R}, x>3\land x^{2} \not>9$
e) There exists an integer a, b and c such that a-b is even and b-c is even and a-c is odd.

3)
Let p denote the statement, and $\neg p$ defined by:
$$
\text{There exists a u in "Discrete Mathematics" that are uppercase. }
$$

Since there is no u in "Discrete Mathematics" , thus $\neg p$ is false.
$\neg p$ is false iff p is true. Thus the original statement is true. It is called vacuously true.

In other word, the statement p can be express as:
$$
\forall u, P(u)\to Q(u)
$$
for which P(u) is a predicate "The letter u is in "Discrete Mathematics"." and Q(u) stand for "The letter u is lowercase."

Since $P(u)$ is false, the whole statement is true regardless of the truth value of $Q(u)$.

4)
a) There exists two integer y, z such that $x+y=z$
$$
\exists y,z \text{ such that }(y,z\in \mathbb{Z}) \land x+y=z
$$


b)Yes, let P(x) denote the predicate "$x=\frac{a}{b} \text{ such that }a,b\in \mathbb{Z } \land b\neq 1\land a \not\geq x$"

It is wrong, because q is false . Since integer is a subset of real number, q is true iff P(x) is true for integer and non-integer.

if q is true then P(x) hold for all real number, since $\mathbb{Z}\subseteq \mathbb{R}$ , it means that every integer is a real number, thus P(x) is hold for all integer, so p is true.


5)
a)
Let x=-2 and y=2  $x+y=(-2)+2=0$
Let x=-1 and y=1  $x+y=(-1)+1=0$
Let x=0 and y=0  $x+y=0+0=0$

Since the predicate "$\exists y \in E\text{ such that }x+y=0$ " is true for all x in D. Thus, the statement is true.

b)
Let x=0
Suppose y=0 , $x+y=0+0=0$ Thus, $x+y=y$
Suppose y=1, $x+y=0+1=1$ Thus, $x+y=y$
Suppose y=2, $x+y=0+2=2$ Thus, $x+y=y$

Since the predicate "$\forall y \in E,x+y=y$ " is true for element x=0 in D. By existential generalization, the statement is true.

6)
a)
Fix $x$ is an arbitrary real number and let $y=x+1$
$$
x<x+1
$$
Thus, by substitution
$$
x<y
$$
Since $x$ is an arbitrary real number, it follow that the conclusion is true for all other element in the set.


b)
$$
S:\exists y \in \mathbb{R},\forall x \in \mathbb{R}\land x<yS
$$

Proof:
We prove the negation of the statement.

$\neg S$:
$$
\begin{align}
\neg(\exists y(y \in \mathbb{R}\land\forall x (x\in \mathbb{R} \to x<y)))&\equiv \forall y(\neg (y \in \mathbb{R})\lor \exists x\neg(x \in \mathbb{R}\to x<y)) \\
&\equiv \forall y \in \mathbb{R},\exists x(x \in \mathbb{R}\land x\geq y) \\
&\equiv \forall y \in \mathbb{R}, \exists x \in \mathbb{R},x\geq y
\end{align}

$$

Let y be an particular but arbitrarily chosen real number and $x=y+1$ 
Since,
$$
y+1\geq y
$$
By substitution
$$
x\geq y
$$

Since y is arbitrary, it follow that $\neg S$ hold for all element $y \in \mathbb{R}$

Since $\neg S$ is true. Thus, by definition $S$ is false.


c)
$$
\forall y \in \mathbb{R}^{+} ,\exists x \in \mathbb{R} \text{ such that }x=y
$$
Proof:
Suppose y is a particular but arbitrarily chosen positive real number. By definition y is an element in $\mathbb{R}^{+}$ which denoted by $y \in \mathbb{R}^{+}$ 


Observe that every element in $\mathbb{R}^{+}$ is in $\mathbb{R}$ . Thus, by definition $\mathbb{R}^{+}\subseteq \mathbb{R}$ . Since $y\in \mathbb{R}^{+}$ , it follow that $y\in \mathbb{R}$. Suppose an element x in $\mathbb{R}$ where $x=y$ . Then $x \in \mathbb{R}$ and $x=y$


Since, y is an arbitrary positive real number. It follow that the conclusion is true for all other element in $\mathbb{R}^{+}$

d)
$$
\exists x \in \mathbb{R} \text{ such that }\forall y \in \mathbb{R}^{-},x>y
$$
Let x=0 and suppose an arbitrary negative real number y. 
By definition, $y<0$
Since $x=0$ and $y<0$ , it follow that  $x>y$.


7)
$$\begin{align}
\neg(\forall x \in D \forall y\in E,P(x,y))&\equiv \exists x \in D, \neg(\forall y \in E,P(x,y)) \\
&\equiv \exists x \in D ,\exists y \in E,\neg P(x,y)
\end{align}
$$


8)
If it doesn't rain, then Ann will go
If Ann won't go, then it rains.

9)
a) 
It is true. 
If a is an integer, a can be express in the fraction form as $\dfrac{a}{1}$ 
Thus, $\dfrac{1}{x}$ is an integer only if $x=1$

Tutor answer: it is false because x can be -1 or 1. Why i am wrong? Because i don't know the formal property of integer:

For all integer a and b , if $a\mid b$ and $b\mid a$ , then $a=b$ or $a=-b$ . This property show that integer involve negative.
$$
\mathbb{Z}\in \{ \dots,-3,-2,-1,0,1,2,3,\dots \}
$$



b)
It is true.
Suppose x is an arbitrary real number. By additive inverse property, there exists a number $-x$ such that:
$$
x+(-x)=0
$$
c)
it is true
Suppose y is an arbitrary real number. By identity property of multiplication :
$$
y\cdot 1=y
$$
Thus, x=1

10)
Not logically equivalent means they have different truth value.

Notice that:
$$
\forall x \in D,(P(x)\to Q(x))
$$
This statement is only true when 
1) $x \in D$
2) $P(x)$
3) $Q(x)$
We can say that $P(x)\implies Q(x)$ . Thus, the truth set of $Q(x)$ is a subset of the truth set of $P(x)$ . We know that $P(x)$ and $Q(x)$ are true for $x \in D$. So we need to find
- $P(x)$ and $Q(x)$ where (both are truth for $x \in D$ or $P(x)$ is false) 
-  $Q(x) \not\implies P(x)$. 
For example,
Let D denote the set of $\mathbb{Z}$
Let P(x) denote x is even
Let Q(x) denote x is old
 
