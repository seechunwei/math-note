To find the derivative of $\sin x$, we have to return to the fundamental limit definition of a derivative:

$$\frac{d}{dx} \sin x = \lim_{h \to 0} \frac{\sin(x+h) - \sin x}{h}$$

Using the angle addition identity $\sin(x+h) = \sin x \cos h + \cos x \sin h$, we can expand the numerator:

$$= \lim_{h \to 0} \frac{\sin x \cos h + \cos x \sin h - \sin x}{h}$$

$$= \lim_{h \to 0} \left( \sin x \frac{\cos h - 1}{h} + \cos x \frac{\sin h}{h} \right)$$Here, we rely on two geometric limit proofs: $\lim_{h \to 0} \frac{\sin h}{h} = 1$ and $\lim_{h \to 0} \frac{\cos h - 1}{h} = 0$. Substituting these in:

$$= \sin x \cdot (0) + \cos x \cdot (1) = \cos x$$

[[Squeeze Theorem]]

### . The Limit Definition

We start with the fundamental definition of the derivative for $f(x) = \cos x$:

$$\frac{d}{dx} \cos x = \lim_{h \to 0} \frac{\cos(x+h) - \cos x}{h}$$

### 2. The Angle Addition Identity

To expand the term $\cos(x+h)$, we use the cosine addition formula: $\cos(\alpha + \beta) = \cos \alpha \cos \beta - \sin \alpha \sin \beta$.

Substituting this into our limit gives:

$$= \lim_{h \to 0} \frac{(\cos x \cos h - \sin x \sin h) - \cos x}{h}$$

### 3. Rearrange and Factor

Now, we group the terms that share a $\cos x$ so we can factor it out:

$$= \lim_{h \to 0} \frac{\cos x \cos h - \cos x - \sin x \sin h}{h}$$

$$= \lim_{h \to 0} \frac{\cos x (\cos h - 1) - \sin x \sin h}{h}$$

### 4. Split the Fractions

Just like we did with the sine derivation, we can split this into two separate fractions:

$$= \lim_{h \to 0} \left( \cos x \frac{\cos h - 1}{h} - \sin x \frac{\sin h}{h} \right)$$

### 5. Evaluate the Known Limits

This is where all the groundwork pays off. We can now plug in the two foundational geometric limits:

- We just proved that $\lim_{h \to 0} \frac{\cos h - 1}{h} = 0$.
    
- We know the geometric truth that $\lim_{h \to 0} \frac{\sin h}{h} = 1$.
    

Substitute these values in:

$$= \cos x \cdot (0) - \sin x \cdot (1)$$

$$= 0 - \sin x$$

$$= -\sin x$$


## Deriving Tangent

Since $\tan x = \frac{\sin x}{\cos x}$, we set $f(x) = \sin x$ and $g(x) = \cos x$.

$$\frac{d}{dx} \tan x = \frac{\cos x (\cos x) - \sin x (-\sin x)}{\cos^2 x}$$

$$= \frac{\cos^2 x + \sin^2 x}{\cos^2 x}$$

By the Pythagorean identity, $\cos^2 x + \sin^2 x = 1$. Therefore:

$$\frac{d}{dx} \tan x = \frac{1}{\cos^2 x} = \sec^2 x$$
## Deriving Secant

Write secant as $\sec x=(\cos x)^{-1}$ and apply the chain rule.

$$
\begin{align}
\frac{d}{dx}(\cos x)^{-1}&=-1(\cos x)^{-2}\cdot(-\sin x) \\
&= \frac{\sin x}{\cos ^{2}x} \\
&= \frac{\sin x}{\cos x} \cdot \frac{1}{\cos x} \\
&=\tan x\cdot \sec x
\end{align}
$$
Thus, $\frac{d}{dx}\sec x=\sec x\tan x$.

The Underlying Symmetry: The "Co-" Functions

- **Sine** becomes **Cosine** ($\cos x$) $\rightarrow$ **Cosine** becomes **Negative Sine** ($-\sin x$).
    
- **Tangent** becomes $\sec^2 x$ $\rightarrow$ **Cotangent** becomes $-\csc^2 x$. You can easily prove this by differentiating $\frac{\cos x}{\sin x}$ via the quotient rule, resulting in $\frac{d}{dx}\cot x=-\csc^{2}x$

**Secant** becomes $\sec x \tan x$ $\rightarrow$ **Cosecant** becomes $-\csc x \cot x$. Again, proven by differentiating $(\sin x)^{-1}$, giving us $\frac{d}{dx}\csc x=-\csc x\cot x$.

