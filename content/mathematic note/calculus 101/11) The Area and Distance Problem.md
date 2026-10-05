
The area $A$ of the region $S$ lies under the graph of the continuous function $f$ is the limit of the sum of the areas of approximating rectangles:

$$
A=\lim_{ n \to \infty }R_{n}=\lim_{ n \to \infty } [f(x_{1})\triangle x+f(x_{2})\triangle x+\dots+f(x_{n})\triangle x] 
$$

or

$$
A=\lim_{ n \to \infty } \sum_{i=1}^{n} f(x_{i})\triangle x
$$

$x_{n}=a+n\vartriangle x$

$$
\triangle x= \frac{b-a}{n}
$$

### The idea
To estimate the area under the curve, we approximate using the area of rectangle with same width under the curve. 

In this case we choose to select the height of rectangle with left end points $(L_{n})$ or right endpoints $(R_{n})$

![[Pasted image 20260622113343.png]]

> [!remark]
> If a graph is increasing then using right endpoints will overestimate the area under the graph and it serve as the upper bound of actual area
> 
> If we use left endpoints, then we will underestimate the area under the graph and it serve as the lower bound of actual area

We try to divide the interval $[a,b]$ into $n$ subintervals

$$
[x_{0},x_{1}],[x_{1},x_{2}],\dots,[x_{n-1},x_{n}]
$$


The right endpoints of the subinterval are

$$
\begin{align}
x_{1}&=a+\triangle x, \\
x_{2}&=a+2\triangle x
, \\
\vdots  \\
\end{align}
$$

where

$$
\triangle x= \frac{b-a}{n}
$$

And the area of the ith rectangle is $f(x_{i})\triangle x$.
The approximation will become better as $n\to \infty$ or $\triangle x\to 0$.

---

### The distance problem

Distance equal to time times velocity

$$
D=\lim_{ n \to \infty } \sum_{i=1}^{n} f(t_{i})\triangle t
$$
---

### Problem set 7

6) To evaluate the upper and lower sums for $f(x) = 1 + \cos(x/2)$ on the interval $[-\pi, \pi]$

with $n =3$

### . Behavior of the Function

The function is $f(x) = 1 + \cos(x/2)$.

- At $x = -\pi$, $f(-\pi) = 1 + \cos(-\pi/2) = 1$.
    
- At $x = 0$, $f(0) = 1 + \cos(0) = 2$ (this is the global maximum).
    
- At $x = \pi$, $f(\pi) = 1 + \cos(\pi/2) = 1$.
    

Since $\cos(x/2)$ is symmetric and strictly increasing on $[-\pi, 0]$ and strictly decreasing on $[0, \pi]$, the maximum always occurs closest to $0$, and the minimum always occurs at the boundaries ($\pm\pi$).

For any symmetric partition of $[-\pi, \pi]$ with $n$ subintervals, the width of each subinterval is:

$$\Delta x = \frac{\pi - (-\pi)}{n} = \frac{2\pi}{n}$$

### 2. Evaluation for $n = 3$

Width of each subinterval: $\Delta x = \frac{2\pi}{3}$

The partition points are: $x_0 = -\pi, \, x_1 = -\frac{\pi}{3}, \, x_2 = \frac{\pi}{3}, \, x_3 = \pi$

- **Subinterval 1: $[-\pi, -\frac{\pi}{3}]$**
    
    - Lower bound ($m_1$) at $x = -\pi$: $f(-\pi) = 1$
        
    - Upper bound ($M_1$) at $x = -\frac{\pi}{3}$: $f(-\frac{\pi}{3}) = 1 + \cos(-\frac{\pi}{6}) = 1 + \frac{\sqrt{3}}{2}$

> [!cite] Remark
Since $f(x)$ is increasing on this subinterval, thus the lower bound is left endpoints and upper bound us right endpoint.


