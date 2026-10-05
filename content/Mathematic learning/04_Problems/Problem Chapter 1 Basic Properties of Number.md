---
aliases:
---
1.  Prove the following
i) If $ax=a$ for some number $a\neq 0$, then $x=1$

Proof:
Suppose $ax=a$. Then

$$
\begin{align}
ax-ax&=a-ax \\
0&=a(1-x) \\

\end{align}
$$
Since $a\neq 0$, it follow that $1-x=0\implies x=1$. $\blacksquare$ 

> [!remark]
> It is actually another way to say the existence of multiplicative identity. Why? Existential statement is $P\land Q$. There exist multiplicative identity and the identity is 1. For the statement to be true, both must be true and $P\land Q=Q\land P$.

ii) $x^{2}-y^{2}=(x-y)(x+y)$

Proof:
$$
\begin{align}
(x-y)(x+y)&=x(x+y)-y(x+y) &&\text{P9}\\
&=x^{2}+xy-xy+y^{2} &&\text{P9 and C10} \\
&=x^{2}-y^{2}&&\blacksquare
\end{align}
$$

iii) If $x^{2}=y^{2}$, then $x=y$ or $x=-y$.

Proof:

$$
\begin{align}
x^{2}&=y^{2} \\ 
x^{2}-y^{2}&=0 \\
(x-y)(x+y)&=0 &&1(ii)
\end{align}
$$

Thus, $x-y=0\implies x=y$ and $x+y=0\implies x=-y$ $\blacksquare$.

iv) $x^{3}-y^{3}=(x-y)(x^{2}+xy+y^{2})$

Proof:
$$
\begin{align}
(x-y)(x^{2}+xy+y^{2})&=x(x^{2}+xy+y^{2})-y(x^{2}+xy+y^{2}) \\
&=x^{3}+x^{2}y+xy^{2}-x^{2}y-xy^{2}-y^{2} \\
&=x^{3}-y^{3} &&\blacksquare
\end{align}
$$


v) $x^{n}-y^{n}=(x-y)(x^{n-1}+x^{n-2}y+\dots+xy^{n-2}+y^{n-1})$

Proof:

$$
\begin{align}
(x-y)(x^{n+1}+x^{n-2}y+\dots+xy^{n-2}+y^{n-1})&=x(x^{n-1}+x^{n-2}y+\dots+xy^{n-2}+y^{n-1}) \\
&-y(x^{n-1}+x^{n-2}y+\dots+xy^{n-2}+y^{n-1}) \\
&=x^{n}+x^{n-1}y+\dots+x^{2}y^{n-2}+xy^{n-1} \\
&-x^{n-1}y-x^{n-2}y^{2}-\dots-xy^{n-1}-y^{n}
\end{align}
$$

From here we can see that the term after $x^{n}$ and term before $-y^{n}$ collapse(cancel) together (Telescoping sum).  Why it happen? Observe iv) how the term cancel each other $x$ and $-y$ as multiplication. Thus, 

$$
\begin{align}
(x-y)(x^{n-1}+x^{n-2}y+\dots+xy^{n-2}+y^{n-1})=x^{n}-y^{n}&& \blacksquare
\end{align}
$$

vi) $x^{3}+y^{3}=(x+y)(x^{2}-xy+y^{2})$  ^ee071a

if $y<0$, then $y^{3}<0$
if $y>0$, then $y^{3}>0$.
Thus we can say $(-y)^{3}=-y^{3}$, it preserve the sign. Or we prove like this 

$$
\begin{align}
(-y)^{3}&=(-1\cdot y)^{3} \\
&=(-1)^{3}y^{3} \\
&=-1y^{3} \\
&=-y^{3}
\end{align}
$$


Let $u=-y$, then $x^{3}+y^{3}=x^{3}+(-u)^{3}=x^{3}-u^{3}$. 

By (iv), it follow that

$$
\begin{align}
x^{3}-u^{3}=(x-u)(x^{2}+xu+u^{2})
\end{align}
$$

By substitution,

$$
\begin{align}
x^{3}-(-y)^{3}&=x^{3}+y^{3} \\
&=(x+y)(x^{2}-xy+y^{2}) &&\blacksquare
\end{align}
$$

> [!remark] General version:
> Let $n =2k+1$ for some integer $k$. Notice that $(-y)^{n}=-y^{n}$. Thus, let $u=-y$, by substitution
> 
> $$
> \begin{align}
> x^{n}+y^{n}&=x^{n}+(-u)^{n} \\
> &=x^{n}-u^{n}
> \end{align}
> $$
> 
> By v) it follow that
> 
> $$
> \begin{align}
> x^{n}-u^{n}&=(x-u)(x^{n-1}+x^{n-2}u+\dots+xu^{n-2}+u^{n-1}) \\
> x^{n}+y^{n}&=(x+y)(x^{n-1}-x^{n-2}y+x^{n-3}y^{2}-\dots +y^{n-1}) &&\blacksquare
> \end{align}
> $$
> 

> [!remark]
> Notice that it is a alternating sign of summation

> [!question]
> Is this true for $n$ is even number?
> Let's test when $n =2$, does $x^{2}+y^{2}$ can be factorize into any linear factor? (No). So the statement only true for $n$ is odd number


2)
We cannot divide $x-y$ from both side, because $x=y\implies x-y=0$.

3)
Prove the following

i) (Expansion/Cancellation rule)
$\cfrac{a}{b}=\cfrac{ac}{bc}$, if $b,c \neq 0$.

Prove:
Suppose $b,c\neq 0$. Thus, $\frac{a}{b}$ exist for some number $a$. From ![[Basic Properties of Numbers#^6b5b8a]] we know that $bc \neq 0$. 
Thus,

$$
\begin{align}
\frac{a}{b}&=\frac{a}{b}\times 1 \\
\end{align}
$$

Since $c \neq 0$, it follow that $cc^{-1}=\frac{c}{c}=1$. (Multiplicate inverse) Thus,

$$
\begin{align}
\frac{a}{b}&=\frac{a}{b}\times \frac{c}{c}
\end{align}
$$

Since we define division from multiplication. Thus, $\frac{a}{b}=ab^{-1}$ and $\frac{c}{c}=cc^{-1}$. Thus,

$$
\begin{align}
ab^{-1}cc^{-1}&=ac b^{-1}c^{-1} && \text{(Commutative law)} \\
&=(ac)(b^{-1}c^{-1}) \\
&=\frac{ac}{bc} &&\text{(Why? refer to 3(iii))}\blacksquare
\end{align}
$$


ii (Addition of fractions)
$\frac{a}{b}+\frac{c}{d}= \frac{ad+bc}{bd}$ if $b,d\neq 0$.

Proof:
Since $b \neq 0$, thus $\frac{a}{b}$ exist for some real number $a$. Since $d \neq 0$, it follow from 3(i) that 

$$
\frac{a}{b}=\frac{ad}{bd}
$$
The same argument apply for $\frac{c}{d}$, thus

$$
\frac{c}{d}= \frac{bc}{bd}
$$
Hence,

$$
\begin{align}
\frac{a}{b}+\frac{c}{d}&= \frac{ad}{bd}+\frac{bc}{bd} \\
&=ad(bd)^{-1}+bc(bd)^{-1} \\
&=(bd)^{-1}(ad+bc) \\
&=\frac{ad+bc}{bd} && \blacksquare
\end{align}
$$

> [!remark]
> Division is defined from multiplication

iii) (Inverse of a product)
$(ab)^{-1}=a^{-1}b^{-1}$, if $a,b \neq 0$. (To do this you must remember the defining property of $(ab)^{-1}$)

Proof:
Suppose $a,b \neq 0$. Then, there exist $a^{-1}$ and $b^{-1}$ such that $aa^{-1}=1$ and $bb^{-1}=1$. Since $1\times 1=1$, it follow that
$$
\begin{align}
(aa^{-1})(bb^{-1})&=1 \\
aa^{-1}bb^{-1}&=1 \\
aba ^{-1}b^{-1}&=1 \\
(ab)a^{-1}b^{-1}&=1
\end{align}
$$
Thus, by definition $a^{-1}b^{-1}=(ab)^{-1}$. $\blacksquare$ 

> [!remark]  Remark
> This is the lemma for proving $3(i)$. 

iv) (Multiplication of fraction)
$\frac{a}{b}\cdot \frac{c}{d}= \frac{ac}{db}$ if $b,d \neq 0$.

Proof:
Suppose $b,d \neq 0$ and suppose $a$ and $c$ are arbitrary real number. Then

$$
\begin{align}
\frac{a}{b}\cdot \frac{c}{d}&=(ab^{-1})(c d^{-1}) \\
&=(ac)(b^{-1}d^{-1}) \\
&=(ac)(bd)^{-1} \\
&=\frac{ac}{bd} &&\blacksquare
\end{align}
$$

v) (Division of fraction)
$\frac{a}{b}/ \frac{c}{d}= \frac{ad}{bc}$, if $b,c,d \neq 0$.

Proof:
Suppose $a,b,c,d$ are arbitrary real numbers and $b,c,d \neq 0$. Thus,

$$
\begin{align}
\frac{a}{b} / \frac{c}{d}&= (ab^{-1})(cd ^{-1})^{-1} \\
&=(ab^{-1})c ^{-1} (d^{-1})^{-1} \\
&=ab^{-1}c^{-1}d \\
&=(ad)(b^{-1}c^{-1}) \\
&= (ad)(bc)^{-1} \\
&= \frac{ad}{bc} && \blacksquare
\end{align} 
$$

> [!remark]
> Remark
> expansion/cancellation rule, addition, multiplication of fraction need 3(iii) which is the inverse of product

vi) (Cross multiplication rule)
If $b,d \neq 0$, then $\frac{a}{b}=\frac{c}{d}$ if $ad=bc$. Also determine when $\frac{a}{b}=\frac{b}{a}$.

Proof:
Suppose $a,b,c,d$ are arbitrary real number and $b,d \neq 0$ .
Assume $ad=bc$. Since $b,d \neq 0$, it follow that there exist $b^{-1}$ and $d^{-1}$.
Thus,
$$
\begin{align}
ad&=bc \\
ad(d^{-1})&=bc(d^{-1}) \\
a&=bc(d^{-1}) \\
b^{-1}a&=(b^{-1})bc(d^{-1}) \\
ab^{-1}&=(b^{-1}b)(cd^{-1}) \\
ab^{-1}&=cd^{-1} \\
\frac{a}{b}&=\frac{c}{d}
\end{align}
$$

Conversely, suppose $\frac{a}{b}=\frac{c}{d}$. Thus,

$$
\begin{align}
\frac{a}{b}&=\frac{c}{d} \\
(ab^{-1})b&=(cd^{-1})b \\
a(b^{-1}b)&=(cd^{-1})b \\
a&=(cd^{-1})b \\
ad&=(cd^{-1})bd \\
&=bc (d^{-1}d) \\
ad&=bc && \blacksquare
\end{align}
$$

4) Find all numbers $x$ for which
i) $4-x<3-2x$

$$
\begin{align}
4-x&<3-2x \\
(4-x)-(3-2x)&<0 &&\text{By definition}\\
1+x&<0 &&(1) \\
x-(-1)&< 0 &&(2) \\
x&< -1 &&\text{By definition}
\end{align}
$$

> [!remark]
> Notice that (1) need Distributive law of multiplication and (2) can actually $-1$ from both side by proving the statement below.


> [!Theorem] (Additive Property of Inequalities)
> If $a<d$, then $a+c<d+c$ for any number $c$. (It is general version of 5(i)) ^d8a496
>  
>  Proof:
> Suppose $a<d$, then
>  
>  $$
>  \begin{align}
>  a-d<0 \\
>  a+c-c-d&<0 \\
>  (a+c)-(d+c)&<0 \\
>  a+c&<d+c &&\blacksquare
>  \end{align}
> $$

 

> [!question]  Does all the step we performed above work in both direction ($\Leftrightarrow$)?
> 
> Yes, and why it is crucial?. It means that the statement is actually biconditional. Thus, the set $(-\infty,-1)$ is identical to the solution set of $4-x<3-2x$.


ii) $5-x^{2}<8$

$$
\begin{align}
5-x^{2}&<8 \\
5-x^{2}-8&<0 \\
3-x^{2}&<0 \\
x^{2}&>3 \\
x&>\sqrt{ 3 } \text{ or }x<-\sqrt{ 3 }
\end{align}
$$

Note: The first case happen if $x>0$ which is proved in 5(x)

