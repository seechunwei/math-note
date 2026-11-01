### Act 1: The Practical Problem (Systems of Equations)

In real life, we want to find a solution based on given conditions. Basically, the solution is some kind of number which represents a variable in real life. Each condition that bounds the variables is actually an equation. (We restrict our scope to **linear equations**).

Thus, we have a group of equations (we call it a **system of linear equations**). At first, we use Gaussian elimination, but soon we realize that the names of the variables ($x_1, x_2, \dots$) and the way of writing equations don't matter—only the coefficients do. Thus, we just keep the numbers and arrange them according to a rectangular array, which turns out to be an **augmented matrix**. Now we can use elementary row operations to solve the system algorithmically.

From here, we study:
- **Matrix forms:** Row Echelon Form (REF) and Reduced Row Echelon Form (RREF).
- **Variables:** **Basic variables** (corresponding to pivot columns) and **free variables** (non-pivot columns, leading to infinitely many solutions).
- **System states:** **Consistent** (at least one solution exists) vs. **Inconsistent** (no solution, e.g., a row like $\begin{bmatrix}0 & \dots & 0 & b\end{bmatrix}$ with $b \neq 0$).
- **Row equivalence:** Two matrices are row equivalent if one can be transformed into the other via row operations, preserving the exact same solution set.
- The early seeds of moving from the **eliminant** to the **determinant** (explored deeply in Act 4).

---

### Act 2: The Geometric Shift (Vector Equations)

Quote from Strang: the solution actually has 2 types of pictures—one is the **row picture** and the other is the **column picture** ([[Linear algebra lec 1]]).

The **row picture** is simply plotting each equation as a line/plane in a Cartesian coordinate system, where the intersection of those lines/planes is the solution. 

But what if we see it in the **column way**? Notice that the coefficients of a variable across each equation in order can be written into an $n$-tuple object (which is called a **vector**). For example:

$$
\begin{aligned}
x + 2y &= 9 \\
2x + 3y &= 7
\end{aligned}
$$

The coefficients of $x$ form the 2-tuple vector $\begin{bmatrix}1 \\ 2\end{bmatrix}$, and for $y$ they form $\begin{bmatrix}2 \\ 3\end{bmatrix}$. Thus, the system becomes a **vector equation**:

$$
x\begin{bmatrix} 1 \\ 2 \end{bmatrix} + y\begin{bmatrix} 2 \\ 3 \end{bmatrix} = \begin{bmatrix} 9 \\ 7 \end{bmatrix}
$$

Notice that we can plot these vectors in the Cartesian plane, where the first entry is the first coordinate and the second entry is the second coordinate. We draw an arrow pointing from the origin to that coordinate to represent a vector. 

Thus, the solution $\begin{bmatrix}x \\ y\end{bmatrix}$ is the set of **weights** for a **linear combination** of the column vectors that reaches the target vector $\begin{bmatrix}9 \\ 7\end{bmatrix}$.

From this perspective, the central question shifts completely:
> **"Can I reach the target vector $\mathbf{b}$ by taking a linear combination of the column vectors?"**

We now link the geometric properties of vectors directly to the type of solution:
- **Span:** The collection of all possible linear combinations of the columns. A solution to the system exists if and only if $\mathbf{b} \in \operatorname{Span}\{\mathbf{a}_1, \dots, \mathbf{a}_n\}$.
- **Linear Independence vs. Linear Dependence (The Homogeneous Connection):**
  Testing for linear dependence means checking if you can return to the origin using non-zero weights:
  $$
  c_1 \mathbf{a}_1 + c_2 \mathbf{a}_2 + \dots + c_n \mathbf{a}_n = \mathbf{0}
  $$
  Notice that this is **literally the homogeneous equation** ($A\mathbf{x} = \mathbf{0}$)!
  - **Linearly Independent:** Only the trivial solution ($c_1 = \dots = c_n = 0$) exists. No vector is redundant; any reachable $\mathbf{b}$ has a **unique** set of weights (at most one solution).
  - **Linearly Dependent:** Non-trivial solutions exist (non-zero weights). At least one vector is **redundant** (trapped in the span of the others), introducing free variables and leading to **infinitely many solutions**.

