1) Let $f(x)= \frac{1}{1+x}$.What is
i) $f(f(x))$ for which $x$ does this make sense?

$$
\begin{align}
f(f(x))&=\frac{1}{1+\frac{1}{1+x}} \\
&= \frac{1}{\left( \frac{2+x}{1+x} \right)} \\
&=\frac{1+x}{2+x}
\end{align}
$$

The domain of $f$: $x\in \mathbb{R}\setminus \{ -1\}$ and 
$$
\begin{align}
1+ \frac{1}{1+x}&= 0 \\
\frac{2+x}{1+x}&=0 \\
2+x&=0 \\
x&=-2
\end{align}
$$
the domain $x \neq-2$. Thus , the domain is $\mathbb{R}\setminus \{ -1,-2 \}$ 

ii) 
$$
\begin{align}
f\left( \frac{1}{x} \right)&= \frac{1}{1+\frac{1}{x}} \\
&= \frac{1}{ \frac{x+1}{x}} \\
&= \frac{x}{x+1}
\end{align}
$$

iii)
$$
\begin{align}
f(cx)&= \frac{1}{1+cx}
\end{align}
$$
iv)
$$
\begin{align}
f(x+y)&= \frac{1}{1+(x+y)}
\end{align}
$$
v) 
$$
\begin{align}
f(x)+f(y)&= \frac{1}{1+x}+ \frac{1}{1+y} \\
&=\frac{2+x+y}{(1+x)(1+y)}
\end{align}
$$


vi) For which numbers $c$ is there a number $x$ such that $f(cx)=f(x)$

$c=1$, for all number $x$. And $c\in \mathbb{R}$ for $x=0$.

vii) For which number $c$ is it true that $f(cx)=f(x)$ for two different numbers $x$?

$c=1$

2) Let $g(x)=x^{2}$, and let 

$$
h(x)=\begin{cases}
0,&x\text{ rational} \\
1,&x\text{ irrational}
\end{cases}
$$

i) For which $y$ is $h(y)\leq y$ 

$y\in \{ y\in \mathbb{Q}: y\geq 0 \}\cup\{ y\in \mathbb{Q}^{c}:y\geq 1 \}$. But notice that for any number $y\geq 1$, the statement is true. Thus, the set can be simplify to $y\in \{ y\in \mathbb{Q}:y\geq 0 \}\cup[1,\infty)$

ii) For which $y$ is $h(y)\leq g(y)?$

Case 1: when $y\in \mathbb{Q}$
Then $h(y)=0$. Since $g(y)\geq 0$ for all $y$. It follow that $y\in \mathbb{Q}$.

Case 2: $y\not\in \mathbb{Q}$
Then, $h(y)=1$. Solving $y^{2}\geq1$ give $|y|\geq 1$.

Combine 2 cases"
Notice that for all $y\in(-\infty,-1)\cup(1,\infty)$, the inequality hold. And $(-1,1)$ only hold when $y\in \mathbb{Q}$. Thus, 

$y\in(-\infty,-1)\cup(1,\infty)\cup \{ y\in \mathbb{Q}:-1<y<1 \}$


iii) What is $g(h(z))-h(z)?$

Case 1: $z\in \mathbb{Q}$
Then, $h(z)=0$, and $g(h(z))=(h(z))^{2}=0^{2}=0$. Thus $g(h(z))-h(z)=0$.

Case 2: $z\not\in \mathbb{Q}$
Then, $h(z)=1$ and $g(h(z))=1^{2}=1$. Thus, $g(h(z))-h(z)=1-1=0$.

Hence in both case,

$$
\begin{align}
g(h(z))-h(z)&=0 
\end{align}
$$

iv) For which $w$ is $g(w)\leq w$?

$$
\begin{align}
g(w)&\leq w \\
w^{2}&\leq w \\
w(w-1)&\leq 0
\end{align}
$$

Case 1: $w< 0$
Then, $w^{2}\geq 0>w$. Thus, $g(w)>w$ ^d0ed66

Case 2: $0\leq w\leq 1$
Then, multiply both side with $w$ implies $w^{2}\leq w$. Thus, $g(w)\leq w$

