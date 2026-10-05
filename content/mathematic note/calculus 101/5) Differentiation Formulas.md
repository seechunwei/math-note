### Constant function

> [!theorem] Derivative of a constant function
> 
> $$
> \frac{d}{dx}(c)=0
> $$
> 

$$
\begin{align}
f'(x)&=\lim_{ h \to 0  } \frac{f(h+x)-f(x)}{h}  \\
&=\lim_{ h \to 0 } \frac{c-c}{h}  \\
&=0
\end{align}
$$

Why? because $h \neq 0$.


### Power functions

$f(x)=x^{n}$
If $n =1$, then $f(x)=x$, the graph is a straight line, thus the slope is 1 which is $f'(x)=1$.


If $n =2$, then $f(x)=x^{2}$, the graph is a parabola curve, thus

$$
\begin{align}
f'(x)&=\lim_{ h \to 0 } \frac{f(h+x)-f(x)}{h} \\
&=\lim_{ h \to 0 }  \frac{(x+h)^{2}-x^{2}}{h} \\
&=\lim_{ h \to 0 }  \frac{2hx+h^{2}}{h}  \\
&=\lim_{ h \to 0 } 2x+h \\
&=2x
\end{align}
$$


![[Pasted image 20260425222618.png]]

The term is always the second term of the binomial expansion without another term

Thus, we can start see the pattern and it is reasonable to make a guess

> [!theorem] The Power Rule
> If $n$ is a positive integer, then 
> $$
> \frac{d}{dx}(x^{n})=nx^{n-1}
> $$
> 

## New Derivatives from Old



> [!theorem] The Constant Multiple Rule
> 
> If $c$ is a constant and $f$ is a differentiable function.
> $$
> \frac{d}{dx}[cf(x)]=c \frac{d}{dx}f(x)
> $$
> 

> [!remark]
> The constant stretch or compress vertically, which is change the value of $f(x)$, thus, the slope will change proportionally.
> 

> [!theorem] The Sum Rule
> If $f$ and $g$ are both differentiable, then
> $$
> \frac{d}{dx}[f(x)+g(x)]=\frac{d}{dx}f(x)+\frac{d}{dx}g(x)
> $$

Proof:

$$
\begin{align}
\frac{d}{dx}[f(x)+g(x)]&= \lim_{ h \to 0 } \frac{[f(x+h)+g(x+h)]-[f(x)+g(x)]}{h} \\
&= \lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h}+\lim_{ h \to 0 } \frac{g(x+h)-g(x)}{h} \\
&=f'(x)+g'(x)
\end{align}
$$

By writing $f-g$ as $f+(-1)g$ and applying the Sum Rule and the Constant Multiple Rule, we get the following formula: 

> [!theorem] The difference rule
> 
> If $f$ and $g$ are both differentiable, then
> 
> $$
> \frac{d}{dx}[f(x)-g(x)]=\frac{d}{dx}f(x)-\frac{d}{dx}g(x)
> $$

> [!theorem] The product rule
> If $f$ and $g$ are both differentiable, then
> 
> $$
> \frac{d}{dx}[f(x)g(x)]=\frac{d}{dx}g(x)f(x)+\frac{d}{dx}f(x)g(x)
> $$
> 

Proof:
$$
\begin{align}
\frac{d}{dx}[f(x)g(x)]&=\lim_{ h \to 0 } \frac{f(x+h)g(x+h)-f(x)g(x)}{h}  \\
&=\lim_{ h \to 0 } \frac{f(x+h)g(x+h)-f(x)g(x+h)-f(x)g(x)+f(x)g(x+h)}{h} \\
&=\lim_{ h \to 0 }  \frac{g(x+h)[f(x+h)-f(x)]+f(x)[g(x+h)-g(x)]}{h} \\
&= g(x)\lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h}+f(x)\lim_{ h \to 0 }  \frac{g(x+h)-g(x)}{h}
\end{align}
$$
This step follow by $\lim_{ x \to a }f(x)g(x)=\lim_{ x \to  a}f(x)\cdot \lim_{ x \to a }g(x)$ and same as addition.

Thus it follow that 

$$
g(x)f'(x)+f(x)g'(x)
$$

