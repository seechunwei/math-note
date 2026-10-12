## Problem Set 1

Instructions: Please make a genuine attempt at the problems before coming to the tutorial, especially the standard problems. Group discussion and peer assistance are strongly encouraged. Working through a problem yourself—even if you get stuck—is an essential part of learning. 

Problems marked with an asterisk (*) will be discussed during the tutorial, if time permits. Since tutorial time is limited, the tutor may focus on the key ideas and approaches rather than writing down every detail step in the solution. Come prepared with your own attempts and questions so that you can follow and understand the discussion. 

Solutions to all problems will be provided on e-Learn afterwards. There is therefore no need to copy solutions during the tutorial. More importantly, seeing a solution is not the same as being able to solve the problem yourself. Give each problem an honest attempt first—the thinking you do before seeing the solution is where much of the learning happens. 

## Standard problems

1) Given that 

$$
\lim _ {x \to a} f (x) = 0, \lim _ {x \to a} g (x) = 1, \lim _ {x \to a} h (x) = \infty , \text { and } \lim _ {x \to a} p (x) = - \infty ,
$$

which of the following limits are indeterminate forms? For those that are not, evaluate the limits where possible. 
(a) $\operatorname* { l i m } _ { x \to a } { \frac { f ( x ) } { p ( x ) } }$ 
$\frac{0}{\infty}$  not indeterminate. Thus
$$
\begin{align}
\lim_{ x \to a } \frac{f(x)}{p(x)}= \frac{0}{\infty}=0
\end{align}
$$

> [!remark]
> A very small number divide very big number push the limit to 0 together

(b) $\operatorname* { l i m } _ { x \to a } [ p ( x ) + h ( x ) ]$ 
$-\infty+\infty$ is an indeterminate form.


(c) $\operatorname* { l i m } _ { x \to a } [ g ( x ) h ( x ) ]$ 
$1\cdot \infty$ not indeterminate. Thus,
$$
\lim_{ x \to a } [g(x)h(x)]=\infty
$$

(d*) $\operatorname* { l i m } _ { x \to a } [ f ( x ) ] ^ { h ( x ) }$ 
$0^{\infty}$ not indeterminate. Thus,
$$
\operatorname* { l i m } _ { x \to a } [ f ( x ) ] ^ { h ( x ) }=0
$$

> [!remark]
> When the base approach to $0$, for example $0$ to 1. The power of the base will shrink to 0. $(0.1)^{1}=0.1$, $(0.1)^{2}=0.01\dots\to 0$.

(e*) $\operatorname* { l i m } _ { x \to a } [ h ( x ) ] ^ { f ( x ) }$ 
$\infty^{0}$ is an indeterminate form.


2) Find the following limits. Use L’Hospital’s Rule wherever it is applicable. 

(a) $\operatorname* { l i m } _ { x \to 0 } { \frac { e ^ { 2 x } - 1 } { \sin x } }$ 
Notice that $\lim_{ x \to 0 }e^{2x}-1=0$ and $\lim_{ x \to 0 }\sin x=0$. Thus, it is an indeterminate form of type $\frac{0}{0}$. Thus, by applying L'Hospital's Rule:
$$
\begin{align}
\lim_{ x \to 0 } \frac{e^{2x}-1}{\sin x}&=\lim_{ x \to 0 } \frac{2e^{2x}}{\cos x} \\
&=0
\end{align}
$$

(b) $\operatorname* { l i m } _ { x \to \infty } { \frac { \ln \ln x } { x } }$ 
Notice that $\lim_{ x \to \infty }\ln(\ln x)=\infty$ and $\lim_{ x \to \infty }x=\infty$. Thus, it is an indeterminate form of  type $\frac{\infty}{\infty}$. Thus, by applying L'Hospital's Rule
$$
\begin{align}
\lim_{ x \to \infty } \frac{\ln(\ln x)}{x}&=\lim_{ x \to \infty } \frac{1}{x(\ln x)} && \text{(Chain rule)}\\
&=0
\end{align}
$$

(c*) $\operatorname* { l i m } _ { x \to 0 } { \frac { \sin 4 x } { \tan 5 x } }$
Notice that $\lim_{ x \to 0 }\sin 4x=0$ and $\lim_{ x \to 0 } \tan 5x=0$. Thus, it is an indeterminate form of type $\frac{0}{0}$. Thus, by applying L'Hospital's Rule:
$$
\begin{align}
\lim_{ x \to 0 } \frac{\sin 4x}{\tan 5x}&= \lim_{ x \to 0 }  \frac{4\cos 4x}{5(\sec ^{2}5x)} \\
&=\frac{4}{5}\lim_{ x \to 0 } \cos 4x (\cos ^{2}5x) \\
&=\frac{4}{5} (1) \\
&= \frac{4}{5}
\end{align}
$$


