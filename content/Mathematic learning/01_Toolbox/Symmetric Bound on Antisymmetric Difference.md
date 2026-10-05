# Symmetric Bound on Antisymmetric Difference (Reverse Triangle Inequality)

When an antisymmetric difference $A(x, y)$ is bounded on one side by a symmetric distance $C(x, y)$, swapping the variables automatically generates the opposite bound for free, packaging both directions into a single absolute value inequality.

---

### 1. 🏷️ Strategic Name (The Trigger)
> **"Symmetric Bound on Antisymmetric Difference"**
> *(Trigger: Whenever you face a difference of distances or norms $A(x, y) \leq C(x, y)$ where the bounding term $C(x, y)$ is symmetric under variable swapping, swap variables to capture both bounds and isolate the absolute value $|A(x, y)| \leq C(x, y)$.)*

---

### 2. 💎 Core Concept (The Alchemy Gold)

* **Input:** A one-sided inequality $A(x, y) \leq C(x, y)$, where:
  1. $C(x, y)$ is **symmetric**: $C(y, x) = C(x, y)$ (e.g. distance $|x - y|$).
  2. $A(x, y)$ is **antisymmetric**: $A(y, x) = -A(x, y)$ (e.g. difference of magnitudes $|x| - |y|$).

* **Mechanism (The Logic):**
  1. Substitute $(y, x)$ into the valid inequality:
     $$
     A(y, x) \leq C(y, x)
     $$
  2. Apply the symmetry of $C$ and antisymmetry of $A$:
     $$
     -A(x, y) \leq C(x, y)
     $$
  3. We now hold two simultaneous bounds:
     $$
     A(x, y) \leq C(x, y) \quad \text{and} \quad -A(x, y) \leq C(x, y)
     $$
  4. By the definition of absolute value (the equivalence $u \leq C \land -u \leq C \iff |u| \leq C$), both directions fold into:
     $$
     |A(x, y)| \leq C(x, y)
     $$

* **Output:** The guaranteed two-sided absolute value bound:
  $$
  |A(x, y)| \leq C(x, y)
  $$

---

### 3. 🌐 Cross-Domain Crystallization (3 Examples)

1. **1D Real Analysis (Spivak 1-12(vi) - Absolute Values on $\mathbb{R}$):**
   - *One-sided Bound:* $|x| - |y| \leq |x - y|$.
   - *Structural Symmetries:* 
     $A(x, y) = |x| - |y|$ satisfies $A(y, x) = |y| - |x| = -(|x| - |y|)$ (antisymmetric).
     $C(x, y) = |x - y|$ satisfies $C(y, x) = |y - x| = |x - y|$ (symmetric).
   - *Tool Upgrade:* Swapping $x \leftrightarrow y$ gives $|y| - |x| \leq |x - y| \implies -(|x| - |y|) \leq |x - y|$.
   - *Result:* $\big| |x| - |y| \big| \leq |x - y|$.
   - *Reference:* [[Problem Chapter 1 Basic Properties of Number]]

2. **Linear Algebra & Vector Spaces (Reverse Triangle Inequality for Norms):**
   - *Context:* In any inner product space or normed vector space $V$ (such as $\mathbb{R}^n$) with norm $\|\cdot\|$.
   - *One-sided Bound:* From the standard triangle inequality $\|\mathbf{u}\| = \|(\mathbf{u} - \mathbf{v}) + \mathbf{v}\| \leq \|\mathbf{u} - \mathbf{v}\| + \|\mathbf{v}\|$, we obtain:
     $$
     \|\mathbf{u}\| - \|\mathbf{v}\| \leq \|\mathbf{u} - \mathbf{v}\|
     $$
   - *Structural Symmetries:* The difference of lengths $A(\mathbf{u}, \mathbf{v}) = \|\mathbf{u}\| - \|\mathbf{v}\|$ is antisymmetric. The Euclidean distance between vectors $C(\mathbf{u}, \mathbf{v}) = \|\mathbf{u} - \mathbf{v}\|$ is symmetric.
   - *Tool Upgrade:* Swapping $\mathbf{u} \leftrightarrow \mathbf{v}$ yields $-(\|\mathbf{u}\| - \|\mathbf{v}\|) \leq \|\mathbf{u} - \mathbf{v}\|$.
   - *Result:* $\big| \|\mathbf{u}\| - \|\mathbf{v}\| \big| \leq \|\mathbf{u} - \mathbf{v}\|$.

3. **Metric Spaces & Topology (1-Lipschitz Continuity of Distance Functions):**
   - *Context:* Let $(X, d)$ be any metric space, and fix a base point $z \in X$. Define $f(x) = d(x, z)$.
   - *One-sided Bound:* By the metric triangle inequality $d(x, z) \leq d(x, y) + d(y, z)$, so:
     $$
     d(x, z) - d(y, z) \leq d(x, y)
     $$
   - *Structural Symmetries:* $A(x, y) = d(x, z) - d(y, z)$ is antisymmetric. The metric distance $C(x, y) = d(x, y)$ is symmetric by the metric axiom.
   - *Tool Upgrade:* Swapping $x \leftrightarrow y$ yields $-(d(x, z) - d(y, z)) \leq d(x, y)$.
   - *Result:* $|d(x, z) - d(y, z)| \leq d(x, y)$ (Guarantees that distance-to-a-point is always uniformly continuous and $1$-Lipschitz on any metric space!).

---

### 4. 🧠 Cognitive Nuances: Symmetry vs. Antisymmetry

| Behavior | Definition | Sign Effect | Canonical Example |
| :--- | :--- | :--- | :--- |
| **Symmetric (Commutative)** | $f(x, y) = f(y, x)$ | Invariant (unchanged) | Distance: $|x - y| = |y - x|$ |
| **Antisymmetric (Skew-Symmetric)** | $f(y, x) = -f(x, y)$ | Flips sign across $0$ | Difference: $y - x = -(x - y)$ |
| **Non-Commutative** | $f(x, y) \neq f(y, x)$ | Arbitrary / unrelated | Matrix product: $AB \neq BA$ |

#### Why This Matters
When an inequality pairs an antisymmetric term on the left with a symmetric term on the right:
$$
A(x, y) \leq C(x, y)
$$
You never need to repeat the work to prove the lower bound. Swapping inputs reflects $A$ across the origin while keeping $C$ firmly in place, trapping $A(x, y)$ between $-C(x, y)$ and $C(x, y)$ in a single stroke.
