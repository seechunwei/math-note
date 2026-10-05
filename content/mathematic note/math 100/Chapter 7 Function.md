Definition 
Suppose $X$ and $Y$ are sets.
A function $f$ from X to Y is a relation $f$ from $X$ to $Y$ such that for every $x \in X$, there exists a unique $y \in Y$ such that $(x,y) \in f$. This unique $y$ for each $x$ is denoted by $f(x)$.

The set X is the domain of f and Y the codomain of f. We write f : X →Y to indicate the domain and codomain of f. The element f (x) is called the image of x under f. 

The two part of definition of function
1) assignment (we need to assign all the element in domain to an element )
2) uniqueness 
$$\text{If } x = y, \text{ then } f(x) = f(y)$$
Does that mean the cardinality of codomain must be at least the same size as domain? No because many $x \in dom(f)$ can map to one same $y\in rng(f)$ .

But if $A$ and $B$ are bijection under f, we can conclude $|A|=|B|$. For example $2\mathbb{N}$ and $\mathbb{N}$

Consider the example which map $\mathbb{R}$ to $\mathbb{Z}$. 
$f:\mathbb{R}\to \mathbb{Z}$ where 
$$f(x) = \lfloor x \rfloor$$
The one way to see whether if it is a function is by visualizing the function in a Cartesian plane. Assignment: we see the continuity of function(Not necessary check for the domain and codomain )
For example, $f:\mathbb{R}\to \mathbb{R}$ where $f(x)=\dfrac{1}{x}$
Since we cannot defined $\dfrac{1}{0}$. We couldn't map $0$ to $y \in \mathbb{R}$ . Thus it is not a function.

But what if we define our domain to be the set $\mathbb{R} \setminus \{  0\}$?

uniqueness:  
Definition of image
Suppose $f:X\to Y$ and $A\subseteq X$.
$$
f[A]=\{ y \in Y\mid y=f(x) \text{ for some }x \in A \}
$$
(vertical line test)


Definition of range
The range of $f$ is the set of all images defined by
$$
rng(f)=\{ y \in Y | y=f(x) \text{ for some } x \in X \}
$$

What is the difference between image and range?
1) The domain of f range is the whole set of domain, it means that you map the whole domain to codomain
2) Image: you map a subset from domain to codomain

### Identity function
Suppose X is a set and $I_{x}:X\to X$ is defined by $I_{x}(x)=x$ for all x ∈ X. Then $I_{x}$ is called the identity function on $X$.

Suppose $f:\mathbb{Q}\to \mathbb{Z}$ is defined by
$$
f\left( \frac{m}{n} \right)=m \text{ for all integers m and n with }n\neq 0
$$
is f a well-defined function?
$f\left( \frac{1}{2} \right)=1, f\left( \frac{2}{4} \right)=1$ .


Definition of preimage
Suppose $f:X\to Y$ and $A\subseteq Y$
$$
f ^{-1}[A]=\{ x \in X | f(x) \in A\}
$$

Preimage: we map a subset of codomain to domain.

Preimage is always exists while inverse function may not exists.
$f^{-1}\circ f[A]\neq f\circ f^{-1}[A]$
$$
f[A]=\emptyset \text{ iff }A\not\subseteq X
$$

If we take an image of  a set and we take the preimage of the image. Does it equal to the original set? Not always because different input can have same output.

Suppose the function $f:\mathbb{Z}\to \mathbb{Z}$ is defined by
$$
f(n)=n^{2} \text{ for all }n \in \mathbb{Z}
$$
if a function is one to one correspondence we can say for each element in codomain , it have a unique preimage. If a function is not a bijection thus it exists an element in codomain which does not have preimage denoted by $f ^{-1}[Y]=\emptyset$ iff $Y\cap rng(y)=\emptyset$.

### The operation of image and preimage
1) 
$$
f[A\cap B]\neq f[A]\cap f[B]
$$
This is because of the Collision. The collision happen when 2 different subset in codomain that have no common intersection but then map to same image. because multiple inputs are allowed to have the same output.

It also mean a thing the if $x$ is not related to $x_{1}$ does that mean their image is not related? because the definition only say if x is related then y must be related.

Let's use a simple function that is not "One-to-One" (Injective).

- **Function:** $f(x) = x^2$
    
- **Set A:** $\{-2\}$
    
- **Set B:** $\{2\}$


Now let's calculate both sides:

**Left Side: $f[A \cap B]$**

