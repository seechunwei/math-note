# Purpose of this course
- Logic and Proof
	- Help student to think abstractly
	- learning to use logically valid forms of argument and avoid common logical errors
	- appreciating what it means to reason from definitions

# 1.1 Variable
## Definition 1.1.1
- Variable is a letter that used as a placeholder to represent ambiguous value

### Function of variable
- talk about something that imagine that it has one or more values but you don’t know what they are,
- you want whatever you say about it to be equally true for all elements in a given set
#### Example
- When a real number is divisible by 6, it is also divisible by 3
- When a real number r is divisible by 6, it is also divisible by 3
	- We use variable r to replace the ambiguous word 'number', the number itself can be vary and refer to particular value

## Mathematical statement
- Statement is a declarative sentence that is either true or false (true value can be determine)
### Universal statement
- Statement that declare all the element in a set is true for certain property]
- All positive numbers are greater than 0
### Conditional statement
- Statement that declare if one thing is true, then some other things also be true
- if p then q 
### Existential statement
- Statement say that there is at least one thing for which the property is true
- There is an even number that is also a prime number
	Noted: We can expressed a statement in different ways without changing the meaning 
	- All even number is divisible by 2
	- if x is an even number, then it is divisible by 2
- 
### Universal Conditional Statement
- Universal statements contain some variation of the words “for every” and conditional statements contain versions of the words “if-then.” A universal conditional statement is a statement that is both universal and conditional
- For every set A, if A have no element in it, then A is consider as an empty set

#### Property
- they can be rewritten in ways to be purely universal or purely conditional
	- If set A have no element in it, then A is consider as an empty set
	- For every empty set A, there is no element in it

### Universal Existential Statement
- It contain 2 part, the first part declare all the element in a set is true for certain property , the second part assert the existence of somethings as the property.
	- Every real number has an additive inverse.

### Existential Universal Statements
- its first part asserts that a certain object exists and is universal because its second part says that the object satisfies a certain property for all things of a certain kind
	- There is a non negative integer m that is less than every positive integer
- it assert at least one things have certain relation with all the element in a set

# 1.2 The Language of Sets
### Cantor Set Theory/Naive Set Theory
- **Set** as a formal mathematical term was introduced in 1879 by Georg Cantor (1845–1918). According to Cantor Set Theory set is a collection of elements. The elements can be every object that you can imagine including no element and itself.
#### Property [[The term used in Mathematic]]
- The **axiom of extension** says that a set is completely determined by what its elements are
	- The order is not important
	- if an element appeal more than 1 times, it is consider the same as if it appeal one times
- The **axiom of unrestricted comprehension**
	- We can make any set that we want and think of
	- we can have empty set we can have set that contain itself


Set-Roaster notation 

$$
\begin{array}{p{width}}
\text{If } S \text{ is a set, the notation } x \in S \text{ means that } x \text{ is an element of } S.\\
\text{The notation } x \notin S \text{ means that } x \text{ is not an element of } S. \\
\text{A set may be specified using the set-roster notation by writing all of its elements between braces.} \\
\text{For finite set A, A}=\{ 1,2,3 \} \\
\text{For infinite set B, B}=\{ 1,2,3,4,\dots \}\text{The ...(ellipsis) means so forth} 
\end{array}
$$
set with single element is call singleton set while set with multiple element is call multi set, set with no element is call empty set or null set denoted by $\emptyset$



In a set we can list out all the element in the set, and we use comma to seperate each element
Finite set: $A=\{ 1,2,3 \}$
Infinite set: $B=\{ 1,2,3,\dots \}$

Notice that sometimes the element inside the set is those element possess some property in a universal set. For example
$A=\{ x \in \mathbb{Z} \mid x> 0 \}$ .The | means such that . This can be written as $A$ is the set containing element $x$ in the set of $\mathbb{Z}$ such that $x> 0$.

A set with same element can be express in different way
$E=\{ ..,-2,0,2,\dots \}$
$E=\{ x \in \mathbb{Z} \mid x=2k \text{ for some integer k}\}$
$E=\{ 2x: x \in \mathbb{Z} \}$
$E=\{ 2\mathbb{Z} \}$


The element of set that satisfy the property is depend on the universal set
$\{ i, -i \}=\{ x \in \mathbb{C} :x^{2}+1=0\}$
$\emptyset=\{ x \in \mathbb{R} :x^{2}+1=0\}$

Example:
$C=\{x \in \mathbb{R}:x^{2}-(2+\sqrt{ 2 })x+2\sqrt{ 2 }=0  \}$ 

AC method 
$ac=-2\cdot -\sqrt{ 2 }$
$b=-2-\sqrt{ 2 }$
Thus, $(x-2)(x-\sqrt{ 2 })$. Thus, $C=\{ 2,\sqrt{ 2 } \}$

