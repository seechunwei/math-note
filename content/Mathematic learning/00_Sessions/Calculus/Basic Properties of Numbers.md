# What is the most basis properties of number?

> [!theorem] P1 (Associative law for addition)
> If $a,b,$ and $c$ are any numbers, then
> $$
> a+(b+c)=(a+b)+c
> $$

### How about 4 number?

1) $((a+b)+c)+d$
2) $(a+(b+c))+d$
3) $a+((b+c)+d)$

Equality of (2) and (3) follow directly from P1, for (2) if we ignore $d$, then it is totally P1, for (3) we view $(b+c)$ as one term.

4) $a+(b+(c+d))$
5) $(a+b)+(c+d)$

$(4)=(3)$ follow from P1 by ignoring $a$. For (5), we view $(c+d)$ as one term and we add the first 2 term first.


### For $n =5$:
We can split into few cases
Case 1: $1+4$ $a+(b+c+d+e)$
There are 5 ways to sum up 4 term and 2 way to split $(4+1)$, so total $2\times 5=10$ ways.

Case 2: $2+3$ $(a+b)+(c+d+e)$
There are 2 way to sum up 3 term and 2 way to split it , so total $2\times 2=4$ ways

Total is 14 ways.

We split into $(k)+(n-k)$
For number 5, we have total 4 way to split it because $1\leq k\leq n-1$.

Even though each case is different when we have different $n$, but the component are the same.
So let $C_{k}$ represent the number of way to sum the first group $(k)$ and $C_{n-k}$ for second group $(n-k)$. 
Case 1:
$C_{1}=1$ and $C_{4}=5$, $1\times 5=5$ (Times 2 because 4+1 and 1+4)

Case 2:
$C_{2}=1$ and $C_{3}=2$ , $1\times 2=2$ (Times 2 because 2+3 and 3+2)

How about $n =4$?
Notice that $C_{2}\times C_{2}$ no need to times $2$, so it is not true that $\sum_{k=1}^{\frac{n-1}{2}}2C_{k}C_{n-k}$

The correct formula is 
$$C_{n}=\sum_{k=1}^{n-1} C_{k}\times C_{n-k}$$

Apply formula when $n =6$:
$C_{1}=1,C_{2}=1,C_{3}=2,C_{4}=5,C_{5}=14$

$$
\begin{align}
C_{6}&=(1\times 14)+(1\times 5)+(2\times 2)+(5\times 1)+(14\times 1) \\
&=42
\end{align}
$$

> [!theorem] Formal statement
> The way of summing up $n$ term by insert parathesis in any place denote by $C_{n}$ is a recursive formula:
> $$C_{n}=\sum_{k=1}^{n-1} C_{k}\times C_{n-k}$$


### How to prove?
Since it is recurrence (based on the $1\leq k\leq n-1$), thus it is suitable to use strong induction.

Proof:
Let $P(n)$ be the statement below:

$$
P(n):C_{n}=\sum_{k=1}^{n-1} C_{k}C_{n-k}
$$
For basis step, $P(2)$ is true because 

$$
\begin{align}
\sum_{k=1}^{1}C_{k}C_{n-k}&=C_{1}C_{1} \\
&=1=C_{2} 
\end{align}
$$

For inductive step, suppose $k$ is an arbitrary integer and suppose $P(k)$ is true for $2\leq k\leq n$.We need to show that $P(n+1)$ is true.

Notice that addition is a binary operator. Any valid full parenthesization is uniquely determined by its final (outermost) addition. Thus, we can split the summation term into 2 group

First group: Consists of first $k$ term where $1\leq k\leq n$
Second group: Consists of last $(n+1)-k$ term where $1\leq(n+1)-k\leq n$.

$$\underbrace{(x_1 + \dots + x_k)}_{\text{Left block of } k \text{ terms}} + \underbrace{(x_{k+1} + \dots + x_{n+1})}_{\text{Right block of } (n+1-k) \text{ terms}}$$

