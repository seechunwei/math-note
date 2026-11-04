
Linear transformation from vector space $V$ to vector space $W$ ($T:V\to W$) is determine by where it send the basis of $V$ to some vector set of $W$. From [[Linear Transformation of Abstract Vector Spaces#^fceb18]], we know that we can always form a matrix $A$ that represent the linear transformation where each column of $A$ is the destination (image) of each vector in the basis of $V$ under linear map $T$. 

If $V=\mathbb{R}^{n}$ and $W=\mathbb{R}^{n}$ and we choose standard basis of $V$ and $W$, then 
$$
A=\begin{bmatrix}
T(e_{1}) & \dots & T(e_{n})
\end{bmatrix}
$$
which is called standard matrix for $T$. More precisely, it is actually

$$
A= \begin{bmatrix}
[T(e_{1})]_{S} & \dots & [T(e_{n})_{S}]
\end{bmatrix}
$$
where $S=\{ s_{1},s_{2} \}$ is the standard basis for $W$. Why? Because we are mapping the element in $V$ to the element in $W$ with $S$ as representation. (In other word coordinate vector with respect to $S$)

$$
\begin{align}
a&=xe_{1}+ye_{2} \\
T(a)&= xT(e_{1})+yT(e_{2}) \\
[T(a)]_{S}&= x[T(e_{1})]_{S}+y[T(e_{2})]_{S} \\
&= \begin{bmatrix}
[T(e_{1})]_{S} & \dots & [T(e_{n})]_{S} 
\end{bmatrix} \begin{bmatrix}
x \\
y
\end{bmatrix}
\end{align}
$$
In practice we will just ignore the coordinate mapping $S$ if the context is about mapping it into the same vector space (Linear operator). Because usually we will use the same standard basis for domain and codomain since they are the same vector space. 

What if we choose different basis? then we have
![[5.4 Eigenvectors and linear transformation#^e94aa5]]

We didn't write $[T]_{B,B}$ in Lay Book which is kind of confused and not precise. In fact we should write $[T]_{S,S}$ for standard basis.

Note that a finite dimensional vector space have infinitely many basis. Hence, it is very natural to think that we use different basis for $V$ and $W$. Hence, suppose $\alpha=\{ v_{1},\dots,v_{n} \}$ is the basis for $V$ and $\beta=\{ w_{1},\dots,w_{m} \}$. Then

$$
\begin{align}
[T]_{\alpha,\beta}= \begin{bmatrix}
[T(v_{1})]_{\beta} & \dots & [T(v_{n})]_{\beta}
\end{bmatrix}
\end{align}
$$

[[5.4 Eigenvectors and linear transformation#^df6f9b]]

----
# Tutorial 3
a. Using the Theorem, show that there is a unique linear transformation $T : \bar { \mathbb { R } ^ { 2 } } \to \mathbb { R } ^ { 2 }$ for which $T ( 1 , 2 ) = ( 2 , 3 )$ and $T ( 0 , 1 ) = ( 1 , 4 )$ 

b. Find a formula for $T \ : \mathrm { i . e }$ find $T ( a , b )$ 

### Approach 1: Vector Form (Finding Coordinates by Hand)
How to find the formula? 
First we need to express arbitrary vector in $\mathbb{R}^{2}$ in term of the basis $\{ (1,2),(0,1) \}$ because $T$ is defined when it send the basis.

$$
\begin{align}
(a,b)&= c_{1}(1,2)+c_{2}(0,1)
\end{align}
$$

This step is equal to find the coordinate vector of $(a,b)$ with respect to basis $\{ (1,2),(0,1) \}$. We can get what is $c_{1},c_{2}$ by solving the system, but in this case we know $c_{1}=a$ and $c_{2}+2c_{1}=b\implies c_{2}+2a=b\implies c_{2}=b-2a$.

$$
\begin{align}
(a,b)&=a(1,2)+(b-2a)(0,1) \\
T(a,b)&= aT(1,2)+(b-2a)T(0,1) \\
&=a(2,3)+(b-2a)(1,4) \\
&= (b,-5a+4b)
\end{align}
$$

### Approach 2: Matrix Form (Standard Matrix Equation)
Instead of solving for coordinates vector-by-vector, we find the standard matrix $A$ directly such that $T(x) = Ax$ for all $x \in \mathbb{R}^2$.

Since $T(v_1) = A v_1$ and $T(v_2) = A v_2$, we bundle them column-by-column into a single matrix equation:

$$
A \begin{bmatrix} v_1 & v_2 \end{bmatrix} = \begin{bmatrix} T(v_1) & T(v_2) \end{bmatrix}
$$

Multiplying on the right by the inverse matrix $\begin{bmatrix} v_1 & v_2 \end{bmatrix}^{-1}$:

$$
A = \begin{bmatrix} T(v_1) & T(v_2) \end{bmatrix} \begin{bmatrix} v_1 & v_2 \end{bmatrix}^{-1}
$$

Substitute the given basis vectors $v_1 = \begin{bmatrix} 1 \\ 2 \end{bmatrix}, v_2 = \begin{bmatrix} 0 \\ 1 \end{bmatrix}$ and target images $T(v_1) = \begin{bmatrix} 2 \\ 3 \end{bmatrix}, T(v_2) = \begin{bmatrix} 1 \\ 4 \end{bmatrix}$:

$$
\begin{aligned}
A &= \begin{bmatrix} 2 & 1 \\ 3 & 4 \end{bmatrix} \begin{bmatrix} 1 & 0 \\ 2 & 1 \end{bmatrix}^{-1} \\
&= \begin{bmatrix} 2 & 1 \\ 3 & 4 \end{bmatrix} \begin{bmatrix} 1 & 0 \\ -2 & 1 \end{bmatrix} \\
&= \begin{bmatrix} 0 & 1 \\ -5 & 4 \end{bmatrix}
\end{aligned}
$$

Now evaluate the transformation for any arbitrary vector $\begin{bmatrix} a \\ b \end{bmatrix}$:

$$
T\begin{pmatrix} \begin{bmatrix} a \\ b \end{bmatrix} \end{pmatrix} = \begin{bmatrix} 0 & 1 \\ -5 & 4 \end{bmatrix} \begin{bmatrix} a \\ b \end{bmatrix} = \begin{bmatrix} b \\ -5a + 4b \end{bmatrix}
$$

---

### Comparison & Corresponding Steps

Both approaches perform the **exact same operations**, but package the sequence differently:

| Step                      | Approach 1 (Vector / Hand Solving)                                                                               | Approach 2 (Matrix Inverse)                                                                                                                                                     | Mathematical Meaning                                                      |
| :------------------------ | :--------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | :------------------------------------------------------------------------ |
| **1. Find Coordinates**   | Solve system by hand: $c_1 = a$, $c_2 = b - 2a$                                                                  | $\begin{bmatrix} c_1 \\ c_2 \end{bmatrix} = \begin{bmatrix} 1 & 0 \\ 2 & 1 \end{bmatrix}^{-1} \begin{bmatrix} a \\ b \end{bmatrix} = \begin{bmatrix} a \\ b - 2a \end{bmatrix}$ | Computing coordinate vector $[x]_B = P^{-1}x$                             |
| **2. Combine Images**     | $c_1 T(v_1) + c_2 T(v_2) = a \begin{bmatrix} 2 \\ 3 \end{bmatrix} + (b-2a) \begin{bmatrix} 1 \\ 4 \end{bmatrix}$ | $\begin{bmatrix} T(v_1) & T(v_2) \end{bmatrix} \begin{bmatrix} c_1 \\ c_2 \end{bmatrix}$                                                                                        | Linear combination of column images                                       |
| **3. Compound Execution** | Carried out on demand for vector $(a, b)$.                                                                       | Multiplies $[T(B)] [B]^{-1}$ *up front* to form matrix $A$.                                                                                                                     | Pre-compounding the two steps into a single operator $A = [T(B)] P^{-1}$. |




