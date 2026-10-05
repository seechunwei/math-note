
There are various type of number. In chapter 1 P1-P12 is applied for rational number and real number.

The set of natural number $\mathbb{N}$ is $\{ x\in 1,2,3,\dots \}$. Notice that some basic properties from P1-P12 does not apply for $\mathbb{N}$, for example P2 and P3 (additive inverse and additive identity)

From this point of view, $\mathbb{N}$ have many deficiency, but it has a important and basic property
1) Mathematical induction

Suppose $P(x)$ is a property or statement holds for the number x. The principle of mathematical induction state that $P(x)$ holds for all natural number $x$ provided that
1) P(1) is true
2) $P(n+1)$ is true whenever $P(n)$ is true

It is like a domino effect, $P(1)$ is true then by (2) $P(2)$ is true, again when $P(2)$ is true then $P(3)$ is true,....

For example [[Chapter 5 Sequences and Mathematical Induction#^34da58]]

It is a technique of proof nevertheless it didn't provide any insight about how the formula was discovered. 

Notice there other equivalent way of mathematical induction, A more precise formulation:
If $A\subseteq \mathbb{N}$  and 
1) $1\in A$
2) $k\in A\implies k+1\in A$
then, $A=\mathbb{N}$.

It seem to be a totally different statement but actually it is the same if we define $A=\{ n\in \mathbb{N}:P(n) \}$ is true. Thus if $A=\mathbb{N}$, then it means that $P(n)$ is true for every natural number.

let see the corresponding part of 2 statement

| Informal Statement with Properties                           | Rigorous Statement with Sets                                    |
| ------------------------------------------------------------ | --------------------------------------------------------------- |
| "The property holds for 1" (P(1) is true)                    | $1\in A$                                                        |
| "Whenever the property holds for k, it holds for k+1"        | Whenever $k\in A$, then $k+1\in A$                              |
| **Conclusion**: "The property holds for all natural numbers" | **Conclusion**: $A=\mathbb{N}$ (every natural number is in $A$) |
Another question how we show $\mathbb{N}\subseteq A$ to show that $A=\mathbb{N}$?

In problem 25 Spivak introduce a rigorous way to write the so on for $\{ 1,2,3,\dots \}$. Spivak uses this exact condition to _define_ what natural numbers are inside the real numbers(Defined natural number from real number):

Definition of a inductive set:
$S\subseteq \mathbb{R}$ is a inductive set if 
1) $1\in S$
2)  $k\in S\implies k+1\in S$ (For example $S=\{ x\in \mathbb{R}:x>0 \}$)

Definition of Natural number $\mathbb{N}$: 
$\mathbb{N}=\bigcap S$ where $S$ is all the inductive set. It means that $\mathbb{N}\subseteq S$ for all $S$. It is the smallest inductive set.

From the question, it is clear that $A\subseteq S$, thus it follow that $\mathbb{N}\subseteq A$, since $A\subseteq \mathbb{N}$ in hypothesis, it follow that $A=\mathbb{N}$.


There is another equivalent statement of mathematical induction which is Well Ordering Principle.

If $A\subseteq \mathbb{N}$ and $A\neq \emptyset$, then $\exists x\in A:x\leq a$ for all $a\in A$. ($A$ must have a smallest number)

Both of them can prove each other [[Well ordering principle]] and is the fundamental axiom of $\mathbb{N}$.

There is also second principle of mathematical induction which is strong induction or complete induction where to prove $P(n+1)$ not only rely on $P(n)$ but more than 1 step before.

What kind of statement suit using induction to prove?
Recursive definition, for example $n!$ is defined as product of $n$ and natural number less than $n$. It can be precisely expressed as
1) $1!=1$
2) $n!=n(n-1)!$

Notice (1) is about the starting point and (2) is about the relationship of 2 consecutive step.

Spivak reveal why we need calculus and function 
1) The Dilemma: A Hole in our Axiom System

In chapter 1 we have P1-P12, and we use these axiom to prove that "There is no rational number $x\in \mathbb{Q}$ such that $x^{2}=2$." 

But P1-P12 is not only applied for $\mathbb{Q}$ it is also applied for $\mathbb{R}$, but we use a property of $\mathbb{Q}$ to prove the statement which is every number can be express as quotient of 2 integer. 

But with the thing we know at this stage, we cannot even prove that a real number $\sqrt{ 2 }$ exists. There must be some property that $\mathbb{R}$ holds but $\mathbb{Q}$ doesn't hold.

2)  The Tempting "Band-Aid" and Why It Fails
Why not we just add a property: Every positive number has a n-root?

Suppose we want to find the solution of $x^{5}+x+1=0$. 
- At $x=-1$, the expression equal to $-1$
- At $x=0$, the expression equals $1$ 

Intuition tell us there must be somewhere between $-1$ and $1$ that the curve cross 0 (Continuity). And that solution is cannot be written using $n-th$ root by **Abel-Ruffini Theorem**.

There is a fundamental difference between $\mathbb{Q}$ and $\mathbb{R}$
- The rational numbers $\mathbb{Q}$ on the number line are full of gaps (a hole at $\sqrt{ 2 }$, a hole at $\pi$, a hole at the root of $x^{5}+x+1$)
- The real number $\mathbb{R}$ have no holes.


