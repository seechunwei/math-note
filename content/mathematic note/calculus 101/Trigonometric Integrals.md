The strategies shown in **image_64c777.png** are used to solve trigonometric integrals where you cannot easily use a standard $u$-substitution because there isn't an "odd man out" power to act as your $du$. By converting the even powers into linear terms with double angles, the integration becomes straightforward.

Here are two classic examples showing how to apply these rules.

### Example 1: Standard Application of a Half-Angle Identity

**Problem:** Evaluate the indefinite integral:

$$\int \sin^2 x \, dx$$

**Solution:**

We cannot use $u$-substitution here directly. Following the rule in **image_64c777.png**, we substitute the identity $\sin^2 x = \frac{1}{2}(1 - \cos 2x)$ into the integrand:

$$\int \sin^2 x \, dx = \int \frac{1}{2}(1 - \cos 2x) \, dx$$

Pull out the constant $\frac{1}{2}$ and integrate the terms individually:

$$= \frac{1}{2} \int (1 - \cos 2x) \, dx$$

$$= \frac{1}{2} \left( x - \frac{\sin 2x}{2} \right) + C$$

$$\mathbf{= \frac{1}{2}x - \frac{1}{4}\sin 2x + C}$$

### Example 2: Using the "Sometimes Helpful" Identity

**Problem:** Evaluate the indefinite integral:

$$\int \sin^2 x \cos^2 x \, dx$$

**Solution:**

Both powers are even, so we could substitute both half-angle formulas. However, the second identity listed in **image_64c777.png** ($\sin x \cos x = \frac{1}{2}\sin 2x$) offers a much faster path.

First, rewrite the integrand as a perfect square:

$$\sin^2 x \cos^2 x = (\sin x \cos x)^2$$

Now, substitute the identity inside the parenthesis:

$$= \left( \frac{1}{2}\sin 2x \right)^2 = \frac{1}{4}\sin^2 2x$$

Now substitute this back into our integral:

$$\int \sin^2 x \cos^2 x \, dx = \int \frac{1}{4}\sin^2 2x \, dx$$

We still have an even power ($\sin^2 2x$), so we apply the first half-angle identity again. Be careful with the angle—since the current angle is $2x$, doubling it makes it $4x$:

$$\sin^2 2x = \frac{1}{2}(1 - \cos 4x)$$

Substitute this expression back in:

$$= \int \frac{1}{4} \cdot \frac{1}{2}(1 - \cos 4x) \, dx$$

$$= \frac{1}{8} \int (1 - \cos 4x) \, dx$$

Finally, perform the integration:

$$= \frac{1}{8} \left( x - \frac{\sin 4x}{4} \right) + C$$

$$\mathbf{= \frac{1}{8}x - \frac{1}{32}\sin 4x + C}$$

> [!remark]
> Lower powering formula $\sin ^{2}x=\frac{1}{2}(1-\cos 2x)$ because $\cos 2x=1-\sin ^{2}x$
> and $\sin 2x=2\sin x\cos x\implies \sin x\cos x=\frac{1}{2}\sin 2x$ 
> 

---

$$
\int \tan dx=\ln|\sec x|+c
$$

$$
\int \sec xdx=\ln|\sec x+\tan x|+C
$$
