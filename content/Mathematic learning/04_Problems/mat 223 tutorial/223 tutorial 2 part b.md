1. Determine whether the following differential equations are exact: 

a. $3 x ^ { 2 } y d x + ( y + x ^ { 3 } ) d y = 0$ 

Let $M(x,y)= \frac{\partial f}{\partial x}=3x^{2}y$ and $N(x,y)= \frac{\partial f}{\partial y}=y+x^{3}$.
Note that $M(x,y)$ and $N(x,y)$ are continuous and have continuous first partial derivative everywhere, thus we can construct a region $R=\{ (x,y)\in \mathbb{R}^{2} \}$.

By theorem ![[2.4 Exact Equations#^9b5675]] the DE is exact iff

$$
M(x,y)_{y}= \frac{\partial M}{\partial y}= \frac{\partial N}{\partial x}=N(x,y)_{x}
$$


Note that
$$
\begin{align}
M(x,y)_{y}&=3x^{2}
\end{align}
$$
and
$$
N(x,y)_{x}=3x^{2}
$$

Thus, it is clear that
$$
M(x,y)_{y}=N(x,y)_{y}
$$
Hence, it is exact.


b. $x y d x + y ^ { 2 } d y = 0$ 

Let $M(x,y)=xy$ and $N(x,y)=y^{2}$. Thus, 

$$
\begin{align}
\frac{\partial M}{\partial y}&= x
\end{align}
$$
and
$$
\begin{align}
\frac{\partial N}{\partial x}&= 0
\end{align}
$$

Since,
$$
\frac{\partial M}{\partial y} \neq \frac{\partial N}{\partial x}
$$
it follow that the DE is not exact.


2. Prove that a separable equation is always exact. 

By definition a first order separable DE always have the form below:
$$
\begin{align}
\frac{dy}{dx}&=g(x)h(y) \\
\frac{1}{h(y)} dy&=g(x) dx \\
 g(x)dx-\frac{1}{h(y)}dy&=0
\end{align}
$$

Let $M(x,y)=g(x)$ and $N(x,y)= H(y)$ where $H(y)=- \frac{1}{h(y)}$. 

Assuming $g(x)$ and $h(x)$ are continuous on interval $I_{x}$ and $I_{y}$ respectively (with $h(y) \neq 0$ on $I_{y}$)

Thus,
$$
\frac{\partial M}{\partial y}=0= \frac{\partial N}{\partial x}
$$

Hence, the DE is exact by Exactness Test Theorem.

> [!remark] Concrete Explanation & Intuition
> To see what this means in practice, consider the simple separable equation **$\frac{dy}{dx} = xy$**:
> 
> 1. **What makes it exact? (Way A vs. Way B):**
>    - **Way A: Don't divide by $y$ (Raw form):**
>      Rearrange directly to $xy\,dx - dy = 0$.
>      Here $M = xy$ and $N = -1$.
>      $\frac{\partial M}{\partial y} = x$ while $\frac{\partial N}{\partial x} = 0$. Since $x \neq 0$, **it is NOT exact!**
>    - **Way B: Divide by $y$ (Separated form):**
>      Divide the equation by $y$ to get $x\,dx - \frac{1}{y}\,dy = 0$.
>      Here $M = x$ and $N = -\frac{1}{y}$.
>      $\frac{\partial M}{\partial y} = 0$ and $\frac{\partial N}{\partial x} = 0$. **Now it IS exact!**
>    - **Key takeaway:** The equation in Way A was not exact. The act of dividing by $y$ (multiplying by $\frac{1}{y}$) was secretly using an **integrating factor $\mu$** that turned it into the exact equation in Way B.
> 
> 2. **Why do we need $h(y) \neq 0$? (The Lost Solution Trap):**
>    - In $\frac{dy}{dx} = xy$, if $y = 0$, then $\frac{dy}{dx} = 0$. This means the horizontal line **$y(x) = 0$ is a valid solution**.
>    - However, in **Way B**, once we divide by $y$ to get $\frac{1}{y}\,dy$, we cannot plug in $y = 0$ (division by zero $\frac{1}{0}$).
>    - That is why we must state $h(y) \neq 0$: dividing by a variable can hide or lose constant solutions (called **equilibrium solutions**).
> 
> 3. **Exact by Definition directly:**
>    - Instead of computing cross-derivatives, you can directly integrate to find the potential function $f(x, y)$:
>      $$f(x, y) = \int x\,dx - \int \frac{1}{y}\,dy = \frac{1}{2}x^2 - \ln|y|$$
>    - Its total differential is $df = x\,dx - \frac{1}{y}\,dy = 0$, which immediately proves exactness from the definition ($df = 0 \implies f(x, y) = c$).

3. Solve 

$$
y ^ {\prime} = \frac {2 + y e ^ {x y}}{2 y - x e ^ {x y}}
$$

$$
\begin{align}
(2y-xe^{xy})dy&= (2+ye^{xy})dx \\
(2+ye^{xy})dx+(xe^{xy}-2y)dy&=0
\end{align}
$$

Let $M(x,y)=2+ye^{xy}$ and $N(x,y)=xe^{xy}-2y$. Note that $M(x,y)$ and $N(x,y)$ is continuous on $\mathbb{R}^{2}$.
Thus, we check the exactness:
$$
\begin{align}
\frac{\partial M}{\partial y}&= yxe^{xy}+e^{xy}
\end{align}
$$
and
$$
\begin{align}
\frac{\partial N}{\partial x}&= xye^{xy}+e^{xy}
\end{align}
$$
Note that $\frac{\partial M}{\partial y}$ and $\frac{\partial N}{\partial x}$ are also continuous on $\mathbb{R}^{2}$.

Hence, it is clear that
$$
\frac{\partial M}{\partial y}= \frac{\partial N}{\partial x}
$$

Thus,
$$
\begin{align}
f(x,y)&= \int M(x,y) \, dx +g(y) \\
&=\int 2+ye^{xy} \, dx +g(y) \\
&=2x+ e^{xy}+g(y) \\
\frac{\partial f}{\partial y}&= \frac{\partial}{\partial y}(2x+e^{xy})+g'(y) \\
xe^{xy}-2y&= xe^{xy}+g'(y) \\
g'(y)&= -2y \\
g(y)&= -y^{2}+c
\end{align}
$$

Thus, $f(x,y)= 2x+e^{xy}-y^{2}+c$. Hence, $2x+e^{xy}-y^{2}=c_{1}$ is the implicit solution for the DE.

> [!tip] Alternative Method: Solving by Inspection (Grouping Differentials)
> Instead of setting up $f(x,y) = \int M\,dx + g(y)$, we can solve exact equations directly by grouping terms into recognizable **total differentials** $du = \frac{\partial u}{\partial x}dx + \frac{\partial u}{\partial y}dy$:
> 
> From the differential form:
> $$ (2 + y e^{xy})\,dx + (x e^{xy} - 2y)\,dy = 0 $$
> 
> Expand and group terms with similar structures:
> $$ (2\,dx - 2y\,dy) + (y e^{xy}\,dx + x e^{xy}\,dy) = 0 $$
> 
> 1. **First group ($2\,dx - 2y\,dy$):**
>    - For $u = 2x - y^2$, the partial derivatives are $\frac{\partial u}{\partial x} = 2$ and $\frac{\partial u}{\partial y} = -2y$:
>      $$d(2x - y^2) = 2\,dx - 2y\,dy$$
> 
> 2. **Second group ($y e^{xy}\,dx + x e^{xy}\,dy$):**
>    - For $u = e^{xy}$, the partial derivatives are $\frac{\partial u}{\partial x} = y e^{xy}$ and $\frac{\partial u}{\partial y} = x e^{xy}$:
>      $$d(e^{xy}) = y e^{xy}\,dx + x e^{xy}\,dy$$
> 
> 3. **Combining differentials:**
>    - Substitute both exact differentials back into the equation:
>      $$d(2x - y^2) + d(e^{xy}) = 0$$
>    - By linearity ($d(A) + d(B) = d(A + B)$):
>      $$d(2x - y^2 + e^{xy}) = 0$$
> 
> 4. **Integrate to find the solution:**
>    - Since $d(F) = 0 \implies F = C$ (a constant):
>      $$2x - y^2 + e^{xy} = C$$


4. Solve the following IVP: 

a. $\begin{array} { r } { y ^ { \prime } = \frac { - 2 x y } { 1 + x ^ { 2 } } ; \quad y ( 2 ) = - 5 } \end{array}$ 
$$
\begin{align}
\frac{1}{-2xy}dy&= \frac{1}{1+x^{2}}dx \\
\frac{1}{y}dy &= -\frac{2x}{1+x^{2}}dx \\
\ln \lvert y \rvert&= -\ln(1+x^{2}) +c \\
\lvert y \rvert&= c_{1}e^{-\ln(1+x^{2})} &&c_{1}= e^{c} \\
&= \frac{c_{1}}{1+x^{2}} \\
y&= \frac{c_{2}}{1+x^{2}} &&c_{2}=\pm c_{1}
\end{align}
$$

Notice that we excluded $y=0$ as a equilibrium solution. But it is in our general solution of one parameter family by setting $c_{2}= 0$.

Substitute the initial condition:
$$
\begin{align}
-5&= \frac{c_{2}}{1+2^{2}} \\
-25&= c_{2}
\end{align}
$$
Thus, $y=-\frac{25}{1+x^{2}}$ is the particular solution for IVP.

> [!remark]
> it is actually first order linear DE: $\frac{dy}{dx}+\left( \frac{2x}{1+x^{2}} \right)y=0$. Thus, by Existence and Uniqueness Theorem for linear equation, since $Q(x)=\frac{2x}{1+x^{2}}$  and $Q(x)=0$ are continuous in $\mathbb{R}$ , thus there exist a unique solution for $x_{0}\in \mathbb{R}$

b. $\begin{array} { r } { \dot { x } = \frac { - x ^ { 2 } } { 2 x t + 1 } ; \quad x ( 1 ) = - 2 } \end{array}$ 

$$
\begin{align}
\frac{dx}{dt}&= \frac{-x^{2}}{2xt+1} \\
-\frac{1}{x^{2}}dx&= \frac{1}{2xt+1}dt \\
-\frac{1}{x}dx- \frac{1}{2xt+1}dt&=0
\end{align}
$$

> [!question] Is it a good way to do so? 
> No if we divide it, then it is very hard to take the partial derivative. Besides that, it is not exact in this case because we alter the equation by multiply a wrong factor $\mu(x,y)$. (In fact this is the idea behind integrating factors,-finding a function that alters a non-exact equation into an exact one!)
> We will only divide it if it is linear to separate the variable but since it is not linear, divide is not favorable here

A simple way:

$$
\begin{align}
\frac{dx}{dt}&= -\frac{x^{2}}{2xt+1} \\
(2xt+1)dx&=-x^{2}dt \\
(2xt+1)dx+x^{2}dt&=0
\end{align}
$$

Let $M(x,y)=2xt+1$ and $N(x,y)=x^{2}$. Note that they are continuous on $\mathbb{R}^{2}$.

Note that
$$
\begin{align}
\frac{\partial M}{\partial t}&= 2x
\end{align}
$$
and
$$
\frac{\partial N}{\partial x}= 2x
$$
which both are continuous on $\mathbb{R}^{2}$. Note that
$$
\frac{\partial M}{\partial t}=\frac{\partial N}{\partial x}
$$
. Thus, by theorem the DE is exact. Hence, there exist a function $f(x,y)$ such that

$$
\begin{align}
f(t,x)&= \int 2xt+1 \, dx +g(t) \\
f(t,x)&=tx^{2}+x+g(t) \\
\frac{\partial f}{\partial t}&= x^{2}+g'(t) \\
x^{2}&=x^{2}+g'(t) \\
g(t)&=c
\end{align}
$$
Thus, $f(t,x)=tx^{2}+x+c$. Hence, $tx^{2}+x=c_{1}$ is the implicit solution of one-parameter family.

Substitute the initial condition:

$$
\begin{align}
1(-2)^{2}-2&=c_{2} \\
c_{2}&= 2
\end{align}
$$

Thus, $x^{2}t+x-2=0$ is the implicit solution.

Explicit solution:

$$
\begin{align}
tx^{2}+x-2&=0
\end{align}
$$
Note that this is a quadratic equation in $x$, thus, by quadratic formula 

$$
\begin{align}
x(t)&= \frac{-1\pm \sqrt{ 1+8t }}{2t}
\end{align}
$$

Check which sign satisfies $x(1)=-2$:
With $+$: $x(1)=1$
With $-$: $x(1)=-2$ (correct). Thus, the explicit solution is

$$
\begin{align}
x(t)= \frac{-1-\sqrt{ 1+8t }}{2t} &&\text{for }t>0
\end{align}
$$


5. Solve $\left( y ^ { 2 } + t y \right) d t + t y d y = 0$ 

Let $M(t,y)=y^{2}+ty$ and $N(t,y)=ty$. Note that there are continuous on $\mathbb{R}^{2}$. Consider their first partial derivative

$$
\begin{align}
\frac{ \partial M }{ \partial y } &=2y+t
\end{align}
$$
and
$$
\begin{align}
\frac{ \partial N }{ \partial t } =y
\end{align}
$$
The DE is not exact. We need to find a integrating factor:

Consider
$$
\begin{align}
\frac{M_{y}-N_{t}}{N}= \frac{2y+t-y}{ty}= \frac{y+t}{ty}
\end{align}
$$

Consider
$$
\frac{N_{t}-M_{y}}{M}= \frac{y-(2y+t)}{y^{2}+ty}=\frac{-y-t}{y(y+t)}=- \frac{1}{y}
$$

Thus, $\mu(y)$ is depending solely on $y$. Thus,
$$
\mu(y)=e^{\int -1/y \, dx }=e^{-\ln \lvert y \rvert}= \frac{1}{y}
$$
Multiply the DE by $\mu(y)= \frac{1}{y}$:

$$
\begin{align}
\frac{1}{y}(\left( y ^ { 2 } + t y \right) d t + t y d y)&=0 \\
(y+t)dt+tdy&=0
\end{align}
$$

Let $M(t,y)=y+t$ and $N(t,y)=t$. Check their exactness:

$$
\begin{align}
\frac{ \partial M }{ \partial y } =1= \frac{ \partial N }{ \partial t } 
\end{align}
$$
Thus, the DE is exact now. By definition there exist a function $f(t,y)$:

$$
\begin{align}
f(t,y)&= \int y+t \, dt +g(y) \\
f(t,y)&=yt+ \frac{t^{2}}{2}+g(y) \\
\frac{ \partial f }{ \partial y } &=t+g'(y) \\
t&=t+g'(y) \\
g(y)&=c
\end{align}
$$
Thus, $f(t,y)=yt+ \frac{t^{2}}{2}+c$. Hence, $yt+ \frac{t^{2}}{2}+c=0$ is the implicit solution of one parameter family.


6. Solve $\begin{array} { r } { \frac { d x } { d t } = \frac { t ^ { 2 } + x ^ { 2 } } { 2 t ^ { 2 } } } \end{array}$ by using substitution method. 

Note that it is a homogeneous DE because let $f(t,x)= \frac{dx}{dt}$. Note that
$$
\begin{align}
f(at,ax)&= \frac{(at)^{2}+(ax)^{2}}{2(at)^{2}} \\
&= \frac{a^{2}(t^{2}+x^{2})}{a^{2}(2t^{2})} \\
&= f(t,x)
\end{align}
$$
Let $x=ut$. Thus $dx=tdu+udt$. Hence,

$$
\begin{align}
\frac{tdu+udt}{dt}&= \frac{t^{2}+(ut)^{2}}{2t^{2}} \\
2t^{2}(tdu+udt)&=(t^{2}+u^{2}t^{2})dt \\
(2t^{2}u-t^{2}-u^{2}t^{2})dt+2t^{3}du&=0 \\
t^{2}(2u-1-u^{2})dt+2t^{3}du&=0 \\
-(u-1)^{2}dt+2tdu&=0 \\
(u-1)^{2}dt&= 2tdu \\
\frac{1}{(u-1)^{2}} \frac{du}{dt}&= \frac{1}{2t} \\
\int \frac{1}{(u-1)^{2}} \, du&= \int  \frac{1}{2t} \, dt \\
-\frac{1}{u-1}&=\frac{\ln \lvert t \rvert}{2}+C \\ 
\frac{1}{1-u}&= \frac{\ln \lvert t \rvert}{2}+C \\
\end{align}
$$
Substitute back $u= \frac{x}{t}$

$$
\begin{align}
\frac{1}{1-\frac{x}{t}}&= \frac{\ln \lvert t \rvert}{2}+C \\
\frac{1}{\left( \frac{t-x}{t} \right)}&= \frac{\ln \lvert t \rvert}{2}+C \\
\frac{t}{t-x}&=  \frac{\ln \lvert t \rvert}{2}+C  \\
t-x&=  \frac{2t}{\ln \lvert t \rvert+C} \\
x(t)&= t- \frac{2t}{\ln \lvert t \rvert+C} \\
&=t\left( 1- \frac{2}{\ln \lvert t \rvert+C} \right)
\end{align}
$$

> [!remark] Remark: Lost/Equilibrium Solution $(u=1)$
> When we divided by $(u-1)^{2}$, we assumed $u \neq 1$. If $u=1\implies \frac{x}{t}=1\implies x(t)=t$.
> 
> $$
> \frac{dx}{dt}=1=  \frac{t^{2}+t^{2}}{2t^{2}}
> $$
> Thus, $x(t)=t$ is also a valid singular solution.

> [!tip] Shortcut: Derivative Form vs. Differential Form
> The product rule for substitution can be written in two equivalent ways:
> - **Differential form:** $dx = t\,du + u\,dt$
> - **Derivative form (divide both sides by $dt$):** $\frac{dx}{dt} = t\frac{du}{dt} + u$
> 
> | If the problem is given in... | Best form to use | Why? |
> | :--- | :--- | :--- |
> | **Derivative form:** $\frac{dx}{dt} = \dots$ | **$\frac{dx}{dt} = t\frac{du}{dt} + u$** | Directly substitutes LHS and avoids cross-multiplying higher powers like $t^3$. |
> | **Differential form:** $M\,dt + N\,dx = 0$ | **$dx = t\,du + u\,dt$** | Matches the existing differentials $dt$ and $dx$. |
> 
> **How to write it on an exam / homework:**
> Given $\frac{dx}{dt} = \frac{t^2 + x^2}{2t^2}$, let $x = ut \implies \frac{dx}{dt} = u + t\frac{du}{dt}$:
> 1. Scale the RHS by dividing numerator and denominator by $t^2$:
>    $$\frac{t^2 + x^2}{2t^2} = \frac{1 + u^2}{2}$$
> 2. Substitute directly into both sides:
>    $$u + t\frac{du}{dt} = \frac{1 + u^2}{2} \implies t\frac{du}{dt} = \frac{1 + u^2 - 2u}{2} = \frac{(u - 1)^2}{2}$$
> 3. Separate variables immediately:
>    $$\frac{1}{(u - 1)^2}\,du = \frac{1}{2t}\,dt$$
> This reaches the separated integral in 2 lines with zero risk of algebraic slips from expanding $2t^2(t\,du + u\,dt)$.

7. By using the substitution $\textstyle y = { \frac { 1 } { v } }$ ,solve $\textstyle x { \frac { d y } { d x } } + y = x y ^ { 2 }$ 

Let $y= \frac{1}{v}$. Thus, the derivative of $y$ with respect to $x$ is 
$$
\begin{align}
\frac{dy}{dx}&=  \frac{-1}{v^{2}} \cdot \frac{dv}{dx}
\end{align}
$$

From question we have
$$
\begin{align}
x \frac{dy}{dx}+y&= xy^{2} \\
\frac{dy}{dx}&= \frac{xy^{2}-y}{x}
\end{align}
$$

Substitute $y= \frac{1}{v}$, we have

$$
\begin{align}
\frac{dy}{dx}&= \frac{x\left( \frac{1}{v} \right)^{2}- \frac{1}{v}}{x} \\
&= \frac{\left( \frac{x-v}{v^{2}} \right)}{x} \\
&= \frac{x-v}{xv^{2}}
\end{align}
$$

$$
\begin{align}
-1v^{-2}\cdot \frac{dv}{dx}&= \frac{x-v}{xv^{2}} \\
\frac{dv}{dx}&= \frac{v-x}{x} \\
\frac{dv}{dx}&= \frac{v}{x}-1 \\
\frac{dv}{dx}- \frac{1}{x}v&=-1
\end{align}
$$

Note that this is a linear DE. Thus, the integrating factor is
$$
\mu(x)=e^{\int -1/x \, dx }=e^{-\ln \lvert x \rvert}+C= \frac{C_{1}}{\lvert x \rvert}= \frac{1}{x}
$$

> [!remark]
> For integrating factor we only need one working factor, so we always drop the absolute value and let $C_{1}=1$.

Multiply DE with $\mu(x)$:

$$
\begin{align}
\frac{d}{dx}\left( \frac{v}{x} \right)&=-\frac{1}{x} \\
\frac{v}{x}&=-\ln \lvert x \rvert+C \\
\frac{1}{xy}&=-\ln \lvert x \rvert+C \\
y(x)&= \frac{1}{-x(\ln x+C_{1})}
\end{align}
$$

Hence, $\frac{1}{-x(\ln x+C_{1})}=y(x)$ is the general solution of one parameter family.


> [!remark]
> This is a Bernoulli's equation. Note that the question is in the form below
> $$
> \frac{dy}{dx}+P(x)y=f(x)y^{n}
> $$
> if we dividing the DE by $x$, then we get
> $$
> \begin{align}
>  { \frac { d y } { d x } } + \frac{1}{x}y = y ^ { 2 }
> \end{align}
> $$
> 
> We can identify $P(x)= \frac{1}{x}$ and $f(x)=1$. Thus, by using Substitution Method we can reduce it into linear DE.
>
>Note that $x=0$ is the singular point (cannot divide by 0). Thus, IVP that involved $x=0$ have no solution

> [!remark] Explicit vs. Implicit Solution & Why It Must Equal $y(x)$ (Not $0$)
> 1. **Why $y(x) = \frac{1}{-x(\ln x+C_{1})}$ and not $\frac{1}{-x(\ln x+C_{1})}=0$:**
>    - The purpose of solving an ODE is to find the unknown function **$y(x)$**. Setting $\frac{1}{-x(\dots)} = 0$ leaves out $y$ entirely! Furthermore, a fraction with $1$ on top can never equal zero ($\frac{1}{\text{anything}} \neq 0$).
> 2. **Standard Solution Formats:**
>    - **Explicit solution:** $y(x) = \frac{1}{-x(\ln x + C_1)} = \frac{1}{x(C - \ln x)}$
>    - **Implicit solution:** $\frac{1}{xy} + \ln x = C \quad \text{or} \quad xy(C - \ln x) = 1$
> 3. **Warning on Constants ($xC \neq C_1$):**
>    - $x$ is a variable and $C$ is an arbitrary constant. You can never absorb a variable $x$ into an arbitrary constant $C_1$—the $x$ must remain attached as $xC$ (or factored as $x(C - \ln x)$).



8. Solve the differential equation $\begin{array} { r } { \cfrac { d P } { d x } = x + 2 P } \end{array}$ , where $P ( 6 ) = 6$ 

$$
\begin{align}
\frac{dP}{dx}-2P&=x
\end{align}
$$

It is a linear DE. Thus, the integrating factor $\mu(x)$ is

$$
\mu(x)=e^{\int -2 \, dx }=e^{-2x}
$$
Multiply DE by $\mu(x)$, we get

$$
\begin{align}
\frac{d}{dx}(e^{-2x}P)&= xe^{-2x} \\
e^{-2x}P&=  \int xe^{-2x} \, dx 
\end{align}
$$
Let $u=x\implies u'=1$ and let $v'=e^{-2x}\implies v= -\frac{1}{2e^{2x}}$. Thus, integration by part

$$
\begin{align}
e^{-2x}P&= -\frac{x}{2e^{2x}}-\int -\frac{1}{2e^{2x}} \, dx \\
&= -\frac{x}{2e^{2x}}- \left( \frac{1}{4e^{2x}}+C \right)  \\
&= \frac{-2x-1}{4e^{2x}}+C_{1} \\
P(x)&= \frac{-2x-1}{4}+ e^{2x}C_{1}
\end{align}
$$
Hence, we obtain the general solution of one-parameter family.

Substitute the initial condition:

$$
\begin{align}
6&= \frac{-2(6)+1}{4}+e^{2(6)}C_{1} \\
6&= -\frac{11}{4}+e^{12}C_{1} \\
C_{1}&= \frac{37}{4}e^{-12}
\end{align}
$$

Thus, $P(x)= \frac{-2x-1}{4}+\left( \frac{37}{4}e^{2(x-6)} \right)$ is the solution for the IVP.
