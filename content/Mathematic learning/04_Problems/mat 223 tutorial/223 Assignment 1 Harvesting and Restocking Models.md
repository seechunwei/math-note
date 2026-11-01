
$$
f(y)= \frac{dy}{dt}= ry\left( 1- \frac{y}{K} \right)-h
$$

a) Analyze this fishery model for $h < \frac { r K } { 4 }$ to show that the equation (1) has two steady-states, $y _ { 1 }$ and $y _ { 2 }$ , with $y _ { 1 } < y _ { 2 }$ . Calculate these steady states. (C4: 2 Marks) 

Let $\frac{dy}{dt}=0$:

$$
\begin{align}
ry\left( 1-\frac{y}{K} \right)-h&=0 \\
ry- \frac{r}{K}y^{2}-h&=0 \\
-\frac{r}{K}y^{2}+ry-h&=0
\end{align}
$$

Note this is a quadratic equation with $y$ as variable. When $h< \frac{rK}{4}$, it follow that 

$$
\begin{align}
4h&< rK \\
r&> \frac{4h}{K} \\
r^{2}&> \frac{4hr}{K} \\
r^{2}- \frac{4rh}{K}&>0 \tag*{(1)}
\end{align}
$$

Since the discriminant $r^{2}- \frac{4rh}{K}>0$ , it follow that $f(y)$ have 2 real distinct equilibrium point.

Thus, by quadratic formula, it follow that

$$
\begin{align}
y&= \frac{-r\pm \sqrt{ r^{2}- \frac{4rh}{K} }}{\frac{-2r}{K}} \tag*{(2)}\\
&=\frac{K}{2r}\left(r \mp \sqrt{ r^{2}- \frac{4rh}{K} } \right)
\end{align}
$$
Thus, 
$$
y_{1}= \frac{K}{2r}\left( r- \sqrt{ r^{2}- \frac{4rh}{K} } \right)
$$
and
$$
y_{2}= \frac{K}{2r}\left( r+ \sqrt{ r^{2}- \frac{4rh}{K} } \right)
$$


Approach 2 standard textbook answer:

Hence, by completing the square
$$
\begin{align}
-\frac{r}{k}y^{2}+ry-h&=0 \\
ry^{2}-rKy+hK&=0 \\
y^{2}-Ky+ \frac{hK}{r}&=0 \\
\left( y- \frac{K}{2} \right)^{2}- \left( -\frac{K}{2} \right)^{2} + \frac{hK}{r}&=0 \\
\left( y-\frac{K}{2} \right)^{2}&= \frac{K^{2}}{4}- \frac{hK}{r} \\
&= \frac{K^{2}r-4hK}{4r} \\
&= \frac{K^{2}}{4} \left( \frac{r^{2}-4h}{r} \right) \\
y-\frac{K}{2}&= \pm\frac{K}{2} \sqrt{ \frac{r^{2}-4h}{r} } \\
y&= \pm\frac{K}{2}+ \frac{K}{2}\sqrt{ \frac{r^{2}-4h}{r} } \\
&= \pm\frac{K}{2}\left( 1+ \sqrt{ \frac{r^{2}-4h}{r} } \right)
\end{align}
$$
---
b) Examine the stability of steady-states, $y _ { 1 }$ and $y _ { 2 }$ . 

Approach 1 derivative test:
$$
\begin{align}
f(y)&= -\frac{r}{K}y^{2}+ry-h \\
\frac{ \partial f }{ \partial y }  &= -\frac{2r}{K}y+ r \tag*{(3)}
\end{align}
$$

When $y= y_{1}= \frac{K}{2r}\left( r- \sqrt{ r^{2}- \frac{4rh}{K} } \right)$ 
$$
\begin{align}
\frac{ \partial f }{ \partial y } &= -\frac{2r}{K}\left( \frac{K}{2r}\left( r- \sqrt{ r^{2}- \frac{4rh}{K} } \right) \right)+r \\
&= -\left( r- \sqrt{ r^{2}- \frac{4rh}{K} } \right)+r \\
&=- \sqrt{ r^{2}-\frac{4rh}{K} }
\end{align}
$$

From (1) we know that $r^{2}-\frac{4rh}{K}>0\implies \sqrt{ r^{2}- \frac{4rh}{K} }\implies-\sqrt{ r^{2}- \frac{4rh}{K} }< 0$. Hence,

$$
\frac{ \partial f }{ \partial y } <0
$$

Therefore, $y_{1}$ is an attractor (asymptotically stable).

When $y=y_{2}=\frac{K}{2r}\left( r+ \sqrt{ r^{2}- \frac{4rh}{K} } \right)$
$$
\begin{align}
\frac{ \partial f }{ \partial y } &= -\frac{2r}{K}\left( \frac{K}{2r}\left( r+ \sqrt{ r^{2}- \frac{4rh}{K} } \right) \right)+r \\
&= -\left( r+ \sqrt{ r^{2}- \frac{4rh}{K} } \right)+r \\
&= \sqrt{ r^{2}-\frac{4rh}{K} }
\end{align}
$$
From (1) we know that $r^{2}-\frac{4rh}{K}>0\implies \sqrt{ r^{2}- \frac{4rh}{K} }$. Hence,

$$
\frac{ \partial f }{ \partial y } > 0
$$

Therefore, $y_{2}$ is an repeller (unstable).

