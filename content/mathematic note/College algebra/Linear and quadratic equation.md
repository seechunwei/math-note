Slope of line

The gradient is the ratio of vertical change over the horizontal change. To find the perpendicular line, we need to rotate it 90 degree, imagine $m=3$ which mean when we move 1 unit right to right , the point move up 3 unit , Thus it form a triangle which the hypothenars  length is the distance from point $A$ to $B$. Imagine this triangle rotate 90 degree, thus it become x move 3 unit, move down 1 unit which mean the $m= -\dfrac{1}{3}{}$. which is the negative reciprocal  of original gradient.


Modelling
We derive a formula to explain the relationship between two quantity. One can express in term of another. Thus, if 1 question have 3 variable and we are given 2 value 1 equation or 3 equation (system of equation) to solve for certain quantity.

Imaginary unit and radical
$$\sqrt{x^2} = |x|$$
$$(\sqrt{ x })^{2}=x$$
This is true because $\sqrt{ x^{2} }$ is principal root of $x^{2}$ which is have same sign with $x^{2}$. Since $x^{2}>0$ Thus, the root always $>0$. 

We can only say $\sqrt{ x^{2} }=x^{\frac{1}{2}(2)}$ if $x>0$. If $x$ is negative $(\sqrt{ -1 })^{2}=-1$ , $\sqrt{ (-1)^{2} }=\sqrt{ 1 }=1$. Thus, we can conclude that if $x$ is negative , the order of taking square and square root is important.  

Notice that $f:\mathbb{R}\to \mathbb{R}$ is defined as $f(x)=x^{2}$ is not a group. 
1) It is because it is many-to-one function
$f(1)=f(-1)$ but $1\neq-1$. Thus, we don't have the reverse property for exponent it violate the Cancellation law. 

We treat $i$ as a constant and we just add and subtract the like term and multiply distribute over addition. 
$i^{2}=-1$.
But when we talk about dividing imaginary number , we need to eliminate the imaginary portion of the denominator. Thus, we need to multiply it with complex conjugate  $(a+bi)(a-bi)$

How to solve a quadratic equation. We write it in standard form $ax^{2}+bx+c=0$ and we factorize the expression and using zero product property to solve. 
Each term is a linear term.

If the quadratic equation is a perfect square trinomial $(x+a)^{2}$ , then $x^{2}+2ax+a^{2}$ For, example, $x^{2}+4x+4=(x+2)^{2}$ In general,
$$
x^{2}+\frac{b}{a}x+\frac{c}{a}=\left( x+\frac{b}{2a} \right)
$$
iff $\frac{c}{a}=\left( \frac{b}{2a} \right)^{2}$  which mean $\frac{c}{a}=\frac{b^{2}}{4a^{2}}$


#### Vieta formula and AC formula

What if it is not a perfect square. That means there exist 2 distinct real root.
Suppose $\alpha$ and $\beta$ are solution for $x^{2}+\frac{b}{a}x+\frac{c}{a}=0$
Thus,$(x-\alpha)(x-\beta)=0$ 
$$
\begin{align}
x^{2}-\alpha x-\beta x+\alpha \beta&=0 \\
x^{2}-(\alpha+\beta)x+\alpha \beta&=0
\end{align}
$$
It is clear that 
$$
\begin{align}
\frac{b}{a}=-(\alpha+\beta) \\
(\alpha+\beta)=-\frac{b}{a}
\end{align}
$$
and 
$$
\alpha \beta=\frac{c}{a}
$$
**Vieta's Formulas** (Relationships between roots and coefficients).
Notice that, we cannot solve the system equation to find the root because it will become a circle loop. For example,
$x^{2}+4x+4=0$
1. Start with sum: $\alpha + \beta = -4$
2. Isolate $\beta$: $\beta = -4 - \alpha$
3. Substitute into product equation:
$$\alpha(-4 - \alpha) = 4$$
4. Expand:
$$-4\alpha - \alpha^2 = 4$$
5. Rearrange:
$$\alpha^2 + 4\alpha + 4 = 0$$

Result: You are staring at the exact same equation you started with!

This proves that the system is equivalent to the equation, but solving the system algebraically doesn't magically give you the answer unless you guess the factors or use the quadratic formula. 
Thus, we can only solve by guessing the number. On the other hand we can also form a quadratic equation with its solution. 

But this Vieta's formula can derive a method call AC method 

Let's take a standard quadratic equation where $a \neq 1$:

$$ax^2 + bx + c = 0$$

Step 1: Vieta's Problem

Vieta's formulas work best when $a=1$.

$$\text{Sum} = -\frac{b}{a}, \quad \text{Product} = \frac{c}{a}$$

The fractions $b/a$ and $c/a$ are annoying to work with mentally. We want to work with integers.

Step 2: The "AC" Trick (Multiply by $a$)

Let's multiply the entire equation by $a$.

$$a(ax^2 + bx + c) = a(0)$$

$$a^2x^2 + abx + ac = 0$$

