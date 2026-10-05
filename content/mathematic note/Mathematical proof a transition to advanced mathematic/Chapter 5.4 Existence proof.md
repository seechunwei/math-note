There exist irrational numbers a and b such that ab is rational.

Since we know $\sqrt{ 2 }$ is irrational . Lets consider $\sqrt{ 2 }^{\sqrt{ 2 }}$.

Case 1: $\sqrt{ 2 }^{\sqrt{ 2 }}$ is rational
Then we are done by taking $a=\sqrt{ 2 }$ and $b=\sqrt{ 2 }$.

Case 2: $\sqrt{ 2 }^{\sqrt{ 2 }}$ is irrational
Let $a=\sqrt{ 2 }^{\sqrt{ 2 }}$ and $b=\sqrt{ 2 }$. Thus 
$$
ab=\sqrt{ 2 }^{\sqrt{ 2 }\cdot \sqrt{ 2 }}=\sqrt{ 2}^{2}=2
$$
Q.E.D.

## The intermediate Value Theorem of Calculus

if $f$ is a function that is continuous on the closed interval $[a,b]$ and $k$ is a number between $f(a)$ and $f(b)$, then there exists a number $c \in(a,b)$ such that $f(c)=k$.

Prove that the equation $x^{5}+2x-5=0$ has a real number solution between $x=1$ and $x=2$.

Proof:
Let $f(x)=x^{5}+2x-5$. Notice that $f$ is continuous function on the set of real number. Thus, $f(1)=-2$ and $f(2)=31$. Since $f(1)<0<f(2)$, by the Intermediate Value Theorem of Calculus that there is a $c \in \mathbb{R}$ such that $f(c)=0$. Thus, c is the solution.

### Proof of uniqueness
An element belonging to some prescribed set A and possessing a certain property P is unique if it is the only element of A having property P.

We prove using two way
1) We assume there is 2 element in the set that possessing the property, and we show that $a=b$ (Direct proof)
2) We assume there are 2 distinct element in the set that possessing the property, and we show that $a=b$ (Proof by contradiction)

