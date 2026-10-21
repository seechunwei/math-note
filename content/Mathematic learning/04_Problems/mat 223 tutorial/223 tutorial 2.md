1. Determine if the following differential equations are separable: 

a. $\sin x d x + y ^ { 2 } d y = 0$ 

$$
\begin{align}
y^{2} dy&=-\sin x dx \\
\end{align}
$$
Thus, it is separable. But it is not linear because $y^{2}$.
 
b. $x y ^ { 2 } d x - x ^ { 2 } y ^ { 2 } d y = 0$ 

$$
\begin{align}
-x^{2}y^{2}dy=-xy^{2}dx
\end{align}
$$
Notice that it is $M(x,y)dy=N(x,y)dx$. Thus, it is not separable and also not linear.

c. $( 1 + x y ) d x + y d y = 0$ 

$$
\begin{align}
ydy&= (xy-1)dx  \\
\frac{dy}{dx}&= \frac{xy-1}{y} \\
&=x- \frac{1}{y} \\
\end{align}
$$
It is not separable and not linear.

2. Solve 

a. $x d x - y ^ { 2 } d y = 0$ 

Note that it is separable DE. Thus,

$$
\begin{align}
x dx&=y^{2}dy \\
y^{2}\frac{dy}{dx}&= x \\
\int y^{2} \frac{dy}{dx} \, dx &= \int x \, dx  &&(1)\\
\int y^{2} \, dy &= \frac{x^{2}}{2} \\
\frac{y^{3}}{3}&=\frac{x^{2}}{2}+c \\
2y^{3}-3x^{2}&=c
\end{align}
$$

(1) By definition of differential $dy= y'(x)dx$. Thus, $2y^{3}-3x^{2}=c$ is the implicit solution of one-parameter family of this DE.

> [!remark]
> This question don't have singular solution because it is divide by $y$, and also for this kind of solution we no need to concern about the interval except it is an IVP or find explicit solution.

b. $\begin{array} { r } { y ^ { \prime } = \frac { x + 1 } { y ^ { 4 } + 1 } } \end{array}$ 

$$
\begin{align}
(y^{4}+1)\frac{dy}{dx}&= x+1 \\
\int (y^{4}+1) \frac{dy}{dx}\, dx &= \int x+1 \, dx  \\
\int y^{4}+1 \, dy &= \frac{x^{2}}{2}+x \\
\frac{y^{5}}{5}+y&= \frac{x^{2}}{2}+x+c \\
2y^{5}+y-5x^{2}-x&=c
\end{align}
$$
Thus, $2y^{5}+y-5x^{2}-x=c$ is the implicit solution of one-parameter family.

c. $\begin{array} { r } { \frac { d x } { d t } = x ^ { 2 } - 2 x + 2 } \end{array}$ 

$$
\begin{align}
\frac{dx}{dt}&= x^{2}-2x+2 \\
\frac{1}{x^{2}-2x+2} \frac{dx}{dt}&=1 \\
\int \frac{1}{x^{2}-2x+2} \, dx &=t \\
\int \frac{1}{(x-1)^{2}+1} \, dx &=t \\
\tan ^{-1}(x-1)&=t+c \\
\tan ^{-1}(x-1)-t&=c
\end{align}
$$

The explicit solution:
$$
\begin{align}
\tan ^{-1}(x-1)&=t+c \\
x-1&=\tan(t+c) \\
x&=\tan(t+c)+1
\end{align}
$$

The function is continuous on domain $I= \mathbb{R}\setminus \left\{  \frac{n\pi}{2}-c|n\in 2\mathbb{Z}+1  \right\}$. One of the single connected interval of definition is $\left( \frac{-\pi}{2}-c, \frac{\pi}{2}-c \right)$. Thus, $x=\tan(t+c)+1$ is the solution of one-parameter family in one connected subinterval on $I$.



3. Find an explicit solution to the given IVP 

a. $\begin{array} { r } { x ^ { 2 } \frac { d y } { d x } = y - x y , ~ y ( - 1 ) = - 1 } \end{array}$ 

