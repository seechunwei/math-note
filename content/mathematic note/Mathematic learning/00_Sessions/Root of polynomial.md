> [!question]
> How to find the root of polynomial

$$
p(t)=a_{0}+a_{1}t+a_{2}t^{2}+\dots+a_{n}t^{n}
$$

polynomial is a finite sum of term which is a product of real coefficient and variable.

> [!question]
> What if the coefficient is complex number?
> 

Any $n$ degree polynomial have $n$ number of root, it is either real or imaginary. 

How to prove?

The expression of polynomial can be factor as $n$ linear factor

$$
p(t)=(t-b_{1})(t-b_{2})\dots(t-b_{n})
$$

(with the assumption that the leading coefficient is 1)

By partial fraction we can notice that every polynomial can be factor to linear factor and non reducible quadratic factor. Since we say that it can have $n$ linear factor, thus the reducible quadratic factor should be factor into 2 linear factor with complex number.

If there is a non reducible quadratic factor for example: $x^{2}+1$ can be factor as 

$$\begin{align}
x^{2}+1&=(x+1i)(x-1i) \\
&=x^{2}-(1i)^{2}
\end{align}
$$

Wait i don't know how to factor? Why? remember what is the property if $a$ is a linear factor of $f(x)=x^{2}+1$? $(x-a)$ is one of the linear factor of $f(x)$ iff $f(a)=0$ (Factor Theorem) . (Factor theorem come from remainder theorem). 

Particularly, (we can isolate $x^{2}$ and think what value of $x$ fulfill the expression)

$$
\begin{align}
x^{2}+1&=0 \\
x^{2}&=-1
\end{align}
$$
The answer is $i$. So $x^{2}+1=(x-i)^{2}$? No because $(x-i)^{2}=x^{2}-2 x i+i^{2}$. Notice that $-i$ is also one of the factor because $(-i)^{2}=(-1)^{2}i^{2}=-1$. Thus,

$$
x^{2}+1=(x+i)(x-i)
$$
Actually i get the answer early but i don't know $-(i)^{^{2}}=1$.

(This method of cancelling out the middle term is called multiplying conjugate). 

> [!question]
> What if we move to 3 degree?



> [!theorem] Quotient-Remainder Theorem/  Division  Algorithms
> For any integer $a$ and (positive?) integer $d$, there exist an unique integer $q$ and $r$ such that $0\leq r<d$ 
> $$
> a=dq+r
> $$

How to prove?

In analogy of polynomial, for any polynomial $f(x)$ and a $d(x)$, there exist an unique polynomial $q(x)$ and $r(x)$ such that degree of $r(x)$ is less than the degree of $d(x)$ (the degree here is like the modulo)

$$
f(x)=d(x)q(x)+r(x)
$$


> [!theorem] The Factor Theorem
>  $r$ is a root of a polynomial iff $(x-r)$ is a factor of $P(x)$

What does it mean to be a factor? (Link to quotient remainder theorem)
It means that $P(x)=(x-r)q(x)$ which is $r(x)=0$. (Notice that degree of $(x-r)$ is 1, this $r(x)$ is a constant)

Suppose $r$ is a root of a polynomial $P$, then by definition $P(r)=0$. From remainder theorem we know that there exist a unique $q(x)$ and $r(x)$ such that degree of $r(x)$ is less than 

$$
\begin{align}
P(x)&=(x-r)q(x)+R \\
P(r)&=(r-r)q(r)+R \\
0&=R
\end{align}
$$
Thus, by remainder theorem $(x-r)$ is a factor of $P(x)$. $\blacksquare$

How about FTA? States that _every_ non-constant polynomial with complex coefficients has _at least one_ complex root. (it is proposition of FTA)

Now we have enough tool to prove (Using FTA and Factor Theorem)
Suppose a polynomial $P(x)$ with $n$ degree . By FTA, it has at least one complex root say $r_{1}$

. Thus, by factor theorem
$$
P(x)=(x-r_{1})Q_{1}(x)
$$
$Q_{1}(x)$ is a polynomial with $n-1$ degree . By FTA again, it has at least one complex root say $r_{2}$. Thus,

$$
P(x)=(x-r_{1})(x-r_{2})Q_{2}(x)
$$

We repeated the process until $Q_{n-1}(x)$ become a linear factor. Thus, we have prove that $n-th$ polynomial have $n$ root. $\blacksquare$

Question:
Does the FTA apply to a polynomial of degree 1? (Look at the definition of FTA—does it apply to _non-constant_ polynomials?)

Yea for a polynomial degree of 1, $Q_{n-1}(x)=(1)Q_{n-1}(x)+0$ , thus the root is simply the solution of $Q_{n-1}(x)=0$ , suppose
$$
Q_{n-1}(x)=ax+b
$$
then,
$$
\begin{align}
ax+b&=0 \\
x&=-\frac{b}{a}
\end{align}
$$
which is the root for $Q_{n-1}(x)$.

If $P(x)=(x-2)(x-2)(x-3)$, my proof state that this is a degree 3 polynomial with 3 roots. However, are there _three distinct_ roots, or just two?

