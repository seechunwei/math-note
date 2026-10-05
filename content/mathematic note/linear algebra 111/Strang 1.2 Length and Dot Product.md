==Fact 1==
The dot product of 2 vectors $v=(v_{1},v_{2})$ and $w=(w_{1},w_{2})$ is the number 
$$
vw=(v_{1}w_{1}+v_{2}w_{2})
$$

It multiply by element and add together. Geometrically, it is length of vectors multiply the angles between them.


The Intuitive View: Projection
Suppose got 2 vector $a$ and $b$ from same point, they form a angle. Imagine we put b on the floor and there exist a light come from $a$ and perpendicular to $b$. Thus, it form a shadow of $a$ onto $b$ and it form a right angle triangle. 

![[Pasted image 20260405152346.png]]



$$\cos \theta = \frac{\text{Adjacent}}{\text{Hypotenuse}} = \frac{\text{length of shadow}}{\|\mathbf{A}\|}$$
Rearranging this gives you the length of that shadow:
$$\text{Length of shadow} = \|\mathbf{A}\| \cos \theta$$

$$\begin{align}
\mathbf{A} \cdot \mathbf{B} = (\text{length of projection}) \times (\text{length of base})& = (\|\mathbf{A}\| \cos \theta) \|\mathbf{B}\|
\end{align}$$

Dot product is zero means Perpendicular vectors. Why?
Suppose the length of vector is not 0, then by zero product rule it follow that $\cos \theta=0$. By unit circle, it is clear that $\theta=90^\circ$. (with the assumption $\theta\leq180$ ). Thus, it is perpendicular. 

The dot product w · v equals v · w. The order of v and w makes no difference.

---
What if we multiply a vector by itself?
Since they are on the same line, the angle is 0. Thus, $\cos 0^\circ=1$. So the equation become
$$
\begin{align}
v^{2}&=\text{length of projection}\times length og base \\
&=||v||^{2}
\end{align}
$$
==Fact 2==
Thus, the length of $v$ is
$$
\begin{align}
||v||&=\sqrt{ v \cdot v } \\
&=\sqrt{ (v_{1}^{2}+v_{2}^{2}+\dots v_{n}^{2}) }
\end{align}
$$

How about 3 dimension?
Suppose a vector $v=(1,2,3)$ the $||v||=\sqrt{ 14 }$


We split in to 2 cases, let examine $(1,2)$ , it a diagonal of parallelogram which side are $1$ and $2$. In other word it is the hypotenuses with side $1,2$ . The length is $\sqrt{ 1^{2}+2^{2} }=\sqrt{ 5 }$. (Pythagoras formula) . 

This base vector is perpendicular to (0, 0, 3) that goes straight up. So the diagonal of the box has length 
$$
\begin{align}
||v||=\sqrt{ 5+9 }=\sqrt{ 14 }
\end{align}
$$
![[Pasted image 20260405155403.png]]


---
==Fact 3==
A unit vector u is a vector whose length equals one. Then u · u = 1.

The unit vector form a unit circle from origin. Thus, it is defined as
$$
v=(\cos \theta,\sin \theta)
$$
==Fact 4==
Unit vector 
$$
u=\frac{u}{||u||}
$$
is a unit vector in the same direction as $u$.

---
The dot product is v ·w = 0 when v is perpendicular to w.

Proof:
When $v$ and $w$ are perpendicular, they form  2 sides of right triangle. The third side is $v-w$. Thus,

$$
||v-w||^{2}=||v||^{2}+||w||^{2}
$$
Writing out the formulas for those lengths in two dimensions, this equation is

$$
(v_{1}-w_{1})^{2}+(v_{2}-w_{2})^{2}=(v_{1}^{2}+v_{2}^{2})+(w_{1}^{2}+w_{2}^{2})
$$

Expand:
$$
v_{1}^{2}-2v_{1}w_{1}+w_{1}^{2}+v_{2}^{2}-2v_{2}w_{2}+w_{2}^{2}
$$

We cancel $v_{1}^{2}+w_{1}^{2}+v_{2}^{2}+w_{2}^{2}$ on both side. Thus,

$$
\begin{align}
-2v_{1}w_{1}-2v_{2}w_{2}&=0 \\
v_{1}w_{1}+v_{2}w_{2}&=0
\end{align}
$$

Conclusion: Right angles produce v · w = 0.

What if $v\cdot w$ is not $0$. It may be positive or negative. $\cos \theta$ is the x-coordinate, if negative means $\theta> 90$ and vice versa.


If $v$ and $w$ are not unit vectors?
$$
\cos \theta= \frac{v\cdot w}{||v||||w||}
$$

Since $|\cos \theta|<1$， it follow that

Schwarz inequality
$$
|v\cdot w|\leq||v|| ||w||
$$
Triangle inequality
$$
||v+w||\leq||v||+||w||
$$

---


### Worked Problem 1.2 A
1) Test $|v\cdot w|\leq||v||||w||$

