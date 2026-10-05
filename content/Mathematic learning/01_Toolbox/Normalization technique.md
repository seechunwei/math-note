# Normalization (WLOG Scaling via Homogeneity)

When an expression or inequality is homogeneous (scale-invariant), the overall magnitude of the variables is an irrelevant degree of freedom. By setting a chosen norm, sum, or denominator to $1$ without loss of generality (WLOG), complex algebraic expressions collapse into clean, decoupled single-variable terms.

---

### 1. 🏷️ Strategic Name (The Trigger)
> **"Normalize Homogeneous Expressions to Unit Invariants"**  
> *(Trigger: Whenever every term on both sides of an inequality has the same degree under the scaling test $f(\lambda \mathbf{x}) = \lambda^d f(\mathbf{x})$, immediately freeze the scale by setting the most algebraically painful term—such as a denominator or cyclic sum—equal to $1$.)*

---

### 2. 💎 Core Concept (The Alchemy Gold)

* **Input:** A homogeneous inequality $L(\mathbf{x}) \leq R(\mathbf{x})$ where scaling all variables by $\lambda > 0$ multiplies both sides by the exact same power $\lambda^d$ ($\lambda$ cancels out completely).
* **Mechanism:** 
  1. **Euler Scaling Test:** Verify that the total degree of every term matches (e.g. $\frac{\lambda a}{\lambda b + \lambda c} = \lambda^0 \frac{a}{b+c}$).
  2. **WLOG Freezing:** Since any arbitrary vector $\mathbf{a}$ can be uniquely written as $\mathbf{a} = L \cdot \mathbf{x}$ where $\|\mathbf{x}\| = 1$, we legally assume WLOG that the normalizing constraint equals $1$ (e.g. $\sum x_i^2 = 1$ or $\sum a_i = 1$).
  3. **Decoupling:** Under the unit constraint, complicated multivariable denominators and roots vanish, decoupling entangled variables into isolated single-variable terms.
  4. **Trivial Closure:** Apply fundamental tools (such as $(u - v)^2 \geq 0 \implies uv \leq \frac{u^2 + v^2}{2}$ or Cauchy-Schwarz) to finish the proof in a single step.
* **Output:** The fully proven inequality restored to all arbitrary non-zero numbers by un-scaling ($\mathbf{a} = L \mathbf{x}$).

---

### 3. 🌐 Cross-Domain Crystallization (3 Examples)

