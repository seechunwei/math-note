Yes, you absolutely can! If you are an engineer working with a modern computer or calculator, you would almost certainly just compute the exact change, $\Delta V = V(r + \Delta r) - V(r)$, to get the most accurate answer possible.

Historically, differentials were invented because multiplying integers was vastly faster than raising five-digit decimals to the third power by hand. But since arithmetic is cheap now, why do mathematicians still care so much about differentials?

From a pure mathematics perspective, calculating the exact numerical change actually **hides the deep structural truth** of what is happening. Here is why we prefer the differential approach over just doing the subtraction.

### 1. It Reveals a Universal Law (Relative Error)

If you just calculate the exact change ($\Delta V = 277.75\text{ cm}^3$), that number only applies to _this specific sphere_ with a radius of $21\text{ cm}$ and an error of $0.05\text{ cm}$. It doesn't tell you anything about how error behaves in general.

Now, look what happens if we use our differential formula to look at **relative error** (the error divided by the total size):

$$\frac{\text{Volume Error}}{\text{Total Volume}} \approx \frac{dV}{V} = \frac{4\pi r^2 \, dr}{\frac{4}{3}\pi r^3}$$

If we simplify this fraction, the $\pi$ cancels out, and the $r^2$ cancels out most of the $r^3$:

$$\frac{dV}{V} = 3 \frac{dr}{r}$$

Look at how beautiful that is. This formula tells us a universal truth: **the percentage error in the volume of a sphere will always be exactly 3 times the percentage error in the radius.** * If your radius measurement is off by $1\%$, your volume will be off by approximately $3\%$.

- This is true whether you are measuring a tiny marble, a basketball, or the planet Earth.
    

If you only calculate the exact change using hard numbers, this elegant, universal scaling law remains completely invisible to you.

### 2. It Allows Us to Do Algebra with "Change"

In advanced mathematics, physics, and economics, we rarely know the exact numbers ahead of time. We often have to analyze systems where everything is changing simultaneously.

Because differentials rewrite a messy algebraic expansion (like $(r + \Delta r)^3 - r^3$) into a clean, linear product ($4\pi r^2 dr$), they allow us to manipulate rates of change using standard algebra. This is the exact bridge that allows us to set up and solve **differential equations**—which are the foundation for predicting everything from fluid dynamics to quantum mechanics.

### Summary

Calculating the exact change gives you a highly accurate **destination** (a single number), but using differentials gives you the **map** (the underlying geometric relationship).

Would you like to see how this same relative error trick ($3 \frac{dr}{r}$) works for other shapes, like the area of a square or the volume of a cube?


---

Spot on again. You can absolutely calculate the exact percentage change by taking your actual change $\Delta V$ and dividing it by the original volume $V$.

If you do that with the exact numbers from our sphere problem, you get:

$$\text{Exact Radius % Change} = \frac{0.05}{21} \times 100\% \approx \mathbf{0.2381\%} 
$$

$$\text{Exact Volume % Change} = \frac{277.75}{38792.39} \times 100\% \approx \mathbf{0.7160\%}
$$

If you divide those two exact percentages ($\frac{0.7160}{0.2381}$), you get **$3.0071$**. It is remarkably close to $3$, but it isn't _exactly_ $3$.

Why is that? Let’s look at the exact algebra under the hood to see the beautiful connection between the exact percentage change and the differential shortcut.

### The Exact Algebra of Percentage Change

Let's calculate the exact relative change ($\frac{\Delta V}{V}$) using purely generic variables, without plugging in any numbers yet.

The exact change in volume is:

$$\Delta V = \frac{4}{3}\pi(r + \Delta r)^3 - \frac{4}{3}\pi r^3$$

If we expand that cubic term $(r + \Delta r)^3$ using the binomial theorem, we get:

$$\Delta V = \frac{4}{3}\pi \left( r^3 + 3r^2\Delta r + 3r(\Delta r)^2 + (\Delta r)^3 \right) - \frac{4}{3}\pi r^3$$

Notice that the $\frac{4}{3}\pi r^3$ terms cancel each other out perfectly, leaving us with:

$$\Delta V = \frac{4}{3}\pi \left( 3r^2\Delta r + 3r(\Delta r)^2 + (\Delta r)^3 \right)$$

Now, let's find the **exact relative change** by dividing this $\Delta V$ by the original volume $V = \frac{4}{3}\pi r^3$:

$$\frac{\Delta V}{V} = \frac{\frac{4}{3}\pi \left( 3r^2\Delta r + 3r(\Delta r)^2 + (\Delta r)^3 \right)}{\frac{4}{3}\pi r^3}$$

The $\frac{4}{3}\pi$ constants cancel out completely. If we divide each term in the parentheses by $r^3$, look at what drops out:

$$\frac{\Delta V}{V} = 3\left(\frac{\Delta r}{r}\right) + 3\left(\frac{\Delta r}{r}\right)^2 + \left(\frac{\Delta r}{r}\right)^3$$

### The "Aha!" Moment

Look closely at that final formula. The exact percentage change actually _does_ contain our clean, universal law of $3\left(\frac{\Delta r}{r}\right)$ right at the front!

But it also contains two extra, messy "higher-order" terms: $3\left(\frac{\Delta r}{r}\right)^2$ and $\left(\frac{\Delta r}{r}\right)^3$.

This is where the magic of differentials comes in:

- The relative error we got using **differentials** ($\frac{dV}{V} = 3\frac{dr}{r}$) is just the **linear part** of this exact equation.
    
- Differentials work by intentionally ignoring those squared and cubed terms.
    

### Why are we legally allowed to ignore them?

Because our radius error is very small relative to the radius ($\frac{\Delta r}{r} \approx 0.00238$).

- When you square a tiny decimal like $0.00238$, it becomes an incredibly microscopic number: $0.00000566$.
    
- When you cube it, it virtually vanishes from reality: $0.0000000135$.
    

Those higher-order terms are so small that they add almost nothing to the final result. They are the mathematical equivalent of worrying about a single grain of sand on a beach.

### Summary

You are completely right that the exact calculation gives you the percentage change. But using differentials allows you to strip away those microscopic, higher-order complications ($(\Delta r)^2$ and $(\Delta r)^3$) right from the very start. It hands you the clean, dominant linear relationship ($3\frac{dr}{r}$) without forcing you to do any heavy polynomial expansion.