
Geometry is a theory study about the properties of geometric figures. 

What is geometric figures.
A set of points, lines, surfaces, or solids positioned in a certain way in space is generally called a geometric figure.

Geometric figures can be a set of point or a point. In other world geometric figures is a universal term (big category)
- A single point is a figure.
- A flat plane is a figure.
- An empty, hollow sphere (just the surface) is a figure.
- A solid cube is _also_ a figure.


Geometric solid is the part of space occupied by a physical object . (3 dimension)
> [!note] geometric boundaries
A geometric solid is separated from the surrounding space by a surface. 
A part of the surface is separated from an adjacent part by a line.
A part of the line is separated from an adjacent part by a point.
>
Thus $n$ dimension geometric figure always separated by $(n-1)$ dimensional geometric figure 
>
In other word, the intersection of  $n$ dimensional geometric figure is $n-1$ dimensional geometric figure with the assumption of they are going unboundedly.


> [!info] Abstraction
In real world point, line, surface, solid is not separated. But we should think of surface as having no thickness as well as line and point

> [!note] Congruent
> Two geometric figuresare called congruent, if by moving one of the figures it is possible to superimpose it onto the other so that the two figures become identified with each other in all their parts.

### The properties of plane
One can superimpose a plane on itself (rotation) or any other plane in a way that takes one given point to any other given point (translation), and this can also be done after flipping the plane upside down (flipping).

#### Mathematical Formalization

If we represent the plane as $\mathbb{R}^2$, these operations form what is known as the **Euclidean Group**, denoted as $E(2)$.

1. **Translations:** $f(v) = v + a$, where $a$ is a constant vector.
2. **Orthogonal Transformations:** $f(v) = Mv$, where $M$ is an orthogonal matrix (representing rotations and reflections).
> [!hint] Commutative
> Notice that geometry operation is not commutative



The relationship between bijective function 
[[Chapter 7 Function#^5dd9d2]]

#### 2. The Symmetry as a "Bijection"

A symmetry operation is an action you perform on that object that leaves it looking exactly the same as when you started. Mathematically, this is a mapping from the set to itself:

- **It is Injective (One-to-One):** When you rotate a square, two corners never crash into the same spot. Every point goes to a unique destination. 
- **It is Surjective (Onto):** After the rotation, there are no "empty" corners. Every spot is filled by a point.

Because it perfectly shuffles the points without losing or duplicating any, a symmetry operation is exactly a **bijective function**.

---
#### The rotation assumption (plane)

You are completely correct that to flip a 2D surface over so its "front" becomes its "back" (like flipping a pancake), you absolutely need to lift it into a 3rd dimension.

However, since you are studying **planimetry** (strictly 2D geometry), the rotations you are dealing with happen entirely _flat_ within the plane itself. Because a plane already has two dimensions (length and width), it has enough room for points to swing around each other without ever leaving the surface.

Here is how the two types of movement differ:

### 1. The 3D Rotation (Flipping out of the plane)

If you have a left-handed glove drawn on a piece of paper, and you want to rotate it to perfectly match a right-handed glove, you cannot do it by just sliding it around on the desk. You would have to peel the paper off the desk into 3D space, flip it over, and put it back down.

- In planimetry, we don't call this a rotation. We call this a **reflection** (flipping across a 1D line).
    

### 2. The 2D Rotation (Spinning within the plane)

In planimetry, when we say "rotation," we mean picking a single point on the flat surface (the center of rotation) and spinning the rest of the shape around that point, like a record on a turntable or the hands of a clock.

- The shape stays entirely flat.
    
- No 3D space is required.
    
- Every point simply travels along a flat, circular path around the center point.
    

### Why lines couldn't do this

A 1D line only has "forward" and "backward." It doesn't have "left" or "right." Because it lacks that second direction, there is no room to draw a circle, which means there is no way to spin a point around without pulling it out of the line entirely. A 2D plane gives you that second direction, unlocking the ability to spin!

---
### The straight line
For every two points in space, there is a straight line passing through them., and such a line is unique. (The gradient tell the difference)

two straight lines can intersect at most at one point. (Because if more than one point intersect, it means that 2 line are identical)

What if we study the property of line in a surface?

Then we can conclude that If a straight line passes through two points of a plane, then all points of this line lie in this plane.

> [!info] Straight line
Thinking of a straight line as extended indefinitely in both directions, one calls it an infinite (or unbounded) straight line. A straight line is usually denoted by two uppercase letters. ($AB$)

> [!info] Straight segment
A part of the straight line bounded on both sides is called a straight segment. It denoted by $AB$ or $a$.

> [!info] Ray
A line which bounded in one direction only  called ray.

> [!info] Congruent of line
Two segments are congruent if they can be laid one onto the other so that their endpoints coincide.

> [!info] Sum of segments
> The sum of several given segments (AB,CD, SF) is a segment which is obtained as follows. Ona line, pick any point M and starting from it mark a segment MN congruent to AB and so on
> 
> It is commutative and associative

---

### Circle
Circle is a curved line where the distance from a set of point and its center is constant.

A segment (EF) connecting the center with a point of the circle is called a radius.

Two circle are congruent when the radius are same.

A line (MN) intersecting the circle at any two points is called a secant.

A segment (EF) both of whose endpoints lie on the circle is called a chord.

A chord (AD) passing through the center is called a diameter.

A part of a circle contained between any two points (for example, EmF) is called an arc. $\stackrel{\frown}{EmF}$

The chord connecting the endpoints of an arc is said to subtend this arc.

The part of the plane bounded by a circle is called a disk.


The part of a disk contained between two radius (the shaded part COB in Figure 6) is called a sector,

and the part of the disk cut off by a secant (the part EmF) is called a disk segment.


![[Pasted image 20260327114843.png]]



Two arcs of the same circle (or of two congruent circles) are congruent if they can be aligned so that their endpoints coincide.

Why same circle? Because if the circle is with different radius, then even though the endpoint coincide but the intermediate point are not coincide.

 Sum of arcs are calculated same as the sum of segment.

