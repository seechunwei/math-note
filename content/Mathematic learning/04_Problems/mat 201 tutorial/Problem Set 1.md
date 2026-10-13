---
aliases:
  - /mathematic-note/04_Problems/mat-201-tutorial/Problem_Set_1
  - /mathematic-note/04_Problems/mat-201-tutorial/Problem-Set-1
---
Instructions: Please make a genuine attempt at the problems before coming to the tutorial, especially the standard problems. Group discussion and peer assistance are strongly encouraged. Working through a problem yourself—even if you get stuck—is an essential part of learning. 

Problems marked with an asterisk (*) will be discussed during the tutorial, if time permits. Since tutorial time is limited, the tutor may focus on the key ideas and approaches rather than writing down every detail step in the solution. Come prepared with your own attempts and questions so that you can follow and understand the discussion. 

Solutions to all problems will be provided on e-Learn afterwards. There is therefore no need to copy solutions during the tutorial. More importantly, seeing a solution is not the same as being able to solve the problem yourself. Give each problem an honest attempt first—the thinking you do before seeing the solution is where much of the learning happens. 

## Standard problems

1) Given that 

$$
\lim_{x \to a} f(x) = 0, \quad \lim_{x \to a} g(x) = 1, \quad \lim_{x \to a} h(x) = \infty, \quad \text{and} \quad \lim_{x \to a} p(x) = -\infty,
$$

which of the following limits are indeterminate forms? For those that are not, evaluate the limits where possible. 

(a) $\lim_{x \to a} \frac{f(x)}{p(x)}$ 
$\frac{0}{\infty}$  not indeterminate. Thus
$$
\begin{aligned}
\lim_{x \to a} \frac{f(x)}{p(x)} = \frac{0}{\infty} = 0
\end{aligned}
$$

> [!remark]
> A very small number divide very big number push the limit to 0 together

(b) $\lim_{x \to a} [p(x) + h(x)]$ 
$-\infty + \infty$ is an indeterminate form.


(c) $\lim_{x \to a} [g(x)h(x)]$ 
$1 \cdot \infty$ not indeterminate. Thus,
$$
\lim_{x \to a} [g(x)h(x)] = \infty
$$

(d*) $\lim_{x \to a} [f(x)]^{h(x)}$ 
$0^{\infty}$ not indeterminate. Thus,
$$
\lim_{x \to a} [f(x)]^{h(x)} = 0
$$

> [!remark]
> When the base approach to $0$, for example $0$ to 1. The power of the base will shrink to 0. $(0.1)^{1}=0.1$, $(0.1)^{2}=0.01\dots\to 0$.

(e*) $\lim_{x \to a} [h(x)]^{f(x)}$ 
$\infty^{0}$ is an indeterminate form.


2) Find the following limits. Use L’Hospital’s Rule wherever it is applicable. 

(a) $\lim_{x \to 0} \frac{e^{2x} - 1}{\sin x}$ 
Notice that $\lim_{x \to 0}(e^{2x}-1)=0$ and $\lim_{x \to 0}\sin x=0$. Thus, it is an indeterminate form of type $\frac{0}{0}$. Thus, by applying L'Hospital's Rule:
$$
\begin{aligned}
\lim_{x \to 0} \frac{e^{2x}-1}{\sin x} &= \lim_{x \to 0} \frac{2e^{2x}}{\cos x} \\
&= 0
\end{aligned}
$$

(b) $\lim_{x \to \infty} \frac{\ln(\ln x)}{x}$ 
Notice that $\lim_{x \to \infty}\ln(\ln x)=\infty$ and $\lim_{x \to \infty}x=\infty$. Thus, it is an indeterminate form of type $\frac{\infty}{\infty}$. Thus, by applying L'Hospital's Rule:
$$
\begin{aligned}
\lim_{x \to \infty} \frac{\ln(\ln x)}{x} &= \lim_{x \to \infty} \frac{1}{x \ln x} && \text{(Chain rule)} \\
&= 0
\end{aligned}
$$