![[Basic Properties of Numbers#^78617a]] 

and the second case happen if $x< 0$. (We need to prove this)

> [!theorem]
> Prove if $a,b\leq0$ and $a^{2}<b^{2}$, then $a>b$. 
> 
>
Contrapositive: if $a,b\leq 0$ and $b>a$, then $a^{2}>b^{2}$

Reverse process:

$$
\begin{align}
a^{2}-b^{2}&>0 \\
(a-b)(a+b)&>0
\end{align}
$$
It is either $(a-b),(a+b)< 0$ or $(a-b),(a+b)\geq 0$.  (it is from Corollary 9) ![[Basic Properties of Numbers#^84b7a2]]
.Since $b>a$ it follow that $a-b<0$. Since $a,b\leq 0$, it follow that $a+b<0$ (why?).(first it is from the case either, second it reveal a law which is  $-P$ closed under addition )

> [!remark]
> (Wait we prove though contrapositive and use reverse process, so it is like the forward direction of the original theorem!!! So this is actually the forward prove using the lemma below)
> 

> [!theorem] Lemma: $-P$ is closed under addition ^cd02a8
> 
> Proof:
> Suppose $a,b$ are arbitrary real number such as $a,b>0$. Thus, by P11 it follow that
> $$
> \begin{align}
> a+b&>0 \\
> -(a+b)&<0 &&\text{5(ii)}\\
> -a+(-b)&<0
> \end{align}
> $$
> Since $-a\in-P$ and $-b\in-P$. Thus, it follow that $-P$ is closed under addition.$\blacksquare$ 


Proof:
Suppose $a,b$ are arbitrary real number and $a,b\leq 0$. Assume that $b>a$, thus $a-b<0$ and $a+b<0$. ($-P$ closed under addition). Thus, by Corollary 9 ![[Basic Properties of Numbers#^84b7a2]]  

$$
\begin{align}
(a-b)(a+b)&>0 \\
a^{2}-b^{2}&>0 \\
a^{2}&>b^{2} &&\blacksquare
\end{align}
$$

> [!remark]
> This is the contrapositive proof



Another approach (Generalization): we use one lemma （The converse of [[Basic Properties of Numbers#^48a371]]）

> [!theorem]  Lemma: If $a<b\leq 0$ and $c<d\leq 0$, then $ac>bd$.
> 
> Reverse process:
> $$
> \begin{align}
> ac-bd&>0 \\
> ac-bc+bc-bd&>0 \\
> c(a-b)-b(d-c)&>0
> \end{align}
> $$
> since $a\leq b$, it follow that $a-b<0$ and since $c<0$, by the lemma above $c(a-b)>0$. Since $c\leq d$, it follow that $d-c> 0$ and since $b<0$, it follow that $b(d-c)< 0$ by lemma of Corollary 5 ![[Basic Properties of Numbers#^1173ea]] 
> . 
> 
> Proof:
> Suppose $a<b\leq 0$ and $c<d\leq 0$. Thus, it follow that $a-b<0$ and $d-c>0$. Since $c<0$, it follow by lemma above ($-P$ is closed under addition) that
> $$
> c(a-b)>0
> $$
> Since $b<0$ and $d-c>0$, it follow by the lemma of Corollary 5 that 
> 
> $$
> b(d-c)<0
> $$
> Thus,
> 
> $$
> \begin{align}
> c(a-b)-b(d-c)&<0 \\
> ac-bc+bc-bd&<0 \\
> ac-bd&<0 \\
> ac&<bd && \blacksquare 
> \end{align}
> $$
> 

Proof (Approach 2):
Suppose $a,b\leq 0$ and $b>a$, then by lemma above 

$$
\begin{align}
b^{2}<a^{2} &&\blacksquare
\end{align}
$$

> [!remark]
> Reverse process need to make sure everything is biconditional : for example we can't straight away use reverse process when we want to prove suppose $a,b\geq0$ if $a^{2}<b^{2}$, then $a<b$ or its converse. In fact we prove for 5(viii), 5(ix) to prove the statement. (We use the contrapositive to prove which is the forward direction) 
> 
> What happen if we work backwards (discovery): Then it will lead to the 2 cases and we need to use another lemma which is what we did in approach 1.
> 
> **Why Contrapositive / Forward Proof Saves Us:** When you prove the **contrapositive** $(a\geq b\geq 0\implies a^{2}\geq b^{2})$
> 
> No ambiguity about signs, no two-case branches
>
>The second approach is about generalization we generalize the problem to become small $\times$ small and big $\times$ big


iii) $5-x^{2}<-2$

$$
\begin{align}
6-x^{2}&<-2 \\
8-x^{2}&<0 \\
-x^{2}&<-8 \\
x^{2}&>8 &&\text{By 5(ii)} \\
x&> \sqrt{ 8 } \text{ or }x<-\sqrt{ 8 }
\end{align}
$$

iv)
$$
(x-1)(x-3)>0
$$
By [[Basic Properties of Numbers#^84b7a2]] , it follow that

Case 1: $(x-1)>0$ and $(x-3)>0$. 
Thus, $x>1$ and $x>3$. Thus, $x>3$

Case 2: $(x-1)<0$ and $(x-3)<0$.
Thus, $x<1$ and $x<3$. Thus, $x<1$.

Thus, it is $x>3$ or $x<1$.. $(-\infty,1)\cup(3,\infty)$.


v) $x^{2}-2x+2>0$

$$
\begin{align}
x^{2}-2x+2&>0 \\
x^{2}-2x+(-1)^{2}-(-1)^{2}+2&>0 \\
(x-1)^{2}+1&>0 \\
\end{align}
$$

Since $(x-1)^{2}\geq 0$ (corollary 10), thus $(x-1)^{2}+1>0$ for all $x\in \mathbb{R}.$

vi) $x^{2}+x+1>2$. ^7861ef

$$
\begin{align}
x^{2}+x+1&>2 \\
x^{2}+x-1&>0 \\
\left( x+\frac{1}{2} \right)^{2}-\left( \frac{1}{2} \right)^{2}-1&>0 \\
\left( x+\frac{1}{2} \right)^{2}-\frac{5}{4}&>0 \\
\left( x+\frac{1}{2} \right)^{2}&> \frac{5}{4} \\
x+\frac{1}{2} >\sqrt{ \frac{5}{4} } &\text{ or }x+\frac{1}{2}<-\sqrt{ \frac{5}{4} }
\end{align}
$$

by Corollary 10.

$$
\begin{align}
x&> \sqrt{ \frac{5}{4} }-\frac{1}{2} \\
&>\sqrt{ \frac{5}{4}-\frac{1}{4} } \\
&> \sqrt{ 1 } \\
&>1
\end{align}
$$
or
$$
\begin{align}
x&<-\sqrt{ \frac{5}{4} }-\frac{1}{2} \\
&<-\left( \sqrt{ \frac{5}{4} } +\frac{1}{2}\right) \\
&<-\sqrt{ \frac{5}{4}+\frac{1}{4} } \\
&<-\sqrt{ \frac{3}{2} }
\end{align}
$$

Thus, $x\in \left\{  x\in \mathbb{R}: x<-\sqrt{ \frac{3}{2} } \text{ or }x>1  \right\}$ (set builder notation) or $x\in\left( -\infty,-\sqrt{ \frac{3}{2} } \right)\cup(1,\infty)$


viii) $x^{2}-x+10>16$

$$
\begin{align}
x^{2}-x+10&>16 \\
x^{2}-x-6&>0 \\
(x-3)(x+2)&>0
\end{align}
$$
Case 1: $(x-3)<0$ and $x+2<0$.
Then $x<3$ and $x<-2$. Thus, $x<-2$.

Case 2: $(x-3)>0$ and $(x+2)>0$
Then $x>3$ and $x>-2$. Thus, $x>3$.

Thus, $x\in(-\infty,-2)\cup(3,\infty)$

viii) $x^{2}+x+1>0$

$$
\begin{align}
x^{2}+x+1&>0 \\
\left( x+\frac{1}{2} \right)^{2}-\left( \frac{1}{2} \right)^{2}+1&>0 \\
\left( x+\frac{1}{2} \right)^{2}+\frac{3}{4}&>0
\end{align}
$$

Since $\left( x+\frac{1}{2} \right)^{2}\geq 0$ for any $x\in \mathbb{R}$. Thus, it follow that $\left( x+\frac{1}{2} \right)^{2}+\frac{3}{4}>0$.


ix) $(x-\pi)(x+5)(x-3)>0$ ^a1970c

By zero product property [[Basic Properties of Numbers#^6b5b8a]] , the expression $(x-\pi)(x+5)(x-3)=0$ when $x=\pi$ or $x=-5$ or $x=3$. By Trichotomy Law, the number except the 3 point on a number line is either positive or negative. So we just need prove that each point in that interval is positive or negative. 

How? we use arbitrary number in that interval. Do we need IVT? No, because we can prove from pure algebraic.

First we can split the number into 4 interval $(-\infty,-5)$ , $(-5,3)$, $(3,\pi)$, $(\pi,\infty)$.

Suppose an arbitrary number $x\in(-5,3)$. 
1) For first factor $(x+5)$:
From supposition, $x>-5\Leftrightarrow (x+5)>0\Leftrightarrow (x+5)\in P$.

2) For second factor $(x-3)$:
From supposition, $x<3\Leftrightarrow (x-3)<0 \Leftrightarrow (x-3)\in-P$

3) For third factor $(x-\pi):$
From supposition, we know that $x<3$ and $3<\pi$, by Transitivity Law, $x<\pi \Leftrightarrow (x-\pi)<0 \Leftrightarrow (x-\pi)\in-P$.

Using the lemma [[Basic Properties of Numbers#^1173ea]] for 2 times, we have $(-P)\cdot P\cdot(-P)\subseteq P$.

Thus, if $x\in(-5,3)$, then $(x+5)(x-3)(x-\pi)>0$.

Suppose an arbitrary number $x\in(-\infty,-5)$

1) For first factor $(x-5)$
From supposition $x<-5 \Leftrightarrow (x+5)<0 \Leftrightarrow (x+5)\in-P$

2) For second factor $(x-3):$
From supposition $x<-5$ and we know that $-5<-3$. Thus, by Transitivity Law $x<-3 \Leftrightarrow (x+3)<0 \Leftrightarrow (x+3)\in-P$

3) For third factor $(x-\pi):$
From supposition $x<-5$ and $-5<\pi$, thus by Transitivity Law $x<\pi \Leftrightarrow (x-\pi)<0 \Leftrightarrow (x-\pi)\in-P$.

Thus, by lemma it follow that $(x-5)(x-3)(x-\pi)<0$

For $x\in(3,\pi)$,  $(x-5)(x-3)(x-\pi)>0$
For $x\in(\pi,\infty)$, $(x-5)(x-3)(x-\pi)<0$. 

Thus, the answer is $x\in(-5,3)\cup(3,\pi)$ .

x) $(x-\sqrt[3]{  2})(x-\sqrt{ 2 })>0$

$$
\begin{align}
(x-\sqrt[3]{  2})(x-\sqrt{ 2 })&>0 \\
\end{align}
$$
Case 1: $(x-\sqrt[3]{2  })>0$ and $(x-\sqrt{ 2 })>0$. Thus,

$$
\begin{align}
x>\sqrt[3]{2  } \\
\end{align}
$$
and
$$
x>\sqrt{ 2 }
$$

Hence, $x>\sqrt{ 2 }$.

Case 2: $(x-\sqrt[3]{2  })<0$ and $(x-\sqrt{ 2 })<0$.
Thus,
$$
x<\sqrt[3]{ 2 }
$$
and
$$
x<\sqrt{ 2 }
$$
Hence, $x<\sqrt[3]{2  }$.

Combining 2 constraint $\sqrt[3]{2  }<x<\sqrt{ 2 }$.

xi) $2^{x}<8$.

$$
\begin{align}
2^{x}&<8 \\
2^{x}&<2^{3} \\
x&<3
\end{align}
$$
What is the reason for last step? Injectivity of exponent function.

xii) $x+3^{x}<4$

$$
\begin{align}
x+3^{x}&<4 \\

\end{align}
$$
When $x\geq1$, then $3^{x}\geq 3$, thus

$$
x+3^{x}\geq 4
$$
. Thus, by Trichotomy Law when $x<1$, then
$$
x+3^{x}<4
$$

xiii) $\frac{1}{x}+\frac{1}{1-x}>0$

$$
\begin{align}
\frac{1}{x}+\frac{1}{1-x}&>0 \\
\frac{1}{x(1-x)}&>0&&\text{By 3(i)}  \\
\end{align}
$$

Since $1>0$, thus it follow that $x(1-x)>0$. 

Case 1: $x>0$ and $(1-x)>0\implies x<1$:

Case 2: $x<0$ and $(1-x)<0\implies x>1$. The $x$ does not exist for this case.

Therefore, $x\in(0,1)$

![[Pasted image 20260827183737.png]]

Limit 
When numerator degree is less than the denominator, then horizontal asymptotes is at $y=0$, because when $x\to \infty$, $y\to{0}$ 

When numerator degree is same with denominator, then horizontal asymptotes $y=\frac{a}{b}$ where $\frac{a}{b}$ is the ratio of leading coefficient.

When numerator degree is more than denominator, then it is a slant aysmptotes.

xiv) $\frac{x-1}{x+1}>0$ ^8f0414

Case 1: $x-1>0$ and $x+1> 0$
Thus, $x>1$ and $x>-1$. Hence, $x>1$

Case 2: $x-1<0$ and $x+1<0$
Thus, $x<1$ and $x<-1$. Hence, $x<-1$.

Thus, $x\in(-\infty,-1)\cup(1,\infty)$

5） [[Basic Properties of Numbers#^7d98e7]]

6) a) Prove that if $0\leq x<y$, then $x^{n}<y^{n}$, $n ={1},2,3,\dots$
Thinking process:
We need to use 5(viii) $0\leq a<b$ and $0\leq c<d$, then $ac<bd$ multiple times. We need use mathematical induction to prove.

The statement $P_{n}$: If $0\leq x<y$, then $x^{n}<y^{n}$, $n ={1},2,3,\dots$ 
For basis step, $P_{1}$ is true by assumption and $P_{2}$ is true because by 5(viii) $0\leq x<y\implies x \times x<y \times y\implies x^{2}<y^{2}$.

For inductive step, suppose $n$ is an arbitrary positive integer and $P_{n}$ is true . We need to prove for $P_{n+1}$.

Suppose $0\leq x<y$. From our inductive hypothesis we know that $x^{n}<y^{n}$. Since $x<y$, by 5(viii), it follow that 

$$
\begin{align}
x^{n}\cdot x&<y^{n}\cdot y \\
x^{n+1}&<y^{n+1}
\end{align}
$$
Thus, $P_{n}$ is true for all $n\in \mathbb{Z}^{+}$.$\blacksquare$

b) Prove that if $x<y$ and $n$ is odd, then $x^{n}<y^{n}$ ^453eb8

Proof: 
Case 1: $x,y<0$
Then, $x<y\implies -x>-y$. Notice that $-x,-y\in P$. Thus, by 6(a), $(-x)^{n}>(-y)^{n}\implies-x^{n}>-y^{n}\implies x^{n}<y^{n}$.

Case 2: $x,y>0$
Then by 6(a), $x^{n}<y^{n}$. 

Case 3: $x,y$ have opposite sign
WLOG suppose $x<0$ and $y>0$. Since $n$ is an arbitrary odd integer, it follow that $x^{n}<0$ and $y^{n}>0$. Thus, by Transitivity Law

$$
\begin{align}
x^{n}<y^{n}&&\blacksquare
\end{align}
$$

c) Prove that if $x^{n}=y^{n}$ and $n$ is odd, then $x=y$. ^d068da

Proof (Wrong version):
$$
\begin{align}
x^{n}&=y^{n} \\
(x^{n})^{1/n}&=(y^{n})^{1/n} \\
x&=y&&
\end{align}
$$
It is wrong to prove like this, because it is a circular step by assuming the $n-th$ root is a well-defined and bijective.

Proof:
We prove by contrapositive. Suppose $n$ is odd ,if $x \neq y$, then $x^{n}\neq y^{n}$. By Trichotomy Law, there are 2 cases. WLOG, suppose $x<y$, then by 6(b), it follow that $x^{n}<y^{n}$. Thus, $x^{n} \neq y^{n}$. $\blacksquare$

Remark
The first thing we should think is what is the relation of 6(b) and 6(c), since both concern about odd number. One is inequality and one is equality. And it seem to be the converse of each other.

We have now establish the strict injectivity of odd power function on all of $\mathbb{R}$.

d) Prove that if $x^{n}=y^{n}$ and $n$ is even, then $x=y$ or $x=-y$.
Thinking process:
We prove using contrapositive. 
Suppose $n$ even, if $x>y$ and $x>-y$, then $x^{n}>y^{n}$  (This is one of the 2 cases).
Or another version, since even power only care about the **magnitudes** , thus we can rewrite the statement into $x>|y|$. Notice that $|y|>0$, thus we can rewrite the statement into if $|x|>|y|$, then $x^{n}>y^{n}$.

