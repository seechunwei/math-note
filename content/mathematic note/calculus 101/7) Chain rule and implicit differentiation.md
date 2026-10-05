
> [!ABSTRACT] Professional Perspective
> **Geometric View**: The [[Chain Rule]] is the statement that **linear approximations compose by multiplication**. If you zoom in on a composite function, the resulting slope is the product of the local slopes of its components.
> **Operational Tip**: For deep nesting, use "Variable Shields" ($u, v, w \dots$) to isolate the calculus from the bookkeeping.
> **Conceptual Key**: Unlike the Product Rule (which is **parallel** change), the Chain Rule describes **sequential** change (dependency).

## Intuition
The [[Chain Rule]] is essentially about **compounding rates of change**. 

Imagine a sequence of connected gears: **Gear X** $\rightarrow$ **Gear U** $\rightarrow$ **Gear Y**.
* If Gear U turns 3 times faster than Gear X ($g'(x) = 3$), and Gear Y turns 2 times faster than Gear U ($f'(u) = 2$), then Gear Y turns $3 \times 2 = 6$ times faster than Gear X.

In terms of functions, if we have a composite function $f(g(x))$, a tiny change in $x$ is first amplified by the rate of change of the "inside" function $g$, and that result is then further amplified by the rate of change of the "outside" function $f$.

> [!COMPARE] Parallel vs. Sequential Change
> It is common to confuse the [[Chain Rule]] with the [[Product Rule]]. The distinction lies in the **direction of the dependency**:
> 
> **1. Parallel (Product Rule)**: $\frac{d}{dx}[u(x) \cdot v(x)]$
> Here, $u$ and $v$ are "side-by-side." They both depend on $x$ independently. The total change is the **sum** of their individual contributions: *"u changes while v is held constant, plus v changes while u is held constant."*
> 
> **2. Sequential (Chain Rule)**: $\frac{d}{dx}[f(g(x))]$
> Here, there is a **dependency chain**. $x$ drives $g$, and $g$ drives $f$. The total change is the **product** of the amplification factors: *"the rate of the first link multiplied by the rate of the second link."*
> 
> **Mental Shortcut**: If the relationship is "A **and** B," it's Parallel (Product). If the relationship is "A **of** B," it's Sequential (Chain).

$$ \text{Total Rate} = (\text{Rate of } f \text{ relative to } u) \times (\text{Rate of } u \text{ relative to } x) $$

This is why the Leibniz notation is so intuitive:
$$ \frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx} $$
It looks like the $du$ terms "cancel out," reflecting how the change propagates through the chain.

> [!IMPORTANT] Key Insight
> The "Outside-Inside" rule is simply a way of applying this: we find how the outer shell reacts to its input, then multiply by how fast that input is actually changing.


---

> [!theorem] Chain rule
>
> If $f(u)$ is differentiable at $u=g(x)$ and $g(x)$ is differentiable at $x$, then the composite function $(f\circ g)(x)$ is differentiable at $x$, and
> 
> $$
> (f\circ g)'(x)=f'(g(x))\cdot g'(x)
> $$
> 
> In Leibniz notation, if $y=f(u)$ and $u=g(x)$, then
> 
> $$
> \frac{dy}{dx}=\frac{dy}{du}\cdot \frac{du}{dx}
> $$
> 
> where $\frac{dy}{du}$ is evaluated at $u=g(x)$.

How to prove?
We start with the definition of derivative
Let $h(x)=f(g(x))$, its derivative $h'(x)$ is defined as

$$
h'(x)=\lim_{ \triangle x \to 0 } \frac{f(g(x+\triangle x))-f(g(x))}{\triangle x} 
$$
By our intuition we can split the derivative into 2 layer by multiplying  $\frac{\triangle u}{\triangle u}$ where $\triangle u=g(x+\triangle x)- g(x)$. Thus,

$$
\begin{align}
\lim_{ \triangle x \to 0 } \frac{f(g(x+\triangle x))-f(g(x))}{\triangle x} &= \lim_{ \triangle x \to 0 }  \frac{f(g(x+\triangle x))-f(g(x))}{\triangle u} \cdot \frac{\triangle u}{\triangle x}
\end{align}
$$

Notice that $u=g(x)$ can be constant function and $\triangle u=0$. We cannot divide something with $0$ (if $\triangle x$ then we can divide because $\triangle x\neq 0$ by limit)

Thus, this is where linearization come in. Instead of writing derivative as a quotient, we can write it as a product and it is call linear approximation of $f$ at $a$