Case 3: $w> 1$
Then, multiply both side with $w$ implies $w^{2}>w$, Thus, $g(w)>w$

Hence, $w\in[-1,1]$ $\blacksquare$.

v) For which $\epsilon$ is $g(g(\epsilon))=g(\epsilon)$?

$$
\begin{align}
g(g(\epsilon))&=g(\epsilon) \\
g(\epsilon^{2})&=\epsilon^{2} \\
\epsilon^{4}&=\epsilon^{2} \\
\epsilon^{4}-\epsilon^{2}&=0 \\
\epsilon^{2}(\epsilon^{2}-1)&=0 \\
\epsilon^{2}(\epsilon-1)(\epsilon+1)&=0
\end{align}
$$

Thus, by zero product property it follow that $\epsilon=0$ or $\epsilon=1$ or $\epsilon=-1$

3) Find the domain of the functions defined by the following formulas.

i) $f(x)=\sqrt{ 1-x^{2} }$

$$
\begin{align}
1-x^{2}&\geq 0 \\
(1-x)(1+x)&\geq 0
\end{align}
$$
Case 1: $x<-1$
Then, $(1-x)>0$ and $(1+x)<0$. Thus, $(1-x)(1+x)<0\implies 1-x^{2}< 0$ 

Case 2: $-1\leq x\leq 1$
Since $x\leq 1$, it follow that $(1-x)\geq 0$ and since $x\geq -1$, it follow that $(1+x)\geq 0$. Thus, $1-x^{2}\geq 0$

Case 3: $x>1$
Then, $(1-x)< 0$ and $(1+x)>0$. Thus, it follow that $1-x^{2}< 0$.

Hence $x\in[-1,1]$

> [!remark]
> The method i use above is sign of the factors, we can also use another method (Interval testing) which is more easier.
>


ii) $f(x)=\sqrt{ 1-\sqrt{ 1-x^{2} } }$

$$
\begin{align}
1-\sqrt{ 1-x^{2} }&\geq 0 \\
\sqrt{ 1-x^{2} }&\leq 1 \\
0\leq1-x^{2}&\leq 1 &&(1)\text{ Since both are  same sign} \\ 
-1\leq-x^{2}&\leq 0 \\
0\leq x^{2}&\leq 1 \\
\end{align}
$$

$x^{2}\geq 0\implies x\in \mathbb{R}$. $x^{2}\leq 1\implies x^{2}-1\leq 0\implies x\in[-1,1]$ (from (i)). Thus $x\in[-1,1]$

> [!remark]
> (1) Need a justification from the statement below
> $\sqrt{ A }\leq B \iff 0\leq A\leq B^{2}$ 
> 
> Proof:
> Forward direction: Since $\sqrt{ A }\geq 0$ and $\sqrt{ A }\leq B$, it follow that
> 
> $$
> \begin{align}
> 0\leq \sqrt{ A }\leq B \\
> 0\leq A\leq B^{2}
> \end{align}
> $$
> By [[Basic Properties of Numbers#^1563fe]]
> 
> Backward direction is true by [[Basic Properties of Numbers#^78617a]]. $\blacksquare$.
> 
> (ix) and (x)  can be generalize to 
> 
> > [!Theorem]
> > if $a,b\geq 0$  then, $0\leq a<b \iff 0\leq a^{2}< b^{2}$ 
> 
> ^a1c187
> 
> It seem like we can combine (ix) and (x) directly into one biconditional statement without the condition $a,b\geq 0$ but notice that the backward direction need this condition. 
>
>The negative version:

> [!theorem]
> if $a,b\leq 0$, then $a<b\leq 0\iff 0\leq b^{2}\leq a^{2}$

iii) $f(x)= \frac{1}{x-1}+ \frac{1}{x-2}$
Let function $g$ denote $x\mapsto \frac{1}{x-1}$ and function $h$ denote $x\mapsto \frac{1}{x-2}$. Thus, $f=g+h$. Thus, the domain of $f$ is the intersection domain of $g$ and domain of $h$.

Domain of $g$:
$$
\begin{align}
x-1&=0 \\
x&=1
\end{align}
$$
Thus, $Domain(g)= \mathbb{R}\setminus \{ 1 \}$

Domain of  $h$:
$$
\begin{align}
x-2&=0 \\
x&=2
\end{align}
$$
Thus, $Domain(h)=\mathbb{R}\setminus \{ 2 \}$

Hence the intersection of this 2 domain are $x\in \mathbb{R}\setminus \{ 1,2 \}$ which is the domain of $f$.

v) $f(x)=\sqrt{ 1-x }+\sqrt{ x-2 }$

Let $g$ denote the function $x\mapsto \sqrt{ 1-x }$ and $h$ denote the function $x\mapsto \sqrt{ x-2 }$.

Domain of $g$:
$$
\begin{align}
1-x&\geq 0 \\
x&\leq 1
\end{align}
$$
Thus, $Domain(g)=(-\infty,1]$

Domain of $h$:
$$
\begin{align}
x-2&\geq 0 \\
x&\geq 2
\end{align}
$$

Thus, $Domain(h)=[2,\infty)$.

Since the intersection of these 2 domain are empty set, it follow that $Domain(f)=\emptyset$

> [!remark]
> If the domain is $\emptyset$, there are no pairs $(x,y)$ in the function at all. (It is called empty function)

4) Let $S(x)=x^{2}$, let $P(x)=2^{x}$, and let $s(x)=\sin x$. Find each of the following. In each case your answer should be a number.

i) 
$$
\begin{align}
(S\circ P)(y)&=(S(P(y))) \\
&= S(2^{y}) \\
&=(2^{y})^{2} \\
&= 2^{2y} \\
&= 4^{y}
\end{align}
$$
ii) 
$$
\begin{align}
(S\circ s)(y)&=S(s(y)) \\
&=S(\sin y) \\
&= (\sin y)^{2} \\
&=\sin ^{2}y
\end{align}
$$

