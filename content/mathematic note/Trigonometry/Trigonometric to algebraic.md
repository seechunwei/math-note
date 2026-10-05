is it possible rewrite any composition of trigonometric in algebraic equation?

1) $T_{1}(T^{-1}_{2}(x))$ can always be written as algebraic expression.


The answer is no. Let $T(x)$ be any trigonometric function and $T^{-1}(x)$ be any inverse of trigonometric function.

Case 1:  $T_{1}(T^{-1}_{2}(x))$ can be always be rewrite as algebraic equation.

Why? $T_{2}^{-1}(x)$ is the real number $t$ and $x$ is any ratio of the angle. Given any ratio of the $t$, can we find the $t$? Of course, because any coordinate in the unit circle can be reach by certain $t$.

In another point of view, Given any ratio of the the angle , can we find the unique $\theta$. Yes, we can always construct a reference right triangle where one ratio is $x$. 

But the $t$ or $\theta$ here are restricted to a certain domain. This $t$ or $\theta$ be a element that map to certain ratio by $T_{1}(x)$.

There are exactly 36 possible combinations of the 6 standard trigonometric functions ($\sin, \cos, \tan, \sec, \csc, \cot$) and their inverses. Every single one of them reduces to an algebraic form.

If you let $y = T_2^{-1}(x)$, then by definition $T_2(y) = x$. You can always construct a reference right triangle where one ratio of sides is $x$ (or $\frac{x}{1}$).

By the Pythagorean theorem, the third side will always be one of three forms:

- $\sqrt{1 - x^2}$
    
- $\sqrt{x^2 + 1}$
    
- $\sqrt{x^2 - 1}$


Case 2: $T_{1}^{-1}(T_{2}(x))$

Example: Range of $\sin x$ is $[-1,1]$ while domain of $\sin ^{-1}x$ is $[-1,1]$. Thus $\sin ^{-1}(\sin x)$ is well defined. 

Inner functions like $\sin x$ or $\tan x$ are periodic they repeat infinitely. Inverse functions like $\sin^{-1}x$ can only output values within a strict, restricted interval (the principal range).

Because of this, functions like $y = \sin^{-1}(\sin x)$ or $y = \tan^{-1}(\tan x)$ form infinite, repeating **sawtooth or triangle waves**.

Here is the problem: standard algebraic tools (like $x^2$, $\sqrt{x}$, or fractions) are smooth and predictable. They cannot draw an infinite chain of sharp, repeating zigzags that go on forever.

But in second case since it is oscillating then we can still form a piecewise function that form by finite formula. For example,

For $y = \sin^{-1}(\sin x)$, a single full cycle lives between $-\frac{\pi}{2}$ and $\frac{3\pi}{2}$. We can write a clean, **finite piecewise function** for just that window:

$$f(x) = \begin{cases} x & \text{if } -\frac{\pi}{2} \leq x \leq \frac{\pi}{2} \\ \pi - x & \text{if } \frac{\pi}{2} < x \leq \frac{3\pi}{2} \end{cases}$$

Then, to make it cover the entire real number line, we just add the periodic rule:

$$f(x + 2\pi) = f(x)$$
