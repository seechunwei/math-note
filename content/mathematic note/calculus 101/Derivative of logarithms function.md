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

$$= x \ln x - x + C$$

---

# Path A: The Derivative Perspective (Euler's Proportionality & The Golden Base)

How does $e$ emerge naturally from the derivative of exponential functions?

### 1. Differentiating Any Base $b^x$ from First Principles

Let $f(x) = b^x$ for any base $b > 0$. Using the limit definition of the derivative:
$$
\begin{align}
\frac{d}{dx}[b^x] &= \lim_{h \to 0} \frac{b^{x+h} - b^x}{h} \\
&= \lim_{h \to 0} \frac{b^x \cdot b^h - b^x}{h} \\
&= \lim_{h \to 0} \frac{b^x(b^h - 1)}{h} \\
&= b^x \cdot \lim_{h \to 0} \frac{b^h - 1}{h}
\end{align}
$$

Notice that the limit factor does not depend on $x$ at all! It is a **pure constant** representing the slope of the curve at $x = 0$:
$$
m(b) = \lim_{h \to 0} \frac{b^h - 1}{h} = f'(0)
$$

> [!important] The Proportionality Principle
> The rate of change of **any** exponential function is strictly **proportional to its current value**:
> $$
> \frac{d}{dx}[b^x] = m(b) \cdot b^x
> $$
> The only difference between different bases is the proportionality constant $m(b)$.

---

### 2. Testing Bases: The Case of $2^x$ and $3^x$

Let us compute this proportionality constant for two everyday bases:

1. **For base $b = 2$**:
   $$
   m(2) = \lim_{h \to 0} \frac{2^h - 1}{h} \approx 0.6931... < 1
   $$
   Therefore:
   $$
   \frac{d}{dx}[2^x] \approx (0.6931...) \cdot 2^x
   $$
   The slope at the $y$-intercept is less than $1$ (the curve is **too flat**).

2. **For base $b = 3$**:
   $$
   m(3) = \lim_{h \to 0} \frac{3^h - 1}{h} \approx 1.0986... > 1
   $$
   Therefore:
   $$
   \frac{d}{dx}[3^x] \approx (1.0986...) \cdot 3^x
   $$
   The slope at the $y$-intercept is greater than $1$ (the curve is **too steep**).

---

### 3. Euler's Question: The Search for the Golden Base

Since $b = 2$ gives a slope less than $1$, and $b = 3$ gives a slope greater than $1$, Euler asked:

> [!question]
> **Is there a magical base between $2$ and $3$ whose proportionality constant is EXACTLY $1$?**
> $$
> m(b) = \lim_{h \to 0} \frac{b^h - 1}{h} = 1
> $$

Because the steepness $m(b)$ varies continuously with the base $b$, by the **Intermediate Value Theorem (IVT)**, there must exist a unique real number between $2$ and $3$ where:
$$
m(e) = 1
$$

For this specific base, which we name **$e$**:
$$
\frac{d}{dx}[e^x] = 1 \cdot e^x = e^x
$$
Its derivative is **identically equal to itself**!

---

#### How Did Euler Actually Calculate the Value $e \approx 2.71828...$?

How do we solve for the number $e$ from the condition that its slope is $1$?

**Step 1: From Infinitesimal Step to the Base**
The condition $m(e) = 1$ means:
$$
\lim_{h \to 0} \frac{e^h - 1}{h} = 1
$$
For an infinitesimally small step $h$:
$$
e^h - 1 \approx h \implies e^h \approx 1 + h
$$
Raise both sides to the power $\frac{1}{h}$ to isolate $e$:
$$
e \approx (1 + h)^{1/h}
$$
Letting $n = \frac{1}{h}$, as $h \to 0$, $n \to \infty$. This recovers Bernoulli's compound interest limit:
$$
e = \lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n
$$

**Step 2: Why the Limit is Too Slow (The Need for the Series)**
Calculating $\left(1 + \frac{1}{n}\right)^n$ directly converges agonizingly slowly:
- For $n = 1{,}000$: $(1 + 0.001)^{1000} \approx 2.7169$ (only 2 decimal places correct).
- For $n = 1{,}000{,}000$: $(1 + 10^{-6})^{10^6} \approx 2.718280$ (needs a million operations).

