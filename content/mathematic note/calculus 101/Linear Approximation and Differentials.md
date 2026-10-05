

A curve lies very close to its tangent line near the point of tangency , in fact by zooming in toward a point on the graph of a differentiable function, we noticed that the graph looks more and more like its tangent line.

We use the tangent line at $(a,f(a))$ as an approximation to the curve $y=f(x)$ when $x$ is near $a$. The equation of this tangent line is

$$
\begin{align}
y-f(a)&=f'(a)(x-a) \\
y&=f'(a)(x-a)+f(a)
\end{align}
$$

and the approximation

$$
f(x)\approx f(a)+f'(a)(x-a)
$$
is called the **linear approximation** or **tangent line approximation** of $f$ at $a$.

The linear function whose graph is this tangent line, that is,

$$
L(x)=f(a)+f'(a)(x-a)
$$
is called the **linearization** of $f$ at $a$.

Remark:
Notice that the text above looking at the exact same algebraic expression through **three entirely different conceptual lenses**: Geometry, Numerical Estimation, and Pure Function Theory.

> [!cite] Remark
> ### The Tangent Line (The Geometric Object)
> 
> $$y = f(a) + f'(a)(x-a)$$
> 
> - **The Core Focus:** The infinite straight line sitting in the $xy$-plane.
>     
> - **Why it's written this way:** This uses standard coordinate geometry (the point-slope form $y - y_1 = m(x - x_1)$). It treats the line as a physical, geometric landmark that touches the curve $f(x)$ perfectly at the point $(a, f(a))$. It answers the question: _What is the equation of the line that grazes this curve?_
>     
> 
> ### 2. The Linear Approximation (The Practical Estimation)
> 
> $$f(x) \approx f(a) + f'(a)(x-a) \quad \text{for } x \text{ near } a$$
> 
> - **The Core Focus:** A calculation tool to estimate difficult numbers.
>     
> - **Why it's written this way:** Notice the **$\approx$ (approximately equal to)** symbol. This is not an equation for a line; it is an arithmetic relationship. It tells you that if you plug an $x$-value that is very close to $a$ into the simple line equation, the output will be practically identical to the complicated true value of $f(x)$.
>     
> - **Example:** If you want to estimate $\sqrt{4.01}$ without a calculator, you set $f(x) = \sqrt{x}$ and $a = 4$. This statement tells you that $\sqrt{4.01} \approx 2 + \frac{1}{4}(4.01 - 4) = 2.0025$.
>     
> 
> ### 3. The Linearization (The Formal Function)
> 
> $$L(x) = f(a) + f'(a)(x-a)$$
> 
> - **The Core Focus:** Creating a brand new, well-behaved linear function.
>     
> - **Why it's written this way:** In pure mathematics, we love to study functions as self-contained machines. By defining $L(x)$ as a distinct function, we can now mathematically analyze it in isolation.
>     
> - We can take its derivative, find its domain, or subtract it from the original function to calculate a brand new function representing the error: $E(x) = f(x) - L(x)$. It elevates a simple line equation into a formal mathematical tool.


Example:
Find the linearization of the function $f(x)=\sqrt{ x+3 }$ at $a=1$ and use it to approximate the numbers $\sqrt{ 3.98 }$ and $\sqrt{ 4.05 }$. Are these approximations overestimates or underestimates?

Linearization at $a=1$:
$$
\begin{align}
L(x)&=f(a)+f'(a)(x-a) \\
\end{align}
$$

$$
f(a)=2
$$
$$
f'(x)= \frac{1}{2}(x+3)^{-1/2}= \frac{1}{2\sqrt{ x+3 }}
$$
Thus,

$$
f'(1)= \frac{1}{2\sqrt{ 1+3 }}= \frac{1}{4}
$$

Hence,

$$
L(x)=2+ \frac{1}{4}(x-1)
$$

Approximate the number $\sqrt{ 3.98 }=\sqrt{ 0.98+3 }$. Thus,

$$
L(0.98)= 1.995
$$
Approximate the number $\sqrt{ 4.05 }=\sqrt{ 1.05+3 }$.
Thus,

