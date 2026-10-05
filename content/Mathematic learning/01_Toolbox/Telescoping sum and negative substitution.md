
> [!tool]
> Telescoping sum is a sum where we can always cancel the middle term when we expand the summation. 

For example,

$$
(x-y)(x^{2}+xy+y^{2})=x(x^{2}+xy+y^{2})-y(x^{2}+xy+y^{2})
$$

Notice that $x(xy)-y(xy)=0$ and $x(y^{2})-y(x^{2})=0$. Thus, it only left with $x^{3}-y^{3}$. It is the same for $x^{n}-y^{n}$.

Now look at the example below (Geometric series):

$$
\begin{align}
S_{n}&=a+ar+\dots+ar^{n-1} \\
rS_{n}&=ar+ar^{2}+\dots+ar^{n} \\
rS_{n}-S_{n}&=a+ar^{n} &&\text{(The middle term collapse)} \\
S_{n}(r-1)&=a+ar^{n} \\
S_{n}&=\frac{a+ar^{n}}{r-1}
\end{align}
$$


> [!question] So what is the trigger?
> We can use this when a series is multiply with a binary term with opposite sign like $(x-y)$ and the middle term is the multiple of these 2 term. And the series shift systematically (like add one degree of x and decrease 1 degree of y)
>
>Or when we have $(x+y)$ and a alternating sign of series. Look at the example below.

Consider
$$
\begin{align}
(x+y)(x^{n-1}-x^{n-2}y+x^{n-3}y^{2}+\dots-xy^{n-2}+y^{n-1})
\end{align}
$$

$x(-x^{n-2}y)+y(xy^{n-2})=0$ so do other middle term that will collapse to 0.


> [!tool] Negative substitution
> When we prove something about $c+a$, we can always prove the negative version by substitute $a=-b$ and vice versa when the operation include preserve the sign. For example $(-a)^{3}=a^{3}$

For example we can prove $x^{n}+y^{n}$ when $n$ is odd using $x^{n}-y^{n}$. 

[[Problem Chapter 1 Basic Properties of Number#^ee071a]]


But subtraction is not always the same as addition. For example addition is commutative but subtraction is not commutative. And also $P$ (the set of positive number) is not closed under subtraction but it is closed under addition.