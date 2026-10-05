Let's find the **first time** the sequence returns to 0. We want to find the smallest integer $k > 0$ such that:

$$k \cdot x \equiv 0 \pmod n$$

This means $k \cdot x$ must be a multiple of $n$. The smallest number that is a multiple of both $x$ and $n$ is the **Least Common Multiple (LCM)**.

$$k \cdot x = \text{lcm}(x, n)$$

Using the formula $\text{lcm}(x, n) = \frac{x \cdot n}{\gcd(x, n)}$, we can solve for $k$:

$$k = \frac{\text{lcm}(x, n)}{x} = \frac{n}{\gcd(x, n)}$$

**The Result:**

The cycle length is **not** $n$. The cycle length is only $\frac{n}{\gcd(x, n)}$.

- The larger the common factor, the shorter the cycle.
    
- The sequence hits 0 (the starting line) much faster.