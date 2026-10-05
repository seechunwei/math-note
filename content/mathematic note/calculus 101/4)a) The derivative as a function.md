Before this we consider derivative at a fixed point. Now, we generalize into a variable.

$$
f'(x)= \lim_{ h \to 0 }  \frac{f(x+h)-f(x)}{h}
$$

> [!question]
> Where is the function $f(x)=|x|$ differentiable?
> 
> - **Case 1: $x > 0$**
> As you correctly showed, when $x$ is strictly positive, the absolute value simplifies to $f(x) = x$. The limit yields a constant slope:
> $$f'(x) = \lim_{h \to 0} \frac{(x+h) - x}{h} = 1$$
> 
> - **Case 2: $x < 0$**
> 
> When $x$ is strictly negative, $f(x) = -x$. The limit yields a constant negative slope:
> 
> $$f'(x) = \lim_{h \to 0} \frac{-(x+h) - (-x)}{h} = -1$$
> 
> - **Case 3: $x = 0$**
> 
> At the origin, the derivative definition requires evaluating the one-sided limits of the difference quotient:
> 
> $$f'(0) = \lim_{h \to 0} \frac{|h|}{h}$$
> 
> - **Left-hand limit ($h \to 0^-$):** Since $h$ approaches from the negative side, $|h| = -h$, meaning $\frac{-h}{h} = -1$.
> 
> - **Right-hand limit ($h \to 0^+$):** Since $h$ approaches from the positive side, $|h| = h$, meaning $\frac{h}{h} = 1$.
> 
> 
> Because the two one-sided limits do not match ($-1 \neq 1$), the general limit does not exist. Geometrically, this manifests as a sharp corner (a "v-shape") at the origin where the slope abruptly jumps from $-1$ to $1$, making a unique tangent line impossible.
> 
> Therefore, its domain of differentiability is:
> 
> $$(-\infty, 0) \cup (0, \infty) \quad \text{or} \quad \mathbb{R} \setminus \{0\}$$
> 

Why does this happen?
To find the derivative at $x=0$, we must examine the limit from both sides. Because the slope differs depending on the direction of approach, the overall limit does not exist, which is visually represented by the sharp corner at the origin.


This is similar to the behavior of floor and ceiling functions:
![[Pasted image 20260415111714.png]]

The derivatives from both sides are different.


Thus, for a function to be differentiable, the limits from both sides must be equal, and the function must be defined at that point. Combining these requirements gives us this theorem:

> [!info] Theorem
> If $f$ is differentiable at $a$, then $f$ is continuous at $a$. 
> (See [[calculus 101/1) The Limit of a Function.md]] and [[calculus 101/2) Continuity.md]] for more on the relationship between limits and continuity).

The converse is false (as seen with the absolute value function). However, the converse is true if we assume the function is "smooth" (meaning its derivative is continuous). 

### When does a function fail to be differentiable?

![[Pasted image 20260415112100.png]]

**When does a function have a vertical tangent?**
A vertical tangent occurs when the limit of the difference quotient approaches $\pm\infty$ as $x \to a$. A classic example is $f(x) = \sqrt[3]{x}$ at $x=0$, where the tangent line becomes perfectly vertical.

### Differentiability over an interval
Notice that when we say a function $f$ is differentiable over an interval, we mean that every number in that interval is differentiable. 

But does that include the endpoints? Differentiability is typically defined on an open interval $(a,b)$. For a closed interval $[a,b]$, we only consider the one-sided derivatives at the endpoints.

> [!question] Why?
> This is because the standard definition of a derivative requires the limit to exist from both sides. At the endpoints of a closed interval $[a, b]$, the function is not defined outside the boundary. Therefore, we can only evaluate the one-sided derivative that is actually possible: the right-hand derivative at $a$ and the left-hand derivative at $b$.


### Higher derivatives 

The instantaneous rate of change of velocity with respect to time is called the acceleration $a(t)$. Thus, the acceleration function is the derivative of the velocity function denoted by

$$
a(t)=v'(t)=s''(t)
$$

or in Leibniz notation

$$
a= \frac{dv}{dt}= \frac{d^{2}s}{dt^{2}}
$$

---
**Next Steps:** [[calculus 101/5) Differentiation Formulas.md]]
