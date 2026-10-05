A function $f$ have inverse iff $f$ is onto and one-to-one.

> [!NOTE] Definition
> A function $f$ is one-to-one if $f(x_{1})=f(x_{2})\implies x_{1}=x_{2}$ 
> 

The definition of inverse function.

> [!NOTE] Theorem
> If $f$ is a one-to-one continuous function defined on an interval, then its inverse function $f^{-1}$ is also continuous.

> [!NOTE] Theorem
> If $f$ is a one-to-one differentiable function with inverse function $f^{-1}$ and $f'(f^{-1}(a))\neq 0$, then the inverse function is differentiable at $a$ and
> $$
> (f^{-1})'(a)= \frac{1}{f'(f^{-1}(a))}
> $$


Why？
![[Pasted image 20260625141059.png]]

if $f(b)=a$ then $f^{-1}(a)=b$, 

$$
(f^{-1})'(a)= \frac{\triangle y}{\triangle x}= \frac{1}{\triangle x/ \triangle y}= \frac{1}{f'(b)}
$$

---

# Exponential Functions and Their Derivatives

Exponential function is function where its exponent is a variable $f(x)=2^{x}$.

In general
$$
f(x)=b^{x}
$$

where $b\geq 0$, why? because $(-1)^{1/2}$ is not defined.

When $x=n$, a positive integer, then

$$
b^{n}=b\cdot b\dots b \text{ (n factors)}
$$

If $x=0$, then $b^{0}=1$. If $x=-n$, then

$$
b^{-n}= \frac{1}{b^{n}}
$$

If $x$ is a rational number, $x= \frac{p}{q}$, where $p$ and $q$ are integers and $q> 0$, then

$$
b^{x}=b^{p/q}= \sqrt[q]{b^{p}  }=(\sqrt[q]{b  })^{p}
$$
But what is the meaning of $b^{x}$ if $x$ is an irrational number?

In particular, since the irrational number $\sqrt{ 3 }$ satisfy

$$
1.7<\sqrt{ 3 }<1.8
$$
we must have
$$
2.17<2^{\sqrt{ 3 }}<2^{1.8}
$$

Similarly, if we use better approximations for $\sqrt{ 3 }$ , we obtain better approximations for $2^{\sqrt{ 3 }}$.

It can be shown that there is exactly one number that is greater than all of the numbers 
$$
2^{1.7},2^{1.73},2^{1.732},\dots
$$
 and less than all of the numbers

$$
2^{1.8},2^{1.74},2^{1.733},\dots
$$

We define $2^{\sqrt{ 3 }}$ to be this number. In general if $b$ is any positive number, we define

> [!NOTE] Definition
> $$
> b^{x}=\lim_{ r \to x }b^{x}~~~\text{r rational} 
> $$

![[Pasted image 20260625150043.png]]

### The Properties of Exponential Function

> [!NOTE] Theorem (Law of Exponents)
> If $b>0$ and $b\neq 1$, then $f(x)=b^{x}$ is a continuous function with domain $\mathbb{R}$ and range $(0,\infty)$. In particular, $b^{x}>0$ for all $x$.
> 
> if $a,b>0$ and $x,y \in\mathbb{R}$, then
> 1. $b^{x+y}=b^{x}b^{y}$
> 2. $b^{x-y}= \frac{b^{x}}{b^{y}}$
> 3. $(b^{x})^{y}=b^{xy}$
> 4. $(ab)^{x}=a^{x}b^{x}$

If x and y are rational numbers, then these laws are well known from elementary algebra. 

For arbitrary real numbers x and y these laws can be deduced from the special case where the exponents are rational by using the definition (limit).

The following limits can be proved from the definition of a limit at infinity.

![[Pasted image 20260625151003.png]]

---

## Derivatives of Exponential Functions

Let's try to compute the derivative of the exponential function $f(x)=b^{x}$ using the definition of a derivative.

$$
\begin{align}
f'(x)&= \lim_{ h \to 0 } \frac{f(x+h)-f(x)}{h} \\
&=\lim_{ h \to 0 } \frac{b^{x+h}-b^{x}}{h} \\
&= \lim_{ h \to 0 } \frac{b^{x}b^{h}-b^{x}}{h} \\
&= \lim_{ h \to 0 } \frac{b^{x}(b^{h}-1)}{h} \\
\end{align}
$$

The factor $b^{x}$ doesn't depend on $h$, so 

$$
f'(x)= b^{x}\lim_{ h \to 0 } \frac{b^{h}-1}{h}
$$
Notice that

$$
\lim_{ h \to 0 } \frac{b^{h}-1}{h}=\lim_{ h \to 0 }  \frac{f(x+h)-f(x)}{h}
$$

when $f(x)=b^{0}$. Thus,

$$
\lim_{ h \to 0 } \frac{b^{h}-1}{h}= f'(0)
$$
Therefore we have shown that if the exponential function $f(x)=b^{x}$ is differentiable at 0, then it is differentiable everywhere and

$$
f'(x)=f'(0)b^{x}
$$
This equation says that the rate of change of any exponential function is proportional to the function itself.

for $b=2$
$$
f'(0)= \lim_{ h \to 0 } \frac{2^{h}-1}{h}\approx 0.69
$$
and for $b=3$,

$$
f'(0)=\lim_{ h \to 0 } \frac{3^{h}-1}{h}\approx 1.10
$$

This is approximation. In fact it can prove these limits exist.

Thus, 

$$
\frac{d}{dx}(2^{x})\approx(0.69)2^{x}
$$
and
$$
\frac{d}{dx}(3^{x})\approx (1.10)3^{x}
$$