> [!theorem] Lemma
> For any number $a$, if $n$ is an even number then
> $$
> |a|^{n}=a^{n}
> $$

Proof of lemma:
Suppose $n$ is an even number and $a$ is an arbitrary real number.

Case 1: $a\geq0$
By definition $|a|=a$, thus $|a|^{n}=a^{n}$.

Case 2: $a<0$
By definition $|a|=-a\implies|a|^{n}=(-a)^{n}$. Since $n$ is even number, it follow that $(-a)^{n}=a^{n}$. Thus, $|a|^{n}=a^{n}$. 

In each case $|a|^{n}=a^{n}$. $\blacksquare$

Proof 1 case of contrapositive:
Suppose $n$ is even and $|x|>|y|$. Since $|x|\geq 0$ and $|y|\geq 0$, by 6(a) it follow that 
$$
|x|^{n}>|y|^{n}
$$
By lemma above, it follow that

$$
\begin{align}
x^{n}>y^{n}&&\blacksquare
\end{align}
$$

Proof of 6(d):
We prove using contrapositive. By Trichotomy Law, it is either $|x|>|y|$ or $|x|<|y|$. WLOG, suppose $|x|>|y|$.... ^8a638a

> [!remark]
> Question 6 is about monotonicity to injectivity $x_{1}<x_{2}\implies f(x_{1})<(>)f(x_{2})$ implies that $f(x_{1})=f(x_{2})\implies x_{1}=x_{2}$ .



7) Prove that if $0<a<b$, then

$$
a<\sqrt{ ab }< \frac{a+b}{2}<b
$$
Notice that the inequality $\sqrt{ ab }\leq \frac{a+b}{2}$ holds for all $a,b\geq 0$. A generalization of this fact occurs in Problem 2-22.

Proof:
$$
\begin{align}
a&<b \\
a^{2}&<ab &&\text{By 5(iv)} \\
a&<\sqrt{ ab } &&\text{By 5(x)}
\end{align}
$$
(First inequality)
Notice that $$ \begin{align} a^{2}+b^{2}&=(a+b)^{2}-2ab \\ (a+b)^{2}&=a^{2}+b^{2}+2ab \end{align} $$
Since $a^{2}+b^{2}>0$, it follow that

$$
\begin{align}
(a+b)^{2}&> 2ab \\
\sqrt{ 2ab }&<a+b \\
\end{align}
$$

We want $\sqrt{ 4ab }$, the inequality we got above is too loose because it threw away the relationship between $a^{2}+b^{2}$ and $2ab$ (we want another $2ab$), we want something like $a^{2}+b^{2}>2ab$

Consider $(a-b)^{2}$

$$
\begin{align}
(a-b)^{2}&>0 \\
a^{2}-2ab+b^{2}&>0 \\
a^{2}+b^{2}&>2ab
\end{align}
$$

By substitution

$$
\begin{align}
(a+b)^{2}&>4ab \\
a+b&>2\sqrt{ ab } \\
\frac{a+b}{2}&>\sqrt{ ab }
\end{align}
$$

(Second inequality)

Another approach of 
Notice that
$$
\begin{align}
(\sqrt{ a }-\sqrt{ b })^{2}&=a-2\sqrt{ ab }+b \\ 
2\sqrt{ ab }&=a+b-(\sqrt{ a }-\sqrt{ b })^{2}
\end{align}
$$

Since $(\sqrt{ a }-\sqrt{ b })^{2}> 0$, it follow that

$$
\begin{align}
2\sqrt{ ab }&>a+b \\
 \\
\sqrt{ ab }&> \frac{a+b}{2} &&\blacksquare
\end{align}
$$

Why we didn't choose $(\sqrt{ a }+\sqrt{ b })^{2}$ ? It is because it produce a plus sign in front of the cross term $+2\sqrt{ ab }$.

8) Although the basic properties of inequalities were stated in terms of the collection $P$ of all positive numbers, and $<$ was defined in term of $P$, this procedure can be reversed. Suppose that P10-P12 are replaced by

P'10) For any numbers $a$ and $b$ one, and only  one, of the following holds:
i) $a=b$
ii) $a<b$
iii) $b<a$

P'11) (Transitivity Law)
For any numbers $a,b$ and $c$ if $a<b$ and $b<c$, then $a<c$. 

P'12) (Additive property of inequality)
For any numbers $a,b$ and $c$, if $a<b$, then $a+c<b+c$

P'13)(Positive multiplicative property of inequality)
For any numbers $a,b$ and $c$, if $a<b$ and $0<c$, then $ac<bc$.

Show that $P 10-P 12$ can then be deduced as theorem.

Proof P10(Trichotomy Law):
Suppose $a$ is an arbitrary number and $b=0$. Thus, by P'10),  it follow that one of the following holds:
i) $a=0$
ii) $a<0$
iii) $0<a$ 

By definition 
i) $a=0$
ii) $a<0\implies a+(-a)<-a\implies 0<-a$. Thus, $-a\in P$
iii) $0<a\implies a>0\implies a\in P$ $\blacksquare$


Proof of P11 (Closure of $P$ under addition):
Suppose 2 arbitrary number $a,b\in P$. By definition $a>0$ and $b>0$. By P'12) (add $b$ to both side of $0<a$), it follow that 
 
$$
a+b>b
$$
Since $b>0$, by P'11) , it follow that

$$
\begin{align}
a+b>0\implies a+b\in P &&\blacksquare
\end{align}
$$

Proof of P12 (Closure of $P$ under multiplication):
Suppose $2$ arbitrary number $a,b\in P$. By definition $a>0$ and $b>0$. By P'13) (Multiplying both side of $a>0$ with $b$ ), it follow that

$$
\begin{align}
ab>0\implies ab\in P &&\blacksquare
\end{align}
$$


9) Express each of the following with at least one less pair of absolute value signs.

i) $|\sqrt{ 2 }+\sqrt{ 3 }-\sqrt{ 5 }+\sqrt{ 7 }|$

Notice that $\sqrt{ 7 }-\sqrt{ 5 }>0$, $\sqrt{ 2 }>0$ and $\sqrt{ 3 }>0$. Thus, 

$$
|\sqrt{ 2 }+\sqrt{ 3 }-\sqrt{ 5 }+\sqrt{ 7 }|=\sqrt{ 2 }+\sqrt{ 3 }-\sqrt{ 5 }+\sqrt{ 7 }
$$

ii) $|(|a+b|-|a|-|b|)|$
By triangle inequality, we know that $|a|+|b|\geq|a+b|$. Thus, the answer is $-(|a+b|-|a|-|b|)$.

iii) $|(|a+b|+|c|-|a+b+c|)|$ 

Let $d=a+b$, thus by triangle inequality $|d|+|c|\geq|d+c|$. Thus, the answer is $(|a+b|+|c|-|a+b+c|)$, 

iv) $|x^{2}-2xy+y^{2}|$
$$
\begin{align}
|x^{2}-2xy+y^{2}|=|(x-y)^{2}| 
\end{align}
$$
Since $(x-y)^{2}\geq 0$, it follow that the answer is $(x^{2}-2xy+y^{2})$.

v) $|(|\sqrt{ 2 }+\sqrt{ 3 }|-|\sqrt{ 5 }-\sqrt{ 7 }|)|$

Since $\sqrt{ 5 }-\sqrt{ 7 }<0$, it follow that $|\sqrt{ 5 }-\sqrt{ 7 }|=-(\sqrt{ 5 }-\sqrt{ 7 })$ and since $(\sqrt{ 2 }+\sqrt{ 3 })> 0$, it follow that $|(\sqrt{ 2 }+\sqrt{ 3 })|=(\sqrt{ 2 }+\sqrt{ 3 })$ Thus,

$$
|(\sqrt{ 2 }+\sqrt{ 3 })+(\sqrt{ 5 }-\sqrt{ 7 })|
$$

Notice that $(\sqrt{ 2 }+\sqrt{ 5 })^{2}=7+2\sqrt{ 10 }>7$. Thus, it follow that $\sqrt{ 2 }+\sqrt{ 5 }>\sqrt{ 7 }$. Hence, it follow that the answer is

$$
\begin{align}
\sqrt{ 2 }+\sqrt{ 3 }+\sqrt{ 5 }-\sqrt{ 7 }
\end{align}
$$


Is $(\sqrt{ 2 }+\sqrt{ 5 })^{2}$ is the only option? No we can also chose $(\sqrt{ 3 }+\sqrt{ 5 })^{2}$. Then what is the condition? 

$$
(\sqrt{ a }+\sqrt{ b })^{2}=a+b+2\sqrt{ ab }
$$
 Once we make sure $a+b>\text{(Target term)}^{2}$ , then since $2\sqrt{ ab }>0$, we can conclude that $\sqrt{ a }+\sqrt{ b }>\text{Target term}$.

The General Law: $\sqrt{ a }+\sqrt{ b }> \sqrt{ a+b }$.

Square of the sum: $(\sqrt{ a }+\sqrt{ b })^{2}=a+b+2\sqrt{ ab }$
Square of the Combined Radical: $(\sqrt{ a+b })^{2}=a+b$

Since $2\sqrt{ ab }>0$, it follow that

$$
(\sqrt{ a }+\sqrt{ b })^{2}-(\sqrt{ a+b })^{2}=2\sqrt{ ab }>0
$$

10) Express each of the following without absolute value signs, treating various cases separately when necessary.

i) $|a+b|-|b|$ 

Case 1: $a+b\geq0$ and $b\geq 0$.
Then, $|a+b|-|b|=a+b-b=a$

Case 2: $a+b<0$ and $b\geq 0$:
Then $|a+b|-|b|=-(a+b)-b=-a-2b$

Case 3: $a+b\geq 0$ and $b<0$:
Then $|a+b|-|b|=a+b+b=a+2b$

Case 4: $a+b< 0$ and $b<0$
Then $|a+b|-|b|=-(a+b)+b=-a$


ii) $|(|x|-1)|$ ^471dd7

Case 1: $|x|\geq 1$ 
$$
\begin{align}
|(|x|-1)|=(|x|-1)
\end{align}
$$
Case 1.1: $x\geq1$
Then the answer is $x-1$

Case 1.2: $x\leq -1$
Then the answer is $-x-1$.

Case 2: $|x|< 1$
$$
|(|x|-1)|=-(|x|-1)
$$

Case 2.1: $0\leq x<1$ 
Then the answer is $-(x-1)=1-x$

Case 2.2: $-1<x<0$.
Then the answer is $-(-x-1)=x+1$

iii) $|x|-|x^{2}|$
Since $x^{2}\geq 0$, it follow that $|x^{2}|=x^{2}$. Thus

$$
|x|-|x^{2}|=|x|-x^{2}
$$
Case 1: $x\geq 0$
Then $|x|-x^{2}=x-x^{2}$

Case 2: $x< 0$
Then $|x|-x^{2}=-x-x^{2}$

iv) $a-|(a-|a|)|$

Case 1: $(a-|a|)\geq 0\implies|a|\leq a$. Since $|a|\geq a$ (Lemma) , it follow that $|a|=a$. Then $a-(a-a)=a$

Case 2: $(a-|a|)< 0\implies |a|> a\implies|a| \neq a\implies |a|=-a$.
Thus, the answer is $a+(a+a)=3a$. 


11) Find all numbers $x$ for which
i) $|x-3|=8$

Case 1: $x-3\geq 0\implies x\geq 3$
$$
\begin{align}
x-3&=8 \\
x&=11
\end{align}
$$

Case 2: $x-3< 0\implies x<3$

$$
\begin{align}
-(x-3)&=8 \\
x-3&=-8 \\
x&=-5
\end{align}
$$
ii) $|x-3|<8$

Case 1: $0\leq(x-3)<8\implies 3\leq x<11$

Case 2: $-8<(x-3)<0\implies-5<x<3$

Thus, combining 2(or) is $-5< x<11$

> [!question] What does that mean $|x-3|<8$?
> it means that the magnitude (absolute value) of $x-3$ is less than 8. It can be 2 cases one is the positive side and one is the negative side.
> 
> $$
> |x-c|<r
> $$
> means the distance between $x$ and the center $c$ is strictly less than $r$.

iii) $|x+4|<2$

Case 1: $0\leq x+4<2\implies -4\leq x<-2$

Case 2: $-2<x+4<0\implies -6<x<-4$

Thus, combining 2 become $-6<x<-2$


iv) $|x-1|+|x-2|>1$ ^c215e8

$$
\begin{align}
|x-1|&>1-|x-2| \\
(x-1)^{2}&>(1-|x-2|)^{2} \\
\end{align}
$$

It is wrong because $(1-|x-2|)$ can be negative, recall 6a) $0\leq x<y\implies x^{n}<y^{n}$ when $n ={1},2,3,\dots$. This is because both odd and even number is monotonic in positive domain. But if odd power is global monotonic, while even only positive monotonic. So we need to make sure the term is non negative.

We find the critical point $|x-1|=0\implies x=1$ and $|x-2|=0\implies x=2$

Thus, we can divide the entire real line into 3 interval:

1) Interval 1: $x<1$
2) Interval 2: $1\leq x\leq 2$
3) Interval 3: $x>2$

When $x<1$, then $x-1<0\implies|x-1|>0$
and  $x-2<-1\implies|x-2|> 1$. Thus,

$$
|x-1|+|x-2|>1
$$

When $1\leq x\leq 2$, then $0\leq x-1\leq1\implies 0\leq|x-1|\leq 1$ and $-1\leq x-2\leq{0}\implies 0\leq|x-2|\leq 1$

Thus,

$$
0\leq|x-1|+|x-2|\leq 2
$$
This inequality is too loose. Since $x\geq 1\implies |x-1|=x-1$ and since $x\leq 2\implies|x-2|=-(x-2)=2-x$. Thus,

$$
\begin{align}
|x-1|+|x-2|=(x-1)+(2-x)=1
\end{align}
$$

When $x>2$, then
$x-1>1\implies|x-1|> 1$ and $x-2>0\implies|x-2|> 0$

Thus,

$$
|x-1|+|x-2|>1
$$
Hence the answer is $x\in(-\infty,1)\cup(2,\infty)$

> [!remark]
> If $a<b$ and $c<d$, then $a+c<b+d$ 5(i)

Notice that it is better we convert to equation for the case $x<1$ or $x>2$. 

When $x<1$, then $x-1<0\implies|x-1|=-(x-1)$ and $x-2<-1\implies|x-2|=-(x-2)$. Thus,

$$
\begin{align}
|x-1|+|x-2|&=-(x-1)-(x-2) \\
&=-2x+3
\end{align}
$$
Now we solve the inequality

