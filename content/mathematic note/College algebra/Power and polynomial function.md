A power function is a function with a single term that is the product of a real number, a coefficient, and a variable raised to a fixed real number.

$$
f(x)=ax^{n}
$$
where $a,n$ is real number.

### Identifying end behavior of Power Functions

The end behavior of a power function can be determined when $x\to \infty$ and $x\to-\infty$.

For example for $f(x)=x^{3}$ We can describe the end behavior as

$x\to  \infty$, $f(x)\to \infty$

Thus, notice that the parity of function make difference on the end behavior.
1) even power
- The end behavior of $f$ is same as $x\to \pm \infty$
1) odd power
- The end behavior of $f$ is different either approach to $-\infty$ or $\infty$

Notice that the coefficient make different on the end behavior



### Identifying Polynomial Functions

A polynomial function consists of either zero or the sum of a finite number of non-zero terms, each of which is a product of a number, called the coefficient of the term, and a variable raised to a non-negative integer power.

$$
f(x)=a_{n}x^{n}+a_{n-1}x^{n-1}+\dots+a_{1}x+a_{0}
$$

The degree of the polynomial is the highest power of the variable that occurs in the polynomial

The leading term is the term containing the highest power of the variable

The leading coefficient is the coefficient of the leading term.

#### Identifying End Behavior of Polynomial Functions

Knowing the degree of a polynomial function is useful in helping us predict its end behavior

Because the power of the leading term is the highest, that term will grow significantly faster than the other terms as x gets very large or very small, so its behavior will dominate the graph.

The end behavior of polynomial function match the power function with same leading terms.

#### Identifying Local Behavior of Polynomial Functions

A turning point is a point at which the function values change from increasing to decreasing or decreasing to increasing.

The x-intercepts occur at the input values that correspond to an output value of zero. It is possible to have more than one x-intercept (one to many)

>Intercepts and turning points of polynomials 
>A polynomial of degree n will have, at most, n x-intercepts and n−1 turning points.


Why?
A $n$ degree polynomial will have at most $n$ factors , thus there is at most $n$ root when $y=0$.

$n-1$ turning point because when you plot the x-intercept in the cartesian plane, notice that polynomial graph is smooth and continuous, thus the only reasonable way to draw polynomial is there is a turning point between each x-intercept.


### Using Factoring to Find Zeros of Polynomial Functions 
root/ zero of f is the value of $x$ when $f(x)=0$ 

### The behavior of the x-intercept
The behavior means that the change of y value when $x$ approach to that x-intercept. It can be pass though the x-axis or bounce off. 

The behavior of x-intercept is depend on the ****
multiplicity. 
> [!note]
> The number of times a given factor appears in the factored form of the equation of a polynomial is called the multiplicity

> [!example]
>$$
f(x)=(x-1)(x-2)^{2}(x-4)^{3}
$$

The multiplicity of respective factor is 1,2,3
$(x-1)$ is called single zero
$(x-2)$ is called double zero
$(x-4)$ is called triple zero

Let $p$ represent the multiplicity of each factors


![[Screenshot 2026-03-04 115137.png]]

> [!question]
> 
Why the multiplicity of linear factor shape the local behavior of corresponding x-intercept because the change of y will also subject to other linear factor when x change?

> [!info] Answer
>
> It is because when $x$ change with the direction of certain linear factor approaching to zero, the factor change significantly small (because the graph is continuous).
>
> Let $(x-r)^m$ be the linear factor with a multiplicity of $m$ and let $Q(x)$ be the product of other linear factors. Thus,
>
> $$P(x)=(x-r)^m \cdot Q(x)$$
>
> Since $r$ is not a root for $Q(x)$, thus $Q(x) \neq 0$. When we evaluate the behavior of the graph right at the $x$-intercept, we are looking at what happens when $x$ is very close to $r$.
>
> Because polynomials are continuous, as $x \to r$, $Q(x)$ simply approaches the constant value $Q(r)$.
>
> Let's call that non-zero constant $C$. In the immediate neighborhood of $x = r$, the entire polynomial behaves almost identically to:
>
> $$P(x) \approx C(x - r)^m$$
>
> Thus, we can just ignore the $C$ constant since it doesn't affect the behavior of graph.


For higher even powers, such as 4, 6, and 8, the graph will still touch and bounce off of the horizontal axis but, for each increasing even power, the graph will appear flatter as it approaches and leaves the x-axis.
(as well as the higher old powers)



### The symmetry of polynomial graph

If the function is an even function, its graph is symmetrical about the y-axis, that is, f(−x)=f(x). If a function is an odd function, its graph is symmetrical about the origin, that is, f(−x)=−f(x).

Why?

### Writing Formulas for Polynomial Functions

> [!info] factored form of polynomials
> If a polynomial of lowest degree $p$ has x-intercept at $x_{1},x_{2},x_{3},\dots x_{n}$. Then, $f(x)=a(x-x_{1})^{p_{1}}(x-x_{2})^{p_{2}}\dots(x-x_{n})^{p_{n}}$ where the $a$ can be determined by value other than x-intercept

We also need to check the number of turning point. 

### Using Local Extrema to Solve Applications

Sometimes we need to find the local extrema to solve the problem because the domain have been restricted due to some reason (no negative). 

