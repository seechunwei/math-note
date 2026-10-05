4.25
Let $x,y \in \mathbb{R}$. Prove that if $x^{2}-4x=y^{2}-4y$ and $x \neq y$ then $x+y =4$

Proof:
Notice that
$(x-y)(x+y)=4(x-y)$

Since $x \neq y$ it follow that $x-y \neq 0$. Thus, 
$$
x+y=4
$$
Q.E.D

4.26
Proof:
Suppose $a< 3m+1$ and $b<2m+1$.  Thus,
$2a<6m+2$ , $3b<6m+6$. Thus,

$$
\begin{align}
2a+3b&<(6m+2)+(6m+6) \\
&<12m+8 \\
&<12m+1
\end{align}
$$
Since it is true and it is logically equivalent to original statement. Thus it is true.

4.27
Proof:
Suppose $x\leq 0$. 
Notice that
$$
x^{7}+x^{3}=x^{3}(x^{4}+1)
$$
Since $x\leq 0$, it follow that $x^{3}\leq0$. Thus, since $x^{4}+1\geq 0$  and $x^{3}\leq 0$, it follow that $x^{3}(x^{4}+1)\leq 0$. Thus, 
$$
x^{7}+x^{3}\leq 0
$$

Notice that, $3x^{4}+1> 0$.

Thus,
$$
x^{7}+x^{3}\leq 0<3x^{4}+1
$$
Thus, it follow that $3x^{4}+1>x^{7}+x^{3}$. Q.E.D

4.28
Prove that if $r$ is a real number such that $0<r<1$, then $\frac{1}{r(1-r)}\geq 4$
Proof:
Suppose $0<r<1$. Thus, 
$$
\begin{align}
-1<-r<0 \\
0<1-r<1
\end{align}
$$

$r-r^{2}$
$0<r^{2}<1$

$r^{2}\geq r$
$r-r^{2}\leq0$
Wrong , this inequality only true for integer.
For example 
$\left( \frac{1}{2} \right)^{2}< \frac{1}{2}$ . Notice that $r>r^{2}$ in this case and notice this is true for $0<r<1$.
Thus, if $0<r<1$ , then $r>r^{2}$. Thus, $r-r^{2}>  0$

Notice that we cannot just prove from the supposition.

Thus, let look at the conclusion.
$1< 4r(1-r)$
$4r-4r^{2}> 1$
$r-r^{2}> \frac{1}{4}$

$r^{2}-r+\frac{1}{4}< 0$
$4r^{2}-4r+1<0$
$(2r-1)^{2}< 0$

It is wrong we cannot simply multiply $r(1-r)$ because we don't know if it is negative or positive. Instead we can just prove by contradiction.

Prove:
We argue by contradiction suppose if $r \in \mathbb{R}$ such that $0<r<1$ , then $\frac{1}{r(1-r)}<4$ Thus,

$$
\begin{align}
1&<4r(1-r) \text{ (since 0<r<1)}\\
1&<4r-4r^{2} \\
4r^{2}-4r+1&<0 \\
(2r-1)^{2}< 0
\end{align}
$$
Since $(2r-1)^{2}\geq 0$ , thus it lead to a contradiction.

==Remark==
Can we prove by direct proof by reversing the process starting from $(2r-1)^{2}\geq 0$?
Why it work?
Because in this case we can reverse the process under the same supposition
Prove:
Suppose $0<r<1$. Notice that $(2r-1)^{2}\geq 0$. Thus,
$$
\begin{align}
(2r-1)^{2}&\geq 0 \\
4r^{2}-4r+1&\geq 0 \\
4r(r-1)&\geq -1 \\
r(1-r)&\leq \frac{1}{4} \\
\frac{1}{r(1-r)}&\geq 4 \text{ (since 0<r<1)}
\end{align}
$$
Q.E.D.

Can we prove by other way? we can prove using AM-GM inequality. because $r\geq 0$, and $4$ is a power of 2, thus since we will get square root in the process, we can just square the inequality.

Proof:
Suppose $0<r< 1$. Thus,
$$
\begin{align}
r+(1-r)&\geq 2\sqrt{ r(1-r) } \\
\frac{1}{2}&\geq \sqrt{ r(1-r) } \\
\frac{1}{4}&\geq r(1-r) \\
4&\leq \frac{1}{r(1-r)}
\end{align}
$$
Q.E.D