- **Subinterval 2: $[-\frac{\pi}{3}, \frac{\pi}{3}]$** (Contains the peak at $x=0$)
    
    - Lower bound ($m_2$) at boundaries: $f(\pm\frac{\pi}{3}) = 1 + \frac{\sqrt{3}}{2}$
        
    - Upper bound ($M_2$) at $x = 0$: $f(0) = 2$


> [!cite] Remark
Notice that $f(x)$ is symmetric on this subinterval and its maximum value for $f(x)$ is at $x=0$ while the minimum is at $x=\pm \frac{\pi}{3}$

- **Subinterval 3: $[\frac{\pi}{3}, \pi]$**
    
    - Lower bound ($m_3$) at $x = \pi$: $f(\pi) = 1$
        
    - Upper bound ($M_3$) at $x = \frac{\pi}{3}$: $f(\frac{\pi}{3}) = 1 + \frac{\sqrt{3}}{2}$

> [!cite] Remark
Since $f(x)$ is decreasing on this subinterval, thus its lower bound is at right endpoint while upper bound is at left endpoint
#### Sums for $n=3$:

- **Lower Sum ($L_3$):**
    
    $$L_3 = \Delta x (m_1 + m_2 + m_3) = \frac{2\pi}{3} \left(1 + \left(1 + \frac{\sqrt{3}}{2}\right) + 1\right) = \frac{2\pi}{3} \left(3 + \frac{\sqrt{3}}{2}\right) \approx 8.090$$
    
- **Upper Sum ($U_3$):**
    
    $$U_3 = \Delta x (M_1 + M_2 + M_3) = \frac{2\pi}{3} \left(\left(1 + \frac{\sqrt{3}}{2}\right) + 2 + \left(1 + \frac{\sqrt{3}}{2}\right)\right) = \frac{2\pi}{3} \left(4 + \sqrt{3}\right) \approx 12.005$$


---

# The Definite Integral

> [!NOTE] Definition of a Definite Integral
> If $f$ is a function defined for $a\leq x\leq b$, we divide the interval $[a,b]$ into $n$ subintervals of equal width $\triangle x=\frac{b-a}{n}$. 
> 
> We let $x_{0}(a),x_{1},\dots,x_{n}(b)$ be the endpoints of these subintervals and we let $x_{1}^{*},x_{2}^{*},\dots,x_{n}^{*}$ be any **sample** **points** in these subintervals , so $x_{i}^{*}$ lies in the ith subinterval $[x_{i-1},x_{i}]$. Then the **definite integral of $f$ from $a$ to $b$** is
> 
> $$
> \int_{b}^{a} f(x) \, dx=\lim_{ n \to \infty } \sum_{i=1}^{n} f(x_{i}^{*})\triangle x 
> $$
> 
> provided that this limit exists and gives the same value for all possible choices of sample points. If it does exist, we say that $f$ is **integrable** on $[a,b]$.

> [!remark]
>  ...and gives the same value for all possible choices of sample points."
> 
> This is the most critical part of the definition. The sample point $x_i^*$ is just an $x$-value you pick inside the $i$-th subinterval to determine the **height** of that specific rectangle, $f(x_i^*)$.
> 
> Because the definition says you can pick _any_ sample point, you have complete freedom in how you construct your rectangles:
> 
> - You could always pick the **left endpoint** of each subinterval ($x_i^* = x_{i-1}$).
>     
> - You could always pick the **right endpoint** ($x_i^* = x_i$).
>     
> - You could pick the **midpoint**, or even a completely random point inside each subinterval.
>     
> 
> For a finite number of rectangles (say, $n = 10$), choosing the left endpoint versus the right endpoint will usually give you different total areas. One might underestimate the true area under the curve, while the other might overestimate it.
> 
> However, the sentence states that **as $n$ approaches infinity, the choice of sample points must cease to matter.** Whether you choose the maximum height, the minimum height, the left, the right, or the midpoint, the infinitely thin rectangles must all squeeze down to yield the exact same final value.

---