$$
\begin{align}
-2x+3&>1 \\
-2x&>-2 \\
x&<1
\end{align}
$$
(It match the interval perfectly)

When $x>2$, then $x-1>1\implies|x-1|=x-1$ and $x-2>0\implies|x-2|=x-2$. Thus,

$$
\begin{align}
|x-1|+|x-2|&=x-1+x-2 \\
&=2x-3
\end{align}
$$
Solve the inequality

$$
\begin{align}
2x-3&>1 \\
2x&>4 \\
x&>2
\end{align}
$$
(It match the interval perfectly)

v) $|x-1|+|x+1|<2$

When $|x-1|=0\implies x=1$
When $|x+1|=0\implies x=-1$

Thus, we can split into 3 invariant interval:

Case 1: when $x<-1$
Then $x-1<-2\implies|x-1|=-(x-1)$ and $x+1<0\implies|x+1|=-(x+1)$. Thus,

$$
\begin{align}
|x-1|+|x+1|&=-(x-1)-(x+1) \\
&=-2x
\end{align}
$$

We solve for the inequality:

$$
\begin{align}
-2x&<2 \\
x&>-1
\end{align}
$$
Since it is not in the interval, thus $|x-1|+|x+1|\geq 2$.

Case 2: $-1\leq x\leq 1$
Then $-2\leq x-1\leq0$. Thus, $|x-1|=-(x-1)$ and since $0\leq x\leq 2$. Thus, $|x+1|=x+1$.

$$
\begin{align}
|x-1|+|x+1|&=-(x-1)+x+1 \\
&=2
\end{align}
$$
Since $2\not<2$, it follow that $|x-1|+|x+1|\geq 2$.

Case 3: $x> 1$.
Then $x-1>0\implies|x-1|=x-1$ and $x+1>2\implies|x+1|=x+1$. Thus,

$$
\begin{align}
|x-1|+|x+1|&=x-1+x+1 \\
&=2x
\end{align}
$$
we solve for the inequality:

$$
\begin{align}
2x&<2 \\
x&<1
\end{align}
$$
Since it is not in the domain, it follow that $|x-1|+|x+1|\geq 2$,

Hence, the is no solution for this inequality.

vi) The same as above

vii) $|x-1|\cdot|x+1|=0$

$|x-1|=0\implies x=1$ and $|x+1|=0\implies x=-1$. Thus, we can split into 3 interval:

Case 1: $x<-1$
$x-1<-2\implies|x-1|=-(x-1)$ and $x+1<0\implies|x+1|=-(x+1)$. Thus,

$$
\begin{align}
-(x-1)\cdot-(x+1)&=0 \\
(x-1)\cdot(x+1)&=0\\
x&=\begin{cases}
1 &\text{if }(x-1)=0\\
-1&\text{if }(x+1)=0
\end{cases}
\end{align}
$$
Since $x$ is not in the domain, it follow that $|x-1|\cdot|x+1|\neq 0$.

Case 2: $-1\leq x\leq 1$
$-2\leq x-1\leq 0\implies|x-1|=-(x-1)$ and $0\leq x+1\leq 2\implies|x+1|=x+1$. Thus,

$$
\begin{align}
-(x-1)\cdot(x+1)&=0 \\
x&=\begin{cases}
1 &\text{if }(x-1)=0\\
-1&\text{if }(x+1)=0
\end{cases}
\end{align}
$$

Case 3: $x> 1$
$x-1>0\implies|x-1|=x-1$ and $x+1>2\implies|x+1|=x+1$. Thus,

$$
\begin{align}
(x-1)\cdot(x+1)&=0 \\
x&=\begin{cases}
1&\text{if }(x-1)=0 \\
-1&\text{if }(x+1)=0
\end{cases}
\end{align}
$$
Since $x$ is not in the domain, it follow that $|x-1|\cdot|x+1| \neq 0$.

Hence the answer is $x=1$ or $x=-1$. 

Another approach: By zero product property it is $|x-1|=0$ or $|x+1|=0$.

Case 1: $|x-1|=0\implies x=1$
Case 2: $|x+1|=0\implies x=-1$.

viii) $|x-1|\cdot|x+2|=3$

> [!theorem] Lemma 12(i):
> $|xy|=|x|\cdot|y|$
> 

$$
\begin{align}
|x-1|\cdot|x+2|&=3 \\
|(x-1)\cdot(x+2)|&=3 \\
|x^{2}+x-2|&=3 \\
\end{align}
$$

Case 1: $x^{2}+x-2\geq 0$. Thus, $|x^{2}+x-2|=x^{2}+x-2$

$$
\begin{align}
x^{2}+x-2&=3 \\
x^{2}+x-5&=0 \\
\left( x+\frac{1}{2} \right)^{2}-\frac{1}{4}-5&=0 \\
\left( x+\frac{1}{2} \right)^{2}&=\frac{21}{4} \\
x+\frac{1}{2}&=\pm\frac{\sqrt{ 21 }}{2} \\
x&=\pm \frac{\sqrt{ 21 }}{2}-\frac{1}{2}
\end{align}
$$

Case 2: $x^{2}+x-2<0$. Thus, $|x^{2}+x-2|=-(x^{2}+x-2)$

$$
\begin{align}
x^{2}+x-2&=-3 \\
x^{2}+x+1&=0 \\
\left( x+\frac{1}{2} \right)^{2}-\frac{1}{4}+1&=0 \\
\left( x+\frac{1}{2} \right)^{2}&=-\frac{3}{4}
\end{align}
$$
No $x$ that satisfy the equation.

Thus, the answer is $x=\pm \frac{\sqrt{ 21 }}{2}-\frac{1}{2}$

> [!remark]
> We can also use critical point partition rule to do this

12) Prove the following:
i) $|xy|=|x|\cdot|y|$

Proof:
We prove by cases.

Case 1: $x\geq 0$ and $y\geq 0$.
Thus, by definition, $|x|=x$ and $|y|=y$. Notice that $xy\geq 0$ (P12 Closure of $P$ on multiplication). Thus, $|xy|=xy$. Hence,

$$
\begin{align}
|x|\cdot|y|&=xy=|xy|
\end{align}
$$

Case 2: WLOG, $x<0$ and $y\geq 0$.
Thus, $xy\leq 0\implies|xy|=-xy$. Notice that $|x|=-x$ and $|y|=y$. Thus,

$$
\begin{align}
|xy|&=-xy=|x|\cdot|y|
\end{align}
$$
Case 3: $x<0$ and $y<0$
Thus, $xy> 0\implies|xy|=xy$. Notice that $|x|=-x$ and $|y|=-y$. Thus,

$$
\begin{align}
|xy|=xy=(-x)\cdot(-y)&=|y|\cdot|x|&& \blacksquare
\end{align}
$$

ii) $| \frac{1}{x}|=\frac{1}{|x|}$, if $x\neq 0$. (The best way to do this is to remember what $|x|^{-1}$ is)

First attempt:
Notice that $|\frac{1}{x}|=|x|^{-1}$ and $|x|\cdot|x|^{-1}=1$. Thus,

$$
\begin{align}
|\frac{1}{x}|\cdot|x|&=1 \\
| \frac{1}{x}|&=\frac{1}{|x|} &&
\end{align}
$$
Wrong because we assume that $|\frac{1}{x}|=|x^{-1}|=|x|^{-1}$ which is what we are trying to prove.

Another attempt:

$$
\begin{align}
| \frac{1}{x}|&=|1\cdot x^{-1}| \\
&=|1|\cdot|x^{-1}| &&\text{By 12(i)} \\
&=1\cdot|x^{-1}| \\
\end{align}
$$

Cannot because we don't know if $|x^{-1}|=|x|^{-1}$.

Third attempt:
We start with the multiplicative inverse property (P7):

$$
\begin{align}
x\cdot \frac{1}{x}&=1 \\
|x\cdot \frac{1}{x}|&=|1| \\
|x|\cdot| \frac{1}{x}|&=1 \\
| \frac{1}{x}|&= \frac{1}{|x|} &&\blacksquare
\end{align}
$$

iii) $\frac{|x|}{|y|}=| \frac{x}{y}|$, if $y\neq 0$.

Proof:

$$
\begin{align}
\frac{|x|}{|y|}&=|x|\cdot|y|^{-1} \\
&=|x|\cdot|y^{-1}|&&\text{By 12(ii)} \\
&=|x\cdot y^{-1}| &&\text{Bt 12(i)}\\
&= | \frac{x}{y}| &&\blacksquare
\end{align}
$$

iv) $|x-y|\leq|x|+|y|$ (Give a very short proof)

Proof:
By triangle inequality
$$
\begin{align}
|x|+|-y|\geq|x-y| \\
\implies|x|+|y|\geq|x-y|&&\blacksquare
\end{align}
$$

v) $|x|-|y|\leq|x-y|$. (A very short proof is possible, if you write things in the right way.) ^b45e11

Approach 1:

Notice that
$$
|x-y|^{2}=x^{2}-2xy+y^{2}
$$
and
$$
(|x|-|y|)^{2}=x^{2}-2|xy|+y^{2}
$$
Since $|xy|\geq xy$, it follow that

$$
\begin{align}
|x-y|^{2}&\geq (|x|-|y|)^{2} \\
\end{align}
$$
Case 1: $|x|-|y|\geq 0$. Then

$$
|x-y|\geq|x|-|y|
$$
because if $a,b\geq 0$, and $a^{2}>b^{2}$, then $a>b$. (Actually it is biconditional because square function is positive monotonic)

Case 2: $|x|-|y|<0$. 
Since $|x-y|\geq0$,  by transitivity law it follow that

$$
\begin{align}
|x-y|>|x|-|y|
\end{align}
$$
Thus, in both case $|x-y|\geq|x|-|y|$ $\blacksquare$


Approach 2:  ^b45e11
$$
\begin{align}
x=(x-y)+y \\
\end{align}
$$
By triangle inequality

$$
\begin{align}
|(x-y)+y|&\leq|x-y|+|y| \\
|x|&\leq|x-y|+|y| \\
|x|-|y|&\leq|x-y|&& \blacksquare
\end{align}
$$


> [!remark]
> How to understand this? (The Detour Principle)
> $|x-y|$ is the distance between $x$ and $y$, while $|y|$ is the distance from origin to $y$. So $|x-y|+|y|$ is like we go from origin to $y$ first and we go from $y$ to $x$.
> 
> if y is in the direction of x then they are equal, if y exceed x (stop at y and go back to x) or in opposite direction (stop y and now need to go for a longer distance to reach x), then $|x|<|x-y|+|y|$.
> 
> How it related to the proof:
> It is a sum of 2 absolute value, so we can always use the triangle inequality

vi) $|(|x|-|y|)|\leq|x-y|$ (Why does this follow immediately from (v)?)

$|(|x|-|y|)|$ is the difference (in positive, in (v) it can be negative and this is the crucial key because in absolute value the difference of 2 term is symmetry) of  distance between origin and $x,y$ in the same direction. For example $y=-2$ and $x=3$, then the difference in same direction is 1.

But $|x-y|$ is the distance of $x$ and $y$ which 5 in earlier case.

Proof:
Case 1: $|x|-|y|<0$, then $|(|x|-|y|)=|y|-|x|$
by 12(v), it follow that
$$
\begin{align}
|y|-|x|\leq|y-x|
\end{align}
$$

Notice that $|x-y|=|y-x|$ . Thus,
$$
\begin{align}
|y|-|x|&\leq|x-y|
\end{align}
$$

Case 2: $|x|-|y|\geq 0$, then $|(|x|-|y|)|=|x|-|y|$. By 12(v), it follow that

$$
\begin{align}
|x|-|y|\leq|x-y| &&\blacksquare
\end{align}
$$

viii) $|x+y+z|\leq|x|+|y|+|z|$. Indicate when equality holds, and prove your statement.

The equality hold in 2 cases:
Case 1: $x,y,z\geq 0$
Then, $|x|=x,|y|=y,|z|=z$ and , $x+y+z\geq 0$. Thus, $|x+y+z|=x+y+z$. Hence,

$$
|x+y+z|=x+y+z=|x|+|y|+|z|
$$

Case 2: $x,y,z< 0$
Then $|x|+|y|+|z|=-x-y-z$ and $x+y+z< 0\implies|x+y+z|=-x-y-z$. Hence,

$$
|x+y+z|=-x-y-z=|x|+|y|+|z|
$$

But the derivation only prove the forward direction, we need to show these are the only cases (which is the biconditional) $|x+y+z|=|x|+|y|+|z|\implies x,y,z$ have same sign.

We need to use 2 times triangle inequality 
$$
|(x+y)+z\leq|x+y|+|z|
$$
and
$$
|x+y|\leq|x|+|y|
$$
When does the $|x+y|=|x|+|y|$?
$$
|x+y|^{2}=x^{2}+2xy+y^{2}
$$
and
$$
(|x|+|y|)^{2}=x^{2}+2|xy|+y^{2}
$$
if $|x+y|=|x|+|y|$, then $2xy=2|xy|$

$$
\begin{align}
2xy&=2|xy| \\
xy&=|xy| \\
xy&\geq 0
\end{align}
$$
$xy\geq 0$ iff exactly one of the 2 cases below hold
1) $x\geq 0$ and $y\geq 0$
2) $x\leq0$ and $y\leq0$

Thus, $|(x+y)+z|=|(x+y)|+|z|$ iff
1) $x+y\geq 0$ and $z\geq 0$
2) $x+y\leq0$ and $z\leq0$

And from earlier result we know that $|x+y+z|=|x|+|y|+|z|$ iff
1) $x\geq 0$ and $y\geq 0$ and $z\geq 0$
2) $x\leq0$ and $y\leq0$ and $z\leq0$ $\blacksquare$

Proof of inequality:
Let $a=x+y$ and let $b=z$. Thus, by triangle inequality

$$
\begin{align}
|a+z|&\leq|a|+|z| \\
\end{align}
$$

By substitution,

$$
|x+y+z|\leq|x+y|+|z|
$$
By triangle inequality

$$
\begin{align}
|x+y|&\leq|x|+|y| \\
|x+y|+|z|&\leq|x|+|y|+|z|
\end{align}
$$

Thus, by transitivity law

$$
\begin{align}
|x+y+z|\leq|x|+|y|+|z| &&\blacksquare
\end{align}
$$

13) The maximum of two numbers x and y is denoted by max(x, y). Thus max $( - 1 , 3 ) = \operatorname* { m a x } ( 3 , 3 ) = 3$ and max $( - 1 , - 4 ) = \operatorname* { m a x } ( - 4 , - 1 ) = - 1$ The minimum of x and y is denoted by min(x, y). Prove that

$$
\max (x, y) = \frac {x + y + | y - x |}{2},
$$

$$
\min (x, y) = \frac {x + y - | y - x |}{2}.
$$

