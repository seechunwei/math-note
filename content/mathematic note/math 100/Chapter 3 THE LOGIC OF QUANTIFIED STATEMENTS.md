## 3.1 Predicates and Quantified Statement

The symbolic analysis of predicates and quantified statements is called the predicate calculus. The symbolic analysis of ordinary compound statements (as outlined in Sections 2.1–2.3) is called the statement calculus (or the propositional calculus).

As noted in Section 2.1, the sentence “$x^{2}+2=11$” is not a statement because it may be either true or false depending on the value of x.

In logic, predicates can be obtained by removing some or all of the nouns from a statement.
let P stand for “is a student at Bedford College” 
let Q stand for “is a student at .”
The sentences “x is a student at Bedford College” and “x is a student at y” are symbolized as P(x) and as Q(x, y),  x and y are predicate variables.

==Definition 3.1.1== A **predicate** is a sentence that contains a finite number of variables and becomes a statement when specific values are substituted for the variables. The **domain** of a predicate variable is the set of all values that may be substituted in place of the variable.

==Definition 3.1.2== If P(x) is a predicate and x has domain D, the truth set of P(x) is the set of all elements of D that make P(x) true when they are substituted for x. The **truth set** of P(x) is denoted 
$$
\{ x \in D \mid P(x) \}
$$
Predicate with n number of statement variable where x represent statement variable
$$
P(x_{1},x_{2},x_{3},x_{4},\dots,x_{n})
$$

The truth set of a predicate is a set containing ...tuple from the domain that make the statement true.

We say $P(x)$ is an open sentence over domain $S$.

Notice that $P(x)$ become a sentence if we define the domain $S$. Thus, it is logically equivalent to $\forall x,x \in S\implies P(x)$
The for all and hypothesis is to narrow the mathematical object that we want to deal with.


Example:
Let Q(n) be the predicate “n is a factor of 8.” Find the **truth set** of Q(n) if
a. the domain of n is $\mathbb{Z}^{+}$, the set of all positive integers
b. the domain of n is $\mathbb{Z}$, the set of all integers.

a)$\{ 1,2,4,8 \}$ It means Q(1) ,Q(2) ,Q(4) ,Q(8) is true
or we say $Q(n)$ is true when $n \in \{ 1,2,4,8 \}$

b)$\{ 1,2,4,8,-1,-2,-4,-8 \}$

- One sure way to change predicates into statements is to assign specific values to all their variables. 
- Another way to obtain statements from predicates is to add quantifiers. Quantifiers are words that refer to quantities such as “some” or “all” and tell for how many elements a given predicate is true. 
- The symbol $\forall$ is called the **universal quantifier**. Depending on the context, it is read as “for every,” “for each,” “for any,” “given any,” or “for all.
- the domain of the predicate variable is generally indicated either between the $\forall$ symbol and the variable name (as in $\forall$ human being x) or immediately following the variable name (as in $\forall x \in H$)

==Definition 3.1.3== Let Q(x) be a predicate and D the domain of x. A universal statement is a statement of the form “ $\forall x \in D$, Q(x).” It is defined to be true if, and only if, Q(x) is true for each individual x in D. It is defined to be false if, and only if, Q(x) is false for at least one x in D. A value for x for which Q(x) is false is called a **counterexample** to the universal statement.
[Witness]


==Definition 3.1.4==. Let Q(x) be a predicate and D the domain of x. An existential statement is a statement of the form “ $\exists x \in D$ such that Q(x).” It is defined to be true if, and only if, Q(x) is true for at least one x in D. It is false if, and only if, Q(x) is false for all x in D.

The symbol $\exists$ denotes “there exists” and is called the existential quantifier