$$
\begin{align}
x^{2} \frac{dy}{dx}&= y(1-x) \\
\frac{1}{y} \frac{dy}{dx}&= \frac{1-x}{x^{2}} \\
\int \frac{1}{y} \, dy&= \int \frac{ 1-x}{x^{2}} \, dx  \\
\ln \lvert y \rvert&= \int \frac{1}{x^{2}} - \frac{1}{x} \, dx  \\
&= - \frac{1}{x}-\ln \lvert x \rvert+c \\  
\lvert y \rvert &= e^{-1/x -\ln \lvert x \rvert+c} \\ 
\lvert y \rvert&= \frac{c_{1}}{e^{\frac{1}{x}}\cdot \lvert x \rvert} &&c_{1}=e^{c} \\
\lvert xy \rvert&= \frac{c_{1}}{e^{1/x}} \\
xy&= \frac{c_{2}}{e^{1/x}} &&c_{2}=\pm c_{1}\\
y&= \frac{c_{2}}{e^{1/x}x}
\end{align}
$$

The given initial condition is $y(-1)=-1$: By substitution

$$
\begin{align}
-1&= \frac{c_{2}}{e^{\frac{1}{-1}}-1} \\
c_{2}&=1
\end{align}
$$
Thus, $y= \frac{1}{e^{1/x}}x$ is the particular solution for this IVP on interval $(-\infty,0)$


> [!remark]
> This is linear DE, and note that $x^{2}$ and $1-x$  and $0$ is continuous everywhere. Thus, By Linear ODE Existence & Uniqueness Theorem, there exist a unique solution in the interval contain $x_{0}$.

b. $\begin{array} { r } { \frac { d y } { d x } = 4 y ^ { 2 } + 1 , ~ y \left( \frac { \pi } { 4 } \right) = 1 . } \end{array}$ 

$$
\begin{align}
\frac{1}{4y^{2}+1} \frac{dy}{dx}&=1 \\
\int \frac{1}{4y^{2}+1} \, dy &=x \\
\frac{1}{2}\tan ^{-1}(2y)&=x+c &&(2)\\
 y&=2\tan(2x+c_{1}) \\
y&= \frac{\tan(2x+c_{1})}{2}
\end{align}
$$

(2) Let $u=2y$, thus $\frac{1}{2}\int \frac{1}{u^{2}+1}  \, du\implies \frac{1}{2}\tan u$.

Substitute the initial condition:
$$
\begin{align}
1&= \frac{\tan\left( \frac{\pi}{2}+c \right)}{2} \\
2&=\tan\left( \frac{\pi}{2}+c \right) \\
\tan ^{-1}\left(2\right)&=\frac{\pi}{2}+c \\
c&=\tan ^{-1}(2)- \frac{\pi}{2}
\end{align}
$$

Find the interval of definition $I$:
$$
\begin{matrix}
-\frac{\pi}{2}<2x+c< \frac{\pi}{2} \\
-\frac{\pi}{2}-\tan ^{-1}(2)+\frac{\pi}{2}<2x< \frac{\pi}{2}-\tan ^{-1}(2)+ \frac{\pi}{2} \\
-\frac{1}{2}\tan ^{-1}(2)< x< \frac{\pi}{2}- \frac{1}{2}\tan ^{-1}(2)
\end{matrix}
$$

Thus, $y= \frac{\tan\left( 2x+\tan ^{-1}(2)- \frac{\pi}{2} \right)}{2}$ is the solution for IVP on $I=\left( -\frac{1}{2}\tan ^{-1}(2), \frac{\pi}{2}-\tan ^{-1}(2) \right)$

> [!remark]
> This is an autonomous solution but it don't have singular solution because no $y$ that make $4y^{2}+1=0$ or $f(y)=0$.
> $P(x)$ and $H(y)$ is also continuous everywhere implies that there exist a unique solution on interval contain $x_{0}$.

c. $e ^ { x } d x - y d y = 0 , \ y ( 0 ) = 1$ 

$$
\begin{align}
e^{x}dx&= ydy \\
y \frac{dy}{dx}&= e^{x} \\
\int y \, dy &=e^{x} \\
\frac{y^{2}}{2}&= e^{x}+c \\
y^{2}&=2e^{x}+c_{1} \\
y&= \pm \sqrt{ 2e^{x} +c_{1}}
\end{align}
$$
Since $y_{0}=1$, it follow that the explicit solution should be
$$
y=\sqrt{ 2e^{x}+c_{1} }
$$

