
Consider a rational function

$$
f(x)= \frac{P(x)}{Q(x)}
$$
where $P$ and $Q$ are polynomials. With the condition: the degree of $P$ is less than the degree of $Q$, it is possible to express $f$ as a sum of simpler fractions.

Why we need the condition?
Think about what the fundamental building blocks of a partial fraction decomposition actually look like. They are always of the form:

$$\frac{A}{(x-r)^k} \quad \text{or} \quad \frac{Bx+C}{(x^2+px+q)^k}$$

Now, consider what happens to these building blocks as $x$ approaches infinity. Because the degree of the denominator in every single partial fraction term is always strictly greater than the degree of its numerator, the limit of each individual term as $x \to \infty$ is exactly $0$.

Consequently, if you sum up a finite number of these terms, the limit of the entire sum must also be $0$.

$$\lim_{x \to \infty} \left( \frac{A}{x-a} + \frac{B}{x-b} + \dots \right) = 0$$

For the original rational function $\frac{P(x)}{Q(x)}$ to be equal to this sum, it must share the exact same asymptotic behavior.

$$\lim_{x \to \infty} \frac{P(x)}{Q(x)} = 0$$

This limit evaluates to $0$ if and only if $\deg(P) < \deg(Q)$. If $\deg(P) \ge \deg(Q)$, the limit as $x \to \infty$ will either be a non-zero constant or diverge to infinity.

First step:
If deg$(P)\geq$deg$(Q)$, then we must perform long division. Thus,

$$
f(x)= \frac{P(x)}{Q(x)}=S(x)+ \frac{R(x)}{Q(x)}
$$

Second step:
Factor the denominator $Q(x)$ as far as possible. It can be shown that any polynomial $Q$ can be factored as a product of linear factors (of the form $ax+b$) and irreducible quadratic factors (of the form $ax^{2}+bx+c$, where $b^{2}-4ac< 0$).

Third step:
Express the proper rational function $\frac{R(x)}{Q(x)}$ as a sum of partial fractions of the form

![[Pasted image 20260625181010.png]]

Case 1: The denominator $Q(x)$ is a product of distinct linear factors.

$$
Q(x)=(a_{1}x+b_{1})(a_{2}x+b_{2})\dots(a_{k}x+b_{k})
$$

where no factor is repeated.

In this case the partial fraction theorem states that there exist constants A1, A2, . . . , Ak such that

$$
\frac{R(x)}{Q(x)}= \frac{A_{1}}{a_{1}x+b_{1}}+\dots+\frac{A_{k}}{a_{k}+b_{k}}
$$

Case II: $Q(x)$ is a product of linear factors, some of which are repeated

$$
\frac{x^{3}-x+1}{x^{2}(x-1)^{3}}= \frac{A}{x}+\frac{B}{x^{2}}+ \frac{C}{x-1}+ \frac{D}{(x-1)^{2}}+ \frac{E}{(x-1)^{3}}
$$


Case III: $Q(x)$ contains irreducible quadratic factors, none of which is repeated.

If $Q(x)$ has the factor $ax^{2}+bx+c$, where $b^{2}-4ac<0$, thus the expression for $\frac{R(x)}{Q(x)}$ will have a term of the form

$$
\frac{Ax+B}{ax^{2}+bx+c}
$$
### Integrating the Irreducible Quadratic Terms

The second half of the image addresses what you actually _do_ with those quadratic terms once you've split them up.

When you look at a term like $\frac{Bx + C}{x^2 + 1}$, you typically split it into two separate integrals:

- $\int \frac{Bx}{x^2 + 1} \, dx$ $\rightarrow$ Handled easily using $u$-substitution ($u = x^2 + 1$).
    
- $\int \frac{C}{x^2 + 1} \, dx$ $\rightarrow$ Handled using the inverse trigonometric formula highlighted in blue box **[10]**.
    

Formula **[10]** states:

$$\int \frac{dx}{x^2 + a^2} = \frac{1}{a} \tan^{-1}\left(\frac{x}{a}\right) + C$$
(This is actually from the trigonometric substitution) 
[[Trigonometry substitution#^15c37a]]

#### How it applies to this specific problem:

- For the $\frac{\dots}{x^2 + 1}$ term, $a^2 = 1 \implies a = 1$. The integral directly yields a standard $\tan^{-1}(x)$ function.
    
- For the $\frac{\dots}{x^2 + 4}$ term, $a^2 = 4 \implies a = 2$. When integrating the constant part over this denominator, you use the formula with $a = 2$, which gives you a result scaled by $\frac{1}{2} \tan^{-1}\left(\frac{x}{2}\right)$.


If a quadratic denominator isn't perfectly clean (e.g., it looks like $x^2 + 4x + 8$), the text notes you would **complete the square** first to force it into the $(x+h)^2 + a^2$ shift-form before applying this exact arctangent rule.

![[Pasted image 20260625182821.png]]

![[Pasted image 20260625182834.png]]

Case IV: $Q(x)$ contains a repeated irreducible quadratic factor.

Each of the terms in (11) can be integrated by using a substitution or by first completing the square if necessary.