By induction hypothesis the number of way summing up first group is $C_{k}$ and second group is $C_{(n+1)-k}$. Since they are independent event, the Multiplication Principle yields $C_k C_{n+1-k}$ ways for a fixed $k$.

Since the choice of $k \in \{1, 2, \dots, n\}$ partitions all possible parenthesizations into $n$ disjoint sets, applying the Addition Principle gives:

$$C_{n+1} = \sum_{k=1}^{n} C_k C_{(n+1)-k}$$

By the Principle of Mathematical Induction (specifically structural induction on the size of the expression), the identity holds for all $n \ge 2$. $\blacksquare$

> [!theorem] Addition Principle:
> If task $A$ can be done in $m$ ways and task $B$ can be done in $n$ ways, and $A$ and $B$ **cannot be performed at the same time** (they share no common choices), then choosing to do task $A$ **or** task $B$ can be done in $m + n$ ways.


> [!theorem] Multiplication Principle:
> If a procedure can be broken down into two sequential steps where:
> 
> 1. Step 1 can be performed in $m$ ways, and
> 2. For _each_ of those choices, Step 2 can be performed in $n$ ways,
> then performing Step 1 **and then** Step 2 together can be done in $m \times n$ ways.


P1 can be generalize into $n$ term and prove at problem 24 using induction.

## Problem 24)

> [!definition]
> Let $a_{1}+\dots+a_{n}$ denote
> 
> $$
> a_{1}+(a_{2}+(a_{3}+\dots+(a_{n+1}+a_{n}))\dots)
> $$
> (This is right nested definition)



> [!question] 24(a)
> Prove that
> 
> $$
> (a_{1}+\dots+a_{k})+a_{k+1}=a_{1}+\dots+a_{k+1}
> $$
> (Prove right nested is equal to left nested)
> 

We use mathematical induction. Let $P(n)$ denote the statement below

$$
(a_{1}+\dots+a_{n-1})+a_{n}=a_{1}+\dots+a_{n}
$$

For basis step $P(2)$ is true because $(a_{1})+a_{2}=a_{1}+a_{2}$.

For inductive step, suppose $k$ is an arbitrary integer and suppose $P(k)$ is true for all $k$ where $2\leq k\leq n$. We need to show $P(n+1)$ is true.

$$
\begin{align}
(a_{1}+\dots+a_{n})+a_{n+1}&=(a_{1}+(a_{2}+\dots+a_{n}))+a_{n+1} && \text{(Apply definition for first n terms)}\\
&= a_{1}+((a_{2}+\dots+a_{n})+a_{n+1}) &&\text{(By inductive hypothesis)} \\
&=a_{1}+(a_{2}+\dots+a_{n+1}) &&\text{(By IH)}\\
&= a_{1}+(a_{2}+(a_{3}+\dots+(a_{n}+a_{n+1}))) \\
&=a_{1}+\dots+a_{n+1}
\end{align}
$$

Thus,  $P(k)$ is true for all integer $k\geq 2$. $\blacksquare$.

Why i cannot do at the first place? Because i didn't know it is right nested and left nested, i thought it must apply to every term, but actually we can see $a_{2}+\dots+a_{n}$ as one term. So we just apply right nested for 3 terms.

> [!question] 24(b)
> Prove that if  $n\geq k$, then
> 
> $$
> (a_{1}+\dots+a_{k})+(a_{k+1}+\dots+a_{n})=a_{1}+\dots+a_{n}
> $$
> 

Proof: Let $P(n)$ denote the statement above.

For basis step $P(2)$ is true because $(a_{1})+(a_{2})=a_{1}+a_{2}$.

For inductive step, suppose $i$ is an arbitrary integer and $P(i)$ is true for $2\leq i\leq n$. We need to show that $P(n+1)$ is true.

Suppose $0\leq k\leq n$.  By part (a) it follow that
$$
\begin{align}
(a_{1}+\dots+a_{k})+(a_{k+1}+\dots+a_{n+1})&= (a_{1}+\dots+a_{k})+((a_{k+1}+\dots+a_{n})+a_{n+1}) \\
&=((a_{1}+\dots+a_{k})+(a_{k+1}+\dots+a_{n}))+a_{n+1}
\end{align}
$$