(c*) $\lim_{x \to 0} \frac{\sin 4x}{\tan 5x}$
Notice that $\lim_{x \to 0}\sin 4x=0$ and $\lim_{x \to 0}\tan 5x=0$. Thus, it is an indeterminate form of type $\frac{0}{0}$. Thus, by applying L'Hospital's Rule:
$$
\begin{aligned}
\lim_{x \to 0} \frac{\sin 4x}{\tan 5x} &= \lim_{x \to 0} \frac{4\cos 4x}{5\sec^2 5x} \\
&= \frac{4}{5} \lim_{x \to 0} \cos 4x \cos^2 5x \\
&= \frac{4}{5}(1) \\
&= \frac{4}{5}
\end{aligned}
$$


(d) $\lim_{x \to 1} \frac{x^8 - 1}{x^5 - 1}$ 
Notice that $\lim_{x \to 1}(x^8-1)=0$ and $\lim_{x \to 1}(x^5-1)=0$. Thus, it is an indeterminate form of type $\frac{0}{0}$. Hence, by applying L'Hospital's Rule:
$$
\begin{aligned}
\lim_{x \to 1} \frac{x^8-1}{x^5-1} &= \lim_{x \to 1} \frac{8x^7}{5x^4} \\
&= 1
\end{aligned}
$$

(e) $\lim_{x \to 0} \frac{x + \sin x}{x + \cos x}$ 
It is not an indeterminate form. Thus, by substitution rule:
$$
\begin{aligned}
\lim_{x \to 0} \frac{x+\sin x}{x+\cos x} &= \frac{0}{1} \\
&= 0
\end{aligned}
$$

(f*) $\lim_{x \to \infty} x^3 e^{-x^2}$ 
Notice that $\lim_{x \to \infty}x^3=\infty$ and $\lim_{x \to \infty}e^{-x^2}= 0$. It is an indeterminate form of type $0\cdot \infty$. Thus, by applying L'Hospital's Rule:
$$
\begin{aligned}
\lim_{x \to \infty} x^3 e^{-x^2} &= \lim_{x \to \infty} \frac{x}{e^{x^2}} \\
&= \lim_{x \to \infty} \frac{1}{2x e^{x^2}} \\
&= 0
\end{aligned}
$$

(g) $\lim_{x \to 0^+} \left[ \frac{1}{x} - \frac{1}{e^x - 1} \right]$ 
Notice that it is an indeterminate form of type $\infty-\infty$. Thus,
by applying L'Hospital's Rule:
$$
\begin{aligned}
\lim_{x \to 0^+} \left[ \frac{1}{x} - \frac{1}{e^x-1} \right] &= \lim_{x \to 0^+} \frac{e^x-1-x}{x(e^x-1)}  \\
&= \lim_{x \to 0^+} \frac{e^x-1}{(e^x-1)+x e^x} \\
&= \lim_{x \to 0^+} \frac{e^x}{e^x+e^x+x e^x} \\
&= \lim_{x \to 0^+} \frac{e^x}{(2+x)e^x} \\
&= \frac{1}{2} 
\end{aligned}
$$

(h*) $\lim_{x \to \infty} (e^x + x)^{1/x}$ 
Notice that it is an indeterminate form of type $\infty^0$. Thus, we let $y=(e^x+x)^{1/x}$ and take the natural logarithm to get $\ln y= \frac{1}{x}\ln(e^x+x)$. 

Find $\lim_{x \to \infty}\ln y$:
$$
\begin{aligned}
\lim_{x \to \infty} \ln y &= \lim_{x \to \infty} \frac{\ln(e^x+x)}{x} \\
&= \lim_{x \to \infty} \frac{e^x+1}{e^x+x} \\
&= \lim_{x \to \infty} \frac{1+ \frac{1}{e^x}}{1+ \frac{x}{e^x}}
\end{aligned}
$$
Notice that by L'Hospital's Rule $\lim_{x \to \infty} \frac{x}{e^x}= \lim_{x \to \infty} \frac{1}{e^x}=0$. Thus, by substitution:

$$
\begin{aligned}
\lim_{x \to \infty} \ln y &= \lim_{x \to \infty} \frac{1+ \frac{1}{e^x}}{1+ \frac{x}{e^x}} \\
&= 1
\end{aligned}
$$
Finally, by the continuity of the exponential function:

$$
\lim_{x \to \infty} (e^x+x)^{1/x}= e^{\lim_{x \to \infty} \ln y}=e
$$