**Step 3: Binomial Expansion into the Ultra-Fast Factorial Series**
In 1748, Euler expanded $\left(1 + \frac{1}{n}\right)^n$ using the **Binomial Theorem**:
$$
\begin{align}
\left(1 + \frac{1}{n}\right)^n &= 1 + n\left(\frac{1}{n}\right) + \frac{n(n-1)}{2!}\left(\frac{1}{n}\right)^2 + \frac{n(n-1)(n-2)}{3!}\left(\frac{1}{n}\right)^3 + \dots \\
&= 1 + 1 + \frac{1}{2!}\left(1 - \frac{1}{n}\right) + \frac{1}{3!}\left(1 - \frac{1}{n}\right)\left(1 - \frac{2}{n}\right) + \dots
\end{align}
$$
Now take the limit as $n \to \infty$. Every term of the form $\left(1 - \frac{k}{n}\right) \to 1$, collapsing the entire expression into the famous **infinite series**:
$$
e = \sum_{k=0}^{\infty} \frac{1}{k!} = 1 + \frac{1}{1!} + \frac{1}{2!} + \frac{1}{3!} + \frac{1}{4!} + \dots
$$

**Step 4: Computing the Digits**
Because factorials grow exponentially fast ($4! = 24$, $7! = 5{,}040$, $10! = 3{,}628{,}800$), each additional term rapidly increases decimal precision:
$$
\begin{aligned}
1 &= 1.000000 \\
1/1! &= 1.000000 \\
1/2! &= 0.500000 \\
1/3! &= 0.166667 \\
1/4! &= 0.041667 \\
1/5! &= 0.008333 \\
1/6! &= 0.001389 \\
\hline
\text{Sum} &\approx \mathbf{2.718056} \quad (\text{accurate to 3 decimal places with just 7 terms!})
\end{aligned}
$$
Using this series, Euler computed $e$ by hand to **23 decimal places**:
$$
e = 2.71828182845904523536028...
$$

---

#### The Universal Nature of $e$: Why Does $e$ Govern Every Proportional Process in Physics?

Why is $e$ called the **natural** base? Why does it appear in radioactive decay, population growth, capacitor charging, and temperature cooling, even when humans initially measure things with arbitrary bases like $2$ or $10$?

##### 1. The Proportional Rate Law in Nature
In physics, chemistry, and biology, many systems obey the law that their **rate of change is directly proportional to their current amount**:
$$
\frac{dy}{dt} = k \cdot y
$$
- If $k > 0$: Growth accelerates as the quantity grows (e.g., bacteria population, compound interest).
- If $k < 0$: Decay slows down as the remaining quantity shrinks (e.g., radioactive decay).

Because the derivative of $e^{kt}$ with respect to $t$ brings down the constant $k$ by the Chain Rule:
$$
\frac{d}{dt}\left[ e^{kt} \right] = k \cdot e^{kt}
$$
the **only mathematical function** that satisfies this natural rate law is:
$$
y(t) = y_0 \cdot e^{kt} \quad (\text{where } y_0 = y(0) \text{ is the initial value})
$$

##### 2. Real-World Example: Newton's Law of Cooling
Suppose a hot cup of coffee with temperature $T(t)$ is placed in a room with a constant ambient surrounding temperature $T_s$.

Sir Isaac Newton observed that the rate at which the coffee cools is proportional to the **temperature difference** between the coffee and the room:
$$
\frac{dT}{dt} = -k (T - T_s) \quad (\text{where } k > 0)
$$
Let the temperature difference be $y(t) = T(t) - T_s$. Then $\frac{dy}{dt} = \frac{dT}{dt}$, which transforms Newton's law into the pure proportional decay equation:
$$
\frac{dy}{dt} = -k y \implies y(t) = y_0 \cdot e^{-kt}
$$
Since $y_0 = y(0) = T_0 - T_s$ (the initial temperature gap), substituting back yields **Newton's Law of Cooling formula**:
$$
T(t) = T_s + (T_0 - T_s) e^{-kt}
$$
As time passes ($t \to \infty$), $e^{-kt} \to 0$, and the coffee smoothly settles at room temperature $T_s$. Base $e$ appears not by human choice, but because the rate of cooling naturally depends on the current temperature gap.

##### 3. How to Relate Any Arbitrary Exponential Function to Base $e$
What if someone models growth using an arbitrary base $b$, like a cell population that doubles every hour ($y = y_0 \cdot 2^t$)?

Because the natural exponential $e^x$ and the natural logarithm $\ln x$ are inverse functions, any positive base $b$ can be rewritten as:
$$
b = e^{\ln b}
$$
Substitute this identity into the power $b^t$:
$$
b^t = \left(e^{\ln b}\right)^t = e^{(\ln b) \cdot t}
$$
Notice that this matches the universal physical form $e^{kt}$, where the continuous rate constant is simply:
$$
k = \ln b
$$
- If $b = 2$ (doubling): $2^t = e^{(\ln 2)t} \approx e^{0.6931 t}$.
- If $b = 10$: $10^t = e^{(\ln 10)t} \approx e^{2.3026 t}$.

