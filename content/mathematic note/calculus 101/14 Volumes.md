
> [!NOTE] Definition of Volume
> Let $S$ be a solid that lies between $x=a$ and $x=b$. If the cross-sectional area of $S$ in the plane $P_{x}$, through $x$ and perpendicular to the x-axis (横截面), is $A(x)$, where $A$ is a continuous function, then the volume of $S$ is
> 
> $$
> V=\lim_{ n \to \infty } \sum_{i=1}^{n} A(x_{i}^{*})\triangle x= \int_{a}^{b} A(x) \, dx 
> $$

![[Pasted image 20260624224233.png]]

Show that the volume of a sphere of radius $r$ is $V= \frac{4}{3}\pi r^{3}$.

$$
r^{2}=y^{2}+ x^{2}
$$

Thus,
$$
y^{2}=r^{2}-x^{2}
$$

The area of cross sectional part

$$
A=\pi y^{2}
$$
By substitution

$$
A(x)=\pi (r^{2}-x^{2})
$$

$$
\begin{align}
\int_{-r}^{r} \pi(r^{2}-x^{2})  \, dx &= \pi r^{2}\int_{-r}^{r}1  \, dx - \pi \int_{-r}^{r} x^{2} \, dx \\
&=\pi r^{2}[x]^{r}_{-r} -\pi\left[ \frac{x^{3}}{3} \right]^{r}_{-r} \\
&=2\pi r^{3}-\pi\left( \frac{r^{3}}{3}+ \frac{r^{3}}{3} \right) \\
&=2\pi r^{3}-\frac{2}{3}\pi r^{3} \\
&=\frac{4}{3}\pi r^{3}
\end{align}
$$

The solids are all called **solids of revolution** because they are obtained by revolving a region about a line. We **calculate** the volume of a solid of revolution by using the basic defining formula

$$
V= \int_{a}^{b} A(x) \, dx \text{ or }V=\int_{c}^{d} A(y) \, dy 
$$

and we find the cross-sectional area A(x) or A(y) in one of the following ways:
- If the cross-section is a disk, we find the radius of the disk (in terms of $x$ or $y$) and use
$$
A=\pi(radius)^{2}
$$
- If the cross-section is a washer, we find we find the inner radius $r_{in}$ and outer radius $r_{out}$ from a sketch and compute the area of the washer by subtracting area of the inner disk from the area of the outer disk:
$$
A=\pi(\text{outer radius})^{2}-\pi(\text{inner radius})^{2}
$$

> [!tip]
> Think process:
> The radius is actually $y$ in term of $x$. (It is the height of the slice that vertical to the rotating axis, so in the derivation, $r$ is the radius of sphere and $y=(r^{2}-x^{2})$ is the radius of each slice.)
> 
> How can this method be generalize?
> $y$ is the radius of each slice, but $y$ is not a fixed number, $y$ is a function value in term of $x$, Thus, the general method of finding the volume rotate $x$-axis is
> 
> $$
> V= \int y \, dx=\int (\text{radius in term of x}) \, dx
> $$
> What if we rotate about $y$-axis?
> Then the radius is $x$, and the thickness of each slice is $\triangle y$. To make the integral with respect to $\triangle y\to 0$ work, we need to express the radius $x$ in term of $y$. (From Riemann Sum). Thus,
> $$
> V=\int x \, dy=\int (\text{radius in term of y}) \, dy
> $$
> Can we generalize further ?
> What if it is hollow? Then it is simply
> 
> $$
> A=\pi(\text{outer radius})^{2}-\pi(\text{inner radius})^{2}
> $$
> 
> What if we didn't rotate about $x,y$ axis?
> 
> For example what if we rotate about $y=1$? (Notice that $y=1$ is a line parallel with $x$-axis)
> 
> So imagine it is like we shift graph $1$ unit down(the radius $r=y$ is shifting down 1 unit.).
> 
> Thus,  The radius become $r=y-1$. We express in term of $x$:
> 
> $$
> A=\pi \int (y_{1}-1)^{2}-(y_{2}-1)^{2} \, dx
> $$
> where $y_{1}$ is outer radius in term of $x$ and $y_{2}$ is inner radius in term of $y$.
> 


---

## Volumes by Cylindrical Shells

Let's consider the problem of finding the volume of the solid by rotating about the y-axis the region bounded by $y=2x^{2}-x^{3}$ and $y=0$

![[Pasted image 20260625094107.png]]

If we slice perpendicular to the $y$-axis, we get a washer.

