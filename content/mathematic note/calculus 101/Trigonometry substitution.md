![[Pasted image 20260709113002.png]]

The table in **image_65b6a2.png** outlines the rules for **Trigonometric Substitution** (often called "Trig Sub").

The big idea behind this technique is a clever math hack: **integrals with square roots are hard, but trigonometric identities can turn two terms under a radical into a single perfect square, effectively destroying the square root.**

Here is how you read the table and use it in real life.

---

## The 3 Core Patterns

Look at the first column of the table in **image_65b6a2.png**. Your entire goal is to match the algebraic pattern inside your integral to one of these three formats (where $a$ is a constant number and $x$ is your variable):

1. **$\sqrt{a^2 - x^2} \implies$ Think: $1 - \sin^2\theta = \cos^2\theta$**
* *When to use:* Number minus Variable.
* *Substitution:* $x = a\sin\theta$


2. **$\sqrt{a^2 + x^2} \implies$ Think: $1 + \tan^2\theta = \sec^2\theta$**
* *When to use:* Number plus Variable (or vice versa).
* *Substitution:* $x = a\tan\theta$


3. **$\sqrt{x^2 - a^2} \implies$ Think: $\sec^2\theta - 1 = \tan^2\theta$**
* *When to use:* Variable minus Number.
* *Substitution:* $x = a\sec\theta$



---

## Step-by-Step Example

Let's solve a problem using the first row from **image_65b6a2.png**:


$$\int \frac{1}{x^2\sqrt{4 - x^2}} \, dx$$

### Step 1: Match the pattern and pick your substitution

The square root is $\sqrt{4 - x^2}$. This matches the pattern $\sqrt{a^2 - x^2}$, where $a^2 = 4$, so **$a = 2$**.
According to the table, our substitution is:


$$x = 2\sin\theta$$

### Step 2: Find the derivative ($dx$)

Don't forget to differentiate your substitution! You must replace $dx$ too:


$$dx = 2\cos\theta \, d\theta$$

### Step 3: Substitute everything into the integral

Let's swap out every $x$ and the $dx$ in our original integral:


$$\int \frac{{2\cos\theta \, d\theta}}{\underbrace{(2\sin\theta)^2}_{x^2} \underbrace{\sqrt{4 - (2\sin\theta)^2}}_{\sqrt{4-x^2}}}$$

Now, use the identity listed in **image_65b6a2.png** to simplify the radical:


$$\sqrt{4 - 4\sin^2\theta} = \sqrt{4(1 - \sin^2\theta)} = \sqrt{4\cos^2\theta} = 2\cos\theta$$

Plug this back in and watch the cancellation magic happen:


$$\int \frac{2\cos\theta}{4\sin^2\theta \cdot 2\cos\theta} \, d\theta$$

The $2\cos\theta$ terms on the top and bottom cancel out completely:


$$\int \frac{1}{4\sin^2\theta} \, d\theta = \frac{1}{4} \int \csc^2\theta \, d\theta$$

### Step 4: Integrate

The antiderivative of $\csc^2\theta$ is $-\cot\theta$:


$$= -\frac{1}{4}\cot\theta + C$$

### Step 5: Convert back to $x$ using a Right Triangle

Our answer is currently in terms of $\theta$, but the original question was in terms of $x$. We need to switch back.

Go back to your original substitution step: $x = 2\sin\theta \implies \sin\theta = \frac{x}{2}$.
Remembering SOH-CAH-TOA, draw a right triangle where:

* **Opposite side** $= x$
* **Hypotenuse** $= 2$
* **Adjacent side** (by Pythagorean theorem) $= \sqrt{4 - x^2}$

Since cotangent ($\cot\theta$) is $\frac{\text{Adjacent}}{\text{Opposite}}$, we read the values straight off our triangle:


$$\text{cot}\theta = \frac{\sqrt{4 - x^2}}{x}$$

Substitute this back into our integrated answer for the final result:


$$\mathbf{= -\frac{\sqrt{4 - x^2}}{4x} + C}$$

Remark
We can also use $x=a\cos \theta$ for the substitution

### So why do textbooks universally default to $x = a \sin\theta$?

It comes down to human psychology and a sneaky negative sign.

#### 1. The Derivative Trap

Look at what happens when you take the derivative to find your $dx$:

- If you use $x = a \sin\theta \implies \mathbf{dx = a \cos\theta \, d\theta}$ (Nice and positive!)
    
- If you use $x = a \cos\theta \implies \mathbf{dx = -a \sin\theta \, d\theta}$ (Watch out for the negative!)
    