> [!remark]
> When $h< \frac{rK}{4}$: Sustainable Harvesting:
> - Mathematical Behavior
> There are two distinct steady states: an unstable threshold $y_{1}$ and a stable carrying capacity $y_{2}(y_{1}<y_{2})$.
> - Ecological & Fishery Interpretation:
> 	- **Sustainability**: The harvest rate is below the maximum reproductive capacity of the fish. If the population more than $y_{1}$, then it will increase to $y_{2}$. The fishery can harvest $h$ fish per unit time indefinitely.
> 	- **The tipping point ($y_{1}$)**: If the population less than $y_{1}$, then natural births cannot offset the the fixed harvest $h$, causing the population to collapse to extinction.


![[fishery_case1_subcritical.png]]

---

c) For $\begin{array} { r } { h > \frac { r K } { 4 } , } \end{array}$ show that $y$ decreases to zero as $t$ increases. (C3: 1.5 Marks) 

Note that the first term of $\frac{dy}{dt}$ is a quadratic equation: 
$$
\begin{align}
ry\left( 1- \frac{y}{K} \right)&= ry- \frac{ry^{2}}{K}
\end{align}
$$

Axis of symmetric ($-\frac{b}{2a}$):
$$
\begin{align}
y&=-\frac{r}{2\left(- \frac{r}{K} \right)} \\
&= r \cdot\left( \frac{K}{2r} \right) \\
&= \frac{K}{2}
\end{align}
$$

The maximum value of first term:

$$
\begin{align}
ry\left( 1- \frac{y}{K} \right)&= r\left( \frac{K}{2} \right)\left( 1- \frac{\left( \frac{K}{2} \right)}{K} \right) \\
&=\frac{rK}{2}\left( 1- \frac{1}{2} \right) \\
&= \frac{rK}{4}
\end{align}
$$
Hence,

$$
\begin{align}
ry\left( 1- \frac{y}{K} \right)&< \frac{rK}{4}
\end{align}
$$
If $h> \frac{rK}{4}$, by transitivity law it follow that
$$
\begin{align}
ry\left( 1- \frac{y}{K} \right)&< h \\
ry\left( 1- \frac{y}{K} \right)-h&<0 \\
\frac{dy}{dt}&<0 
\end{align}
$$
for all $y\geq 0$.

Since $y(t)$ is strictly decreasing and bounded below by $y=0$, it must decrease continuously to 0 as $t$ increase.

Approach 2 direct from inequality:
$$
\begin{gathered}
h> \frac{rK}{4} \\
-h>-\frac{rK}{4} \\
ry\left( 1- \frac{y}{K} \right)-h< ry\left( 1- \frac{y}{K} \right)- \frac{rK}{4} \\
\frac{dy}{dt}<0
\end{gathered}
$$

> [!remark]
> When $h> \frac{rK}{4}$: Overharvesting
> - **Mathematical Behavior**:
> There are no steady state. The rate of change is strictly negative everywhere:
> $$
> \begin{gathered}
> \frac{dy}{dt}<0 &&\text{for all }y\geq 0
> \end{gathered}
> $$
> - **Ecological & Fishery Interpretation**:
> 	- Total Depletion: Humans are removing fish faster than the species can reproduce, even under optimal condition
> 	- Guaranteed Extinction: The population will decrease and hit extinction ($y=0$) in finite time. 

![[fishery_case3_supercritical.png]]


---

d) What happens to the steady-state population and its stability when $h = \frac { r K } { 4 } ?$ Provide a detailed analysis of the equilibrium and its stability. Relate your findings to the biological interpretation of this critical harvesting intensity as an environmental tipping point and its implications for the long-term sustainability of harvesting from the natural fish population. 

When $h=\frac{rK}{4}$

$$
\begin{align}
4h&= rK \\
r&= \frac{4h}{K} \\
r^{2}&= \frac{4hr}{K} \\
r^{2}- \frac{4rh}{K}&=0 
\end{align}
$$

Hence, by (2) the equilibrium point is 
$$
\begin{align}
y&=  \frac{-r\pm \sqrt{ r^{2}- \frac{4rh}{K} }}{\frac{-2r}{K}} \tag*{(2)} \\
&= -r \cdot \left( \frac{K}{-2r} \right) \\
&= \frac{K}{2}
\end{align}
$$

Stability by derivative test:
From (3) we have
$$
\begin{align}
\frac{ \partial f }{ \partial y }  &= -\frac{2r}{K}y+ r \\
&= -\frac{2r}{K}\left( \frac{K}{2} \right)+r \\
&=0
\end{align}
$$
$y= \frac{K}{2}$ is semi-stable. A solution from an initial point $(t_{0},y_{0})$ sufficiently near $c$ is attracted to $c$ from one side and repelled from the other side.

> [!remark]
> When $h= \frac{rK}{4}$: Maximum Sustainable Yield (MSY/Critical)
> - **Mathematical Behavior**:
> The two steady states collide into a single, semi-stable equilibrium at
> $$
> y=\frac{K}{2}
> $$
> - **Ecological and Fishery Interpretation**:
> 	- Maximum Theoretical Catch: This rate is called the **Maximum Sustainable Yield (MSY)**—the absolute maximum harvest a biological system can support.
> 	- **Extreme Fragility:** This state is practically dangerous. If the population is even slightly above $\frac{K}{2}$ ​, it slowly drops to$\frac{K}{2}$​. But if any random environmental perturbation drops the population even slightly below $\frac{K}{2}$​, reproduction drops below $h$, triggering an **irreversible collapse to extinction**.


![[fishery_case2_critical.png]]

e) By plotting the right-hand side of equation (1) i.e., $f(y)$ against $y$, using an appropriate computer package, demonstrate that your graphical findings are consistent with your analytical results in parts (a)–(d).

