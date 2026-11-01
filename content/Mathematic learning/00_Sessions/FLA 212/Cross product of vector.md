While dot product is a function that map 2 vector to a real number, the cross product $u\times v$ map 2 vector in $\mathbb{R}^{3}$ to a new vector.

The property of the new vector
1) Direction: It points strictly perpendicular (orthogonal) to both $u$ and $v$, following the Right-Hand Rule (it is the orthogonal line when we project a vector to another vector, this is why we will use $\sin$ rather than $\cos$)
2) Magnitude: Its length equals the area of the parallelogram formed by $u$ and $v$. 

                 u x v  (Perpendicular to the entire plane)
                   ^
                   |
                   |
                   + - - - - - - - - - +
                  /                   /
             u   /                   /
                /   Area = ||u x v||/
               /                   /
              +-------------------+
                       v
## Geometric Definition
$$
u\times v= (\lVert u \rVert\lVert v \rVert \sin \theta )\hat{n}
$$

- $\lVert u \rVert\lVert v \rVert \sin \theta$: The area of the parallelogram(since base=$\left\| v \right\|$ and height=$\left\| u \right\|\sin \theta$)
- $\theta \in[0,\pi]$: The angle between $u$ and $v$.
- $\hat{n}$: The unit normal vector pointing perpendicular to the plane spanned by $u$ and $v$

#### **The Right-Hand Rule**

To determine which way $\mathbf{\hat{n}}$ points:

1. Point your right index finger along $u$
2. Curl your middle finger toward $v$.
3. Your thumb points in the direction of $u\times v$.

> [!tip]
> If $u\in Span \{ v \}$ or vice versa, then $\sin \theta=0$ so:
> 
> $$
> u\times v=0 \text{ and in particular }u\times u=0
> $$
> 

## Coordinate/Determinant Formula

Given 2 vectors in Cartesian components:
$$
u= \begin{bmatrix}
u_{1} \\
u_{2} \\
u_{3}
\end{bmatrix}, v=\begin{bmatrix}
v_{1} \\
v_{2} \\
v_{3}
\end{bmatrix}
$$

The cross product can be written using a symbolic determinant:

$$
u\times v=\det \begin{bmatrix}
i & j & k \\
u_{1} & u_{2} & u_{3} \\
v_{1} & v_{2} & v_{3}
\end{bmatrix}
$$

Expanding along the top row:

$$
\begin{align}
u\times v&=i\det \begin{bmatrix}
u_{2} & u_{3} \\
v_{2} & v_{3}
\end{bmatrix}-j\det \begin{bmatrix}
 u_{1} & u_{3} \\
 v_{1} & v_{3} 
\end{bmatrix}+k \det \begin{bmatrix}
u_{1} & u_{2} \\
v_{1} & v_{2}
\end{bmatrix} \\
&= i(u_{2}v_{3}-u_{3}v_{2})-j(u_{1}v_{3}-u_{3}v_{1})+k(u_{1}v_{2}-u_{2}v_{1}) \\
&= \begin{bmatrix}
u_{2}v_{3}-u_{3}v_{2} \\
-(u_{1}v_{3}-u_{3}v_{1}) \\
u_{1}v_{2}-u_{2}v_{1}
\end{bmatrix}
\end{align}
$$


What is $i,j,k$?
$i,j,k$ are $e_{1},e_{2},e_{3}\in \mathbb{R}^{3}$. 

What if we replace $i,j,k$ with other random number like $w=\begin{bmatrix}w_{1} \\  w_{2} \\  w_{3}\end{bmatrix}$? 

Then it is simply the dot product of $w$ and the vector $(u\times v)$. $(w\cdot(u\times v))$ 


---

## Core Mathematical Properties

1. **Anticommutative (order matters!):**
   $$v \times u = -(u \times v)$$
   *Swapping the vectors reverses your right hand, flipping the direction.*

2. **Orthogonality:**
   $$(u \times v) \cdot u = 0 \quad \text{and} \quad (u \times v) \cdot v = 0$$
   *The cross product is strictly perpendicular to both input vectors.*