Another way to restate universal and existential statements informally is to place the quantification at the end of the sentence. For instance, instead of saying “For any real number x, $x^{2}$ is nonnegative,” you could say “$x^{2}$ is nonnegative for any real number x.” In such a case the quantifier is said to “trail” the rest of the sentence.
(Noted: It's not always equivalent ) 
Example:
$\forall m \in \mathbb{R},\exists n \in \mathbb{R}$ such that m + n is prime number.
$\exists n \in \mathbb{R},\forall m \in \mathbb{R}$ such that m + n is prime number.

#### Equivalent Forms of Universal and Existential Statements

Observe that the two statements “$\forall$ real number x, if x is an integer then x is rational” and “$\forall$ integer x, x is rational” mean the same thing because the set of integers is a subset of the set of real numbers, $\mathbb{Z}\subset \mathbb{R}$.
$$\forall x \in U,if\ P(x)\ then\ Q(x)\equiv \forall x \in D,Q(x)$$ by narrowing U to be the subset D consisting of all values of the variable x that make P(x) true.

$$
if\ P(x)\ ,then\ Q(x) 
$$
The statement above is a implicit universal statement that equivalent to $\forall x \in U,if\ P(x),\ then\ Q(x)$


#### Implicit Quantification
If a number is an integer, then it is a rational number.
This statement is equivalent to a universal statement. However, it does not contain the telltale word all or every or any or each.

The statement “The number 24 can be written as a sum of two even integers” can be expressed formally as “ $\exists$ even integers m and n such that 24=m + n.”

if x>2 then $x^{2}>4$, in this statement the x implicitly indicate $\mathbb{R}$
For every real number x, if x>2 then $x^{2}>4$

Mathematicians often use a double arrow to indicate implicit quantification symbolically. For instance, they might express the above statement as 
$$
x>2\implies x^{2}>4
$$

==Definition3.1.5==. Let P(x) and Q(x) be predicates and suppose the common domain of x is D.
- The notation P(x)$\implies$Q(x) means that every element in the truth set of P(x) is in the truth set of Q(x), or, equivalently, $\forall$x, P(x)$\to$Q(x).
  （包含关系：if n is a factor of 4, then n is a factor of 8, we know that n is from same domain implicitly thus we say the the truth set of first predicate is the subset of truth set of second predicate.)

- The notation P$\Leftrightarrow$Q(x) means that P(x) and Q(x) have identical truth sets, or, equivalently, $\forall$x, P(x)$\leftrightarrow$Q(x).

The quantification of a statement—whether universal or existential—crucially determines both how the statement can be applied and what method must be used to establish its truth.

a. $(x+1)^{2}=x^{2}+2x+1$
$\forall x \in \mathbb{R},(x+1)^{2}=x^{2}+2x+1$
b. 3x-4=5
Show (by finding a value) that $\exists$ a real number x such that 3x-4=5.

[Tarski's World ]

## 3.2 Predicates and Quantified Statements II

==Theorem 3.2.1== Negation of a Universal Statement
$$
\neg(\forall x \in D, \ Q(x))\equiv \exists x \in D,\ \neg Q(x)
$$
Consider a statement "All book are red color." The negation of it means this statement is false, for this statement to be false means there is at least one book that is not red color.

==Theorem 3.2.2== Negation of an Existential Statement
$$
\neg(\exists x \in D,\ Q(x))\equiv \forall x \in D,\ \neg Q(x)
$$
For the existential statement to be false means Q(x) is false for every single x in D.

**Negation of a Universal Conditional Statement**
$$\begin{align}
\neg(\forall x \in D,P(x)\to Q(x))&\equiv \exists x \in D,\neg(P(x)\to Q(x)) \\
&\equiv \exists x  \in D,P(x)\land \neg Q(x)
\end{align}

$$

in a sense, universal statements are generalizations of and statements, and existential statements are generalizations of or statements.

If Q(x)is a predicate and the domain D of x is the set $\{ x_{1},x_{2},\dots,x_{n} \}$, then the statements
$$
\forall x \in D,Q(x)\equiv Q(x_{1})\land Q(x_{2})\land\dots \land Q(x_{n})
$$
$$
\exists x \in D,Q(x)\equiv Q(x_{1})\lor Q(x_{2})\lor\dots \lor Q(x_{n})
$$

**Vacuous Truth of Universal Statements**
Suppose that no balls at all are placed in the bowl. Consider the statement: 
$$
\text{All the ball in the ball are blue}
$$
This statement can be written as $\forall \ ball,\text{ if the ball is in bowl, the ball is blue}$
We know that the ball is not in the bowl, thus the hypothesis of the if-then statement is false, the statement is vacuously true.

**Variants of Universal Conditional Statements**