---

### Act 3: Matrices as Actions (Matrix Equation $Ax = b$ & Transformations)

From the vector equation, we package the column vectors together into a matrix $A = \begin{bmatrix}\mathbf{a}_1 & \dots & \mathbf{a}_n\end{bmatrix}$ to define the **matrix equation**:
$$
A\mathbf{x} = \mathbf{b}
$$
This equation has the exact same solution as the vector equation and the original system of linear equations. 

From here, we:
1. **Define matrix operations:** Matrix addition, scalar multiplication, and especially **matrix multiplication** $AB$, which represents the **composition** of transformations (applying transformation $B$ first, then transformation $A$).
2. **Study solution structure:** We link the nonhomogeneous system $A\mathbf{x} = \mathbf{b}$ to the homogeneous system $A\mathbf{x} = \mathbf{0}$. The general solution has the form:
   $$
   \mathbf{x} = \mathbf{p} + \mathbf{v}_h
   $$
   where $\mathbf{p}$ is a particular solution to $A\mathbf{x} = \mathbf{b}$, and $\mathbf{v}_h$ is any solution to $A\mathbf{x} = \mathbf{0}$ (the null space). Geometrically, this means the solution set is a translated subspace!
3. **Define the matrix inverse ($A^{-1}$):** If a matrix can "scramble" space, its inverse $A^{-1}$ acts as the **"undo" button**, satisfying $A^{-1}A = I$.

#### The Conceptual Shift: Linear Transformations
We introduce the concept of a **linear transformation** $T(\mathbf{x}) = A\mathbf{x}$. 
- Instead of a static table of numbers, we view matrix $A$ as an **active function / machine** that maps an input vector from a **domain** ($\mathbb{R}^n$) to an output vector in a **codomain** ($\mathbb{R}^m$).
- The size of the matrix ($m \times n$) determines the dimensions of the domain ($n$) and codomain ($m$).
- It satisfies the fundamental linearity rules: $T(\mathbf{u} + \mathbf{v}) = T(\mathbf{u}) + T(\mathbf{v})$ and $T(c\mathbf{u}) = cT(\mathbf{u})$.

---

### Act 4: The Geometric Definition of Determinant

The determinant originally comes from the concept of an **eliminant** when it was first used algebraically to determine whether a square system is consistent or inconsistent, and whether its solution is unique.

#### Why does $\det A \neq 0 \implies A\mathbf{x} = \mathbf{b}$ have a unique solution?
Because $\det A$ has a profound geometric meaning: **it measures the factor by which the transformation scales volume (or area)**.
$$
\text{Volume}(T(S)) = |\det A| \cdot \text{Volume}(S)
$$
Specifically, $|\det A|$ is the hypervolume of the $n$-dimensional parallelepiped formed by the column vectors of $A$.

* **If $\det A \neq 0$:** The transformation preserves the full dimension of the space. No directions are flattened, so the mapping is one-to-one and onto—meaning the transformation can be fully reversed ($A^{-1}$ exists), and $A\mathbf{x} = \mathbf{b}$ has a unique solution.
* **If $\det A = 0$:** The volume collapses to zero! The matrix squashes $n$-dimensional space into a lower-dimensional flat line, plane, or point. Because dimension and information are permanently lost (flattened), you cannot reverse the transformation ($\implies$ non-invertible, no unique inverse exists).

---

### Act 5: The Grand Abstraction (General Vector Spaces)

After working through $\mathbb{R}^n$, we pause and ask a fundamental question:
> **What actually is a vector? Is it just a column of numbers $\begin{bmatrix}x_1 \\ \vdots \\ x_n\end{bmatrix}$? Or is it defined by the properties it satisfies?**

We realize that the columns and brackets were just a convenience. What truly made all our theorems work was that vectors could be **added** and **scaled**, and obeyed consistent algebraic laws (closure, commutativity, associativity, zero vector, distributive laws).

