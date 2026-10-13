1.  Determine the (i) order, (ii) dependent variable and (iii) the independent variable in each of the following differential equations: 

a) $y''-4xy'=e^{x}+1$

i) Order: Second order ($y''$)
ii) Dependent variable: $x$ because $y'=\frac{dy}{dx}$
iii) Independent variable: $y$

b) $\frac{1}{2}\left( \frac{d^{4}b}{da^{4}} \right)^{5}+2\left( \frac{db}{da} \right)^{10}+b^{7}-b^{5}=a$ ^ff6f2d

i) Order: 4 ($\frac{d^{4}b}{da^{4}}$)
ii) Dependent variable: $a$ 
iii) Independent variable: $b$

c) $t \ddot { s } - t \dot { s } = 1 - s \mathrm { i n } t$

i) Order: 2 $(\ddot{s})$
ii) Dependent variable: $s$
iii) Independent variable: $t$

> [!remark] Dot Notation (Newton's Notation)
> In physics and applied mathematics, dots placed above a variable denote differentiation with respect to time $t$:
> -  $\dot{s}$ (pronounced _"s-dot"_): First derivative with respect to time. $\dot{s}=\frac{ds}{dt}$​ _(In mechanics, this often represents velocity.)
>     
> -  $\ddot{s}$ (pronounced _"s-double-dot"_): Second derivative with respect to time.$\ddot{s}= \frac{d^{2}s}{dt^{2}}$​ _(In mechanics, this often represents acceleration.)

d) $\frac{d^{n}x}{dy^{n}}=y^{3}+12$

i) Order: $n$
ii) Dependent variable: $x$
iii) Independent variable: $y$

2. Check if $y ( x ) = 2 e ^ { - x } + x e ^ { - x }$ is the solution of $y ^ { \prime \prime } + 2 y ^ { \prime } + y = 0$.

$y':$
$$
\begin{align}
y(x)&=2e^{-x}+xe^{-x} \\
y'&=-2e^{-x}+ -xe^{-x}+e^{-x}&&(\text{Product Rule}) \\
&=-(y)+e^{-x} \\
\end{align}
$$

$y'':$

$$
\begin{align}
y'&=-y+e^{-x} \\
y''&=-y'-e^{-x}
\end{align}
$$

Notice that $y.y',y''$ is continuous in the interval $I=(-oo,\infty)$. Thus it fulfill the continuity condition.

Thus, by substitution,

$$
\begin{align}
y''+2y'+y&=0 \\
(-y'-e^{-x})+2(-y+e^{-x})+y&=0 \\
(y-e^{-x}-e^{-x})-2y+2e^{-x}+y&=0 \\
0&=0
\end{align}
$$

Thus, by definition [[Solution of an ODE|Solutions of Differential Equations]] , it follow that $y(x)$ is the solution of the ODE in $I$.

\newpage

3. Verify that the following functions are solutions to the given differential equations for all $x$.
 a. $y ( x ) = 3 e ^ { 2 x }$ and $\begin{array} { r } { \frac { d y } { d x } - 2 y = 0 . } \end{array}$ 
 b. $y ( x ) = x + 4 { \sqrt { x + 2 } } \operatorname { a n d } ( y - x ) y ^ { \prime } = y - x + 8 .$ 

a) 

$y':$
$$
\begin{align}
y(x)&=3e^{2x} \\
y'&=6e^{2x}
\end{align}
$$

Notice that $y,y'$ are continuous on $I=(-\infty,\infty )$.

By Substitution:
$$
\begin{align}
\frac{dy}{dx}-2y&=0 \\
6e^{2x}-2(3e^{2x})&=0 \\
0&=0
\end{align}
$$

Thus, by definition $y(x)$ is the particular solution (one parameter solution) for the ODE in $I$.

b.

$y':$
$$
\begin{align}
y(x)&=x+4\sqrt{ x+2 } \\
y'&=1+\frac{2}{\sqrt{ x+2 }}
\end{align}
$$

Notice that, $y$ and $y'$ are continuous in $I=(-2,\infty)$.

By substitution:
$$
\begin{align}
(y-x)y'&=y-x+8 \\
(x+4\sqrt{ x+2 }-x)\left( 1+ \frac{2}{\sqrt{ x+2 }} \right)&=x+4\sqrt{ x+2 }-x+8 \\
4\sqrt{ x+2 }+8&=4\sqrt{ x+2 }+8
\end{align}
$$

Thus, $y(x)$ is the solution of the ODE on $I$.


> [!remark]
> Remark: Non-linear ODE usually have implicit solution.

\newpage

4. Find a solution to the boundary-value problem $\begin{array} { r } { y ^ { \prime \prime } + 4 y = 0 ; y \left( \frac { \pi } { 8 } \right) = 0 , y \left( \frac { \pi } { 6 } \right) = 1 } \end{array}$ , if the general solution to the differential equations is $y(x)=a\sin 2x+b\cos 2x$ ^451ae6

Notice that it is a second order boundary value problem. (We have $y(x_{0})$ and $y(x_{1})$ as condition )