Substitution:
$$
\begin{align}
1&= \sqrt{2 e^{0}+c_{1} } \\
1&=2+c_{1} \\
c_{1}&=-1
\end{align}
$$

Finding interval of definition $I$:

$$
\begin{align}
2e^{x}-1&>0 \\
2e^{x}&>1 \\
e^{x}&> \frac{1}{2} \\
x&> \ln \left( \frac{1}{2} \right)
\end{align}
$$


Thus, $y=\sqrt{ 2e^{x}-1 }$ is the particular solution for this IVP on interval $I=\left( \ln\left( \frac{1}{2} \right),\infty \right)$.


4. Determine if the following differential equations are linear: 
a. $y ^ { \prime } = x \sin y + e ^ { x }$ (Not linear because of $\sin y$.)

b. $\begin{array} { r } { \frac { d y } { d x } = ( \sin x ) y + e ^ { x } } \end{array}$(linear)

c. ${ \frac { d y } { d x } } = y ^ { 2 } + x$ (Not linear because $y^{2}$)

d. $t y ^ { \prime } + y = \sqrt { y }$ (Not linear because $\sqrt{ y }$)

e. $x ^ { \prime } + t x = e ^ { t } x$ (linear)


5. Find an integrating factor for $y ^ { \prime } - 3 y = 6$ and solve the differential equation. 

Note that it is linear equation and separable also. 

Finding integrating factor:

$$
\begin{align}
\mu(x)&=e^{\int -3  \, dx } \\
&=e^{-3x+c} \\
&=e^{-3x}
\end{align}
$$
Multiply $e^{-3x}$ :

$$
\begin{align}
\frac{d}{dx}(ye^{-3x})&= 6e^{-3x} \\
ye^{-3x}&=\int 6e^{-3x} \, dx \\
&=-2e^{-3x}+c \\
y&=  -2+ ce^{3x} 
\end{align}
$$

> [!remark]
> The equilibrium solution can be obtained when $c=0$


6. Solve the following differential equations: 
a. $\textstyle { \frac { d y } { d x } } + 3 x ^ { 2 } y = x ^ { 2 }$ 

Note that it is linear and separable equation.

$$
\begin{align}
\frac{dy}{dx}&=x^{2}-3x^{2}y \\
&=x^{2}(1-3y) \\
\frac{1}{1-3y} \frac{dy}{dx} &=x^{2} \\
\int \frac{1}{1-3y} \, dy &= \int x^{2} \, dx  \\
-\frac{1}{3}\ln \lvert 1-3y \rvert&= \frac{x^{3}}{3}+c \\
\ln \lvert 1-3y \rvert & = -x^{3}+c_{1} \\
\lvert 1-3y \rvert&= c_{2}e^{-x^{3}} \\
1-3y&=\frac{c_{3}}{e^{x^{3}}} &&c_{3}=\pm c_{2} \\
-3y&= \frac{c_{3}}{e^{x^{2}}}-1 \\
y&=\frac{1}{3}- \frac{c_{4}}{e^{x^{3}}} \\
\end{align}
$$
Thus, $y= \frac{1}{3}- \frac{c^{4}}{e^{x^{3}}}$ is the solution of 1-parameter family on interval $I=(-\infty,\infty)$


b. $x ^ { 2 } y ^ { \prime } + x ( x + 2 ) y = e ^ { x }$ 

Note that it is linear but not separable. We rewrite it using to the standard form by dividing $x^{2}$

$$
\begin{align}
\frac{dy}{dx}+ \frac{x+2}{x}y&= \frac{e^{x}}{x^{2}} \\
\frac{dy}{dx}+\left( 1+ \frac{2}{x} \right)y&= \frac{e^{x}}{x^{2}}
\end{align}
$$

Find the integrating factor:
$$
\mu(x)=e^{\int 1+ \frac{2}{x} \, dx }=e^{x+2\ln \lvert x \rvert}=e^{x}\cdot(x^{2})
$$

Thus, multiplying DE by $\mu(x)$:

$$
\begin{align}
\frac{d}{dx}(yx^{2}e^{x})&=e^{2x} \\
yx^{2}e^{x}&= \int e^{2x} \, dx \\ 
&= \frac{1}{2}e^{2x}+c \\
y&= \frac{e^{x}}{2x^{2}} + \frac{c}{x^{2}e^{x}} \\
&= \frac{e^{2x}+c_{1}}{2x^{2}e^{x}}
\end{align}
$$

