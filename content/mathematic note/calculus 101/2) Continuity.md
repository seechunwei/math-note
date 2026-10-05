
> [!definition] Continuity
> A function $f$ is continuous at a number $a$ if
> $$
> \lim_{ x \to a } f(x)=f(a)
> $$
> 1) $f(a)$ is defined
> 2) $\lim_{ x \to a }f(x)$ exists
> 3) $\lim_{ x \to a } f(x)=f(a)$

Where are each of the following functions discontinuous?

a) **Removable Discontinuity**: $$f(x)=\frac{x^{2}-x-2}{x-2}$$

This function is discontinuous at $x=2$, because $f(2)$ is not defined. Instead $f$ is a rational function and rational function is continuous within the domain defined.

b) **Infinite Discontinuity**
$$
f(x)=\begin{cases}
\frac{1}{x^{2}}&\text{ if }x\neq 0 \\
1&\text{ if }x=0
\end{cases}
$$

$f$ is discontinuous at $x=0$, because $\lim_{ x \to 0 }f(x)$ does not exist.

c) **Removable Discontinuity**
$$
f(x)=\begin{cases}
\frac{x^{2}-x-2}{x-2}&\text{ if }x\neq 2 \\
1&\text{ if }x=2
\end{cases}
$$
$$
\begin{align}
\lim_{ x \to 2 } \frac{x^{2}-x-2}{x-2}&=\lim_{ x \to 2 } \frac{(x-2)(x+1)}{x-2} \\
&= \lim_{ x \to 2 } x+1 \\
&=3
\end{align}
$$

Since $\lim_{ x \to 2 }f(x)\neq f(2)$ , it follow that $f$ is not continuous at $x=2$.

> [!remark]
> Why the $\lim_{ x \to 2 }f(x)=\lim_{ x \to 2 } \frac{x^{2}-x-2}{x-2}$ ? Because when we say limit when $x\to{2}$, it means that $x\neq 2$.



> [!definition]
> A function $f$ is continuous from the right at a number $a$ if 
> $$
> \lim_{ x \to a^{+} } f(x)=f(a)
> $$
> 
> and $f$ is continuous from left at $a$ if
> $$
> \lim_{ x \to a^{-} } f(x)=f(a)
> $$

> [!definition] Definition
> A function $f$ is continuous on an interval $(a,b)$ if it is continuous at every point $c \in(a,b)$. For a closed interval $[a,b]$, we also require;
> 
> $$
> \lim_{ x \to a^{+} } f(x)=f(a) \text{ and }\lim_{ x \to b^{-} } f(x)=f(b) 
> $$

Example;
Prove that the function $f(x) = x^2$ is continuous on the closed interval $[1, 3]$.

To satisfy your definition, we need to break this down into three distinct logical steps:

1. Show it is continuous at an **arbitrary interior point** $c \in (1, 3)$.
2. Show the **right-hand limit** matches at the left endpoint: $\lim_{x \to 1^+} f(x) = f(1)$.
3. Show the **left-hand limit** matches at the right endpoint: $\lim_{x \to 3^-} f(x) = f(3)$.

#### 1. Continuity on the open interval (1, 3)

Let $c\in(1,3)$ be an arbitrary real number.
$$
\begin{align}
\lim_{ x \to c } f(x)&=\lim_{ x \to c } x^{2} \\
&=[\lim_{ x \to c } x]^{2} &&\text{(By power law)} \\
&=c^{2}=f(c) 
\end{align}
$$

Thus, $f$ is continuous at every point in the open interval $(1,3)$

#### 2. Right-continuity at x=1

$$
\begin{align}
\lim_{ x \to 1^{+} }f(x)&=\lim_{ x \to 1^{+} }x^{2}   \\
&=1^{2}=f(1)
\end{align}
$$
Thus, $f$ is continuous from the right at left endpoint.

#### 3. Left-continuity at x=3