Derive a formula for $\operatorname* { m a x } ( x , y , z )$ and min $( x , y , z )$ , using, for example

$$
\max (x, y, z) = \max (x, \max (y, z)).
$$

Proof for max:
WLOG, suppose $x\geq y$. Then $y-x\leq 0\implies|y-x|=x-y$. Thus,

$$
\begin{align}
\frac{x+y+|y-x|}{2}&= \frac{x+y+(x-y)}{2} \\
&= \frac{2x}{2} \\
&=x \\
&=max(x,y) &&\blacksquare
\end{align}
$$

Proof for min:
WLOG, suppose $x\geq y$. Then $y-x\leq 0\implies|y-x|=x-y$. Thus,

$$
\begin{align}
\frac{x+y-|y-x|}{2}&= \frac{x+y-(x-y)}{2} \\
&=\frac{2y}{2} \\
&=y
\end{align}
$$
Formula for max(x,y,z)=max(x,max(y,z)):

$$
\begin{align}
\frac{x+max(y,z)+|max(y,z)-x|}{2}&= \frac{\frac{2x+y+z+|y-z|}{2}+|\frac{-2x+y+z+|y-z|}{2}|}{2} \\ 
&=\frac{2x+y+z+|y-z|+|(-2x+y+z+|y-z|)|}{4}
\end{align}
$$


Formula for min(x,y,z)=min(x,min(y,z)):

$$
\begin{align}
\frac{x+min(y,z)-|min(y,z)-x|}{2}&= \frac{2x+y+z-|y-z|-|(-2x+y+z-|y-z|)|}{4}
\end{align}
$$

14)(a) Prove that $| a | = | { - a } |$ . (The trick is not to become confused by too many cases. First prove the statement for $a \ge 0$ . Why is it then obvious for $a \leq 0 \mathrm { { ? } ) }$

Proof:
Case 1: $a\geq 0$
Then, $|a|=a$ and $-a< 0\implies|-a|=-(-a)=a$. Thus,
$$
|a|=a=-(-a)=|-a|
$$
Case 2: $a< 0$
Then, $|a|=-a$ and $-a> 0\implies|-a|=-a$. Thus,
$$
\begin{align}
|a|=-a=|-a| &&\blacksquare
\end{align}
$$

(b) Prove that $- b \leq a \leq b$ if and only if $| a | \leq b$ . In particular, it follows that $- | a | \leq a \leq | a |$

15)Prove that if $x$ and $y$ are not both $0$, then ^356df0
$$
\begin{array}
\ x^{2}+xy+y^{2}>0 \\
x^{4}+x^{3}y+x^{2}y^{2}+xy^{3}+y^{4}>0 \\
\end{array}
$$
Hint: Use Problem 1
Proof;
Suppose $x,y \neq 0$.

Case 1: Both are not zero
Case 1.1: $x=y$
Then $x^{2}>0$ and $y^{2}>0$ and $xy=x^{2}> 0$. Thus,

$$
x^{2}+xy+y^{2}>0
$$
Case 1.2: $x \neq y$.
Then, $x-y \neq 0$. Notice that

$$
\begin{align}
(x^{2}+xy+y^{2})&= \frac{x^{3}-y^{3}}{x-y}
\end{align}
$$
If $x>y$, then $x^{3}-y^{3}> 0$ (Monotonicity) and $x-y> 0$. Thus, 

$$
\begin{align}
(x^{2}+xy+y^{2})&= \frac{x^{3}-y^{3}}{x-y}> 0
\end{align}
$$

If $x<y$, then $x^{3}-y^{3}< 0$ and $x-y< 0$. Thus, 

$$
(x^{2}+xy+y^{2})= \frac{x^{3}-y^{3}}{x-y}> 0
$$

Case 2: Exactly one of them equal to zero
WLOG, let $x=0$ and $y \neq 0$. Thus, it follow that $x^{2}=0$ and $xy=0$ by Zero Product Property. Notice that $y^{2}>0$. Thus,

$$
\begin{align}
x^{2}+xy+y^{2}>0 &&\blacksquare
\end{align}
$$

Proof for second inequality:

Case 1: $x,y \neq 0$.
Case 1.1: $x=y$. Then, $x^{4}>0$ and $x^{3}y=x^{4}>0$ and $x^{2}y^{2}=x^{4}> 0$ and $y^{4}> 0$. Thus,

$$
x^{4}+x^{3}y+x^{2}y^{2}+xy^{3}+y^{4}>0
$$
Case 1.2: WLOG, $x>y$.
Notice that 

$$
\begin{align}
(x^{5}-y^{5})&=(x-y)(x^{4}+x^{3}y+x^{2}y^{2}+xy^{3}+y^{4}) \\
\end{align}
$$
$$
x^{4}+x^{3}y+x^{2}y^{2}+xy^{3}+y^{4}= \frac{x^{5}-y^{5}}{x-y}
$$
Since $x>y$, hence it follow that $x-y> 0$ and $x^{5}>y^{5}\implies x^{5}-y^{5}> 0$ . Thus,

$$
x^{4}+x^{3}y+x^{2}y^{2}+xy^{3}+y^{4}= \frac{x^{5}-y^{5}}{x-y}>0
$$
Case 2: WLOG $x=0$ and $y\neq 0$.
Thus, $x^{4}=0$ and $x^{3}y=0$ and $x^{2}y^{2}=0$ and $xy^{3}=0$ and $y^{4}>0$. Thus, it follow that

$$
\begin{align}
x^{4}+x^{3}y+x^{2}y^{2}+xy^{3}+y^{4}> 0 &&\blacksquare
\end{align}
$$

\*16. (a) Show that

$$
(x + y) ^ {2} = x ^ {2} + y ^ {2} \quad \text {   only   when   } x = 0 \text {   or   } y = 0,
$$

$$
(x + y) ^ {3} = x ^ {3} + y ^ {3} \quad \text{only when } x = 0 \text{ or } y = 0 \text{ or } x = - y.
$$

Proof of first statement:
It is a biconditional statement. Suppose $(x+y)^{2}=x^{2}+y^{2}$. Thus, 

$$
\begin{align}
(x+y)^{2}&=x^{2}+y^{2} \\
x^{2}+2xy+y^{2}&=x^{2}+y^{2} \\
2xy&=0 \\
xy&=0
\end{align}
$$
By zero product property it follow that $x=0$ or $y=0$. $\blacksquare$

Proof of second statement:
Suppose $(x+y)^{3}=x^{3}+y^{3}$

$$
\begin{align}
(x+y)^{3}&=x^{3}+y^{3} \\
x^{3}+3x^{2}y+3xy^{2}+y^{3}&=x^{3}+y^{3} \\
3x^{2}y+3xy^{2}&=0 \\
x^{2}y+xy^{2}&=0 \\
xy(x+y)&=0
\end{align}
$$
By zero product property, it follow that $x=0$ or $y=0$ or $x+y=0\implies x=-y$. $\blacksquare$. 


b) Using the fact that
$$
x^{2}+2xy+y^{2}=(x+y)^{2}\geq 0
$$
show that $4x^{2}+6xy+4y^{2}> 0$ unless $x$ and $y$ are both $0$.

> [!remark]
> $P$ unless $Q$ is equivalent to $\neg Q\implies  P$.
> 

$$
\begin{align}
4x^{2}+6xy+4y^{2}&=x^{2}+y^{2}+3x^{2}+6xy+3y^{2} \\
&=x^{2}+y^{2}+3(x^{2}+2xy+y^{2}) \\
\end{align}
$$
Notice that $x^{2}\geq 0$ and $y^{2}\geq 0$ and by the fact above $3(x^{2}+2xy+y^{2})\geq 0$. Thus,

$$
\begin{align}
x^{2}+y^{2}+3(x^{2}+2xy+y^{2})&\geq 0 \\
\end{align}
$$
Suppose $x$ and $y$ are not both zero ($\neg Q$)

Case 1: Exactly one of them is 0 
WLOG suppose $x=0$ and $y \neq 0$. Then $x^{2}=0$, $y^{2}> 0$ and $3(x^{2}+2xy+y^{2})=3(x+y)^{2}=3y^{2}> 0$. Thus

$$
\begin{align}
x^{2}+y^{2}+3(x^{2}+2xy+y^{2})&> 0 \\
\implies 4x^{2}+6xy+4y^{2}&> 0
\end{align}
$$
Case 2: $x,y \neq 0$
Then $x^{2}> 0$ and $y^{2}> 0$ and $3(x+y)^{2}\geq 0$. Thus,  we reach the same conclusion as case 1. $\blacksquare$.


c) Use part (b) to find out when $(x+y)^{4}=x^{4}+y^{4}$

$$
\begin{align}
(x+y)^{4}&=x^{4}+4x^{3}y+6x^{2}y^{2}+4xy^{3}+y^{4} \\
\end{align}
$$
Suppose $(x+y)^{4}=x^{4}+y^{4}$. Then $4x^{3}y+6x^{2}y^{2}+4xy^{3}=0$. Notice that 
$$
\begin{align}
4x^{3}y+6x^{2}y^{2}+4xy^{3}&=0 \\
xy(4x^{2}+6xy+4y^{2})&=0
\end{align}
$$
By zero product property, it follow that $x=0$ or $y=0$ or $4x^{2}+6xy+4y^{2}=0$.

The contrapositive of part (b) is $4x^{2}+6xy+4y^{2}=0\implies x=0$ and $y=0$.

So the answer is $x=0$ or $y=0$.$\blacksquare$

d) Find out when $(x+y)^{5}=x^{5}+y^{5}$

Suppose $(x+y)^{5}=x^{5}+y^{5}$. Notice that

$$
\begin{align}
(x+5)^{5}=x^{5}+5x^{4}y+10x^{3}y^{2}+10x^{2}y^{3}+5xy^{4}+y^{5}
\end{align}
$$
From assumption we can deduce that

$$
\begin{align}
5x^{4}y+10x^{3}y^{2}+10x^{2}y^{3}+5xy^{4}&=0 \\
5xy(x^{3}+2x^{2}y+2xy^{2}+y^{3})&=0
\end{align}
$$
By zero product property it follow that $x=0$ or $y=0$ or $x^{3}+2x^{2}y+2xy^{2}+y^{3}=0$

Suppose $x\neq 0$ and $y\neq 0$, then $x^{3}+2x^{2}y+2xy^{2}+y^{3}=0$. Notice that

$$
\begin{align}
x^{3}+2x^{2}y+2xy^{2}+y^{3}&=0 \\
x^{3}+y^{3}+2xy(x+y)&=0
\end{align}
$$
Notice that from Problem 1
$$
x^{3}+y^{3}=(x+y)(x^{2}-xy+y^{2})
$$
Thus,
$$
\begin{align}
(x+y)(x^{2}-xy+y^{2})+2xy(x+y)&=0 \\
(x+y)(x^{2}-xy+y^{2}+2xy)&=0 \\
(x+y)(x^{2}+xy+y^{2})&=0
\end{align}
$$

Thus, by zero product property $(x+y)=0$ or $(x^{2}+xy+y^{2})=0$. Notice that $x+y=0\implies x=-y$. From problem 15 (contrapositive), we know that $x^{2}+xy+y^{2}=0\implies x=0\text{ and }y=0$. $\blacksquare$. Thus, the answer is $x=-y$ or $(x=0\text{ and }y=0)$ or ($x=0\text{ or }y=0$). Since the second condition is subcase of 
third condition, it follow that the answer is $x=-y$ or $x=0$ or $y=0$.$\blacksquare$

> [!remark]
> We can make a guess about when $(x+y)^{n}=x^{n}+y^{n}$
> Case 1: When $n =2k$ for $k\in \mathbb{Z}$, then the answer is $x=0$ or $y=0$ (The middle term will become something like $x^{2}+y^{2}+a(x+y)^{2}$)
> Case 2: when $n =2k+1$ for $k\in \mathbb{Z}$, then the answer is $x=0$ or $y=0$ or $x=-y$ (The middle term will be like $x^{3}+y^{3}+\dots$ and we can factorize  the $x^{3}+y^{3}$ and factor out the same term so it become a product) 
> 
> Notice how the question is connected:
> 1. **Problem 1** developed the factorizations for difference and sum of powers 
> 2. **Problem 6(b)** established the strict monotonicity of odd powers ($x<y\implies x^{n}<y^{n}$)
> 3. **Problem 15** combined Problem 1 and Problem 6 to prove that the remaining polynomial factors $(x^{2}+xy+y^{2}\text{ and }x^{4}+\dots+y^{4})$ are strictly positive whenever $x,y$ are not both 0.
> 4. **Problem 16** reused that exact positivity from Problem 15 to prove that those factors can never equal zero, leaving only$x=0,y=0$ or $x=-y$.
> 
> Odd power use problem 15$\leftarrow 6\text{ and }1$, while even number use 16)b) \
> 
> What fundamental algebraic behavior separates between even power and odd power? 
> Is is because when $n$ is odd number, $-(a)^{n}=(-a)^{n}$, thus the middle term like $2x^{2}y+2xy^{2}$ cancel each other and leave $x^{5}+y^{5}$.
> 
> When $x=-y$ $(x+y)^{n}=(-y+y)^{n}=0$ while $x^{n}+y^{n}=(-y)^{n}+y^{n}=-y^{n}+y^{n}=0$. Because the order is changeable.

17)
a) Find the smallest possible value of $2x^{2}-3x+4$. Hint: "Complete the square" (Why?, because vertex form)

$$
\begin{align}
2x^{2}-3x+4&= 2\left( x^{2}-\frac{3}{2} x\right)+4 \\
&=2\left( x- \frac{3}{4} \right)^{2}- 2\left( \frac{9}{16} \right)+4 \\
&=2\left( x-\frac{3}{4} \right)^{2}-\frac{9}{8}+4 \\
&=2\left( x- \frac{3}{4} \right)^{2}+2 \frac{7}{8}
\end{align}
$$
The minimum value is $2 \frac{7}{8}$.

b) Find the smallest possible value of $x^{2}-3x+2y^{2}+4y+2$

$$
\begin{align}
x^{2}-3x+2y^{2}+4y+2&=\left( x-\frac{3}{2} \right)^{2}-\left( -\frac{3}{2} \right)^{2}+2(y+1)^{2} \\
&=\left( x-\frac{3}{2} \right)^{2}+2(y+1)^{2}-\frac{9}{4}
\end{align}
$$
Thus, the smallest value is $-\frac{9}{4}$

c) Find the smallest possible value of $x^{2}+4xy+5y^{2}-4x-6y+7$

$$
\begin{align}
x^{2}+4xy+5y^{2}-4x-6y+7&=(x+2y)^{2}+y^{2}-6y+7-4x \\ 
&=(x+2y)^{2}+(y-3)^{2}-(-3)^{2}+7-4x \\
&=(x+2y)^{2}+(y-3)^{2}-2-4x
\end{align}
$$
We still have a $x$, so it is not gonna work