Thus, we propose the abstract concept of a **Vector Space** $V$:
- **Subspaces:** Subsets of $V$ that are themselves vector spaces (closed under addition and scalar multiplication).
- **Basis & Dimension:** A minimal set of spanning vectors that are linearly independent. The number of vectors in a basis defines the intrinsic **dimension** of the space.
- **Coordinates:** By choosing a basis $\mathcal{B}$, any abstract vector $\mathbf{v} \in V$ can be uniquely represented as a coordinate vector $[\mathbf{v}]_{\mathcal{B}} \in \mathbb{R}^n$.

#### The Realization: Sneaky Vectors Everywhere
We discover that many objects in mathematics share these exact same properties and are secretly vectors:
1. **Polynomials ($\mathbb{P}_n$):** You can add and scale polynomials; $\{1, t, t^2, \dots, t^n\}$ forms a basis!
2. **Continuous Functions ($C[a, b]$):** Functions can be added and scaled, forming an infinite-dimensional vector space.
3. **Solutions to Differential Equations:** The principle of superposition in physics ($y = c_1 y_1 + c_2 y_2$) is literally saying that the solutions form a vector space (the kernel of a linear differential operator!).
4. **Matrices themselves ($M_{m \times n}$):** Matrices can be added and scaled, forming their own vector space.

**The Ultimate Payoff:** 
*"Prove once, apply everywhere."* By abstracting vectors into vector spaces, all the machinery we built—bases, dimensions, subspaces, linear transformations, and projections—can now be used to solve calculus, differential equations, physics, and modern machine learning!

---

### Act 6: The Range and Domain as Subspaces (Null Space and Column Space)

Now that we have the formal language of **Vector Spaces, Subspaces, Bases, and Dimension**, we can revisit our matrix equation $A\mathbf{x} = \mathbf{b}$ and linear transformation $T: \mathbb{R}^n \to \mathbb{R}^m$. 

Everything from Acts 1, 2, and 3 suddenly snaps together into a unified geometric picture.

> [!tip] Why this feels "tangled and messy" (And how it actually untangles!)
> It feels familiar yet repetitive because you are revisiting the exact same arithmetic concepts from Acts 1–3, but now viewing them in their **true geometric clothing**:
> 
> | Early Course View (Acts 1–3) | Geometric Vector Space View (Act 6) |
> | :--- | :--- |
> | **All outputs of $A\mathbf{x}$** | **The Column Space $\operatorname{Col}(A)$** (Subspace of codomain $\mathbb{R}^m$) |
> | **Number of pivot columns** | **$\operatorname{dim}(\operatorname{Col} A) = \operatorname{Rank}(A)$** |
> | **Solutions to $A\mathbf{x} = \mathbf{0}$** | **The Null Space $\operatorname{Nul}(A)$** (Subspace of domain $\mathbb{R}^n$) |
> | **Number of free variables** | **$\operatorname{dim}(\operatorname{Nul} A) = \operatorname{Nullity}(A)$** |
> | **Pivots $+$ Free variables $= n$** | **The Rank-Nullity Theorem:** $\operatorname{rank}(A) + \operatorname{nullity}(A) = n$ |
> | **Solution $\mathbf{x} = \mathbf{p} + \mathbf{v}_h$** | **A translated subspace:** $\mathbf{x} \in \mathbf{p} + \operatorname{Nul}(A)$ |


#### 1. The Subspace Theorem Meets the Domain and Range
From the Subspace Theorem, we know that **the linear span of any set of vectors is automatically a subspace** (Theorem 1 in 4.1). This immediately reveals two fundamental subspaces hidden inside every matrix:

* **In the Codomain ($\mathbb{R}^m$) — The Column Space $\operatorname{Col}(A)$:**
  The range (all possible outputs $A\mathbf{x}$) is formed by linear combinations of the columns of $A$:
  $$
  \text{Range}(T) = \{ A\mathbf{x} : \mathbf{x} \in \mathbb{R}^n \} = \operatorname{Span}\{\mathbf{a}_1, \dots, \mathbf{a}_n\}
  $$
  Because it is a span, the range is guaranteed to be a **subspace of $\mathbb{R}^m$**, called the **Column Space** $\operatorname{Col}(A)$.
  * **Link to solutions:** $A\mathbf{x} = \mathbf{b}$ has a solution **if and only if** $\mathbf{b} \in \operatorname{Col}(A)$.

* **In the Domain ($\mathbb{R}^n$) — The Null Space $\operatorname{Nul}(A)$:**
  The set of all inputs that get crushed to zero ($A\mathbf{x} = \mathbf{0}$) forms the **kernel** of $T$. 
  When we solve $A\mathbf{x} = \mathbf{0}$ by row reduction, the parametric vector solution is expressed as a linear combination of vectors associated with the free variables:
  $$
  \mathbf{x} = x_{f_1}\mathbf{v}_1 + \dots + x_{f_k}\mathbf{v}_k = \operatorname{Span}\{\mathbf{v}_1, \dots, \mathbf{v}_k\}
  $$
  Because it is also a span, the solution set to the homogeneous system is guaranteed to be a **subspace of $\mathbb{R}^n$**, called the **Null Space** $\operatorname{Nul}(A)$.

---

#### 2. From Spanning Sets to Bases and Dimension
A spanning set can have redundant vectors. To describe these subspaces efficiently without waste, we prune the redundancy using the **Spanning Set Theorem** to find a **Basis** (a linearly independent spanning set):

* **Basis for $\operatorname{Col}(A)$:** 
  Only the **pivot columns of $A$** are linearly independent. The non-pivot columns are redundant combinations of earlier pivot columns.
  $$\operatorname{dim}(\operatorname{Col} A) = \text{number of pivot columns} = \operatorname{Rank}(A)$$

* **Basis for $\operatorname{Nul}(A)$:** 
  The vectors $\{\mathbf{v}_1, \dots, \mathbf{v}_k\}$ generated by the free variables in parametric vector form are automatically linearly independent (because each vector has a $1$ in the slot of its own free variable and $0$ in the others).
  $$\operatorname{dim}(\operatorname{Nul} A) = \text{number of free variables} = \operatorname{Nullity}(A)$$

---

#### 3. The Grand Synthesis: Rank-Nullity and Solution Structure
This is where the entire journey untangles:

1. **Conservation of Dimension (The Rank-Nullity Theorem):**
   Every column of matrix $A$ ($n$ columns in total) is either a **pivot column** or a **free variable column**:
   $$
   \underbrace{\operatorname{rank}(A)}_{\text{dim of Range / pivots}} + \underbrace{\operatorname{nullity}(A)}_{\text{dim of Kernel / free variables}} = n \quad (\text{dimension of Domain})
   $$
   *Dimension is conserved:* What the transformation doesn't keep in its image ($\operatorname{Col} A$), it must have crushed into its kernel ($\operatorname{Nul} A$).

2. **Unifying the Homogeneous and Nonhomogeneous Solutions:**
   In Act 3, we wrote the solution to $A\mathbf{x} = \mathbf{b}$ as $\mathbf{x} = \mathbf{p} + \mathbf{v}_h$. Now we can understand this with full geometric clarity:
   $$
   \text{Solution Set} = \mathbf{p} + \operatorname{Nul}(A)
   $$
   * The nonhomogeneous solution set is literally the **subspace $\operatorname{Nul}(A)$ translated by the particular vector $\mathbf{p}$**!
   * **If $\operatorname{nullity}(A) = 0$ (no free variables, columns independent):** $\operatorname{Nul}(A) = \{\mathbf{0}\}$, so the solution is a single unique point $\mathbf{p}$.
   * **If $\operatorname{nullity}(A) > 0$ (free variables, columns dependent):** The solution set is an entire line, plane, or $k$-dimensional hyperplane parallel to $\operatorname{Nul}(A)$, explaining why free variables create infinitely many solutions.