---
$$
\begin{align}
\int \tan x \, dx&=\int  \frac{\sin x}{\cos x} \, dx \\
\end{align}
$$

We use $u$-substitution. Let $u=\cos x$ Why? (because $-\sin x$ is the derivative of $\cos x$) 
Thus,
$du= -\sin x~dx$ $\implies$ $-du=\sin x~dx$. Thus,

$$
\begin{align}
\int \tan x \, dx&= \int \frac{1}{u} \, -du \\
&=-\int \frac{1}{u} \, du
\end{align}
$$
The integral of $\frac{1}{u}$ is a fundamental calculus identity that results in the natural logarithm:

$$-\int \frac{1}{u} \, du = -\ln|u| + C$$

Thus, by substitution

$$
\int \tan xdx=-\ln|\cos x|+C
$$


How about

$$
\int \sec x dx
$$
## Method 1: The Logical Approach (No Magic Tricks)

If you don't want to memorize a random shortcut, you can derive the integral using basic definitions, a Pythagorean identity, and **Partial Fractions**.

Start by rewriting $\sec x$ in terms of cosine:

$$\int \sec x \, dx = \int \frac{1}{\cos x} \, dx$$

To create a situation where we can use a $u$-substitution, multiply the top and bottom by $\cos x$:

$$= \int \frac{\cos x}{\cos^2 x} \, dx$$

Now use the identity $\cos^2 x = 1 - \sin^2 x$:

$$= \int \frac{\cos x}{1 - \sin^2 x} \, dx$$

### Step 1: Substitution

Let $u = \sin x$, which means $du = \cos x \, dx$. Substituting these in gives a pure rational function:

$$\int \frac{1}{1 - u^2} \, du$$

### Step 2: Partial Fractions

We can factor the denominator as $(1-u)(1+u)$ and split the fraction apart:

$$\frac{1}{(1-u)(1+u)} = \frac{A}{1-u} + \frac{B}{1+u}$$

Solving for the constants yields $A = \frac{1}{2}$ and $B = \frac{1}{2}$. Now, substitute them back into the integral:

$$= \int \left( \frac{1/2}{1-u} + \frac{1/2}{1+u} \right) \, du$$

### Step 3: Integrate

