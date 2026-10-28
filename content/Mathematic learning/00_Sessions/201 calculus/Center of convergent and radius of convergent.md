## What is a power series?
A power series is like an infinite polynomial:

$$
\sum_{n=0}^{\infty} c_{n}(x-a)^{n}=c_{0}+c_{1}(x-a)+c_{2}(x-a)^{2}+\dots
$$
Here:
$x$ is variable
$c_{n}$ are the coefficient 
$a$ is a fixed number called the center.


## Center of Convergence (a)

Suppose we want to find the value of $x$ where the power series converges.

Key property: A power series always converges at its center.
If you plug in $x=a$:
$$
(x-a)=0\implies c_{0}+c_{1}(0)+\dots=c_{0}
$$
Example:

$\sum x^{n}$: Center is $a=0$ 
$\sum(x-3)^{n}$: Center is $a=3$

## Radius of Convergence (R)

Is $x=a$ is the only possible value of $x$ to make the power series converges?

What if we move away from the center $x=a$. ($x<a$ or $x>a$).

The radius of convergence is (denoted by $R$, where $R\geq 0$ or $R=\infty$) is the maximum distance you can move away from the center while the series is still converges.

- **Inside the radius ($\lvert x-a \rvert<R$) :** The series converges (in fact, absolutely converges).
- **Outside the radius ($\lvert x-a \rvert>R$):** The series diverges.
- **At the boundary ($\lvert x-a \rvert=R$):** The test is inconclusive; each endpoint must be checked individually.

### The 3 possibilities for $R:
1. $R=0$: The series only converges at the center $x=a$
2. $0<R<\infty$: The series converges in a finite interval around $a$
3. $R=\infty$: The series converges for all real numbers $x\in(-\infty,\infty )$

## Why is it called a "Radius"

On the 1D real number line, the region of convergence is an interval:
$$
(a-R,a+R)
$$
Here $R$ refer to half of the width of interval.

However if we expand $x$ to complex numbers ($z\in \mathbb{C}$):
$$
\lvert z-a \rvert<R
$$
The equation defines the interior geometric disk of radius $R$ in the complex plane. This is where the term radius come from.

## Example

Consider the series:
$$
\sum_{i=0}^{\infty} (-4)^{i}(x-5)^{i} = \sum_{i=0}^{\infty} \big(-4(x-5)\big)^{i}
$$

### 1. Identifying the Center ($a$)
From the standard power series form $\sum c_i (x - a)^i$:
$$
\sum_{i=0}^{\infty} (-4)^i (x - 5)^i
$$
The center is directly visible as **$a = 5$**.

> **Note:** While algebraically $\big(-4(x-5)\big)^i = (-4x + 20)^i$, keeping $(x - 5)$ factored out ensures $x$ has a leading coefficient of $1$, keeping the center $a = 5$ explicit.

### 2. Finding the Radius of Convergence ($R$)
This is a geometric series $\sum r^i$ with common ratio $r = -4(x - 5)$. It converges if and only if $\lvert r \rvert < 1$:

$$
\begin{align}
\lvert -4(x - 5) \rvert &< 1 \\
\lvert -4 \rvert \cdot \lvert x - 5 \rvert &< 1 \\
4\lvert x - 5 \rvert &< 1 \\
\lvert x - 5 \rvert &< \frac{1}{4}
\end{align}
$$

Comparing this to the standard condition $\lvert x - a \rvert < R$:
- **Center:** $a = 5$
- **Radius of convergence:** $R = \frac{1}{4}$

### 3. Interval of Convergence
$$
\left(5 - \frac{1}{4}, \; 5 + \frac{1}{4}\right) = \left(\frac{19}{4}, \; \frac{21}{4}\right) = (4.75, \; 5.25)
$$