iii)
$$
\begin{align}
(S\circ P\circ s)(t)+(s\circ P)(t)&=S(P(s(t)))+(s(P(t))) \\
&=S(P(\sin t))+(s(2^{t})) \\
&= S(2^{\sin t})+\sin 2^{t} \\
&=(2^{\sin t})^{2}+\sin 2^{t} \\
&=4^{\sin t}+\sin 2^{t}
\end{align}
$$
iv) 
$$
\begin{align}
s(t^{3})&=\sin t^{3}
\end{align}
$$

6) a) If $x_{1},\dots,x_{n}$ are distinct numbers, find a polynomial function $f_{i}$ of degree $n-1$ which is $1$ at $x_{i}$ and $0$ at $x_{j}$ for $j \neq i$. Hint: the product of all $(x-x_{i})$ for $j \neq i$, is $0$ at $x_{j}$ if $j \neq i$. (This product is usually denoted by
$$
\prod_{j=1,j \neq i}^{n} (x-x_{j})
$$

How this formula come from?
Let $f_{1}(x)$ be the polynomial function for 2 distinct number $x_{1}$, $x_{2}$. We want to find a degree-1 polynomial $f_{1}(x)$ such that: $f_{1}(x_{2})=0$ and $f_{1}(x_{1})=1$

If $f_{1}(x_{2})=0$, it follow that $(x-x_{2})$ is one of the factor of $f_{1}$. (Factor theorem). Thus, $f_{1}(x)=c\cdot(x-x_{2})$ for some constant $c$.

What must be the constant $c$ so that $f_{1}(x_{1})=1$?

$$
\begin{align}
f_{1}(x_{1})&=c(x_{1}-x_{2}) \\
c&= \frac{1}{x_{1}-x_{2}}
\end{align}
$$

Thus, $f_{1}(x)= \frac{x-x_{2}}{x_{1}-x_{2}}$.

Now suppose we have 3 distinct numbers $x_{1},x_{2},x_{3}$. We want a polynomial $f_{1}(x)$ of degree 2 such that $f_{1}(x_{1})=1$ and $f_{1}(x_{2})=0$ and $f_{1}(x_{3})=0$.

Then the same argument $f_{1}(x)=c(x-x_{2})(x-x_{3})$. Let

$$
\begin{align}
f_{1}(x_{1})&=1 \\
c(x_{1}-x_{2})(x_{1}-x_{3})&=1 \\
c&= \frac{1}{(x_{1}-x_{2})(x_{1}-x_{3})}
\end{align}
$$
Thus,

$$
f_{1}(x)= \frac{(x-x_{2})(x-x_{3})}{(x_{1}-x_{2})(x_{1}-x_{3})}
$$


So the general version is:
$$
f_{i}(x)= \prod_{j=1,j \neq i}^{n}\frac{(x-x_{j}) }{x_{i}-x_{j}}
$$

Notice that the degree is $n-1$ since $f_{i}(x)$ is a product of $n-1$ of linear term. When $x=x_{i}$, denominator is same as numerator make the hold product collapse to 1. When $x=x_{k}$ for any $k \neq i$, $f_i(x)=0$. (By remainder theorem)


> [!remark]
> We don't need to prove using induction because our proof is constructive i wrote down the explicit formula directly. The formula didn't rely on the step before $n$. ($1,2,\dots,n-1$).
>
>For example to show $f_{i}(x)=0$ for all $x=x_{j}$ where $j \neq i$ no need justification from previous step. We can just directly substitute.

b) Now find a polynomial function $f$ of degree $n-1$ such that $f(x_{i})=a_{i}$, where $a_{1},\dots,a_{n}$ are given numbers. (You should use the function from part (a)) (Lagrange interpolation formula)