Notice that $(a_{1}+\dots+a_{n})$ consists of $n$ terms, thus by IH it follow that

$$
(a_{1}+\dots+a_{k})+(a_{k+1}+\dots+a_{n+1})=a_{1}+\dots+a_{n+1}
$$

By mathematical induction, $P(n)$ is true for all $n\geq 2$.$\blacksquare$

c)

> [!question] 24(c)
> Let $s(a_{1},\dots,a_{k})$ be some sum formed from $a_{1},\dots,a_{k}$. Show that
> 
> $$
> s(a_{1},\dots,a_{k})=a_{1}+\dots+a_{k}
> $$
> 

Since sum is a binary operator, it follow that there exist 2 sum $s'(a_{1},\dots a_{t})$ and $s''(a_{t+1},\dots,a_{k})$ such that

$$
s(a_{1},\dots,a_{k})=s'(a_{1},\dots,a_{t})+s''(a_{t+1},\dots,a_{k})
$$

From part (b) we know that

$$
s'(a_{1},\dots,a_{t})+s''(a_{t+1},\dots,a_{k})=a_{1}+\dots+a_{k}
$$

Thus,

$$
\begin{align}
s(a_{1},\dots,a_{k})=a_{1}+\dots+a_{k} &&\blacksquare
\end{align}
$$


> [!remark]
> To prove the associativity law, since addition is a binary operator there exist 2 group of sub sum that sum up to the final result. (c)
> 
> We need to prove that no matter how this 2 group be formed, it is still the same as $a_{1}+\dots+a_{n}$.  (We need to define how to add this first, we define as right nested parenthesis) (b)
> 
> To prove (b) we need to have the ability to move the parathesis right and left, so that $(X+Y)+Z=X+(Y+Z)$
> 
> Why right nested parenthesis is being choose as definition? Actually we can use left nested parenthesis as definition.

---

The property of number 0

> [!theorem] P2 (Existence of additive identity)
> If $a$ is any number, then
> $$
> a+0=0+a=a
> $$

> [!theorem] P3 (Existence of additive inverse)
> For every number $a$, there is a number $-a$ such that
> 
> $$
> a+(-a)=(-a)+a=0
> $$

Another characteristic statement of P2:
If a number $x$ satisfy
$$
a+x=a
$$
for any number $a$, then $x=0$. (We can prove this by add $(-a)$ on both side)

We always use P1-P3 to justify the operation of find $x$ in an equation.

$$
\begin{align}
a+x&=a \\
(-a)+(a+x)&=(-a)+a=0 \\
(-a+a)+x&=0 \\
x&=0
\end{align}
$$

Notice that subtraction is an operation derived from addition, for example $a-b$ is $a+(-b)$.

> [!theorem] P4 (Commutative law for addition)
> If $a$ and $b$ are any numbers, then
> 
> $$
> a+b=b+a
> $$

Notice that not all operation process this property, for example subtraction. Usually, $a-b\neq b-a$, but when $a-b=b-a$? It is not enough to use only P1-P4 to find the answer. Why? 

$$
\begin{align}
a-b&=b-a \\
(-a)+a-b&=b-a+(-a) \\
-b&=b-2a \\
-2b&=-2a \\
a&=b
\end{align}
$$

Can we do like like this? Cannot because we haven't define what is multiplication and division and also we haven't establish the fact $(1+1=2)$ .Thus, we need some other properties as below:

[[Basic Properties of Numbers#^5acf15]]

> [!theorem] P5 (Associative law for multiplication)
> If $a,b$ and $c$ are any numbers, then
> 
> $$
> a\cdot(b\cdot c)=(a\cdot b)\cdot c
> $$

> [!theorem] P6 (Multiplicative identity)
> If $a$ is any number, then
> $$
> a\cdot 1=1\cdot a=1
> $$

Moreover $1\neq 0$, the assertion that $1 \neq 0$ need to be listed because it cannot be proved.

> [!theorem] P7 (Multiplicative inverse)
> For every number $a\neq 0$, there is a number $a^{-1}$ such that 
> 
> $$
> a\cdot a^{-1}=a^{-1}\cdot a=1
> $$

The condition of $a\neq 0$ is crucial because since $0\cdot b=0$ for all number of $b$. 

(This can be prove using P9 below).
[[Basic Properties of Numbers#^9ef430]]

Thus, it follow that no number $0^{-1}$ such as $0\cdot 0^{-1}=1$. Thus, division by 0 is always undefined.

Division is defined in terms of multiplication, the symbol $\frac{a}{b}$ means $a\cdot b^{-1}$. 

### Consequence of P7
$ab=ac$ does not imply $b=c$ (it is only true when $a\neq 0$). Because if $a=0$, then $a^{-1}$ is not exist.

> [!theorem] Corollary 1
> Suppose $a \neq 0$, then 
> $$
> ab=ac\implies b=c
> $$

Proof when $a\neq 0$:

$$
\begin{align}
a\cdot b&=a\cdot c \\
a^{-1}\cdot(a\cdot b)&=a^{-1}\cdot(a\cdot c) \\
(a^{-1}\cdot a)\cdot b&=(a^{-1}\cdot a)\cdot c \\
1\cdot b&=1\cdot c \\
b&=c
\end{align}
$$

Another consequence of P7:

> [!theorem] Corollary 2 (Zero Product Property)
> If $a\cdot b=0$, then either $a=0$ or $b=0$.

^6b5b8a

Proof:
WLOG suppose $a\neq 0$.Thus,

$$
\begin{align}
ab&=0 \\
a^{-1}ab&=a^{-1}0 \\
b&=0
\end{align}
$$

The consequence of corollary 2:

$$
(x-1)(x-2)=0
$$
implies that $x-1=0$ or $x-2=0$.

(P7 allow us to implies each factor given the product, it is like division)

> [!remark]
> To prove either case, we just need to suppose when one condition is failed then another condition must happen



> [!theorem] P8 (Commutative law for multiplication)
> If $a$ and $b$ are any numbers, then
> $$
> a\cdot b=b\cdot a
> $$

With P1-P8 we can only prove little.

> [!theorem] P9 (Distributive law)
> If $a,b$ and $c$ are any numbers, then
> $$
> a\cdot(b+c)=a\cdot b+a\cdot c
> $$

P9 is a property combine addition and multiplication 

### Consequence of P9:

Determine when $a-b=b-a$: ^5acf15

$$
\begin{align}
a-b&=b-a \\
(a-b)+b&=b+(b-a) \\
a+a&=(b+b)+(-a)+a \\
a+a&=b+b \\
a(1+1)&=b(1+1) \\
a&=b &&\text{(By cor0llary 1)}
\end{align}
$$

> [!theorem] Corollary 3
> If $a-b=b-a$, then $a=b$

> [!question]
> How to we know $1+1\neq 0$? 
> 
> We know that 1 is multiplicative identity. Thus, $1^{2}=1\neq 0$ . From [[Basic Properties of Numbers#^1e22c2]] , we know that $1^{2}>0\implies 1>0$. From [[Basic Properties of Numbers#^7d98e7]]. Thus, $1+1>0$ (Closure under addition)  


Prove that $a\cdot 0=0$: ^9ef430

$$
\begin{align}
a\cdot 0+(a\cdot 0)&=a(0+0) \\
&=a\cdot 0
\end{align}
$$
By characteristic of P2, it follow that $a\cdot 0=0$. (subtract $a\cdot 0$ from both side).$\blacksquare$

> [!question]
> Why we start like this?
> It is because the non trivial property of 0 is $0+0=0$,
> and the only connection of multiplication and addition is P9
> 

> [!theorem] Corollary 4
> For any number $a$, $a\cdot 0=0$

>[!theorem] Corollary 5
> For any number $a,b$ 
> $$
> (-a)\cdot(-b)=ab
> $$
>  

^1b98fa

Reverse process
$$
\begin{align}
(-a)\cdot(-b)&=ab \\
(-a)\cdot(-b)+(-(ab))&=0  \\
(-a)(-b+b)&=0 \\
(-a)\cdot 0&=0
\end{align}
$$

In the reverse process we use the lemma below. Thus, we only need to prove
> [!theorem] Lemma 
> For any number $a,b$ 
> $$-(ab)=(-a)\cdot b$$

^1173ea

Proof:
$$
(-a)\cdot b+ab=b(a+(-a))=0
$$
Thus, $(-a)\cdot b=-(ab)$ $\blacksquare$

Proof for Corollary 5:
Notice that
$$
\begin{align}
(-a)\cdot 0=&0 \\
(-a)(b+(-b))&=0 \\
-(ab)+ ((-a)\cdot(-b))&=0 &&\text{(By Lemma)}\\
ab+(-ab)+((-a)\cdot(-b))&=ab \\
(-a)\cdot(-b)&=ab &&\blacksquare
\end{align}
$$

> [!remark]
> Corollary 5 is the justification why $ab>0$ if $a,b<0$ and lemma show that $ab<0$ if one of them is in $-P$.
> [[Basic Properties of Numbers#^84b7a2]]
> 

Actually, P9 is the justification for almost all algebraic manipulations.

The multiplication $(x-1)(x-2)$ is a multiple use of P9.

The multiplication algorithms is a way to write 

$$
\begin{align}
13\cdot 24&=13(2\cdot 10+4) \\
&=13(2\cdot 10)+13(4) \\
&=26\cdot 10+52 \\ 
&=312
\end{align}
$$
and it use P9 as well.

The 3 basis properties of numbers which remain to be listed are concerned with inequalities.

$a>b$ is the same as $b<a$. The same assertion). $a$ is positive iff $a>0$ while $a$ is negative iff $a<0$. 

$a<b\implies b-a> 0$, for convenience let $P$ denote the set of all positive number.

> [!theorem] P10 (Trichotomy law) 
> For every number $a$, one and only one of the following holds:
> 
> i) $a=0$
> ii) $a$ is in $P$
> iii) $-a$ is in $P$


> [!theorem] P11 Closure under addition
If $a,b\in P$, then $a+b\in P$.

> [!theorem] P12 Closure under multiplication
> If $a,b\in P$, then $a\cdot b\in P$.

These three properties should be complemented with the following definitions:
1) $a>b$ iff $a-b\in P$;
2) $a<b$ iff $b>a$; (It is very clean)
3) $a\geq b$ iff $a-b\in P$ or $a=b$
4) $a\leq b$ iff $b\geq a$