$$
f(x)-f(a)\approx f'(a)(x-a)
$$
Thus,
$$\begin{align}
f(g(x+\triangle x))-f(g(x))\approx f'(g(x))\cdot \triangle u&&(1)
\end{align}$$
and
$$\begin{align}
g(x+\triangle x)-g(x)\approx g'(x)\cdot \triangle x&&(2)
\end{align}$$

Substitute this (2) into (1) , we get

$$
f(g(x+\triangle x))-f(g(x))\approx f'(g(x))\cdot(g'(x)\cdot \triangle x)
$$

Substitute this into the limit definition:
$$
\begin{align}
\lim_{ \triangle x \to 0 } \frac{f(g(x+\triangle x))-f(g(x))}{\triangle x} &\approx \lim_{ \triangle x \to 0 } f'(g(x))\cdot g(x) \\
&\approx f'(g(x))\cdot g(x)
\end{align}
$$


But this is not rigorous, because it is only approximation, that is why we need the tool **Carathéodory's Definition** $\phi(x)$

> [!definition] Carathéodory’s definition 
> 
> states that a function $g$ is differentiable at $c$ if and only if there exists a function $\phi(x)$ that is **continuous at $c$** such that:
> 
> $$g(x) - g(c) = \phi(x)(x - c)$$
> 
> Where $\phi(c) = g'(c)$.

Instead of saying it _equals_ the derivative times the nudge, we say it equals a **continuous function**  times the nudge:

Thus,

Since $f$ is differentiable at $u$, thus, there exist a continuous function $\phi_{f}$ at $u$ such that 
$$\begin{align}
f(g(x+\triangle x))-f(g(x))= \phi _{f}(g(x+\triangle x))\cdot \triangle u&&(1)
\end{align}$$

and Since $g$ is differentiable at $x$, thus, there exist a continuous function $\phi_{g}$ at $x$ such that 

$$\begin{align}
g(x+\triangle x)-g(x)= \phi_{g}(x+\triangle x)\cdot \triangle x&&(2)
\end{align}$$
Hence,

$$
f(g(x+\triangle x))-f(g(x))= \phi_{f}(g(x+\triangle x))\cdot(\phi_{g}(x)\cdot \triangle x)
$$

Thus, substitute it onto the limit definition

$$
\begin{align}
\lim_{ \triangle x \to 0 } \frac{f(g(x+\triangle x))-f(g(x))}{\triangle x} &= \lim_{ \triangle x \ \to 0 } \frac{\phi_{f}(g(x+\triangle x))\cdot(\phi_{g}(x+\triangle x)\cdot \triangle x)}{\triangle x}
\end{align}
$$

Since $\phi_{f}$ and $\phi_{g}$ are continuous, as $h\to 0$, $\phi_{f}(g(x)+\triangle x)\to\phi_{f}(g(x))$ and $\phi_{g}(x+h)\to\phi_{g}(x)$. Thus,

$$
h'(x)=\phi_{f}(g(x))\cdot\phi_{g}(x)
$$
Since $\phi_{f}(u)=f'(g(x))$ and $\phi_{g}(x)=g'(x)$, we conclude that

$$
(f\circ g)'(x)=f'(g(x)))\cdot g'(x)
$$

> [!IMPORTANT] The "Secret" of Carathéodory: Fixed vs. Moving Points
> A common mistake is to evaluate the helper function $\phi$ at the fixed point $x$ instead of the moving point $x + \Delta x$.
> 
> **Counter-Example**: Let $f(x) = x^2$ at $a = 0$.
> - If we use the fixed point $\phi(0) = f'(0) = 0$, the equation becomes $f(x) - f(0) = 0 \cdot x$, which simplifies to $x^2 = 0$. This is only true at the point $x=0$.
> - If we use the moving point $\phi(x) = x$, the equation becomes $f(x) - f(0) = x \cdot x$, which simplifies to $x^2 = x^2$. This is true for **all** $x$.
> 
> **Key Takeaway**: To maintain a formal equality throughout the proof, $\phi$ must "track" the function at $x + \Delta x$. The limit only converts this moving point back to the fixed point $f'(a)$ at the very final step.



### Outside inside rule
We differentiate the outside function without change the inside function as input and multiply by the derivative of the inside function.

## Generalizations