1. First, find the intersection of inputs: $A \cap B$.
    
    Since $\{-2\}$ and $\{2\}$ have no common elements, $A \cap B = \emptyset$ (Empty Set).
1. Apply the function:
    
    $$f[\emptyset] = \emptyset$$
**Right Side: $f[A] \cap f[B]$**

1. Find the image of A: $f(-2) = 4$. So, $f[A] = \{4\}$.
    
2. Find the image of B: $f(2) = 4$. So, $f[B] = \{4\}$.
    
3. Find the intersection of the images:
    
    $$\{4\} \cap \{4\} = \{4\}$$
    

The Result:

$$\emptyset \neq \{4\}$$


2) 
$$
f[A\cup B]=f[A]\cup f[B]
$$
Proof:
Suppose $y$ is an arbitrary element in $f[A\cup B]$. By definition $y=f(x)$ for some $x \in A\cup B$.  Thus. $x \in A$ or $x \in B$
Case 1: $x \in A$
$y \in f[A]$ . Thus, $y \in f[A]\cup f[B]$

Case 2: $x \in B$
$y \in f[B]$. Thus, $y \in f[B]\cup f[A]$

In either case, $y \in f[B]\cup f[A]$. Thus, $f[A\cup B]\subseteq f[B]\cup f[A]$

Conversely, suppose $y$ is an arbitrary element in $f[A]\cup f[B]$. Thus, $y \in f[A]$ or $y \in f[B]$. 

Case 1: $y \in f[A]$
Then $y=f(x)$ for some $x \in A$, it follow that $x \in A\cup B$ . Thus, $y \in f[A\cup B]$

Case 2: $y \in f[B]$
Then $y=f(x)$ for some $x \in B$, it follow that $x \in A\cup B$. Thus, $y \in f[A\cup B]$.

In either case $y \in f[A\cup B]$. Hence, $f[A]\cup f[B]\subseteq f[A\cup B]$ . Since, $f[A\cup B]\subseteq f[A]\cup f[B]$ and $f[A]\cup f[B]\subseteq f[A\cup B]$. Thus, $f[A\cup B]=f[A]\cup f[B]$


3) 

$$
f ^{-1}[A\cup B]=f ^{-1}[A]\cup f ^{-1}[B]
$$
it is true


4) 
$$
f ^{-1}[A\cap B] = f ^{-1}[A]\cap f ^{-1}[B]
$$
This is true because of the uniqueness of image. Even though output can have many preimage but their preimage will not intersect if the output is not same.

For this statement the core proof lies in
$$
f ^{-1}[A]\cap f ^{-1}[B]\subseteq f ^{-1}[A\cap B]
$$
For the another side we can just use the definition of "and" to prove. The statement is equivalent to this statement if $a=b$ then $f(a)=f(b)$. 
if $f(a)\neq f(b)$ then $a\neq b$ (This is the core idea)

We suppose $x \in f ^{-1}[A]$ and $x \in f ^{-1}[B]$. By definition $y_{1} \in A$ and $y_{2} \in B$. By the uniqueness of image we can conclude $y_{1}=y_{2}$ .Thus there exist a $y \in A \cap B$.

What if we want to prove 
$$
f[A]\cap f[B]\subseteq f[A\cap B]
$$
We suppose an arbitrary element y in the set.
By definition $f(x_{1}) = y$ for $x_{1} \in A$ and $f(x_{2})=y$  for $x_{2} \in B$.  But there is no evidence that show $x_{1}=x_{2}$.


Function is one to one function (injective) when it satisfy the condition

$$
f(a)=f(b)\implies a=b
$$
or 
$$
a\neq b\implies f(a)\neq f(b)
$$

### Equality between function
Suppose f is a function from A to B and g is a function from C to D. Then f is equal to g, denoted f = g, iff A = C, B = D, and f (x) = g(x) for all x ∈ A.

Suppose $f:\mathbb{R}^{-}\to \mathbb{R}$ and $g:\mathbb{R}^{-}\to \mathbb{R}$ are defined by $f(x)=-x$ and $g(x)=\sqrt{ x^{2} }$ for all $x \in \mathbb{R}^{-}$. Does f = g?

$dom(f)=dom(g)$ and $codom(f)=codom(g)$. 
$f(x)=g(x)$ for all $x \in \mathbb{R}^{-}$ , thus $f=g$.
By definition $f(x)=|x|$ and $g(x)=|x|$ .