> [!remark]
> The definition of inequality is based on the trichotomy law (set)


All the familiar facts about inequalities are the consequence of P10-P12. 

For example,

> [!theorem] Corollary 6
> For any number $a$ and $b$, it follow that one and only one hold by P10
> 
> i) $a-b=0$ 
> ii) $a-b\in P$
> iii) $-(a-b)=b-a\in P$ 
> 
> By definition it is equivalent to
> i) $a=b$
> ii) $a> b$
> iii) $b>a$
> 
> 

> [!theorem] Corollary 7
> If $a<b$, then $(b+c)-(a+c)> 0$.
> 

Characteristic:
if $a<b$, then $a+c<b+c$

Proof: 

$$
\begin{align}
(b+c)-(a+c)&=b+c-a-c \\
&=b-a+c-c \\
&=b-a \\
&> 0 && \blacksquare
\end{align}
$$


How to prove if $a<b$ and $b<c$, then $a<c$ ?

Notice that $b-a> 0$ and $c-b>0$.

$$
\begin{align}
c-a&=(c-b)+(b-a)> 0
\end{align}
$$

> [!theorem] Transitivity Law
> if $a<b$ and $b<c$, then $a<c$

Prove that 

> [!theorem] Corollary 8
> 
> If $a<0$ and $b<0$, then $ab>0$.
> 