Notice that
$$
f_{i}(x_{j})=\begin{cases}
1&j=i \\
0&j \neq i
\end{cases}
$$
We want to get $f(x_{i})=a_{i}$. Thus it must be $a_{i}f_{i}(x_{i})$. Because if it is $f_{j}$ where $j \neq i$, then $a_{i}f_{j}(x_{1})=a_{i}(0)=0$. Thus, the function is

$$
\begin{align}
f(x)&=a_{1}f_{1}(x)+a_{2}f_{2}(x)+\dots+a_{n}f_{n}(x) \\
&=\sum_{i=1}^{n} a_{i}f_{i}(x)
\end{align}
$$

When $x=x_{1}$, $a_{2}f_{2}(x)+\dots+a_{n}f_{n}(x)=0$ and $a_{1}f_{1}(x)=a_{1}$. Thus, $f(x_{1})=a_{1}$.

Generally, let $x=x_{k}$ for $k\in \{ 1,\dots,n \}$. Thus, 

$$
\begin{align}
f(x)&=a_{k}f_{k}(x_{k})+ \sum_{i=1,i \neq k}^{n}a_{i}f_{i}(x_{k}) \\
 &=a_{k}(1)+0 \\
 &=a_{k}
\end{align}
$$

Since $a_{i}f_{i}(x)$ is a $n-1$ degree function for $i\in \{ 1,\dots,n \}$ from (a), thus it follow that $f(x)$ is at most $n-1$ degree function. (The highest degree might cancel out)

> [!remark] Remark: Question (6) Lagrange interpolation rule
> 
> In this problem we prove that given any set of ordered pair that scattered everywhere for example $(1,999),(2,-\pi),(3, 10^{50}),\dots$ Problem 6 guarantees that there exist a single smooth polynomial curve that goes exactly though every single one of them.
> 
> How Lagrange think of it?
> Given a set of ordered pair, $(x_{1},a_{1}),(x_{2},a_{2})\dots(x_{n},a_{n})$, we need to find a smooth polynomial function $f(x_{i})=a_{i}$ for $i\in \{ 1,2,\dots,n \}$. 
> 
> How? What is the relationship of the point and the construction of polynomial function? Soon or later, we will think about $x-$intercept. If $(x_{i},0)$ is a $x-$intercept for a function $g$, then $g(x_{i})=0$, according to Factor Theorem, $(x-x_{i})$ is a linear factor of function $g$. 
> 
> But it is zero, there is nothing we can do to make $0$ become $a_{i}$. So, the next problem is can we make it to $1$, so that we can just multiply $a_{i}$ for the construction? 
> 
> But there is so many point, we need certain condition of rule to sort out the $x$ value, so whenever we plug in $x_{1}$, we will get $a_{1}$. It is some kind of switch like
> 
> $$
> f(x)=a_{1}f_{1}(x)+a_{2}f_{2}(x)+\dots+a_{n}f_{n}(x)
> $$
> 
> So we need to construct some thing like this:
> 
> $$
> f_{i}(x_{j})=\begin{cases}
> 1& j=i \\
> 0&j \neq i
> \end{cases}
> $$
> then we go back to $(a)$.

