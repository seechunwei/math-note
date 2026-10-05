
Consider the region $S$ that lies between two curves, $y=f(x)$ and $y=g(x)$ and between the line $x=a$ and $x=b$ where $f(x)\geq g(x)$ for all $x \in[a,b]$.

![[Pasted image 20260624214828.png]]

How to get the area between this 2 curve?

Notice that there are 4 condition 
1) $f(x)\geq 0$ and $g(x)\geq 0$ 
Then, the area is simply the Riemann sum of $f(x)$ minus the Riemann sum of $g(x)$. 

2) $f(x)\geq 0$ and $g(x)\leq 0$
Then, the Riemann sum of $g(x)$ is negative. Thus, to take the absolute value of the Riemann sum, we take the Riemann Sum of $f(x)$ minus the Riemann sum of $g(x)$.

3) $f(x)\leq 0$ and $g(x)\leq 0$
Then try to reflect it on x-axis, thus it is - Riemann sum of $g(x)$ - (-) Riemann sum of $f(x)$. Thus, it is Riemann sum of $f(x)$ minus Riemann sum of $g(x)$.

Thus, we have following formula rule

> [!NOTE]
> The area $A$ of the region bounded by curves $y=f(x)$, $y=g(x)$, and the lines $x=a$, $x=b$, where $f$ and $g$ are continuous and $f(x)\geq g(x)$ for all $x$ in $[a,b]$ is
> 
> $$
> A= \int_{a}^{b} [f(x)-g(x)] \, dx 
> $$


What if $f(x)\geq g(x)$ for certain interval and $g(x)\geq f(x)$ for certain interval?, then we have the following formula

$$
|f(x)-g(x)|=\begin{cases}
f(x)-g(x)&when~f(x)\geq g(x) \\
g(x)-f(x)&when~g(x)\geq f(x)
\end{cases}
$$


> [!NOTE]
> The area between the curves $y=f(x)$ and $y=g(x)$ and between $x=a$ and $x=b$ is
> 
> $$
> A=\int_{a}^{b} |f(x)-g(x)| \, dx 
> $$

> [!remark]
> Notice that the absolute value is not outside the integral so it is wrong that calculating the integral and then take its absolute value (In this case we will get the absolute value of net change)
> 
> In fact we might need to split the integral into different interval where $f(x)\geq g(x)$ or $g(x)\geq f(x)$.

For example
Find the area of the region bounded by the curves $y=\sin x$ and $y=\cos x$, $x=0$ and $x= \frac{\pi}{2}$.

$$
\begin{align}
A&= \int_{0}^{\pi/4} \cos x-\sin x \, dx + \int_{\frac{\pi}{4}}^{\pi/2}\sin x-\cos x  \, dx 
\end{align}
$$

![[Pasted image 20260624222353.png]]

Notice that it is symmetric about $x=\frac{\pi}{4}$, thus

$$
A=2 \int_{0}^{\pi/4}(\cos x-\sin x)  \, dx 
$$

Some regions are best treated by regarding x as a function of y. If a region is bounded by curves with equations
$x=f(y),x=g(y),y=c,y=d$ for $c\leq y\leq d$. Then its area is

$$
A=\int_{c}^{d} [f(y)-g(y)] \, dx 
$$

![[Pasted image 20260624222742.png]]