Proof:

If $a<0$ , then $-a> 0$ Why?
$a<0\implies 0-a=-a>0$ . (It is a special case for [[Basic Properties of Numbers#^6475d5]])

Similarly $-b>0$. From Corollary 5, we know that 

$$
\begin{align}
(-a)\cdot(-b)&=ab \\
&>0 &&\text{(Closure under multiplication)}\blacksquare
\end{align}
$$


The fact that

> [!theorem] Corollary 9
> 
> $ab>0$ iff $a>0,b>0$ or $a<0,b<0$ 
> 

^84b7a2

> [!remark] 
> From Corollary 9, we know that suppose $a,b\neq 0$,  $ab<0$ iff exactly one of the factor is negative.(From cases exhaustion) 
> 
> Or without the assumption of $a,b \neq 0$, we can say the factor have opposite sign

have one special consequence: 

> [!theorem] Corollary 10
> $$a^{2}>0 \text{ if }a\neq 0$$
> 

^1e22c2

From Corollary 10 we can infer that $1>0$ because $1^{2}=1>0$.

What does $-a>0$ means? It means that $-(-a)=a<0$.

### Absolute value

Definition of absolute value

$$
|a|=\begin{cases}
a, & a\geq 0 \\
-a, & a< 0
\end{cases}
$$


> [!theorem] Theorem 1 Triangle inequality
> For all numbers $a$ and $b$, we have
> 
> $$
> |a+b|\leq|a|+|b|
> $$
> 

Reverse process:
We square both side using the fact that $|a|^{2}=a^{2}$

$$
\begin{align}
|a+b|^{2}&\leq(|a|+|b|)^{2} \\
a^{2}+2ab+b^{2}&\leq^{2}+2|ab|+b^{2}
\end{align}
$$

Thus, we only need to prove $ab\leq|ab|$ as lemma below:

> [!theorem]  Lemma 1
> For all $a\in \mathbb{R}$, $|a|\geq a$.

Proof:
Suppose $a$ is an arbitrary integer.

Case 1: $a\geq0$
Then by definition $|a|=a$.

Case 2: $a<0$.
By definition, $|a|=-a$. Since $a<0$, it follow that $-a>0$. Thus, $|a|=-a> 0$.  Hence

$$
a<0<|a|
$$
By transitivity law $|a|\geq a$.$\blacksquare$

> [!theorem] Lemma 2
> If $x^{2}<y^{2}$, then $x<y$.
> 

Proof: [[Basic Properties of Numbers#^7d98e7]]


Proof for the theorem:
Suppose 2 arbitrary real number $a$ and $b$. 
$$
\begin{align}
|a+b|^{2}&=(a+b)^{2} \\
&=a^{2}+2ab+b^{2}
\end{align}
$$

$$
\begin{align}
(|a|+|b|)^{2}=a^{2}+2|ab|+b^{2}
\end{align}
$$


By lemma 1 $|ab|>ab$. Hence, it follow that

$$
\begin{align}
(|a|+|b|)^{2}\geq|a+b|^{2} \\
|a|+|b|\geq|a+b|&&\blacksquare
\end{align}
$$

> [!remark] Remark
> We use squaring method to eliminate the absolute value
> We can also use case division strategy

Another approach using case division:

Reverse process:
Case 1: $(x+y)\geq0$
By definition $|x+y|=x+y$. Thus,

$$
x+y\leq |x|+|y|
$$
To show this we only need to prove $|a|\geq a$ for all $a\in \mathbb{R}$. (Lemma 1)

Case 2: $(x+y)< 0$
By definition $|x+y|=-(x+y)=-x+(-y)$. Thus,

$$
\begin{align}
-x+(-y)\leq|x|+|y|
\end{align}
$$
To prove this we only need to show $|x|\geq-x$. By lemma 1 $|-x|\geq -x$. Since $|-x|=|x|$ (lemma 2*), it follow that $|x|\geq -x$. $\blacksquare$

> [!question]
> Question: When $|a+b|=|a|+|b|$ and $|a+b|<|a|+|b|$?
> 
> $|a+b|=|a|+|b|$ if $a,b$ have same sign or if one of the 2 is 0
> 
> $|a+b|<|a|+|b|$ if $a$ and $b$ are opposite sign
> 
> 

### Problem 5:

^7d98e7

i) if $a<b$ and $c<d$, then $a+c<b+d$.

Proof:
By definition $b-a> 0$ and $d-c> 0$.

$$
\begin{align}
b+d-(a+c)&=b-a+d-c \\
&> 0
\end{align}
$$
By definition $a+c<b+d$. $\blacksquare$

![[Problem Chapter 1 Basic Properties of Number#^d8a496]] (The general version)

ii)
If $a<b$, then $-b<-a$ (Multiply negative 1) ^6475d5

Reverse process:
$$
\begin{align}
-b-(-a)&<0 \\
-b+a&<0 \\
a-b&<0 \\
a&<b
\end{align}
$$

Proof:
By definition $a<b \Leftrightarrow b>a \Leftrightarrow b-a\in P$. Thus, $b-a> 0$.

$$
a-b<0
$$
Thus

$$
\begin{align}
-b+a&<0 \\
-b-(-a)&<0 \\
-b<&-a &&\blacksquare
\end{align}
$$



> [!remark]
> From here we can deduce that $-P$ is closed under addition [[Problem Chapter 1 Basic Properties of Number#^cd02a8]]
> 
> 

iii)
If $a<b$ and $c>d$, then $a-c<b-d$. (small-big < big-small)

Reverse Process:
We need to show that 
$$
\begin{align}
(b-d)-(a-c)&> 0 \\
(b-a)+(c-d)&> 0 \\
(b-a)-(d-c)&> 0
\end{align}
$$

By definition $b-a>d-c$. (This is the thing we need to show)

Proof:
By definition $b-a>0$ and $d-c<0$. Thus, it follow that

$$
d-c<0<b-a
$$
by transitivity law, $d-c<b-a$. Thus, by definition

$$
\begin{align}
(b-a)-(d-c)&>0 \\
(b-d)+(c-a)&>0 \\
(b-d)-(a-c)&>0
\end{align}
$$
Thus, by definition $b-d>a-c$. $\blacksquare$.

iv) If $a<b$ and $c>0$, then $ac<bc$. (Multiply positive number)

We need to show that
$$
\begin{align}
bc-ac&>0 \\
c(b-a)&>0
\end{align}
$$

Since $c>0$, it follow that $b-a>0$. Why? Because $ab>0$ iff
1) $a>0$ and $b>0$ or
2) $a<0$ and $b<0$ 

Proof:
By definition $b-a>0$, since $b-a>0$ and $c>0$, it follow that their product $c(b-a)>0$. Thus

$$
\begin{align}
c(b-a)&>0 \\
bc-ac&>0
\end{align}
$$

By definition $bc>ac$. $\blacksquare$

v) If $a<b$ and $c<0$, then $ac>bc$. (Multiply negative number)

Reverse process:

$$
\begin{align}
ac-bc&>0 \\
c(a-b)&>0
\end{align}
$$
Since $c< 0$, by Corollary 9, it follow that $a-b<0\implies a<b$. $\blacksquare$.

> [!remark]
> Notice that 5(v) is the generalization of 5(ii)

Proof: 
By definition $a-b<0$ and by supposition $c<0$. Thus, by Corollary 9, it follow that

$$
\begin{align}
c(a-b)>0 \\
ac-bc&>0
\end{align}
$$
By definition $ac>bc$. $\blacksquare$

> [!remark]
> This prove that why whenever we multiply both side with negative we flip the sign: $a+b>0\implies-(a+b)<0$ [[Problem Chapter 1 Basic Properties of Number#^cd02a8]]
> 

vi) If $a>1$, then $a^{2}>a$

Reverse process:
By definition
$$
\begin{align}
a^{2}-a&>0 \\
a(a-1)&>0
\end{align}
$$
Since $a>1$, $a-1> 0$, and $a>0$. Thus, by corollary 9, it is true.

Proof:
Suppose $a>1$, then $a>0$ and $a-1> 0$. Thus, by Corollary 9, it follow that

$$
\begin{align}
a(a-1)&> 0 \\
a^{2}-a&>0 \\
a^{2}&>a&&\blacksquare
\end{align}
$$

vii) If $0<a<1$, then $a^{2}<a$.

Reverse process:
$$
\begin{align}
a^{2}-a&<0 \\
a(a-1)&<0
\end{align}
$$
Since $0<a<1$, it follow that $a>0$, thus $(a-1)<0$ . By definition

$$
\begin{align}
a<1
\end{align}
$$

> [!remark]
> (vi) and (vii) are talking about the same thing in different condition

Proof:
Suppose $0<a<1$. Thus, $a>0$ and $a<1\implies a-1< 0$. Since they have opposite sign,  by Corollary 9 it follow that
$$
\begin{align}
a(a-1)&<0 \\
a^{2}-a&<0
\end{align}
$$
By definition $a^{2}<a$. $\blacksquare$

viii) If $0\leq a<b$ and $0\leq c<d$, then $ac<bd$. (Positive: small$\times$small < big$\times$big) ^48a371

$$
\begin{align}
bd-ac&>0 \\
(bd-ad)+(ad-ac)&>0 \\
d(b-a)+a(d-c)&>0
\end{align}
$$

From supposition we know that $d>0,(b-a)>0,a\geq0,(d-c)>0$

Generalize:
We need $b$ and $a$ as comparison, but we have $bd$, we want $b$ but we don't want $d$, thus we multiply we $ad$ and factor out $d$.
#tool/add-zero-to-decouple

> [!remark] Strategy: Add Zero to Decouple
> We add zero (-ad + ad) to decouple the double variation (a -> b and c -> d) into single-variable differences.

Proof:
Suppose $0\leq a<b$ and $0\leq c<d$. Thus, it follow that $d>0,(b-a)>0,a\geq0,(d-c)>0$. Hence,

By P12 (Closure under multiplication)
$$
d(b-a)>0 \text{ and }a(d-c)\geq0
$$
By P11(Closure under addition)

$$
\begin{align}
d(b-a)+a(d-c)&>0 \\
bd-ad+ad-ac&>0 \\
bd-ac&>0 \\
bd&>ac &&\blacksquare
\end{align}
$$

ix) If $0\leq a<b$, then $a^{2}<b^{2}$. (Use (viii)) ^1563fe