$$
\begin{align}
\lim_{ x \to 3^{-} }f(x)&=\lim_{ x \to 3^{-} }x^{2}   \\
&=3^{2}=9=f(3)
\end{align}
$$
Thus, $f$ is continuous from the left at right endpoint.

Thus, by definition $f$ is continuous on the closed interval $[1,3]$

> [!remark]
> Notice that continuity always concern about the value at particular point, that's why we always use closed interval not opened interval


> [!theorem]
> If $f$ and $g$ are continuous at $a$ and $c$ is a constant, then the following functions are also continuous at $a$:
> 
> 1) $f+g$
> 2) $f-g$
> 3) $cf$
> 4) $fg$
> 5) $\frac{f}{g}$ if $g(a)\neq 0$

> [!theorem] 
> 
> a) Any polynomial is continuous at $(-\infty,\infty )$
> b) Any rational function is continuous where it is defined

(This follow from the direct substitution property)

### Continuity of trigonometry function at $\theta=0$

Notice that 
$$
\lim_{ \theta \to 0 } \cos \theta=1 \text{ and } \lim_{ \theta \to 0 } \sin \theta=0
$$

Since $\cos 0=1$ and $\sin 0=0$. It follow that both function are continuous at 0.

The addition formulas for cosine and sine can then be used to deduce that these functions are continuous everywhere.

Proof for continuity of $\sin x$:
To prove $\sin x$ is continuous at everywhere, we need to show that for any real number $c$,

$$
\lim_{ x \to c } \sin x=\sin c
$$
Instead of letting $x$ slide toward $c$, a clever algebraic trick is to define a new variable $h$ representing the distance between $x$ and $c$. Let $x = c + h$. As $x$ approaches $c$, the distance $h$ shrinks to $0$ ($h \to 0$).

Now we can rewrite the limit as:

$$\lim_{x \to c} \sin x = \lim_{h \to 0} \sin(c + h)$$
By addition formula,

$$
\begin{align}
\lim_{ h \to 0 } \sin(c+h)&=\lim_{ h \to 0 } (\sin c\cos h+\cos c\sin h) \\
&=(\sin c\cdot \lim_{ h \to 0 } \cos h)+(\cos c\cdot \lim_{ h \to o } \sin h) \\
&=\sin c(1)+\cos c(0) \\
&=\sin c &&\blacksquare
\end{align}
$$

Proof for continuity of $\cos x$:
We use the exact same strategy for cosine, deploying the cosine addition formula, $\cos(A + B) = \cos A \cos B - \sin A \sin B$:

$$\lim_{x \to c} \cos x = \lim_{h \to 0} \cos(c + h)$$

$$= \lim_{h \to 0} (\cos c \cos h - \sin c \sin h)$$

$$= \left(\cos c \cdot \lim_{h \to 0} \cos h\right) - \left(\sin c \cdot \lim_{h \to 0} \sin h\right)$$

Substitute the foundational limits again:

$$= (\cos c \cdot 1) - (\sin c \cdot 0)$$

$$\begin{align}
= \cos c &&\blacksquare
\end{align}$$ 

> [!remark]
> 1. The Global-to-Local Reduction Move
> - By using the substitution $x = c + h$, they shift the perspective.
>     
> - The parameter $c$ represents the infinite wilderness of the number line, but $h \to 0$ pulls the core action right back to the origin ($0$).
> 
> Once you prove the function behaves smoothly at $0$, the algebraic machinery safely transfers that smoothness to any arbitrary point $c$
> 
> 2. Exploiting "Translation Invariance" (Symmetry)
> Why does this trick work for sine and cosine, but fails for a chaotic, highly irregular function? Because sine and cosine possess deep geometric and algebraic symmetry.
> 
> To study this rigorously, we define a **Translation Operator**, often denoted as $T_c$. This operator takes a function and shifts its input by a constant distance $c$:
> 
> $$T_c f(x) = f(x + c) **Removable Discontinuity**$$
> An intrinsic property or an operator $A$ (like taking a derivative or measuring a length) is said to be **translation-invariant** if it commutes with this shift. That is, shifting the input first and then applying the property yields the exact same result as applying the property first and then shifting:
> 
> $$A(T_c f) = T_c (A f)$$
> 
> 
> The addition formula acts as the algebraic bridge, ensuring that the local smoothness at $0$ translates perfectly to the rest of the universe.
> 
> In abstract algebra and topology, this concept is generalized even further: spaces with this property are often framed as **topological groups**, where the act of "shifting" is replaced by a group operation.

