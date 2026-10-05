$$
\frac{d}{dx} \sin x=\cos x
$$

$$
\begin{align}
\lim_{ h \to 0 } \frac{\sin(x+h)-\sin x}{h}&=\lim_{ h \to 0 } \frac{\sin x\cos h+\cos x\sin h-\sin x}{h} \\
&= \lim_{ h \to 0 } \left[ \sin x \frac{\cos h-1}{h}+\cos x \left[ \frac{\sin h}{h} \right]\right] \\
&=\sin x+\cos x(0) \\
&=\sin x
\end{align}
$$


#### Why does $\frac{\sin h}{h} \to 1$?

When the angle $h$ (in radians) gets incredibly close to $0$, the length of the arc ($h$) and the vertical height of the triangle ($\sin h$) on a unit circle become nearly identical. Because they approach $0$ at the exact same rate, their ratio becomes $1$.

#### Why does $\frac{\cos h - 1}{h} \to 0$?

We can actually prove this one algebraically using the first limit! If we multiply the top and bottom by $(\cos h + 1)$, we get:

$$\lim_{h \to 0} \frac{\cos h - 1}{h} \cdot \frac{\cos h + 1}{\cos h + 1} = \lim_{h \to 0} \frac{\cos^2 h - 1}{h(\cos h + 1)}$$

Using the identity $\cos^2 h - 1 = -\sin^2 h$:

$$= \lim_{h \to 0} \frac{-\sin^2 h}{h(\cos h + 1)}$$

Now, split it up so you can use the first limit:

$$= \lim_{h \to 0} \left( -\frac{\sin h}{h} \cdot \frac{\sin h}{\cos h + 1} \right)$$

Take the limit of both parts as $h \to 0$:

$$= -(1) \cdot \frac{0}{1 + 1} = 0$$
[[Squeeze Theorem]]