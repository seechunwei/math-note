
In this chapter, Spivak point out that function is an mathematical object rather than a process or action. For the sake of understanding the motivation of define modern definition of function, we use a intuitive definition:


> [!definition]
> A function is a rule that assign to each certain real numbers, some other real numbers

The rule not necessarily need to be express using mathematic language (algebraic formula). For example: The rule which assign $2$ to $\pi$.

If $f$ is a function, then the number which $f$ associates to a number $x$ is denoted by $f(x)$ read "$f$ of $x$". For example:

$$
\begin{align}
f(x)=x^{2} &&\text{for all }x
\end{align}
$$

Notice that the for all $x$ indicating that  what $f(x)$ is for every number $x\in Domain(f)$. Notice that the for all $x$ can be omitted and being understood. 

Always remember that $f(x)$ is a real number. It is more precise the express function as a object itself. 

To do this we need to define something. Identity function $I(x)=x$ and any function $f$ for $f(x)$. For example the rule that output the $\sin(x)$ is $\sin$.

How to define the $+,\times, /$ operation of function?

The new function $f+g$  called the sum of $f$ and $g$ is defined as
$$
(f+g)(x)=f(x)+g(x)
$$
The domain of $f+g$ is $Domain(f) \cap Domain(g)$

In a similar vein, we define product $f\cdot g$ and the quotient $\frac{f}{g}$ by

$$
(f\cdot g)(x)=f(x)\cdot g(x)
$$
and
$$
\begin{align}
\left( \frac{f}{g} \right)(x)= \frac{f(x)}{g(x)}&& g(x)\neq 0
\end{align}
$$

Scalar multiplication:
$$
(c\cdot g)(x)=c\cdot g(x)
$$
This can be view as a special case of product of function by replace the $c$ to $f$ where $f(x)=c$ is a constant function.

The associativity and commutativity and distributivity is all prove by the property of number.

The composition of $f$ and $g$ is

$$
(f\circ g)(x)=f(g(x))
$$
the domain is all $x$ in domain $g$ and $g(x)$ is in domain $f$.

Thus,

$$
f(x)= \frac{x+x^{2}+x\sin ^{2}x}{x\sin x+x\sin ^{2}x}
$$
can be express as

$$
f= \frac{I+I\cdot I+I\cdot \sin \cdot \sin }{I\cdot \sin+I\cdot \sin \cdot \sin}
$$
in term of function itself. Although this method of writing can reveal function as a object, but it is not readable when the function is getting complex.  

The best notation is 
$$
x\mapsto \sin(x^{2})
$$
Why this is important?
Imagine someone say the function $x^{2}+t$. It is ambiguous in the sense that $x$ is the input or $t$ is the input.

> [!remark]
> $\to$ and $\mapsto$ are different. When we write $f:A\to B$ means it map one set(domain) to another set (codomain). If we write $f:x\mapsto f(x)$ , it means $f$ map each element in the domain to $f(x)$.



How to we define a function is equal?
For example,
$$
f(x)=x^{2}
$$
and
$$
f(x)=x^{2}+3x+3-3(x+1)
$$

If we talk about the rule, they are totally different 
Rule 1: Take $x$ and square it
Rule 2: Take $x$ square it, add $3x$, add $3$ subtract $3(x+1)$

But they both give the exact same output for every input. If we write the assignment in an ordered pair, it will be like $(1,1),(2,4),\dots$

The correct question to ask about a function is not \What is a rule?" or \What is an association?" but \What does one have to know about a function in order to know all about it?"

And we collect those ordered pair in to a set. Thus, function can be defined as a collection of pairs of numbers and we need to prevent 2 pair have the same input with different output. Thus, the definition is 

> [!definition]
> A function is a collection of pairs of numbers with the property: if $(a,b)=(a,d)$, then $b=d$.

> [!definition]
> If $f$ is a function, the domain of $f$ is the set of all $a$ where there is a unique number $b$ such that $(a,b)\in f$.

[[Chapter 1-Speaking mathematically#^f551f4]]

# APPENDIX ORDERED PAIRS

Definition of ordered pair in set
$$
(a,b)=\{ \{ a \},\{ a,b \} \}
$$

[[Chapter 1-Speaking mathematically]]