$$
\begin{align}
x^{2}+4xy+5y^{2}-4x-6y+7&=x^{2}+(4y-4)x+(5y^{2}-6y+7) \\
&=(x+2y-2)^{2}-(2y-2)^{2}+(5y^{2}-6y+7) \\
&=(x+2y-2)^{2}-(4y^{2}-8y+4)+(5y^{2}-6y+7) \\
&=(x+2y-2)^{2}+y^{2}+2y+3 \\
&=(x+2y-2)^{2}+(y+1)^{2}+2
\end{align}
$$
The minimum value is 2

> [!remark]
> $x^{2}+(4y-4)x$ is the crucial step, we view $y$ as a coefficient of $x$ and divide 2


18)
(a) Suppose that $b ^ { 2 } - 4 c \geq 0$ . Show that the numbers

$$
\frac {- b + \sqrt {b ^ {2} - 4 c}}{2}, \quad \frac {- b - \sqrt {b ^ {2} - 4 c}}{2}
$$

both satisfy the equation $x ^ { 2 } + b x + c = 0 .$

$$
\begin{align}
x^{2}+bx+c&=0 \\
\left( x+\frac{b}{2} \right)^{2}-\left( \frac{b}{2} \right)^{2}+c&=0 \\
\left( x+\frac{b}{2} \right)^{2}&=-c+\frac{b^{2}}{4} \\
&=\frac{-4c+b^{2}}{4} \\
x+\frac{b}{2}&=\pm\frac{\sqrt{b^{2}-4c }}{2} \\
x&=\frac{-b\pm \sqrt{ b^{2}-4c }}{2}
\end{align}
$$

> [!remark]
> In this question we prove that $b^{2}-4c\geq 0\implies x^{2}+bx+c=0$. 
> Can we find the contrapositive? Can
> $x^{2}+bx+c \neq 0\implies b^{2}-4c< 0$. This is because although one of the component is equality but the another component is a inequality that include 2 cases. (Trichotomy Law only 3 cases). Thus, we no need to care about the order.

^af41ce


(b) Suppose that $b ^ { 2 } - 4 c < 0 .$ . Show that there are no numbers x satisfying $x ^ { 2 } + b x + c = 0 ;$ in fact, $x ^ { 2 } + b x + c > 0$ for all x. Hint: Complete the square.


Suppose that $b^{2}-4c<0$, then $\sqrt{ b^{2}-4c }$ does not exist, thus by 6(a) $x$ does not exist. 

$$
\begin{align}
x^{2}+bx+c&=\left( x+\frac{b}{2} \right)^{2}-\left( \frac{b}{2} \right) ^{2}+c& \\
&=\left( x+\frac{b}{2} \right) ^{2}+(- \frac{b^{2}-4c}{4})
\end{align}
$$

Notice that $\left( x+ \frac{b}{2} \right)^{2}\geq 0$ and by our assumption $b^{2}-4c< 0\implies \frac{b^{2}-4c}{4}<0\implies- \frac{b^{2}-4c}{4}> 0$. Thus,

$$
\begin{align}
x^{2}+bx+c=\left( x+\frac{b}{2} \right) ^{2}+(- \frac{b^{2}-4c}{4})> 0 &&\blacksquare
\end{align}
$$

> [!remark]
> Notice that 
> 18a) prove that $b^{2}-4c\geq0\implies \exists x\text{ s.t }x^{2}+bx+c=0$
> 18b) prove that $b^{2}-4c<0\implies \forall x, x^{2}+bx+c>0$. This 2 statement complete all the cases and build a biconditional statement.




c)Use this fact to give another proof that if x and y are not both $0 ,$ then $x ^ { 2 } + x y + y ^ { 2 } > 0$ [[Problem Chapter 1 Basic Properties of Number#^356df0]]

Let $b=y$ and $c=y^{2}$ 
$$
\begin{align}
x^{2}+xy+y^{2}&=\left( x+\frac{y}{2} \right)^{2}-\left( \frac{y}{2} \right)^{2}+y^{2} \\
&=\left( x+\frac{y}{2} \right)^{2}+\left(- \frac{y^{2}-4y^{2}}{4} \right)
\end{align}
$$
(Actually the above part can be omitted since we can straight away substitute)
Notice that 
$$
\begin{align}
b^{2}-4c=y^{2}-4y^{2}=-3y^{2}
\end{align}
$$

When $y\neq 0$, it follow that $b^{2}-4c=-3y^{2}< 0$. Thus, by 18(b), it follow that $x^{2}+xy+y^{2}>0$. (This include the case where $x=0$ or $x\neq 0$ because we don't care about $x$). So case left.

When $y=0$ and $x\neq 0$, then $x^{2}>0,xy=0,y^{2}=0$. Thus, $x^{2}+xy+y^{2}>0$$\blacksquare$

> [!remark]
> Spivak is transitioning you from an **ad-hoc trick** to a **universal theory**:
> 
> 1. **In Problem 15**, you proved $x^2 + xy + y^2 > 0$ using a clever algebraic trick: $\frac{x^3 - y^3}{x - y}$ and the monotonicity of odd powers. But that trick only works for very specific polynomials.
> 2. **In Problem 18(b)**, Spivak builds a universal machine: whenever any quadratic $x^2 + bx + c$ has a negative discriminant ($b^2 - 4c < 0$), completing the square proves it floats strictly above the $x$-axis ($> 0$ everywhere).
> 3. **In Problem 18(c)**, you applied that new machine to $x^2 + (y)x + y^2$ by treating $y$ as a constant coefficient, showing that its discriminant $-3y^2$ is negative.

d) For which numbers α is it true that $x ^ { 2 } + \alpha x y + y ^ { 2 } > 0$ whenever x and y are not both 0?

Let $\alpha y=b$ and $c=y^{2}$. Thus,

$$
\begin{align}
b^{2}-4c&=(\alpha y)^{2}-4(y^{2}) \\
&=\alpha^{2}y^{2}-4y^{2}
\end{align}
$$
Suppose  $\alpha^{2}y^{2}-4y^{2}< 0$. Thus

$$
\begin{align}
y^{2}(\alpha^{2}-4)<0
\end{align}
$$
Since $y^{2}>0$ for $y \neq 0$, thus 
$$
\begin{align}
\alpha^{2}-4&< 0 \\
a^{2}&<4 \\ 
a^{2}-4&<0 \\  
(a+2)(a-2)&<0 \\

-2<&\alpha<2
\end{align}
$$

If $y=0$ and $x\neq 0$, then $x^{2}>0$ and $axy=0$ and $y^{2}=0$. Thus, $x^{2}+\alpha xy+y^{2}> 0$. (Nothing to do with $\alpha$ in this case)

> [!question] What is the use of this question?
> Question 18(d) serves three profound purposes:
> 
>  1. It Unifies Your Previous Problems
> - In **Problem 15**, you had $\alpha = 1$ ($x^2 + xy + y^2$). Since $1 \in (-2, 2)$, it is strictly positive!
> - In **Problem 16(b)**, dividing $4x^2 + 6xy + 4y^2$ by $4$ gave $\alpha = 1.5$. Since $1.5 \in (-2, 2)$, it is strictly positive!
> 
> 1. It Prepares You for Problem 19 (The Cauchy-Schwarz Inequality)
> In higher mathematics, expressions like $x^2 + \alpha xy + y^2$ are called **positive definite quadratic forms**. The principle that *a quadratic is strictly positive if and only if its discriminant is negative* is the exact foundation used in Problem 19 to prove the most famous inequality in mathematics: the **Schwarz inequality**.


To see what happens when you step outside the boundary: if you choose $\alpha = 3$, can you find a pair $(x, y) \neq (0, 0)$ that makes $x^2 + 3xy + y^2$ negative? Test $x = 1, y = -1$.


e) Find the smallest possible value of $x ^ { 2 } + b x + c$ and of $a x ^ { 2 } + b x + c ;$ for $a > 0 .$

$$
\begin{align}
x^{2}+bx+c&=\left( x+\frac{b}{2} \right) ^{2}-\left( \frac{b}{2} \right)^{2}+c \\
&=\left( x+\frac{b}{2} \right)^{2}+ \frac{4c-b^{2}}{4}
\end{align}
$$

Thus, the minimum value is $\frac{4c-b^{2}}{4}$ for $x^{2}+bx+c$.

$$
\begin{align}
ax^{2}+bx+c&= a\left( x+\frac{b}{2a} \right)^{2}-a\left( \frac{b}{2a} \right)^{2}+c \\
&=a\left( x+ \frac{b}{2} \right)^{2}+ \frac{4ac-b^{2}}{4a}
\end{align}
$$

Thus, the minimum value is $\frac{4ac-b^{2}}{4a}$

19)The fact $a^{2}\geq 0$, is the fundamental idea of one of the most important inequality which is Cauchy-Schwarz Inequality:

$$
x_{1}y_{1}+x_{2}y_{2}\leq \sqrt{ x_{1}^{2}+x_{2}^{2} }\sqrt{ y_{1}^{2}+y_{2}^{2} }
$$

((A more general form occurs in Problem 2-21.) The three proofs of the Schwarz inequality outlined below have only one thing in common their reliance on the fact that $a ^ { 2 } \geq 0$ for all $ $a$)

(a) Prove that if $x _ { 1 } = \lambda y _ { 1 }$ and $x _ { 2 } = \lambda y _ { 2 }$ for some number $\lambda ,$ then equality holds in the Schwarz inequality. Prove the same thing if $y _ { 1 } = y _ { 2 } = 0$ Now suppose that $y _ { 1 }$ and $y _ { 2 }$ are not both $0 ,$ and that there is no number λ such that $x _ { 1 } = \lambda y _ { 1 }$ and $x _ { 2 } = \lambda y _ { 2 }$ . Then

$$
\begin{array}{r l} & 0 <   (\lambda y _ {1} - x _ {1}) ^ {2} + (\lambda y _ {2} - x _ {2}) ^ {2} \\ & \quad = \lambda^ {2} (y _ {1} ^ {2} + y _ {2} ^ {2}) - 2 \lambda (x _ {1} y _ {1} + x _ {2} y _ {2}) + (x _ {1} ^ {2} + x _ {2} ^ {2}). \end{array}
$$

Using Problem 18, complete the proof of the Schwarz inequality.  


Proof for first:
Suppose $x_{1}=\lambda y_{1}$ and $x_{2}=\lambda y_{2}$, then

$$
\begin{align}
x_{1}y_{1}+x_{2}y_{2}&=\lambda y_{1}^{2}+\lambda y_{2}^{2} \\
&=\lambda(y_{1}^{2}+y_{2}^{2})
\end{align}
$$
and

$$
\begin{align}
\sqrt{ x_{1}^{2}+x_{2}^{2} }\sqrt{ y_{1}^{2}+y_{2}^{2} }&=\sqrt{ (\lambda y_{1})^{2}+(\lambda y_{2})^{2} } \sqrt{ y_{1} ^{2}+y_{2}^{2}} \\
&=\sqrt{ \lambda^{2}(y_{1}^{2}+y_{2}^{2})(y_{1}^{2}+y_{2}^{2}) } \\
&=\sqrt{ \lambda^{2}(y_{1}^{2}+y_{2}^{2})^{2} } \\
&=\lambda(y_{1}^{2}+y_{2}^{2})
\end{align}
$$

Thus,

$$
x_{1}y_{1}+x_{2}y_{2}= \sqrt{ x_{1}^{2}+x_{2}^{2} }\sqrt{ y_{1}^{2}+y_{2}^{2} }
$$

Remark 
Let $x=(x_{1},x_{2})$ and $y=(y_{1}.y_{2})$, then $y=\lambda x$.

Proof for second:
Suppose $y_{1}=y_{2}=0$. Then 

$$
\begin{align}
x_{1}y_{1}+x_{2}y_{2}&=0x_{1}+0x_{2} \\
&=0 
\end{align}
$$
and

$$
\begin{align}
\sqrt{ x_{1}^{2}+x_{2}^{2} }\sqrt{ y_{1}^{2}+y_{2}^{2} }&=\sqrt{ x_{1}^{2}+x_{2}^{2} }\sqrt{ 0+0 } \\
&=0\sqrt{ x_{1}^{2}+x_{2}^{2} } \\
&=0
\end{align}
$$

Thus,
$$
x_{1}y_{1}+x_{2}y_{2}= \sqrt{ x_{1}^{2}+x_{2}^{2} }\sqrt{ y_{1}^{2}+y_{2}^{2} }
$$

Proof for third:
Suppose $y_{1}$ and $y_{2}$ are not both $0$, and that there is no number $\lambda$ such that $x_{1}=\lambda y_{1}$ and $x_{2}=\lambda y_{2}$.

Since $x_{1} \neq \lambda y_{1}$ and $x_{2}\neq \lambda y_{2}$. It follow that $\lambda y_{1}-x_{1} \neq 0$ and $\lambda y_{2}-x_{2}\neq 0$. Thus, it follow that 

$$
\begin{align}
(\lambda y_{1}-x_{1})^{2}+(\lambda y_{2}-x_{2})^{2}&> 0 \\
\lambda^{2}(y_{1}^{2}+y_{2}^{2})-2\lambda(x_{1}y_{1}+x_{2}y_{2})+(x_{1}^{2}+x_{2}^{2})&>0
\end{align}
$$

Notice that $(y_{1}^{2}+y_{2}^{2})> 0$, thus we divide the whole inequality with $(y_{1}^{2}+y_{2}^{2})$:

$$
\begin{align}
\lambda^{2}- \frac{2(x_{1}y_{1}+x_{2}y_{2})}{y_{1}^{2}+y_{2}^{2}}\lambda+ \frac{x_{1}^{2}+x_{2}^{2}}{y_{1}^{2}+y_{2}^{2}}> 0
\end{align}
$$

Let $b=- \frac{2(x_{1}y_{1}+x_{2}y_{2})}{y_{1}^{2}+y_{2}^{2}}$ and $c= \frac{x_{1}^{2}+x_{2}^{2}}{y_{1}^{2}+y_{2}^{2}}$. From contrapositive of 18(a), we know that $x^{2}+bx+c\neq 0\implies b^{2}-4c<0$. Thus,

