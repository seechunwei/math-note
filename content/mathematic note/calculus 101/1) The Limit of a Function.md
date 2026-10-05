
> [!definition] The intuitive definition of limit
> Suppose $f(x)$ is defined on some open interval that contains $a$, except possibly at $a$ itself. Then we write,
> 
> $$
> \lim_{ x \to a } f(x)=L
> $$
> and say
> "the limit of $f(x)$ as $x$ approaches $a$, equals $L$"
> 
> If we can make $f(x)$ arbitrarily close to $L$ by restricting $x$ to be sufficiently close to $a$. (the formal definition define the arbitrarily close in term of interval of $x$)

### One-Sided Limit

![[Pasted image 20260412211749.png]]

Notice that the when $x$ approaches to $0$ from left side, $y$ approaches to 0. Conversely, when $x$ approaches $0$ from right side , $y$ approaches to $1$.

We write 
$$
\lim_{ t \to 0^{+} }H(t)=1 \text{   } \lim_{ t \to a^{-} } H(t)=0
$$

> [!definition] Definition of One-Sided Limits
> $$
> \lim_{ x \to a^{-} } f(x)=L
> $$
> If we can make the $f(x)$ arbitrarily close to $L$ when $x$ sufficiently close to $a$ with $x<a$.

Thus, by combining these 2 definition we can make a statement below

> [!theorem]
> $$
> \lim_{ x \to a } f(x)=L \text{ iff } \lim_{ x \to a^{-} } f(x)=L \text{ and } \lim_{ x \to a^{+} } f(x)=L
> $$


### Infinite limits

> [!definition] Intuitive Definition of an Infinite Limit
> 
> Let $f$ be a function defined on both sides of $a$, except possibly at $a$ itself. Then
> 
> $$
> \lim_{ x \to a } f(x)=\pm\infty
> $$
> means that the values of $f(x)$ can be made arbitrarily large (as large as we please) by taking $x$ sufficiently close to $a$. (Notice that infinite limit doesn't mean limit exists)

> [!definition] Definition Vertical Asymptote
> 
> The vertical line $x=a$ is called a vertical asymptote of the curve (is impossible to be a line) $y=f(x)$ if at least one of the following is true:
> 
> $$
> \lim_{ x \to a^{-} }f(x)=\pm \infty \text{ or }\lim_{ x \to a^{+} }f(x)=\pm\infty 
> $$