Step 3: The Substitution

Notice that $a^2x^2$ is just $(ax)^2$. Let's invent a new variable $y = ax$.

Substitute $y$ into the equation:

$$y^2 + by + ac = 0$$

Step 4: Apply Vieta to the NEW equation

Now look at this new equation in terms of $y$. The leading coefficient is 1!

We can apply Vieta's logic cleanly here:

- **Sum of roots ($y_1 + y_2$):** $-b$
    
- **Product of roots ($y_1 \cdot y_2$):** $ac$

Since we know $y = ax$, we substitute back:

$$(ax + P)(ax + Q) = 0$$

If we find the sum of roots = b, then
$$(ax - P)(ax - Q) = 0$$
Thus, we should use this version and convert it in this form so that we can use this method when $a$ is not 1.

This gives you the factors involving $a$. Usually, you can simplify one or both brackets by dividing out a common factor (because we multiplied by $a$ at the start, we introduced an extra factor of $a$ that needs to be removed).


#### Cross Method
Besides AC method we have Cross-Multiplication method which derive from the visualization of FOIL method when we multiply 2 linear term. 

Here is exactly how the Cross Method maps to FOIL.

 The Anatomy of FOIL

Let's look at the general multiplication of two linear factors:

$$(ax + b)(cx + d)$$

If we expand this using **FOIL**, we get:

1. **F**irst: $(ax)(cx) = \mathbf{ac}x^2$
    
2. **O**uter: $(ax)(d) = \mathbf{ad}x$
    
3. **I**nner: $(b)(cx) = \mathbf{bc}x$
    
4. **L**ast: $(b)(d) = \mathbf{bd}$
    

The final quadratic is:

$$(\mathbf{ac})x^2 + (\mathbf{ad} + \mathbf{bc})x + (\mathbf{bd})$$

Now look at the Cross Method diagram for the exact same problem.

$$\begin{array}{c|c} \mathbf{ax} & \mathbf{b} \\ \mathbf{cx} & \mathbf{d} \end{array}$$

1. Left Column: You are finding factors of the first term.
$$ax \cdot cx = \mathbf{ac}x^2 \quad (\text{Matches \textbf{F}irst}) $$
    
2. Right Column: You are finding factors of the last term.
    $$b \cdot d = \mathbf{bd} \quad (\text{Matches \textbf{L}ast}) $$

3. **The Cross (The "X"):**
    
    - $ax \cdot d = \mathbf{ad}x$ (Matches **O**uter)
    - $cx \cdot b = \mathbf{bc}x$ (Matches **I**nner)
    
4. The Sum: You add the cross results to check the middle term.
$$\mathbf{ad}x + \mathbf{bc}x \quad (\text{Matches the Middle Term}) $$



if there is no linear term in equation, we use square root property, if $x^{2}=k$, then $x=\pm \sqrt{ k }$.

$(ax+b)(cx+d)=acx^{2}+dax+bcx+bd$

Thus, we find $ac$ which is the product of leading coefficient and $bd$ the product of last term where $da+bc=$ coefficient of $x$. The two intersection line in the working step is because term will only multiply term in another parenthesis.

completing the square $\to$ quadratic formula


The discriminant?
![[Pasted image 20260110233634.png]]

$x^{\frac{n}{m}}=c$ When $n$ is even integer $x$ have two possible value 

$x^{\frac{4}{5}}$

$x^{\frac{n}{m}}$ we take the square root first then only square thus, x can be negative or positive.
Thus,
$$
\begin{align}
x^{\frac{n}{m}}=c \\
x^{n}=c^{m} \\
x=c^{\frac{m}{n}}
\end{align}
$$
#### Solving equations Using Factoring

What is polynomial equation is a sum of term where each term is a product of number and variable up to power $n$ for some non-negative integer
$$
a_{n}x^{n}+a_{n-1}x^{n-1}+\dots+a_{1}x+a
$$
1) GCF
2) Grouping

Solving Radical equations
When solving radical equation notice that there may exists extraneous solution which is root that are not solution. This happen because when we square and factorize again it will give us 2 answer( many to one)
It is like $f^{-1}\circ f[A]\neq f\circ f^{-1}[A]$

Thus we need to check each answer.

Solving a Radical Equation Containing Two Radicals. As this equation contains two radicals, we isolate one radical, eliminate it, and then isolate the second radical.

For example
$$
\sqrt{ 2x+3 }=\sqrt{ x-2 }=4
$$Solving an Absolute value equation

If c < 0, |ax+b|=c has no solution.
If c=0, |ax+b|=c has one solution.
If c > 0, |ax+b|=c has two solutions

Solving Equations in Quadratic Form
$x^{4}-5x^{2}+4=0$
$x^{\frac{2}{3}}+4x^{\frac{1}{3}}+2$

Equations in quadratic form are equations with three terms. The first term has a power other than 2. The middle term has an exponent that is one-half the exponent of the leading term. The third term is a constant.

Solving Rational Equations Resulting in a Quadratic