$$
\begin{align}
\left( -\frac{2(x_{1}y_{1}+x_{2}y_{2})}{y_{1}^{2}+y_{2}^{2}} \right)^{2}-4\left( \frac{x_{1}^{2}+x_{2}^{2}}{y_{1}^{2}+y_{2}^{2}} \right) &< 0 \\
\frac{4(x_{1}y_{1}+x_{2}y_{2})^{2}}{(y_{1}^{2}+y_{2}^{2})^{2}}-\frac{4(x_{1}^{2}+x_{2}^{2})(y_{1}^{2}+y_{2}^{2})}{(y_{1}^{2}+y_{2}^{2})}&< 0 \\
4(x_{1}y_{1}+x_{2}y_{2})^{2}-4(x_{1}^{2}+x_{2}^{2})(y_{1}^{2}+y_{2}^{2})&<0 \\
(x_{1}y_{1}+x_{2}y_{2})^{2}&<(x_{1}^{2}+x_{2}^{2})(y_{1}^{2}+y_{2}^{2}) \\
\end{align}
$$

Thus,

$$
\begin{align}
-\sqrt{( x_{1}^{2}+x_{2}^{2})(y_{1}^{2}+y_{2}^{2}) }&<x_{1}y_{1}+x_{2}y_{2}<\sqrt{ (x_{1}^{2}+x_{2}^{2})(y_{1}^{2}+y_{2}^{2}) } \\
-\sqrt{ x_{1}^{2}+x_{2}^{2} }\sqrt{ y_{1}^{2}+y_{2}^{2} }&<x_{1}y_{1}+x_{2}y_{2}<\sqrt{ x_{1}^{2}+x_{2}^{2} }\sqrt{ y_{1}^{2}+y_{2}^{2} }
\end{align}
$$

> [!remark] Remark
> The Schwarz inequality can be view in vector space view. Let $x$ and $y$ be a vector in $\mathbb{R}^{2}$. When one of case hold:
> i) if there exist $\lambda$ such as $x=\lambda y$ or 
> ii) if one of them is zero (Both expression are 0)
> then the equality hold. Why?
> It is because $x=\lambda y$ means they are in the same direction. and $x_{1}y_{1}+x_{2}y_{2}=x\cdot y$ which is the dot product and it is defined as $||x||||y||\cos \theta$ ($\theta=0\implies \cos \theta=1$)
> [[6.1 Inner Product, Length, and Orthogonality#^bc84ba]]


b)Prove the Schwarz inequality by using $2 x y \le x ^ { 2 } + y ^ { 2 }$ (how is this derived?) with
$$
x = \frac {x _ {i}}{\sqrt {x _ {1} ^ {2} + x _ {2} ^ {2}}}, \qquad y = \frac {y _ {i}}{\sqrt {y _ {1} ^ {2} + y _ {2} ^ {2}}},
$$
first for $i = 1$ and then for $i = 2$  ^prob-1-19-b

Proof for $2xy\leq x^{2}+y^{2}$:

$$
\begin{align}
(x-y)^{2}=x^{2}-2xy+y^{2}
\end{align}
$$
Since $(x-y)^{2}\geq 0$, it follow that

$$
\begin{align}
x^{2}-2xy+y^{2}&\geq 0 \\
x^{2}+y^{2}&\geq 2xy
\end{align}
$$
Proof for Schwarz inequality:

For $i=1$

$$
\begin{align}
\left( \frac{x_{1}}{\sqrt{ x_{1}^{2}+x_{2}^{2} }} \right)^{2}+\left( \frac{y_{1}}{\sqrt{ y_{1}^{2}+y_{2}^{2} }} \right)^{2}&\geq 2 \left( \frac{x_{1}}{\sqrt{ x_{1}^{2}+x_{2}^{2} }} \right)\left( \frac{y_{1}}{\sqrt{ y_{1}^{2}+y_{2}^{2} }} \right) \\
\frac{x_{1}^{2}}{x_{1}^{2}+x_{2}^{2}}+ \frac{y_{1}^{2}}{y_{1}^{2}+y_{2}^{2}}&\geq \frac{2x_{1}y_{1}}{\sqrt{ x_{1}^{2}+x_{2}^{2} }\sqrt{ y_{1}^{2}+y_{2}^{2} }} &&(1)\\

\end{align}
$$

For $i=2$,

$$
\begin{align}
\frac{x_{2}^{2}}{x_{1}^{2}+x_{2}^{2}}+ \frac{y_{2}^{2}}{y_{1}^{2}+y_{2}^{2}}&\geq \frac{2x_{2}y_{2}}{\sqrt{ x_{1}^{2}+x_{2}^{2} }\sqrt{ y_{1}^{2}+y_{2}^{2} }}&&(2)
\end{align}
$$

(1)+(2)
$$
\begin{align}
\frac{x_{1}^{2}+x_{2}^{2}}{x_{1}^{2}+x_{2}^{2}}+ \frac{y_{1}^{2}+y_{2}^{2}}{y_{1}^{2}+y_{2}^{2}}&\geq \frac{2(x_{1}y_{1}+x_{2}y_{2})}{\sqrt{ x_{1}^{2}+x_{2}^{2} }\sqrt{ y_{1}^{2}+y_{2}^{2} }} \\
\sqrt{ x_{1}^{2}+x_{2}^{2} }\sqrt{ y_{1}^{2}+y_{2}^{2} }&\geq x_{1}y_{1}+x_{2}y_{2}
\end{align}
$$

> [!remark] 
> The author's thought process is based on one of the most powerful concepts in mathematics: **Normalization (Scaling to Unit Vectors)**.
> 
> 1) Homogeneity: the relationship remain unchanged when the objects being scaled.
> 
> Suppose we multiply $z_{1}$ and $x_{2}$ by 10:
> Left Side: $10x_{1}y_{1}+10x_{2}y_{2}=10(x_{1}y_{1}+x_{2}y_{2})$
> Right side: $\sqrt{ (10x_{1})^{2}+(10x_{2})^{2} }=\sqrt{ 100(x_{1}^{2}+x_{2}^{2}) }=10\sqrt{ x_{1}^{2}+x_{2}^{2} }$
> 
> 2) The Simplification: Make their Lengths Equal to 1
> 
> Since scaling didn't affect the relationship. We can divide each $x_{i}$ by its length $\sqrt{ x_{1}^{2}+x_{2}^{2} }$ and each $y_{i}$ by $\sqrt{ y_{1}^{2}+y_{2}^{2} }$ 
> Thus,
> 
> 
> $$
> u_i = \frac{x_i}{\sqrt{x_1^2 + x_2^2}} \implies u_1^2 + u_2^2 = 1
> $$
> 
> $$
> v_i = \frac{y_i}{\sqrt{y_1^2 + y_2^2}} \implies v_1^2 + v_2^2 = 1
> $$
> For these unit vectors, the right side $\sqrt{u_1^2 + u_2^2}\sqrt{v_1^2 + v_2^2} = 1 \cdot 1 = 1$.
> So the Schwarz inequality for unit vectors is simply:
> 
> $$
> u_1 v_1 + u_2 v_2 \leq 1
> $$
> 
> 3. Connect Products to Squares
> Now, how do you bound a product $u_i v_i$ using squares whose sums equal $1$? 
> You use the most basic inequality in algebra:
> 
> $$
> 2 u_i v_i \leq u_i^2 + v_i^2 \iff u_i v_i \leq \frac{u_i^2 + v_i^2}{2}
> $$
> The sum equals $1$ because of the exact denominator Spivak chose. Look at what happens when you square and add:
> 
> Define:
> 
> $$
> u_1 = \frac{x_1}{\sqrt{x_1^2 + x_2^2}} \quad \text{and} \quad u_2 = \frac{x_2}{\sqrt{x_1^2 + x_2^2}}
> $$
> 
> When you square each term:
> 
> $$
> u_1^2 = \frac{x_1^2}{x_1^2 + x_2^2} \quad \text{and} \quad u_2^2 = \frac{x_2^2}{x_1^2 + x_2^2}
> $$
> 
> Now add them together:
> 
> $$
> u_1^2 + u_2^2 = \frac{x_1^2}{x_1^2 + x_2^2} + \frac{x_2^2}{x_1^2 + x_2^2} = \frac{x_1^2 + x_2^2}{x_1^2 + x_2^2} = 1
> $$
> 
> The numerator and denominator become identical, so the sum is guaranteed to be $1$! (The exact same thing happens for $v_1^2 + v_2^2 = 1$).
> 
> 

> [!remark]
> 
> Homogeneity$\to$simplify inequality$\to$use a trivial inequality to prove  


c) Prove the Schwarz inequality by first proving Lagrange's Identity  ^prob-1-19-c

$$
(x_{1}^{2}+x_{2}^{2})(y_{1}^{2}+y_{2}^{2})=(x_{1}y_{1}+x_{2}y_{2})^{2}+(x_{1}y_{2}-x_{2}y_{1})^{2}
$$

Proof for Lagrange's identity:
Expand right hand side:
$$
\begin{align}
(x_{1}^{2}+x_{2}^{2})(y_{1}^{2}+y_{2}^{2})&=x_{1}^{2}y_{1}^{2}+x_{1}^{2}y_{2}^{2}+x_{2}^{2}y_{1}^{2}+x_{2}^{2}y_{2}^{2}
\end{align}
$$

Expand left hand side:

$$
\begin{align}
(x_{1}y_{1}+x_{2}y_{2})^{2}+(x_{1}y_{2}-x_{2}y_{1})^{2}&=x_{1}^{2}y_{1}^{2}+2x_{1}x_{2}y_{1}y_{2}+x_{2}^{2}y_{2}^{2}+x_{1}^{2}y_{2}^{2}-2x_{1}x_{2}y_{1}y_{2}+x_{2}^{2}y_{1}^{2} \\
&=x_{1}^{2}y_{1}^{2}+x_{2}^{2}y_{2}^{2}+x_{1}^{2}y_{2}^{2}+x_{2}^{2}y_{1}^{2}
\end{align}
$$

Thus,

$$
\begin{align}
(x_{1}^{2}+x_{2}^{2})(y_{1}^{2}+y_{2}^{2})=(x_{1}y_{1}+x_{2}y_{2})^{2}+(x_{1}y_{2}-x_{2}y_{1})^{2} &&\blacksquare
\end{align}
$$

Proof for Schwarz inequality:

Let $a=x_{1}^{2}+x_{2}^{2}$ , $b=y_{1}^{2}+y_{2}^{2}$ , $c=(x_{1}y_{1}+x_{2}y_{2})^{2}$ and $d=(x_{1}y_{2}+x_{2}y_{1})^{2}$.Thus, we have
$$
ab=c^{2}+d^{2}
$$
and we need to prove
$$
\sqrt{ ab }\geq c
$$
Since $c^{2},d^{2}\geq 0$, thus $ab\geq c^{2}$ and $ab\geq d^{2}$. Thus, it follow that

$$
\begin{align}
\sqrt{ ab }&\geq \sqrt{ c^{2} } \\
\sqrt{ ab }&\geq |c| \\
\end{align}
$$

Since $|c|\geq c$, by transitivity law, it follow that
$$
\begin{align}
\sqrt{ ab }\geq c &&\blacksquare
\end{align}
$$

> [!remark]
> How mathematician think of Lagrange identity?
> Whenever want to prove $A\geq B$, a standard instinct is:
> Subtract them and see what is left over.
> 
> $$
> \begin{align}
> (x_{1}^{2}+x_{2}^{2})(y_{1}^{2}+y_{2}^{2})-(x_{1}y_{1}+x_{2}y_{2})^{2}=x_{1}^{2}y_{2}^{2}-2x_{1}x_{2}y_{1}y_{2}+x_{2}^{2}y_{1}^{2}
> \end{align}
> $$
> 
> Notice that they form a perfect square:
> $$
> (x_{1}y_{2}-x_{2}y_{1})^{2}
> $$
> Reverse process:
> 
> $$
> \sqrt{ (x_{1}^{2}+x_{2}^{2})(y_{1}^{2}+y_{2}^{2}) }-(x_{1}y_{1}+x_{2}y_{2})\geq 0
> $$
> We square both side and continue until we get Lagrange identity 

> [!remark]
> 19a) prove using quadratic discriminant with the fact that if $x=\lambda y$ or $y=0$ , the equality hold.
> 19b) prove using normalization and a trivial inequality
> 19c) prove using reverse process and deduce Lagrange identity
> 

d) Deduce, from each of these three proofs, that equality holds only when $y _ { 1 } = y _ { 2 } = 0$ or when there is a number λ such that $x _ { 1 } = \lambda y _ { 1 }$ and $x _ { 2 } = \lambda y _ { 2 }$

Deduce from $c)$:
The equality hold when the leftover 
$$
(x_{1}y_{2}-x_{2}y_{1})^{2}=0\implies x_{1}y_{2}-x_{2}y_{1}=0
$$
Thus,
$$
\begin{align}
x_{1}y_{2}&=x_{2}y_{1} \\
\end{align}
$$
Suppose $y_{1}\neq 0$ or $y_{2}\neq 0$, we need to show that $x_{1}=\lambda y_{1}$ and $x_{2}=\lambda y_{2}$ for some number $\lambda$.

Case 1: $y_{1}\neq 0$ and $y_{2} \neq 0$. Then
$$
\begin{align}
\frac{x_{1}}{y_{1}}&=\frac{x_{2}}{y_{2}}
\end{align}
$$
Let $\lambda=\frac{x_{1}}{y_{1}}=\frac{x_{2}}{y_{2}}$. Thus, $x_{1}=\lambda y_{1}$ and $x_{2}=\lambda y_{2}$

Case 2: WLOG $y_{1} \neq 0$ and $y_{2}=0$. 

Since $y_{2}=0$.Then, $x_{1}y_{2}=0$ and this forced $x_{2}y_{1}=0$. Since $y_{1}\neq 0$, it follow that $x_{2}=0$ by Zero Product Property. 

Since $y_{1}\neq 0$. Then let $\lambda=\frac{x_{1}}{y_{1}}$. Thus, $x_{1}=\lambda y_{1}$. Notice that $\lambda y_{2}=0=x_{2}$. 

All cases we get $x_{1}=\lambda y_{1}$ and $x_{2}=\lambda y_{2}$.$\blacksquare$

Deduce from b):

$$
\begin{align}
2uv&=u^{2}+v^{2} \\
u^{2}+v^{2}-2uv&=0 \\
(u-v)^{2}&=0 \\
u-v&=0 \\
u&=v
\end{align}
$$
Since Schwarz inequality was obtained by adding two inequalities for $i=1$ and $i=2$, equality holds iff

$$
u_{1}=v_{1}\text{ and }u_{2}=v_{2}
$$
Suppose $y_{1}\neq 0$ or $y_{2} \neq 0$, then $\sqrt{ y_{1}^{2}+y_{2}^{2} }\neq 0$. We need to prove $x_{1}=\lambda y_{1}$ and $x_{2}=\lambda y_{2}$ for some $\lambda$. By substitution,
 