(i) $\lim_{x \to \frac{\pi}{2}} \cos x\sec 5x$ 
$$
\begin{aligned}
\lim_{x \to \frac{\pi}{2}} \cos x \sec 5x &= \lim_{x \to \frac{\pi}{2}} \frac{\cos x}{\cos 5x} \\
&= \lim_{x \to \frac{\pi}{2}} \frac{-\sin x}{-5\sin 5x} \\
&= \frac{1}{5}(1) \\
&= \frac{1}{5}
\end{aligned}
$$

(j) $\lim_{x \to 0^+} (\cos x)^{1/x^2}$ 
It is an indeterminate form of type $1^\infty$. Let $y=(\cos x)^{1/x^2}$ and take the natural logarithm to get $\ln y= \frac{1}{x^2}\ln(\cos x)$. Thus,

$$
\begin{aligned}
\lim_{x \to 0^+} \ln y &= \lim_{x \to 0^+} \frac{\ln(\cos x)}{x^2} \\
&= \lim_{x \to 0^+} \frac{-\sin x}{2x \cos x} \\
&= \lim_{x \to 0^+} \frac{-\tan x}{2x} \\
&= \lim_{x \to 0^+} \frac{-\sec^2 x}{2} \\
&= \lim_{x \to 0^+} -\frac{1}{2\cos^2 x} \\
&= -\frac{1}{2}   
\end{aligned}
$$

(k) $\lim_{x \to \infty} (x - \ln x)$ 
$$
\begin{aligned}
\lim_{x \to \infty} (x-\ln x) &= \lim_{x \to \infty} (x\ln e-\ln x) \\
&= \lim_{x \to \infty} \left( \ln \frac{e^x}{x} \right) \\ 
&= \ln \left( \lim_{x \to \infty} \frac{e^x}{x} \right) \\
&= \ln\left( \lim_{x \to \infty} \frac{e^x}{1} \right) \\
&= \infty
\end{aligned}
$$


3*) Show that $\lim_{x \to \infty} \frac{x + \sin x}{x} = 1$. What can you say about $\lim_{x \to \infty} \frac{\frac{d}{dx}(x + \sin x)}{\frac{d}{dx} x}$? Does it violate L’Hospital’s Rule? 

$$
\begin{aligned}
\lim_{x \to \infty} \frac{x+\sin x}{x} &= \lim_{x \to \infty} \left( 1+ \frac{\sin x}{x} \right) \\
&= 1+\lim_{x \to \infty} \frac{\sin x}{x}
\end{aligned}
$$
Notice that since $-1 \le \sin x \le 1$, it follows that for $x > 0$:
$$
-\frac{1}{x} \le \frac{\sin x}{x} \le \frac{1}{x}
$$
Since $\lim_{x \to \infty} \left(-\frac{1}{x}\right) = 0$ and $\lim_{x \to \infty} \frac{1}{x} = 0$, it follows that $\lim_{x \to \infty} \frac{\sin x}{x} = 0$ by the Squeeze Theorem. $\blacksquare$


It is an indeterminate form of type $\frac{\infty}{\infty}$. By applying L'Hospital's Rule:

$$
\begin{aligned}
\lim_{x \to \infty} \frac{x+\sin x}{x} &= \lim_{x \to \infty} \frac{1+\cos x}{1}
\end{aligned}
$$
Since as $x\to \infty$, $1+\cos x$ oscillates between $0$ and $2$ without approaching any single value. Therefore, this limit does not exist.

No, L'Hospital's Rule states that if $\lim_{x \to a} \frac{f'(x)}{g'(x)}$ exists or is $\pm\infty$, then $\lim_{x \to a} \frac{f(x)}{g(x)} = \lim_{x \to a} \frac{f'(x)}{g'(x)}$. Since the hypothesis is not fulfilled, we cannot deduce anything about $\lim_{x \to a} \frac{f(x)}{g(x)}$ by L'Hospital's Rule.


4) Determine whether each of the following integrals is convergent or divergent. 
(a) $\int_1^\infty \frac{\ln x}{x} \, dx$ 

$$
\int_1^\infty \frac{\ln x}{x} \, dx = \lim_{t \to \infty} \int_1^t \frac{\ln x}{x} \, dx
$$
Let $u = \ln x \implies \frac{du}{dx} = \frac{1}{x} \implies dx = x \, du$. When $x = 1 \implies u = \ln 1 = 0$.
Thus,

