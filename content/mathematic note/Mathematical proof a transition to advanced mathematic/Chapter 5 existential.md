
How to think of the question?
Example: Parity
think of 1 expression that involve multiplication and addiction (we can use the theorem to infer).

$n^{2}+3n$ , we know that this expression is always even for all $n \in \mathbb{Z}$, thus we ask the reader to disprove the below statement
$$
n^{2}+3n \text{ is even }\to n \text{ is odd}
$$
Which is wrong because $n$ can be even. In this case the counter example is all the even integer.

$\forall x \in D,P(x)\to Q(x)$
The negation is $\exists x \in D,P(x)\land \neg Q(x)$



Example 5.9
$a^{4}x^{2}+b^{4}y^{2}>2a^{2}b^{2}xy$

$(a^{2}x-b^{2}y)^{2}\geq 0$

Any $x,y$ that make the expression become 0 is counterexample.

## Sections 5.1 Exercise
5.1 
$\log(ab)=\log (a)+\log(b)$
Apparently this is from exponent rule. But what if $a,b$ is negative? Then, $\log(ab)=\log(-a)+\log(-b)$

$\log(-a)$ and $\log(-b)$ is undefined in log (refer to the logarithm graph)


5.4 take $n =5$

5.5
$(a+b)^{3}=a^{3}+3a^{2}b+3ab^{2}+b^{3}$

Notice that $3a^{2}b+3ab^{2}\neq 2a^{2}b+2ab+2ab^{2}$

when does it right?
$$
\begin{align}
3a^{2}b+3ab^{2}-2ab(a+1+b)&=3ab(a+b)-2ab(a+1+b) \\
&=ab(a+b)-2ab
\end{align}
$$
By setting the difference to zero. The only solution is when $a=1$ and $b=1$ .


5.7
a)
$$
\begin{align}
\frac{a+b}{a}+\frac{a+b}{b}=\frac{(a+b)(a+b)}{ab}
\end{align}
$$
Expand 
$$\frac{a^{2}+2ab+b^{2}}{ab}$$

Split
$$
\frac{a}{b}+2+\frac{b}{a}
$$
Since $\frac{a}{b}+\frac{b}{a}\geq 2$.(because AM-GM) Thus. the expression above greater than 4.

(generally the sum of two reciprocal is greater than or equal to 2.)
b)
Yes, how to prove ? just derive the equality become $a=b$.

5.8 
$$
1+\frac{c^{2}}{d^{2}}+\frac{d^{2}}{c^{2}}+1
$$

$$
\begin{align}
\frac{c^{2}}{d^{2}}+\frac{d^{2}}{c^{2}}&\geq 2\sqrt{ 1 } \\
&\geq 2
\end{align}
$$
Thus,
$$
1+\frac{c^{2}}{d^{2}}+\frac{d^{2}}{c^{2}}+1\geq 4
$$

Counter example $c=1$ and $d=1$

5.9
Let $x=3$ and $n =2$ (Pythagoras theorem)

5.10
2,4,6 or 1,3,5
Any 3 positive integers that have same parity can be counter example.

5.11
1,2,3 
analysis: The sum is even integer, for a even integer divisible by 3, it must divisible by 6.
For example (1,3,5)=42=3x14

