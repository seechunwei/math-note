Suppose we have three functions, $f(x)$, $g(x)$, and $h(x)$, such that for all $x$ near a point $c$ (except possibly at $c$ itself):

1. **The Trap:** $g(x) \leq f(x) \leq h(x)$
    
2. **The Limits:** $\lim_{x \to c} g(x) = L$ and $\lim_{x \to c} h(x) = L$

**Conclusion:**

$$\lim_{x \to c} f(x) = L$$

Squeeze theorem is good at applying at trigonometric function which is oscillating within a boundary point.


We can use squeeze theorem to prove the fundamental trigonometric limits
$$
\lim_{ h \to 0 }  \frac{\sin(h)}{h}=1
$$

We cannot direct substitute and factorize. Thus, we can try compare $\theta$ and $\sin \theta$. 

$\theta$ is an arc length while $\sin \theta$ is y-coordinate (vertical length).
How to compare them? We turn it into area.


The area of small triangle form by $(0,0),(\cos \theta,0),(\cos \theta,\sin \theta)$

$$
Area= \frac{1}{2}\cos \theta \sin \theta
$$
The circular sector. The "pizza slice" with angle $\theta$.

$$
Area= \frac{1}{2}r^{2}\theta= \frac{1}{2}\theta
$$

Large triangular: Outside the circle, with vertices at $(0,0),(1,0)$ and $(1,\tan \theta)$ 
Why is $\tan \theta$?
It is because 
$$
\begin{align}
\tan \theta&=\frac{AC}{OA} \\
&=\frac{\text{Height}}{1} \\
\text{Height}&=\tan \theta
\end{align}
$$

Thus, the area

$$
Area= \frac{1}{2}(\tan \theta)= \frac{\sin \theta}{2\cos \theta}
$$

![[Pasted image 20260430183324.png]]

Thus, we can create an inequality between these 3 area by restricting $\theta \in\left( 0, \frac{\pi}{2} \right)$

$$
\begin{array}
/ \frac{1}{2}\cos \theta \sin \theta< \frac{1}{2}\theta < \frac{\sin \theta}{2\cos \theta} \\

\end{array}
$$

First, multiply the entire inequality by $2$ to clear the fractions:

$$\cos \theta \sin \theta < \theta < \tan \theta$$

### 2. Addressing the Division by $\sin \theta$

To get $\frac{\sin \theta}{\theta}$ in the middle, we need to divide. You asked: _Can we do this if $\sin \theta$ can be zero?_

- **The Limit Definition:** In the limit $\lim_{\theta \to 0}$, we evaluate values of $\theta$ that are arbitrarily close to $0$, but **never equal to $0$**.
    
- **The Interval:** We restrict our proof to the interval $(0, \frac{\pi}{2})$. Within this interval, $\sin \theta$ is strictly positive ($\sin \theta > 0$).
    
- **Non-Zero Guarantee:** Since $\sin \theta \neq 0$ for all $\theta$ in our chosen interval, division is mathematically legal.

Divide the inequality by $\sin \theta$:

$$\frac{\cos \theta \sin \theta}{\sin \theta} < \frac{\theta}{\sin \theta} < \frac{\tan \theta}{\sin \theta}$$

Since $\tan \theta = \frac{\sin \theta}{\cos \theta}$, the right side simplifies:

$$\cos \theta < \frac{\theta}{\sin \theta} < \frac{1}{\cos \theta}$$

### 4. Taking the Reciprocal

To find $\frac{\sin \theta}{\theta}$, we take the reciprocal of all terms. This **flips** the inequality signs:

$$\frac{1}{\cos \theta} > \frac{\sin \theta}{\theta} > \cos \theta$$

Or, written more traditionally:

$$\cos \theta < \frac{\sin \theta}{\theta} < \frac{1}{\cos \theta}$$

### 5. Applying the Squeeze

Now we apply the limit as $\theta \to 0$:

- $\lim_{\theta \to 0} \cos \theta = 1$
    
- $\lim_{\theta \to 0} \frac{1}{\cos \theta} = 1$
    

By the **Squeeze Theorem**, since $\frac{\sin \theta}{\theta}$ is trapped between two functions that both approach $1$, it must also approach $1$.

### 3. The "Pure" Alternative: Taylor Series

If the geometric approach feels too "visual" or arbitrary, the **analytic** approach defines $\sin(x)$ as a power series:

$$\sin(x) = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \dots$$

When you divide by $x$:

$$\frac{\sin(x)}{x} = 1 - \frac{x^2}{3!} + \frac{x^4}{5!} - \dots$$

As $x \to 0$, all the terms with $x$ vanish, leaving you with **1**. Many mathematicians prefer this because it relies purely on algebra rather than drawing circles, though it requires you to first prove that the series itself is valid.

---

How about $\lim_{ h \to 0 } \frac{\cos h-1}{h}$

$$
\begin{align}
\lim_{ h \to 0 } \frac{\cos h-1}{h}&= \lim_{ h \to 0 }  \frac{(\cos h-1)(\cos h+1)}{h(\cos h+1)} \\
&=\lim_{ h \to 0 } \frac{\cos ^{2}h-1}{h(\cos h+1)} \\
&=\lim_{ h \to 0 } \frac{-\sin ^{2}h}{h(\cos h+1)} \\
&=\lim_{ h \to 0 }[ - \frac{\sin h}{h}\cdot \frac{\sin h}{\cos h+1}] \\
&=0
\end{align}
$$
---