$$
|v\cdot w|=12+12=24
$$
The length of $v$ and $w$:
$$
||v||=\sqrt{ v^{2} }=\sqrt{ 25 }=5
$$
$$
||w||=\sqrt{ w^{2} }=\sqrt{ 25 }=5
$$

$|24|<25\to24<25$. True


Test; $||v+w||\leq||v||+||w||$

$v+w=(7,7)$
$||v+w||=\sqrt{ (v+w)^{2} }=\sqrt{ 98 }=2\sqrt{ 7 }$

$2\sqrt{ 7 }<5+5$

Find $\cos \theta$ for the angle between $v$ and $w$.
$$
\begin{align}
\frac{v\cdot w}{||v||||w||}&=\cos \theta \\
\cos \theta&= \frac{24}{25}
\end{align}
$$

One vector is a multiple of the other as in w = cv. Then the angle is 0° or 180°.In this case $|\cos \theta|=1$ and $|w\cdot v|=||w||||v||$ 

If the angle is 0°, as in w = 2v, then $||v+w||=||v||+||w||$ (both sides give 3llvll). This v, 2v, 3v triangle is flat!

1.2 B
$|v|=\sqrt{ v^{2} }=\sqrt{ (25) }=5$

$$
\begin{align}
u&=\frac{v}{|v|} \\
&=\left( \frac{3}{5}, \frac{4}{5} \right) \\
\end{align}
$$

Suppose $U$ is perpendicular to $u$. Then it follow that 
$$
\begin{align}
|U\cdot u|&=0 \\
\left( U_{1}\times \frac{3}{5} \right)+\left( U_{2}\times \frac{4}{5} \right)&=0 \\
U&=\left( -\frac{4}{5}, \frac{3}{5} \right)
\end{align}
$$

or 
$$
\begin{align}
U=\left( \frac{4}{5}, -\frac{3}{5} \right)
\end{align}
$$

### Problem set 1.2
1)
$u\cdot v=-24+24=0$ 
$u\cdot w=-6+16=10$
$v+w=(5,5)$  $u\cdot(v+w)=-30+40=10$
$w\cdot v=10$

2)
$||u||=\sqrt{ u^{2} }=\sqrt{ 100 }=10$
$||v||=\sqrt{ v^{2} }=\sqrt{ 25 }=5$
$||w||=\sqrt{ w^{2} }=\sqrt{ 5 }$

Schwarz inequality
$|u\cdot v|=0<150=||u||||v||$
$|v\cdot w|=10\leq 5\sqrt{ 5 }=||v||||w||$


3)
$\frac{v}{||v||}=\left( \frac{4}{5}, \frac{3}{5} \right)$

$\frac{w}{||w||}=\left( \frac{1}{\sqrt{ 5 }}, \frac{2}{\sqrt{ 5 }} \right)$

$\cos \theta=\frac{10}{5\sqrt{ 5 }}$

$0^\circ$ with w: $a=(2,4)$
$90^\circ$: $b=(-2,1)$ or $b=(2,-1)$
$180^\circ$: $c=(-1,-2)$

4)
a) $v\cdot-v=-(v^{2})=-1$
b) $$
\begin{align}
(v+w)\cdot(v-w)&=v^{2}-vw+vw-w^{2} \\
&=v^{2}-w^{2} \\
&=||v||^{2}-||w||^{2} \\
&=1-1 \\
&=0
\end{align}
$$

#### Distributive law for dot pruduct
Let’s test $(\mathbf{u} + \mathbf{v}) \cdot \mathbf{w}$:

1. **The Sum:** $\mathbf{u} + \mathbf{v} = (u_1 + v_1, u_2 + v_2)$
    
2. **The Dot Product:** $(\mathbf{u} + \mathbf{v}) \cdot \mathbf{w} = (u_1 + v_1)w_1 + (u_2 + v_2)w_2$
    
3. **Distribute the _Scalars_:** Since $u_1, v_1, w_1$ are just regular numbers, we know we can distribute them:
    
    $$u_1w_1 + v_1w_1 + u_2w_2 + v_2w_2$$
    
4. **Rearrange:** Group the $u$ terms and the $v$ terms:
    
    $$(u_1w_1 + u_2w_2) + (v_1w_1 + v_2w_2)$$
    
5. **The Result:** This is exactly $\mathbf{u} \cdot \mathbf{w} + \mathbf{v} \cdot \mathbf{w}$.
    

**The takeaway:** The dot product is distributive because the regular multiplication of the individual coordinates is distributive.

#### The Geometric Proof (The "Shadow" Reason)

Remember the "shadow" (projection) analogy? The dot product is the length of the shadow of one vector onto another.

Imagine you have two vectors, $\mathbf{u}$ and $\mathbf{v}$.

- If you add them together ($\mathbf{u} + \mathbf{v}$), you get a new, longer vector.
    