Carrying a negative sign all the way through a massive, multi-step integration problem drastically increases the chance that a student will accidentally drop it or make a arithmetic error. Instructors and textbooks prefer the positive derivative of sine because it is simply safer.

What if the $a$ is not a square number?

If the constant under your square root is some number $C$, you just set $a^2 = C$, which means:

$$a = \sqrt{C}$$

|**Expression**|**If the number is 5...**|**Your a value**|**Your Substitution**|
|---|---|---|---|
|$\sqrt{a^2 - x^2}$|$\sqrt{5 - x^2}$|$a = \sqrt{5}$|$x = \sqrt{5}\sin\theta$|
|$\sqrt{a^2 + x^2}$|$\sqrt{5 + x^2}$|$a = \sqrt{5}$|$x = \sqrt{5}\tan\theta$|
|$\sqrt{x^2 - a^2}$|$\sqrt{x^2 - 5}$|$a = \sqrt{5}$|$x = \sqrt{5}\sec\theta$|

---

The best way to understand this formula is to see it as a direct application of the **trigonometric substitution** we just discussed!

Because the denominator contains the pattern $x^2 + a^2$, it matches the second row of your table ($a^2 + x^2$). Let's walk through the derivation using that exact toolkit, and then look at the shortcut intuition for why the constants land where they do.

### 1. The Proof Using Trig Substitution

^15c37a

Let's solve $\int \frac{1}{x^2 + a^2} \, dx$ using the substitution from the table:

- **Step 1: Choose the substitution**
    
    $$x = a\tan\theta$$
    
- **Step 2: Find the derivative ($dx$)**
    
    $$dx = a\sec^2\theta \, d\theta$$
    
- **Step 3: Substitute into the integral**
    
    Replace $x$ and $dx$ with our trigonometric terms:
    
    $$\int \frac{a\sec^2\theta \, d\theta}{(a\tan\theta)^2 + a^2}$$
    
- **Step 4: Simplify the denominator**
    
    Factor out the $a^2$ and apply the Pythagorean identity ($1 + \tan^2\theta = \sec^2\theta$):
    
    $$(a\tan\theta)^2 + a^2 = a^2\tan^2\theta + a^2 = a^2(\tan^2\theta + 1) = a^2\sec^2\theta$$
    
    Now, plug this back into the integral:
    
    $$\int \frac{a\sec^2\theta}{a^2\sec^2\theta} \, d\theta$$
    
- **Step 5: Cancel terms and integrate**
    
    The $\sec^2\theta$ terms cancel out completely, and $\frac{a}{a^2}$ reduces to $\frac{1}{a}$:
    
    $$\int \frac{1}{a} \, d\theta = \frac{1}{a}\theta + C$$
    
- **Step 6: Convert $\theta$ back to $x$**
    
    Go back to your original substitution and solve for $\theta$:
    
    $$x = a\tan\theta \implies \tan\theta = \frac{x}{a} \implies \theta = \tan^{-1}\left(\frac{x}{a}\right)$$
    
    Substitute this back into your integrated result:
    
    $$\mathbf{\frac{1}{a}\tan^{-1}\left(\frac{x}{a}\right) + C}$$
    

### 2. The Direct Intuition: Working Backward

Another way to understand why this formula works is to look at it from the perspective of derivatives and the **Chain Rule**.

You already know the fundamental derivative rule for the basic inverse tangent function:

$$\frac{d}{dx}\left[\tan^{-1}(x)\right] = \frac{1}{1 + x^2}$$

What happens if we scale the angle and take the derivative of $\tan^{-1}\left(\frac{x}{a}\right)$? Let's use the chain rule:

$$\frac{d}{dx}\left[\tan^{-1}\left(\frac{x}{a}\right)\right] = \frac{1}{1 + \left(\frac{x}{a}\right)^2} \cdot \frac{1}{a}$$

Let's clean up that fraction by multiplying the top and bottom by $a^2$:

$$= \frac{1}{1 + \frac{x^2}{a^2}} \cdot \frac{1}{a} = \frac{a^2}{a^2 + x^2} \cdot \frac{1}{a} = \frac{\mathbf{a}}{x^2 + a^2}$$

Notice what happened: taking the derivative of $\tan^{-1}\left(\frac{x}{a}\right)$ gives us the exact denominator we want, but it leaves an **extra $a$** sitting on top.

To counteract and get rid of that extra $a$ on top, we have to multiply the front of our integration formula by $\mathbf{\frac{1}{a}}$. That is exactly why the $\frac{1}{a}$ sits on the outside of the final formula!

Does seeing it derived from the substitution help tie the table patterns together for you?