Ans: There are just 2 distinct root, but in my proof we didn't use the property of distinct root, so our statement is sill having $n$ roots counted with multiplicity. 


Notice from Factor theorem we only concern about  $f(x)=0$ iff the remainder theorem is $0$. Is it true for other value?

Again by Quotient Remainder Theorem. Suppose

$$
\begin{align}
P(x)&=(x-a)Q(x)+r \\
P(a)&=(a-a)Q(a)+r \\
&=r
\end{align}
$$
 it is true for opposite direction. (Biconditional)
Thus,

$f(a)=r$ iff the remainder of $\frac{f(x)}{(x-a)}$ is $r$. It is called Quotient Theorem in some book.

Mathematically, we say that Factor Theorem is a corollary of the Remainder Theorem.(It is a special case of Remainder Theorem). it is the foundation of Synthetic Division and Horner's Method.

What if it divide by a quadratic?

If $P(x)$ has real coefficient, we will notice that the non-real complex roots always come in "conjugate pairs".
This is because when we multiply the complex conjugate, the middle imaginary term will cancel each other and left with the real part

Conjugate Root Theorem
The property that conjugation is a homomorphism over complex addition and multiplication??

> [!remark]
> Remark
> I found that the the way to prove this is the same way to prove fundamental theorem of arithmetic. (It is something like we factor it into a simplest form)
> 
> We can categorize these kind of question into Unique Factorization Domains (UFD)   
> 
> But notice that if we have a polynomial with real coefficients, i cannot always factor it into purely real linear factor. So in this case what is the simplest form?
> 
> The simplest form is less than or equal to degree 2? Observation from partial fraction. how to prove?


Go back to our main question how to find the root of polynomial.

From our proof we know that, for any $n$ degree polynomial $P(x)$ ,

$$
P(x)=b_{0}+b_{1}x+\dots+b_{n}x^{n}
$$

it can be express uniquely as

$$
P(x)=(a_{1}x_{1}-r_{1})(a_{2}x_{2}-r_{2})..(a_{n}x_{n}-r_{n})
$$
where $r$ is complex number. Notice that 

$$
\prod_{i=1}^{n} a_{i}=b_{n} \text{ and } \prod_{i=1}^{n} r_{i}=b_{0}
$$

which is the leading coefficient of $P(x)$ and the constant term of $P(x)$ respectively. Thus,

$$
\begin{align}
a_{i}x_{i}-r_{i}&=0 \\
a_{i}x_{i}&= r_{i} \\
x_{i}&=\frac{r_{i}}{a_{i}}
\end{align}
$$
Thus, every root is in this form , it is called Rational Zero Theorem. We can make a guess if the coefficient of the polynomial is integer. where $r_{i}$ is the factor of constant and $a_{i}$ is the factor of leading coefficient.

What happen if the leading and constant is integer but the other term is not?

Question
If i have a polynomial like $P(x)=x^{2}-2$, the roots are $\pm \sqrt{ 2 }$
1) These roots are not rational 

2) Notice that $\sqrt{ 2 }=\frac{\sqrt{ 2 }}{1}$ , but $\sqrt{ 2 }$ is not a factor of 2 , because it is not an integer.

3) So the limitation of this rational zero theorem is only applied when the polynomial has rational root. 

When it will have rational root? when the coefficient of the polynomial is rational. But for us to guess the factor, it should be integer.


Example of encapsulation: Think of factor theorem is the special case of remainder theorem, and reminder theorem act like a function, the value of domain will map to the remainder value.

$$
f:a\mapsto \text{ remainder of } \frac{P(x)}{x-a}
$$

The degree is like modulo, if degree 1 mean modulo a linear factor.
$$
P(x) \equiv R (\text{mod }(x-a))
$$
So the degree of my modulo is the degree of the divisor. What if $P(x)$ divide by
$(x-1)$ leaves a remainder of 3 and $P(x)$ divided by $(x-2)$ leaves a remainder of 5, can we construct the remainder of $P(x)$ when divided by $(x-1)(x-2)$.

$$
r(x)=Ax+B
$$

So,
$$
P(x)=(x-1)(x-2)Q(x)+(Ax+B)
$$

substitute $P(1)=3$

$$
\begin{align}
3&=(A+B) \\
B&=3-A
\end{align}
$$

Substitute $P(2)=5$

$$
5=(5A+B)
$$

Solve the simultaneous system of linear equation:

$$
\begin{align}
5&=5A+(3-A) \\
5&=4A+3 \\
A&=2
\end{align}
$$
Thus,
$$
B=1
$$
hence, the remainder $r(x)=2x+1$

Generalization:
So whenever we have the remainder of $\frac{P(x)}{x-a_{i}}$ , then we can find the remainder of $\frac{P(x)}{\prod a_{i}}$. This actually Chinese Remainder Theorem. The divisor must be pairwise coprime (which means all the $a_{i}$ values must be distinct) (Why? to make sure the number of equation match the number of variable in the system of linear equation) 

Challenge: What if the root is not distinct?  If i know $P(1)=3$ and $P'(1)=2$, can i still construct the remainder for the divisor $(x-1)^{2}$? (Hermite Interpolation)

2 tool
1) mod
2) the proof of Unique Factorization domain