$(f+g)(x)=f(x)+g(x)$ for all $x \in \mathbb{R}$. Show that $f+g=g+f$. 

Since $f(x)$ and $g(x)$ have same domain and codomain thus $f+g$ and $g+f$ have the same domain and codomain . It is because the new function is form by map the $x \in \mathbb{R}$ to $g(x)+f(x)$ or $f(x)+g(x)$ which is also in $\mathbb{R}$. (Since $f(x)$ and $g(x)$ are mathematical object which have the commutativity) . Thus , it is suffice to show $(f+g)(x)=(g+f)f(x)$ for all $x \in \mathbb{R}$.
$$
(f+g)(x)=f(x)+g(x)=g(x)+f(x)=(g+f)(x)
$$

Does $(f+g)(x)=(g+f)(x)$ always true? What if set $x$ is a sequence of letter where the order is important.
Consider the function below

- Let $x$ be the set of string.
- $f(x) = \text{"Hello"}$
- $g(x) = \text{"World"}$

Using the definition:

$$(f+g)(x) = f(x) + g(x) = \text{"HelloWorld"}$$

If we swap the order:

$$(g+f)(x) = g(x) + f(x) = \text{"WorldHello"}$$
The commutativity that matters is located in the **Codomain** (the destination set), not the Domain (the input set).

But notice that the set of $\mathbb{R}$ and binary operation $+$ is a group so if we change the $codom(f)$ and $codom(g)$ to $\mathbb{Z}$ also work

![[Pasted image 20260109113840.png]]

## 7.2 Injections and Surjections
Suppose f is a function from X to Y. We say that f is one-to-one (or injective) iff for all elements a and b in X
if $f(a)=f(b)$ then $a=b$.

How to disprove injectivity?
Let $f:\mathbb{Z}\to \mathbb{Z}$ be defined by $f(x)=x^{2}$ for all $x \in \mathbb{Z}$. Show that $f$ is not one-to-one.
By definition f is one to one iff $f(a)=f(b)\to a=b$.
To disprove this we need to find a counter example. 
Notice that $f(2)=4=f(-2)$ and $2\neq-2$. Thus, f is not one to one.


How to show injectivity?
To show that a function f is one-to-one, we suppose a and b are arbitrary elements from the domain of f such that f(a) = f(b) and then show that a = b.

Let $f:\mathbb{R}^{-}\to \mathbb{R}$ be defined by $f(x)=x^{2}$ for all $x \in \mathbb{R} ^{-}$. Show that f is one-to-one.
Suppose $a$ and $b$ are arbitrary element in $\mathbb{R}^{-}$ such that $f(a)=f(b)$. We need to show $a=b$.
$$
\begin{align}
a^{2}&=b^{2} \\
\sqrt{ a^{2} }&=\sqrt{ b^{2} } \\
|a|&=|b| \\
-a&=-b \text{ since a,b<0}\\
a&=b
\end{align}
$$
Therefore, $f$ is one to one.

$\sqrt{ a^{2} }=|a|$

Suppose $f:\mathbb{R}\to \mathbb{R}$ and $g:\mathbb{R}\to \mathbb{R}$ are both one to one functions. Must $f+g$ be one to one. No
Let consider $f(x)=x$ and $g(x)=-x$.
Thus, $(f+g)(x)=0$ for all $x \in \mathbb{R}$.


### (Optional) Operation
Suppose $A$ is a set and $n$ is a positive integer. An $n-ary$ (unary, binary,...) operation on $A$ is a function from the Cartesian product $A^{n}$ into A.
Imagine something like this 
$f:\mathbb{Z}^{2}\to \mathbb{Z}$ defined by $f((x,y))=z$ where $z=x+y$ for all $(x,y)\in \mathbb{Z}^{2}$. f is a binary operation on $\mathbb{Z}$.

for simplicity, $f((x,y))$ is normally written as $f(m,n)$.

### Group
Based on the image you provided, here is an explanation of what a **Group** is, breaking down the formal definition into plain English.

### The Big Idea: The "Undo" Button

In simple terms, a **Group** is a collection of things (numbers, actions, rotations) where you can combine any two of them to get another one, and—crucially—**you can always undo whatever you did.**

Think of a Group as a game with strict rules about fairness and reversibility.

---

### Decoding the Definition (from your slide)