Apply first boundary $y\left( \frac{\pi}{8} \right)=0$
$$
\begin{align}
0&=a\sin 2\left( \frac{\pi}{8} \right)+b\cos 2\left(  \frac{\pi}{8} \right) \\
&=a\sin \left( \frac{\pi}{4} \right)+b\cos \left( \frac{\pi}{4} \right) \\
&=a\left( \frac{\sqrt{ 2 }}{2} \right)+b\left( \frac{\sqrt{ 2 }}{2} \right) \\
b&=-a
\end{align}
$$

Apply second boundary $y\left( \frac{\pi}{6} \right)=1$:

$$
\begin{align}
1&=a \sin 2\left( \frac{\pi}{6} \right)+b \cos 2\left( \frac{\pi}{6} \right) \\
&= a\left( \frac{\sqrt{ 3 }}{2} \right)+ b\left( \frac{1}{2} \right) \\
\end{align}
$$
Since $a=-b$ (from first boundary) , by substitution

$$
\begin{align}
1&= a\left( \frac{\sqrt{ 3 }}{2} \right)-a\left( \frac{1}{2} \right) \\ 
1&= a\left(  \frac{\sqrt{ 3 }-1}{2} \right) \\
a&= \frac{2}{\sqrt{ 3 }-1} \times \frac{\sqrt{ 3 }+1}{\sqrt{ 3 }+1} \\
&= \frac{2(\sqrt{ 3 }+1)}{2} \\
&= \sqrt{ 3 }+1
\end{align}
$$

Since $b=-a$, it follow that

$$
b=-(\sqrt{ 3+1 })
$$

The the solution is

$$
y(x)=(\sqrt{ 3}+1)\sin(2x)-(\sqrt{ 3 }+1)\cos(2x)
$$

> [!remark]
> Remark: 
> In this case the solution $y(x)$ is apparently continuous every where, thus it must be continuous in $\left[ \frac{\pi}{6}, \frac{\pi}{8} \right]$
> 
> 
> What if the solution is not given at the first place?
> Then we just need to check the DE.
> In the differential equation equation: $y''+4y=0$, the standard linear form $y''+P(x)y'+Q(x)y=g(x)$, the coefficient are:
> $$
> \begin{align}
> P(x)&=0 \\
> Q(x)&=4 \\
> g(x)&=0
> \end{align}
> $$
> 
> 
> Since they are all continuous everywhere. By Linear ODE Theorem, it follow that the solution $y(x)$ is continuous on everywhere and twice differentiable 

\newpage

5. Find values of $a$ and $b$ so that the given functions will satisfy the initial conditions: 

a. $y ( x ) = a e ^ { x } + b e ^ { - x } + 4 \sin x ; \quad y ( 0 ) = 1 , \quad y ^ { \prime } ( 0 ) = - 1 .$ 

Substitute $y(0)=1$:

$$
\begin{align}
1&=ae^{0}+be^{-0}+4\sin(0) \\
1&=a+b+4(0) \\
a&=1-b
\end{align}
$$

$y'$:
$$
\begin{align}
y'(x)&=ae^{x}-be^{-x}+4\cos x \\
\end{align}
$$
Substitute $y'(0)=-1$:

$$
\begin{align}
-1&=ae^{0}-be^{-0}+4\cos(0) \\
-1&=a-b+4 \\
-5&=a-b \\
a&=b-5
\end{align}
$$

Thus,
$$
\begin{align}
1-b&=b-5 \\
2b&=6 \\
b&=3
\end{align}
$$
Hence,
$$
\begin{align}
a&=b-5 \\
&=3-5 \\
&=-2
\end{align}
$$
Thus the solution is:
$$
y(x)=-2e^{x}+3e^{-x}+4\sin x
$$

\newpage

b. $y (x) = a e ^ {x} + b e ^ {2 x} + 3 e ^ {3 x}; \quad y (0) = 0, \quad y ^ {\prime} (0) = 0.$

Substitute $y(0)=0:$
$$
\begin{align}
0&=ae^{0}+be^{2(0)}+3e^{3(0)} \\
0&=a+b+3 \\
a&=-b-3
\end{align}
$$
$y':$
$$
\begin{align}
y'&=ae^{x}+2be^{2x}+9e^{3x}
\end{align}
$$
Substitute $y'(0)=0:$
$$
\begin{align}
0&=ae^{0}+2be^{2(0)}+9e^{3(0)} \\
0&=a+2b+9 \\
a&=-2b-9
\end{align}
$$
Thus,
$$
\begin{align}
-b-3&=-2b-9 \\
b&=-6
\end{align}
$$
Hence,
$$
\begin{align}
a&=-(-6)-3 \\
&=3
\end{align}
$$
Thus, the solution is
$$
y(x)=3e^{x}-6e^{2x}+3e^{3x}
$$

c. $y ( x ) = a \sin x + b \cos x + 1 ; \quad y ( \pi ) = 0 , \quad y ^ { \prime } ( \pi ) = 0 .$ 