In the notion $\int_{a}^{b}f(x)  \, dx$ , $f(x)$ is called the **integrand** and $a$ and $b$ are called the limits of integration; $a$ is the **lower limit** and $b$ is the **upper limit.**

Note 1: The definite integral $\int_{a}^{b} f(x) \, dx$ is a number; it does not depend on $x$. In fact, we could use any letter in place of $x$ without changing the value of the integral:

$$
\int_{a}^{b} f(x) \, dx =\int_{a}^{b} f(t) \, dt =\int_{a}^{b} f(r) \, dr 
$$

Note 3:
The sum:
$$
\sum_{i=1}^{n} f(x_{i}^{*})\triangle x
$$
is called **Riemann sum**.

---

Consider a graph that is not always above the x-axis, it have negative value of $f(x)$, then the definite integral can be interpreted as a **net area**. (difference of areas)

![[Pasted image 20260623114152.png]]


There are also situation in which it is better to work with subintervals of unequal width. 

If the subinterval width are $\triangle x_{1},\triangle x_{2},\dots,\triangle x_{n}$, we have to ensure that all these widths approach $0$ in the limiting process,

$$
\int_{a}^{b} f(x) \, dx =\lim_{ max \triangle x_{i} \to \infty }  \sum_{i=1}^{n} f(x_{i}^{*}) \triangle x
$$
### Why $n \to \infty$ fails here

When all rectangles have the exact same width ($\Delta x = \frac{b-a}{n}$), letting the number of rectangles ($n$) go to infinity automatically forces the width ($\Delta x$) of every single rectangle to shrink to $0$.

But if the widths are **unequal**, a dangerous loophole opens up.

Imagine you are integrating from $0$ to $2$. You decide to slice the interval $[0, 1]$ into a million, a billion, or infinitely many tiny subintervals. But you leave the interval $[1, 2]$ as just **one single, giant subinterval**.

If you take the limit as $n \to \infty$:

- The number of rectangles $n$ definitely goes to infinity (because you have infinitely many in the first half).
    
- However, your area approximation will be completely wrong because that one massive rectangle on the right side never shrinks, leaving a huge, inaccurate blocky gap under the curve.
    

### 3. The Fix: "Control the Biggest" ($\max \Delta x_i \to 0$)

To close this loophole, mathematicians stopped focusing on the _number_ of rectangles ($n$) and started focusing on the _widest_ rectangle.

The notation $\max \Delta x_i$ means **"the width of the single largest subinterval in the entire setup."**

By demanding that $\max \Delta x_i \to 0$, you are saying:

> _"I don't care how many rectangles you add, or where you put them. You must shrink the single fattest rectangle down to a width of zero."_

> [!question]
> how demand single rectangle affect other rectangle?

By definition, $\max \Delta x_i$ is the width of the absolute widest subinterval in your partition.

Now, pick _any_ random subinterval from your setup—let's call its width $\Delta x_k$. Because $\max \Delta x_i$ is the largest, your chosen width $\Delta x_k$ must be less than or equal to it. And since widths must be positive, we can write this unbreakable inequality:

$$0 < \Delta x_k \le \max \Delta x_i$$

Now, apply the limit. If we demand that the right side of the inequality goes to zero ($\max \Delta x_i \to 0$), what happens to $\Delta x_k$?

It is trapped. It is trapped between $0$ on the left and a value that is shrinking to $0$ on the right. By the **Squeeze Theorem**, $\Delta x_k$ has absolutely no choice but to shrink to $0$ as well.

Because this applies to _every single_ subinterval $k$ in the partition, forcing the maximum width to zero simultaneously forces **every individual width** to zero.

---

> [!info] Theorem
If $f$ is continuous on $[a,b]$, or if $f$ has only a finite number of jump discontinuities, then $f$ is integrable on $[a,b]$; that is, the definite integral $\int_{a}^{b} f(x) \, dx$ exists.

Why finite number of jump, it is still integrable because it means that the discontinuity is just a point (it is not a line)

