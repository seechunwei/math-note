# The Critical Point Partitioning Principle

---

### 1. 🏷️ Strategic Name (The Trigger)
> **Trigger Condition:** There exist transition points (roots $g(x) = 0$, derivative zeroes $f'(x) = 0$, or piecewise boundary centers) that split the real line into several intervals, and each interval has the **structural invariant property** (constant formula, sign, or monotonicity).
> *(Trigger: Whenever an expression contains two or more points where internal signs, piecewise rules, or derivative directions change behavior—slice the domain into invariant intervals at those critical boundaries.)*

---

### 2. 💎 Core Concept (The Alchemy Gold)

* **Input:** An equation, inequality, or function consisting of component factors ($g_i(x)$), absolute values ($|x - c_i|$), or derivatives ($f'(x)$) that cannot be solved globally because the mathematical behavior flips at different locations on the number line.

* **Logic (Mechanism):**
  * **Step 1 (Find Boundaries / Critical Points):** Set each component function, factor, or absolute value argument to its transition boundary (usually $0$, or where undefined) to extract critical points $c_1 < c_2 < \dots < c_k$.
  * **Step 2 (The Structural Invariance Rule):** Prove that within each open interval $(c_k, c_{k+1})$, the behavior is **structurally invariant** (by Intermediate Value Theorem / Order Axioms, an expression cannot flip signs or change formulas without hitting a transition boundary).
  * **Step 3 (Local Evaluation & Union):** Evaluate or solve the simplified local algebraic expressions in each interval, and combine the valid solutions using **"or" / union ($\cup$) logic**.

* **Output:** Converts a complex global non-linear, multi-root, or piecewise problem into a finite set of simple local linear/monotonic problems, combined via union ($\cup$).

---

### 3. 🌐 Cross-Domain Crystallization (3 Examples)

1. **Algebra (Polynomial & Rational Inequalities from Problem 4ix):**
   - *Expression:* $(x - \pi)(x + 5)(x - 3) > 0$.
   - *Boundaries:* Setting factors to zero yields $x = -5, 3, \pi$.
   - *Partitioning:* Slices $\mathbb{R}$ into 4 invariant intervals: $(-\infty, -5), (-5, 3), (3, \pi), (\pi, \infty)$.
   - *Structural Invariant:* **Sign Invariance** (each factor is purely positive or negative throughout).
   - *Solution:* Testing arbitrary elements in each invariant interval yields $x \in (-5, 3) \cup (3, \pi)$.
   - *Reference:* [[Problem Chapter 1 Basic Properties of Number#^a1970c]]

2. **Analysis (Piecewise Absolute Value Inequalities from Problem 11iv):**
   - *Expression:* $|x - 1| + |x - 2| > 1$.
   - *Boundaries:* Setting $|x - 1| = 0 \implies x = 1$ and $|x - 2| = 0 \implies x = 2$.
   - *Partitioning:* Slices $\mathbb{R}$ into 3 intervals:
     - $x < 1 \implies 3 - 2x > 1 \implies x < 1$ (All $x < 1$).
     - $1 \le x \le 2 \implies 1 > 1$ (No solution).
     - $x > 2 \implies 2x - 3 > 1 \implies x > 2$ (All $x > 2$).
   - *Structural Invariant:* **Formula Invariance** (absolute values lock into exact linear polynomials $3-2x, 1, 2x-3$).
   - *Solution:* $x \in (-\infty, 1) \cup (2, \infty)$.

3. **Calculus (Curve Sketching & Monotonicity via First Derivative):**
   - *Expression:* Finding where a function $f(x)$ is increasing or decreasing.
   - *Boundaries:* Setting $f'(x) = 0$ or undefined identifies critical points.
   - *Partitioning:* Critical points slice the domain into intervals where $f'(x)$ maintains a constant sign.
   - *Structural Invariant:* **Direction Invariance** ($f'(x) > 0 \implies$ strictly increasing, $f'(x) < 0 \implies$ strictly decreasing).

---

### 4. 🧠 The Spectrum of Invariant Properties
* **Formula Invariance:** Absolute values $|x - c|$ lock into exact linear expressions ($+(x-c)$ or $-(x-c)$).
* **Sign Invariance:** Continuous factors $g(x)$ maintain a single sign ($> 0$ or $< 0$).
* **Direction Invariance:** Derivatives $f'(x)$ lock into a single monotonic direction ($\uparrow$ or $\downarrow$).
* **Curvature Invariance:** Second derivatives $f''(x)$ lock into purely concave up or concave down.

---

### 5. 🧠 Quick Diagnostic: Global vs. Partitioned Solving
* **Can be solved Globally:** Monotonic functions ($x^3 = 8, x + 3^x = 4$) or global invariants ($x^2 + 1 > 0$, $|a+b| \le |a| + |b|$).
* **Must be Partitioned:** Multiple root crossings ($\prod (x - r_i)$), competing absolute values ($\sum |x - c_i|$), or derivative sign changes where behavior flips at different locations.


