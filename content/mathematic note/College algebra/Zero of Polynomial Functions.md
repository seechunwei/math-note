> [!note] The division algorithms for polynomial
>
if $P(x)$ is divide by $d(x)$ where the degree of $d(x)$ is less than or equal to $P(x)$, there exists an unique $Q(x)$ and $r(x)$ such that
>
>$$P(x)=Q(x)d(x)+r(x)$$
>
>where the degree of $r(x)$ is strictly less than $d(x)$.

> [!note] Remainder Theorem for polynomial
> If a polynomial $f(x)$ is divided by $x-k$, then the remainder is the value of $f(k)$
>
>For example let $P(x)$ divide by $(x-k)$
>$$P(x)=(x-k)q(x)+r$$
>
Since $(x-k)$ is a linear factor, it follow that the remainder is a constant say $r$. 
What happen if we substitute $k$?
$$P(k)=(k-k)q(k)+r=0+r=r$$
>
>Thus, we can conclude that the value of $P(k)$ is the remainder of $P(x)$ divide by $(x-k)$. 




> [!info] Factor Theorem
> What if $k$ is a zero of the function?. Thus, $P(k)= 0$ , thus, according to Remainder Theorem, remainder of $P(k)$ divide by $(x-k)$ is 0.
>
>$$P(k)=q(k)(x-k)+0$$
>
>Thus, we can conclude that if $k$ is a zero of $P(x)$, then $(x-k)$ is a factor of $P(k)$. Conversely, if $(x-k)$ is a factor of $P(x)$, then $P(k)=0$, thus $k$ is a zero of $P(x)$. 
>
Thus, $k$ is a zero of $P(x)$ if and only if $(x-k)$ is a factor of $P(x)$.

### Using Rational Zero Theorem to find rational zeros

Suppose a polynomial function $P(x)$ with rational zeros $\frac{p_{n}}{k_{n}}$. Thus, by Factor Theorem it follow that $P(x)=\left( x-\frac{p}{k} \right)\left( x-\frac{p_{1}}{k_{1}}\ \right)\dots\left( x-\frac{p_{n}}{k_{n}} \right)$  where $p_{n},k_{n}$ are arbitrary integers.

Let $P(x)=0$ (to find the zeros), thus one of the factor must=0. Thus,

$$
\begin{align}
x-\frac{p}{k}=0 \\
kx-p=0
\end{align}
$$
Thus,

$$P(x)=\left( kx-p \right)(k_{1}x-p_{1})\dots(k_{n}x-p_{n})$$

Notice that the leading coefficient is $kk_{1}\dots k_{n}$ and the constant is $pp_{1}\dots p_{n}$. 

Thus. when the leading coefficient is 1, the possible rational zeros are factors of the constant term.

How?
1) List all the integer factors for leading coefficient and constant term.
2) list all the combination of rational zeros
3) check by substituting into the function
4) After find one use division algorithms to find the quotient 

### Using the Fundamental Theorem of Algebra

The Fundamental Theorem of Algebra states that, if f(x) is a polynomial of degree n>0, then f(x) has at least one complex zero.

We can use this theorem to argue that, if f(x) is a polynomial of degree n>0, and a is a non-zero real number, then f(x) has exactly n linear factors
f(x)=a(x−c1)(x−c2)...(x−cn)where c1, c2, ..., cn are complex numbers. 

Therefore, f(x) has n roots if we allow for multiplicities.

Sometimes we can only find one linear factor for function with degree 3. Thus, there must be 2 imaginary roots that indicate 2 turning point that does not cross the x-axis.

![[Pasted image 20260311132816.png|316]]

> [!info] Linear Factorization Theorem
> According to the Linear Factorization Theorem, a polynomial function will have the same number of factors as its degree, and each factor will be in the form (x−c), where c is a complex number.

---

Suppose $P(x)$ have a real coefficient and a complex zero say $(a+bi)$ where $b\neq 0$. To make the coefficient real, there must exist a conjugate pair of $(a+bi)$ which is $(a-bi)$ as a factor of $P(x)$ so that when multiply, it will eliminate the imaginary part

> [!info] complex conjugate theorem
> If the polynomial function f has real coefficients and a complex zero in the form a+bi, then the complex conjugate of the zero, a−bi, is also a zero.

