How to show if $A\cong B$ and $B\cong C$, then $A\cong C$.

The definition of congruent:
We say 2 geometry figure is congruent if we move one of the geometric figure without changing the distance and shape and it is able to superimpose the other. (All point that form the geometric figure is overlapping)

Notice that the action of moving is like transformation under a function which is bijective (one to one and onto). Thus, we can define a function $f:A\to B$ where $A$ is the set of all point in first geometric figures and as well as $B$ defined as
$$
f(A)=B
$$


How to formalize the property of without change, which mean without enlargement or shrinking. It work by preserving the distance between any 2 point in the geometric figure. Thus, in detail
$$
d(x,y)=d(f(x),f(y))
$$
where $d(x,y)$ is the distance any 2 point.

Thus we define a new function for $B\cong C$ where $d(g(x),g(y))=d(x,y)$
$$
g(B)=C
$$
Thus, let's define a new function 
$$
h=g \circ f
$$
Now, we must verify two things about $h$:

**First, does $h$ map $A$ to $C$?**

If we apply $h$ to the entire figure $A$, we get:

$$h(A) = g(f(A))$$

Since we know $f(A) = B$, we can substitute $B$ into the equation:

$$h(A) = g(B)$$

And since we know $g(B) = C$, it follows that:

$$h(A) = C$$

**Second, is $h$ an isometry?**

Let $x$ and $y$ be any two points. We need to check if $h$ preserves the distance between them.

$$d(h(x), h(y)) = d(g(f(x)), g(f(y)))$$

Because $g$ is an isometry, it preserves the distance between the points $f(x)$ and $f(y)$:

$$d(g(f(x)), g(f(y))) = d(f(x), f(y))$$

Because $f$ is also an isometry, it preserves the distance between the original points $x$ and $y$:

$$d(f(x), f(y)) = d(x, y)$$

Therefore, linking the equations together, we find:

$$d(h(x), h(y)) = d(x, y)$$

---
In other world the formal definition for congruent:

We say $A$ and $B$ (which can be thought of as sets of points in a metric space, like $\mathbb{R}^n$) are defined as congruent, written as $A \cong B$, if there exists an **isometry** that maps $A$ perfectly onto $B$.

An isometry is a bijective (one-to-one and onto) function that preserves the distance between any two points. If $d(x, y)$ is the distance between points $x$ and $y$, a function $f$ is an isometry if:

$$d(f(x), f(y)) = d(x, y)$$