But to compute the inner radius and the outer radius of the washer, we’d have to solve the cubic equation $y=2x^{2}-x^{3}$for x in terms of y; that’s not easy.

Fortunately, there is a method, called the **method of cylindrical shells.**

### The Algebraic Derivation (The Rigorous Way)
The volume $V$ is calculated by subtracting the volume $V_{1}$ of the inner cylinder from the volume $V_{2}$ of the outer cylinder.

$$
\begin{align}
V&=V_{2}-V_{1} \\
&=\pi r_{2}^{2}h-\pi r_{1}^{2}h \\
&=\pi h(r_{2}^{2}-r_{1}^{2}) \\
&=\pi h(r_{2}-r_{1})(r_{2}+r_{1}) \\

\end{align}
$$
1. **Thickness:** $\Delta r = r_2 - r_1$
    
2. **Average Radius:** $r = \frac{1}{2}(r_2 + r_1) \implies (r_2 + r_1) = 2r$
    

Substitute these two definitions directly back into our factored volume equation:

$$V = \pi h \underbrace{(r_2 - r_1)}_{\Delta r} \underbrace{(r_2 + r_1)}_{2r}$$

Rearrange the factors, and there it is:

$$V = 2\pi r h \, \Delta r$$
### The Geometric Intuition (The "Unrolling" Way)

Imagine the cylindrical shell is made of thin cardboard. If you make a vertical slice straight down the side (this is the main step to calculate the volume with respect to $x$) and unroll it flat, what shape do you get? You get a flat, rectangular box (a rectangular prism).

![[Pasted image 20260625100342.png]]



To find the volume of this flattened box, you just multiply its three dimensions: $\text{Length} \times \text{Height} \times \text{Thickness}$.

- **Length:** This was the outer boundary of the cylinder, which is just its circumference. Since the average radius is $r$, the unrolled length is $2\pi r$.
    
- **Height:** The vertical height of the cylinder remains exactly the same, $h$.
    
- **Thickness:** The thickness of the cardboard box is the change in radius, $\Delta r$.
    

Multiplying these together yields the exact same result:

$$\text{Volume} = \underbrace{(2\pi r)}_{\text{circumference}} \times \underbrace{\vphantom{(2\pi r)}h}_{\text{height}} \times \underbrace{\vphantom{(2\pi r)}\Delta r}_{\text{thickness}}$$

### How is it related to $x$?

### Breaking Down the Shell Components

Look at how a single vertical rectangle forms a shell when spun around the $y$-axis (as shown in Figure 5 on page 10):

- **The Thickness ($\Delta x$ or $dx$):** Because the rectangle stands vertically, its thickness lies flat along the horizontal axis. Therefore, the thickness of the shell is a tiny change in $x$, which translates to $dx$ in the integral.
    
- **The Radius ($x$):** The radius of the shell is the distance from the center of rotation (the $y$-axis) out to the rectangle. Since it is a horizontal distance from $x=0$ to whatever coordinate you are at, the radius is simply $x$.
    
- **The Height ($f(x)$):** The height of the vertical rectangle is determined by how tall the function is at that specific $x$-coordinate, which is $f(x)$.
    

When you put all of these pieces into the volume formula from page 5 ($V = 2\pi \cdot \text{radius} \cdot \text{height} \cdot \text{thickness}$) , everything naturally lands in terms of $x$:

$$V = \int_{a}^{b} 2\pi \cdot \underbrace{x}_{\text{radius}} \cdot \underbrace{f(x)}_{\text{height}} \cdot \underbrace{\vphantom{f(x)}dx}_{\text{thickness}}$$
It is because

$$
\lim_{ n \to \infty } \sum_{i=1}^{n} 2\pi x_{i}
$$

Thus,

The volume of the solid , obtained by rotating about the y-axis the region under the curve $y=f(x)$ from $a$ to $b$, is

$$
V= \int_{a}^{b} 2\pi xf(x) \, dx 
$$

![[Pasted image 20260625103527.png]]
### Example 1
Find the volume of the solid obtained by rotating about the y-axis the region bounded by $y=2x^{2}-x^{3}$ and $y=0$.

