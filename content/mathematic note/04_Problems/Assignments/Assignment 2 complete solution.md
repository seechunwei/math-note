
### 1)

Given that:

$$A = \begin{bmatrix} -1 & -3 & 1 \\ -2 & 2 & -2 \\ 2 & -2 & 0 \\ 4 & 0 & -2 \end{bmatrix}$$

We need to make sure that the columns of $A$ are linearly independent.
$$\begin{aligned}
\begin{bmatrix} -1 & -3 & 1 \\ -2 & 2 & -2 \\ 2 & -2 & 0 \\ 4 & 0 & -2 \end{bmatrix} 
&\xrightarrow{R_{1}(-1)} \begin{bmatrix} 1 & 3 & -1 \\ -2 & 2 & -2 \\ 2 & -2 & 0 \\ 4 & 0 & -2 \end{bmatrix} \\
&\xrightarrow{\begin{matrix} R_{2}^{1}(2) \\ R_{3}^{1}(-2) \\ R_{4}^{1}(-4) \end{matrix}} \begin{bmatrix} 1 & 3 & -1 \\ 0 & 8 & -4 \\ 0 & -8 & 2 \\ 0 & -12 & 2 \end{bmatrix} \\
&\xrightarrow{R_{2}\left( \frac{1}{8} \right)} \begin{bmatrix} 1 & 3 & -1 \\ 0 & 1 & -1/2 \\ 0 & -8 & 2 \\ 0 & -12 & 2 \end{bmatrix} \\
&\xrightarrow{\begin{matrix} R_{3}^{2}(8) \\ R_{4}^{2}(12) \end{matrix}} \begin{bmatrix} 1 & 3 & -1 \\ 0 & 1 & -1/2 \\ 0 & 0 & -2 \\ 0 & 0 & -4 \end{bmatrix} \\
&\xrightarrow{R_{4}^{3}(-2)} \begin{bmatrix} 1 & 3 & -1 \\ 0 & 1 & -1/2 \\ 0 & 0 & -2 \\ 0 & 0 & 0 \end{bmatrix}
\end{aligned}$$
(3 pivots for 3 columns), so columns of $A$ are linearly independent.

Based on the QR Factorization Theorem (page 403), $A$ is a $4 \times 3$ matrix with linearly independent columns, then $A$ can be factored as $A = QR$ where $Q$ is a $4 \times 3$ matrix whose columns form an orthonormal basis for $\text{Col } A$ and $R$ is a $3 \times 3$ upper triangular invertible matrix with positive entries on its diagonal.

<div class="page-break" style="page-break-before: always;"></div>

### We apply the Gram-Schmidt process to the columns of $A$:

$$A = \begin{bmatrix} x_1 & x_2 & x_3 \end{bmatrix} \quad \text{where} \quad x_1 = \begin{bmatrix} -1 \\ -2 \\ 2 \\ 4 \end{bmatrix}, \; x_2 = \begin{bmatrix} -3 \\ 2 \\ -2 \\ 0 \end{bmatrix}, \; x_3 = \begin{bmatrix} 1 \\ -2 \\ 0 \\ -2 \end{bmatrix}$$

#### ① Find $u_1$

$$v_1 = x_1 = \begin{bmatrix} -1 \\ -2 \\ 2 \\ 4 \end{bmatrix}$$

$$\|v_1\| = \sqrt{(-1)^2 + (-2)^2 + 2^2 + 4^2} = 5$$

$$u_1 = \frac{1}{\|v_1\|}v_1 = \frac{1}{5}\begin{bmatrix} -1 \\ -2 \\ 2 \\ 4 \end{bmatrix} = \begin{bmatrix} -1/5 \\ -2/5 \\ 2/5 \\ 4/5 \end{bmatrix}$$



#### ② Find $u_2$

$$v_2 = x_2 - \frac{x_2 \cdot v_1}{v_1 \cdot v_1}v_1$$

$$x_2 \cdot v_1 = (-3)(-1) + (2)(-2) + (-2)(2) + (0)(4) = -5$$

$$v_1 \cdot v_1 = \|v_1\|^2 = 25$$

$$v_2 = \begin{bmatrix} -3 \\ 2 \\ -2 \\ 0 \end{bmatrix} - \left(\frac{-5}{25}\right)\begin{bmatrix} -1 \\ -2 \\ 2 \\ 4 \end{bmatrix} = \begin{bmatrix} -16/5 \\ 8/5 \\ -8/5 \\ 4/5 \end{bmatrix}$$

We multiply $v_2$ with $\frac{5}{4}$ to simplify the arithmetic:

