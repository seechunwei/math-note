
What we do here is we try to define the arbitrarily close into rigorous statement.

> [!definition]
> Precise Definition of a Limit
> Let $f$ be a function defined on some open interval that contains the number $a$, except possibly at $a$ itself. Then we say that the limit of $f(x)$ as $x$ approaches $a$ is $L$, and we write
> 
> $$
> \lim_{ x \to a } f(x)=L
> $$
> iff for every number $\epsilon>0$, there exist a number $\delta>0$ such that
> 
> $$
> 0<|x-a|<\delta\implies|f(x)-L|<\epsilon
> $$

> [!question]
> Why we need to set $0<|x-a|$ because $x-a\neq 0\implies x\neq a$. (We don't care the exact value of $f(x)$)
>
>Another reason is the "Removable Discontinuity", if we allowed $x=a$ , then we might get the jump value

> [!remark]
> The definition of limit says that if any small interval $(L-\epsilon,L+\epsilon)$ is given around $L$, then we can find an interval $(a-\delta,a+\delta)$ around $a$ such that $f$ maps all the points in $(a-\delta,a+\delta)$ (except possibly $a$) into the interval $(L-\epsilon,L+\epsilon)$.
> 

![[Pasted image 20260707221737.png]]

Consider the function below
$$
f(x)=\begin{cases}
2x-1 & \text{ if }x\neq 3 \\
6 & \text{ if }x={3}
\end{cases}
$$

$$
\lim_{ x \to 3 } f(x)=5
$$


We use distance to represent the difference or the change $|x-3|$ and $|f(x)-5|$.

> [!remark]
> We want to prove that 
> if for every $\epsilon > 0$, there exists a $\delta > 0$ such that:
> 
> if $0<|x-a|<\delta$ , then $|f(x)-L|<\epsilon$
> 
> 
> it is like a onto function, for every $y \in Y$, there exists $x \in X$ such that $f(x)=y$. 
> 
> Why we cannot just prove that if $a=b$ then $f(a)=f(b)$, (because it is not onto). The formal definition of limit is something like this, need to prove for every $\epsilon$.... 


In this case $a=3$ and $L=5$.

We want to find a $\delta$ such that $|(2x - 1) - 5| < \epsilon$ whenever $|x - 3| < \delta$.


$$
\begin{align}
|2x-1-5|&<\epsilon \\
|2x-6|&<\epsilon \\
2|x-3|&<\epsilon \\
|x-3|&< \frac{\epsilon}{2}
\end{align}
$$


> [!remark]
> We find $\delta$ in term of $\epsilon$. So that we can prove the statement if... then... with $\delta$ in term of $\epsilon$. $\delta$ is depend on $\epsilon$ and we prove the relationship between them. 


Now we can prove
Proof:
Let $\epsilon> 0$. Choose $\delta= \frac{\epsilon}{2}$. Assume $0<|x-3|<\delta$. We need to show that $|f(x)-5|<\epsilon$

Since $0<|x-3|$, we know that $x\neq 3$, so $f(x)=2x-1$. Then,

$$
\begin{align}
|f(x)-5|&=|(2x-1)-5| \\
&=|2x-6| \\
&=2|x-3| \\
&< 2\left( \frac{\epsilon}{2} \right) \\
&<\epsilon
\end{align}
$$
Thus, we have shown that for any $\epsilon > 0$, there exists a $\delta = \epsilon/2$ such that if $0 < |x - 3| < \delta$, then $|f(x) - 5| < \epsilon$. Therefore, by the formal definition of a limit, **$\lim_{x \to 3} f(x) = 5$**.


> [!remark] The "Floor" Problem (Jump Discontinuities)
> 
> Imagine a function with a jump at $x = 3$:
> 
> $$f(x) = \begin{cases} 0 & \text{if } x < 3 \\ 10 & \text{if } x \geq 3 \end{cases}$$
> 
> Does the limit exist as $x \to 3$? Intuitively, no. But let's look at what happens if we start with $\delta$:
> 
> - If you pick **$\delta = 1$**, the values of $f(x)$ in the interval $(2, 4)$ are either $0$ or $10$.
>     
> - You could say, "Okay, then these values stay within an distance $\epsilon = 10$ of the point $L=5$."
>     
> - Even if you shrink $\delta$ to $0.00001$, the values of $f(x)$ are **still** $0$ and $10$. You are still stuck with an $\epsilon$ of at least $5$ to cover that gap.
>     
> 
> **The Failure:** The limit definition requires that we can make $\epsilon$ **arbitrarily small** (approaching zero). In this jump example, you can provide a $\delta$ for a large $\epsilon$ (like $\epsilon = 10$), but the moment I challenge you with a small $\epsilon$ (like $\epsilon = 0.1$), you can no longer find a $\delta$ that works.
> 

---

Prove $\lim_{ x \to 3 }x^{2}=9$ exists using epsilon delta definition.

Preliminary

$$
\begin{align}
|x^{2}-9-0|&<\epsilon \\
|x-3||x+3|&<\epsilon
\end{align}
$$
(We need to establish the relationship between $|x-3|$ and $|x+3|$ given $|x-3|$ less than a small number ) This number is like a supposition, if $|x-3|<a$
, then $|x+3|<b$. We need to set a and find b.

Let $a=1$. Thus,
$$
\begin{align}
|x-3|&<1 \\
2<x&<4 \\
5<x+&3<7
\end{align}
$$

So if $|x+3|<1$, then $|x+3|<7$. Thus,

$$
\begin{align}
7|x-3|&<\epsilon \\
|x-3|&< \frac{\epsilon}{7}
\end{align}
$$
If we satisfy $|x - 3| < \frac{\epsilon}{7}$, and we also stay within our safety window ($|x - 3| < 1$), then the product $|x - 3||x + 3|$ is guaranteed to be less than $\epsilon$.

By picking the **minimum**, you ensure that **both** condition are satisfied.

Thus, we choose 
$$
\delta= \text{min}\left( 1, \frac{\epsilon}{7} \right)
$$

> [!question]
> Why we choose $|x+3|<7$ ?
> - For $|x-a|<\delta$(finite limits): We want to 'trap' the function. We replace variable part with upper bounds to ensure the result stay below $\epsilon$. 
> - For $x>M$, we want to "push" the function. We replace variable part with lower bounds to ensure the result stay below $\epsilon$ when $x$ grows towards infinity


> [!question]
>  What happens if we DON'T use "min"?
> 
> Let's see the logic break. Imagine we just said $\delta = \frac{\epsilon}{7}$ and ignored the $\delta \leq 1$ part.
> 
> Suppose the "Skeptic" gives you a huge $\epsilon$, like $\epsilon = 70$.
> 
> - If you use $\delta = \frac{\epsilon}{7}$, then $\delta = 10$.
>     
> - Your interval for $x$ is now $0 < |x - 3| < 10$.
>     
> - This means $x$ could be $12$.
>     
> - If $x = 12$, then $|x + 3| = |12 + 3| = \mathbf{15}$.
>     
> 
> **The Crash:** In your proof, you claimed that $|x^2 - 9| = |x-3||x+3| < \delta \cdot 7$.
> 
> But if $x=12$, then $|x^2 - 9| = 9 \cdot 15 = 135$.
> 
> Your "trap" ($7$) failed because $x$ was allowed to wander too far away from the center. The inequality $135 < 10 \cdot 7$ is **false**.


Proof:
Suppose $\epsilon> 0$ and $0<|x-3|<\delta$ where $\delta=\text{min}\left( 1, \frac{\epsilon}{7} \right)$. We need to show that $|x^{2}-9|<\epsilon$.

Since $\delta\leq 1$, it follow that 
$$
\begin{align}
|x-3|&<1 \\
2<x&<4 \\
5<x+&3<7
\end{align}
$$

Thus, $|x+3|<7$, 

Since $\delta\leq \frac{\epsilon}{7}$, we know that $|x-3|< \frac{\epsilon}{7}$.

Therefore, by substitution
$$
\begin{align}
|x^{2}-9|&=|x+3||x-3| \\
&<7\left( \frac{\epsilon}{7} \right) \\
&<\epsilon
\end{align}
$$

Therefore, $\lim_{x \to 3} x^2 = 9$. $\blacksquare$


---

> [!question] Understanding Check
> 
> **Q1: If you found a $\delta$ that satisfies a strict $\epsilon = 0.1$, do you need to find a new $\delta$ for a larger $\epsilon = 100$?**
> - **Answer:** No. Since the $\delta$ already guarantees the function stays within $0.1$ of the limit, and $0.1 < 100$, that same $\delta$ automatically satisfies the requirement for $\epsilon = 100$.
> 
> **Q2: Prove $\lim_{x \to 4} x^2 = 16$. If you restrict your "safety window" to $|x - 4| < 1$, what is the maximum value that $|x + 4|$ can take?**
> - **Answer:** If $|x - 4| < 1$, then $3 < x < 5$. Adding 4 to the inequality gives $7 < x + 4 < 9$. Therefore, the maximum value $|x + 4|$ can take is $9$.
> 
> **Q3: Consider $f(x) = x^2$ for $x \neq 5$ and $f(5) = 100$. Does $\lim_{x \to 5} f(x) = 25$?**
> - **Answer:** Yes. Because the definition of a limit uses $0 < |x - a|$, we explicitly exclude the point $x = a$. Therefore, the value of $f(x)$ at $x = 5$ is ignored, and the limit correctly describes the behavior as $x$ approaches $5$.
