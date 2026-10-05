1)
a)
Let $f:Z\to X$  defined as $f(z)=x$ for all $z \in Z$ such that $z=x$ 

b)
Let $g:X\to Z$ defined as $g(n)\equiv n$ (mod 2)
Or 
$$
g(n)=\begin{cases}
 1 \text{ if n is odd}\\
2 \text{ if n is even}
\end{cases}
$$

c)
No because Since $|X|=|Y|$ and f is one-to-one, it follow that h must be onto.

2)
a)
Proof:
Suppose $a$ and $b$ are arbitrary real number and $a,b \neq 0$ such that $f(a)=f(b)$. we need to show that $a=b$ .

Thus,
$$
\begin{align}
\frac{3a-1}{a}&=\frac{3b-1}{b} \\
3ba-b&=3ba-a \\
-b&=-a \\
a&=b
\end{align}
$$

Therefore, $f$ is one-to-one.

b)
Proof:
Suppose $a$ and $b$ are arbitrary real number for which $a,b\geq 2$ such that $f(a)=f(b)$. We need to prove $a=b$
Thus,
$$
\begin{align}
1+\sqrt{ a-2 }&=1+\sqrt{ b-2 } \\
\sqrt{ a-2 }&=\sqrt{ b-2 } \\
a-2 &=b-2 \\
a & =b
\end{align}
$$
Therefore, $f$ is one-to-one

How about $x^{2}$?

c)
Note:
Suppose $a$ and $b$ are arbitrary real number such that $f(a)=f(b)$. Thus,

$$
\begin{align}
\frac{a}{a^{2}+1}&=\frac{b}{b^{2}+1} \\
ab^{2}+a&=ba^{2}+b \\
ab^{2}-b&=ba^{2}-a \\
b(ab-1)&=a(ab-1) \\
(b-a)(ab-1)&=0
\end{align}
$$
Thus, $b=a$ or $ab=1$. Notice that we can form a counterexample that in the form of $ab=1$. Let $a=\frac{1}{2}$ and $b=2$. $f(2)=\frac{2}{5}=f\left( \frac{1}{2} \right)$ and $2 \neq \frac{1}{2}$. Thus, $f$ is not one-to-one.




3)
No because $\frac{1}{2}=\frac{2}{4}$  but $f\left( \frac{1}{2} \right)=-1$ and $f\left( \frac{2}{4} \right)=-2$ .

4)
a)
$f(2)=\{ 2 \}$
$f(24)=\{ 2,3 \}$
$f(27)=\{ 3 \}$
$f(30)=\{ 2,3,5 \}$

b) Yes, it is because by Fundamental Theorem of Arithmetic, For every integer $n$ for which $n> 1$ , there exists distinct prime number $p$ and positive integer $f$such that $n =p_{1}^{f_{1}}\cdot\dots p_{e_{k}}^{f_{k}}$ .

5)
Proof:
Suppose $c,x,y$ are arbitrary real number and $c \neq 0$ . We need to show that for every $y$, there exist an element $x \in \mathbb{R}$ such that $(c\circ f)(x)=y$. 

Notice that $(c\circ f)(x)$ is a composite function which can be decomposed as $c:\mathbb{R}\to \mathbb{R}$
$c(n)=cn$ for all $n \in \mathbb{R}$ and $f:\mathbb{R}\to \mathbb{R}$. 

Let $z=c(n)$
Take $n=\frac{1}{c}z$  and $z \in \mathbb{R}$. Thus,
$$
\begin{align}
c(n)&=c \cdot \frac{1}{c}(z) \\
&=z
\end{align}
$$

Thus, it follow that $c$ is onto. Since $f$ and $c$ is onto, it follow that $cf$ is onto.

6)
Proof:
Part 1
Wee need to prove If $f$ is onto, then $rng(f)=Y$.  Suppose $f$ is onto and $y$ is an arbitrary element in $Y$, it follow that $y=f(x)$ for some $x \in X$. Thus, it follow that $y \in rng(f)$. Therefore, $Y \subseteq rng(f)$. Conversely, by definition it is clear that $rng(f)\subseteq Y$. Thus, $rng(f)=Y$.

Part 2
We need to prove if $rng(f)=Y$, then $f$ is onto. Suppose $rng(f)=Y$ and $y$ is an arbitrary element in $Y$. It follow that $y \in rng(f)$. Thus, by definition $y=f(x)$ for some $x \in X$. Since $y \in Y$, it follow that $f$ is onto.