> [!ABSTRACT] The Linear Algebra Connection: Composition as Multiplication
> The [[Chain Rule]] is not just a formula for 1D functions; it is a specific instance of a much deeper algebraic truth: **The derivative of a composition is the composition of the derivatives.**
> 
> In `[[linear algebra 111]]`, we learn that the composition of two linear transformations is represented by the **multiplication of their matrices**. Since the derivative is essentially the "best linear approximation" of a function, the Chain Rule is actually **Matrix Multiplication in disguise**.
> 
> - **1D Case**: $\text{Slope}_1 \times \text{Slope}_2$ (Multiplication of $1 \times 1$ matrices).
> - **General Case**: $\text{Jacobian}_f \times \text{Jacobian}_g$ (Multiplication of $m \times n$ matrices).
> 
> **Meta-Cognitive Insight**: Whenever you see a "Chain" of dependencies in mathematics or physics, the total rate of change will almost always be a product of the individual rates. This is the fundamental bridge between the continuous world of Calculus and the structural world of Linear Algebra.

> [!INFO] The Derivative as a Linear Transformation
> To understand why the Chain Rule is matrix multiplication, we must realize that the derivative $f'(a)$ is actually a **linear transformation** that maps an input nudge $\Delta x$ to an output change $\Delta y$:
> $$ L(\Delta x) = f'(a) \cdot \Delta x $$
> This mapping satisfies the two requirements of linearity:
> 1. **Scaling**: $L(c \cdot \Delta x) = c \cdot L(\Delta x)$
> 2. **Additivity**: $L(\Delta x_1 + \Delta x_2) = L(\Delta x_1) + L(\Delta x_2)$
> 
> Thus, the "slope" is not just a number; it is the simplest possible linear map from $\mathbb{R} \to \mathbb{R}$. The Chain Rule is simply the composition of two such maps.

---

### Implicit Differentiation

**Formal Definition**: Given an equation $F(x, y) = 0$ that defines $y$ implicitly as a function of $x$, implicit differentiation is the method of finding the derivative $\frac{dy}{dx}$ without requiring an explicit formula for $y$ in terms of $x$.

> [!IMPORTANT] The Rigorous Logic: The Variable Shield
> The core of implicit differentiation is the recognition that $y$ is not an independent variable, but a **function** $y(x)$. Therefore, any term containing $y$ is actually a composite function.
> 
> By the [[Chain Rule]], the derivative of any function $g(y)$ with respect to $x$ is:
> $$ \frac{d}{dx}[g(y)] = \frac{dg}{dy} \cdot \frac{dy}{dx} $$
> This $\frac{dy}{dx}$ factor is the "echo" of the internal dependency of $y$ on $x$.

#### The Systematic Procedure
To find $\frac{dy}{dx}$ for an implicit equation:
1. **Differentiate both sides** of the equation with respect to $x$.
2. **Apply the [[Chain Rule]]** to every term containing $y$. (Every time you differentiate $y$, you must multiply by $\frac{dy}{dx}$).
3. **Apply the [[Product Rule]]** to any terms where $x$ and $y$ are multiplied together (e.g., $x \cdot y(x)$).
4. **Isolate the $\frac{dy}{dx}$ terms** on one side of the equation.
5. **Factor out $\frac{dy}{dx}$** and solve for it algebraically.

#### Detailed Example: The Folium of Descartes
Find $\frac{dy}{dx}$ for the curve defined by:
$$ x^3 + y^3 = 6xy $$

**Step 1: Differentiate both sides with respect to $x$**
$$ \frac{d}{dx}(x^3 + y^3) = \frac{d}{dx}(6xy) $$

**Step 2: Apply differentiation rules**
- For $x^3$: Use power rule $\rightarrow 3x^2$
- For $y^3$: Use [[Chain Rule]] $\rightarrow 3y^2 \cdot \frac{dy}{dx}$
- For $6xy$: Use [[Product Rule]] $\rightarrow 6 \left( x \frac{dy}{dx} + y \cdot 1 \right)$

The equation becomes:
$$ 3x^2 + 3y^2 \frac{dy}{dx} = 6x \frac{dy}{dx} + 6y $$

**Step 3: Isolate $\frac{dy}{dx}$**
Move all terms containing $\frac{dy}{dx}$ to the left and all other terms to the right:
$$ 3y^2 \frac{dy}{dx} - 6x \frac{dy}{dx} = 6y - 3x^2 $$

**Step 4: Factor and Solve**
$$ \frac{dy}{dx} (3y^2 - 6x) = 6y - 3x^2 $$
$$ \frac{dy}{dx} = \frac{6y - 3x^2}{3y^2 - 6x} $$

**Step 5: Simplify**
Dividing both numerator and denominator by 3:
$$ \frac{dy}{dx} = \frac{2y - x^2}{y^2 - 2x} $$