$D=\{x \in \mathbb{Q}:x^{2}-(2+\sqrt{ 2 })x+2\sqrt{ 2 }=0  \}$ 
Thus, $D=\{ 2 \}$


>==Definition 1.2.1==. Suppose A and B are sets. We say that A and B are equal, denoted A=B, iff every element x in A is in B and vice versa, every element in B is in A.

So consider a set A=$\{ 1,2,3 \}$, and set B=$\{ 3,2,1 \}$ and set C$=\{ 1111,22,3 \}$, Are they a same set?
Ans: Yes, because they have same element that is 1,2,3
1. is $\{  \}\in \{ \{  \} \}$ . Yes
2. is $\{ \{ 2 \} \}\in \{ \{ \{ 2 \} \} \}$ Let$\{ \{ 2 \} \}$ =a . Thus $a\in \{ a \}$ 
3. is 0=$\{ 0 \}$ . No, because 0 is an element while $\{ 0 \}$ is a set 

>==Set-Builder notation==
Let S denote a set and let P(x) be a property that elements of S may or may not satisfy. We may define a new set to be the **set of all elements x in S such that P(x) is true.**
We denote this set as follows:
$$
\begin{array}
\ \{ x \in S \mid P(x) \}
\end{array}
$$
we cannot write $\{ x \mid P(x) \}$ , because it will lead to contradiction such that **Russel Paradox**. The set S could be specified if necessary.

What is Russel Paradox?
Let S denote a set such that S$=\{ x\mid x\not\in x \}$ ,it means S is set of all sets that **do not contain themselves** as an element.

if S is an element of S denoted by $S \in S$, it does not satisfy the property $x \not\in x$ , thus $S \not\in S$ 
if S is not an element of S denoted by $S \not\in S$, it does satisfy the property $x \not\in x$ , thus $S \in S$ . Conclusion, it is a contradiction. Nowadays, Zermelo-Fraenkel Set theory (ZFC) with axiom of choice is the commonly recognized axiomatic set theory as the foundations of mathematics. [ZFC]

>==Definition 1.2.2==.Suppose A and B are sets. We say that A is a subset of B, denoted A⊆B , iff for every element x in A, we know x is in B. 
$A\not\subseteq B$ means that there is at least one element x such that $x \in A$ and $x \not\in B$.

Every set is a subset of itself.

Suppose two set $A$ and $B$ such that $A$ is both an element and a subset of $B$
$A=\{ 1 \}$
$B=\{ 1,\{ 1 \} \}$

 How about $B=\{\emptyset,\{ \emptyset \}  \}$ ?
Empty set is a subset of every set but not element .

$A \in B$. $B \in C$ and $A \not\in C$
Example:
$A=\emptyset$
$B=\{ \emptyset \}$
$C=\{ \{ \emptyset \} \}$
Element in $C$ is $\{ \emptyset \}$ which is not $A$



>==Definition 1.2.3==.We say that A is a proper subset of B, denoted $A\subset B$ iff for every element x in A, we know x is in B and there is at least one element x such that $x \in B$ and $x \not\in A$.

>==Definition 1.2.4==.   Kazimierz Kuratowski
Given two elements a and b, the ordered pair (a, b) is defined to be the set $\{ \{ a \},\{ a,b \} \}$.

Definition (Hausdorff)
Given two elements a and b, the ordered pair (a, b) is defined to be the set {{a, 1},{b, 2}}.

- Since we know the order of an order pair (a, b) is important, if we define (a, b) as $\{ a,b \}$ , we cannot define (b, a) as $\{ b,a \}$ because $\{ a,b \}=\{ b,a \}$ but (a, b) $\neq$ (b, a), so we need to distinguish each element in the set to represent the order
- So we need to define 2 set X and Y that represent the order pair $(a,b)(b,a)$ such that a and b are a part of element in X and Y but $X\neq Y$ 
- So we need to add something to the a and b so that when a and b exchange it won't be same, for example $\{ \{ a,1 \},\{ b,2 \} \}$ where 1 and 2 represent the first and second value in the order pair but what if there is a order pair $(a,b)$
- but this definition need extra symbol, what if we use $\{ a \}$ to represent first number, and $\{ a,b \}$ to represent second number vice versa {b} and {b, a}.

>==Theorem 1.2.5.== Suppose $(a,b)$ and $(c,d)$ are ordered pair. Then $(a,b)=(c,d)$ if and only if a=c and b=d.

Prove by definition (forward) 

