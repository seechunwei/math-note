### 4.1 Direct Proof and Counterexample I: Introduction

One of the best ways to think of a mathematical proof is as a carefully reasoned argument to convince a skeptical listener (often yourself) that a given statement is true. Imagine the listener challenging your reasoning every step of the way, constantly asking, “Why is that so?” If you can counter every possible challenge, then your proof as a whole will be correct.

A direct proof is a way of showing the truth or falsehood of a given statement by a straightforward combination of established facts, usually axioms, existing lemmas and theorems, without making any further assumptions.

Assumptions
-  Law of basic algebra
- three properties of equality
1) $A=A$
2) if $A=B$, then $B=A$
3) if $A=B$ and $B=C$ , then $A=C$
- Principle of substitution : For all objects A and B, if A=B, then we may substitute B wherever we have A.
- The set of all integers is closed under addition, subtraction, and multiplication. This means that sums, differences, and products of integers are integers.


==Definition 4.1.1== An integer n is even if, and only if, n equals twice some integer. An integer n is odd if, and only if, n equals twice some integer plus 1.
$$
\text{n is even}\Leftrightarrow n =2k\text{ for some integer k}
$$
$$
\text{n ia old} \Leftrightarrow n =2k+1 \text{ for some integer k}
$$
$$
\forall n,if \ n\ is\ even,\ then \ n =2k \text{ for some integer 2k}
$$
Noted that the definition state a if and only if relation, it means that you can deduce an integer n is even knowing that n have the form $n =2k$ . Conversely, you can deduce an integer n have the form $n =2k$ knowing that n is even.

The particular names used for the variables have no meaning themselves and are freely replaceable by other names. For example, you can substitute any symbols you like in place of n and k in the definitions of even and odd without changing the meaning of the definitions.

==Definition 4.1.2== An integer n is prime if, and only if, $n >1$ and for all positive integers r and s, if $n =rs$, then either r or s equals n. 
An integer n is composite if, and only if, $n >1$ and $n =rs$ for some integers r and s with $1<r<n$ and $1<s<n$.
$$
\forall r,s \in Z^{+}, n =rs\to (r=1 \text{ and } s=n) \oplus(r=n \text{ and }s=1)
$$

$$
\exists r,s \in \mathbb{Z}^{+},n =rs \text{ and } 1<r<n \text{ and } 1<s<n
$$

For all because there is only two possibility $r,s \in \{ 1,n \}$ , note that the negation of the predicate is $1<r<n$ and $1<s<n$

In proving an universal statement above, we can use without loss of generality (WLOG) to show only one possibility for example $r=1$ and $s=n$ (it means that we assume one case because all others are equivalent or symmetric. Exp: $a<b$ or $b<a$)



#### Proving Existential Statements
$$
\exists x \in D \text{ such that }Q(x)
$$

The statement is only true when Q(x) is true for at least one x in D

Constructive proofs of existence.
 1) Find an x (witness) in D that makes Q(x) true. 
 2) Another way is to give a set of directions for finding such an x.  

How it works?
==Existential generalization== It says that if you know a certain property is true for a particular object, then you may conclude 
that “there exists an object for which the property is true.”
	it is not an if and only if relation because 
	the converse is not true, there exists an object for which the property is true doesn't implies that the property is true for a particular object, because we don't know what is the particular object that make it true

there exists a such that P(x) hold ->P(a) is wrong


A nonconstructive proof of existence showing either:
1)  that the existence of a value of x that makes Q(x) true is guaranteed by an axiom or a previously proved theorem or 
2) that the assumption that there is no such x leads to a contradiction

==Existential Instantiation==
	If the existence of a certain kind of object is assumed or has been deduced, then it can be given a name, as long as that name is not currently being used to refer to something else in the same discussion.

For example suppose m is an even integer. By definition we know that m is equal to twice some integer. By existential instantiation, we can let k denote the some integer.