$$
\begin{align}
\frac{x_{1}}{\sqrt{ x_{1}^{2}+x_{2}^{2} }}&=\frac{y_{1}}{\sqrt{ y_{1}^{2}+y_{2}^{2} }} \\
x_{1}&= \frac{y_{1}\sqrt{ x_{1}^{2}+x_{2}^{2} }}{\sqrt{ y_{1}^{2}+y_{2}^{2} }}
\end{align}
$$
and
$$
\begin{align}
\frac{x_{2}}{\sqrt{ x_{1}^{2}+x_{2}^{2} }}&= \frac{y_{2}}{\sqrt{ y_{1}^{2}+y_{2}^{2} }} \\
x_{2}&= \frac{y_{2}\sqrt{ x_{1}^{2}+x_{2}^{2} }}{\sqrt{ y_{1}^{2}+y_{2}^{2} }}
\end{align}
$$


Let $\lambda= \frac{\sqrt{ x_{1}^{2}+x_{2}^{2} }}{\sqrt{ y_{1}^{2}+y_{2}^{2} }}$. Thus, $x_{1}=\lambda y_{1}$ and $x_{2}=\lambda y_{2}$. 


Deduce from a):
When the equality hold, we can deduce $(x_{1}y_{1}+x_{2}y_{2})^{2}=(y_{1}^{2}+y_{2}^{2})(x_{1}^{2}+x_{2}^{2})$. Thus, the discriminant $b^{2}-4ac$ is

$$
\begin{align}
4(x_{1}y_{1}+x_{2}y_{2})^{2}-4(y_{1}^{2}+y_{2}^{2})(x_{1}^{2}+x_{2}^{2})&=4[(x_{1}y_{1}+x_{2}y_{2})^{2}-(y_{1}^{2}+y_{2}^{2})(x_{1}^{2}+x_{2}^{2})] \\
&=4(0) \\
&=0
\end{align}
$$

Since the discriminant is 0, from question 18a) and b), we know that there exist solution for the quadratic equation

$$
\begin{align}
\lambda^{2}(y_{1}^{2}+y_{2}^{2})-2\lambda(x_{1}y_{1}+x_{2}y_{2})+(x_{1}^{2}+x_{2}^{2})&=0 \\
(\lambda y_{1}-x_{1})^{2}+(\lambda y_{2}-x_{2})^{2}&= 0 \\
\end{align}
$$

Since $(\lambda y_{1}-x_{1})^{2}\geq 0$ and $(\lambda y_{2}-x_{2})^{2}\geq 0$. For the equality to hold, it follow that $(\lambda y_{1}-x_{1})^{2}=0$ and $(\lambda y_{2}-x_{2})^{2}=0$. Thus, $\lambda y_{1}-x_{1}=0\implies \lambda y_{1}=x_{1}$ and 
$\lambda y_{2}-x_{2}=0\implies \lambda y_{2}=x_{2}$.

20) Prove that if

$$
| x - x _ {0} | <   \frac {\varepsilon}{2} \quad \text { and } \quad | y - y _ {0} | <   \frac {\varepsilon}{2},
$$
then

$$
\begin{array}{l} {| (x + y) - (x _ {0} + y _ {0}) | <   \varepsilon ,} \\ {| (x - y) - (x _ {0} - y _ {0}) | <   \varepsilon .} \end{array}
$$

Proof:

$$
\begin{align}
|(x+y)-(x_{0}+y_{0})|&=|(x-x_{0})+(y-y_{0})| \\
&\leq|x-x_{0}|+|y-y_{0}|&&\text{By traingle inequality} \\
&< \frac{\epsilon}{2}+\frac{\epsilon}{2} \\
&<\epsilon
\end{align}
$$

$$
\begin{align}
|(x-y)-(x_{0}-y_{0})|&=|(x-x_{0})-(y-y_{0})|  \\
&\leq|x-x_{0}|+|y-y_{0}|&&\text{By 12 iv)} \\
&<\frac{\epsilon}{2}+\frac{\epsilon}{2} \\
&< \epsilon
\end{align}
$$

21) Prove that if  ^prob-1-21

$$
| x - x _ {0} | <   \min \left(\frac {\varepsilon}{2 (| y _ {0} | + 1)}, 1\right) \quad \text { and } \quad | y - y _ {0} | <   \frac {\varepsilon}{2 (| x _ {0} | + 1)},
$$

then $| x y - x_0 y_0 | < \varepsilon.$

Proof: 

> [!warning]
>Notice that
> $$
> \begin{align}
> (x-x_{0})(y-y_{0})=xy-xy_{0}-yx_{0}+x_{0}y_{0}
> \end{align}
> $$
> and
> $$
> \begin{align}
> (x+x_{0})(y+y_{0})=xy+xy_{0}+yx_{0}+x_{0}y_{0}
> \end{align}
> $$
> 
> Thus,
> 
> $$ 
> xy+x_{0}y_{0}= \frac{(x-x_{0})(y-y_{0})+(x+x_{0})(y+y_{0})}{2}
> $$
> 
> It is nothing related because we want $xy-x_{0}y_{0}$ and also we don't have bound for $x+x_{0}$ and $y+y_{0}$.

Notice that they are sum of  product and we want to make it into something like $x-x_{0}$, thus we can use the decouple variation tool

$$
\begin{align}
xy-x_{0}y_{0}&=xy-yx_{0}+yx_{0}-x_{0}y_{0} \\
&=y(x-x_{0})+x_{0}(y-y_{0})
\end{align}
$$
We can also do in this way:

$$
\begin{align}
xy-x_{0}y_{0}&=xy-xy_{0}+xy_{0}-x_{0}y_{0} \\
&=x(y-y_{0})+y_{0}(x-x_{0})
\end{align}
$$

Which one we need to use? (The answer is second one) .Observe the supposition in the question, $|x-x_{0}|<1$ actually control the $|x|$, how? (the answer lies in question 12 v) [[Problem Chapter 1 Basic Properties of Number#^b45e11]] ) Notice that

$$
\begin{align}
x&=(x-x_{0})+x_{0} \\
|x|&=|(x-x_{0})+x_{0}| \\
&\leq|x-x_{0}|+|x_{0}|
\end{align}
$$
From supposition we know that $|x-x_{0}|<1$, thus

$$
|x|<1+|x_{0}|
$$
Go back to the equation we have earlier and apply triangle inequality (to use the bound)

$$
\begin{align}
|xy-x_{0}y_{0}|&=|x(y-y_{0})+y_{0}(x-x_{0})| \\
&\leq|x(y-y_{0})|+|y_{0}(x-x_{0})| \\
&\leq|x||y-y_{0}|+|y_{0}||x-x_{0}|
\end{align}
$$
Now we substitute the bound below into the inequality
1) $|x|<1+|x_{0}|$ and $|y-y_{0}|< \frac{\epsilon}{2(|x_{0}|+1)}$
2) $|x-x_{0}|< \frac{\epsilon}{2(|y_{0}|+1)}$

Thus,

$$
\begin{align}
|xy-x_{0}y_{0}|&<(1+|x_{0}|)\left( \frac{\epsilon}{2(|x_{0}+1)} \right)+|y_{0}|\left( \frac{\epsilon}{2(|y_{0}|+1)} \right) \\
&<  \frac{\epsilon}{2}+ \left( \frac{|y_{0}|}{|y_{0}|+1} \right) \frac{\epsilon}{2}
\end{align}
$$

Since $|y_{0}|\geq 0$, it follow that $|y_{0}|+1>0$. Thus, $\frac{|y_{0}|}{|y_{0}|+1}>0$.
Notice that $|y_{0}|+1\geq|y_{0}|$, thus, it follow that 

$$
\begin{align}
0< \frac{|y_{0}|}{|y_{0}|+1}<1 \\
0< \left( \frac{|y_{0}|}{|y_{0}|+1} \right) \frac{\epsilon}{2}< \frac{\epsilon}{2}
\end{align}
$$

Thus,

$$
\begin{align}
|xy-x_{0}y_{0}|&< \frac{\epsilon}{2}+ \frac{\epsilon}{2} \\
&< \epsilon &&\blacksquare
\end{align}
$$

22) Prove that if $y _ { 0 } \neq 0$ and

$$
| y - y _ {0} | <   \min \left(\frac {| y _ {0} |}{2}, \frac {\varepsilon | y _ {0} | ^ {2}}{2}\right),
$$

then $y \neq 0$ and

$$
\left| \frac {1}{y} - \frac {1}{y _ {0}} \right| <   \varepsilon .
$$


Thinking process:

$$
\begin{align}
\left| \frac{1}{y}- \frac{1}{y_{0}} \right|&<\epsilon \\
| \frac{1}{y}| -| \frac{1}{y_{0}}|&<\epsilon
\end{align}
$$
This didn't work because it is nothing to do with the constraint $\left|y-y_{0}  \right|$
or

$$
\begin{align}
\left| \frac{1}{y}-\frac{1}{y_{0}} \right| &<\epsilon \\
\left| \frac{y_{0}-y}{yy_{0}} \right| &<\epsilon \\
\frac{\left| y_{0}-y \right| }{\left| y \right| \left| y_{0} \right| }&<\epsilon \\
\end{align}
$$


From supposition we know that 

$$
|y-y_{0}|< \frac{|y_{0}|}{2}\text{ (1) and } |y-y_{0}|<  \frac{\epsilon|y_{0}|^{2}}{2}\text{ (2)}
$$

The same technique (detour principle)

First we need to prove that $y\neq 0$, to make sure $\frac{1}{y}$ exist, to do this we need to find the lower bound of $\left| y \right|$, notice that (1) say that the distance between $y$ and $y_{0}$ is less than the half distance from 0 to $y_{0}$ and we need to use this to show that if $y$ stay within the distance, $y\neq 0$.

$$
\begin{align}
(y_{0}-y)+y&=y_{0} \\
\left| y_{0} \right| &\leq\left| y_{0}-y \right| +\left| y \right|  \\
\left| y_{0} \right| &\leq \left| y-y_{0} \right| +\left| y \right|  \\
\left| y \right| &\geq\left| y_{0} \right| -\left| y-y_{0} \right|  \\
\left| y \right| &> \left| y_{0} \right| - \frac{\left| y_{0} \right| }{2} \\ 
 \left| y \right| &> \frac{\left| y_{0} \right| }{2} \\
\left| y \right|&> 0  \\
y&\neq 0
\end{align}
$$

Now we need to prove for $\left| \frac{1}{y}-\frac{1}{y_{0}} \right|<\epsilon$. Earlier we get

$$
\begin{align}
\frac{\left| y_{0}-y \right| }{\left| y \right| \left| y_{0} \right| }&< \frac{\epsilon\left| y_{0} \right| ^{2}}{2\left| y \right| \left| y_{0} \right| } \\ 
&< \frac{\epsilon\left| y_{0} \right| }{2\left| y \right| } \\
&< \frac{\epsilon\left| y_{0} \right| }{2}\cdot \frac{1}{\left| y \right| }
\end{align}
$$
From earlier inequality we have 

$$
\begin{align}
\left| y \right| &> \frac{\left| y_{0} \right| }{2} \\
\frac{1}{\left| y \right| }&> \frac{2}{\left| y_{0} \right| }
\end{align}
$$

> [!theorem] Lemma:
>  Suppose $a,b \neq 0$ and $a,b$ have same sign. If $a>b$, then $\frac{1}{a}< \frac{1}{b}$. 
> 
> 
> 
> $$
> \begin{align}
> a-b&>0 \\
> \frac{a-b}{ab}&>0 &&\text{Since } \frac{1}{ab}>0 \\
> \frac{1}{b}-\frac{1}{a}&>0 \\ 
> \end{align}
> $$
> Thus, $\frac{1}{a}< \frac{1}{b}$. $\blacksquare$

> [!remark]
> In other word, if $a,b$ have different sign, then the inequality won't flip

Thus, by transitivity law

$$
\begin{align}
\left| \frac{1}{y}- \frac{1}{y_{0}} \right| &< \frac{\epsilon\left| y_{0} \right| }{2}\cdot \frac{2}{\left| y_{0} \right| } \\
&<\epsilon &&\blacksquare
\end{align}
$$


23）

$$
\begin{align}
\left| \frac{x}{y} - \frac{x_{0}}{y_{0}}\right| &<\epsilon \\
\left| x\left( \frac{1}{y} \right)-x_{0}\left( \frac{1}{y_{0}} \right) \right| <\epsilon \\
\end{align}
$$
Thus, from question 21, we can deduce that

$$
| \frac{1}{y} -  \frac{1}{y_{0}} | <   \frac {\varepsilon}{2 (| x _ {0} | + 1)}
$$
and
$$
\begin{align}
\left| x-x_{0} \right|< min\left(  \frac{\epsilon}{2\left(   \frac{1}{\left| y_{0} \right| }+1   \right)},1 \right)
\end{align}
$$

Notice that $\left| y_{0} \right|$ become $\frac{1}{\left| y_{0} \right|}$.


Notice that from question 22,  

$$
\left| \frac{1}{y} - \frac{1}{y_0} \right| < \text{Target}
$$

whenever you set:

$$
|y - y_0| < \min\left(\frac{|y_0|}{2}, \frac{\text{Target} \cdot |y_0|^2}{2}\right)
$$

Remark
Why Spivak introducing these statement that seem to just involve random inequality?

Actually it is the mechanism or algebra behind 4 limit law
1) $\lim(f\pm g)=\lim f\pm \lim g$
2) $\lim(f\cdot g)=(\lim f)\cdot(\lim g)$
3) $\lim\left( \frac{1}{g} \right)= \frac{1}{\lim g}$
4) $\lim\left( \frac{f}{g} \right)=\frac{\lim f}{\lim g}$

Spivak deliberately extracted all the painful inequality algebra into **Chapter 1**:
* **Problem 20:** Limits of Sums & Differences (Errors simply add: $\varepsilon/2 + \varepsilon/2$).
* **Problem 21:** Limit of Products (Non-linear error: requires the Detour Principle to cap growth $|x| < |x_0| + 1$).
* **Problem 22:** Limit of Reciprocals (Singularity danger: requires the Detour Principle to stay away from zero $|y| > |y_0|/2 > 0$).
* **Problem 23:** Limit of Quotients.

 2. Why Problem 23 Specifically? (The Modularity Principle)

Why didn't Spivak just stop at 22? Why make you do division?

Because Problem 23 demonstrates **Modular Engineering in Mathematics**:
$$
\frac{x}{y} = x \cdot \frac{1}{y}
$$

He wants to show you:
1. You **do not** need to invent a brand-new, painful algebraic method for division.
2. Problem 21 is an engine for **Products**.
3. Problem 22 is an engine for **Inverses**.
4. Division is just chaining the two engines together:
   $$\text{Quotient}(x, y) = \text{Product}\left(x, \frac{1}{y}\right)$$

Once you have verified the interface of 21 and 22, the quotient rule is **solved for free by composition**.