![[Pasted image 20260623120427.png]]

Even though we have discontinuity there, but we can split the graph into 2 part. $[a,c']\cup[c',b]$, thus it is still integrable on $[a,b]$.

> [!NOTE] Theorem
> If $f$ is integrable on $[a,b]$, then 
> 
> $$
> \int_{a}^{b} f(x) \, dx =\lim_{ n \to \infty } \sum_{i=1}^{n} f(x_{i}) \triangle x
> $$
> 
> where 
> $$
> \triangle x =\frac{b-a}{n} \text{ and }x_{i}=a+i\triangle x
> $$
> 

Why is $x_{i}$ not $x_{i}^{*}$? because when $n\to \infty$, $x_{i}=x_{i}^{*}$ for any sample points.

it is called Leibniz notation.

---

### How to evaluate integrals?

To evaluate a definite integral, we need to know how to work with the sums.

$$
\begin{align}
\sum_{i=1}^{n} i&= \frac{n(n+1)}{2} \\
\sum_{i=1}^{n} i^{2}&= \frac{n(n+1)(2n+1)}{6} \\
\sum_{i=1}^{n} i^{3}&= \left[ \frac{n(n+1)}{2} \right]^{2}
\end{align}
$$

How to derive?

Example


---
### The Midpoint Rule

$$
\int_{a}^{b} f(x) \, dx \approx  \sum_{i=1}^{n} f(\bar{x}_{i}) \triangle x = \triangle x[f(\bar{x}_{1})+\dots+f(\bar{x})_{n}]
$$

where 

$$
\triangle x= \frac{b-a}{n}
$$
and

$$
\bar{x}_{i}= \frac{1}{2}(x_{i-1}+x_{i})= \text{midpoint of }[x_{i-1},x_{i}]
$$

---

### Properties of the Definite Integral

When we defined the definite integral $\int_{a}^{b} f(x) \, dx$, we implicitly assumed that $a<b$.

But the definition as a limit of Riemann sums makes sense even if $a>b$.

If $a> b$, then $\triangle x$ is negative, in the meanwhile $\frac{a-b}{n}$ is positive 
thus

$$
\int_{b}^{a} f(x) \, dx= -\int_{a}^{b}f(x)  \, dx  
$$


if $a=b,$ then $\triangle x=0$ and so 

$$
\int_{a}^{a} f(x) \, dx =0
$$
### Basic Properties of the Integral
For any function $f(x)$ and $g(x)$ that are integrable on $[a,b]$ (or continuous) and any constant, we have

1) $$
\int_{a}^{b} c \, dx =c(b-a) 
$$2)
$$
\int_{a}^{b} [f(x)+g(x)] \, dx= \int_{a}^{b}f(x)  \, dx  + \int_{a}^{b} g(x) \, dx 
$$

3)
$$
\int_{a}^{b} cf(x) \, dx =c\int_{a}^{b} f(x) \, dx 
$$
4)

$$
\int_{a}^{b} [f(x)-g(x)] \, dx = \int_{a}^{b} f(x) \, dx -\int_{a}^{b} g(x) \, dx  
$$

$2,3,4$ follow the property of summation.

Or intuitively

![[Pasted image 20260623135540.png]]

5)

$$
\int_{a}^{c} f(x) \, dx+\int_{c}^{b} f(x) \, dx = \int_{a}^{b} f(x) \, dx  
$$


### Comparison Properties of the Integral

6)
If $f(x)\geq 0$, for $a\leq x\leq b$. then $\int_{a}^{b}f(x)  \, dx\geq 0$.

7)
if $f(x)\geq g(x)$ for $a\leq x\leq b$, then $\int_{a}^{b} f(x) \, dx\geq \int_{a}^{b} g(x) \, dx$

8)
If $m\leq f(x)\leq M$ for $a\leq x\leq b$, then

$$
m(b-a)\leq \int_{a}^{b} f(x) \, dx \leq M(b-a)
$$


Problem set 7-12