
In this chapter Spivak point out that graph as a visualization tool can help us to justify or understand something intuitively, but it cannot be a formal proof since it is not that rigorous.

And also in this chapter Spivak show a lot of not 'nice' function that have hole, oscillating, corner and so on which motivates some of the important concept in calculus.

Besides that, Spivak try to link the algebraic expression $f(x)=cx$ to a geometric graph with justification. (Similar triangle)

### Real line

We usually use a line to represent the set of real number $\mathbb{R}$. And we determine the inequality by determine the relative position of number. For example, $a<b$ iff $a$ lies to the left of $b$.

It is clear that any rational number like $\frac{1}{2}$ can be fit somewhere in the line. For irrational number we just take it for granted. (But actually we can approximate it using rational number by linear approximation in calculus)

The number $|a-b|$ has a simple interpretation in terms of this geometric picture: it is the distance between $a$ and $b$, 

The geometric interpretation of $|x-a|<\epsilon$. Open interval and closed interval notation.


## Link function with its graph (Linear function)

Along side the use of point on real number line to represent a number, our greater interest is to draw a pair of numbers and this require a "coordinate system".

Suppose there are 2 axes that intercept at right angle that form 4 quadrant, a number $(a,b)$ is plot $a$ unit right along the x-axis (horizontal axis) while $b$ unit up along the y-axis (vertical axis). The x-axis represent the set $\{ (a,b):b=0 \}$ while the y-axis represent the set $\{ (a,b):a=0 \}$. Thus, the intersection of this 2 set is $(0,0)$ which is called origin. The number $a$ and $b$ are called first and second coordinate respectively.

Draw a function simply means draw all the point (ordered pair) in the function. Now let's consider the simple function $f(x)=cx$. It's graph is a straight line though origin. How to prove?

Proof:
Let $x$ be some number not equal to 0 and let $L$ represent the straight line pass though the origin and though $A$, corresponding to the point $(x,cx)$. Suppose a point $A'$ with first coordinate $y$ will lie on $L$, Notice that the triangle $A'B'O$ is similar to triangle $ABO$ (Why? Because they bounded by 2 same line). Thus, 

$$
\frac{A'B'}{OB'}=\frac{AB}{OB}=c
$$
thus, the corresponding point of $A'$ is $(y,cy)$ which is in the function. $\blacksquare$
(Note that this is not the formal proof, the rigorous proof require the real proof that points on a straight line correspond exact way to the real numbers).

(The general version can be prove in this way also)

Thus, a straight line pass though origin is just a set $\{ (x,cx):x\in \mathbb{R} \}$.

To proceed we need another definition **distance** between $(a,b)$ and $(c,d)$ is

$$
\sqrt{ (a-c)^{2}+(b-d)^{2} }
$$

(Justified by Pythagorean theorem)


It is not hard to see that the function $f(x)=cx+d$ is a straight line with slop $c$, passing though the point $(0,d)$ and it is called **linear function**.

What if we want to find a straight line pass though 2 different points $(a,b)$ and $(c,d)$?

Let $f(x)=\alpha x+\beta$. Thus, 
$$
\begin{align}
\alpha a+\beta&=b \\
\alpha c+\beta&=d
\end{align}
$$
Solving this, we get $\alpha= \frac{d-b}{c-a}$ and $\beta= b-a\left( \frac{d-b}{c-a} \right)$, so

$$
f(x)= \frac{d-b}{c-a}x+b- \frac{d-b}{c-a}a
$$
which is call the intercept form but it is too messy let's try simplify it.

$$
\begin{align}
f(x)&= \frac{d-b}{c-a}(x-a)+b \\
f(x)-b&= \frac{d-b}{c-a}(x-a)
\end{align}
$$

which is know as point-slop form. 

Any straight line represent a graph of function? No for vertical line because by definition if $(a,b)$ and $(a,c)$ is in the function, then $b=c$. But it is not the case for vertical line. Thus, we can use vertical line test to test if a graph is a function or not.

## Parabola, Power function and Polynomial

$f(x)=x^{2}$. We plot some point and connect it, then we will get a parabola. 
![[Pasted image 20261004223909.png]]

But how do we know it won't be like this in the middle? 

The first one is impossible because $0\leq x<y\implies x^{2}<y^{2}$. The second one we plot as many point as we want in between to show that it won't have a jump. But in order to prove this we some fundamental concept of calculus to define the "jump".

The function $f(x)=x^{n}$ for $n\in \mathbb{N}$ is called power function. It is special case of polynomial function.

Polynomial function have at most $n-1$ extremum. 

## Rational function

## Interesting graph

The function $f$ define as
$$
f=\begin{cases}
f\left( \frac{1}{n} \right)=(-1)^{n+1} \\
f\left( -\frac{1}{n} \right)=(-1)^{n+1} \\
f(x)=1&|x|\geq 1
\end{cases}
$$


![[Pasted image 20261004224636.png]]


|  $n$  |  $x = \frac{1}{n}$  |    $y = (-1)^{n+1}$    | Point on Graph $(x, y)$ | What happens? |
| :---: | :-----------------: | :--------------------: | :---------------------: | :------------ |
| **1** |         $1$         | $(-1)^2 = \mathbf{+1}$ |        $(1, 1)$         | Peak          |
| **2** |     $1/2 = 0.5$     | $(-1)^3 = \mathbf{-1}$ |       $(1/2, -1)$       | Valley        |
| **3** | $1/3 \approx 0.333$ | $(-1)^4 = \mathbf{+1}$ |       $(1/3, 1)$        | Peak          |
| **4** |    $1/4 = 0.25$     | $(-1)^5 = \mathbf{-1}$ |       $(1/4, -1)$       | Valley        |
| **5** |     $1/5 = 0.2$     | $(-1)^6 = \mathbf{+1}$ |       $(1/5, 1)$        | Peak          |
| **6** | $1/6 \approx 0.167$ | $(-1)^7 = \mathbf{-1}$ |       $(1/6, -1)$       | Valley        |

Notice that the number $x=0$ is excluded from the domain. Since it oscillates between $-1$ and $1$, there is no single point you could assign to $f(0)$ to make it connect smooth to the zigzag.

there are a lot of function like $f(x)= \sin \frac{1}{x}$ and $f(x)=x \sin x$.

## Circle and Hyperbola

