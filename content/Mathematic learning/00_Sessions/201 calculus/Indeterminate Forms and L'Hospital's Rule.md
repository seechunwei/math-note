Notice that the L'Hospital's Rule need 2 condition
1) the limit is in indeterminate form
2) $\lim_{ x \to a } \frac{f'(x)}{g'(x)}$ exist or limit is $\infty$ or $-\infty$

### Find $\lim_{ x \to 0 } \frac{\sec ^{2}x-1}{3x^{2}}$.

$$
\begin{align}
\lim_{ x \to 0 }  \frac{\sec ^{2}x-1}{3x^{2}}&=\lim_{ x \to 0 }  \frac{\tan ^{2}x}{3x^{2}} \\

\end{align}
$$
Notice that $\lim_{ x \to 0 }\tan ^{2}x=0$ and $\lim_{ x \to 0 }3x^{2}=0$. Thus, By L Hospital's Rule

$$
\begin{align}
\lim_{ x \to 0 } \frac{\tan ^{2}x}{3x^{2}}&=\lim_{ x \to 0 } \frac{2\tan x\sec ^{2}x}{6x} \\
\end{align}
$$

Notice that $\lim_{ x \to 0 }2\tan x\sec ^{2}x=0$ and $\lim_{ x \to 0 }6x=0$. Thus, by L'Hospital's Rule again (It is too complicated, let's simplify first)

$$
\begin{align}
\lim_{ x \to 0 } \frac{2\tan x\sec ^{2}x}{6x}&= \frac{1}{3}\lim_{ x \to 0 }  \frac{\tan x}{x}\cdot \lim_{ x \to 0 } \sec ^{2}x &&(1)\\
&= \frac{1}{3} \lim_{ x \to 0 } \sec ^{2}x \cdot 1 \\
&= \frac{1}{3}(1) \\
&= \frac{1}{3}
\end{align}
$$
(1) In this step it is justified by the Product Law of Limit ![[1)a) The limit laws#^b6c735]] , but we don't know if $\lim_{ x \to 0 } \frac{\tan x}{x}$ exist or not, so we assume it is exist and we apply the law


Another approach using the fact that $\lim_{ x \to 0 } \frac{\sin x}{x}=1$:

$$
\begin{align}
\lim_{ x \to 0 } \frac{\tan ^{2}x}{3x^{2}}&= \frac{1}{3}\lim_{ x \to 0 } \left( \frac{\tan x}{x}   \right)^{2} \\
&=\frac{1}{3}\lim_{ x \to 0 } \left( \frac{\sin x}{\cos x\cdot x} \right)^{2} \\
&= \frac{1}{3}   \left( \lim_{ x \to 0 }  \frac{\sin x}{\cos x\cdot x}  \right) ^{2} &&(2)\\
&= \frac{1}{3}\left(  \lim_{ x \to 0 }  \frac{\sin x}{x} \cdot \lim_{ x \to 0 }  \frac{1}{\cos x} \right)^{2} \\
&=  \frac{1}{3} (1)^{2} \\
&= \frac{1}{3}
\end{align}
$$

(2) this is also the same, we assume $\lim_{ x \to 0 } \frac{\sin x}{\cos x\cdot x}$ exist.


### Find $\lim_{ x \to \frac{\pi}{4} }[(1-\tan x)\sec 2x]$

Notice that $\lim_{ x \to \frac{\pi}{4} }(1-\tan x)=1-1=0$. But $\lim_{ x \to \frac{\pi}{4} }\sec 2x$ does not exist because

$$
\begin{align}
\lim_{ x \to \frac{\pi}{4} } \sec 2x &= \lim_{ x \to \frac{\pi}{4} }  \frac{1}{\cos 2x} \\
&= \frac{1}{0} \text{(does not exist)}
\end{align}
$$
But $\lim_{ x \to \frac{\pi}{4}^{+} }\sec 2x=-\infty$ while $\lim_{ x \to \frac{\pi}{4}^{-} }\sec 2x=\infty$. The question is: Is it an indeterminate form?

What is actually indeterminate form?
It is something like we want to evaluate a limit of 2 factor where there exist a tension between the 2 factor. For example,

Factor A ($1-\tan x$) is pulling the product toward 0
Factor B ($\sec 2x$, whose magnitude $\lvert g(x) \rvert\to \infty$) 

Recall that the L'Hospital's Rule can be apply in any limit whether $x\to a^{+}$ or $x\to a^{-}$. Thus, the next question is do we need to split into 2 cases?

In this case, the answer is no because
- when $x\to \frac{\pi}{4}^{-}$, $1-\tan x>0$
- when $x\to \frac{\pi}{4}^{+}$, $1-\tan x<0$ 

They change sign simultaneously!!

From other perspective, we can see it as

$$
\lim_{ x \to \frac{\pi}{4} }  \frac{1-\tan x}{\cos 2x}
$$
Then it is just a $\left[\frac{0}{0}\right]$ type of indeterminate form.

Thus, by L'Hospital's Rule:

$$
\begin{align}
\lim_{ x \to \frac{\pi}{4} } \frac{1-\tan x}{\cos 2x} &= \lim_{ x \to \frac{\pi}{4} } \frac{-\sec^{2}x}{-2\sin 2x} \\
&= \frac{-\sec^{2}(\frac{\pi}{4})}{-2\sin(2 \cdot \frac{\pi}{4})} \\
&= \frac{-(\sqrt{2})^{2}}{-2\sin(\frac{\pi}{2})} \\
&= \frac{-2}{-2(1)} \\
&= 1
\end{align}
$$

Alternatively, by algebraic factorization (revealing the hidden shared zero-factor):

$$
\begin{align}
\frac{1 - \tan x}{\cos 2x} &= \frac{1 - \frac{\sin x}{\cos x}}{\cos^2 x - \sin^2 x} \\
&= \frac{\frac{\cos x - \sin x}{\cos x}}{(\cos x - \sin x)(\cos x + \sin x)} \\
&= \frac{1}{\cos x (\cos x + \sin x)} \quad \left(x \neq \frac{\pi}{4}\right)
\end{align}
$$

Evaluating the limit directly:

$$
\lim_{ x \to \frac{\pi}{4} } \frac{1}{\cos x (\cos x + \sin x)} = \frac{1}{\frac{1}{\sqrt{2}}\left(\frac{1}{\sqrt{2}} + \frac{1}{\sqrt{2}}\right)} = \frac{1}{\frac{1}{\sqrt{2}}(\sqrt{2})} = 1
$$

---

> [!important] The Boundary Rule: When Must We Split into One-Sided Limits?
> **Core Principle**: 
> The initial indeterminate form $\left[\frac{0}{0}\right]$ or $[0 \cdot \infty]$ is only an **entry ticket** allowing the use of algebraic tools or L'Hospital's Rule. It has **zero predictive power** over whether the limit requires a left/right split. 
> 
> Whether a split is required depends strictly on the **outcome**—the behavior of the simplified form or $\lim_{x \to c} \frac{f'(x)}{g'(x)}$:
> 
> 1. **No Split Needed (Two-Sided Limit Guaranteed)**:
>    - If $\lim_{x \to c} \frac{f'(x)}{g'(x)} = L$ exists as a finite real number (specifically $g'(c) \neq 0$ and $f', g'$ are continuous at $c$).
>    - Or algebraically, when the shared vanishing factor $(\cos x - \sin x)$ cancels out completely, leaving a denominator that does not vanish at the limit point.
> 
> 2. **Split IS Mandatory**:
>    - **Case A (Direction-Sensitive Functions)**: Expressions involving absolute values $\lvert \cdot \rvert$, piecewise definitions, or roots of squares ($\sqrt{u^2} = \lvert u \rvert$) whose definition branches at $x = c$.
>      *Example:* $\lim_{x \to 0} \frac{\sqrt{1 - \cos 2x}}{x} = \lim_{x \to 0} \frac{\sqrt{2}\lvert \sin x \rvert}{x}$ branches to $+\sqrt{2}$ (from right) and $-\sqrt{2}$ (from left).
>    - **Case B (Surviving Odd Power of Zero in Denominator)**: If after L'Hospital stops or after factoring, an uncancelled odd zero remains in the denominator ($g'(x) \to 0$ with a sign flip while $f'(x) \neq 0$).
>      *Example:* $\lim_{x \to 0} \frac{1 - \cos x}{x^3} \xrightarrow{\text{L'H}} \lim_{x \to 0} \frac{\sin x}{3x^2} \xrightarrow{\text{L'H}} \lim_{x \to 0} \frac{\cos x}{6x}$. Here $\frac{1}{6(0^+)} \to +\infty$ while $\frac{1}{6(0^-)} \to -\infty$, forcing a split (limit DNE).



## Find Indeterminate Form of Type $\infty-\infty$

### Find $\lim_{ x \to 0^{+} }\left( \frac{1}{x}- \frac{1}{\sin x} \right)$

$$
\begin{align}
\lim_{ x \to 0^{+} } \left( \frac{1}{x}- \frac{1}{\sin x} \right)&= \lim_{ x \to 0^{+} }  \left( \frac{\sin x-x}{x\sin x} \right) \\ 
\end{align}
$$

Notice that $\lim_{ x \to 0^{+} }(\sin x-x)=0$ and $\lim_{ x \to 0^{+} }x\sin x=0$. Thus

$$
\begin{align}
\lim_{ x \to 0^{+} }  \left( \frac{\sin x-x}{x\sin x} \right)&= \lim_{ x \to 0^{+} } \frac{\cos x-1}{x\cos x+\sin x} \\
&= \lim_{ z \to 0^{+} } \frac{-\sin x}{-x\sin x+\cos x+\cos x} \\
&=  \frac{0}{0+1+1} \\
&=0 
\end{align}
$$


## Power type

$0^{0},\infty^{0}$ or $1^{\infty}$.

> [!question]
> Why $1^{\infty}$ is an indeterminate type while $0^{\infty}$ is not?
> $0^{\infty}$ is basically $0\times 0 \times\dots=0$
> 
> while $1^{\infty}\neq \lim_{ n \to \infty } 1^{\infty}\neq 1$ because we can approach $1$ from left hand side or right hand side. The correct expression should be
> 
> $$
> \lim_{ t \to a } [f(t)]^{g(t)}
> $$
> where $f(t)\to 1$ and $g(t)\to \infty$.
> 
> If $0.99999^{\infty}\to 0$ , while $(1,0000001)^{\infty}\to \infty$. So there exist a tension between them.





