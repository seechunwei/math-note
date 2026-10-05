
## Tangent 
How to find a tangent at one point?

Consider a curve function $y=f(x)$, if we want to construct a tangent line at $(a,f(a))$ , then we need to consider a nearby point $(x,f(x))$, where $x \neq a$,

$$
m= \frac{f(x)-f(a)}{x-a}
$$

Imagine that the distance between 2 point get closer and closer, and the tangent line will become more accurate. We can use the limit here to indicate the process of getting near.

Thus,

> [!definition]
> The tangent line to the curve $y=f(x)$ at the point $P(a,f(a))$ is the line though $P$ with slope
> 
> $$
> m=\lim_{ x \to a } \frac{f(x)-f(a)}{x-a} 
> $$
> 
> Or
> $$
> m=\lim_{ h \to 0 } \frac{f(a+h)-f(a)}{h}
> $$
> provided that this limit exists.

> [!question]
> When does the derivative fail to exist?
> When there is a sharp turn or it is a infinite limit (vertical tangent.)

The first one use 2 different point while the second one use the fixed point as base point.


## Velocities

Velocity=$\frac{\text{change of displacement}}{\text{change of time}}$

Thus, the question is what is the instantaneous velocity at $t=a$?

> [!definition]
> We define the instantaneous velocity at $t=a$ to be the limit of this average velocity
> $$
> v(a)=\lim_{ h \to 0 } \frac{f(a+h)-f(a)}{h} 
> $$
> 

## Derivatives

> [!definition]
> The derivative as instantaneous change at one point denoted by $f'(a)$, is
> 
> $$
> f'(a)= \lim_{ h \to 0 } \frac{f(a+h)-f(a)}{h} 
> $$
> if this limit exists.


Thus, we can define tangent line as

> [!definition]
> The tangent line to $y=f(x)$ at $(a,f(a))$ is the line though $(a,f(a))$ whose slope is equal to $f'(a)$, the derivative of $f$ at $a$.
> 

### Rate of change

Suppose $y$ is a quality that depends on another quantity $x$. Thus, $y$ is a function of $x$ and we write $y=f(x)$.

if $x$ change from $x_{1}$ to $x_{2}$, then the change in $x$ (also called the increment of $x$) is

$$
\triangle x=x_{2}-x_{1}
$$
and the corresponding change in $y$ is

$$
\triangle y=f(x_{2})-f(x_{1})
$$

> [!definition]
> The quotient;
> 
> $$
> \frac{\triangle y}{\triangle x}= \frac{f(x_{2})-f(x_{1})}{x_{2}-x_{1}}
> $$
> is called the average rate of change of $y$ with respect to $x$ over the interval $[x_{1},x_{2}]$.

(This is actually gradient)

> [!definition] Instantaneous rate of change 
> $$
> \lim_{ \triangle x \to 0 } \frac{\triangle y}{\triangle x}=\lim_{ x_{2} \to x_{1} } \frac{f(x_{2})-f(x_{1})}{x_{2}-x_{1}} 
> $$

Connect this with derivative, we have 

> [!remark]
> The derivative $f'(a)$ is the instantaneous rate of change of $y=f(x)$ with respect to $x$ when $x=a$.



## Exercise: Particle Motion

> [!example] Problem
> A particle moves along a straight line, and its position (in meters) at time $t$ (in seconds) is given by $s(t) = t^3 - 6t^2 + 9t$. 
> Find the instantaneous velocity at $t = 2$ using the limit definition of the derivative.

> [!answer]  Solution
> We want to find $v(2) = s'(2) = \lim_{ h \to 0 } \frac{s(2+h)-s(2)}{h}$.
> 
> 1. Calculate $s(2)$:
>    $s(2) = 2^3 - 6(2^2) + 9(2) = 8 - 24 + 18 = 2$
> 
> 2. Set up the limit:
>    $$
>    \begin{align}
>    v(2) &= \lim_{ h \to 0 } \frac{(2+h)^3 - 6(2+h)^2 + 9(2+h) - 2}{h} \\
>         &= \lim_{ h \to 0 } \frac{(8 + 12h + 6h^2 + h^3) - 6(4 + 4h + h^2) + 18 + 9h - 2}{h} \\
>         &= \lim_{ h \to 0 } \frac{8 + 12h + 6h^2 + h^3 - 24 - 24h - 6h^2 + 18 + 9h - 2}{h} \\
>         &= \lim_{ h \to 0 } \frac{-3h + h^3}{h} \\
>         &= \lim_{ h \to 0 } (-3 + h^2) \\
>         &= -3 \text{ m/s}
>    \end{align}
>    $$