$$v_2' = \frac{5}{4} \begin{bmatrix} -16/5 \\ 8/5 \\ -8/5 \\ 4/5 \end{bmatrix} = \begin{bmatrix} -4 \\ 2 \\ -2 \\ 1 \end{bmatrix}$$

$$\|v_2'\| = \sqrt{(-4)^2 + 2^2 + (-2)^2 + 1^2} = 5$$

$$u_2 = \frac{v_2'}{\|v_2'\|} = \frac{1}{5}\begin{bmatrix} -4 \\ 2 \\ -2 \\ 1 \end{bmatrix} = \begin{bmatrix} -4/5 \\ 2/5 \\ -2/5 \\ 1/5 \end{bmatrix}$$
<div class="page-break" style="page-break-before: always;"></div>

#### ③ Find $u_3$

$$v_3 = x_3 - \frac{x_3 \cdot v_1}{v_1 \cdot v_1}v_1 - \frac{x_3 \cdot v_2'}{v_2' \cdot v_2'}v_2'$$

> [!info]
$$x_3 \cdot v_1 = \begin{bmatrix} 1 & -2 & 0 & -2 \end{bmatrix} \begin{bmatrix} -1 \\ -2 \\ 2 \\ 4 \end{bmatrix} = -5$$
>
>$$v_{1}\cdot v_{1}=25$$
>
>$$x_3 \cdot v_2' = \begin{bmatrix} 1 & -2 & 0 & -2 \end{bmatrix} \begin{bmatrix} -4 \\ 2 \\ -2 \\ 1 \end{bmatrix} = -10$$
>
>$$v_2' \cdot v_2' = \|v_2'\|^2 = 25$$


Thus,
$$v_3 = \begin{bmatrix} 1 \\ -2 \\ 0 \\ -2 \end{bmatrix} - \left(\frac{-5}{25}\right)\begin{bmatrix} -1 \\ -2 \\ 2 \\ 4 \end{bmatrix} - \left(\frac{-10}{25}\right)\begin{bmatrix} -4 \\ 2 \\ -2 \\ 1 \end{bmatrix}$$

$$v_3 = \begin{bmatrix} -4/5 \\ -8/5 \\ -2/5 \\ -4/5 \end{bmatrix}$$


We multiply with $\frac{5}{2}$ to simplify the arithmetic:

$$v_3' = \frac{5}{2}\begin{bmatrix} -4/5 \\ -8/5 \\ -2/5 \\ -4/5 \end{bmatrix} = \begin{bmatrix} -2 \\ -4 \\ -1 \\ -2 \end{bmatrix}$$

$$\|v_3'\| = \sqrt{(-2)^2 + (-4)^2 + (-1)^2 + (-2)^2} = 5$$

$$u_3 = \frac{v_3'}{\|v_3'\|} = \frac{1}{5}\begin{bmatrix} -2 \\ -4 \\ -1 \\ -2 \end{bmatrix} = \begin{bmatrix} -2/5 \\ -4/5 \\ -1/5 \\ -2/5 \end{bmatrix}$$
<div class="page-break" style="page-break-before: always;"></div>

### To form $Q$, 

$Q = [u_1, u_2, u_3]$

The columns of $Q$ are orthonormal.

$$Q = \begin{bmatrix} -1/5 & -4/5 & -2/5 \\ -2/5 & 2/5 & -4/5 \\ 2/5 & -2/5 & -1/5 \\ 4/5 & 1/5 & -2/5 \end{bmatrix}$$

### To find R

Since $Q^T Q = I$

Thus, $Q^T A = Q^T(QR) = (Q^T Q)R = IR = R$

$$R = Q^T A$$

$$\begin{align}
R &= \begin{bmatrix} -1/5 & -2/5 & 2/5 & 4/5 \\ -4/5 & 2/5 & -2/5 & 1/5 \\ -2/5 & -4/5 & -1/5 & -2/5 \end{bmatrix} \begin{bmatrix} -1 & -3 & 1 \\ -2 & 2 & -2 \\ 2 & -2 & 0 \\ 4 & 0 & -2 \end{bmatrix} \\
&= \begin{bmatrix} 5 & -1 & -1 \\ 0 & 4 & -2 \\ 0 & 0 & 2 \end{bmatrix}
\end{align}$$


Therefore, $A = QR$ with

$$Q = \begin{bmatrix} -1/5 & -4/5 & -2/5 \\ -2/5 & 2/5 & -4/5 \\ 2/5 & -2/5 & -1/5 \\ 4/5 & 1/5 & -2/5 \end{bmatrix}$$

and

$$R = \begin{bmatrix} 5 & -1 & -1 \\ 0 & 4 & -2 \\ 0 & 0 & 2 \end{bmatrix}$$

---
<div class="page-break" style="page-break-before: always;"></div>

### 2)a)

The standard basis for $\mathbb{P}_{3}(\mathbb{R})$ is $S=\{ 1,t,t^{2},t^{3} \}$

Thus, for any $p \in \mathbb{P}_{3}(\mathbb{R})$ such that
$p=P(t)=a+bt+cd^{2}+dt^{3}$

we define a coordinate mapping $[~~]_{S}$ such that for any $p \in \mathbb{P}_{3}$,

$$
[p]_{S}= \begin{bmatrix}
a \\
b \\
c \\
d
\end{bmatrix}
$$
where $[p]_{S} \in \mathbb{R}^{4}$. Thus, the polynomial in set $A$ and $B$ can be map to a coordinate vector relative to $S$ under the coordinate mapping $[~~]_{S}$ such that

$$
A= \left\{  \begin{bmatrix}
1 \\
0 \\
1 \\
0
\end{bmatrix} ,\begin{bmatrix}
0 \\
1 \\
0 \\
1
\end{bmatrix}, \begin{bmatrix}
1 \\
-1 \\
0 \\
1
\end{bmatrix} , \begin{bmatrix}
1 \\
0 \\
0 \\
1
\end{bmatrix} \right\}
$$
and

$$
B= \left\{  \begin{bmatrix}
1 \\
1 \\
1 \\
1
\end{bmatrix}, \begin{bmatrix}
1 \\
0 \\
0 \\
-1
\end{bmatrix} , \begin{bmatrix}
0 \\
1 \\
0 \\
0
\end{bmatrix}, \begin{bmatrix}
0 \\
0 \\
1 \\
0
\end{bmatrix} \right\}
$$

Given that for $x=a+bt+ct^{2}+dt^{3}$ ,

$$
\begin{align}
x&= \begin{bmatrix}
b_{1} & b_{2} & b_{3} & b_{4}
\end{bmatrix}\begin{bmatrix}
\frac{1}{2}(a+d) \\
\frac{1}{2}(a-d) \\
-\frac{1}{2}(a-2b+d) \\
-\frac{1}{2}(a-2c+d)
\end{bmatrix}
\end{align}
$$

Notice that $P_{S\leftarrow B}=\begin{bmatrix}b_{1} & b_{2} & b_{3} & b_{4}\end{bmatrix}$ such that

$$
x=P_{S\leftarrow B}[x]_{B}
$$
<div class="page-break" style="page-break-before: always;"></div>

Thus,

$$
\begin{align}
[x]_{B}&= \begin{bmatrix}
\frac{1}{2}(a+d) \\
\frac{1}{2}(a-d) \\
-\frac{1}{2}(a-2b+d) \\
-\frac{1}{2}(a-2c+d)
\end{bmatrix} \\
&=a \begin{bmatrix}
\frac{1}{2} \\
\frac{1}{2} \\
-\frac{1}{2} \\
-\frac{1}{2}
\end{bmatrix}+b\begin{bmatrix}
0 \\
0 \\
1 \\
0
\end{bmatrix}+ c \begin{bmatrix}
0 \\
0 \\
0 \\
1
\end{bmatrix}+d \begin{bmatrix}
\frac{1}{2} \\
-\frac{1}{2} \\
-\frac{1}{2}\\
-\frac{1}{2}
\end{bmatrix} \\
&= \begin{bmatrix}
\frac{1}{2} & 0 & 0 & \frac{1}{2 \\
} \\
\frac{1}{2} & 0 & 0 & -\frac{1}{2}  \\
-\frac{1}{2} & 1 & 0 & -\frac{1}{2} \\
-\frac{1}{2} & 0 & 1 & -\frac{1}{2}
\end{bmatrix} \begin{bmatrix}
a \\
b \\
c \\
d
\end{bmatrix}
\end{align}
$$

Thus,

$$
P_{B\leftarrow S}= \begin{bmatrix}
\frac{1}{2} & 0 & 0 & \frac{1}{2 \\
} \\
\frac{1}{2} & 0 & 0 & -\frac{1}{2}  \\
-\frac{1}{2} & 1 & 0 & -\frac{1}{2} \\
-\frac{1}{2} & 0 & 1 & -\frac{1}{2}
\end{bmatrix}
$$
such that

$$
[x]_{B}=P_{B\leftarrow S}(x)
$$


We want to find $P_{B\leftarrow A}$, such that

$$P_{\mathcal{B} \leftarrow \mathcal{A}} = \begin{bmatrix} [a_1]_{\mathcal{B}} & [a_2]_{\mathcal{B}} & [a_3]_{\mathcal{B}} & [a_4]_{\mathcal{B}} \end{bmatrix}$$
(By Theorem 15 page 275)

Thus, we define a coordinate mapping $[~~]_{B}$ for any $x \in \mathbb{R}^{4}$ such that

$$
[x]_{B}=P_{B\leftarrow S}(x)
$$

Hence, 
$$
\begin{align}
[a_{1}]_{B}&= P_{B\leftarrow S}(a_{1}) \\
&= \begin{bmatrix}
\frac{1}{2} & 0 & 0 & \frac{1}{2 \\
} \\
\frac{1}{2} & 0 & 0 & -\frac{1}{2}  \\
-\frac{1}{2} & 1 & 0 & -\frac{1}{2} \\
-\frac{1}{2} & 0 & 1 & -\frac{1}{2}
\end{bmatrix} \begin{bmatrix}
1 \\
0 \\
1 \\
0
\end{bmatrix} \\
&=\begin{bmatrix}
\frac{1}{2} \\
\frac{1}{2} \\
-\frac{1}{2} \\
\frac{1}{2}
\end{bmatrix}
\end{align}
$$
$$
\begin{align}
[a_{2}]_{B}&=P_{B\leftarrow S}(a_{1}) \\
&= \begin{bmatrix}
\frac{1}{2} & 0 & 0 & \frac{1}{2 \\
} \\
\frac{1}{2} & 0 & 0 & -\frac{1}{2}  \\
-\frac{1}{2} & 1 & 0 & -\frac{1}{2} \\
-\frac{1}{2} & 0 & 1 & -\frac{1}{2}
\end{bmatrix} \begin{bmatrix}
0 \\
1 \\
0 \\
1
\end{bmatrix}  \\
&= \begin{bmatrix}
\frac{1}{2} \\
-\frac{1}{2} \\
\frac{1}{2} \\
-\frac{1}{2}
\end{bmatrix}
\end{align}
$$
$$
\begin{align}
[a_{3}]_{B}&=P_{B\leftarrow S}(a_{3}) \\
&=  \begin{bmatrix}
\frac{1}{2} & 0 & 0 & \frac{1}{2 \\
} \\
\frac{1}{2} & 0 & 0 & -\frac{1}{2}  \\
-\frac{1}{2} & 1 & 0 & -\frac{1}{2} \\
-\frac{1}{2} & 0 & 1 & -\frac{1}{2}
\end{bmatrix} \begin{bmatrix}
1 \\
-1 \\
0 \\
1
\end{bmatrix}   \\
&=\begin{bmatrix}
1 \\
0 \\
-2 \\
-1
\end{bmatrix}
\end{align}
$$

$$
\begin{align}
[a_{4}]_{B}&=P_{B\leftarrow S}(a_{4}) \\
&= \begin{bmatrix}
\frac{1}{2} & 0 & 0 & \frac{1}{2 \\
} \\
\frac{1}{2} & 0 & 0 & -\frac{1}{2}  \\
-\frac{1}{2} & 1 & 0 & -\frac{1}{2} \\
-\frac{1}{2} & 0 & 1 & -\frac{1}{2}
\end{bmatrix} \begin{bmatrix}
1 \\
0 \\
0 \\
1
\end{bmatrix} \\
&= \begin{bmatrix}
1 \\
0 \\
-1 \\
-1
\end{bmatrix} 
\end{align}
$$

Thus,


$$\begin{align}
P_{\mathcal{B} \leftarrow \mathcal{A}} &= \begin{bmatrix} [a_1]_{\mathcal{B}} & [a_2]_{\mathcal{B}} & [a_3]_{\mathcal{B}} & [a_4]_{\mathcal{B}} \end{bmatrix} \\
&= \begin{bmatrix}
\frac{1}{2} & \frac{1}{2} & 1 & 1 \\
\frac{1}{2} & -\frac{1}{2} & 0 & 0 \\
-\frac{1}{2} & \frac{1}{2} & -2 & -1 \\
\frac{1}{2} & -\frac{1}{2} & -1 & -1
\end{bmatrix}
\end{align}$$



---
<div class="page-break" style="page-break-before: always;"></div>

### 2)b)

To show $T$ is a linear transformation , we need to how its linearity, for any $x_{1},x_{2} \in \mathbb{P}_{3}(\mathbb{R})$ and any real scalar $k$:

$$
\begin{align}
L_{1}&:T(x_{1}+x_{2})=T(x_{1})+T(x_{2}) \\
L_{2}&:T(kx_{1})=kT(x_{1})
\end{align}
$$
(by Definition of linear transformation page 94)


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
<div class="page-break" style="page-break-before: always;"></div>

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