Your image lists a **Set $A$** (the collection of things) and a **Binary Operation $\bullet$** (the rule for combining them). For a set to be a "Group," it must satisfy these three specific rules:

#### 1. Associativity (The "Grouping" Rule)

> _Formal:_ $(a \bullet b) \bullet c = a \bullet (b \bullet c)$

**What it means:** The order in which you perform the calculations doesn't matter _as long as the sequence stays the same_. You don't need parentheses.

- **Example:** $(2 + 3) + 4$ is the same as $2 + (3 + 4)$. Both equal 9.
    

#### 2. Identity Element (The "Neutral" Move)

> _Formal:_ There exists $e \in A$ such that $e \bullet x = x$ and $x \bullet e = x$.

**What it means:** There must be a special element in the set that "does nothing" when you combine it with others.

- **Example (Addition):** The number **0** is the identity. If you add 0 to anything ($5 + 0$), it stays the same ($5$).
    
- **Example (Multiplication):** The number **1** is the identity. ($5 \times 1 = 5$).
    

#### 3. Inverse Element (The "Undo" Button)

> _Formal:_ For every $x$, there exists a $y$ such that $x \bullet y = e$ and $y \bullet x = e$.

**What it means:** For every element, there must be a "partner" that cancels it out and brings you back to the Identity (the neutral state).

- **Example (Addition):** If you have **5**, you must have **-5**. When you combine them ($5 + (-5)$), you get back to **0** (the Identity).
    

---

### Answering the "Food for Thought" (Integers $\mathbb{Z}$)

The slide asks you to verify if the set of Integers ($\mathbb{Z}$) with Addition ($+$) forms a group. Let's check the rules:

1. **Operation:** Can we add two integers? Yes. $2 + 5 = 7$ (still an integer).
    
2. **Associativity:** Does $(a+b)+c = a+(b+c)$? **Yes.** Addition is always associative.
    
3. Identity: Is there a "do nothing" number in the integers? Yes, 0.
    
    $$x + 0 = x$$
    
4. Inverse: If I pick an integer $x$, is there a number I can add to get back to 0? Yes, $-x$.
    
    $$5 + (-5) = 0$$
    
    Since negative numbers are part of the Integers ($\mathbb{Z}$), the inverses exist inside the set.
    

**Verdict:** ✅ **Yes, $(\mathbb{Z}, +)$ is a group.**

---

### A Counter-Example (When it breaks)

Let's try the **Integers ($\mathbb{Z}$)** with **Multiplication ($\times$)**. Is this a group?

1. **Identity:** The identity is **1** (since $x \cdot 1 = x$).
    
2. Inverse: If I have the number 2, what do I multiply it by to get back to 1?
    
    $$2 \cdot (?) = 1$$
    
    I would need $\frac{1}{2}$.
    
3. The Problem: Is $\frac{1}{2}$ an integer? No.
    
    The inverse does not exist inside the set.
    

**Verdict:** ❌ **The Integers are NOT a group under multiplication.**

### Summary

A group is simply a system where you can **combine** things, **do nothing** (Identity), and **reverse** things (Inverse).

Next Step:

Would you like to explore why the set of Rational Numbers ($\mathbb{Q}$) almost works for multiplication, but fails for exactly one number (Zero)?

Mathematicians define **Groups** because they realized that widely different mathematical systems (numbers, geometric shapes, matrices, encryption) all share the exact same underlying "skeleton."

Instead of studying these systems one by one, they defined the "Group" to study the skeleton itself. If you prove a fact about Groups, you instantly prove it for _everything_ that is a group.

Here are the three main reasons why the definition exists:

### 1. To Capture the Concept of "Symmetry"

This is the most powerful intuition for groups. A group is the mathematical way to describe **symmetry**.

Think of a Square. What can you do to it so it still looks like a square in the same position?

- You can rotate it 90°.
    
- You can flip it horizontally.
    
- You can do nothing (Identity).
    
- You can undo a rotation (Inverse).
    

If you collect all these "actions" together, they satisfy the definition of a Group (specifically, the _Dihedral Group_).

Mathematicians defined groups to quantify how "symmetrical" an object is.

- A circle has an infinite continuous group of symmetries.
    
- A butterfly has a small group of symmetries (Identity and one Flip).
    
- A chaotic scribble has only the Identity group (no symmetry).
    

### 2. The "Write Once, Run Everywhere" Philosophy

Before Group Theory, mathematicians solved problems in isolation:

- "How do integers behave?"
    