### Descartes's Rule of Signs

What is the relationship between the number of positive real zeros and the number of sign changes?

In other word, how many linear factor in the form of $(x-k)$ where $k> 0$ and the number of sign change.

Suppose the polynomial with one positive real zeros

$$
P(x)=(x-k)Q(x)
$$

Thus, Let's align them by their powers of $x$ (like old-school long multiplication) to see the new coefficients for $P(x)$:

$$\begin{array}{rccccccc} \text{Signs of } x \cdot Q(x): & + & - & - & + & 0 \\ \text{Signs of } -r \cdot Q(x): & 0 & - & + & + & - \\ \hline \text{Signs of } P(x): & + & ? & ? & + & - \end{array}$$

When we multiply $Q(x)$ with $x$, it preserve the sign and add one degree to each term

When we multiply $Q(x)$ with $-k$, it change the sign of each term.

Thus, notice that the leading coefficient and the last term have opposite sign. 

What if we multiply a polynomial with 2 linear factor
$$
P(x)=(x-k)(x-k_{1})Q(x)
$$
Thus, $P(x)$ has 2 positive real zeros, thus we look at the graph , the y-intercept is when $x=0$, which is the last term, and when $x\to \infty$ , the leading change significantly large. Thus, if both are same sign, then at least 2 change of sign.

If different sign, then at least 3 change of sign. 

---

 WHY? Zero Sign Changes = A One-Way Street

Imagine a polynomial where every single coefficient is positive, like $P(x) = x^3 + 4x^2 + 2x + 5$.

For any positive value of $x$, every single term is positive. The constant term pulls up. The $x$ term pulls up harder. The $x^2$ term pulls up even harder.

Because there are zero sign changes, there is no disagreement among the terms. The graph starts positive and strictly rockets upwards. It is geometrically impossible for it to cross the x-axis.

- **Algebra:** 0 sign changes.
    
- **Geometry:** 0 positive roots.
    

### 3. A Sign Change = A Reversal of Force

Now, imagine a sign change occurs. Let’s look at $P(x) = x^3 - 4x^2 + 2x - 5$.

The sequence of signs is $(+, -, +, -)$.

Read this from right to left (from the lowest power to the highest), just as the graph experiences it when sweeping from $x=0$ outwards:

1. **Start ($a_0 = -5$):** The graph starts below the x-axis.
    
2. **First Handoff ($a_1 x = +2x$):** As $x$ grows, a positive term takes over. It pulls the graph UP toward the x-axis.
    
3. **Second Handoff ($a_2 x^2 = -4x^2$):** As $x$ grows further, a negative term takes over, pulling the graph back DOWN.
    
4. **Final Handoff ($a_3 x^3 = +x^3$):** Eventually, the positive $x^3$ term dominates, pulling the graph violently UP toward infinity.
    

**The Golden Link:** Every time there is a sign change in the coefficients, the "dominant force" pulling on the graph switches direction.

Each switch in direction gives the graph an _opportunity_ to cross the x-axis. Since the sequence $(+, -, +, -)$ has 3 sign changes, the graph reverses its vertical trajectory 3 times as $x$ grows, giving it exactly 3 opportunities to cross the x-axis.

---

Thus we can conclude that Every single time you introduce a positive root, the algebra forces a new sign change to appear.

1, at least 1 sign change
2, at least 2 sign change 
.Thus, we can narrow the possibility when we want to study what happen to positive real zeros with the number if sign change.

if sign change is 3, then the positive real zeros must less than or equal to 3. Because if the number of positive zeros is 4, then it has at least 4 sign of change (contradiction)

Why is reduce by even number?
because of the parity, the parity of number of sign is the same as the parity of number of positive real zeros

==Formal Proof==
**Rolle's Theorem** and mathematical induction
Segner’s Lemma 

> [!note] Descartes’ Rule of Signs
> According to Descartes’ Rule of Signs, if we let f(x)=anxn+an−1xn−1+...+a1x+a0 be a polynomial function with real coefficients:
> 
> • The number of positive real zeros is either equal to the number of sign changes of f(x) or is less than the number of sign changes by an even integer.
> 
> • The number of negative real zeros is either equal to the number of sign changes of f(−x) or is less than the number of sign changes by an even integer.