7) a) Prove Polynomial remainder theorem
b) Prove The Factor Theorem
c) A polynomial of degree $n$ has at most $n$ roots.
d Giving examples of degree $n$ polynomials with $n$ roots, 0 roots (for even $n$), or 1 root (for odd $n$).

8) For which numbers $a,b,c$ and $d$ will the function

$$
f(x)= \frac{ax+b}{cx+d}
$$
satisfy $f(f(x))=x$ for all $x$.

$f(f(x))=x$ for all $x$ means that $f(x)$ is a inverse function of itself.

$$
\begin{align}
f(f(x))=\frac{a\left( \frac{ax+b}{cx+d} \right)+b}{c\left( \frac{ax+b}{cx+d} \right)+d}&=x \\
\frac{\frac{a(ax+b)+b(cx+d)}{cx+d}}{\frac{c(ax+b)+d(cx+d)}{cx+d}}&=x \\
\frac{a(ax+b)+b(cx+d)}{c(ax+b)+d(cx+d)}&=x &&(1) \\
a(ax+b)+b(cx+d)&=x(cax+c b+dcx+d^{2}) \\
a^{2}x+ab+bcx+bd&= (a+d)cx^{2}+(c b+d^{2})x \\
(a^{2}+bc)x+(a+d)b&=(a+d)cx^{2}+(c b+d^{2})x \\
(a+d)cx^{2}+(c b+d^{2}-a^{2}-bc)x-(a+d)b&=0 \\
(a+d)cx^{2}+(d^{2}-a^{2})x-(a+d)b&=0 \\
(a+d)(cx^{2}+(d-a)x-b)&=0
\end{align}
$$

Case 1: $a+d=0$
$a+d=0\implies a=-d$

Case 2: $cx^{2}+(d-a)x-b=0$
For this to hold for all $x$, every coefficient must equal to 0. Thus, $c=0$ and $d-a=0\implies d=a$ and $b=0$

Substitution:
Case 1: 
$$
\begin{align}
f(x)= \frac{-dx+b}{cx+d} \text{ or } f(x)= \frac{ax+b}{cx-a}
\end{align}
$$

> [!question]
> How do these function look like?
> $f(x)=\frac{0x+1}{x+0}= \frac{1}{x}$ and $f(x)= \frac{-x+0}{0x+1}=-\frac{x}{1}=-x$ and $f(x)= \frac{2x+3}{5x-2}$.


Case 2:

$$
f(x)= \frac{ax+0}{0x+a}= \frac{ax}{a}=x
$$
This is simply identity function $f(x)=x$.


> [!question]
> Is there any restriction needed so that $f(x)$ doesn't collapse into a **constant function** (e.g., $f(x=5),$ where $f(f(x))=5 \neq x$)?
> (Hint: When is a fraction $\frac{ax+b}{cx+d}$ a constant? Think about the determinant $ad-bc$.)
> 
> The fraction will become a constant when
> $$
> \begin{align}
> ax+b&=n(cx+d) \\
> ax+b&=cnx+nd
> \end{align}
> $$
> $a=cn$ and $b=nd$ for some $n\in \mathbb{R}$. 
> 
> $$
> \begin{align}
> ad-bc&=cnd-cnd=0
> \end{align}
> $$
> Thus, when $ad-bc=0$, it follow that the function is a constant.

Notice that the question above is the implication form $(1)$, $c(ax+b)+d(cx+d) \neq 0$

Suppose $a=-d$ , then 

$$
\begin{align}
c(ax+b)+d(cx+d)&=-cdx+bc+cdx+d^{2} \\
&=bc+d^{2}
\end{align}
$$

and
$$
ad-bc=-d^{2}-bc=-(bc+d^{2})
$$

Notice that Denominator not equal to 0 implies that $bc+d^{2}\neq 0$ and $-(bc+d^{2})\neq 0$. Thus, $ad-bc \neq 0$.

Thus, the final answer is
Case 1: $a=-d$ and $ad-bc \neq 0$
Case 2: identity function

9)