1. **Real Analysis (Spivak 1-19(b) - The Cauchy-Schwarz Inequality):**
   - *Target:* $x_1 y_1 + x_2 y_2 \leq \sqrt{x_1^2 + x_2^2}\sqrt{y_1^2 + y_2^2}$.
   - *Homogeneity:* Degree $1$ in $\mathbf{x}$ and degree $1$ in $\mathbf{y}$ (total degree $2$).
   - *Normalization:* WLOG assume $x_1^2 + x_2^2 = 1$ and $y_1^2 + y_2^2 = 1$.
   - *Simplified Target:* $x_1 y_1 + x_2 y_2 \leq 1$.
   - *Resolution:* By the trivial inequality $x_i y_i \leq \frac{x_i^2 + y_i^2}{2}$, summing over $i = 1, 2$ yields:
     $$
     x_1 y_1 + x_2 y_2 \leq \frac{(x_1^2 + x_2^2) + (y_1^2 + y_2^2)}{2} = \frac{1 + 1}{2} = 1
     $$
   - *Reference:* [[Problem Chapter 1 Basic Properties of Number#^prob-1-19-b]]

2. **Olympiad Algebra (Nesbitt's Inequality - Cyclic Denominators):**
   - *Target:* $\frac{a}{b+c} + \frac{b}{c+a} + \frac{c}{a+b} \geq \frac{3}{2}$ for $a, b, c > 0$.
   - *Homogeneity:* Degree $0$ (since $\frac{\lambda a}{\lambda(b+c)} = \lambda^0$).
   - *Normalization:* Set the parent sum $a + b + c = 1$.
   - *Decoupling:* Each denominator $(b+c)$ becomes $(1-a)$, so $\frac{a}{b+c} = \frac{a}{1-a} = \frac{1}{1-a} - 1$.
   - *Resolution:* Denominators sum to $(1-a) + (1-b) + (1-c) = 3 - 1 = 2$. By Cauchy-Schwarz / AM-HM:
     $$
     \sum \frac{1}{1-a} \geq \frac{(1+1+1)^2}{2} = \frac{9}{2} \implies \frac{9}{2} - 3 = \frac{3}{2}
     $$

3. **Linear Algebra & Quantum Mechanics (Unit Vectors & Rayleigh Quotient):**
   - *Context:* Maximizing the Rayleigh quotient $R(\mathbf{x}) = \frac{\mathbf{x}^T A \mathbf{x}}{\mathbf{x}^T \mathbf{x}}$.
   - *Homogeneity:* Degree $0$ in $\mathbf{x}$ ($R(\lambda \mathbf{x}) = R(\mathbf{x})$).
   - *Normalization:* Constrain $\mathbf{x}$ to the unit sphere: $\|\mathbf{x}\|^2 = \mathbf{x}^T \mathbf{x} = 1$.
   - *Resolution:* The denominator is eliminated entirely, reducing the problem to maximizing the quadratic form $\mathbf{x}^T A \mathbf{x}$ subject to $\|\mathbf{x}\| = 1$, which directly yields the maximum eigenvalue $\lambda_{\max}$.

---

### 4. 🧠 Cognitive Nuances: The Normalization Decision Manual

#### Step 1: When Can You Normalize?
Only when the expression passes the **Euler Scaling Test**:

$$
f(\lambda x_1, \lambda x_2, \dots) = \lambda^d \cdot f(x_1, x_2, \dots)
$$

If every term scales with the exact same power $d$, the overall scale cancels out, giving you complete mathematical freedom to fix one scale degree of freedom.

#### Step 2: What Term Should You Set to 1?

| Structural Pattern | The Algebraic Pain | What to Set to $1$ | Transformation |
| :--- | :--- | :--- | :--- |
| **A. Explicit Norm / Root** | $\sqrt{x_1^2 + x_2^2}$ | Set $\mathbf{x_1^2 + x_2^2 = 1}$ | $\sqrt{1} = 1$, eliminating denominators completely. |
| **B. Cycling Split Denominators** | $(b+c), (c+a), (a+b)$ | Set parent sum $\mathbf{a + b + c = 1}$ | Turns pairs $(b+c)$ into single-variable $(1-a)$. |
| **C. Geometric Products** | $\sqrt[3]{abc}$ | Set product $\mathbf{abc = 1}$ | $\sqrt[3]{1} = 1$, turning products into constants. |

#### Step 3: Why $a + b + c = 1$ is Not the Only Choice (Freedom of Scale $S$)
Setting $a + b + c = 1$ is **not** an equation forced by the problem—it is an **active tactical weapon** chosen by the mathematician!

> [!NOTE] Precision Nuance: Expression vs. Inequality
> - **Scale-Invariant Expression:** A function or expression $f(\mathbf{x})$ is strictly scale-invariant when it is **degree $0$** ($f(\lambda \mathbf{x}) = \lambda^0 f(\mathbf{x}) = f(\mathbf{x})$), as in Nesbitt's $\sum \frac{a}{b+c}$.
> - **Homogeneous Inequality:** An inequality $L(\mathbf{x}) \le R(\mathbf{x})$ only requires **matching degree $d$** on both sides ($\lambda^d L(\mathbf{x}) \le \lambda^d R(\mathbf{x})$). The inequality relation is scale-invariant because $\lambda^d > 0$ cancels completely (or dividing yields the degree $0$ condition $\frac{L(\mathbf{x})}{R(\mathbf{x})} \le 1$). So a scale invariant inequality can always turn to a scale invariant expression

Because the inequality/expression has this scale redundancy, you could legally set any homogeneous constraint:
* $a + b + c = 3$
* $abc = 1$
* $a^2 + b^2 + c^2 = 1$
* or any positive constant $S$ you want!

We deliberately chose $a + b + c = 1$ because it specifically destroys the algebraic obstacle on the page, turning the two-variable denominator $b + c$ into the single variable $1 - a$.

#### Step 4: The "Behind-the-Scenes" Algebra (Why WLOG is 100% Airtight)
To see why setting $a + b + c = 1$ rigorously proves the theorem for all numbers:
1. Start with completely arbitrary positive numbers $A, B, C > 0$ with any random sum $S = A + B + C$.
2. Define the scaled unit variables:
   $$
   a = \frac{A}{S}, \quad b = \frac{B}{S}, \quad c = \frac{C}{S} \implies a + b + c = \frac{A+B+C}{S} = 1
   $$
3. Divide the numerator and denominator of each original fraction by $S$:
   $$
   \frac{A}{B + C} = \frac{\frac{A}{S}}{\frac{B + C}{S}} = \frac{a}{b + c} = \frac{a}{1 - a}
   $$
Because the scaling factor $S$ cancels out completely inside each fraction, the original expression in arbitrary $A, B, C$ is **identically equal** to the expression in the unit variables $a, b, c$:
$$
\frac{A}{B + C} + \frac{B}{C + A} + \frac{C}{A + B} \equiv \frac{a}{1 - a} + \frac{b}{1 - b} + \frac{c}{1 - c}
$$
Proving that the right side is $\geq \frac{3}{2}$ under $a + b + c = 1$ automatically proves it for **all** numbers $A, B, C$ in the universe without any loss of generality!