Proof: Suppose $0\leq a<b$. Thus, let $c=a$ and $d=b$ by (viii), it follow that

$$
\begin{align}
a^{2}<b^{2} && \blacksquare
\end{align}
$$

> [!remark]
> Notice that this is actually a biconditional statement. Why?
> Consider the contrapositive: Suppose $a,b\geq 0$,  if $b^{2}\leq a^{2}$, then $0\leq b<a$.
> 
> We use this fact to show the question below.


x) If $a,b\geq 0$ and $a^{2}<b^{2}$, then $a<b$. (Use (ix),backwards) ^78617a

Proof:
By the contrapositive of ix), suppose $a,b\geq 0$, if $a^{2}\leq b^{2}$, then $0\leq a<b$. $\blacksquare$

> [!remark]
> (vii), (ix) and (x) is consecutive step to prove (x) and notice that (x) and (ix) are equivalent statement


> [!question]
> The last question will be does P1-P12 account for all properties of numbers? In next chapter we will see the deficiency of these properties.

Another 2 property [[Problem Chapter 3 Function#^d0ed66]]

> [!theorem]
> 
> 1) If $0\leq w\leq 1$, then $0\leq w^{2}\leq w$.
> 2) If $|w|>1$, then $w^{2}>w$.
> 

Generalize version of (ix) and (x) [[Problem Chapter 3 Function#^a1c187]]