$$
\begin{aligned}
\int_1^\infty \frac{\ln x}{x} \, dx &= \lim_{t \to \infty} \int_0^{\ln t} u \, du \\  
&= \lim_{t \to \infty} \left[ \frac{u^2}{2} \right]_0^{\ln t} \\
&= \lim_{t \to \infty} \left( \frac{(\ln t)^2}{2} - 0 \right) \\
&= \infty
\end{aligned}
$$
Thus, the integral is divergent.

(b) $\int_0^1 \frac{1}{1-x} \, dx$ 

$$
\begin{aligned}
\int_0^1 \frac{1}{1-x} \, dx &= \lim_{t \to 1^-} \int_0^t \frac{1}{1-x} \, dx \\
&= \lim_{t \to 1^-} \left[ -\ln|1-x| \right]_0^t \\
&= \lim_{t \to 1^-} (-\ln|1-t| - 0) \\
&= -(-\infty) \\
&= \infty
\end{aligned}
$$
Thus, the integral is divergent.

(c*) $\int_{-\infty}^0 y e^{3y} \, dy$ 

$$
\int_{-\infty}^0 y e^{3y} \, dy = \lim_{t \to -\infty} \int_t^0 y e^{3y} \, dy
$$
Let $u = y \implies u' = 1$ and $w' = e^{3y} \implies w = \frac{e^{3y}}{3}$. Thus,

$$
\begin{aligned}
\lim_{t \to -\infty} \int_t^0 y e^{3y} \, dy &= \lim_{t \to -\infty} \left( \left[ \frac{ye^{3y}}{3} \right]_t^0 - \int_t^0 \frac{e^{3y}}{3} \, dy \right) \\
&= \lim_{t \to -\infty} \left[ \frac{ye^{3y}}{3} - \frac{e^{3y}}{9} \right]_t^0 \\
&= \lim_{t \to -\infty} \left( \left[ 0 - \frac{1}{9} \right] - \left[ \frac{t e^{3t}}{3} - \frac{e^{3t}}{9} \right] \right) \\
&= -\frac{1}{9} - \frac{1}{3}\lim_{t \to -\infty} (t e^{3t}) + \frac{1}{9}\lim_{t \to -\infty} (e^{3t}) \\
&= -\frac{1}{9} - 0 + 0 \\
&= -\frac{1}{9}
\end{aligned}
$$
Since $\lim_{t \to -\infty} t e^{3t} = \lim_{t \to -\infty} \frac{t}{e^{-3t}} \overset{\text{H}}{=} \lim_{t \to -\infty} \frac{1}{-3e^{-3t}} = 0$.

Thus, the integral is convergent and equals $-\frac{1}{9}$.


(d*) $\int_1^\infty \frac{e^{-\sqrt{x}}}{\sqrt{x}} \, dx$


(e*) $\int_2^3 \frac{1}{(2x - 6)^3} \, dx$ 

(f) $\int_0^9 \frac{1}{\sqrt[3]{x - 1}} \, dx$ 


# Non-standard Problems

5) If $f'$ is continuous, $f(2) = 0$, and $f'(2) = 7$, evaluate $\lim_{x \to 0} \frac{f(2 + 3x) + f(2 + 5x)}{x}$.

6) (*) For which values of $a$ and $b$ does $\lim_{x \to 0} \left( \frac{\sin 2x}{x^3} - a + \frac{b}{x^2} \right) = 0$?

7) (Easy) (a) Show that $\int_{-\infty}^\infty x \, dx$ is divergent according to our definition. 

(b) Show that $\lim_{t \to \infty} \int_{-t}^t x \, dx = 0$.

(Remark: Therefore, the improper integral $\int_{-\infty}^\infty f(x) \, dx$ is not the same as $\lim_{t \to \infty} \int_{-t}^t f(x) \, dx$.) 

8) Show that the improper integral $\int_0^1 \frac{1}{x^p} \, dx$ for $p > 0$ is convergent when $0 < p < 1$ and divergent when $p \ge 1$. (Note that when $p \le 0$, it is not an improper integral.) 

Hint: Consult the proof of the theorem regarding the convergence of $\int_1^\infty \frac{1}{x^p} \, dx$. 