- The shadow of this **combined** vector onto a third vector $\mathbf{w}$ is exactly equal to the shadow of $\mathbf{u}$ plus the shadow of $\mathbf{v}$ laid end-to-end.
    

Because the "total shadow" is the sum of the "individual shadows," the math stays consistent:

$$(\text{Shadow of } \mathbf{u} + \mathbf{v}) = (\text{Shadow of } \mathbf{u}) + (\text{Shadow of } \mathbf{v})$$


c)
$$
\begin{align}
(v-2w)\cdot(v+2w)&=v^{2}-4w^{2} \\
&=||v||^{2}-4||w||^{2} \\
&=1-4 \\
&=-3
\end{align}
$$

5)
a)
$||v||=\sqrt{ v^{2} }=\sqrt{ 10 }$
$||w||=\sqrt{ w^{2} }=3$

$u_{1}=\left( \frac{1}{\sqrt{ 10 }}, \frac{3}{\sqrt{ 10 }} \right)$  $u_{2}=\left( \frac{2}{3}, \frac{1}{3}, \frac{2}{3} \right)$

$U_{1}=\left( -\frac{3}{\sqrt{ 10 }}, \frac{1}{\sqrt{ 10 }} \right)$

- **One Perpendicular Vector:** $U_{2} = (1, -2, 0)$
    
- **Another Perpendicular Vector:** $U_2 = (0, 2, -1)$ (try the math on this one—it also equals 0!)

6) a)
$w=(1,2)$ $w=(-1,-2)$ $w=(c,2c)$
$w\cdot v=2w_{1}-1w_{2}=0$
$2w_{1}=w_{2}$
Thus, $w=(c,2c)$
One free variable

b) plane
2 free variable
We need to find
$$
x+y+z=0
$$
$x=-y-z$
Thus, $w=(-y+z,y,z)$

c) 
The vectors perpendicular to both (1, 1, 1) and (1, 2, 3) lie on a line.

It because the vectors perpendicular to the vectors $(1,1,1)$ is a plane and also $(1,2,3)$. Thus, the intersection of 2 plane is a line.

7)
a) 
$$
\begin{align}
\cos \theta&= \frac{v\cdot w}{||v||||w||}
\end{align}
$$
$$
\begin{align}
v\cdot w=1
\end{align}
$$

$$
||v||=\sqrt{ v^{2} }=\sqrt{ 4 }=2
$$

$$
\begin{align}
||w||&=\sqrt{ w^{2} }=\sqrt{ 1 }=1
\end{align}
$$

Thus,
$$
\begin{align}
\cos \theta&= \frac{1}{1(2)} \\
&=\frac{1}{2} \\
\theta&=60^\circ 
\end{align}
$$


8)
a) it is false, because $v$ and $w$ can be any vectors
b) It is true. Because any linear combination of $u$ and $v$ lies in the same plane with $u$ and $v$. In other word,

$$
\begin{align}
u \cdot(v+2w)&= (u\cdot v)+(2w\cdot u) \\
&=0
\end{align}
$$
(because $\cos \theta=0$)

c) 
$$
\begin{align}
||u-v||&= \sqrt{ (u-v)^{2} } \\
&=\sqrt{ u^{2}+v^{2} } \\
&=\sqrt{ 1+1 } \\
&=\sqrt{ 2 }
\end{align}
$$

9)
Suppose $\frac{v_{2}w_{2}}{v_{1}w_{1}}=-1$. Then
$$
\begin{align}
v_{2}w_{2}&=-v_{1}w_{1} \\
v_{2}w_{2}+v_{1}w_{1}&=0 \\
v\cdot w&=0
\end{align}
$$

Since $v \cdot w=0$, It follow that $v$ and $w$ are perpendicular

10)
perpendicular

==11)==
$90^\circ<\theta<270^\circ$. Wrong.

This is because the angle between 2 vector only range from $0\leq \theta\leq 180^\circ$. Why? if it exceed $180^\circ$, one can just take the smallest angle which is for example $200^\circ=160^\circ$. And how do we differentiate between $45^\circ$ and $135^\circ$? By the sign of dot product , if dot product <0, then $\theta>90^\circ$ and vice versa.
![[Pasted image 20260410165635.png]]

a and b are conjugate angle and we always choose the smaller one

The key to telling the difference between $45^\circ$ and $135^\circ$ in 3D space isn't just about the lines, but the **direction of the arrows**.

So the $w's$ fill half of the 3-dimensional space.



12)
$$
\begin{align}
(w-cv)\cdot v&=(w_{1}-cv_{1})\cdot v_{1}+(w_{2}-cv_{2})\cdot v_{2} \\
\end{align}
$$

Since they are perpendicular, it follow that their dot product is 0.

$$
\begin{align}
(1-c)\cdot 1+(5-1c)&=0 \\
1-c+5-c&=0 \\
-2c&=-6 \\
c&=3
\end{align}
$$

13)