Thus, $y=\frac{e^{2x}+c_{1}}{2x^{2}e^{x}}$ is the solution of 1-parameter family on interval $I=(-\infty,0)$ or $I=(0,\infty)$

7. Solve the initial value problems; 

a. $\begin{array} { r } { y ^ { \prime } - ( \sin x ) y = 2 \sin x ; y \left( \frac { \pi } { 2 } \right) = 1 . } \end{array}$ 

Note that it is linear. 

Finding integrating factor:
$$
\mu(x)=e^{\int- \sin x \, dx }=e^{\cos x+c}=e^{\cos x}
$$

Multiplying DE by $\mu(x)$:

$$
\begin{align}
\frac{d}{dx}(ye^{\cos x})&=2\sin x e^{\cos x} \\
ye^{\cos x}&= \int 2\sin xe^{\cos x} \, dx  \\
&= -2e^{\cos x}+c  \\
y&= -2+ ce^{-\cos x}
\end{align}
$$

Substitute $(x_{0},y_{0})= (\frac{\pi}{2},1)$:

$$
\begin{align}
1&=-2+ce^{-\cos(\pi/2)} \\
1&=-2+c \\
c&=3
\end{align}
$$

Thus $y=-2+3e^{-\cos x}$ is the particular solution for the IVP on $I=(-\infty.\infty)$

b. $y ^ { \prime } + y = \sin x ; y ( \pi ) = 1 \quad$ 

It is linear equation.

Find integrating factor:
$$
\mu(x)=e^{\int  1 \, dx }=e^{x}
$$

Multiplying DE by $\mu(x)$:
$$
\begin{align}
\frac{d}{dx}(ye^{x})&=e^{x}\sin x \\
ye^{x}&= \int e^{x}\sin x \, dx
\end{align}
$$
Notice that:
$$
\begin{align}
\int e^{x}\sin x \, dx&=e^{x}\sin x -\int e^{x}\cos x  \, dx  \\
&=e^{x}\sin x-\left( e^{x}\cos x+\int e^{x}\sin x \, dx  \right) \\
2\int e^{x}\sin x \, dx  &=e^{x}\sin x-e^{x}\cos x \\
\int e^{x}\sin x \, dx&=  \frac{e^{x}\sin x-e^{x}\cos x}{2}+c
\end{align}
$$

> [!remark]
> $\int e^x \sin x \, dx$ is a famous **cyclic ("boomerang") integral**. Applying Integration by Parts twice returns the original integral on the right-hand side, allowing us to solve for it algebraically by adding it over to the left side.


Thus, 
$$
\begin{align}
ye^{x}&=  \frac{e^{x}\sin x-e^{x}\cos x}{2}+c \\
y&= \frac{\sin x-\cos x}{2}+ \frac{c}{e^{x}}
\end{align}
$$

Substitute $(x_{0},y_{0})=(\pi,1)$:

$$
\begin{align}
1&= \frac{\sin \pi-\cos \pi}{2}+ \frac{c}{e^{\pi}} \\
1&= \frac{1}{2}+ \frac{c}{e^{\pi}} \\
c&= \frac{e^{\pi}}{2}
\end{align}
$$

Thus, $y= \frac{\sin x-\cos x}{2}+ \frac{e^{\pi}}{2e^{x}}$ is the particular solution for this IVP on interval $I=(-\infty,\infty)$



8. Solve $\begin{array} { r } { \frac { d Q } { d t } + k Q = 1 0 0 k } \end{array}$ , where $k$ denotes a constant. 

It is a linear equation.

Find the integrating factor:
$$
\mu(t)=e^{\int k \, dt }=e^{kt}
$$

Multiply DE by $\mu(t)$:

$$
\begin{align}
\frac{d}{dt}(Qe^{kt})&= e^{kt}100k \\
Qe^{kt}&= \int e^{kt}100k \, dt \\
&=\frac{1}{k}(e^{kt}100k)+c \\
Qe^{kt}&=100e^{kt} +c \\
Q&=100 +\frac{c}{e^{kt}}
\end{align}
$$