- "How do permutations of a deck of cards behave?"
    
- "How do rotations of a sphere behave?"
    

They realized these distinct problems followed the same rules (Associativity, Identity, Inverses). By defining a **Group**, they created a unified language.

Example:

If you prove the statement: "In any group, the inverse of a product is $(a \bullet b)^{-1} = b^{-1} \bullet a^{-1}$", you don't need to re-prove it for matrices, or for numbers, or for Rubik's cubes. You know it is true for all of them automatically.

### 3. To Solve Impossible Equations (History)

Historically, this is actually where groups came from. In the 1830s, a teenager named **Évariste Galois** invented Group Theory to answer a specific question:1

> _"Why is there a quadratic formula for $x^2$, cubic for $x^3$, and quartic for $x^4$, but **no formula** for $x^5$?"_

He realized that the "symmetry" of the roots of the equation formed a Group.

- If the group is "solvable" (a specific group property), you can write a formula.
    
- If the group is complex/messy (like the group for $x^5$), you cannot write a formula.
    

He translated a problem about **formulas** into a problem about **structure (groups)**.

---

### Summary: The "Interface" Analogy

If you code, think of a Group as an **Interface** in programming.

- It doesn't tell you _what_ the object is (it could be an integer, a matrix, or a rotation).
    
- It tells you _what you can do_ with it (you can combine them, and you can undo them).
    

### Next Step

The "Symmetry of a Triangle" is the classic "Hello World" example of a group that is **not** commutative (where $a \bullet b \neq b \bullet a$). Would you like me to walk you through that to visualize why order matters?

- **Group:** Commutativity is **optional**.
    
- **Abelian Group:** A special type of group where commutativity **is** required.

### Surjections
Suppose f is a function from X to Y. We say that f is onto (or surjective) iff for every element y in Y, there exists an element x in X such that y = f(x)

To show that a function f is onto, we first suppose y is an arbitrary element in the codomain of f . Then we show that there exists an element x in the domain of f such that f(x) = y.

Let $f:\mathbb{Q}\to \mathbb{Q}$ be a function defined by $f(x)=4x-1$ for all $x \in \mathbb{Q}$ .Show that f in onto.

Suppose $y$ is an arbitrary rational number. 
Take $x=\dfrac{y+1}{4}$. Clearly, $x \in dom(f)$. Also, $f(x)=f\left( \frac{y+1}{4} \right)=4\left( \frac{y+1}{4} \right)-1=y$.



Suppose $f:\mathbb{R}\to \mathbb{R}$ is a function defined by
$$
f(x)=\begin{cases}
2x \text{ if }x\geq 0 \\
\frac{1}{x} \text{ if }x< 0
\end{cases}
$$


Suppose y is an arbitrary real number. 
Case 1:$y\geq 0$
Take $x=\dfrac{y}{2}$. Note that $x\geq 0$.Hence, $f\left( \frac{y}{2} \right)=2\times \frac{y}{2}=y$

Case 2: $y<0$
Take $x=\dfrac{1}{y}$. Note that $x<0$. Hence, $f(x)=f\left( \frac{1}{y} \right)=y$

In either case, there exists a real number x (in the domain) such that f (x) = y. Therefore, f is onto.




#### Bijection
Suppose f is a function from X to Y. We say that f is a one-to-one correspondence (or bijection) iff f is both one-to-one and onto.

Inverse function
Suppose $f:X\to Y$ is a one to one correspondence. Define $g:Y\to X$ by
$$
g(y)=x \iff f(x)=y, \text{ for all }y \in Y
$$
$f-1(y)=x$

Suppose y is an arbitrary element in Y. Since f is onto, $y=f(x)$ for some $x \in X$. Hence, by definition of g, y is sent to x under g. 

Suppose $y=f(x)$ and $y=f(x')$. Since f is one-to-one $f(x)=f(x')\to x=x'$. Hence $y=f(x)$ for a unique $x$.

Therefore, $x$ is the unique image of y under g. We conclude that g is well defined function.

![[Pasted image 20260109180613.png]]