==Extra==
Prove that for any $x > 0$:
$$x + \frac{9}{x} \geq 6$$
Proof:
$$
\begin{align}
x+\frac{9}{x}&\geq 2\sqrt{ x\left( \frac{9}{x} \right) } \\
x+\frac{9}{x}&\geq 2(3) \\
&\geq 6
\end{align}
$$
Q.E.D

When we can use AM-GM
1) When the variable is positive $r$ and $1-r$ is greater than 0 because $0<r<1$
2) The "Disappearing Variable" Trick
- We spot there is a product of 2 term where its sum can diminish the variable (vice versa)


4.29
Proof strategy:
$-1<r-1<1$
$0<r<2$
Notice that the product $r(4-r)$ , the sum is $4$, thus we can use $AM-GM$

Proof:
Suppose $|r-1|< 1$. Thus , 
$$
\begin{array}
\ -1<r-1<1 \\
0<r<2
\end{array}
$$
Since $0<r< 1$, it follow that $r> 0$ and $4-r> 0$. 
$$
\begin{array}
\ r+(r-4)\geq  2\sqrt{ r(4-r) } \\
2\geq \sqrt{ r(4-r) } \\
4\geq r(4-r) \\
\frac{1}{4}\leq \frac{1}{r(4-r)} \\
\frac{4}{r(4-r)}\geq 1
\end{array}
$$
Q.E.D

4.31
Lemma 1: $-|r|\leq r\leq|r|$
Lemma 2: $|-r|=|r|$

Proof:
Suppose $x$ and y are arbitrary real number.

Case 1: $x\geq 0$ and $y\geq 0$
Thus $x+y\geq 0$.
$$
\begin{align}
 |x+y|&=x+y \\
&=|x|+|y| \\
&\geq|x| \\
&\geq|x|-|y|
\end{align}
$$

Case 2: $x<0$ and $y<0$
Thus, $x+y< 0$
$$
\begin{align}
|x+y|&=-(x+y) \\
&=-x+(-y) \\
&=|x|+|y| \\
&\geq|x| \\
&\geq|x|-|y|
\end{align}
$$
Case 3: WLOG $x\geq 0$ and $y< 0$
By lemma 1,

$$
\begin{align}
 x+y\leq |x+y| \\
\end{align}
$$
Since $x=|x|$ and by lemma 1, $y\geq-|y|$. Thus, $x+y\geq|x|-|y|$. Hence,
$$
\begin{align}
|x+y|&\geq|x|-|y|
\end{align}
$$

==Remark==
Notice that in case 3 $x+y=|x|-|y|$ , thus we just substitute. No need to establish the fact that $y\geq -|y|$ because $y=-|y|$

4.33.
Lemma 1
Prove: 
$a^{2}+b^{2}+c^{2}\geq ab+bc+bc$ where $a,b,c \in \mathbb{R}$ and $a,b,c\geq 0$ 

Notice that $a^{2}+b^{2}\geq 2ab$
$b^{2}+c^{2}\geq 2bc$
$a^{2}+c^{2}\geq 2ac$
Thus,

$$
\begin{align}
(a^{2}+b^{2})+(b^{2}+c^{2})+(a^{2}+c^{2})&\geq 2ab+2bc+2ac \\
a^{2}+b^{2}+c^{2}\geq ab+bc+ac
\end{align}
$$


The sum of three cubes identity
$$a^3 + b^3 + c^3 - 3abc = (a+b+c)(a^2 + b^2 + c^2 - ab - bc - ca)$$




Thus, if $a,b,c\geq 0$, then $a^{3}+b^{3}+c^{3}\geq 0$

Proof:
$$
\begin{align}
\sqrt[3]{r^{3}s ^{3}t ^{3} }&\leq \frac{r^{3}+s ^{3}+t ^{3}}{3} \\
3rst&\leq r^{3}+s ^{3}+ t^{3} \\
r^{3}+ s ^{ 3}+ t ^{3}-3rst\geq  0
\end{align}
$$
By identity and lemma 1 this is true, thus by reversing the process the original statement is true.

==Remark==
Why we need to substitute the $r^{3} s ^{3} t ^{3}$ at the first place
1) To simplify the expression, in fact we can just do like that but it is hard for us to spot the pattern to use the identity of sum of cubes


Prove the sum of three cubes identity

$a^{2}+b^{2}+c^{2}- ab-bc-ac=0$

