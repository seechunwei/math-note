
#### Two Universal quantifier
$$
\forall x \in D,\forall y \in E,P(x,y)
$$
When is this statement true?
This statement is true iff for all x in D and for all y in E such that $P(x,y)$ hold. 
$P(x,y)$ is true for all ordered pair $(x,y)\in D\times E$

How to prove?
[Prove by contradiction]
[Divison into case method of analysis or prove by cases[[#^708188]]]
[Direct prove]

When does it wrong?
This statement is wrong iff there exist one element x in D or one element y in E such that $P(x,y)$ does not hold. That means there is a counter example (x, y) that makes P(x, y) false.

Let p represent the universal statement above, if we want to prove p is wrong, we just need to prove $\neg p$ is true. Notice the true statement that make the universal wrong is:
$$
\exists x \in D, \exists y\in E,\neg P(x,y)
$$
Thus, we can say that the negation of universal statement is existential statement with the negation of the predicate


Notice that $P(x,y)$ is a predicate with 2 statement variable.

$$\begin{array}
\ \forall x \in D,\forall y \in E,P(x,y) \\
\equiv\forall y \in E,\forall x \in D, P(x,y)
\end{array}
$$
But notice that,
$$\begin{array}
\ \forall x \in E, \forall y \in D,P(x,y) \not\equiv \forall x \in D,\forall y\in E,P(x,y)
\end{array}
$$

Suppose $E=\{ 1,2 \}$ ,$D=\{ 3,4 \}$
Then, $\forall x \in D,\forall y \in E,x>y$ is true.
However, $\forall x \in E,\forall y \in D,x>y$ is false.

Thus, the domain matter. 

The relation among $\forall,\exists,\land,\lor$
The negation of a for all statement is a there exists statement, and the negation of a there exists statement is a for all statement. These facts are analogous to De Morgan’s laws. This similarity is not accidental. In a sense, universal statements are generalizations of and statements, and existential statements are generalizations of or statements.


Suppose that $Q(x)$ is a predicate and the domain D is the set of $\{ x_{1},x_{2},x_{3},\dots,x_{n} \}$

$$
\forall x \in D,Q(x)\equiv Q(x_{1})\land Q(x_{2})\land\dots \land Q(x_{n})
$$

$$
\exists x \in D,Q(x)\equiv Q(x_{1})\lor Q(x_{2})\lor\dots Q(x_{n}) 
$$



#### Two existential quantifiers
$$
\exists x \in D,\exists y \in E, P(x,y)
$$
When does it true ?
It is true when there is a witness (x, y) that makes P(x, y) true

when does it false?
P(x, y) is false for all element (x, y)




#### Statement with multiple quantifiers

1) Universal existential statement
$$
\forall x \in D,\exists y \in E \text{ such that }P(x,y)


It is actually a universal statement .$\exists y \in E \text{ such that }P(x,y)$ is a predicate for $\forall x \in D$ denoted by $\forall x \in D,Q(x)$ . Notice that the whole predicate refer to the object x thus is $Q(x)$ but not $Q(x,y)$

Negation of it:
$$
The negation of
$$\forall x \in D,\exists y \in E \text{ such that }P(x,y)
$$
is
$$
\exists x \in D,\forall y \in E \text{ such that }\neg P(x,y)
$$

when does it true?
It is true if Q(x) is true for every $x \in D$. That means we can find at least one $y\in E$ for each $x \in D$ such that $P(x,y)$ is true.


2) Existential universal statement
$$
\exists x \in D,\forall y \in E \text{ such that }P(x,y) 
$$
it is actually a existential statement of the form $\exists x \in D,Q(x)$
we need at least one witness $x \in D$ such that $\forall y \in E,P(x,y)$ is true.

Note that this two statement is totally different. And the order of quantifier mattered.


#### Universal conditional statement
Vacuous Truth of Universal Statements
Consider the following statement:
$$
\text{All ball in the bowl is blue}
$$
What is the truth value of this statement is there is no ball in the bowl. A statement is consider true iff it's negation is false

The negation of it:
$$
\text{There exists a ball in the bowl that is not blue}
$$

This statement only be true iff there is at least a ball in the bowl, since the bowl do not have any ball thus the statement is false.
Thus, the universal statement is true.
This clearly show that how this two statement be formalize into formal logical notation in next section

In conclusion,

$$
\forall x \in D, P(x)\to Q(x)
$$


is called vacuously true or true by default if, and only if, P(x) is false for every x in D.

The negation of it
$$
\exists x \in D, P(x) \land \neg Q(x)
$$


#### Formal logical notation
It is useful to use formal logical notation to represent the word *such that* so that we can perform operation.

$$\begin{array}
\ \forall x \in D,\text{ such that }P(x) \\
\forall x ,x \in D\to P(x) \\
\forall x,x \in D \leftrightarrow P(x)
\end{array}
$$

$\to$ iff $x \in D \subseteq P(x)$
$\leftrightarrow$ iff $P(x)$ and $x \in D$ have same truth set


$$
\begin{array}
\ \exists x \in D \text{ such that } P(x) \\
\exists x(x \in D \land P(x))
\end{array}
$$



The operation order
1) $\land \lor$
2) $\to$
3) $\forall,\exists$

$\forall$ can be convert to $\to$ and then convert to $\land \lor$
$\exists$ can be convert to $\land \lor$ 

Taken together, the symbols for quantifiers, variables, predicates, and logical connectives make up what is known as the language of first-order logic

Example
$$
\exists y \in \mathbb{R},\forall x \in \mathbb{R}\land x<y
$$
The negation of the statement is
$$
\begin{align}
\neg(\exists y(y \in \mathbb{R}\land\forall x (x\in \mathbb{R} \to x<y)))&\equiv \forall y(\neg (y \in \mathbb{R})\lor \exists x\neg(x \in \mathbb{R}\to x<y)) \\
&\equiv \forall y \in \mathbb{R},\exists x(x \in \mathbb{R}\land x\geq y) \\
&\equiv \forall y \in \mathbb{R}, \exists x \in \mathbb{R},x\geq y
\end{align}

$$

Since we y is always in $\mathbb{R}$ thus $\neg(y \in \mathbb{R})$ is false. Thus, $y \in \mathbb{R}$ is true

Note that we use the Negation of Universal Statement Theorem is way more easier than convert it into formal logical notation.

### Characterization

Let say we are studying one concept that declare $\forall x \in S,P(x)$ , and $Q(x)$ is a predicate concerning about the concept.

We say $P(x)$ is characterize by $Q(x)$ which mean that $\forall x \in S,P(x)\iff Q(x)$ . $Q(x)$ provide a different angle of interpreting the concept. (alternative way of looking at the concept)

For example Mathematical induction$\iff$ Well ordering Principle. 