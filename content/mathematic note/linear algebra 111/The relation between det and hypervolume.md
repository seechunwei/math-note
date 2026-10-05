
See exercise 43 at section 3.1

From the question we know that the determinant for a $2\times 2$ matrix is the area of parallelogram formed by its column vectors. 

Suppose a $2\times 2$ matrix $A$ where each column of $A$ represent a vector in $\mathbb{R}^{2}$.

$$
A=\begin{bmatrix}
1 & 0 \\
0 & 1 \\
\end{bmatrix}
$$

Thus, $A$ is a square in cartesian plane. Suppose the row operation $R^{1}_{2}(k)$ represented by $E^{1}_{2}(k)$ . Thus,

$$
E^{1}_{2}(k)A=\begin{bmatrix}
1 &  0\\
k & 1
\end{bmatrix}
$$
is a parallelogram after vertical shearing by k unit.  

![[Pasted image 20260517164141.png]]

Notice that the area doesn't change since the vertical length and horizontal length remain unchanged. Thus, 

$$
|E^{1}_{2}(k)A|=
|A|
$$

Thus, we can generalize this concept to $n\times n$ matrix where each column is a vector in $\mathbb{R}^{n}$.

In linear algebra, the absolute value of the determinant of an $n \times n$ matrix is the **hypervolume** of the $n$-dimensional parallelepiped (the multi-dimensional version of a parallelogram) formed by its column vectors.

#### Key Properties that Generalize:

- **Expansion/Contraction:** If you multiply one vector by a scalar $k$, the hypervolume is multiplied by $|k|$.
    
- **Linear Dependence:** If the vectors are linearly dependent (meaning one vector lies in the "span" of the others), the parallelepiped is "squashed" flat in at least one dimension. Its $n$-dimensional volume becomes **0**, which matches the fact that the determinant of a linearly dependent matrix is 0.
    
- **Orientation:** The determinant actually provides a **signed volume**. A positive determinant means the vectors follow the "right-hand rule" orientation, while a negative determinant means the orientation has been flipped (like a mirror image).

==Jacobian determinant==

---

We can use this concept to see Cramer rule

Let $A$ be an invertible $n\times n$ matrix. For any $b \in \mathbb{R}^{n}$, the unique solution $x$ of $Ax=b$ has entries given by

$$x_i = \frac{\det(A_i(\mathbf{b}))}{\det(A)}$$
where $i=1,2,\dots,n$

$A_{i}(b)$ is the matrix obtained from $A$ by replacing column $i$ by the vector $b$.

$$
A_{i}(b)=\begin{bmatrix}
a_{1} & \dots & b & \dots & a_{n}
\end{bmatrix}
$$

A very natural question is what operation bring $A$ to $A_{i}(b)$. It only change the column which implies that it is a right multiplication, since the other column remain unchanged, thus it is a right multiplication with identity matrix where $ith$ column is different.

Since 
$$
x_{1}a_{1}+\dots+x_{n}a_{n}=b
$$

it follow that
$$
A\begin{bmatrix}
x_{1} \\
\dots \\
x_{n}
\end{bmatrix}=b
$$
Thus, the identity matrix with $ith$ column different is $(2\times 2)$  

$$I_2(\mathbf{x}) = \begin{bmatrix} 1 & x_1 & 0 \\ 0 & x_2 & 0 \\ 0 & x_3 & 1 \end{bmatrix}$$


Proof:

$$
\begin{align}
A(I_{i}(x))&=A\begin{bmatrix}
e_{1} & \dots & x & \dots & e_{n} \\
\end{bmatrix} \\
&=\begin{bmatrix}
Ae_{1} & \dots & Ax & \dots & Ax_{n}
\end{bmatrix} \\
&=\begin{bmatrix}
a_{1} & \dots & b & \dots & a_{n}
\end{bmatrix} \\
&=A_{i}(b)
\end{align}
$$

By theorem

$$
\det A_{i}(b)=(\det A)(\det I_{i}(x))
$$

$\det I_{i}(x)=x_{i}$ by cofactor expansion across $ith$ row. Hence,

