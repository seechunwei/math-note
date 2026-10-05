b)
To show $T$ is a linear transformation , we need to how its linearity, for any $x_{1},x_{2} \in \mathbb{P}_{3}(\mathbb{R})$ and any real scalar $k$:

$$
\begin{align}
L_{1}&:T(x_{1}+x_{2})=T(x_{1})+T(x_{2}) \\
L_{2}&:T(kx_{1})=kT(x_{1})
\end{align}
$$



Let us define two arbitrary polynomials in $\mathbb{P}_3(\mathbb{R})$:
$$
x_{1}=x_{1}(t)=a_{1}+b_{1}t+c_{1}t^{2}+d_{1}t^{3}
$$
and
$$
x_{2}=x_{2}(t)=a_{2}+b_{2}t+c_{2}t^{2}+d_{2}t^{3}
$$
 
 First we show for $L_{1}$. Thus, for any $x_{1},x_{2} \in \mathbb{P}_{3}$, we have 

$$
x_{1}+x_{2}=(a_{1}+a_{2})+(b_{1}+b_{2})t+(c_{1}+c_{2})t^{2}+(d_{1}+d_{2})t^{3}
$$


Hence,
$$
\begin{align}
T(x_{1}+x_{2})&= (c_{1}+c_{2})b_{1} \\
&+ (d_{1}+d_{2}+c_{1}+c_{2}-(a_{1}+a_{2}))b_{2}\\
&+(d_{1}+d_{2}+2(c_{1}+c_{2})-(b_{1}+b_{2})-2(a_{1}+a_{2}))b_{3} \\
&+(d_{1}+d_{2}+c_{1}+c_{2}-(b_{1}+b_{2})-(a_{1}+a_{2}))b_{4} \\
\vdots  \\

&=T(x_{1})+T(x_{2})
\end{align}
$$

Regrouping the coefficient:
$$
\begin{align}
T(x_{1}+x_{2})&= \left[ c_{1} + c_{2} \right]b_{1} \\
&\quad + \left[ (d_{1}+c_{1}-a_{1}) + (d_{2}+c_{2}-a_{2}) \right]b_{2} \\
&\quad + \left[ (d_{1}+2c_{1}-b_{1}-2a_{1}) + (d_{2}+2c_{2}-b_{2}-2a_{2}) \right]b_{3} \\
&\quad + \left[ (d_{1}+c_{1}-b_{1}-a_{1}) + (d_{2}+c_{2}-b_{2}-a_{2}) \right]b_{4} \\
\end{align}
$$

Splitting into 2 sum:
$$
\begin{align}
T(x_{1}+x_{2}) &= \left[ c_{1}b_{1} + (d_{1}+c_{1}-a_{1})b_{2} + (d_{1}+2c_{1}-b_{1}-2a_{1})b_{3} + (d_{1}+c_{1}-b_{1}-a_{1})b_{4} \right] \\
&\quad + \left[ c_{2}b_{1} + (d_{2}+c_{2}-a_{2})b_{2} + (d_{2}+2c_{2}-b_{2}-2a_{2})b_{3} + (d_{2}+c_{2}-b_{2}-a_{2})b_{4} \right] \\
\end{align}
$$

Thus,

$$
T(x_{1}+x_{2})=T(x_{1})+T(x_{2})
$$

Second we prove for $L_{2}$.

For any $x_{1} \in \mathbb{P}_{3}$ and any real scalar $k$, we have
$$kx_{1} = (ka_1) + (kb_1)t + (kc_1)t^2 + (kd_1)t^3$$

Apply the transformation $T$ to $kx_{1}$:

$$T(kx_{1}) = (kc_1)b_1 + (kd_1+kc_1-ka_1)b_2 - (kd_1+2kc_1-kb_1-2ka_1)b_3 + (kd_1+kc_1-kb_1-ka_1)b_4$$

Factor out the scalar $k$ from every term:

$$T(kx_{1}) = k \cdot \left[ c_1b_1 + (d_1+c_1-a_1)b_2 - (d_1+2c_1-b_1-2a_1)b_3 + (d_1+c_1-b_1-a_1)b_4 \right]$$

Substitute the definition of $T(x_{1})$ back in:

$$T(kx_{1}) = kT(x_{1})$$

Since $T$ satisfy $L_{1}$ and $L_{2}$, it follow that $T$ is a linear transformation.


---

b)



Notice that

$$
T(x)=\begin{bmatrix}
b_{1} & b_{2} & b_{3} & b_{4}
\end{bmatrix} \begin{bmatrix}
c \\
d+c-a \\
d+c-b-a \\
2a+b-2c-d
\end{bmatrix}
$$

for any $x \in \mathbb{P}_{3}(\mathbb{R})$. 

Notice that we can define $T(x)$ as a composition of 2 linear transformation which is 
$$
T(x)=(L_{2}\circ L_{1})(x)=L_{2}(L_{1}(x))
$$

We define $L_{1}$ as linear transformation where $L_1: \mathbb{P}_3(\mathbb{R}) \rightarrow \mathbb{R}^4$ such that 

$$
L_{1}(x)= \begin{bmatrix}
c \\
d+c-a \\
d+2c-b-2a \\
d+c-b-a
\end{bmatrix}
$$
where 
$$
x=x(t)=a+bt+ct^{2}+dt^{3}
$$
Because every component of the vector $L_1(x)$ is a linear combination of the coefficients $a, b, c,$ and $d$, it can be factored into a standard matrix multiplication:

$$L_1(x) = \begin{bmatrix} 0 & 0 & 1 & 0 \\ -1 & 0 & 1 & 1 \\ -2 & -1 & 2 & 1 \\ -1 & -1 & 1 & 1 \end{bmatrix} \begin{bmatrix} a \\ b \\ c \\ d \end{bmatrix}$$

Since matrix multiplication is inherently a linear transformation from $\mathbb{R}^4 \to \mathbb{R}^4$, and the isomorphism mapping a polynomial to its standard coefficient vector $\begin{bmatrix} a & b & c & d \end{bmatrix}^T$ is also linear, $L_1$ is guaranteed to be linear.



Next, we define a second transformation $L_2: \mathbb{R}^4 \rightarrow \mathbb{P}_3(\mathbb{R})$ such that

$$L_2\left(\begin{bmatrix} a \\ b \\ c \\ d \end{bmatrix}\right) = ab_1 + bb_2 + cb_3 + db_4$$

This is the classic inverse coordinate mapping $[~~]_{\mathcal{B}}^{-1}$, which is by definition a linear transformation.

> [!info] Theorem
The composition of linear transformation is still linear transformation

Since $T=L_{2}\circ L_{1}$ it follow that $T$ is linear transformation.

