
The first part of the Fundamental Theorem deals with the functions defined by an equation of the form

$$
g(x)= \int_{a}^{x} f(t) \, dt 
$$
where $f$ is a continuous function on $[a,b]$ and $x$ varies between $a$ and $b$. Observe that $g$ depends only on $x$, which appear as the variable upper limit in the integral.

If $x$ is a fixed number, then the integral $\int_{a}^{x} f(x) \, dx$ is a definite number.

If we let $x$ vary, the number $\int_{a}^{x} f(x) \, dx$ also varies and defines a function of $x$ denoted by $g(x)$.

Think of $g$ as the 'area so far' function;

![[Pasted image 20260623142908.png]]


if we let $f(x)=x$ and $a=0$, then we have a quadratic function where domain is $[0,\infty)$ 

$$
g(x)= x^{2}
$$
If we sketch the derivative of the function $g$. Then we get back the graph $f(x)=x$. Thus, we suspect that $g'=f$.

### General
To see why this might be generally true we consider any continuous function $f$ with $f(x)\geq 0$. Then, $g(x)= \int_{a}^{x} f(x) \, dx$ can be interpreted as the area under the graph of $f$ from $a$ to $x$,

Observe that, for $h>0$, $g(x+h)-g(x)$ is the area under the graph of $f$ from $x$ to $x+h$.

![[Pasted image 20260623145359.png]]


For small $h$, we can see the area is approximately equal to the area of the rectangle with height $f(x)$ and width $h$:

$$
g(x+h)-g(x) \approx hf(x)
$$
so

Intuitively, we therefore expect that

$$
\frac{g(x+h)-g(x)}{h} \approx f(x)
$$
Thus, 

$$
g'(x)= \lim_{ h \to 0 }  \frac{g(x+h)-g(x)}{h}=f(x)
$$


> [!NOTE] The Fundamental Theorem of Calculus, Part 1
> If $f$ is continuous on $[a,b]$, then the function $g$ defined by
> 
> $$
> g(x)=\int_{a}^{x} f(t) \, dt ~~~~a\leq x\leq b 
> $$
> 
> is continuous on $[a,b]$ and differentiable on $(a,b)$, and $g'(x)=f(x)$.
> 

Or we can write this theorem as when $f$ is continuous 
$$
\frac{d}{dx}\int_{a}^{x} f(t) \, dt=f(x) 
$$

> [!NOTE] The Fundamental Theorem of Calculus, Part 2
> If $f$ is continuous on $[a,b]$, then 
> 
> $$
> \int_{a}^{b} f(x) \, dx =F(b)-F(a)
> $$
> where $F$ is any antiderivative of $f$, that is a function such that $F'=f$.

Combine to together

> [!NOTE] The Fundamental Theorem of Calculus
> Suppose $f$ is continuous on $[a,b]$.
> 1) If $g(x)=\int_{a}^{x} f(t) \, dt$, then $g'(x)=f(x)$
> 2) $\int_{a}^{b} f(x) \, dx=F(b)-F(a)$, where $F'=f$.
> 

---

## Indefinite Integrals and the Net Change Theorem

From FTC1, we know that $\int f(x) \, dx=F(x)$ where $F'(x)=f(x)$.

For example 

$$
\int x^{2} \, dx= \frac{x^{3}}{3}+c \text{ because } \frac{d}{dx}\left( \frac{x^{3}}{3}+c \right)
$$

Any formula can be verified by differentiating the function on the right side and obtaining the integrand.

Remark
We adopt the convention that when a formula for a general indefinite integral is given, it is valid only on an interval.

$$
\int  \frac{1}{x^{2}} \, dx=- \frac{1}{x}+c
$$

with the understanding that it is valid on the interval $(0,\infty)$ or $(-\infty,0)$

This is true despite the general antiderivative of the function is

$$
F(x)=\begin{cases}
-\frac{1}{x}+c_{1} & if & x<0 \\
-\frac{1}{x}+c_{2} & if & x>0
\end{cases}
$$
---
### Application

From FTC2

$$
 \int_{a}^{b} f(x) \, dx =F(b)-F(a)
$$

where $F$ is any antiderivative of $f$. This means that $F'=f$, so

$$
 \int_{a}^{b} F'(x) \, dx =F(b)-F(a)
$$

We know that $F'(x)$ is the rate of change of $y=F(x)$ with respect of $x$.

Thus, we can reformulate FTC2

> [!NOTE] Net Change Theorem
> The integral of a rate of change is the net change:
> 
> $$
> \int_{a}^{b} F'(x) \, dx=F(b)-F(a) 
> $$
> 


