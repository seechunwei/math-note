### 1. The Derivative of the Natural Logarithm

Your formula sheet states that $\frac{d}{dx}\ln|x|=\frac{1}{x}$. Here is the rigorous way to derive it without relying on rote memorization.

**Step 1: Rewrite as an Exponential**

Let's define our function:

$$y = \ln x$$

To work with this, we rewrite the logarithmic equation in its exponential form. Since the natural logarithm has a base of $e$, this becomes:

$$e^y = x$$

**Step 2: Differentiate Implicitly**

Now, take the derivative of both sides with respect to $x$. Remember that $y$ is a function of $x$, so we must apply the chain rule on the left side:

$$e^y \cdot \frac{dy}{dx} = 1$$

**Step 3: Isolate and Substitute**

Divide both sides by $e^y$ to solve for the derivative:

$$\frac{dy}{dx} = \frac{1}{e^y}$$

Since we established in Step 1 that $e^y = x$, we simply substitute $x$ back into the denominator:

$$\frac{d}{dx}\ln x = \frac{1}{x}$$

_(Note: The absolute value in $\ln|x|$ simply extends the domain to negative numbers, but the core derivation remains exactly the same.)_

Thus,

$$
\int \frac{1}{x} \, dx =\ln|x|+c
$$
This fills the gap in the rule for integrating power functions

### 2. The Derivative of a General Base Logarithm

What if you face $\log_a x$ instead of $\ln x$? You don't need a new proof. You just need the **Change of Base formula** from basic algebra:

$$\log_a x = \frac{\ln x}{\ln a}$$

Since $\ln a$ is just a constant, you can pull it out to the front:

$$\frac{d}{dx} \log_a x = \frac{d}{dx} \left( \frac{1}{\ln a} \cdot \ln x \right)$$

$$= \frac{1}{\ln a} \cdot \frac{d}{dx}(\ln x)$$

$$= \frac{1}{\ln a} \cdot \frac{1}{x} = \frac{1}{x \ln a}$$

### 3. The Integral of the Natural Logarithm

Your sheet lists the result as $\int \ln x \, dx=x \ln x-x+C$. Deriving this requires a clever application of **Integration by Parts**, which follows the formula: $\int u \, dv = uv - \int v \, du$.

**Step 1: Assign $u$ and $dv$**

Looking at $\int \ln x \, dx$, it might seem like we don't have two parts. The trick is to treat the invisible $1$ as our second function.

- Let $u = \ln x$ (because we know how to differentiate this).
    
- Let $dv = 1 \, dx$ (because we know how to integrate this).
    

**Step 2: Find $du$ and $v$**

- Differentiate $u$: $\frac{du}{dx} = \frac{1}{x} \implies du = \frac{1}{x} \, dx$
    
- Integrate $dv$: $v = \int 1 \, dx = x$
    

**Step 3: Apply the Formula**

Substitute our pieces into $uv - \int v \, du$:

$$\int \ln x \, dx = (x)(\ln x) - \int (x)\left(\frac{1}{x}\right) \, dx$$

**Step 4: Simplify and Solve**

The $x$ and $\frac{1}{x}$ in the integral cancel each other out beautifully, leaving just $1$:

$$= x \ln x - \int 1 \, dx$$

$$= x \ln x - x + C$$---

# Exponential function

$$
\frac{d}{dx}e^{x}=e^{x}
$$
and

$$
\frac{d}{dx}a^{x}=\ln a~a^{x}
$$


**Integrating $a^x$:**

We just proved that $\frac{d}{dx}a^x = a^x \ln a$.

If we want to integrate just $a^x$, we have to account for that extra $\ln a$ constant that pops out during differentiation. To neutralize it, we simply divide by it when integrating:

$$\int a^x \, dx = \frac{a^x}{\ln a} + C$$
 