Every exponential function in the universe, regardless of base, is secretly the natural exponential $e^{kt}$ in disguise, scaled by the factor $k = \ln b$. This directly unlocks the general differentiation and integration formulas below.

---

### 4. Generalizing to Any Base $a^x$ and Integrating

Once we have base $e$, any general base $a > 0$ can be rewritten as:
$$
a^x = \left(e^{\ln a}\right)^x = e^{x \ln a}
$$

By the Chain Rule:
$$
\frac{d}{dx}[a^x] = \frac{d}{dx}\left[e^{x \ln a}\right] = e^{x \ln a} \cdot \ln a = a^x \ln a
$$

This reveals that Euler's constant of proportionality $m(a)$ is none other than the natural logarithm: $m(a) = \ln a$!

**Integrating $a^x$:**
Since differentiation multiplies by the constant $\ln a$, integration divides by it:
$$
\int a^x \, dx = \frac{a^x}{\ln a} + C
$$

---

# Path B: The Rigorous Integral-First Construction (Analysis Approach)

In standard calculus, we often introduce $e^x$ first and define $\ln x$ as its inverse. However, in modern analysis (e.g., Spivak's *Calculus*), we construct the natural logarithm and the number $e$ from pure integration.

---

### 1. The Teleological Motivation: The Black Hole in the Power Rule

Recall the power rule for integration:
$$
\int x^n \, dx = \frac{x^{n+1}}{n+1} + C \quad (\text{for all } n \neq -1)
$$

When $n = -1$, the formula breaks down completely:
$$
\int x^{-1} \, dx = \frac{x^0}{0} \quad (\text{undefined!})
$$

Every single power of $x$ has an algebraic antiderivative **except** $x^{-1} = \frac{1}{x}$. Yet the curve $y = \frac{1}{x}$ is continuous for $x > 0$, so by the Fundamental Theorem of Calculus, its area function must exist.

---

### 2. Defining the Accumulation Function $G(x)$

To fill this missing gap, we define a brand-new function $G(x)$ representing the accumulated area under $y = \frac{1}{t}$:

> [!definition] The Natural Logarithm via Accumulation
> For any $x > 0$, we define:
> $$
> G(x) = \int_{1}^{x} \frac{1}{t} \, dt
> $$

#### Why start from $1$ and not $0$?
1. **Vertical Asymptote at $0$**: As $t \to 0^+$, $\frac{1}{t} \to \infty$. The integral $\int_{0}^{x} \frac{1}{t} \, dt$ diverges to infinity.
2. **The Multiplicative Identity**: When an interval $[a, ab]$ is scaled by factor $\frac{1}{a}$ (substitution $t = a u$), the lower endpoint rescales to:
   $$
   u = \frac{a}{a} = 1
   $$
   Starting at $1$ guarantees that $G(1) = \int_{1}^{1} \frac{1}{t} \, dt = 0$, ensuring no unwanted constants appear when multiplying inputs.

---

### 3. Derivative of $G(x)$

By Part 1 of the **Fundamental Theorem of Calculus**:
$$
G'(x) = \frac{d}{dx} \left[ \int_{1}^{x} \frac{1}{t} \, dt \right] = \frac{1}{x}
$$

---

### 4. Proving the Logarithm Property: $G(ax) = G(x) + G(a)$

We now prove that this purely geometric area function naturally converts multiplication into addition.

Let $a > 0$ be a fixed constant, and consider the composite function $f(x) = G(ax)$.

By the **Chain Rule**:
$$
\frac{d}{dx}[G(ax)] = G'(ax) \cdot \frac{d}{dx}(ax) = \frac{1}{ax} \cdot a = \frac{1}{x}
$$

Notice that both $G(ax)$ and $G(x)$ share the **exact same derivative**:
$$
\frac{d}{dx}[G(ax)] = \frac{d}{dx}[G(x)] = \frac{1}{x}
$$

By the **Mean Value Theorem Corollary** (if two functions have identical derivatives everywhere on an interval, their difference must be a constant $C$):
$$
G(ax) - G(x) = C \implies G(ax) = G(x) + C
$$

To determine the value of $C$, evaluate both sides at $x = 1$:
$$
\begin{align}
G(a \cdot 1) &= G(1) + C \\
G(a) &= 0 + C \quad (\text{since } G(1) = 0) \\
C &= G(a)
\end{align}
$$

Substituting $C = G(a)$ back into the equation:
$$
G(ax) = G(x) + G(a)
$$

> [!theorem] Logarithmic Identity
> Because $G(x)$ satisfies the fundamental characteristic law of logarithms ($G(ab) = G(a) + G(b)$), we formally name $G(x)$ the **natural logarithm**, denoted $\ln x$:
> $$
> \ln x \equiv \int_{1}^{x} \frac{1}{t} \, dt
> $$

---

### 5. Why is the Base of this Logarithm Exactly $e$? (Connecting Path A & Path B)

We proved that $G(x) = \int_{1}^{x} \frac{1}{t} \, dt$ satisfies the logarithm rule $G(ab) = G(a) + G(b)$. Therefore, $G(x)$ must be a logarithm with *some* base $b$:
$$
G(x) = \log_b(x)
$$

**How do we prove that this base $b$ is Euler's number $e$?**

#### Step 1: Differentiate the Inverse Function
Since $G(x)$ is strictly increasing, it has an inverse function $E(x) = G^{-1}(x)$. 

Using the derivative rule for inverse functions $[f^{-1}]'(x) = \frac{1}{f'(f^{-1}(x))}$:
$$
E'(x) = \frac{1}{G'(E(x))}
$$
Since $G'(u) = \frac{1}{u}$, we have $G'(E(x)) = \frac{1}{E(x)}$:
$$
E'(x) = \frac{1}{\frac{1}{E(x)}} = E(x)
$$
Look at that result: **$E'(x) = E(x)$**. The derivative of the inverse function is **identically equal to itself**!

