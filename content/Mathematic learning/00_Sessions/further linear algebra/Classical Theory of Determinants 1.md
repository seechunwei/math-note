### The Algebraic Route: Elimination

In 1683 (Japan) and 1693 (Germany), Seki Takakazu and Gottfried Wilhelm Leibniz independently discovered determinant expressions while trying to eliminate variables from systems of simultaneous linear equations.

For a system of two linear equations in two unknowns:

$$\begin{aligned} a_1 x + b_1 y &= k_1 \\ a_2 x + b_2 y &= k_2 \end{aligned}$$​​

Multiplying the first equation by b2​, the second by b1​, and subtracting eliminates y:

$$(a_1 b_2 - a_2 b_1)x = k_1 b_2 - k_2 b_1$$

The scalar quantity:

$$
\Delta = a_1 b_2 - a_2 b_1
$$

is the **eliminant** (later termed the *determinant* by Cauchy). It dictates the solvability behavior:
- If $\Delta \ne 0$, the system possesses a **unique** solution:
  $$
  x = \frac{k_1 b_2 - k_2 b_1}{a_1 b_2 - a_2 b_1}, \quad y = \frac{a_1 k_2 - a_2 k_1}{a_1 b_2 - a_2 b_1}
  $$
- If $\Delta = 0$ and the numerators are non-zero, the system is **inconsistent** (no solution).
- If $\Delta = 0$ and the numerators vanish, the system possesses **infinitely many** solutions.

Notice that the numerator of  $x$ is the $\det A_{1}(b)$ which is replacing the first column of $A$ by $b$ (the target vector) while the numerator of $y$ is $\det A_{2}(b)$. 
[[3.3 Cramer's Rule]]