Let $f:[1,\infty]\to[3,\infty]$ be a function defined by
$$
f(x)=2x+1 \text{ for all }x \in[1,\infty]
$$
a)
One to one
Suppose $x$ and $x'$ are arbitrary real number for which $x,x'\geq 1$ such that $f(x)=f(x')$.
$$
\begin{align}
2x+1&=2x'+1 \\
2x&=2x' \\
x&=x'
\end{align}
$$

Therefore, $f(x)=f(x')\to x=x'$. Thus, by definition f is one-to-one.

Onto
Suppose y in an arbitrary element in $[3,\infty]$. Thus, take $x= \dfrac{y-1}{2}$ . Since $y>3$, $x \in [1,\infty]$. Therefore, $f(x)=f\left( \frac{y-1}{2} \right)=2\left( \frac{y-1}{2} \right)+1=y$

Therefore, f is onto.

b) Find $f ^{-1}$
![[Pasted image 20260109182205.png]]

Why we need to know that $rng(f ^{-1})=dom(f)$ because when we find inverse function, sometimes we need restrict the $dom(f)$ to be equal to $rng(f ^{-1})$ 

Consider the question below
Let $f:\mathbb{R} ^{-}\to \mathbb{R}^{+}$ be a function defined by
$$
f(x)=x^{2} \text{ for all }x \in \mathbb{R}^{-}
$$
a)Show $f$ is one-to-one and onto.
b) Find $f ^{-1}$

a)
One-to-one 
Suppose $a$ and $b$ are arbitrary negative real number such that $f(a)=f(b)$. Thus,
$$
\begin{align}
a^{2}&=b^{2} \\
\sqrt{ a^{2} }&=\sqrt{ b^{2} } \\
|a|&=|b| \\
-a&=-b \text{ (a,b<0)}\\
a&=b
\end{align}
$$
Therefore, f is one-to-one.

Onto
Suppose $a$ is an arbitrary positive real number. Thus, take x=$-\sqrt{ y }$ because $x<0$ . Thus, $f(x)=f(-\sqrt{ y })=(-\sqrt{ y })^{2}=y$
. Therefore, $f$ is onto.


Although the surjectivity of a function, by definition, does depend on the codomain, the nature of the function itself is mostly irrelevant to the codomain. What we mean is that most interesting properties of a function (for example, injectivity, continuity, and differentiability) depend on the domain of the function and its rule of mapping.

If a function $f$ is one-to-one but not onto, we can just shrink to codomain while the domain still the same. Precisely, $g:X\to rng(f)$ defined by

$$
g(x)=f(x) \text{ for all }x \in X
$$


### Section 7.3 Composition of Functions
Suppose $f:X\to Y$ and $g:Y'\to Z$ are function such that $rng(f)\subseteq Y'$. Define a new function $g \circ f:X\to Z$ by 
$$
(g\circ f)(x)=g(f(x)) \text{ for all }x \in X
$$
The function $g \circ f$ is called the composition of f and g.  We first find the image of $x$ under f, followed by the image of $f(x)$ under g. 

The composition of f and g is defined if and only if rng(f ) ⊆ dom(g).


>Alternative Definition of Composition
>$dom(g \circ f)=\{ x \in dom(f)|f(x) \in dom(g) \}$


==Theorem==
Suppose $f:X\to Y$ is a one-to-one and onto function. Then
$$
\begin{array}
\ f ^{-1} \circ f=I_{x} \\
f \circ f ^{-1}=I_{y}
\end{array}
$$
By definition, $f ^{-1}f:X\to X$ and $I_{x}: X\to X$. It suffices to show that $(f ^{-1} \circ f)(x)=I_{x}(x)$  for all $x \in X$.

Suppose $x$ is an arbitrary element of $X$. Let $y=f(x)$. By definition of $f ^{-1}$, we know that $f ^{-1}(y)=x$.
Therefore, $(f ^{-1}\circ f)(x)=f ^{-1}(f(x))=f ^{-1}(y)=x=I_{x}(x)$


==Theorem (Associativity)==^122
Suppose $f:Y\to Z$, $g:X\to Y$, and $h:W\to X$. Then, ^4266f3
$$
(f \circ g)\circ h=f \circ(g \circ h)
$$
Proof:
Notice that $(f \circ g) \circ h \text{ and } f \circ(g \circ h)$ are function from $W$ to $Z$.
Suppose $x$ is an arbitrary element in $W$. Thus
$$
\begin{align}
(f \circ g)\circ h&=(f \circ g)(h(x)) \\
&=f(g(h(x))) \\
&=f((g \circ h)(x)) \\
&=(f \circ(g \circ h))(x)
\end{align}
$$
The composition of function is a group, it is same as addiction, no matter how to operate there is last operation which include 2 assignments. 