#### Step 2: Bridge with Path A (Euler's Proportionality)
From **Path A**, we already proved from first principles that for any general exponential base $b^x$:
$$
\frac{d}{dx}[b^x] = m(b) \cdot b^x, \quad \text{where } m(b) = \lim_{h \to 0} \frac{b^h - 1}{h}
$$
The **only** base whose proportionality constant is exactly $1$ ($m(b) = 1$) is Euler's base $e$:
$$
\frac{d}{dx}[b^x] = b^x \iff b = e
$$
Since $E'(x) = E(x)$ with initial condition $E(0) = 1$ (because $G(1) = 0$), the inverse function **must be $e^x$**:
$$
E(x) = e^x
$$

#### Step 3: Conclusion on the Base
Because the inverse function of $G(x)$ is $e^x$, the function $G(x)$ itself must be the inverse of $e^x$, which is the logarithm with base $e$:
$$
G(x) = \log_e(x) \equiv \ln x
$$

The base of any logarithm is the input that produces an output of $1$ ($\log_b(b) = 1$). Therefore, $e$ is the unique upper limit where the area under the hyperbola equals **exactly $1$**:
$$
G(e) = \int_{1}^{e} \frac{1}{t} \, dt = 1 \iff \ln(e) = 1
$$
Numerically, $e \approx 2.718281828...$

---

### 6. Summary: The Complete Cycle

$$\begin{array}{ccc}
\text{The Hyperbola Area } G(x) = \int_1^x \frac{1}{t} dt & \overset{\text{invert}}{\longrightarrow} & \text{The Inverse Function } E(x) \\
\big\downarrow \text{FTC} & & \big\downarrow \text{Inverse Derivative} \\
G'(x) = \frac{1}{x} & \overset{\text{reciprocal}}{\longrightarrow} & E'(x) = E(x) \implies E(x) = e^x \\
\end{array}$$

Thus:
$$
G(x) \equiv \ln x \quad \text{and} \quad G^{-1}(x) \equiv e^x
$$
Both paths—the geometric area under $\frac{1}{t}$ and the rate-of-change of $e^x$—are two sides of the exact same mathematical coin.

---

> [!info] Historical Context & Alternative Perspectives
> - **John Napier (1614)**: Created the first logarithm tables for computation, implicitly using a base near $1/e \approx (1 - 10^{-7})^{10^7}$.
> - **Grégoire de Saint-Vincent (1647)**: Discovered scale-invariance under the hyperbola: intervals in geometric progression have identical area under $y = 1/x$.
> - **Jacob Bernoulli (1683)**: Formulated $e$ through continuous compound interest:
>   $$
>   e = \lim_{n \to \infty} \left( 1 + \frac{1}{n} \right)^n
>   $$
>   He proved $2 < \lim_{n \to \infty} \left( 1 + \frac{1}{n} \right)^n < 3$ using the Binomial Theorem.
> - **Leonhard Euler (1728–1748)**: Unified Bernoulli's limit, the hyperbola area, the derivative problem ($\frac{d}{dx}b^x = b^x$), and defined the letter $e$.
> - Reference: [History of e - bilibili](https://www.bilibili.com/video/BV1xyCvBHEpy/)