7)
Proof:
Suppose $f:X\to Y$ is a one-to-one and onto function and its inverse function $f^{-1}:Y\to X$. 

Part 1: one-to-one
Suppose $y_{1}$ and $y_{2}$ are arbitrary element in $Y$ such that $f^{-1}(y_{1})=f^{-1}(y_{2})$ and suppose $x_{1}$ and $x_{2}$ are arbitrary element in $X$. Since $f$ is a function, if $x_{1}=x_{2}$, then $f(x_{1})=f(x_{2})$. It follow that, $y_{1}=y_{2}$. Therefore, $f^{-1}$ is one=to=one.

Part 2: Onto
Suppose $x$ is an arbitrary element in $X$. We know $f: X \to Y$ is a function. By the definition of a function, for every $x \in X$, there exists some $y \in Y$ such that $f(x) = y$. Thus, it follow that $x=f^{-1}(y)$ for some $y \in Y$. Therefore, $f^{-1}$ is onto.

8)
Proof:
Suppose $B$ is an arbitrary subset in $Y$. $f^{-1}[B]=\{ x \in X \mid f(x) \in B  \text{ for some }x \in X\}$.

Since $f$ is onto, it follow that $B \subseteq rng(f)$. Suppose $y$ is an arbitrary element in $B$. Thus, the preimage of $y$ is $x \in X$ such that $f(x)=y$. Thus, $x \in f^{-1}[B]$ . It follow that $f(x) \in f[f^{-1}[B]]$. Since $f(x) = y$, it follows that $y \in f(f^{-1}[B])$. Thus, $B\subseteq f[f^{-1}[B]]$


What if $f$ is not onto? Can you find a counter example?
$B\cap rng(f)=\emptyset$
Thus, $f^{-1}[B]=\emptyset$. It follow that $f(f^{-1}[B])=\emptyset$. Thus, if $B$ is nonempty subset in $Y$ $B\not\subseteq f(f^{-1}[B])$ 


The backward inclusion is always true, regardless of whether f is surjective or not. Can you prove this?
For all subset $B\subseteq Y, f[f^{-1}[B]]\subseteq B$.

Proof:
Suppose $B$ is an arbitrary subset in $Y$. $f^{-1}[B]=\{ x \in X \mid f(x) \in B  \text{ for some }x \in X\}$. 

Case 1:
$B\cap rng(f)=\emptyset$
Thus, $f^{-1}[B]=\emptyset$. It follow that $f[f^{-1}[B]]=\emptyset$.  Thus, it follow that $f[f^{-1}[B]]\subseteq B$.

Case 2: $B\cap rng(f)$ is non-empty set
Suppose $y$ is an arbitrary element in $f[f^{-1}[B]]$. Thus, it follow that there exist $x \in f^{-1}[B]$ such that $y=f(x)$. Thus, it follow that $y \in B$.  Thus, $f[f^{-1}[B]]\subseteq B$

Thus, it follow that the preimage of y is $x \in X$ such that $f(x)=y$. Thus, $x \in f^{-1}[B]$ . It follow that $f(x) \in f[f^{-1}[B]]$. Since $f(x) = y$, it follows that $y \in f(f^{-1}[B])$. Thus, $B\subseteq f[f^{-1}[B]]$



9)
Proof:
Suppose $A$ and $B$ are arbitrary subset of $X$ and suppose $y$ is an arbitrary element in $f[A]\cap f[B]$. It follow that $y \in f[A]$ and $y \in f[B]$. By definition $f[A]=\{ y \in Y \mid y=f(x) \text{ for some }x \in A\}$ and $f[B]=\{ y \in Y \mid y=f(x_{1}) \text{ for some }x_{1} \in B \}$. Since $f(x)=f(x_{1})$ and $f$ is one-to-one, it follow that $x=x_{1}$. Thus, it follow that $x \in A\cap B$. Since $y=f(x)$ , it follow that $y \in f[A\cap B]$. Thus, $f[A]\cap f[B]\subseteq f[A\cap B]$.

The backward inclusion is always true, regardless of whether f is injective or not. Can you prove this?

For all subsets $A$ and $B$ of $X$, $f[A\cap B]\subseteq f[A]\cap f[B]$.

Proof:
Suppose $y$ is an arbitrary element in $f[A\cap B]$. Thus, there exist an $x \in A\cap B$ such that $f(x)=y$. Thus, $x \in A$ and $x \in B$. Since $f(x)=y$ , it follow that $y \in f[A]\cap f[B]$. Thus, $f[A\cap B]\subseteq f[A]\cap f[B]$.