---
## How Do We Know the Limit Actually Exists?

Numerically plugging in smaller and smaller values of $h$ gives us a strong hint, but it isn't a rigorous proof of existence. To prove the limit must exist, we look at the structural properties of the function $f(x) = b^x$.

- **Convexity:** The function $f(x) = b^x$ is strictly convex (it always curves upward).
    
- **Monotonicity:** Because of this upward curvature, the difference quotient $\frac{b^h - 1}{h}$ (which represents the slope of the secant line passing through $(0,1)$ and $(h, b^h)$) decreases monotonically as $h$ approaches $0$ from the right ($h \to 0^+$).
    
- **Boundedness:** As $h \to 0^+$, these slopes are bounded below by any secant slope taken from the left side ($h < 0$).
    

By the **Monotone Convergence Theorem**, any functional relationship that is monotonic and bounded as it approaches a point _must_ converge to a unique real number limit. This guarantees the limit exists, even before we give it a name.

---
In view of the estimates of $f'(0)$ for $b=2$ and $b=3$, it seems reasonable that there is a number b between 2 and 3 for which $f'(0)=1$. It is traditional to denote this value by the letter e.

Let’s define a function $L(b)$ that spits out the value of this limit for any base $b$:

$$L(b) = \lim_{h \to 0} \frac{b^h - 1}{h}$$

By looking at how this function behaves when we change the base, the number $e$ and the natural logarithm emerge completely naturally.

Notice that the limit on the right is exactly our definition of $L(b)$. This gives us a beautiful structural property:

$$f'(x) = b^x \cdot L(b)$$

The derivative of an exponential function is always **proportional to the function itself**, and the constant of proportionality is $L(b)$ (the slope at $x=0$).

### Step 2: Discovering the Logarithmic Property

Now, let's see what happens to this multiplier $L(b)$ if we change the base. Suppose we relate a base $b$ to another base $a$ by some scaling factor $k$, such that $b = a^k$.

If we evaluate the derivative of $f(x) = b^x = (a^k)^x = a^{kx}$ at $x=0$, we can do it in two different ways:

1. **By our definition of $L$:** The slope of $b^x$ at $x=0$ is simply $L(b)$. Substituting $b = a^k$, this is $L(a^k)$.
    
2. **By the Chain Rule:** The derivative of $a^{kx}$ with respect to $x$ is $k \cdot a^{kx} \cdot L(a)$. Evaluating this at $x=0$ gives $k \cdot L(a)$.
    

Because both methods must yield the exact same slope, we get the foundational functional equation:

$$L(a^k) = k \cdot L(a)$$
This is the defining characteristic of a **logarithm**—exponents inside the function pull out to the front as multipliers. This tells us that $L(b)$ must be a logarithm function.

### Step 3: The Invention of $e$
Since $L(b)$ behaves like a logarithm, its value changes continuously as we change the base $b$.

- For $b = 2$, the slope $L(2) \approx 0.693$
    
- For $b = 3$, the slope $L(3) \approx 1.098$
    

Because the function is continuous, intermediate value properties imply there must be some perfect, magical base between 2 and 3 where the scaling factor $L(b)$ is exactly equal to **$1$**.

> [!NOTE] Definition 
> We define this unique base as $e$. By definition:
> 
> $$L(e) = \lim_{h \to 0} \frac{e^h - 1}{h} = 1$$

Thus,

> [!NOTE]
> Derivative of the Natural Exponential Function
> $$
> \frac{d}{dx}(e^{x})=e^{x}
> $$

If we combine with Chain Rule, then

$$
\frac{d}{dx}(e^{u})=e^{u} \frac{du}{dz}
$$

### Step 4: The Grand Finale

Now that we have defined $e$ such that $L(e) = 1$, we can find the exact value of $L(b)$ for _any_ arbitrary base $b$.

We can rewrite any positive number $b$ as a power of $e$ using the natural logarithm: $b = e^{\ln(b)}$.

Now, substitute this into our limit function $L(b)$ and apply the logarithmic pulling-out property we proved in Step 2:

$$L(b) = L\left(e^{\ln(b)}\right)$$

$$\text{Since } L(a^k) = k \cdot L(a), \text{ let } a = e \text{ and } k = \ln(b):$$

$$L(b) = \ln(b) \cdot L(e)$$

Since we defined $L(e) = 1$, the expression collapses beautifully:

$$L(b) = \ln(b) \cdot 1 = \ln(b)$$

---
![[Pasted image 20260625165951.png]]

## Integration

$$
\int e^{x} \, dx=e^{x}+c
$$

$$
\begin{align}
\int x^{2}e^{x^{3}} \, dx
\end{align}
$$
Let $u=x^{3}$, then $du=3x^{2}~dx\implies \frac{du}{3}=x^{2}~ dx$. Thus,

$$
\begin{align}
\int x^{2}e^{x^{3}} \, dx&= \frac{1}{3}\int e^{u} \, du \\
&=\frac{1}{3}e^{u }+c \\
&=\frac{1}{3}e^{x^{3}}+c
\end{align}
$$
---

## Logarithmic Functions

Since the exponential function is one-to-one , thus we can defined an inverse function

$$
\log_{b}x=y \Leftrightarrow b^{y}=x
$$

The cancellation equations

$$
\begin{align}
\log _{b}(b^{x})&=x ~~\text{ for every }x \in\mathbb{R} \\
b^{\log_{b}x}&=x~~\text{for every }x>0
\end{align}
$$

TBC

---