$$
\begin{align}
(\det A)x_{i}&=\det A_{i}(b) \\
x_{i}&= \frac{\det A_{i}(b)}{\det A}
\end{align}
$$

---
### Intuitive way to understand Cramer's rule^123

^760b50

Remember that determinant is the hypervolume of the $n$-dimensional parallelepiped. 

We can view a matrix $A$ as a transformation that turns a unit cube into a slanted $n-$ dimensional box.

When we solve $A\mathbf{x} = \mathbf{b}$, we are looking for the coordinates $(x_1, x_2, \dots, x_n)$ that scale the columns of $A$ to reach the target vector $\mathbf{b}$. Cramer's Rule tells us that:

> The $i$-th coordinate of the solution is simply the ratio of two volumes.


==Remark==
The word scale is the key word to imagine what the $x$ does to the column of $A$.
[[1.9 The Matrix of a Linear Transformation#^0b3e70]]


By replacing the $ith$ column with $b$, we are creating a new box. What happen to the volume of the box?

To see why $x_i$ acts as a "height" or scaling factor, it helps to look at how $\mathbf{b}$ is constructed and how the determinant reacts to it.

Consider we are in 2D with a matrix $A=\begin{bmatrix}a_{1} & a_{2}\end{bmatrix}$ where $a_{1},a_{2} \in \mathbb{R}^{2}$ .We want to solve $Ax=b$, which means 
$$
b=x_{1}a_{1}+x_{2}a_{2}
$$

When we calculate $\det(A_{1}(b))$, we are finding the area of the parallelogram formed by $b$ and $a_{2}$

$$
Area(b,a_{2})=Area(x_{1}a_{1}+x_{2}a_{2},a_{2})
$$

Because the determinant is linear in each column 

$$
Area(b,a_{2})=Area(x_{1}a_{1},a_{2})+Area(x_{2}a_{2},a_{2})
$$

Look at the second term: $\text{Area}(x_2\mathbf{a}_2, \mathbf{a}_2)$. Since both vectors are in the same direction, they form a "flat" parallelogram with **zero area**.

Now look at the first term: $\text{Area}(x_1\mathbf{a}_1, \mathbf{a}_2)$. We can pull the scalar $x_1$ out:

$$\text{Area}(x_1\mathbf{a}_1, \mathbf{a}_2) = x_1 \cdot \text{Area}(\mathbf{a}_1, \mathbf{a}_2)$$

So, the area of the "new" box is just the **original area** scaled by $x_1$.

### 3. The "Height" Metaphor

In geometry, the volume of a parallelepiped is:

$$\text{Volume} = \text{Area of Base} \times \text{Perpendicular Height}$$

If we are looking for $x_i$, we can think of all the _other_ vectors ($j \neq i$) as forming the "Base."

- Any component of $\mathbf{b}$ that is a linear combination of those other vectors ($x_j\mathbf{a}_j$) stays within that base. This is a **shear**, and as we discussed with the $x$ variable earlier, shearing does not change volume.
    
- The only part of $\mathbf{b}$ that moves "up" away from that base is the $x_i\mathbf{a}_i$ component.
    

By replacing $\mathbf{a}_i$ with $\mathbf{b}$, you are essentially saying: "I don't care about the parts of $\mathbf{b}$ that are sliding parallel to the floor; I only want to measure how much $\mathbf{b}$ reaches in the direction of $\mathbf{a}_i$."

1. Dividing the "New Volume" by the "Original Volume" cancels out the base measurements, leaving you with only the scaling factor $x_i$.
    

$$\frac{\text{Volume}(\text{Base} \dots x_i\mathbf{a}_i)}{\text{Volume}(\text{Base} \dots \mathbf{a}_i)} = \frac{x_i \cdot \text{Volume}(\text{Base} \dots \mathbf{a}_i)}{\text{Volume}(\text{Base} \dots \mathbf{a}_i)} = x_i$$

notice that $ith$ column under changed reveal $x_{i}$. Because all the vector $(i\neq j)$ form the base.


==Remark==
Cramer's Rule give us formula for the solution $Ax=b$ for given $b$.