4.34
Proof:
Suppose $x,y,z$ are arbitrary real number. Since 
$$
|x-z|=\begin{cases}
x-z,\,\, x\geq z \\
-(x-z), \,\, x\leq z
\end{cases}
$$
Thus, WLOG assume $x\leq z$, thus we have 3 cases

Case 1: $x\leq y\leq z$
Thus, $|x-z|=z-x$ and $|x-y|=y-x$ and $|y-z|=z-y$. Thus,

$$
\begin{align}
|x-z|&=z-x \\
&=(y-x)+(z-y) \\
&=|x-y|+|y-z|
\end{align}
$$

Case 2: $x\leq z\leq y$
Thus, $|x-z|\leq |x-y|$. Thus,
$$
|x-z|\leq|x-y|+|y-z|
$$

Case 3: $y\leq x\leq z$
Thus, $|x-z|\leq|y-z|$. Thus,
$$
|x-z|\leq|y-z|+|x-y|
$$

In either case $|x-z|\leq|x-y|+|y-z|$.

==Algebraic method==
Proof:
Notice that $x-z=x-y+y-z$. Thus, 
$x-z=(x-y)+(y-z)$

By triangle inequality, it follow that 
$$
|x-z|\leq|x-y|+|y-z|
$$
Q.E.D

4.35
Proof:
Suppose $x \in\mathbb{R}$ such as $-2\leq x\leq 1$. Thus, $-1\leq x+1\leq 2$. Thus,

$2\leq x(x+1)\leq 2$

It is wrong!!

Proof:
$$
\begin{align}
x(x+1)>2 \\
x^{2}+x-2> 0 \\
(x+2)(x-1)>0
\end{align}
$$
If $ab>0$, then $-a\times-b> 0$. Thus,

Case 1: $(x+2)>0$ and $(x-1)>0$
Thus, $x>-2$ and $x>1$. Hence, $x>1$.

Case 2: $(x+2)< 0$ and $(x-1)< 0$
Thus, $x<-2$ and $x<1$. Hence , $x<-2$

Thus, it follow that $x<-2$ or $x>1$.

4.36
$$
\begin{align}
x^{4}+1&\geq x^{3}+x \\
x^{3}(x-1)&\geq x-1 \\ 
(x^{3}-1)(x-1)&\geq 0
\end{align}
$$
Since $x\geq 1$, it follow that $x^{3}-1\geq 0$, $x-1\geq 0$. Thus, it follow that $(x^{3}-1)(x-1)\geq 0$

Proof:
Suppose $x$ is arbitrary positive real number. Notice that $(x^{3}-1)(x-1)\geq 0$. 
...

4.37
Proof:
Suppose $x,y,z \in \mathbb{R}$. Notice that $a^{2}+b^{2}\geq 2ab$ for $a,b \in \mathbb{R}$. Thus,

$$
\begin{align}
(x^{2}+y^{2})+(x^{2}+z^{2})+(y^{2}+z^{2})&\geq 2xy+2xz+2yz \\
x^{2}+y^{2}+z^{2}&\geq xy+xz+yz
\end{align}
$$

4.38
Proof:
Suppose $a,b,x,y \in \mathbb{R}$ and $r \in \mathbb{R}^{+}$ such that $|x-a|< \frac{r}{2}$ and $|y-b|< \frac{r}{2}$.
Thus,
$|x-a|+|y-b|<r$

Notice that $|(x-a)+(y-b)|\leq |x-a|+|y-b$. Thus,

$$
\begin{align}
|(x-a)+(y-b)|<r
\end{align}
$$
Q.E.D


4.39
Proof: 
Suppose $a,b,c,d \in \mathbb{R}$. Notice that
$(ab+cd)^{2}=(ab)^{2}+2abcd+(cd)^{2}$
and$(a^{2}+c^{2})(b^{2}+d^{2})=(ab)^{2}+(ad)^{2}+(bc)^{2}+(cd)^{2}$. Let $ad=x$ and $bc=y$, Notice that,

$$
\begin{align}
x^{2}+y^{2}&\geq 2 xy \\
ad^{2}+bc^{2}&\geq 2abcd \\
(ab)^{2}+(ad)^{2}+(bc)^{2}+(cd)^{2}&\geq (ab)^{2}+2abcd+(cd)^{2} \\
(a^{2}+c^{2})(b^{2}+d^{2})&\geq(ab+cd)^{2}
\end{align}
$$
Q.E.D