> [!question]
> How to understand this intuitively?
> The Geometric Intuition: The Growing Rectangle
> 
> Imagine a rectangle where the width is $f(x)$ and the height is $g(x)$. The area of this rectangle is $A=f(x)g(x)$
> 
> Now imagine that $x$ increases by a tiny amount, $\triangle x$. 
> The width: $f(x+\triangle x)=f(x)+\triangle f$
> The height: $g(x+\triangle x)=g(x)+\triangle g$
> 
> The new area is:
> $$
> \text{New Area}=(f+\triangle f)(g+\triangle g)
> $$
> If you expand this, you get:
> 
> $$
> \text{New Area}=fg+f\triangle g
> + g\triangle f+\triangle f\triangle g$$
> 
> The change of area:
> $$
> \triangle A=f \triangle g+g \triangle f+ \triangle f \triangle g
> $$
> To find the derivative, we divide by $\triangle x$ and let $\triangle x\to 0$
> 
> $$
> \frac{\triangle A}{\triangle x}= f \frac{\triangle g}{\triangle x}+g \frac{\triangle f}{\triangle x}+ \frac{\triangle f \triangle g}{\triangle x}
> $$
> 
> What about that last term, $\frac{df \cdot dg}{dx}$? Visually, this represents the tiny, insignificant corner of the expanded rectangle. Mathematically, because both $df$ and $dg$ are shrinking to zero, their product shrinks _orders of magnitude faster_ than the other terms. It becomes a higher-order infinitesimal and vanishes to $0$.


> [!theorem]
> The Quotient Rule
> If $f$ and $g$ are differentiable, then
> 
> $$
> \frac{d}{dx}\left[ \frac{f(x)}{g(x)} \right]= \frac{g(x)f'(x)-f(x)g'(x)}{[g(x)]^{2}}
> $$
> 

Proof:
Using the same idea of product rule

> [!theorem] General power functions
> The Quotient Rule can be used to extend the Power Rule to the case where the exponent is a negative integer.
> 
> If $n$ is a real integer, then
> $$
> \frac{d}{dx}(x^{-n})=nx^{-n-1}
> $$
> 

## Connections

> [!INFO] Meta-Cognitive Strategy Guide
> 
> **1. The Limit Definition (The "Hammer")**
> - **Note**: [[calculus 101/4) Derivatives and rates of change.md]]
> - **Trigger**: Use when you need to prove a rule from first principles, or when a function is defined such that standard formulas don't yet apply.
> - **Boundary**: Fails when the limit does not exist (e.g., sharp turns, jump discontinuities) or when the algebra is so complex that you first need a trigonometric or algebraic identity to simplify the expression.
> 
> **2. Algebraic Intervention (The "Decoupler")**
> - **Note**: [[calculus 101/6) Formula for derivative of trigonometric function.md]]
> - **Trigger**: Use when two variables are coupled (changing simultaneously) and you cannot separate them to apply limit laws (e.g., the $f(x+h)g(x+h)$ "stuck" feeling).
> - **Boundary**: Fails if the intervention introduces new singularities (like division by zero) or if the function's growth is so erratic that "freezing" one variable doesn't actually simplify the limit.
> 
> **3. Geometric Bounding (The "Trap")**
> - **Note**: [[calculus 101/Squeeze Theorem.md]]
> - **Trigger**: Use when dealing with oscillating functions (like $\sin x, \cos x$) where a direct algebraic limit is difficult, but you can "trap" the function between two simpler ones that converge to the same point.
> - **Boundary**: Fails if you cannot find two bounding functions that converge to the same limit, or if the "trap" is too loose to force the target function to a single value.

## Professional Perspective

> [!ABSTRACT] The Mathematician's Mental Model
> 
> While the formulas are useful for calculation, a professional mathematician views the Product Rule through the lens of **Linearization**.
> 
> **1. The Core Intuition: Weighted Changes**
> Instead of a formula, see the product $f \cdot g$ as a system. The change in the product is the sum of the changes of its components, each weighted by the other component:
> $$d(fg) = f \cdot dg + g \cdot df$$
> 
> **2. The Professional Trick: The Differential View**
> Experts often stop thinking in terms of $\frac{d}{dx}$ and switch to **Differentials**. This allows them to apply the rule to objects that aren't that are not just functions of $x$ (like tensors or manifolds), treating the derivative as a **Linear Map**.
> 
> **3. The Comparison: Parallel vs. Sequential**
> - **Product Rule (Parallel)**: $f$ and $g$ change simultaneously. Their effects are added.
> - **Chain Rule (Sequential)**: One change triggers another. Their effects are multiplied.
> 
> **Advanced Search Terms for Further Study**:
> - *Leibniz rule for differentiation*
> - *Differential forms*
> - *First-order Taylor approximation*
> - *Linear Map*