(d) $\operatorname* { l i m } _ { x \to 1 } { \frac { x ^ { 8 } - 1 } { x ^ { 5 } - 1 } }$ 
Notice that $\lim_{ x \to 1 }x^{8}-1=0$ and $\lim_{ x \to 1 }x^{5}-1=0$. Thus, it is an indeterminate form of type $\frac{0}{0}$. Hence, by applying L'Hospital's Rule:
$$
\begin{align}
\lim_{ x \to 1 } \frac{x^{8}-1}{x^{5}-1}&= \lim_{ x \to 1 }  \frac{8x^{7}}{5x^{4}} \\
&= 1
\end{align}
$$

(e) $\operatorname* { l i m } _ { x \to 0 } { \frac { x + \sin x } { x + \cos x } }$ 
It is not an indeterminate form. Thus, by substitution rule
$$
\begin{align}
\lim_{ x \to 0 } \frac{x+\sin x}{x+\cos x}&= \frac{0}{1} \\
&=0
\end{align}
$$

(f*) $\operatorname* { l i m } _ { x \to \infty } x ^ { 3 } e ^ { - x ^ { 2 } }$ 
Notice that $\lim_{ x \to \infty }x^{3}=\infty$ and $\lim_{ x \to \infty }e^{-x^{2}}= 0$. It is an indeterminate form of type $0\cdot \infty$. Thus, by applying L'Hospital's Rule:
$$
\begin{align}
\lim_{ x \to \infty } x^{3}e^{-x^{2}}&= \lim_{ x \to \infty } \frac{x}{e^{x^{2}}} \\
&= \lim_{ x \to \infty }  \frac{1}{2xe^{x^{2}}} \\
&= 0
\end{align}
$$

(g) $\operatorname* { l i m } _ { x \to 0 ^ { + } } \left[ { \frac { 1 } { x } } - { \frac { 1 } { e ^ { x } - 1 } } \right]$ 
Notice that it is an indeterminate form of type $\infty-\infty$. Thus,
by applying L'Hospital's Rule:
$$
\begin{align}
\lim_{ x \to 0^{+} } \left[ \frac{1}{x}- \frac{1}{e^{x}-1} \right]&= \lim_{ x \to 0^{+} } \frac{e^{x}-1-x}{x(e^{x}-1)}  \\
&=\lim_{ x \to 0^{+} } \frac{e^{x}-1}{(e^{x}-1)+x(e^{x})} \\
&= \lim_{ x \to 0^{+} }  \frac{e^{x}}{e^{x}+e^{x}+xe^{x}} \\
&= \lim_{ x \to 0^{+} } \frac{e^{x}}{(2+x)e^{x}} \\
&= \frac{1}{2} 
\end{align}
$$

(h*) $\operatorname* { l i m } _ { x \to \infty } ( e ^ { x } + x ) ^ { 1 / x }$ 
Notice that it is an indeterminate form of type $\infty^{0}$. Thus, we let $y=(e^{x}+x)^{1/x}$ and take the natural logarithms to get $\ln y= \frac{1}{x}(\ln(e^{x}+x))$. 

Find $\lim_{ x \to \infty }\ln y$:
$$
\begin{align}
\lim_{ x \to \infty } \ln y&=\lim_{ x \to \infty } \frac{\ln(e^{x}+x)}{x} \\
&= \lim_{ x \to \infty } \frac{e^{x}+1}{(e^{x}+x)} \\
&= \lim_{ x \to \infty } \frac{1+ \frac{1}{e^{x}}}{1+ \frac{x}{e^{x}}} \\
\end{align}
$$
Notice that by L'Hospital's Rule $\lim_{ x \to \infty } \frac{x}{e^{x}}= \lim_{ x \to \infty } \frac{1}{e^{ x }}=0$. Thus, by substitution

$$
\begin{align}
\lim_{ x \to \infty } \ln y&= \lim  \lim_{ x \to \infty } \frac{1+ \frac{1}{e^{x}}}{1+ \frac{x}{e^{x}}} \\
&= 1
\end{align}
$$
Finally, by the continuity of the exponential function

$$
\lim_{ x \to \infty } (e^{x}+x)^{1/x}= e^{\lim_{ x \to \infty } \ln y}=e
$$


(i) $\lim_{ x \to \frac{\pi}{2} }\cos x\sec 5x$ 
$$
\begin{align}
\lim_{ x \to \frac{\pi}{2} } \cos x \sec 5x&=\lim_{ x \to \frac{\pi}{2} } \frac{\cos x}{\cos 5x} \\
&= \lim_{ x \to \frac{\pi}{2} } \frac{-\sin x}{-5\sin 5x} \\
&= \frac{1}{5}(1) \\
&= \frac{1}{5}
\end{align}
$$