==Theorem(One-to-one)==
Suppose $f:X\to Y$ and $g:Y\to Z$ are both one-to-one functions. Then $g \circ f$ is one-to-one.

Proof:
Suppose a and $b$ are arbitrary element in X such that $(g \circ f)(a)=(g \circ f)(b)$ . By definition,
$$
\begin{align}
g(f(a))&=g(f(b))
\end{align}
$$
Since g is one-to-one, we can conclude that $f(a)=f(b)$. Since f is one-to-one, we can conclude that $a=b$. Thus, $g \circ f$ is one-to-one.

==Theorem(onto)==
Suppose $f:X\to Y$ and $g: Y\to Z$ are onto function. Then, $g \circ f$ is onto.

Proof:
Suppose $z$ is an arbitrary element in $Z$. Since $g$ is onto, $z=g(f(x))$ for some $f(x)\in Y$. Since, $f$ is onto, let $y=f(x)$ for some $x \in X$.

Now,$(g \circ f)(x)=g(f(x))=g(y)=z$ Therefore, we can conclude that $g\circ f$ is onto.

==Corollary==
Suppose f : X → Y and g: Y →Z are both one-to-one and onto. Then g ◦f is also one-to-one and onto.

==Theorem==
Suppose $f:X\to Y$ and $g:Y\to Z$. if $g \circ f$ is one to one, then f is one to one.

Proof:
Suppose $x$ and $x_{1}$ are arbitrary element in $X$ such that $f(x)=f(x_{1})$. Thus,
$$
g(f(x))=g(f(x_{1}))
$$
Since $g \circ f$ is one-to-one , thus it follow that $x=x_{1}$ . Therefore $f$  is one-to-one.

==Remark==
We want to prove f is one-to-one thus we assume a and b is in X such that $f(a)=f(b)$, and we need to prove $a=b$. Since $f(a)=f(b)$, $(g \circ f)(a)=(g \circ f)(b)$ . Thus, since $g \circ f$ is one-to-one $a=b$.


Why $g$ no need to be one-to-one?
It is because $g$ only map the $rng(f)$ to $rng(g)$. Thus, g can be many-to-one if other element in $dom(g)$ but not in $rng(f)$. Suppose $f:\mathbb{R}^{+}\to \mathbb{R}$ and $g:\mathbb{R}\to \mathbb{R}$

$f(x)=x$ and $g(y)=y^{2}$ . Clearly $g$ is not one-to-one because $g(1)=g(-1)$, and $1\neq-1$. But look carefully here $-1$ is in $dom(g)$ but never in $rng(f)$. Thus $g\circ f$ is still one-to-one. 

We say that g is restricted to range of f.

==Theorem==
Suppose $f:X\to Y$ and $g:Y\to Z$. If $g\circ f$ is onto, then g is onto.

Proof:
Suppose $z$ is an arbitrary element in $Z$. We need to show that $z=g(y)$ for some $y \in Y$. 

Since $g\circ f$ is onto , it follow that $z=g(f(x))$ for some $x \in X$. Let $y=f(x)$, thus $z=g(y)$ for some $y \in Y$. We conclude that g is onto.

If $g\circ f$ is onto, then $g$ is onto. Thus, this can only happen when $codom(g)$ have lesser element than $rng(f)$ . If not, we couldn't map the extra element in $codom(g)$ from  $rng(f)$,

### 7.4 Cardinality
Suppose A and B are any sets. We say that A has the same cardinality as B, denoted |A| = |B|, iff there is a bijection from A into B.

1) Reflexivity $|A|=|A|$;
2) Symmetry if $|A|=|B|$, then $|B|=|A|$
3) Transitivity if $|A|=|B|$ and , $|B|=|C|$, then $|A|=|C|$ 

---
A bijective function that map the domain to the same set of object (closure) with the operation composition is a group

$(f\circ g)\circ h=f\circ (g\circ h)$ (associative)
Identity function (neutral move)
Inverse function (undo move)

Any operation and object that is symmetry can be view as a bijective function with composition

For example Euclidean geometry
If you take a square and rotate it 90 degrees (let's call this bijection $R$), and then you flip it horizontally (let's call this bijection $F$), you have performed two operations in a row.In mathematics, doing one function and then another is function composition, written as $F \circ R$. Because the composition of any two bijections is always another bijection, combining any two symmetries always results in a third, valid symmetry.^123 ^5dd9d2