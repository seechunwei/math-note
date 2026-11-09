
Note that the solution we obtained from non linear DE by determine if it is separable, exact or homogeneous is not the general solution of the DE even though it is in the form of a one-parameter family. 

The culprit is actually singularity (divisible by 0)

Note that for separable it is very clear that we divide $h(y)$. Hence, we lost the possibility when $h(y)=0$.

How about exactness?
Even though Zill didn't mention in the book but actually we say that $N(x,y)$ and $M(x,y)$ are differential of a function $f$ if
$$
\frac{dy}{dx}= - \frac{M(x,y)}{N(x,y)}
$$

Thus, we are finding a solution $y=\phi(x)$ for the DE where $N(x,y)=0$ is singularity.

But wait isn't it a function in 2 variable? Because the exist a function $f(x,y)$ such that the differential $\Delta f=0$ can be express as
$$
M(x,y)dx+N(x,y)dy=0
$$
Note that when we set the differential $\Delta f=0$, we are downgrading it from 3D to 2D. It means that if we know $x$ then we can deduce $y$. $\Delta f$ is not important, because it is $0$. The implicit solution we will get is
$$
f(x,y)=c
$$

How about integrating factor? For integrating factor we multiply it with
$$
\mu(x)=e^{\int P(x) \, dx }
$$
which only depend on $x$ and never = to 0.

Note that we have 2 types of singularity: **Singular Points** and **Singular Solutions**:

| Concept               | What is it?                                      | Where does it come from?                                               | What does it affect?                                                                                                                                                                                                                                                                                     |
| :-------------------- | :----------------------------------------------- | :--------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Singular Point**    | A specific $x$-value ($x = x_0$) on the $x$-axis | Dividing by the leading coefficient $a_n(x)$ to put into standard form | Restricts the **interval of definition $I$** (must exclude zeros of $a_n(x)$). See [[Mathematic learning/00_Sessions/223 Differential Equations/2.3 Linear Equations#Singular Points and Intervals of Definition\|2.3 Linear Equations]].                                                                |
| **Singular Solution** | An entire solution curve $y = \phi(x)$           | Dividing by a function of $y$ ($h(y)$ or $y^n$) during solving         | Violates the **general solution** property (the curve cannot be obtained from the parameter family for any choice of $c$). See [[Mathematic learning/00_Sessions/223 Differential Equations/Solution of an ODE#8.4 Singular Solutions (Beyond the Family)\|Solution of an ODE: 8.4 Singular Solutions]]. |

---

### Why Linear First-Order Equations Are the "One Exception"

As discussed in [[Mathematic learning/00_Sessions/223 Differential Equations/Solution of an ODE#8.5 Structural Remark: Linear vs. Nonlinear ODEs|Solution of an ODE: 8.5 Structural Remark]], linear differential equations **never possess singular solutions**:

1. **No Division by $y$ or $h(y)$:**
   By definition of linearity:
   $$a_1(x)\frac{dy}{dx} + a_0(x)y = g(x)$$
   The dependent variable $y$ appears only to the first power ($y^1$). We never divide by any function of $y$.
2. **Integrating Factor is Strictly Positive:**
   $$\mu(x) = e^{\int P(x)\,dx} > 0 \quad (\text{never } 0)$$
   When isolating $y$, we only divide by $\mu(x)$, which depends solely on $x$ and never vanishes.
3. **The Parameter Family is the General Solution:**
   Once singular points on the $x$-axis are avoided by choosing an open interval $I$ where $P(x)$ and $f(x)$ are continuous, the Existence & Uniqueness Theorem guarantees that:
   $$y(x) = \frac{1}{\mu(x)}\left[\int \mu(x)f(x)\,dx + c\right]$$
   contains **every single solution** that exists on $I$. No solutions are left out.

---

### Comparison Across Chapter 2 Methods

* **Separable Equations ([[Mathematic learning/00_Sessions/223 Differential Equations/2.2 Separable Equation|2.2 Separable Equation]]):**  
  Dividing by $h(y)$ excludes $h(y) = 0$. Constant/equilibrium solutions are lost and become singular solutions.
* **Exact Equations ([[Mathematic learning/00_Sessions/223 Differential Equations/2.4 Exact Equations|2.4 Exact Equations]]):**  
  Yields an implicit relation $f(x, y) = c$. Vertical tangents occur where $N(x, y) = \frac{\partial f}{\partial y} = 0$, breaking the single-valued function $y = \phi(x)$. Additionally, integrating factors $\mu(x, y)$ require dividing by $N$ or $M$, which can lose or introduce solutions.
* **Bernoulli / Substitutions ([[Mathematic learning/00_Sessions/223 Differential Equations/2.5 Solutions by Substitution|2.5 Solutions by Substitution]]):**  
  Dividing by $y^n$ loses the trivial solution $y \equiv 0$, which is a singular solution.
* **Linear Equations ([[Mathematic learning/00_Sessions/223 Differential Equations/2.3 Linear Equations|2.3 Linear Equations]]):**  
  Only divides by $a_1(x)$ (chops the $x$-axis into intervals), never divides by $y$. On each valid interval $I$, the 1-parameter family is the true **General Solution**.

---
# 4.1.1 Initial-Value and Boundary-Value Problems

## Existence and uniqueness

For a linear differential equation an **nth-order initial-value problem (IVP)** is

Solve:
$$
\begin{align}
a_{n}(x) \frac{d^{n}y}{dx^{n}}+\dots+a_{1}(x) \frac{dy}{dx}+a_{0}(x)y=g(x) \tag*{(1)}
\end{align}
$$
Subject to:
$$
\begin{gathered}
y(x_{0})=y_{0},  & y'(x_{0})=y_{1}\dots y^{(n-1)}(x_{0})=y_{n-1}
\end{gathered}
$$

Theorem 4.1.1 Existence of a Unique Solution
![[1.2 IVP and BHP and Existence and Uniqueness#^59ceaf]]

Why $a_{n}(x) \neq 0$?
Because from [[1.2 IVP and BHP and Existence and Uniqueness#^b070e8]] , The Existence and Uniqueness Theorem require the highest derivative $\frac{d^{n}y}{dx^{n}}$ is continuous. To isolate $\frac{d^{n}y}{dx^{n}}$, we need to divide $a_{n}(x)=0$. Hence $a_{n}(x)\neq 0$. ^3585a9
### Example 1
The IVP
$$
\begin{gathered}
3y'''+5y''-y'+7y=0, & y(1)=0, & y'(1)=0
, & y''(1)=0\end{gathered}
$$

Note that $y=0$ is the trivial solution. Since all constant coefficient is continuous everywhere and $a_{n}(x) =3\neq 0$, hence, by Theorem $y=0$ is the only solution on any interval containing $x=1$.

### Example 2
Consider the IVP
$$
\begin{gathered}
x^{2}y''-2xy'+2y=6, & y(0)=3, & y'(0)=1
\end{gathered}
$$

Note that $a_{n}(x)=x^{2}$. And when $x=0$, $a_{n}(0)=0$. Hence, the existence and uniqueness of the theorem does not guaranteed by the theorem.

---
## Boundary-Value Problem

It is a type of problem consists of solving a DE of order two or grater in which $y$ or its derivative are specified at different points. 

Solve:
$$
\begin{align}
a_{2}(x) \frac{d^{2}y}{dx^{2}}+ a_{1}(x) \frac{dy}{dx}+ a_{0}(x)y=g(x)
\end{align}
$$
Subject to (boundary conditions):
$$
\begin{gathered}
y(a)=y_{0}, & y(b)=y_{1}
\end{gathered}
$$

> [!remark]
> It doesn't matte if it is $y$ or its derivative, the important thing is the condition is about different point $a$ and $b$ in this case

### General Boundary Conditions & The 3 Classical Types

General linear boundary conditions for a 2nd-order ODE are:
$$
\begin{cases}
\alpha_1 y(a) + \beta_1 y'(a) = \gamma_1 \\
\alpha_2 y(b) + \beta_2 y'(b) = \gamma_2
\end{cases}
$$

By adjusting the coefficients $\alpha$ and $\beta$, we get the **3 classical types**:

| Type | Condition | Intuition / Physics |
| :--- | :--- | :--- |
| **1. Dirichlet** | $y(a) = y_0,\; y(b) = y_1$ ($\beta_i = 0$) | Fixed **value / position** (e.g., tied-down string ends). |
| **2. Neumann** | $y'(a) = y_0,\; y'(b) = y_1$ ($\alpha_i = 0$) | Fixed **derivative / flux** (e.g., insulated heat ends, zero heat escape). |
| **3. Robin (Mixed)** | $\alpha y + \beta y' = \gamma$ ($\alpha_i, \beta_i \neq 0$) | Combination of both (e.g., spring support, convection cooling). |

![[Pasted image 20261105180815.png]]

### Number of Solutions of a BVP

^d69b3c

Even though a DE satisfies all conditions of Theorem 4.1.1 (coefficients continuous, $a_2(x) \neq 0$), a **Boundary-Value Problem can have a unique solution, infinitely many solutions, or no solution at all**.

#### How to Determine the Solution Type

To solve a 2nd-order BVP, substitute the general solution $y(x) = c_1 y_1(x) + c_2 y_2(x) + y_p(x)$ into the boundary conditions at $x = a$ and $x = b$:

$$
\begin{pmatrix}
y_1(a) & y_2(a) \\
y_1(b) & y_2(b)
\end{pmatrix}
\begin{pmatrix}
c_1 \\
c_2
\end{pmatrix}
=
\begin{pmatrix}
y_0 - y_p(a) \\
y_1 - y_p(b)
\end{pmatrix}
\implies A_{\text{BVP}} \mathbf{c} = \mathbf{b}
$$

The number of solutions depends strictly on the determinant $\det(A_{\text{BVP}}) = y_1(a)y_2(b) - y_2(a)y_1(b)$:

```
                         Calculate det(A_BVP)
                                  │
                 ┌────────────────┴────────────────┐
                 ▼                                 ▼
         det(A_BVP) ≠ 0                    det(A_BVP) = 0
                 │                                 │
                 ▼                                 ▼
          UNIQUE SOLUTION               Check System Consistency
            (Exactly 1)                            │
                                  ┌────────────────┴────────────────┐
                                  ▼                                 ▼
                            Consistent (0 = 0)            Contradiction (0 = k)
                                  │                                 │
                                  ▼                                 ▼
                         INFINITELY MANY                       NO SOLUTION
```

1. **Unique Solution ($\det \neq 0$):** $A_{\text{BVP}}$ is invertible $\implies$ unique pair of constants $(c_1, c_2)$.
2. **Infinitely Many Solutions ($\det = 0$, consistent):** Redundant equations ($0 = 0$) $\implies$ one constant is free.
3. **No Solution ($\det = 0$, contradiction):** Equations contradict ($0 = k \neq 0$) $\implies$ no possible constants satisfy the conditions.

---

### Example: All 3 Cases on the Same DE (Zill Example 3)

Consider:
$$x'' + 16x = 0 \implies x(t) = c_1 \cos(4t) + c_2 \sin(4t)$$

* **Case 1: Unique Solution (Interval $[0, \frac{\pi}{8}]$)**
  * BC: $x(0) = 0, \; x(\frac{\pi}{8}) = 0$
  * $t = 0 \implies c_1 = 0$
  * $t = \frac{\pi}{8} \implies c_2 \sin(\frac{\pi}{2}) = c_2 = 0$
  * $\det = \cos(0)\sin(\frac{\pi}{2}) - \sin(0)\cos(\frac{\pi}{2}) = 1 \neq 0 \implies$ **Unique solution: $x(t) \equiv 0$**.

* **Case 2: Infinitely Many Solutions (Interval $[0, \frac{\pi}{2}]$)**
  * BC: $x(0) = 0, \; x(\frac{\pi}{2}) = 0$
  * $t = 0 \implies c_1 = 0$
  * $t = \frac{\pi}{2} \implies c_2 \sin(2\pi) = 0 \cdot c_2 = 0 \implies$ **$0 = 0$** (True for any $c_2 \in \mathbb{R}$!)
  * $\implies$ **Infinitely many solutions: $x(t) = c_2 \sin(4t)$**.

* **Case 3: No Solution (Interval $[0, \frac{\pi}{2}]$ with non-zero target)**
  * BC: $x(0) = 0, \; x(\frac{\pi}{2}) = 1$
  * $t = 0 \implies c_1 = 0$
  * $t = \frac{\pi}{2} \implies c_2 \sin(2\pi) = 1 \implies \mathbf{0 = 1}$ (Contradiction!)
  * $\implies$ **No solution**.

---

### Why BVP Forms a Degenerate System but IVP Does Not: The Wronskian

Both IVPs and BVPs produce a $2 \times 2$ algebraic system to find $c_1, c_2$. Why does an IVP (with continuous coefficients and $a_n(x_0) \neq 0$) always have a unique solution, while a BVP can still fail?

#### 1. The IVP System & The Wronskian
In an IVP, all conditions are specified at the **same point $x_0$**:
$$
\begin{pmatrix}
y_1(x_0) & y_2(x_0) \\
y_1'(x_0) & y_2'(x_0)
\end{pmatrix}
\begin{pmatrix}
c_1 \\
c_2
\end{pmatrix}
=
\begin{pmatrix}
y_0 \\
y_1
\end{pmatrix}
$$

The determinant of this matrix is the **Wronskian** [[Chapter 4 Higher-order DE 4.1  Preliminary theory—linear equations#^36dfab]] evaluated at $x_0$:
$$\det(A_{\text{IVP}}) = y_1(x_0)y_2'(x_0) - y_2(x_0)y_1'(x_0) = \mathbf{W(y_1, y_2)(x_0)}$$

Because $\det(A_{\text{IVP}}) = W(x_0) \neq 0$, the IVP matrix is **always invertible**.  
$\implies$ **Under the hypotheses of Theorem 4.1.1 (linear, continuous coefficients, and $x_0$ is not a singular point), an IVP ALWAYS has exactly 1 unique solution.**  
*(Recall: if the ODE is nonlinear, or if $a_n(x_0) = 0$ as in Example 2, an IVP can indeed fail to be unique!).*

#### 2. The BVP System (No Wronskian Protection)
In a BVP, conditions are evaluated at **different points $a \neq b$**:
$$
A_{\text{BVP}} = \begin{pmatrix} y_1(a) & y_2(a) \\ y_1(b) & y_2(b) \end{pmatrix}
$$
Its determinant is:
$$\det(A_{\text{BVP}}) = y_1(a)y_2(b) - y_2(a)y_1(b)$$

* **This is NOT the Wronskian!** The second row contains values at $x = b$, not derivatives at $x = a$.
* It does **not** have the protection of Abel's Theorem.
* When the interval length $(b - a)$ matches the oscillation of the solutions (e.g. standing wave nodes), this determinant **hits zero**.
* Once $\det(A_{\text{BVP}}) = 0$, uniqueness is lost, resulting in **0 or $\infty$ solutions**.

---

## 4.1.2 Homogeneous Equation

$$
\begin{align}
a_{n}(x) \frac{d^{n}y}{dx^{n}}+\dots+a_{1}(x) \frac{dy}{dx}+a_{0}(x)y=0
\end{align}
$$
is homogeneous whereas
$$
\begin{align}
a_{n}(x) \frac{d^{n}y}{dx^{n}}+\dots+a_{1}(x) \frac{dy}{dx}+a_{0}(x)y=g(x) 
\end{align}
$$
where $g(x)\neq 0$ is said to be nonhomogeneous.

We shall see that to solve a nonhomogeneous linear equation (7), we must first be able to solve the associated homogeneous equation (6).

> [!tip] Assumption from this part onward
> 1) the coefficient functions $a_{i}(x)$ and $g(x)$ is continuous on some interval
> 2)  $a_{n}(x)\neq 0$ for every $x$ in the interval. 

### Differential Operators

The symbol $D$ is called differential operator because it map a differentiable function into another function denoted by $D(y)= \frac{dy}{dx}$. For example, $D(\cos 4x)=-4 \sin 4x$. 

For higher-order derivatives can be expressed in term of $D$ in a natural manner:
$$
\frac{d}{dx}\left(  \frac{dy}{dx} \right)= \frac{d^{2}y}{dx^{2}}=D(Dy)=D^{2}y
$$
in general,
$$
\frac{d^{n}y}{dx^{n}}=D^{n}(y)
$$

In general, we define an $n-$th order differential operator or polynomial operator to be
$$
L=a_{n}(x)D^{n}+a_{n-1}(x)D^{n-1}+\dots+a_{1}(x)D+a_{0}(x)
$$

> [!tip]  Linearity of Differential Operator
> 1) $D(cf(x))=cD(f(x))$
> 2) $D(f(x)+g(x))=D(f(x))+D(g(x))$
> 
> It preserve the linear combination of 2 function:
> $$
> L(\alpha f(x)+\beta g(x))=\alpha L(f(x))+\beta L(g(x))
> $$
> 

Hence any linear differential equation can be expressed in term of $D$ alone with $g(x)$:
$$
\begin{align}
y''+5y'+6y&=5x-3 \\
D^{2}y+5Dy+6y&=5x-3 \\
(D^{2}+5D+6)y&=5x-3
\end{align}
$$

Hence, any homogeneous and non homogeneous linear DE can be express as
$$
\begin{gathered}
L(y)=0&\text{and}&L(y)=g(x)
\end{gathered}
$$
respectively.

###  Superposition Principle

> [!theorem] Theorem 4.1.2 Superposition Principle- Homogeneous Equations
> 
> Let $y_{1},y_{2},\dots,y_{k}$ be solutions of the homogeneous $n$th-order DE on an interval $I$. Then the linear combination 
> $$
> y=c_{1}y_{1}(x)+c_{2}y_{2}(x)+\dots+c_{k}y_{k}(x)
> $$
> where $c_{i},i=1,2,\dots,k$ are arbitrary constant, it is also a solution on the interval.

Proof:
We prove the case $k=2$. Suppose $y_{1}(x)$ and $y_{2}(x)$ are solution for the homogeneous equation $L(y)=0$. If we define $y=c_{1}y_{1}(x)+x_{2}y_{2}(x)$, by Linearity of $L$ we have

$$
\begin{align}
L(y)&=L(c_{1}y_{1}(x)+c_{2}y_{2}(x)) \\
&=c_{1}L(y_{1}(x))+c_{2}L(y_{2}(x)) \\
&= c_{1}0+c_{2}0 \\
&=0 \tag*{$\blacksquare$}
\end{align}
$$

> [!theorem] Corollary to the Theorem 4.1.2
> A homogeneous linear DE always possesses the trivial solution $y=0$


### Linear Dependence and Linear Independence

It is the same definition of linear independence of vector in vector space.
[[1.7 Linear Independence]]. But there is one thing that need to emphasis here which is if a set of 2 function is linearly dependent, then one function is simply constant multiple of other.

In other word, 2 set of function is linearly independent when neither function is a constant multiple of the other on interval. For example,
$$
f_{1}(x)=\mu(x)f_{2}(x)
$$
where $\mu(x)$ is not a constant function. We will use this fact in next section

#### Remark of number of solution:
An $n$-order linear homogeneous ordinary differential equation always has exactly $n$ linearly independent solutions in a fundamental set, under the existence and uniqueness assumption

Why?
$L(y)=0$ is a homogeneous equation, and  $L$ itself is a linear transformation, recalled from linear algebra, there exist a matrix $A$ such that $Ay=0$, and the solution is the nullspace which allow us to find  a basis. In perspective of linear transformation [[Linear Transformation of Abstract Vector Spaces]], $\ker(L)$ is always a subspace. This, answer the question why we only focus on homogeneous linear DE.

Why the dimension is exactly $n$? (The intuition)
For any $nth$-order DE:
For arbitrary point $x_{0}\in I$, we have initial condition:
$$
\begin{gathered}
y(x_{0})=k_{0} & y'(x_{0})=k_{1} & \dots. & y^{(n-1)}(x_{0})=k_{n-1}
\end{gathered}
$$

Hence, the vector $(k_{0},k_{1},\dots,k_{n-1})\in \mathbb{R}^{n}$. Finding the solution is same as finding the linear transformation that map $x_{0}$ to each value $k_{0},k_{1},\dots,k_{n-1}$. For instance, $T:S\to \mathbb{R}^{n}$ defined as
$$
\begin{align}
T(y)= \begin{pmatrix}
y(x_{0}) \\
y'(x_{0}) \\
\vdots  \\
y^{(n-1)}(x_{0})
\end{pmatrix} \tag*{(2)}
\end{align}
$$

where $y=\{ y_{1},y_{2},\dots,y_{n} \}$ is the set of solution for the DE.
- Surjective: By the Existence theorem, $\mathrm{Im}(T)=\mathbb{R}^{n}$ (there is a solution that maps to it)
- Injective (one-to-one): By the Uniqueness theorem, if $T(y)=0$, then $y(x)=0$ is the only solution (the kernel is trivial $\{ 0 \}$).

Because $T$ is a isomorphism, we have
$$
\dim(S)=\dim(\mathbb{R}^{n})=n
$$
Hence, the set of solution form by basis that consists $n$ vector (or function).

> [!question]
> Why we mention IVP here?
> Because the Existence and Uniqueness Theorem is the bridge of this proof. We suppose arbitrary $x_{0}$, so that it work for all value in the interval.

How the matrix representation of this linear transformation $T$ looks like?
Suppose we have a set of $n$ solutions $\{y_1, y_2, \dots, y_n\}$ and form the general linear combination:
$$
y(x) = c_1 y_1(x) + c_2 y_2(x) + \dots + c_n y_n(x)
$$
To satisfy an arbitrary initial condition vector $\mathbf{k} = (k_0, k_1, \dots, k_{n-1})^T \in \mathbb{R}^n$ at $x_0$, we evaluate $y(x)$ and its first $n-1$ derivatives at $x_0$:
$$
\begin{align}
c_1 y_1(x_0) + c_2 y_2(x_0) + \dots + c_n y_n(x_0) &= k_0 \\
c_1 y_1'(x_0) + c_2 y_2'(x_0) + \dots + c_n y_n'(x_0) &= k_1 \\
&\;\;\vdots \\
c_1 y_1^{(n-1)}(x_0) + c_2 y_2^{(n-1)}(x_0) + \dots + c_n y_n^{(n-1)}(x_0) &= k_{n-1}
\end{align}
$$

In matrix form:
$$
\begin{pmatrix}
y_1(x_0) & y_2(x_0) & \dots & y_n(x_0) \\
y_1'(x_0) & y_2'(x_0) & \dots & y_n'(x_0) \\
\vdots & \vdots & \ddots & \vdots \\
y_1^{(n-1)}(x_0) & y_2^{(n-1)}(x_0) & \dots & y_n^{(n-1)}(x_0)
\end{pmatrix}
\begin{pmatrix}
c_1 \\ c_2 \\ \vdots \\ c_n
\end{pmatrix}
=
\begin{pmatrix}
k_0 \\ k_1 \\ \vdots \\ k_{n-1}
\end{pmatrix}
$$

Notice that the columns of this coefficient matrix are precisely the image vectors $T(y_1), T(y_2), \dots, T(y_n)$:
$$
M(x_0) = \begin{pmatrix} T(y_1) & T(y_2) & \dots & T(y_n) \end{pmatrix}
$$

By the **Existence and Uniqueness Theorem**, for every initial condition vector $\mathbf{k} \in \mathbb{R}^n$, there exists a unique solution (hence a unique set of scalars $c_1, \dots, c_n$). In linear algebra, a square system $M(x_0)\mathbf{c} = \mathbf{k}$ has a unique solution for every $\mathbf{k}$ if and only if $M(x_0)$ is invertible ($\det(M(x_0)) \neq 0$).

The determinant of this matrix is precisely the **Wronskian** evaluated at $x_0$:
$$
\det(M(x_0)) = W(y_1, y_2, \dots, y_n)(x_0) \neq 0
$$
Thus, $\{y_1, \dots, y_n\}$ is a fundamental set (basis) if and only if their Wronskian does not vanish!

### Wronskian

^36dfab

Suppose each of the function $f_{1}(x),f_{2}(x),\dots f_{n}(x)$ possesses at least $n-1$ derivatives. The determinant

$$
\begin{align}
W(f_{1},f_{2},\dots,f_{n})= \begin{vmatrix}
f_{1} & f_{2} & \dots & f_{n} \\
f_{1}' & f_{2}' & \dots & f'_{n} \\
\vdots  \\
f_{1}^{n-1} & f_{2}^{n-1} & \dots & f_{n}^{n-1}
\end{vmatrix}
\end{align}
$$

where the primes denote derivatives, is called the Wronskian of the functions.

> [!theorem] Theorem 4.1.3 Criterion for Linearly Independent Solutions
> 
> Let $f_{1},\dots,f_{n}$ be $n$ solutions of the homogeneous linear nth-order DE on an interval $I$. Then the set of solution:
> 
> If $W(f_{1},f_{2},\dots,f_{n})=0$, then $\{ f_{1},f_{2},\dots,f_{n} \}$ is linearly dependent.
> If $W(f_{1},\dots,f_{n}) \neq 0$, then it is linearly independent.

To determine if the solution set for a homogeneous DE is linearly independent or not, we just need to evaluate the Wronskian (determinant) at any value of $x$ in the interval $I$.

Note that this doesn't work for general function. Precisely, for the case of linearly independent which is $W(f_{1},\dots,f_{n})\neq 0$, we only need to evaluate at one point for general function and as well as the solution for homogeneous DE.

But for the case of linearly dependent which is $W(f_{1},\dots,f_{n})= 0$, it follow that evaluating at one point only work for solution of DE but it doesn't work for general function.
What it means here is determinant=0 at some fixed point doesn't work to all the other point in an interval $I$. It might me linearly independent also for other point.

Why?
#### 1. General Functions: Isolated Root vs. Identically Zero
For general functions, the Wronskian $W(x)$ is simply another function that can have **isolated roots** (points where it touches or crosses zero) without being zero everywhere:
- **Example:** Consider $f_1(x) = x^2$ and $f_2(x) = x^3$ on $[-1, 1]$:
  $$
  W(x) = \begin{vmatrix} x^2 & x^3 \\ 2x & 3x^2 \end{vmatrix} = 3x^4 - 2x^4 = x^4
  $$
  - At $x_0 = 0$: $W(0) = 0$.
  - At $x = 1$: $W(1) = 1 \neq 0$.
  Here, $x = 0$ is merely an isolated root. The functions are clearly linearly independent on $[-1, 1]$. Evaluating only at $x_0 = 0$ does not imply dependence.
- **Even stronger caveat:** Even if $W(x) = 0$ for **all** $x \in I$, general functions can still be linearly independent (e.g., $f_1(x) = x^2$ and $f_2(x) = x|x|$ on $(-1, 1)$, where $W(x) \equiv 0$, yet they are linearly independent).

#### 2. ODE Solutions: Abel's Identity (All-or-Nothing)
Why cannot the Wronskian of solutions to a linear homogeneous ODE have an isolated zero like $x^4$?

Because solutions to $y^{(n)} + P_{n-1}(x)y^{(n-1)} + \dots + P_0(x)y = 0$ are constrained by the differential equation. Differentiating their Wronskian yields **Abel's differential equation**:
$$
W'(x) = -P_{n-1}(x)W(x)
$$
Solving this separable first-order ODE gives **Abel's Identity**:
$$
W(x) = W(x_{0}) \exp\left(-\int_{x_{0}}^{x} P_{n-1}(t)\,dt\right)
$$
Since the exponential factor $\exp(\dots)$ is **strictly positive (never zero)**:
- If $W(x_{0}) = 0 \implies W(x) = 0 \cdot (\text{positive}) = 0$ for **all** $x \in I$.
- If $W(x_{0}) \neq 0 \implies W(x) = (\text{non-zero}) \cdot (\text{positive}) \neq 0$ for **all** $x \in I$.

Therefore, for ODE solutions, the Wronskian **never crosses or touches zero** unless it is identically zero everywhere.

#### 3. Why $W(x_0) \neq 0$ at One Point Proves Linear Independence for Both
Linear dependence is a strict global requirement: there must exist constants $c_1, \dots, c_n$ (not all zero) such that
$$
c_1 f_1(x) + \dots + c_n f_n(x) = 0 \quad \text{for all } x \in I
$$
If this relation holds globally, it must hold along with its first $n-1$ derivatives at any chosen point $x_0$, yielding the matrix equation $[W(x_0)]\mathbf{c} = \mathbf{0}$.
- If $W(x_0) \neq 0$, the matrix at $x_0$ is invertible, forcing $\mathbf{c} = \mathbf{0}$.
- This contradicts the existence of non-trivial constants. Hence, finding **just one point** where $W(x_0) \neq 0$ conclusively proves linear independence for *both* general functions and ODE solutions.

#### Summary Comparison

| Condition at $x_0 \in I$ | ODE Solutions on $I$ | General Differentiable Functions on $I$ |
| :--- | :--- | :--- |
| **$W(x_0) \neq 0$ at some point** | **Linearly Independent** ($W \neq 0$ everywhere) | **Linearly Independent** (even if $W=0$ elsewhere) |
| **$W(x_0) = 0$ at some point** | **Linearly Dependent** (forces $W \equiv 0$ everywhere) | **Inconclusive** (might just be an isolated root) |
| **$W(x) = 0$ for all $x \in I$** | **Linearly Dependent** | **Inconclusive** (can still be linearly independent) |

> [!tdefinition] Fundamental Set of Solutions
> Any set $y_{1},y_{2},\dots,y_{n}$ of $n$ linearly independent solutions of the homogeneous linear nth-order DE on an interval $I$ is fundamental set of solution on the interval.
> 

It is the basis for the kernel $T$ where $T$ is defined as (2).

> [!theorem] Theorem 4.1.4 Existence of a Fundamental Set
> There exists a fundamental set of solutions for the homogeneous linear nth-order differential equation (6) on an interval $I$.

This is the natural result from [[Chapter 4 Higher-order DE 4.1  Preliminary theory—linear equations#^d69b3c]], $\ker(T)$ is a n dimensional vector space, hence its basis must contain $n$ element.

> [!theorem] Theorem 4.1.5 General Solution- Homogeneous Equations
> Let $y_{1},y_{2},\dots,y_{n}$ be a fundamental set of solutions of the homogeneous linear $n$th-order DE on an interval $I$. Then the general solution of the equation on the interval is
> $$
> y=c_{1}y_{1}(x)+c_{2}y_{2}(x)+\dots+c_{n}y_{n}(x)
> $$
> where $c_{i},i=1,2,\dots,n$ are arbitrary constants.

Proof:
Let $Y$ be a solution and let $y_{1}$ and $y_{2}$ be linearly independent ^710293