Integrate both terms carefully (watching out for the chain rule's negative sign on the first term):

$$= -\frac{1}{2}\ln|1-u| + \frac{1}{2}\ln|1+u| + C$$

Using log properties ($\ln A - \ln B = \ln \frac{A}{B}$), combine them into a single logarithm:

$$= \frac{1}{2} \ln\left| \frac{1+u}{1-u} \right| + C$$

### Step 4: Substitute back and simplify

Replace $u$ with $\sin x$:

$$= \frac{1}{2} \ln\left| \frac{1+\sin x}{1-\sin x} \right| + C$$

To get this into the standard textbook form, multiply the inside of the fraction by $\frac{1+\sin x}{1+\sin x}$:

$$= \frac{1}{2} \ln\left| \frac{(1+\sin x)^2}{1-\sin^2 x} \right| = \frac{1}{2} \ln\left| \frac{(1+\sin x)^2}{\cos^2 x} \right|$$

Pull the exponent $2$ out of the natural log to cancel the $\frac{1}{2}$:

$$= \ln\left| \frac{1+\sin x}{\cos x} \right| + C$$

$$= \ln\left| \frac{1}{\cos x} + \frac{\sin x}{\cos x} \right| + C$$

$$\mathbf{= \ln|\sec x + \tan x| + C}$$


---
# Inverse trigonometric

Let's derive $\frac{d}{dx}\sin^{-1}x$.

**Step 1: Rewrite the equation**

We start by defining our function as $y$:

$$y = \sin^{-1}x$$

To get rid of the inverse function, we apply the sine operation to both sides. This gives us an equation we already know how to handle:

$$\sin y = x$$

**Step 2: Differentiate implicitly**

Now, take the derivative of both sides with respect to $x$. Remember to use the chain rule for the left side because $y$ is a function of $x$:

$$\cos y \cdot \frac{dy}{dx} = 1$$

**Step 3: Isolate the derivative**

Divide by $\cos y$ to get $\frac{dy}{dx}$ by itself:

$$\frac{dy}{dx} = \frac{1}{\cos y}$$

We have our derivative, $\frac{1}{\cos y}$, but it is in terms of $y$. We need it in terms of $x$. This is where the right triangle comes in.

Look back at our Step 1 equation: $\sin y = \frac{x}{1}$.

Think of $y$ as an angle in a right triangle. Since sine is $\frac{\text{Opposite}}{\text{Hypotenuse}}$, we can label our triangle:

- **Opposite side:** $x$
    
- **Hypotenuse:** $1$
    

Using the Pythagorean theorem ($a^2 + b^2 = c^2$), we can find the adjacent side:

$$(\text{Adjacent})^2 + x^2 = 1^2$$

$$\text{Adjacent} = \sqrt{1 - x^2}$$

Now, look at our derivative: $\frac{dy}{dx} = \frac{1}{\cos y}$.

Cosine is $\frac{\text{Adjacent}}{\text{Hypotenuse}}$. Looking at our triangle, $\cos y = \frac{\sqrt{1 - x^2}}{1} = \sqrt{1 - x^2}$.

Substitute this back into the derivative:

$$\frac{d}{dx}\sin^{-1}x = \frac{1}{\sqrt{1 - x^2}}$$

### Applying the Logic to Tangent Inverse

You can apply this exact same logic to $\tan^{-1}x$, which is highly likely to show up on a calculus test.

1. **Rewrite:** Let $y = \tan^{-1}x \implies \tan y = x$.
    
2. **Differentiate:** $\sec^2 y \cdot \frac{dy}{dx} = 1$.
    
3. **Isolate:** $\frac{dy}{dx} = \frac{1}{\sec^2 y}$.
    
4. **Triangle Geometry:** If $\tan y = \frac{x}{1}$ (Opposite/Adjacent), then the Hypotenuse is $\sqrt{x^2 + 1^2}$.
    
5. **Translate:** Since $\sec y = \frac{\text{Hypotenuse}}{\text{Adjacent}} = \sqrt{x^2 + 1}$, then $\sec^2 y = (\sqrt{x^2 + 1})^2 = x^2 + 1$.
    
6. **Result:** $\frac{d}{dx}\tan^{-1}x = \frac{1}{x^2 + 1}$.
    

### The "Co-" Symmetry Continues

Just like the standard trigonometric derivatives, the symmetry of calculus makes the rest of the list incredibly predictable. The inverse "co-" functions are simply the **negative versions** of their counterparts:

- $\frac{d}{dx}\sin^{-1}x = \frac{1}{\sqrt{1-x^2}}$ $\rightarrow$ $\frac{d}{dx}\cos^{-1}x = \frac{-1}{\sqrt{1-x^2}}$
    
- $\frac{d}{dx}\tan^{-1}x = \frac{1}{x^2+1}$ $\rightarrow$ $\frac{d}{dx}\cot^{-1}x = \frac{-1}{x^2+1}$
    
- $\frac{d}{dx}\sec^{-1}x = \frac{1}{|x|\sqrt{x^2-1}}$ $\rightarrow$ $\frac{d}{dx}\csc^{-1}x = \frac{-1}{|x|\sqrt{x^2-1}}$





## Example 

Consider $\frac{d}{dx}(\sec ^{-1}x)= \frac{1}{x\sqrt{ x^{2}-1 }}$.

Let $y=\sec ^{-1}x$ , Thus, $\sec y=x$

$$
\begin{align}
\frac{d}{dx}\sec y&=\frac{d}{dx} x\\

\end{align}
$$

$\frac{d}{dx}\sec y$ =$\sec y\tan y\cdot \frac{dy}{dx}$ and $\frac{d}{dx}=1$. Thus,

$$
\begin{align}
\sec y\tan y\cdot \frac{dy}{dx}&=1 \\
\frac{dy}{dx}&= \frac{1}{\sec y\tan y}
\end{align}
$$

Since $y=\sec ^{-1}x$ , it follow that

$$
\frac{dy}{dx}=\frac{1}{x\tan y}
$$

For $y$ in first quadrant and third quadrant. Thus,

$$
\tan y=\pm \sqrt{ \sec ^{2}y-1 }=\pm \sqrt{ x^{2}-1 }
$$

- **Quadrant I:** $\tan y$ is **positive** ($\geq 0$).
    
- **In Quadrant III:** $\tan y$ is **also positive** ($\geq 0$).
Thus,


$$\frac{d}{dx}(\sec^{-1} x) = \frac{1}{x\sqrt{x^2-1}}$$

Remark:
why for $\frac{d}{dx}\tan ^{-1}$ and $\frac{d}{dx}\cot ^{-1}$ , the denominator is $x^{2}+1$ instead of $x^{2}-1$?

It is because $\frac{d}{dx}\tan x=\sec ^{2}x$, thus $\sec ^{2}x=\tan ^{2}x+1$. We express sec in term of tan

not $\tan$ in term of $\sec$. Besides, since we already have $\sec ^{2}x$, thus we don't need $\sqrt{  }$.