According the the definition of ordered pair:
$$
\begin{array} \\
(a,b)=\{ \{ a \},\{ a,b \} \text{ and } (c,d)=\{ \{ c \},\{ c,d \} \}  \\

\end{array}
 
$$

Given that $(a,b)=(c,d)$ , thus,
$$
\{ \{ a \},\{ a,b \} \}=\{ \{ c \},\{ c,d \} \}
$$

by definition, If set A and set B are same iff every element x in A is in B and vice versa, every element in B is in A. Thus
$$
\begin{array}
\ \{ a \}=\{ c \} \text{ and } \{ a,b \}=\{ c,d \}
\end{array}
$$
since $\{ a \}=\{ c \},\text{thus a=c}$ , $\{ a,b \}=\{ c,d \}$ ,since a=c,  b=d.

what if a=b and c=d
$$\begin{array}
\{ \{ a \},\{ a,b \}= \{ \{ a \},\{ a,a \} \}  \\
=\{\{ a \},\{ a \} \}\\
=\{ \{ a \} \}
\end{array}

$$
$$
\begin{array}
\{ \{ c \},\{ c,d \}= \{ \{ c \},\{ c,c \} \}  \\
=\{ \{ c \},\{ c \} \} \\
=\{ \{ c \} \}
\end{array}
$$
Thus, a=c

Prove by definition (forward) 
if a=c, b=d
$$
\begin{align}
\ (a,b)&=\{ \{ a \},\{ a,b \} \} \\
&=\{ \{ c \},\{ c,d \} \} \\
&=(c,d)
\end{align}
$$



>==Definition 1.2.6==.Suppose A and B are sets. Then the Cartesian product of A and B, denoted A×B, is the set of all ordered pairs (a,b), where a is in A and b is in B.
$$
A\times B=\{ (a,b)\mid a\in A \text{ and } b\in B \}
$$

For example, the Cartesian plane $\mathbb{R}^{2}$  is the Cartesian product of$\mathbb{R}$ and $\mathbb{R}$.
$$\mathbb{R}^{2}=\{ (x,y)\mid x \in \mathbb{R} \text{ and } y \in \mathbb{R} \}$$
How about triple?
$$
\mathbb{R}^{2}\times \mathbb{R}=\{ ((x,y),z)\mid x,y,z \in \mathbb{R} \}
$$
$$\mathbb{R}^{2}\times \mathbb{R}\neq \mathbb{R}\times \mathbb{R}^{2}\text{ because }((x,y),z)\neq(x(y,z))$$
$\mathbb{R}^{3}$ is actually $\mathbb{R}^{2}\times \mathbb{R}$ by convention

Suppose A and B are sets. Is A×B generally equals B×A?

==No==

the size/ cardinality / the number of element of a set A is denoted by |A|. For example, if A={2,4,5}, then |A|= 3.

Suppose A and B are finite sets. What is |A×B| in terms of |A| and |B| ?

==ordered n-tuple==

==string==

#### 1.3 The Language of relations and functions

Mathematical objects are related in various ways. For example, 1<2 and √2< π. Hence, the “less than” relation, denoted<, is a relation between the real numbers. The following gives a formal definition of mathematical relation.

>==Definition 1.3.1== Let A and B be sets. A relation R from A to B is a subset of A x B demoted by $R\subseteq A\times B$.
Given an ordered pair (x, y) in A x B, **x is related to y by R**, written x **R** y, iff (x, y) is in R. 
The set A is called the domain of R and the set B is called its co-domain.
$$
\text{x R y means that $(x,y)\in R$}
$$
$$
x \not R y\text{ means that (x,y)}\not\in R
$$

Arrow Diagram of a Relation Suppose R is a relation from a set A to a set B. The arrow diagram for R is obtained as follows:
1. Represent the elements of A as points in one region and the elements of B as points in another region.
2. For each x in A and y in B, draw an arrow from x to y if, and only if, x is related to y by R. Symbolically:

>==Definition 1.3.2==. A function F from a set A to a set B is a relation with domain A and co-domain B that satisfies the following two properties:
>1. For every element x in A, $x \in A$ there is an element y in B such that (x, y)$\in$F.
>2. For all elements x in A and y and z in B,
$$
\text{if }(x,y)\in F\text{ and }(x,z) \in F\text{  ,then y=z }
$$
it means  each element in A mapped to one unique element in B.

==Functions and relations on Sets of Strings== ^f551f4

>==Definition 1.3.3==. Suppose f is a function from A to B (denoted f : A→B ) and g is a function from C to D (denoted g : C→D ). Then f is equal to g, denoted f=g, iff A=C, B=D, and f(x) =g(x) for all x ∈ A

#### 1.4 The language of graph

### 
$\{ x:P(x) \}\equiv \{ x \mid P(x) \}$
Both : and | mean the same thing