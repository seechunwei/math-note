
Notice that $x^{3}+y^{3}+z^{3}-3xyz$ is a polynomial with 3 variable
Main idea
**Treating a multivariable expression as a polynomial in a single variable** to exploit the **Factor Theorem**.

### The Core Idea: Variable Isolation

We want to factor the expression:

$$P(x, y, z) = x^3 + y^3 + z^3 - 3xyz$$

**The Technique:** Instead of trying to juggle $x$, $y$, and $z$ simultaneously, we treat the expression as a polynomial **only in terms of $x$**. We treat $y$ and $z$ as if they are constants.

Let's rewrite $P$ specifically as a function of $x$, denoted as $f(x)$:

$$f(x) = x^3 - 3(yz)x + (y^3 + z^3)$$

Notice this is now a standard cubic polynomial in the form $Ax^3 + Bx + C$.

### Step 1: Guessing a Root (The Symmetry Trick)

To factor $f(x)$, we need to find a root $r$ such that $f(r) = 0$. If we find such a root, then by the **Factor Theorem**, $(x - r)$ is a factor of the polynomial.

Since the original expression is symmetric (swapping variables doesn't change it), we can guess that the factors might involve combinations like $(x+y)$, $(x+y+z)$, etc.

Let's test the root $x = -(y+z)$. (This corresponds to the potential factor $x + y + z$).

Substitute $x = -(y+z)$ into our function $f(x)$:

$$f(-(y+z)) = [-(y+z)]^3 - 3yz[-(y+z)] + (y^3 + z^3)$$

Expand the cubic term $[-(y+z)]^3 = -(y^3 + 3y^2z + 3yz^2 + z^3)$:

$$f(-(y+z)) = -(y^3 + 3y^2z + 3yz^2 + z^3) + 3y^2z + 3yz^2 + y^3 + z^3$$

Now, cancel the terms:

- $-y^3$ cancels with $+y^3$
    
- $-z^3$ cancels with $+z^3$
    
- $-3y^2z$ cancels with $+3y^2z$
    
- $-3yz^2$ cancels with $+3yz^2$
    

$$f(-(y+z)) = 0$$

### Step 2: Applying the Factor Theorem

Since $f(-(y+z)) = 0$, we have proven that:

$$x - (-(y+z)) = x + y + z$$

is a factor of the polynomial.

This is the power of the technique: **We found a complex multivariable factor by solving a single-variable root finding problem.**

### Step 3: Polynomial Division (The Derivation)

Now that we know $(x+y+z)$ is a factor, we can perform polynomial long division (dividing $f(x)$ by $x+y+z$) or compare coefficients to find the remaining factor.

We know:

$$x^3 + y^3 + z^3 - 3xyz = (x+y+z) \cdot Q(x,y,z)$$

Since the Left Hand Side (LHS) is degree 3 and $(x+y+z)$ is degree 1, $Q$ must be a degree 2 polynomial. The general symmetric form for a degree 2 polynomial is:

$$k_1(x^2+y^2+z^2) + k_2(xy+yz+zx)$$

By comparing the coefficient of $x^3$ (which is 1), we see that $k_1$ must be **1** (since $x \cdot x^2 = x^3$).

By comparing the coefficient of $-3xyz$, we see that $k_2$ must be **-1**.

Thus, the second factor is:

$$(x^2 + y^2 + z^2 - xy - yz - zx)$$

### The Result

Putting it together, we arrive at the identity:

$$x^3 + y^3 + z^3 - 3xyz = (x+y+z)(x^2 + y^2 + z^2 - xy - yz - zx)$$

### Why this technique matters for you

As you study discrete math and proofs, this "Variable Isolation" technique is transferable. Whenever you are asked to factor or prove inequalities for symmetric polynomials (like in AM-GM proofs or Olympiad-style algebra), try treating the expression as a function of **one** variable to verify roots. It reduces the cognitive load of the problem significantly.

---

In mathematics, an expression is **symmetric** if you can swap any two variables and the expression remains exactly the same. It treats every variable "equally."

For your specific expression $P(x, y, z) = x^3 + y^3 + z^3 - 3xyz$, here is the formal test for symmetry.

### The Swap Test

Let’s swap the positions of $x$ and $y$.

- Everywhere you see an $x$, put a $y$.
    
- Everywhere you see a $y$, put an $x$.
    
- Leave $z$ alone.
    

**Original:**

$$x^3 + y^3 + z^3 - 3xyz$$

**After Swapping $x$ and $y$:**

$$y^3 + x^3 + z^3 - 3(y)(x)z$$

**Simplifying the Swap:**

Since addition and multiplication are commutative (order doesn't matter), $y^3 + x^3$ is the same as $x^3 + y^3$, and $yx$ is the same as $xy$.

$$= x^3 + y^3 + z^3 - 3xyz$$

**Conclusion:** The result is identical to the original. You could do this with $x$ and $z$, or $y$ and $z$, and the result would always be the same. Therefore, the polynomial is symmetric.

### A Non-Symmetric Counter-Example

To see the difference, look at the expression:

$$f(x, y) = x^2 - y$$

If we swap $x$ and $y$, we get:

$$f(y, x) = y^2 - x$$

Since $x^2 - y \neq y^2 - x$, this expression is **not symmetric**. It treats $x$ differently than it treats $y$.

### Why does this matter for the proof technique?

This is crucial for the "Guessing a Root" step I showed you earlier.

Because the expression treats $x, y,$ and $z$ equally, the factors usually treat them equally too.

1. If we suspect there is a linear factor involving $x$, it likely involves $y$ and $z$ in a balanced way (like $x+y+z$).
    
2. It would be very unlikely for a symmetric expression to have a non-symmetric factor like $(x - y)$ without also having the matching factors $(y - z)$ and $(z - x)$ to "balance it out."
    

Recognizing symmetry narrows down your guesses significantly.

Would you like me to explain **Cyclic Symmetry**, which is a slightly different but related concept often found in these types of proofs?

---
This is a crucial concept in proof writing called **Structure Preservation**.

Think of a symmetric polynomial as a perfectly balanced weighing scale. Because the parent expression (the polynomial) is balanced, the children (the factors) must combine to create that same balance.

If a single factor is "lopsided" (treats variables differently), it **must** bring along "partner" factors to correct that lopsidedness.

Here is how the "balancing out" works in two specific ways:

### 1. The "If One, Then All" Rule (Group Balancing)

If you find a factor that **is not** symmetric on its own, you are automatically forced to include all its swapped versions to maintain the symmetry of the total product.

**Example:**

Imagine you have a symmetric polynomial $P(x,y,z)$.

Suppose you discover that **$x$** is a factor.

- **The Problem:** The factor $x$ is biased. It includes $x$ but ignores $y$ and $z$.
    
- **The Conflict:** If $P(x,y,z)$ is symmetric, swapping $x$ and $y$ shouldn't change anything. But if we swap $x$ and $y$ in the factor $x$, it becomes $y$. The factor has changed!
    
- **The Solution (Balancing):** For $P$ to remain symmetric, if $x$ is a factor, then **$y$** and **$z$** MUST also be factors.
    

Therefore, the factors balance out by appearing as a trio:

$$\text{Total Factor} = x \cdot y \cdot z$$

Now, if you swap $x$ and $y$, the product $xyz$ becomes $yxz$, which is identical. The group is balanced, even though the individual parts were not.

### 2. The "Self-Symmetric" Rule (Internal Balancing)

Sometimes, a single factor is already balanced internally. It doesn't need partners because it already treats everyone equally.

**Example from your identity:**

Look at the factor we found: $(x + y + z)$.

- **Test:** Swap $x$ and $y$.
    
- **Result:** $(y + x + z)$.
    
- **Conclusion:** This is identical to the original factor.
    

Because this factor is **Self-Symmetric**, it is allowed to exist alone. It doesn't need a partner like $(x+y)$ or $(y+z)$ to balance it, because it is already stable under any swap.

### Summary: How to use this in proofs

When you are trying to factor a symmetric expression $P(x, y, z)$:

1. **Check for "Group" Factors:** Does the expression become $0$ if $x=0$? If yes, then $x$ is a factor. By symmetry, $y$ and $z$ are also factors. So $xyz$ is a factor.
    
2. **Check for "Self" Factors:** Does the expression become $0$ if $x = -(y+z)$? (which is $x+y+z=0$). If yes, then the self-symmetric term $(x+y+z)$ is a factor.
    
3. **Check for "Pair" Factors:** Does the expression become $0$ if $x=y$? (i.e., factor is $x-y$). If yes, then by symmetry, $(y-z)$ and $(z-x)$ must also be factors to balance it out.
    

In the case of $x^3 + y^3 + z^3 - 3xyz$:

- It does **not** vanish if $x=y$ (so no $x-y$ group).
    
- It does **not** vanish if $x=0$ (so no $xyz$ group).
    
- It **does** vanish if $x+y+z=0$.
    

So we found the "Self-Symmetric" factor $(x+y+z)$, and the remaining "messy" factor $(x^2+y^2+z^2-xy-yz-zx)$ is also Self-Symmetric, keeping the whole equation balanced.

Would you like to try applying this "Group Balancing" logic to factor a different expression, like $(x+y+z)^3 - x^3 - y^3 - z^3$?

---
Example
Let's look at a classic example where finding just **one** "lopsided" factor immediately gives you two others for free, purely because of the balancing rule.

We will factor this expression:

$$P(x, y, z) = (x+y+z)^3 - (x^3 + y^3 + z^3)$$

### Step 1: Verify Symmetry (The Setup)

First, we check if the expression is symmetric. If we swap $x$ and $y$:

- $(x+y+z)^3$ becomes $(y+x+z)^3$ $\rightarrow$ **Same.**
    
- $-(x^3 + y^3 + z^3)$ becomes $-(y^3 + x^3 + z^3)$ $\rightarrow$ **Same.**
    

Since the expression is symmetric, any factor we find must be part of a balanced set.

### Step 2: Find "One" Lopsided Factor

Let's use the Factor Theorem technique (guessing a root). We want to make the expression zero.

Let's try setting $x = -y$ (which means $x + y = 0$).

Substitute $x = -y$ into the expression:

$$P(-y, y, z) = (-y + y + z)^3 - ((-y)^3 + y^3 + z^3)$$

Simplify the first part: $(-y+y+z)^3 = (0+z)^3 = z^3$.

Simplify the second part: $(-y)^3 + y^3 + z^3 = -y^3 + y^3 + z^3 = z^3$.

So we get:

$$z^3 - z^3 = 0$$

**The Discovery:**

Since the expression equals $0$ when $x = -y$, we know that **$(x + y)$ is a factor.**

### Step 3: The "Balancing" Act (The Magic)

Now look at our factor: **$(x + y)$**.

Is this factor symmetric? **No.**

It involves $x$ and $y$, but it ignores $z$. It is "lopsided."

Because the original expression $P(x,y,z)$ is symmetric, it cannot have a "favorite" pair of variables. If $(x+y)$ is a factor, the expression **must** also treat the other pairs exactly the same way.

- By swapping $y$ with $z$, the factor $(x+y)$ implies the existence of **$(x+z)$**.
    
- By swapping $x$ with $z$, the factor $(x+y)$ implies the existence of **$(z+y)$**.
    

**The Inference:**

Without doing any more math, we know the factorization must look like this:

$$(x+y+z)^3 - (x^3 + y^3 + z^3) = k \cdot (x+y)(y+z)(z+x)$$

_(where $k$ is just some number constant)_

### Step 4: Finding the Constant ($k$)

We have practically solved it. We just need to find $k$. We can do this by picking simple numbers for $x, y, z$ to test the equation.

Let $x=1, y=1, z=1$.

**Left Hand Side:**

$(1+1+1)^3 - (1^3 + 1^3 + 1^3)$

$= 3^3 - (1 + 1 + 1)$

$= 27 - 3 = \mathbf{24}$

**Right Hand Side:**

$k \cdot (1+1)(1+1)(1+1)$

$= k \cdot (2)(2)(2)$

$= \mathbf{8k}$

**Solve for $k$:**

$24 = 8k \implies k = 3$

### The Final Result

$$(x+y+z)^3 - x^3 - y^3 - z^3 = 3(x+y)(y+z)(z+x)$$

### Summary of the Technique

1. We did the hard work **only once** (checking $x=-y$).
    
2. We used **Symmetry** to copy-paste that logic to the other variables ($y+z$ and $z+x$).
    
3. We used simple substitution to find the constant $3$.
    

This is much faster than expanding $(x+y+z)^3$ entirely, which would result in a messy page of algebra! This "find one, get the rest free" tactic is the primary reason we check for symmetry first.

Would you like to try a practice problem where you have to determine if a factor is "lopsided" or "self-symmetric"?


---
This can be prove for AM-GM inequality for 3 terms

$$
\frac{a+b+c}{3}\geq3\sqrt{abc  }
$$
by treating $x=3\sqrt{a }$ and so on.