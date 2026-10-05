1) 

$$
\begin{align}
x^{2}-9&\geq 0 \\
(x-3)(x+3)&\geq 0 \\
x\leq -3 \text{ or } x&\geq 3 
\end{align}
$$
$(-\infty,-3]\cup[3,\infty)$

The vertical asymptotes:
$$
\begin{align}
4-\sqrt{ x^{2}-9 }&=0 \\
\sqrt{ x^{2}-9 }&=4 \\
x^{2}-9&=16 \\
x^{2}&=25 \\
x=&\pm 5
\end{align}
$$
Thus,  Domain: $(-\infty,-3]\cup[3,\infty) \setminus \{ -5,5 \}$

2)
$$
\begin{align}
(g\circ h)(x)&=\frac{1}{\frac{1}{x}+4} \\
&=\frac{x}{1+4x}, x\neq -\frac{1}{4}
\end{align}
$$

$$
\begin{align}
(f\circ  g\circ h)(x)&= \sqrt{ \frac{x}{1+4x}+1 } \\
&=\sqrt{ \frac{5x+1}{1+4x} } \\
\end{align}
$$


Domain:
$$
\begin{align}
\frac{5x+1}{1+4x}&\geq 0 \\

\end{align}
$$

Critical point:
vertical asymptotes: $-\frac{1}{4}$
x-intercept: $-\frac{1}{5}$

 **Interval $(-\infty, -1/4)$:** Testing $x = -1$ gives $\frac{-4}{-3} > 0$. (**Valid**)
 **Interval $(-1/4, -1/5]$:** Testing $x = -0.22$ gives $\frac{-0.1}{0.12} < 0$. (**Invalid**)
**Interval $[-1/5, \infty)$:** Testing $x = 1$ gives $\frac{6}{5} > 0$. (**Valid**)

Thus, the domain:
$$
\left( -\infty,-\frac{1}{4} \right)\cap\left[ -\frac{1}{5},\infty \right)
$$


3)
Double-Angle Identity $\sin 2\theta = 2 \sin \theta \cos \theta$

$$2 \sin \theta \cos \theta - \cos \theta = 0$$
$$\cos \theta (2 \sin \theta - 1) = 0$$

$\cos \theta = 0$
$2 \sin \theta - 1 = 0 \implies \sin \theta = \frac{1}{2}$

**From $\cos \theta = 0$:**

- $\theta = \frac{\pi}{2} + n\pi$ (where $n$ is any integer)

- In the interval $[0, 2\pi)$, this gives: **$90^\circ$ ($\frac{\pi}{2}$)** and **$270^\circ$ ($\frac{3\pi}{2}$)**.

**From $\sin \theta = \frac{1}{2}$:**

- $\theta = \frac{\pi}{6} + 2n\pi$ or $\theta = \frac{5\pi}{6} + 2n\pi$
- In the interval $[0, 2\pi)$, this gives: **$30^\circ$ ($\frac{\pi}{6}$)** and **$150^\circ$ ($\frac{5\pi}{6}$)**.

4)
Let $f(x)=\frac{1}{x-1}$
$\lim_{ x \to 1^{-}}f(x)=-\infty$ and $\lim_{ x \to 1^{+} }f(x)=\infty$

Since
$$
\lim_{ x \to 1^{-} } f(x)\neq \lim_{ x \to 1^{+} } f(x)
$$
It follow that $\lim_{ x \to 1 }f(x)$ does not exist.

5)
No, because $f(c)$ is defined is not the necessary condition for  $\lim_{ x \to c }f(x)$ exist. 

To check if the limit exist we only need to check the limit from both side are same or not.

6)
a) 
$$
\begin{align}
\lim_{ x \to -3 } \frac{x+3}{x^{2}+4x+3}&= \lim_{ x \to -3 } \frac{x+3}{(x+3)(x+1)} \\
&=\lim_{ x \to -3 } \frac{1}{x+1} \\
&=-\frac{1}{2}
\end{align}
$$
b)

$$
\begin{align}
\lim_{ x \to 0 } \frac{\frac{1}{x-1}+\frac{1}{x+1}}{x} &= \frac{\frac{2x}{(x+1)(x-1)}}{x} \\
&=\frac{2}{(x+1)(x-1)} \\
&=-2
\end{align}
$$

c)
$$
\begin{align}
\lim_{ x \to 0 } (x^{2}-1)(2-\cos x)&=\lim_{ x \to 0 } (x^{2}-1) \times \lim_{ x \to 0 } (2-\cos x) \\
&=-1\times(1) \\
&=-1
\end{align}
$$

d)
$$
\begin{align}
\lim_{ x \to 0 } \sqrt{ 7-\sec ^{2}x }&= \sqrt{ \lim_{ x \to 0 } (7-\sec ^{2} x) } \\
&=\sqrt{ 7-\lim_{ x \to 0 }  (\frac{1}{\cos x})^{2} } \\
&=\sqrt{ 7-1 } \\
&=\sqrt{ 6 }
\end{align}
$$

7)
a)
Since we cannot substitute , thus we check for one sided limits
$$
\begin{align}
\lim_{ x \to 2^{-} } \frac{x^{2}+5x+4}{x-2}&= \lim_{ x \to 2^{-} } \frac{(x+4)(x+1)}{x-2} \\
&= -\infty
\end{align}
$$
$$
\lim_{ x \to 2^{+} } \frac{(x+4)(x+1)}{x-2}=\infty 
$$

Thus, the limit does not exist.

b)
$$
\begin{align}
\lim_{ t \to 3 } \frac{t^{3}-27}{t^{2}-9} &= \lim_{ t \to 3 } \frac{(t-3)(t^{2}+3t+9)}{(t-3)(t+3)} \\
&=\lim_{ t \to 3 } \frac{t^{2}+3t+9}{t+3} \\
&= \frac{27}{6} \\
&=\frac{9}{2}
\end{align}
$$



9)
$$
\begin{align}
\lim_{ x \to -2 } \frac{3x^{2}+ax+a+3}{x^{2}+x-2} 
\end{align}
$$

Notice that $\lim_{ x \to -2 }x^{2}+x-2=0$. Thus, the one sided limit would be infinite ($\pm\infty$).

$$
\lim_{ x \to -2 } 3x^{2}+ax+a+3=15-a
$$
Thus, the limit only exist when set the numerator equal to 0 which is when $a=15$.


Calculate the limit:

$$
\begin{align}
\lim_{ x \to -2 } \frac{3x^{2}+15x+15+3}{x^{2}+x-2} &=\lim_{ x \to -2 } \frac{3(x^{2}+5x+6)}{(x-1)(x+2)} \\
&= \lim_{ x \to -2 } \frac{3(x+2)(x+3)}{(x-1)(x+2)} \\
&=\lim_{ x \to -2 } \frac{3(x+3)}{x-1} \\
&= -1
\end{align}
$$

==Remark==:
If the denominator is 0, the limit exist only if the numerator is 0. If there exist common factor, then we need to factor and cancel. Why?

if $g(x)=f(x)$ when $x\neq c$, then $\lim_{ x \to c } g(x)=f(c)$