> [!tip]
> The thinking process:
> We want to find integral with respect to $dx$, how to find the volume of a solid of revolution with respect to $dx$? Imagine a geometric figure with width is $dx$ and height is $f(x)$,  is a rectangle parallel to the rotating axis!!! How this rectangle used to form the volume? It form by rotating the rectangle along the axis. 
> 
> How to find the formula?
> Notice that if we unrolling it and flatten out the rotating rectangle with small amount of width($dx$), then it become a sheet of paper where its width is $2\pi x$ and height is $f(x)$, thus the volume is
> 
> $$
> 2\pi xf(x)dx
> $$
> To calculate the Riemann Sum, it become
> 
> $$
> A=2\pi \int {x}f(x)\,dx
> $$
> but what if it is bounded by 2 curve? Then we just simply take $V_{1}-V_{2}$ where $V_{1}$ is bigger than $V_{2}$. 
> 
> Notice that if we have 2 different curve, the only component that different is the value of function, the $x$ is still the same, thus
> 
> $$V = 2\pi \int_{a}^{b} x \left[ f(x) - g(x) \right] dx$$**Shell Height:** Distance from one end of the slice to the other (e.g., $f(x)$, or $\text{Top} - \text{Bottom}$, or $\text{Right} - \text{Left}$).


> [!remark]
> Notice that the $x$ is the average radius, but because we take the limit to infinity, we can ignore about this fact, but if we want to take finite limit Riemann Sum then we need to use the midpoint of the interval,
>
>As we take the limit as $n \to \infty$ (meaning the thickness $\Delta x \to 0$):
>
>- The inner radius $x_{i-1}$ and the outer radius $x_i$ squeeze closer and closer together.
  >  
>- The midpoint is trapped between them.
>
By the time we transition to the continuous integral, the interval shrinks to an infinitely thin width ($dx$). The inner radius, outer radius, and midpoint all collapse into the exact same value: a single, continuous variable **$x$**.
>
Because any sample point (left endpoint, right endpoint, or midpoint) converges to the exact same value under a definite integral, the distinction completely vanishes in the limit.
> 

---

## The Core Problem

We analyzed the volume of a solid generated by rotating the curve $y = x^2$ (from $y = 0$ to $y = 4$) around the **$y$-axis**.

Because the axis of rotation is vertical, the Shell Method requires setting up vertical strips and integrating with respect to $x$.

- **Radius ($r$):** The distance from the $y$-axis to the strip, which is always $x$.
    
- **Limits of Integration:** From $x = 0$ to $x = 2$ (where the curve hits the ceiling $y = 4$).
    

The generic shell formula is:

$$V = \int_{a}^{b} 2\pi \cdot (\text{radius}) \cdot (\text{height}) \, dx$$

## Two Interpretations: Case 1 vs. Case 2

Depending on how a problem specifies the bounded region, the setup changes entirely:

### Case 1: Region Above the Curve (The Solid Dome)

- **Keywords:** Bounded by $y = x^2$, the $y$-axis, and the ceiling $y = 4$.
    
- **Shell Height:** The vertical strip goes from the curve up to the ceiling.
    
    $$\text{Height} = \text{Top} - \text{Bottom} = 4 - x^2$$
    
- **The Integral:**
    
    $$V = \int_{0}^{2} 2\pi x (4 - x^2) \, dx = 2\pi \int_{0}^{2} (4x - x^3) \, dx = \mathbf{8\pi}$$
    

### Case 2: Region Below the Curve (The Hollowed Bowl)

- **Keywords:** Bounded by $y = x^2$, the $x$-axis (floor), and the line $x = 2$.
    
- **Shell Height:** The vertical strip goes from the floor up to the curve.
    
    $$\text{Height} = x^2$$
    
- **The Integral:**
    
    $$V = \int_{0}^{2} 2\pi x (x^2) \, dx = 2\pi \int_{0}^{2} x^3 \, dx = \mathbf{8\pi}$$
    

## The Great Coincidence

You noticed that both integrals resulted in the exact same answer: **$8\pi$**.

This is a beautiful geometric fluke unique to $y = x^2$ on this specific interval. Imagine a solid outer cylinder of radius 2 and height 4. Its total volume is:

$$V_{\text{total}} = \pi r^2 h = \pi (2)^2 (4) = 16\pi$$

The parabola $y = x^2$ happens to slice this entire cylinder **exactly in half (50% each)**. Case 1 calculates the solid top piece ($8\pi$), and Case 2 calculates the bottom piece ($8\pi$). When you change the function to anything else (like $y = x^3$), this symmetry breaks completely, and the two cases yield completely different volumes.

> [!remark] Critical Remark
>  
>  **We cannot blindly take the function value ($y = f(x)$) as the height of the shell.**
>  
>  You must always look at the physical boundaries of the problem to determine if the height is measured from the floor up to the curve ($\text{height} = f(x)$) or from the curve up to a ceiling ($\text{height} = \text{ceiling} - f(x)$). Missing this detail usually leads to a wrong answer—unless you get lucky with $y = x^2$!