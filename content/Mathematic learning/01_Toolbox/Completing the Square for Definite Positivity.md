# 🧰 Completing the Square for Definite Positivity

> [!ABSTRACT] Teleological Core (The Black Box)
> - **Input / Trigger:** A quadratic expression with no real roots ($\Delta = b^2 - 4ac < 0$) where factoring into linear factors over $\mathbb{R}$ fails, or when you need to prove an expression is strictly positive for all $x$.
> - **Invariant Logic (Sum of Squares):** Decompose the quadratic into an isolated squared term plus a positive residue:
> 
>   $$
>   ax^2 + bx + c = a\left(x + \frac{b}{2a}\right)^2 + \frac{4ac - b^2}{4a}
>   $$
> 
>   Since $u^2 \ge 0$ for all real $u$, the squared term cannot pull the expression below its positive constant floor $k > 0$.
> - **Output:** An unconditional positive lower bound ($\min = k > 0$) proving $Q(x) > 0$ for all $x \in \mathbb{R}$.

---

## 🏛️ 3 Diverse Manifestations

### Example 1: Univariate Real Inequality (Foundations)
* **Goal:** Prove $x^2 - 2x + 2 > 0$ for all $x \in \mathbb{R}$.
* **Mechanism:**
  
  $$
  x^2 - 2x + 2 = (x - 1)^2 + 1 \ge 0 + 1 = 1 > 0
  $$

* **Reference:** [[Problem Chapter 1 Basic Properties of Number#^7861ef]]

### Example 2: Bivariate Homogeneous Positivity (Multivariate SOS)
* **Goal:** Prove $x^2 + xy + y^2 > 0$ for all $(x, y) \neq (0, 0)$.
* **Mechanism:** Treat $x$ as the variable and complete the square with respect to $y$:
  
  $$
  x^2 + xy + y^2 = \left(x + \frac{y}{2}\right)^2 + \frac{3}{4}y^2
  $$

  Since both terms are non-negative squares and cannot simultaneously vanish unless $x = y = 0$, the sum is strictly positive for all non-zero pairs.

### Example 3: Calculus Denominator Non-Vanishing (Integration / Limits)
* **Goal:** Evaluate $\int \frac{1}{x^2 + 2x + 5} \, dx$ or prove the rational function is smooth everywhere on $\mathbb{R}$.
* **Mechanism:**
  
  $$
  x^2 + 2x + 5 = (x + 1)^2 + 4 \ge 4 > 0
  $$

  This guarantees the denominator never vanishes on $\mathbb{R}$, eliminating singularities and converting directly into the standard arctan form:
  
  $$
  \int \frac{1}{(x+1)^2 + 2^2} \, dx = \frac{1}{2}\arctan\left(\frac{x+1}{2}\right) + C
  $$