We can use existential instantiation when we want to prove existential statement by non-constructive proof. We can give a name to the existence of element based on assumption even though we don't know the particular candidate for the element.

#### Disproving Universal Statements by Counterexample
$$
\forall x \in D, P(x)\to Q(x)
$$

Showing that this statement is false is equivalent to showing that its negation is true.
$$
\exists x \in D,P(x)\land \neg Q(x)
$$

To disprove a statement of the form “,$\forall x \in D, P(x)\to Q(x)$” find a value of x in D for which the hypothesis P(x) is true and the conclusion Q(x) is false. Such an x is called a counterexample.


#### Proving Universal Statements

$$
\forall x \in D, P(x)\to Q(x)
$$

1) if the domain is a finite set, we can use ==method of exhaustion==
	We prove Q(x) is true for all the element in the set that satisfy P(x)

2) Generalizing from the Generic Particular
	To show that every element of a set satisfies a certain property, suppose x is a particular but arbitrarily chosen element of the set, and show that x satisfies the property.


The point of having x be arbitrarily chosen (or generic) is to make a proof that can be generalized to all elements of the domain. The word generic means “sharing all the common characteristics of a group or class.” Thus everything you deduce about a generic element x of the domain is equally true of any other element of the domain.


1) Whenever you want to write a prove always think what is the starting point "What am I supposing?" 
2)  Then ask yourself, “What conclusion do I need to show in order to complete the proof?”
3) Use the definition and law to complete it



$$
\forall x \in D,P(x)\to Q(x)\equiv \forall \{x \in D \mid P(x)  \},Q(x)
$$

==Theorem 4.1.1== The sum of any two even integers is even.
Suppose m and n arbitrary particular even integer. By definition of even, $m=2r$ and $n =2s$ for some integer r and s. Then
$$
\begin{align}
m+n&=2r+2s \text{  by substitution} \\
&= 2(r+s) \text{  by distributive law} 
\end{align}
$$
//We want to show that $m+n =2(\text{ for some integer})$ . Thus, by existential instantiation we can name the integer as $t$. 

Let $t=r+s$ . Note that $t$ is an integer because it is a sum of integers. Hence,
$$
m+n =2t \text{ where t is an integer}
$$
It follow by definition of even that $m+n$ is even.


Note that It's double directions  
The definition of even number is a iff relation  
So at first by definition we use the $\to$ to show that m,n=2(some integer), and then after some multiplication and substitution we use the $<-$ part to show that m+n is even


### The method of exhaustion 
Let $S=\{ 0,1,2 \}$ and ley $n \in S$. Prove that if $\frac{n^{2}+n-6}{2}$ is odd, then $\frac{2n^{3}+3n^{2}+n}{6}$ is even

Proof:
Let $n \in S$ such that $\frac{n^{2}+n-6}{2}$ is odd. 
Case 1 $n =0$
$\frac{0^{2}+0-6}{2}=-3$ which is odd. $\frac{2(0)^{3}+3(0)^{2}+0}{6}=0$ which is even. Thus, the statement is true.

Case 2: $n ={1}$
$\frac{1^{2}+1-6}{2}=-2$ which is even. Thus, the statement is vacuously true.

Case 3: $n =2$
$\frac{2^{2}+2-6}{2}=0$ which is even. Thus, the statement is vacuously true.

In either cases, the statement is true. Thus, it follow that the statement is true for $n \in S$.

==Exmaple 2==
Let $A=\{ n \in \mathbb{Z}:n> 2 \text{ and n is odd}\}$ and $B=\{ n \in \mathbb{Z}: n<11 \}$. Prove that if $n \in A\cap B$, then $n^{2}-2$ is prime.

Proof
Since $n \in A\cap B$, it follow that $n \in \{ 3,5,7 \}$. 

Case 1: $n =3$
$3^{2}-2=7$ which is prime.

Case 2: $n =5$
$5^{2}-2=23$ which is prime.

Case 3: $n =7$
$7^{2}-2=47$ which is prime.

In either case the statement is true.