It follow that from Theorem 4
$$
\tan x=\frac{\sin x}{\cos x}
$$
is continuous when $\cos x\neq 0$.

Thus the tangent function is not continuous when $x$ is odd integer multiple of $\frac{\pi}{2}$. Thus

$x=\pm \frac{\pi}{2},\pm \frac{3\pi}{2}, \frac{5\pi}{2},\dots$

> [!theorem] Theorem 7
> The following types of functions are continuous at every number in their domains:
> 
> - polynomials
> - rational functions
> - root functions
> - trigonometric function



> [!theorem] Theorem 8
> If $f$ is continuous at $b$ and $\lim_{ x \to a }g(x)=b$, then $\lim_{ x \to a }f(g(x))=f(b)$. In other words,
> 
> $$
> \lim_{ x \to a } f(g(x))=f(\lim_{ x \to a } g(x))
> $$
> 

Because $f(x)$ is continuous at $b$. Thus,

$$
\lim_{ x \to b } f(x)=f(b)
$$
- **The Goal:** Calculating the limit of a complex, nested expression.
- **The Requirement:** You need to know that the "outer" function  is continuous so that you can move the limit inside.



> [!theorem] Theorem 9
> 
> If $g$ is continuous at $a$ and $f$ is continuous at $g(a)$, then the composite function $f\circ g$ given by $(f\circ g)(x)=f(g(x))$ is continuous at $a$.

> [!remark]
> Theorem 9 (continuity of composite functions) is essentially the practical application of Theorem 8. Why?
> 
> A function $h$ is continuous at a point $a$ iff $\lim_{ x \to a }h(x)=h(a)$. 
> 
> If we set $h(x)=f(g(x))$, then for $h$ to be continuous at $a$, we must satisfy;
> 
> $$
> \lim_{ x \to a } f(g(x))=f(g(a))
> $$
> **Here is how they link:**
> 1) Start with the limit: We want to evaluate $\lim_{ x \to a }f(g(x))$ 
> 2) Use Theorem 8: Since $f$ is continuous, we "push" the limit inside: $f(\lim_{ x \to a }g(x))$
> 3) Use the continuity of $g$: Since $g$ is continuous, we know $\lim_{ x \to a }g(x)=g(a)$.
> 4) Substitute: We get $f(g(a))$
> 
> By the definition of continuity, this means the composite function $f\circ g$ is continuous at $a$.

> [!theorem] Theorem 10 The Intermediate Value Theorem
> 
> Suppose $f$ is continuous on the closed interval $[a,b]$ and let $N$ be any number between $f(a)$ and $f(b)$, where $f(a)\neq f(b)$. Then, there exists a number $c$ in $(a,b)$ such that $f(c) **Removable Discontinuity**=N$.

Why it is closed interval, 
1) the definition of continuous require it to be closed interval because it concern about the limit and the value at certain point 
2) imagine if it is only continuous at open interval, then the continuous function line can be in continuous at the end point 
### 1. The "Trivial Case" vs. the "Interesting Case"

If we allowed $N$ to be equal to $f(a)$ or $f(b)$, the theorem would become "trivially true."

- If $N = f(a)$, then we already know a value for $c$: it's just $a$.
- If $N = f(b)$, then $c$ is just $b$.