Substitute $y(\pi)=0:$
$$
\begin{align}
0&=a\sin (\pi)+b\cos (\pi)+1 \\
&=a(0)+b(-1)+1 \\
&=-b+1 \\
b&=1
\end{align}
$$

$y':$
$$
y'(x)=a\cos x-b\sin x
$$

Substitute $b=1$ and $y'(\pi)=0:$
$$
\begin{align}
0&=a \cos(\pi)-1\sin(\pi) \\
0&=a(-1)-1(0) \\
0&=-a \\
a&=0
\end{align}
$$

Thus, the solution is:
$$
y(x)=\cos x +1
$$

\newpage

6. Apply Theorem 1.2 to the initial value problem 

$$
{\frac {d y}{d x}} = {\frac {3 x ^ {2} + 4 x + 2}{2 (y - 1)}}, y (0) = - 1.
$$

a. Check if it has a unique solution in some interval about $x=0$

Identify $f(x,y)$ and compute $\frac{\partial f}{\partial y}$:

$$
f(x,y)= \frac{3x^{2}+4x+2}{2(y-1)}
$$
and
$$
\frac{\partial f}{\partial y}= \frac{2(3x^{2}+4x+2)}{4(y-1)^{2}}= \frac{3x^{2}+4x+2}{2(y-1)^{2}} 
$$

> [!remark]
> Use quotient rule and treat $x$ as constant.

Check continuity: 
Both $f(x,y)$ and $\frac{\partial y}{\partial x}$ are rational function, thus it is continuous everywhere except $y=1$.

Define a Rectangle $R$:
The initial point is $(x_{0},y_{0})=(0,-1)$. Thus we can define a rectangular region $R$ containing $(0,-1)$ and does not cross $y=1$, for example $R=\{ (x,y)| -\infty<x<\infty \text{ and }-\infty<y<1\}$ (The largest region)

Conclusion:
Since both $f(x,y)$ and $\frac{\partial f}{\partial y}$ are continuous on $R$, by Theorem 1.2, there exist some interval $I_{0}=(-h,h)$ with $h>0$ in $R$ centered at $x_{0}=0$ on which the given IVP has a unique solution. 


on the region that contains $(0,1)$ and stay below the line $y=1$ Since $(0,-1)$ is in the region, by Theorem 1.2, there exist some interval $(0-h,0+h)$ such that it has a unique solution for the IVP.



b. What happen if the initial condition is changed to $y ( 0 ) = 1 ?$ 

At $(x_{0},y_{0})=(0,1)$, $f(x,y)$ is undefined due to division by zero. Thus, no solution exists for this IVP. (It means that any candidate function that being substitute is not differentiable)

\newpage

7. For the following problems: 
i. Identify the equilibrium values 
ii. Construct a phase line. Identify the signs of $y ^ { \prime }$ and $y ^ { \prime \prime }$ . 
iii. Sketch several solution curves. 

a. $\begin{array} { r } { \frac { \mathrm { d } \mathbf { y } } { \mathrm { d } \mathbf { x } } = ( \mathbf { y } + 2 ) ( \mathbf { y } - 3 ) } \end{array}$ 
i)
Let $\frac{dy}{dx}=f(y)$. The equilibrium point is the zero of $f$. 

Thus, let $f(y)=0$
$$
\begin{align}
0&=(y+2)(y-3) \\ 
y=-2 &\text{ or }y=3
\end{align}
$$

Thus, $y(x)=-2$ and $y(x)=3$ are constant solution for autonomous DE $f(y)$.

ii) 

Find $y''$:
$$
\begin{align}
y''&=\frac{d}{dx} f(y) \\
&= f'(y)\cdot \frac{dy}{dx}&&\text{(Chain rule)}\\
&=((y+2)+(y-3))\cdot(y+2)(y-3) \\
&=(2y-1)(y+2)(y-3)
\end{align}
$$

The critical point are $y= \frac{1}{2}$ , $y=3$ and $y=-2$. Thus,

iii)
![[WhatsApp Image 2026-10-12 at 17.05.01.jpeg]]

\newpage

b. $\begin{array} { r } { \frac { d y } { d x } = y ^ { 2 } - 2 y } \end{array}$ 

i)
Let $f(y)=\frac{dy}{dx}$. The equilibrium point is the zero of $f$. 

Thus, let $f(y)=0$
$$
\begin{align}
0&=y^{2}-2y \\
0&=y(y-2) \\
y=0 &\text{ and } y=2
\end{align}
$$
Thus, $y(x)=0$ and $y(x)=2$ are constant solution for autonomous DE $f(y)$.

ii)
Find $y''$:
$$
\begin{align}
y''&=f'(y)\cdot f(y) \\
&= (2y-2)(y)(y-2)
\end{align}
$$
Thus, the critical point is $y=1$, $y=0$ and $y=2$

iii)
![[WhatsApp Image 2026-10-12 at 17.05.02.jpeg]]

\newpage

8. Consider the differential equation $y ^ { \prime } = x y ^ { 2 }$ 

a. Sketch the direction field for the given differential equation for $- 3 \leq x , \ y \leq 3$ 

b. Solve the differential equation with the initial condition $y ( 1 ) = - 2 .$ 