(j) $\operatorname* { l i m } _ { x \to 0 ^ { + } } ( \cos x ) ^ { 1 / x ^ { 2 } }$ 
It is an indeterminate form of type $1^{\infty}$. Let $y=(\cos x)^{1/x^{2}}$ and take the natural logarithms $\ln y= \frac{1}{x^{2}}\ln(\cos x)$. Thus,

$$
\begin{align}
\lim_{ x \to 0^{+} }\ln y&= \lim_{ x \to 0^{+} } \frac{\ln(\cos x)}{x^{2}} \\
&= \lim_{ x \to 0^{+} } \frac{-\sin x}{\cos x\cdot {2}x} \\
&= \lim_{ x \to 0^{+} } \frac{-\tan x}{2x} \\
&= \lim_{ x \to 0^{+} } \frac{-\sec ^{2}x}{2} \\
&= \lim_{ x \to 0^{+} } - \frac{1}{2\cos ^{2}x} \\
&=- \frac{1}{2}   
\end{align}
$$

(k) $\operatorname* { l i m } _ { x \to \infty } ( x - \ln x )$ 
$$
\begin{align}
\lim_{ x \to \infty } (x-\ln x)&= \lim_{ x \to \infty } (x\ln e-\ln x) \\
&=\lim_{ x \to \infty } \left( \ln \frac{e^{x}}{x} \right) \\ 
&=\ln \left( \lim_{ x \to \infty } \frac{e^{x}}{x} \right) \\
&=\ln\left( \lim_{ x \to \infty } \frac{e^{x}}{1} \right) \\
&=\infty
\end{align}
$$


3*) Show that $\operatorname* { l i m } _ { x \to \infty } { \frac { x + \sin x } { x } } = 1$ . What can you say about $\operatorname* { l i m } _ { x \to \infty } { \frac { { \frac { d } { d x } } ( x + \sin x ) } { \frac { d } { d x } x } } ?$ Does it violate L’Hospital’s Rule? 

$$
\begin{align}
\lim_{ x \to \infty } \frac{x+\sin x}{x}&=\lim_{ x \to \infty } \left( 1+ \frac{\sin x}{x} \right) \\
&=1+\lim_{ x \to \infty } \frac{\sin x}{x}
\end{align}
$$
Notice that since $-1\leq\sin x\leq 1$, it follow that 
$$
-\frac{1}{x}< \frac{\sin x}{x}< \frac{1}{x}
$$
Since $\lim_{ x \to \infty }-\frac{1}{x}=0$ and $\lim_{ x \to \infty } \frac{1}{x}=0$, it follow that $\lim_{ x \to \infty } \frac{\sin x}{x}=0$ by Squeeze Theorem.$\blacksquare$


It is an indeterminate form of type $\frac{\infty}{\infty}$. By applying L'Hospital's Rule:

$$
\begin{align}
\lim_{ x \to \infty } \frac{x+\sin x}{x}&= \lim_{ x \to \infty } \frac{1+\cos x}{1}  \\
\end{align}
$$
Since as $x\to \infty$, $1+\cos x$ oscillates between $0$ and $2$ without approaching any single value. Therefore, this limit does not exist.

No, the L'Hospital's Rule state if $\lim_{ x \to  a} \frac{f'(x)}{g'(x)}$ exist or this limit is $\infty$ or $-\infty$, then $\lim_{ x \to a } \frac{f(x)}{g(x)}=\lim_{ x \to a } \frac{f'(x)}{g'(x)}$. Since the hypothesis is not fulfill, then we deduce anything about $\lim_{ x \to a } \frac{f(x)}{g(x)}$ by L'Hospital's Rule.


4) Determine whether each of the following integrals is convergent or divergent. 
 (a) $\int _ { 1 } ^ { \infty } { \frac { \ln x } { x } } d x$ 

$$
\begin{align} 
\int _{1}^{\infty} \frac{\ln x}{x} \, dx&= \lim_{ t \to \infty } \int _{1}^{t} \frac{\ln x}{x} \, dx \\ 
\end{align}
$$
Let $u=\ln x$ $\frac{du}{dx}= \frac{1}{x}\implies dx=xdu$. $x=1\implies u=\ln 1=0$
Thus,