$$
L(1.05)=2.0125
$$

To determine this rigorously without looking at a calculator, we check the **concavity** of the original function by taking the second derivative.

$$f''(x) = -\frac{1}{4}(x+3)^{-3/2} = -\frac{1}{4\sqrt{(x+3)^3}}$$

$f''(x)$ is **strictly negative** ($f''(x) < 0$). A negative second derivative means the graph of $f(x)$ is **concave down** (it bends downward like a dome).

Thus, the tangent line at $a=1$ is above the graph $f(x)$, thus, it is overestimate.


> [!question]
> Can we use $\sqrt{ x }$ to do approximation? 
> Can and the final answers are **exactly identical** to the previous method.
> 
> Geometrically, the function $f(x) = \sqrt{x+3}$ is just the standard graph of $f(x) = \sqrt{x}$ shifted **3 units to the left**.
> 
> Because the entire graph moved left by 3 units, the "sweet spot" where the perfect square lives also moved left by 3 units: from $x = 4$ down to $x = 1$.

## Differentials

The ideas behind linear approximations are sometimes formulated in the terminology and notation of differentials

If $y=f(x)$ where $f$ is a differentiable function

The differential $dy$ is defined in terms of $dx$ by the equation

$$
dy=f'(x)dx
$$
(It is actually linearization above)

![[Pasted image 20260623220219.png]]

And this is the reason why we can perform the substitution rule by the algorithm. 

The change in $y$ of $f$ is
$$
\triangle y=f(y+\triangle x)-f(x)
$$


> [!question]
> Our final example illustrates the use of differentials in estimating the errors that occur because of approximate measurements
> 
> The radius of a sphere was measured and found to be 21 cm with a possible error in measurement of at most 0.05 cm. What is the maximum error in using this value of the radius to compute the volume of the sphere?

Solution:

Before answer the question, we need to know something

Let's go back to the formal definition of the derivative for the volume function $V(r)$:
$$
V'(r)=\lim_{ \triangle r \to 0 } \frac{\triangle V}{\triangle r} 
$$
Where $\Delta r$ is the actual error in the radius, and $\Delta V$ is the actual resulting error in the volume ($V(r + \Delta r) - V(r)$).

When the error $\Delta r$ is **extremely small** (like $0.05\text{ cm}$ compared to a large $21\text{ cm}$ radius), we don't even need to take the limit to infinity. The difference quotient is already _almost equal_ to the derivative:

$$\frac{\Delta V}{\Delta r} \approx V'(r)$$

If we multiply both sides of this approximation by $\Delta r$, we get:

$$\Delta V \approx V'(r) \cdot \Delta r$$o turn this approximation into an clean, operational equation, mathematicians **defined** two new variables called differentials ($dr$ and $dV$):

- We define **$dr = \Delta r$** (the differential of the independent variable is exactly equal to the real change).
    
- We define **$dV = V'(r) \, dr$** (the differential of the dependent variable is the _estimated_ change).
    

Therefore, because $\Delta V \approx V'(r) \Delta r$, it means:

$$\text{Actual Error } (\Delta V) \approx \text{Estimated Error } (dV)$$

Thus go back to the question.
The error of radius is $\triangle r=dr=0.05$ and we need to find $\triangle V$ using $dV$ as approximation.

The formula of volume of a sphere is

$$
V= \frac{4}{3}\pi r^{3}
$$
Thus, 

$$dV = V'(r) \, dr$$$$dV = \left(4\pi r^2\right) dr$$
We are given:

- Measured radius, $r = 21\text{ cm}$
    
- Maximum error in radius, $dr = 0.05\text{ cm}$
    

Plugging these into our differential equation:

$$dV = 4\pi (21)^2 (0.05)$$

$$dV = 4\pi (441) (0.05)$$

$$dV = 1764\pi (0.05)$$

$$dV = 88.2\pi\text{ cm}^3$$

If we approximate $\pi \approx 3.14159$:

$$dV \approx 88.2 \times 3.14159 \approx \mathbf{277.09\text{ cm}^3}$$

[[approximation]] 