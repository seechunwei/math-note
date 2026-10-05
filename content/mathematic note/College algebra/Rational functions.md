Rational functions is a function which denominator and numerator are polynomial

The basic graph of reciprocal function $\frac{1}{x}$, $\frac{1}{x^{2}}$.

Notice that the domain of $\frac{1}{x}$ is $\mathbb{R} /\{ 0 \}$ , because the graph is undefined when $x=0$.

### The local behavior of $\frac{1}{x}$
![[Pasted image 20260312100150.png]]


> [!info] vertical asymptote
>  which is a vertical line that the graph approaches but never crosses. In this case, the graph is approaching the vertical line x=0 as the input becomes close to zero
>  
>  A vertical asymptote of a graph is a vertical line x=a where the graph tends toward positive or negative infinity as the inputs approach a. We write As x →a, f(x) →∞, or as x →a, f(x) →−∞.

### End behavior of $f(x)=\frac{1}{x}$

![[Pasted image 20260312101201.png]]


Based on this overall behavior and the graph, we can see that the function approaches 0 but never actually reaches 0; it seems to level off as the inputs become large. This behavior creates a horizontal asymptote

> [!info] horizontal asymptote 
> A horizontal asymptote of a graph is a horizontal line y=b where the graph approaches the line as the inputs increase or decrease without bound. We write As x →∞ or x →−∞, f(x) →b.

### Using Transformations to Graph a Rational Function

$$
y=\frac{1}{x-2}+3
$$
The vertical asymptotes is $x=2$ which move 2 unit to the right and the horizontal asymptotes is $y=3$ which move 3 unit to up

### Identifying Vertical Asymptotes of Rational Functions

We identify the vertical asymptotes by setting the factor in denominator that are not common to the factors in the numerator to 0. 

Thus, the first step we need to do is factor out the numerator and denominator.

What if numerator and denominator have common factors?

Thus, when the factor approach to zero, it will become $\frac{0}{0}$ which is undefined but at the same time when $x$ approach opposite direction from the undefined point, the graph follow the change by other factor. Thus, $f(x)$ is not longer approach to infinity.

In this case, it is called **Removable Discontinuities** 

Does the multiplicity of common factor affect the result? 

The answer is yes. Let's suppose the function below
$$
f(x)=\frac{x-3}{(x-3)^{2}}
$$
The $x\to 3$, $(x-3)^{2}$ approach to zero significantly faster than $(x-3)$, thus $x-3<(x-3)^{2}$ when $x\to 3$ and the difference will become bigger and bigger when $x\to 3$. Thus, it is something like $\frac{1}{x-3}$. Thus. the output value will approach to $+\infty$ or $-\infty$. 

In this case it will becomes a vertical asymptotes.

### Identifying Horizontal Asymptotes of Rational Functions


The horizontal asymptotes refer to the end behavior of the graph. A polynomial’s end behavior will mirror that of the leading term. Likewise, a rational function’s end behavior will mirror that of the ratio of the function that is the ratio of the leading term.

Case 1: If the degree of the denominator>degree of the numerator

Then, $f(x)=\frac{c}{x}$ where $C$ is a constant. Thus, when $x\to \pm \infty$ , $f(x)\to 0$. Thus, the horizontal asymptotes is $y=0$.

Case 2: If the degree of the denominator<degree of the numerator by one, we get a slant asymptote.

For example,
$$
f(x)=\frac{3x^{2}-2x+1}{x-1}
$$
Let's look at the ratio of leading term $\frac{3x^{2}}{x}=3x$. When $x\to \infty$, $f(x)\to \infty$, thus no horizontal asymptotes. But since $f(x)$ behave similarly with the line $3x$. It follow that it is a slant asymptotes.

To find the equation of the slant asymptote, divide $\frac{3x^{2}-2x+1}{x-1}$. The quotient is 3x+1, and the remainder is 2. Th slant asymptote is the graph of the line g(x)=3x+1.

Recall that the leading coefficient of a quadratic function determine how fast growing the output value. Thus, it is something similar with this.

![[Pasted image 20260312112602.png]]

Case 3: If the degree of the denominator=degree of the numerator

horizontal asymptote at ratio of leading coefficients.

Notice that a rational function can have many vertical asymptotes and never cross the line while can only have 1 horizontal asymptotes and may cross

> [!info] intercepts of rational functions
> A rational function will have a y-intercept when the input is zero, if the function is defined at zero. A rational function will not have a y-intercept if the function is not defined at zero. 
> 
> Likewise, a rational function will have x-intercepts at the inputs that cause the output to be zero. Since a fraction is only equal to zero when the numerator is zero, x-intercepts can only occur when the numerator of the rational function is equal to zero.
The factor of denominator determine the vertical asymptotes while the factor of numerator determine the x-intercept.

> [!important] Multiplicity of numerator factor
> Notice that the multiplicity of factor of numerator shape the local behavior of intercept as polynomial.


> [!important]
The multiplicity of factor of denominator shape the local behavior of vertical asymptotes which mirror one of the two toolkit reciprocal function.

When the multiplicity is odd
One side of vertical asymptotes will go until $+\infty$ while the other side will go $-\infty$.

![[Pasted image 20260313161545.png]]

When the multiplicity is even
Both side go to the same direction
![[Pasted image 20260313161528.png]]

Now we can use the knowledge above to draw a rational function and vice versa.