$$
\begin{align}
\int _{1}^{\infty} \frac{\ln x}{x} \, dx&= \lim_{ t \to \infty } \int _{0}^{\ln t} \ u \, du \\  
&=\lim_{ t \to \infty } \left[ \frac{u^{2}}{2} \right]^{\ln t}_{0} \\
&=\lim_{ t \to \infty } \left( \frac{(\ln t)^{2}}{2}-0 \right) \\
&=\infty
\end{align}
$$
Thus, the integral is divergent.

(b) $\int _ { 0 } ^ { 1 } { \frac { 1 } { 1 - x } } d x$ 

$$
\begin{align}
\int_{0}^{1} \frac{1}{1-x} \, d&= \lim_{ t \to 1^{-} } \int_{0}^{t} \frac{1}{1-x} \, dx \\
&= \lim_{ t \to 1^{-} } [-\ln |1-x|]^{t}_{0} \\
&=\lim_{ t \to 1^{-} } (-\ln| (1-t)-0) \\
&= -(-\infty) \\
&=\infty
\end{align}
$$
Thus, the integral is divergent.

(c*) $\int _ { - \infty } ^ { 0 } y e ^ { 3 y } d y$ 

$$
\begin{align}
\int_{-\infty}^{0} ye^{3y} \, dy&=\lim_{ t \to -\infty } \int_{t}^{0}ye^{3y}  \, dy \\
\end{align}
$$
Let $u=y\implies u'=1$ and $w'=e^{3y}\implies w= \frac{e^{3y}}{3}$.Thus,

$$
\begin{align}
\lim_{ t \to -\infty } \int_{t}^{0}ye^{3y}  \, dy&=\lim_{ t \to -\infty } \left(  \left[ \frac{ye^{3y}}{3} \right]^{0}_{t} -\int_{t}^{0}  \frac{e^{3y}}{3} \, dy \right) \\
&= \lim_{ t \to -\infty } \left[ \frac{ye^{3y}}{3} - \frac{e^{3y}}{9} \right]^{0}_{t} \\
&= \lim_{ t \to -\infty } \left( \left[ 0 - \frac{1}{9} \right] - \left[ \frac{te^{3t}}{3} - \frac{e^{3t}}{9} \right] \right) \\
&= -\frac{1}{9} - \frac{1}{3}\lim_{ t \to -\infty } (te^{3t}) + \frac{1}{9}\lim_{ t \to -\infty } (e^{3t}) \\
&= -\frac{1}{9} - 0 + 0 \\
&= -\frac{1}{9}
\end{align}
$$
Since $\lim_{ t \to -\infty } te^{3t} = \lim_{ t \to -\infty } \frac{t}{e^{-3t}} \overset{\text{H}}{=} \lim_{ t \to -\infty } \frac{1}{-3e^{-3t}} = 0$.

Thus, the integral is convergent and equals $-\frac{1}{9}$.


(d*) $\int _ { 1 } ^ { \infty } { \frac { e ^ { - { \sqrt { x } } } } { \sqrt { x } } } d x$


(e*) $\int _ { 2 } ^ { 3 } { \frac { 1 } { ( 2 x - 6 ) ^ { 3 } } } d x$ 

(f) $\int _ { 0 } ^ { 9 } { \frac { 1 } { \sqrt [ 3 ] { x - 1 } } } d x$ 


# Non- standard Problem

5) If $f ^ { \prime }$ is continuous, $f ( 2 ) = 0$ , and $f ^ { \prime } ( 2 ) = 7 .$ , evaluate $\operatorname* { l i m } _ { x \to 0 } { \frac { f ( 2 + 3 x ) + f ( 2 + 5 x ) } { x } }$ 

6) (* )For which values of a and b does  $\lim_{ x \to 0 }\left( { \frac { \sin 2 x } { x ^ { 3 } } } - a + { \frac { b } { x ^ { 2 } } } \right) = 0 ?$ x→0 

7) (Easy) (a) Show that $\int _ { - \infty } ^ { \infty } x d x$ is divergent according to our definition. 

(b) Show that  $\lim_{ t \to \infty }\int _ { - t } ^ { t } x d x = 0 .$ t→∞ 

(Remark: Therefore, the improper integral $\int _ { - \infty } ^ { \infty } f ( x ) d x$ is not the same as $\operatorname* { l i m } _ { t \to \infty } \int _ { - t } ^ { t } f ( x ) d x . )$ 

8) Show that the improper integral $\int _ { 0 } ^ { 1 } { \frac { 1 } { x ^ { p } } } d x$ for $p > 0$ is convergent when $0 < p < 1$ and divergent when $p \geq 1$ . (Note that when $p \leq 0$ , it is not an improper integral.) 

Hint: Consult the proof of the theorem regarding the convergence of $\int _ { 1 } ^ { \infty } { \frac { 1 } { x ^ { p } } } d x .$ 