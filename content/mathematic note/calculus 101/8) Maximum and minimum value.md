> [!definition] 
> Let $c$ be a number in the domain $D$ of a function $f$. Then $f(c)$ is 
> - absolute maximum value of $f$ on $D$ if $f(c)\geq f(x)$ for all $x$ in $D$.
> - absolute minimum value of $f$ on $D$ if $f(c)\leq f(x)$ for all $x$ in $D$.

> [!definition]
> The number $f(c)$ is a 
> - local maximum if $f(c)\geq f(x)$ when $x$ is near $c$.
> - local minimum if $f(c)\leq f(x)$ when $x$ is near $c$.


> [!remark]
> Notice that a function $f$ can has more than 1 local or absolute maximum/minimum which the absolute extremum value are the same. (for example cos function)
> 

> [!theorem] The Extreme value theorem
> If $f$ is continuous on a closed interval $[a,b]$, then $f$ has an absolute maximum value $f(c)$ and an absolute minimum value $f(d)$ at some numbers $c$ and $d$ in $[a,b]$.

> [!question]
> 
> Why it is a closed interval, because if it is open interval then we do not have a fixed end point, for example $(0,4)$, if $f(x)=max$ when $x\to{4}$, but we couldn't find the maximum value because we can move $x$ arbitrary close to $4$.
> 
> Besides it need to be continuous so that is no gap which will cause the situation above. (From the definition of continuous it need the limit = the value of $f(x)$)

> [!definition]
> Critical point is the value of $c$ where $f'(c)=0$ or $f'(c)$ does not exist. (it is a turning point)

> [!remark]
> critical point doesn't mean it is local maximum or local minimum, it can be point of inflection.

> [!theorem] Fermat theorem
> if $f(c)$ is a local maximum or local minimum (turning point) and $f'(c)$ (smooth turning point) exists, then $f'(c)=0$.

Proof:
WLOG. assume $f$ has a local maximum at $c$, there exists an interval $(c-\delta,c+\delta)$ such that for all $x$ in this interval

$$
f(c)\geq f(x)
$$
Let $h\leq|\delta|$, then for all $h$, we have

$$
f(c+h)-f(c)\leq 0
$$
1) **Analyzing the Right-Hand Derivative**
Consider $h>0$. Since $f(c+h)-f(x)\leq 0$, the difference quotient is

$$
\frac{f(c+h)-f(c)}{h}\leq 0
$$
By the Limit Laws, if a function is non-positive, its limit must be $\leq 0$.
**Analyzing the Right-Hand Derivative**
$$
f'(c)=\lim_{ h \to 0^{+} } \frac{f(c+h)-f(c)}{h}\leq 0
$$
2) **Analyzing the Right-Hand Derivative** 
Consider $h< 0$. Since $f(c+h)-f(c)\leq 0$ and $h< 0$, the difference quotient is

$$
\frac{f(c+h)-f(c)}{h}\geq 0
$$
By the Limit Laws, 

$$
f'(c)=\lim_{ h \to 0^{-} } \frac{f(c+h)-f(c)}{h}\geq 0 
$$
We are given that $f'(c)$ **exists**. By definition, this means the left-hand limit and right-hand limit must be equal:

The only real number that satisfy both condition is 

$$
f'(c)=0
$$
$\blacksquare$



In terms of critical numbers, Fermat's Theorem can be rephrased as follows.

$$
\text{if f has a local maximum or minimum at c, then c is a critical number of f}
$$

Why? notice the Fermat Theorem tell one case of (critical point) which is when $f'(c)$ is exists.

Why it is not if and only if?
It can be a point of inflection (reason it is not if and only if).

![[Pasted image 20260429155832.png]]

---


