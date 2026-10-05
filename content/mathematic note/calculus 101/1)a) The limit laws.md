
> [!theorem]
> Suppose $c$ is a constant and the limits
> 
> $$
> \lim_{ x \to a }f(x) \text{ and }\lim_{ x \to a } g(x) 
> $$
> 
> exist. Then,
> 
> 1) $\lim_{ x \to a }[f(x)+g(x)]=\lim_{ x \to a }f(x)+\lim_{ x \to a }g(x)$
> 2) $\lim_{ x \to a }[f(x)-g(x)]=\lim_{ x \to a }f(x)-\lim_{ x \to a }g(x)$
> 3) $\lim_{ x \to a }[cf(x)]=c\lim_{ x \to a }f(x)$
> 
> 4) $\lim_{ x \to a }[f(x)g(x)]=\lim_{ x \to a }f(x)\cdot \lim_{ x \to a }g(x)$
> 
> 5) $\lim_{ x \to a } \frac{f(x)}{g(x)}= \frac{\lim_{ x \to a }f(x)}{\lim_{ x \to a }g(x)}$ if $\lim_{ x \to a }g(x)\neq 0$.


If we use the Product Law repeatedly with $g(x)=f(x)$, we obtain the following law.

> [!theorem] 6) Power law
> $$
> \lim_{ x \to a } [f(x)]^{n}=[\lim_{ x \to a } f(x)]^{n}
> $$
> 

Since we know that
7) $\lim_{ x \to a }c=c$
8) $\lim_{ x \to a }x=a$

Thus, if we now put $f(x)=x$ in Law 6 and use law 8, we get another useful special limit.

$$
\begin{align}
\lim_{ x \to a } x^{n}&=(\lim_{  x\to a }x )^{n} \\
&=a^{n}
\end{align}
$$
where $n$ is a positive integer.


10)
$$
\lim_{ x \to a } \sqrt[n]{ x }=\sqrt[n]{ a }
$$
where $n$ is a positive integer (If $n$ is even, we assume that $a>0$)


> [!theorem] Root law
> 
> $$
> \begin{align}
> \lim_{ x \to a } \sqrt[n]{ f(x) }=\sqrt[n]{\lim_{ x \to a } f(x)  } &&\text{where n is a positive integer}
> \end{align}
> $$
> 
> If $n$ is even, we assume that $\lim_{ x \to a }f(x)>0$.


> [!theorem]  Direct Substitution Property
> If $f$ is a polynomial or a rational function and $a$ in the domain of $f$, then
> 
> $$
> \lim_{ x \to a } f(x)=f(a)
> $$
> 

In more general

> [!theorem] Replacement Theorem
> if $f(x)=g(x)$, when $x\neq a$, then $\lim_{ x \to a }f(x)=\lim_{ x \to a }g(x)$, provided the limit exist.

(It is the exact mathematical justification behind almost every algebraic trick (like factoring, canceling, or rationalizing) used to solve limits.)

> [!theorem]
> If $f(x)\leq g(x)$ when $x$ is near $a$ and the limit of $f$ and $g$ both exist as $x$ approaches $a$, then
> 
> $$
> \lim_{ x \to a } f(x)\leq \lim_{ x \to a } g(x)
> $$

> [!theorem]
> The Squeeze Theorem
> If $f(x)\leq g(x)\leq h(x)$ when $x$ is near $a$ (except possibly at $a$) and
> 
> $$
> \lim_{ x \to a } f(x)=\lim_{ x \to a }h(x)=L 
> $$
> then
> $$
> \lim_{ x \to a } g(x)=L
> $$

The application of squeeze theorem