3. **Bilinear (distributive over vector addition & scalar scaling):**
   $$u \times (c v + w) = c(u \times v) + (u \times w)$$
   $$(c u + w) \times v = c(u \times v) + (w \times v)$$

4. **Non-Associative:**
   $$(u \times v) \times w \neq u \times (v \times w)$$
   *(It does not associate. Instead, it satisfies the BAC-CAB rule: $u \times (v \times w) = v(u \cdot w) - w(u \cdot v)$).*

5. **Lagrange's Identity (Relationship to Dot Product):**
   $$\|u \times v\|^2 = \|u\|^2 \|v\|^2 - (u \cdot v)^2$$
   *(This algebraically mirrors $\sin^2\theta = 1 - \cos^2\theta$, linking magnitude directly to the parallelogram area).*

This is the vector version of Lagrange's Identity, we have seen the algebraic version which is 

$$
(x_{1}^{2}+x_{2}^{2})(y_{1}^{2}+y_{2}^{2})=(x_{1}y_{1}+x_{2}y_{2})^{2}+(x_{1}y_{2}-x_{2}y_{1})^{2}
$$
[[Problem Chapter 1 Basic Properties of Number#^prob-1-19-c]]

$(x_{1}^{2}+x_{2}^{2})(y_{1}^{2}+y_{2}^{2})=\lVert u \rVert^{2}\lVert v \rVert^{2}$
$(x_{1}y_{1}+x_{2}y_{2})^{2}=(u\cdot v)^{2}$ (Dot product)
$(x_{1}y_{2}-x_{2}y_{1})^{2}=\lVert u\times v \rVert^{2}$ (Cross product)

The Geometric Picture $(\cos ^{2}\theta+\sin ^{2}\theta=1)$

$$
\begin{align}
\lVert u\times v \rVert^{2}+(u\cdot v)^{2}&=\lVert u| \rVert^{2}\lVert v \rVert^{2}\sin ^{2} \theta+\lVert u \rVert^{2}\lVert v \rVert^{2}\cos ^{2}\theta \\
&=\lVert u \rVert^{2}\lVert v \rVert^{2}(\sin ^{2}\theta+\cos ^{2}\theta)=\lVert u \rVert^{2}\lVert v \rVert^{2}
\end{align}
$$

Cauchy-Schwarz can be prove using Lagrange identity.

---

### Interactive 3D Visualization Tool

Here is an interactive 3D visualizer built to let you see the geometry directly. You can drag with your mouse to rotate the 3D perspective, toggle the shadow projections on/off, or adjust the vector components:

```html-embed
cross_product_visualizer.html
```

*(You can also open the standalone visualizer tab in Obsidian: [[attachments/cross_product_visualizer.html|cross_product_visualizer.html]])*

---

### The Geometric Connection: The "Three Shadows" Principle

To understand why the algebraic formula:
$$
\mathbf{u} \times \mathbf{v} = 
\mathbf{i} \underbrace{\det \begin{bmatrix} u_2 & u_3 \\ v_2 & v_3 \end{bmatrix}}_{\text{Red Shadow}} 
- \mathbf{j} \underbrace{\det \begin{bmatrix} u_1 & u_3 \\ v_1 & v_3 \end{bmatrix}}_{\text{Green Shadow}} 
+ \mathbf{k} \underbrace{\det \begin{bmatrix} u_1 & u_2 \\ v_1 & v_2 \end{bmatrix}}_{\text{Blue Shadow}}
$$
is defined this way, look at what happens when a tilted 3D parallelogram is projected onto the three perpendicular coordinate walls:

#### 1. What does each $2 \times 2$ determinant represent?
In 2D flat space, a $2 \times 2$ determinant $\det \begin{bmatrix} a & b \\ c & d \end{bmatrix} = ad - bc$ calculates the **signed area of a parallelogram**.

When your parallelogram $\mathbf{u}, \mathbf{v}$ floats tilted in 3D space:
* **Shine a flashlight along the $x$-axis ($\mathbf{i}$):**
  It ignores the $x$-coordinates and casts a shadow on the $yz$-wall.
  The shadow's 2D vertices are $(u_2, u_3)$ and $(v_2, v_3)$.
  $$\text{Area of } yz\text{-shadow} = \det \begin{bmatrix} u_2 & u_3 \\ v_2 & v_3 \end{bmatrix} = u_2 v_3 - u_3 v_2$$
  Since this wall faces the **$x$-direction ($\mathbf{i}$)**, this area is placed in the **$\mathbf{i}$-slot**.

* **Shine a flashlight along the $y$-axis ($\mathbf{j}$):**
  It casts a shadow on the $xz$-wall.
  $$\text{Area of } xz\text{-shadow} = -\det \begin{bmatrix} u_1 & u_3 \\ v_1 & v_3 \end{bmatrix} = u_3 v_1 - u_1 v_3$$
  Since this wall faces the **$y$-direction ($\mathbf{j}$)**, this area is placed in the **$\mathbf{j}$-slot**.

* **Shine a flashlight along the $z$-axis ($\mathbf{k}$):**
  It casts a shadow on the flat floor ($xy$-plane).
  $$\text{Area of } xy\text{-shadow} = \det \begin{bmatrix} u_1 & u_2 \\ v_1 & v_2 \end{bmatrix} = u_1 v_2 - u_2 v_1$$
  Since this wall faces the **$z$-direction ($\mathbf{k}$)**, this area is placed in the **$\mathbf{k}$-slot**.

---

### 2. The 3D Pythagorean Theorem for Areas (De Gua's Theorem)

Think about how length works in 3D:
$$\text{Length}^2 = x^2 + y^2 + z^2$$
A 1D length squared is the sum of the squares of its 1D shadows on the three axes.

Remarkably, **the exact same rule holds for 2D areas in 3D space**:
$$
(\text{Total 3D Area})^2 = (\text{Area}_{yz})^2 + (\text{Area}_{xz})^2 + (\text{Area}_{xy})^2
$$

If you take the vector formed by these three shadow areas:
$$
\mathbf{w} = \begin{pmatrix} \text{Area}_{yz} \\ \text{Area}_{xz} \\ \text{Area}_{xy} \end{pmatrix} = \begin{pmatrix} u_2 v_3 - u_3 v_2 \\ u_3 v_1 - u_1 v_3 \\ u_1 v_2 - u_2 v_1 \end{pmatrix}
$$
then its vector length $\|\mathbf{w}\|$ is:
$$
\|\mathbf{w}\| = \sqrt{(\text{Area}_{yz})^2 + (\text{Area}_{xz})^2 + (\text{Area}_{xy})^2} = \text{Total 3D Area} = \|\mathbf{u}\|\|\mathbf{v}\|\sin\theta
$$

---

### 3. Why Does This Vector Point Perpendicular to the Surface?

If you tilt a plane in 3D space:
- Tilting it steep relative to the floor shrinks its floor shadow ($xy$).
- At the same time, its vertical wall shadows ($yz$ and $xz$) grow larger.

The trigonometric ratio between how large the shadows are on the three walls **exactly matches the direction of the normal vector** pointing straight out of the surface. 

By grouping the three wall shadows into $\mathbf{i}$, $\mathbf{j}$, and $\mathbf{k}$, the formula guarantees that:
1. **The vector points along the normal direction** ($\mathbf{u} \cdot \mathbf{w} = 0$ and $\mathbf{v} \cdot \mathbf{w} = 0$).
2. **The length of the vector equals the true 3D area** ($\|\mathbf{w}\| = \|\mathbf{u}\|\|\mathbf{v}\|\sin\theta$).

---

### What is 3D Area?

In everyday language:
* People hear **"2D"** and think **Area** (square meters, $\text{m}^2$).
* People hear **"3D"** and think **Volume** (cubic meters, $\text{m}^3$).

So hearing the phrase *"3D Area"* feels like an oxymoron! 

A more precise, unambiguous phrase is:
> **"The surface area of a 2D flat sheet that happens to be floating tilted inside 3D space."**

---

### The Paper Analogy

Imagine holding a flat sheet of paper (like an A4 sheet, or a flat solar panel):

1. **Lay it flat on your desk (2D space):**
   * It has a length and a width.
   * Its surface area is, say, $600\text{ cm}^2$.
   * Its 3D volume is essentially $0$ (it has no thickness).

2. **Now pick it up and tilt it at a $45^\circ$ angle in the air (3D space):**
   * Did it suddenly become a solid 3D brick with volume? **No!**
   * It is still just a flat sheet of paper with zero thickness.
   * Its surface area is **still $600\text{ cm}^2$**!
   * The only difference is that each corner now has three coordinates $(x, y, z)$ instead of two.

That is what was meant: **it is still a 2D area (measured in $\text{m}^2$, not $\text{m}^3$)**, but the parallelogram is floating tilted in 3D coordinate space.

---

### The 1D vs 2D vs 3D Embedding Analogy

To see why an object's **own dimension** is different from the **space it lives in**, look at a piece of string (a 1D line):

| Object                                        | Lives in...          | What we measure                                    | Formula                                                                                        |
| :-------------------------------------------- | :------------------- | :------------------------------------------------- | :--------------------------------------------------------------------------------------------- |
| **A straight string** on a ruler              | 1D space ($x$)       | **1D Length** ($\text{m}$)                         | $L=x$                                                                                          |
| **A string tilted** on a flat table           | 2D space ($x, y$)    | **Still 1D Length** ($\text{m}$)! *(Not an area)*  | $L = \sqrt{x^2 + y^2}$                                                                         |
| **A string tilted** in the air                | 3D space ($x, y, z$) | **Still 1D Length** ($\text{m}$)! *(Not a volume)* | $L = \sqrt{x^2 + y^2 + z^2}$                                                                   |
| **A flat sheet (parallelogram)** on the table | 2D space ($x, y$)    | **2D Area** ($\text{m}^2$)                         | $\text{Area}=a\times b$                                                                        |
| **A flat sheet tilted** in the air            | 3D space ($x, y, z$) | **Still 2D Area** ($\text{m}^2$)! *(Not a volume)* | $\text{Area} = \sqrt{A_{yz}^2 + A_{xz}^2 + A_{xy}^2} = \|\mathbf{u}\|\|\mathbf{v}\|\sin\theta$ |
| **A solid box (parallelepiped)**              | 3D space ($x, y, z$) | **3D Volume** ($\text{m}^3$)                       | $\text{Volume} = \mathbf{w} \cdot (\mathbf{u} \times \mathbf{v})$                              |

---

### Summary in One Sentence

* **$\|\mathbf{u}\| \|\mathbf{v}\| \sin\theta$** tells you: *"How many square meters of paint would it take to paint this tilted sheet?"* $\implies$ **Area** ($\text{m}^2$).
* **$\det[\mathbf{u} \quad \mathbf{v} \quad \mathbf{w}]$** tells you: *"How many liters of water can this solid box hold?"* $\implies$ **Volume** ($\text{m}^3$).


---

## Method 2: Expanding from the Unit Axes (Algebraic Route)

Another intuitive way to arrive at the determinant formula is to expand the cross product directly using the standard unit basis vectors $\mathbf{i}, \mathbf{j}, \mathbf{k}$ (where $\mathbf{i} = \begin{bmatrix}1\\0\\0\end{bmatrix}, \mathbf{j} = \begin{bmatrix}0\\1\\0\end{bmatrix}, \mathbf{k} = \begin{bmatrix}0\\0\\1\end{bmatrix}$).

### 1. The Rules for Basis Vectors
Applying the geometric definition ($\text{length} = \|\mathbf{a}\|\|\mathbf{b}\|\sin\theta$ and the right-hand rule) directly to $\mathbf{i}, \mathbf{j}, \mathbf{k}$ gives three simple rules:

1. **Parallel vectors give zero** ($\theta = 0^\circ \implies \sin 0^\circ = 0$):
   $$\mathbf{i} \times \mathbf{i} = \mathbf{0}, \qquad \mathbf{j} \times \mathbf{j} = \mathbf{0}, \qquad \mathbf{k} \times \mathbf{k} = \mathbf{0}$$

2. **Perpendicular unit axes cycle forward** ($\theta = 90^\circ$, area $= 1 \times 1 = 1$):
   $$\mathbf{i} \times \mathbf{j} = \mathbf{k}, \qquad \mathbf{j} \times \mathbf{k} = \mathbf{i}, \qquad \mathbf{k} \times \mathbf{i} = \mathbf{j}$$
   *(Mnemonic: $\mathbf{i} \to \mathbf{j} \to \mathbf{k} \to \mathbf{i}$)*

3. **Reversing the order flips the sign** (right hand curls backward):
   $$\mathbf{j} \times \mathbf{i} = -\mathbf{k}, \qquad \mathbf{k} \times \mathbf{j} = -\mathbf{i}, \qquad \mathbf{i} \times \mathbf{k} = -\mathbf{j}$$

### 2. Distributing the Product Across All 9 Terms
Write arbitrary vectors $\mathbf{u}$ and $\mathbf{v}$ in unit vector form:
$$\mathbf{u} = u_1 \mathbf{i} + u_2 \mathbf{j} + u_3 \mathbf{k}, \qquad \mathbf{v} = v_1 \mathbf{i} + v_2 \mathbf{j} + v_3 \mathbf{k}$$

Because the cross product distributes over addition, multiplying them expands into $3 \times 3 = 9$ terms:
$$
\begin{aligned}
\mathbf{u} \times \mathbf{v} 
&= u_1 v_1 (\mathbf{i} \times \mathbf{i}) + u_1 v_2 (\mathbf{i} \times \mathbf{j}) + u_1 v_3 (\mathbf{i} \times \mathbf{k}) \\
&\quad + u_2 v_1 (\mathbf{j} \times \mathbf{i}) + u_2 v_2 (\mathbf{j} \times \mathbf{j}) + u_2 v_3 (\mathbf{j} \times \mathbf{k}) \\
&\quad + u_3 v_1 (\mathbf{k} \times \mathbf{i}) + u_3 v_2 (\mathbf{k} \times \mathbf{j}) + u_3 v_3 (\mathbf{k} \times \mathbf{k})
\end{aligned}
$$

Substitute the basis rules:
- The 3 self-products vanish: $u_1 v_1(\mathbf{0}) + u_2 v_2(\mathbf{0}) + u_3 v_3(\mathbf{0}) = \mathbf{0}$.
- The remaining 6 terms pair up:
$$
\begin{aligned}
\mathbf{u} \times \mathbf{v} 
&= u_1 v_2 (\mathbf{k}) + u_1 v_3 (-\mathbf{j}) + u_2 v_1 (-\mathbf{k}) + u_2 v_3 (\mathbf{i}) + u_3 v_1 (\mathbf{j}) + u_3 v_2 (-\mathbf{i})
\end{aligned}
$$

### 3. Grouping into $2 \times 2$ Determinants
Factoring out $\mathbf{i}, \mathbf{j}, \mathbf{k}$:
$$
\mathbf{u} \times \mathbf{v} = 
(u_2 v_3 - u_3 v_2)\mathbf{i} 
- (u_1 v_3 - u_3 v_1)\mathbf{j} 
+ (u_1 v_2 - u_2 v_1)\mathbf{k}
$$

Each paired coefficient is precisely a $2 \times 2$ determinant:
$$
\mathbf{u} \times \mathbf{v} = 
\mathbf{i}\det \begin{bmatrix} u_2 & u_3 \\ v_2 & v_3 \end{bmatrix} 
- \mathbf{j}\det \begin{bmatrix} u_1 & u_3 \\ v_1 & v_3 \end{bmatrix} 
+ \mathbf{k}\det \begin{bmatrix} u_1 & u_2 \\ v_1 & v_2 \end{bmatrix} 
= \begin{bmatrix}
u_2 v_3 - u_3 v_2 \\
-(u_1 v_3 - u_3 v_1) \\
u_1 v_2 - u_2 v_1
\end{bmatrix}
$$

---

## Generalization to $n$ Dimensions

### 1. Why the Standard Cross Product Only Works in 3D (The $n - 2$ Rule)

Why can't we take two vectors in 4D or 5D and get a single perpendicular vector?

Two vectors $\mathbf{u}$ and $\mathbf{v}$ always span a **2D plane**. In an $n$-dimensional space, the space of all directions perpendicular to that plane has dimension:
$$\text{Perpendicular Dimension} = n - 2$$

- **In 2D ($n = 2$):** $2 - 2 = 0$. There are no perpendicular directions inside the plane! (The result is a scalar).
- **In 3D ($n = 3$):** $3 - 2 = \mathbf{1}$. The perpendicular space is a **1-dimensional line**. A 1D line has only one direction ($\pm \hat{\mathbf{n}}$). This unique coincidence is why 3D has a single cross product vector!
- **In 4D ($n = 4$):** $4 - 2 = \mathbf{2}$. The perpendicular space is an entire **2D plane**. There are infinitely many perpendicular directions with no unique choice.

---

### 2. Generalization A: The $(n-1)$-Vector Cross Product (To get a Vector)

If you want a single perpendicular vector in $n$ dimensions, you must supply **$n - 1$ vectors**. 

The perpendicular dimension is then:
$$\text{Perpendicular Dimension} = n - (n - 1) = \mathbf{1} \quad (\text{always a unique line!})$$

This generalized cross product uses an $n \times n$ determinant with the basis vectors along the top row:

* **In 2D (needs $2 - 1 = 1$ vector):**
  $$\mathbf{v}^\perp = \det \begin{bmatrix} \mathbf{i} & \mathbf{j} \\ v_1 & v_2 \end{bmatrix} = \begin{bmatrix} -v_2 \\ v_1 \end{bmatrix}$$
  *(Rotates a 2D vector by $90^\circ$)*

* **In 3D (needs $3 - 1 = 2$ vectors):**
  $$\mathbf{u} \times \mathbf{v} = \det \begin{bmatrix} \mathbf{i} & \mathbf{j} & \mathbf{k} \\ u_1 & u_2 & u_3 \\ v_1 & v_2 & v_3 \end{bmatrix}$$

* **In 4D (needs $4 - 1 = 3$ vectors):**
  $$\mathbf{u} \times \mathbf{v} \times \mathbf{w} = \det \begin{bmatrix} \mathbf{e}_1 & \mathbf{e}_2 & \mathbf{e}_3 & \mathbf{e}_4 \\ u_1 & u_2 & u_3 & u_4 \\ v_1 & v_2 & v_3 & v_4 \\ w_1 & w_2 & w_3 & w_4 \end{bmatrix}$$
  *(Produces a single 4D vector perpendicular to all three input vectors)*

---

### 3. Generalization B: The Wedge Product $\mathbf{u} \wedge \mathbf{v}$ (To get Area)

If you strictly want to multiply **only two vectors** in any dimension $n$, mathematicians use **Exterior Algebra**:
* Instead of forcing the output to be a 1D arrow, we define the product $\mathbf{u} \wedge \mathbf{v}$ (called a **bivector**).
* A bivector represents the **oriented 2D parallelogram itself**, rather than a normal arrow.
* This works identically in 2D, 3D, 4D, and any $n$-dimensional space. In 3D, the Hodge star dual converts this 2D bivector into the classical cross product arrow: $\star(\mathbf{u} \wedge \mathbf{v}) = \mathbf{u} \times \mathbf{v}$.