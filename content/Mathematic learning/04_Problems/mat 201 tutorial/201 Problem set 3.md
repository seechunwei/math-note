## Standard problems

1) (Easy) Let $a _ { n } = { \frac { 2 n } { 3 n + 1 } }$ for all $n \geq 1$ 

(a) Determine whether the sequence $\langle a _ { n } \rangle _ { n = 1 } ^ { \infty }$ is convergent or divergent. 

$$
\begin{align}
\lim_{ n \to \infty }  \frac{2n}{3n+1}&= \lim_{ n \to \infty } \frac{2}{3+\frac{1}{n}} \\
&= \frac{2}{3}
\end{align}
$$
Thus, it is convergent.


(b) Is the series $\sum _ { i = 1 } ^ { \infty } a _ { i }$ convergent or divergent? Why? 

Since $\lim_{ i \to \infty }a_{i} \neq 0$, by divergence test it follow that $\sum_{i=1}^{\infty}a_{i}$ is divergent.

(c) Let $s _ { n }$ denote the n-th partial sum of the series $\sum _ { i = 1 } ^ { \infty } a _ { i }$ . Is the sequence $\langle s _ { n } \rangle _ { n = 1 } ^ { \infty }$ convergent or divergent? 

Since the series $\sum_{i=1}^{\infty}a_{i}$ is divergent, it follow that
$$
\sum_{i=1}^{\infty} a_{i}=\lim_{ n \to \infty } s_{n}
$$
is also divergent by definition.


2) Express the number $2 . { \overline { { 5 1 6 } } } = 2 . 5 1 6 5 1 6 5 1 6 \dots$ as a ratio of integers. 

$$
2.\overline{516}=2+ \left( \frac{516}{1000}+ \frac{516}{1000^{2}}+\dots  \right)
$$
Note that the second term in the sum is a geometric series with $a=\frac{516}{1000}$ and $r= \frac{1}{1000}$. Since $\lvert r \rvert<1$, it follow that

$$
\begin{align}
S_{\infty}&= \frac{a}{1-r} \\
&=  \frac{\frac{516}{1000}}{\left( \frac{999}{1000} \right)} \\
&=\frac{516}{999} \\
\end{align}
$$
Thus,
$$
\begin{align}
2.\overline{516}&= 2+S_{\infty} \\
&=2+\frac{526}{999} \\
&= \frac{2564}{999} 
\end{align}
$$


3*) Determine the values of x for which the series $\sum _ { i = 0 } ^ { \infty } ( - 4 ) ^ { i } ( x - 5 ) ^ { i }$ is convergent. 

Remark: In Section 11.8, we will see that any series of this form is called a power series, and the values of x for which the series converges form an interval called the interval of convergence. 


$$
\begin{align}
\sum_{i=0}^{\infty} (-4)^{i}(x-5)^{i}&= \sum_{i=0}^{\infty} (-4(x-5))^{i} \\
&=\sum_{i=0}^{\infty} (-4x+20)^{i} 
\end{align}
$$

It is a geometric series, by theorem ![[Series#^4a9158]]
The series is divergent iff

$$
\begin{matrix}
\lvert -4x+20 \rvert\geq 1 \\
-4x+20\geq 1 &\text{or}&-4x\leq- 1\\
-4x\geq -19 &\text{or}&-4x\leq-21\\
 x\leq \frac{19}{4} &\text{or}&x\geq \frac{21}{4}
\end{matrix}
$$

Since the negation of convergent is divergent, it follow that the series is divergent iff
$$
\frac{19}{4}<x< \frac{21}{4}
$$


> [!remark]
> $\sum_{i=0}^{\infty}(-4x+20)^{i}$ is a geometric series, but note that the theorem start from $i=1$. But we can identify $a=1$ and $r=(-4x+20)$. Because when $i=0$, $a=(-4x+20)^{0}=1$

[[Center of convergent and radius of convergent]]

4) (a) If $\sum _ { i = 1 } ^ { \infty } a _ { i }$ is divergent and $c \neq 0 .$ , prove that $\sum _ { i = 1 } ^ { \infty } c a _ { i }$ is divergent.  ^eea206

Proof:
Assume for the sake of contradiction $\sum_{i=1}^{\infty}ca_{i}$ is convergent. Thus, there exist $L\in \mathbb{R}$ such that
$$
\lim_{ n \to \infty } s_{n}=\lim_{ n \to \infty } \sum_{i=1}^{n} ca_{i}=L
$$
Then, by law of series, it follow that $\sum_{i=1}^{\infty} \frac{1}{c}ca_{i}$ is convergent. Note that

$$
\begin{align}
\lim_{ n \to \infty }\sum_{i=1}^{n}  \frac{1}{c}ca_{i}&=  \lim_{ n \to \infty } \sum_{i=1}^{n} a_{i}
\end{align}
$$
Thus, $\sum_{i=1}^{\infty}a_{i}$ it convergent which is a contradiction. $\blacksquare$



(b*) If $\sum _ { i = 1 } ^ { \infty } a _ { i }$ is convergent and $\sum _ { i = 1 } ^ { \infty } b _ { i }$ is divergent, prove that $\sum _ { i = 1 } ^ { \infty } ( a _ { i } + b _ { i } )$ is divergent. 

Proof:
Suppose $\sum_{i=1}^{\infty}a_{i}$ is convergent, then $\lim_{ i \to \infty }a_{i}=0$. We need to show $\lim_{ i \to \infty }(a_{i}+b_{i}) \neq 0$.

$$
\begin{align}
\lim_{ i \to \infty } (a_{i}+b_{i})&=\lim_{ i \to \infty } a_{i}+\lim_{ i \to \infty } b_{i} \tag*{(1)}\\
&= \lim_{ i \to \infty } b_{i}
\end{align}
$$
But we cannot conclude anything from $\sum_{i=1}^{\infty}b_{i}$  is divergent. And also (1) is true when $\lim_{ i \to \infty }a_{i}$ and $\lim_{ i \to \infty }b_{i}$ exist.

Try prove by contradiction:
Suppose $\sum_{i=1}^{\infty}(a_{i}+b_{i})$ is convergent. Then since $\sum_{i=1}^{\infty}a_{i}$ is convergent, it follow that $\sum_{i=1}^{\infty}-a_{i}$ is also convergent. Thus, 
by Law of Series it follow that

$$
\begin{align}
\sum_{i=1}^{\infty} (a_{i}+b_{i}-a_{i})=\sum_{i=1}^{\infty} b_{i}
\end{align}
$$
is convergent which lead to contradiction. $\blacksquare$


(c*) Is it possible that $\sum _ { i = 1 } ^ { \infty } ( a _ { i } + b _ { i } )$ is convergent but both $\sum _ { i = 1 } ^ { \infty } a _ { i }$ and $\sum _ { i = 1 } ^ { \infty } b _ { i }$ are divergent? 

Yes ![[Series#^e95560]]


5) Determine whether the series is convergent or divergent. 

(a) $\sum _ { i = 1 } ^ { \infty } { \frac { 5 - 2 { \sqrt { i } } } { i ^ { 3 } } }$ 

$$
\frac{5-2\sqrt{ i }}{i^{3}}= \frac{5}{i^{3}}- \frac{2}{i^{5/2}}
$$
By p-series test, it follow that $\sum_{i=1}^{\infty} \frac{1}{i^{3}}$ and $\sum_{i=1}^{\infty} \frac{1}{i^{5/2}}$ is convergent. And by Law of Series, it follow that 
$$
\sum_{i=1}^{\infty} \frac{5}{i^{3}} \text{ and } \sum_{i=1}^{\infty} -\frac{2}{i^{5/2}}
$$

are both convergent. Thus, it follow that 

$$
\sum_{i=1}^{\infty} \frac{5}{i^{3}}+ \sum_{i=1}^{\infty}  -\frac{2}{i^{5/2}}= \sum_{i=1}^{\infty} \left( \frac{5}{i^{3}}- \frac{2}{i^{5/2}} \right)= \sum_{i=1}^{\infty}  \frac{5-2\sqrt{ i }}{i^{3}}
$$
is convergent. $\blacksquare$.

(b<sup>*</sup>) $\sum _ { i = 1 } ^ { \infty } \left( e ^ { \frac { 1 } { i } } - e ^ { \frac { 1 } { i + 1 } } \right)$ 

Note that we can use telescoping sum.

$$
\begin{align}
s_{n}&= e-e^{\frac{1}{2}}+ e^{\frac{1}{2}}-e^{\frac{1}{3}}+\dots+ e^{\frac{1}{n}}-e^{\frac{1}{n+1}} \\
&=e- e^{ \frac{1}{n+1}}
\end{align}
$$

Thus,
$$
\begin{align}
\lim_{ n \to \infty } s_{n}&=\lim_{ n \to \infty } e-e^{\frac{1}{n+1}} \\
&= e-1
\end{align}
$$


> [!warning]
> It didn't work because i try make it complicated, and i didn't notice the structure $f(x)-f(x+1)$ 
> $$
> \begin{align}
> e^{\frac{1}{i}}- e^{\frac{1}{i+1}}&= e^{\frac{1}{i}}\left( 1-e^{\frac{1}{i+1}- \frac{1}{i}} \right) \\
> &=e^{\frac{1}{i}}(1-)
> \end{align}
> $$
> 
> $$
> \begin{align}
> \frac{1}{i+1}- \frac{1}{i}= \frac{1}{i^{2}+i}
> \end{align}
> $$
> 

> [!remark]
> Since $\lim_{ i \to \infty }e^{1/i}$ and $\lim_{ i \to \infty }e^{\frac{1}{1+i}}$ are diverge we cannot use the Law of Series [[Series#^80f337]]

(c<sup>*</sup>) $\sum _ { i = 1 } ^ { \infty } \ln \left( { \frac { i ^ { 2 } + 1 } { 2 i ^ { 2 } + 1 } } \right)$ 

$$
\begin{align}
\lim_{ i \to \infty } \frac{i^{2}+1}{2i^{2}+1}&= \lim_{ i \to \infty } \frac{1+ \frac{1}{i^{2}}}{2+ \frac{1}{i^{2}}} \\
&= \frac{1}{2}
\end{align}
$$
Thus,
$$
\lim_{ i \to \infty } \ln\left(  \frac{i^{2}+1}{2i^{2}+1} \right)= \ln\left( \frac{1}{2} \right)\neq 0
$$

Hence, by Test of Divergence, it follow that $\sum_{i=1}^{\infty}\ln \left(  \frac{i^{2}+1}{2i^{2}+1} \right)$ is divergent. $\blacksquare$

> [!remark]
> We can push the limit inside because $\ln x$ is continuous on $(0,\infty)$ and notice that $\frac{i^{2}+1}{2i^{2}+1}> 0$ 

(d<sup>*</sup>) $\sum _ { i = 1 } ^ { \infty } { \frac { 1 + 3 ^ { i } } { 2 ^ { i } } }$ 

$$
\begin{align}
\frac{1+3^{i}}{2^{i}}&= \frac{1}{2^{i}}+ \left( \frac{3}{2} \right)^{i} \\
&= \left( \frac{1}{2} \right)^{i}+ \left( \frac{3}{2} \right)^{i}
\end{align}
$$
Note that $\lim_{ i \to \infty }\left( \frac{1}{2} \right)^{i}=0$ and $\lim_{ i \to \infty }\left( \frac{3}{2} \right)^{i}=\infty$. Thus,

$$
\lim_{ i \to \infty } \frac{1+3^{i}}{2^{i}}= \infty
$$
By Test of Divergent, it follow that $\sum_{i=1}^{\infty} \frac{1+3^{i}}{2^{i}}$ is divergent.

> [!remark]
> Note that the term are geometric sequence. Thus, by theorem $\lim_{ i \to \infty }\left( \frac{1}{2} \right)^{i}$ is converges and $\lim_{ i \to \infty }\left( \frac{3}{2} \right)^{i}$ is converges. Since $\lim_{ i \to \infty }\left( \frac{1}{2} \right)^{i}$ is just a real number, thus it cannot change the divergence of $\lim_{ i \to \infty } \frac{1+3i}{2i}$

(e) $\sum _ { i = 1 } ^ { \infty } { \frac { 1 } { 3 i + 2 } }$ 

Cannot use test of divergent. For all $i\geq 1$, it follow that
$$
\frac{1}{3i+2}> \frac{1}{6i}= \frac{1}{6}\left( \frac{1}{i} \right)
$$

Since $\sum_{i=1}^{\infty} \frac{1}{i}=\infty$ it follow that $\sum_{i=1}^{\infty} \frac{1}{6i}=\infty$. Ans since both series on contain nonnegative term. By Comparison Test, it follow that $\sum_{i=1}^{\infty} \frac{1}{3i+2}$ is divergent.$\blacksquare$

Another approach:
Use Limit Comparison Theorem. (No need the algebraic trick to create inequality). 

Note that when $i\to \infty$, 
$$
\frac{1}{3i+2}\approx \frac{1}{3i}
$$
Consider the limit below:

$$
\begin{align}
\lim_{ n \to \infty }  \frac{\frac{1}{3i+2}}{\frac{1}{3i}}&= \lim_{ n \to \infty } \frac{3i}{3i+2} \\
&=\lim_{ n \to \infty } \frac{3}{3+\frac{2}{i}} \\
&= 1
\end{align}
$$
Since $1>0$ and $\sum_{i=1}^{\infty} \frac{1}{3i}$ is divergent. It follow that $\sum_{i=1}^{\infty} \frac{1}{3i+2}$ is divergent.

Another approach: Integration Test

> [!question] What if the question is $\sum_{i=1}^{\infty} \frac{1}{3^{i}+2}?$ 
> $$
> \frac{1}{3^{i}+2}< \frac{1}{3^{i}}= \left( \frac{1}{3} \right)^{i}
> $$
> Note that $\sum_{i=1}^{\infty} \left( \frac{1}{3} \right)^{i}$ is a geometric series with $\lvert r \rvert<1$. Thus, the series is convergent. 
> 
> Since $\sum_{i=1}^{\infty} \frac{1}{3i+1}<\sum_{i=1}^{\infty}\left( \frac{1}{3} \right)^{i}$ ,  $\frac{1}{3i+2}\geq 0$ and $\left( \frac{1}{3} \right)^{i}\geq0$ 
> By comparison test, it follow that  $\sum_{i=1}^{\infty} \frac{1}{3i+2}$ is convergence.
> 


(f) $\sum _ { k = 1 } ^ { \infty } { \frac { 3 } { k ( k + 3 ) } }$ 

Note that
$$
\frac{3}{k(k+3)}= \frac{1}{k}- \frac{1}{k+3}
$$

Hence, we expand the partial sum
$$
\begin{align}
s_{n}&=\sum_{i=1}^{n} \frac{3}{i(i+3)}  \\
&= 1- \frac{1}{4}+ \frac{1}{2}- \frac{1}{5}+\frac{1}{3}- \frac{1}{6}+\frac{1}{4}-\frac{1}{7}+\dots+ \frac{1}{n}- \frac{1}{n+3} \\
&=1+\frac{1}{2}+ \frac{1}{3}- \frac{1}{n+1}- \frac{1}{n+2}- \frac{1}{n+3}
\end{align}
$$

Thus, 
$$
\lim_{ n \to \infty } s_{n}= 1+ \frac{1}{2}+\frac{1}{3}= \frac{11}{6}
$$


6*) Determine whether the series $\sum _ { i = 2 } ^ { \infty } { \frac { 1 } { i \ln i } }$ is convergent or divergent.  ^2e3a60

Note that the function $f(x)= \frac{1}{x \ln x}$ is positive and continuous on $[2,\infty)$. 

$$
\begin{align}
f'(x)&= \frac{-(1+\ln x)}{x^{2}(\ln x)^{2}} \\
&\leq0
\end{align}
$$
Thus, $f(x)$ is decreasing and we can apply Integral Test.

$$
\begin{align}
\int_{1}^{\infty} \frac{1}{x\ln x}   \, dx&= \lim_{ t \to \infty } \int_{2}^{t} \frac{1}{x\ln x} \, dx \\
&=\lim_{ t \to \infty } \left[  \ln(\ln x) \right]^{t}_{2} \tag*{(1)}   \\ \\
&= \lim_{ t \to \infty } (\ln(\ln t)-\ln(\ln 2)) \\
&= \infty
\end{align}
$$
By the integral test, the series $\sum_{i=2}^{\infty} \frac{1}{i \ln i}$ is diverge.

(1) Substitution: Let $u=\ln x\implies du= \frac{1}{x}dx\implies dx=xdu$. Thus,
$$
\begin{align}
\int \frac{1}{u} \, dx= \ln u=\ln(\ln x) 
\end{align}
$$

> [!remark]
> Why LCT fail:
> Note that $n$ is the leading term compare to $\ln n$
> if we compare with $b_{n}= \frac{1}{n}$, $\lim \frac{a_{n}}{b_{n}}= \lim \frac{1}{\ln n}=0$. (Inconclusive)



7*) Consider the series $\sum _ { i = 1 } ^ { \infty } i e ^ { - i }$ 

(a) Justify why the Integral Test can be applied. 

Consider the function $f(x)= \frac{x}{e^{x}}$, it is continuous, positive on $[1,\infty)$. Note that

$$
\begin{align}
f'(x)&= \frac{e^{x}-xe^{x}}{e^{2x}} \\
&= \frac{1-x}{e^{x}}
\end{align}
$$

$1-x\leq 0\implies x\geq 1$. Thus, $f(x)$ is decreasing when $x\geq 1$. Thus, we can apply Integral Test.

(b) Using the Integral Test, determine whether the series is convergent or divergent. 

$$
\begin{align}
\int_{1}^{\infty} \frac{ x}{e^{x}} \, dx&= \lim_{ t \to \infty } \int_{1}^{t}  \frac{x}{e^{x}} \, dx   
\end{align}
$$
Integration by part:
Let $u=x$ and $v'=e^{-x}$, thus $u'=1$ and $v=-e^{-x}$ . Hence,

$$
\begin{align}
\int \frac{x}{e^{x}} \, dx &=-xe^{-x}- \int -e^{-x} \, dx  \\
&=-xe^{-x}-e^{-x}
\end{align}
$$

Therefore, by substitution

$$
\begin{align}
\int_{1}^{\infty}  \frac{x}{e^{x}} \, dx&= \lim_{ t \to \infty }  [-xe^{-x}-e^{-x}]^{t}_{1}  \\
&= \lim_{ t \to \infty } [e^{-x}(-x-1)]^{t}_{1} \\
&= \lim_{ t \to \infty } (e^{-t}(-t-1)- e^{-1}(-2)) \\
&=\lim_{ t \to \infty } \frac{-t-1}{e^{t}}+ \frac{2}{e} \\
&\overset{H}{=} \lim_{ t \to \infty } \frac{-1}{e^{t}}+ \frac{2}{e} \\
&= \frac{2}{e}
\end{align}
$$

Thus, by Integral Test th series $\sum_{i=1}^{\infty} ie^{-1}$ is convergent.

8) (a) Show that the function $f ( x ) = { \frac { \ln x } { x ^ { 3 } } }$ is decreasing on $[ 2 , \infty )$ 

$$
\begin{align}
f'(x)&= \frac{x^{2}-2x^{2}\ln x}{x^{6}} \\
&= \frac{1-2\ln x}{x^{4}}
\end{align}
$$
$2\ln x\geq 1\implies x^{2}\geq e\implies x>\sqrt{ e }\approx 1.65$. Thus, $f(x)$ is decreasing on$[2,\infty)$.


(b) Show that $\int { \frac { \ln x } { x ^ { 3 } } } d x = - { \frac { \ln x } { 2 x ^ { 2 } } } - { \frac { 1 } { 4 x ^ { 2 } } } + c .$ 

Let $u=\ln x$ and $v'= \frac{1}{x^{3}}$, thus $u'= \frac{1}{x}$ and $v=- \frac{1}{2x^{2}}$. Integration by Parts:

$$
\begin{align}
\int \frac{\ln x}{x^{3}} \, dx& =-\frac{\ln x}{2x^{2}}- \int -\frac{1}{2x^{3}} \, dx  \\
&= - \frac{\ln x}{2x^{2}}- \frac{1}{4x^{2}}+c
\end{align}
$$


(c) Determine whether the series $\sum _ { i = 2 } ^ { \infty } { \frac { \ln { i } } { i ^ { 3 } } }$ is convergent or divergent. 

Note that the function $f(x)= \frac{\ln x}{x^{3}}$ is continuous, positive and decreasing on $[2,\infty)$.  Thus, we can apply Integration Test.

$$
\begin{align}
\int_{2}^{\infty}  \frac{\ln x}{x^{3}} \, dx&=\lim_{ t \to \infty } \int_{2}^{t} \frac{\ln x }{x^{3}} \, dx   \\
&=  \lim_{ t \to \infty } \left[ - \frac{\ln x}{2x^{2}}- \frac{1}{4x^{2}} \right]^{t}_{2} \\
&= \lim_{ t \to \infty } \left( - \frac{\ln t}{2t^{2}}- \frac{1}{4t^{2}}-\left( - \frac{\ln 2}{2(2)^{2}}- \frac{1}{4(2)^{2}} \right)  \right) \\
&=\lim_{ t \to \infty } -\frac{\ln t}{2t^{2}}-\lim_{ t \to \infty }  \frac{1}{4t^{2}} -\left( \frac{-\ln 2}{8}- \frac{1}{16} \right)
\end{align}
$$

Note that
$$
\begin{align}
\lim_{ t \to \infty } - \frac{\ln t}{2t^{2}}&\overset{H}{=} -\lim_{ t \to \infty } \frac{ \frac{1}{t}}{4t} \\
&=-\lim_{ t \to \infty }  \frac{1}{4t^{2}} \\
&=0
\end{align}
$$
Therefore,

$$
\begin{align}
\int_{2}^{\infty} \frac{ \ln x}{x^{3}} \, dx&=(0-0)-\left( \frac{-\ln 2}{8}- \frac{1}{16} \right) \\
&= \frac{\ln 2}{8}+ \frac{1}{16} \\
&= \frac{2\ln 2+1}{16}
\end{align}
$$

By Integration Test, it follow that $\sum_{i=2}^{\infty} \frac{\ln i}{i^{3}}$ is convergent. $\blacksquare$

## Non-standard problems 

9) (a) For any positive integer n, show that $\int _ { n } ^ { \infty } { \frac { 1 } { ( 2 x + 1 ) ^ { 6 } } } d x = { \frac { 1 } { 1 0 ( 2 n + 1 ) ^ { 5 } } } .$ 

$$
\begin{align}
\int_{n}^{\infty}  \frac{1}{(2x+1)^{6}} \, dx &= \lim_{ t \to \infty } \int_{n}^{t} \frac{1}{(2x+1)^{6}} \, dx \\
&= \lim_{ t \to \infty } \left[ -\frac{1}{10(2x+1)^{5}} \right]^{t}_{n} \\
&=\lim_{ t \to \infty } \left( -\frac{1}{10(2t+1)}+ \frac{1}{10(2n+1)^{5}}  \right) \\
&= \frac{1}{10(2n+1)^{5}}
\end{align}
$$

> [!remark]
> From here we know that it is converge assume that it fullfill the condition of integral test

(b*) How many terms of the series $\sum _ { i = 1 } ^ { \infty } { \frac { 1 } { ( 2 i + 1 ) ^ { 6 } } }$ would you need to find its sum to within 0.00001? 

Since $f(x)= \frac{1}{(2i+1)^{6}}$ is continuous, positive and decreasing on $[1,\infty)$. By Remainder Estimate Theorem,
$$
\begin{align}
\int_{n}^{\infty} \frac{1}{2x+1}^{6} \, dx &\leq 0.00001 \\
\frac{1}{10(2n+1)^{5}}&\leq 0.00001 \\
10(2n+1)^{5}&\geq \frac{1}{0.00001} \\
(2n+1)^{5}&\geq 10000 \\
2n+1&\geq 6.31 \\
n&\geq 2.655
\end{align}
$$

Thus, $n =3$ enough to approximate the series within 0.000001.

10) What is wrong with the following reasoning that leads to a contradiction? 

$$
\begin{array}{r l} & 0 = 0 + 0 + 0 + \dots \\ & \quad = (1 - 1) + (1 - 1) + (1 - 1) + \dots \\ & \quad = 1 - 1 + 1 - 1 + 1 - 1 + \dots \\ & \quad = 1 + (- 1 + 1) + (- 1 + 1) + (- 1 + 1) + \dots \\ & \quad = 1 + 0 + 0 + 0 + \dots = 1 \end{array}
$$

Note: No answer will be provided. 

> [!remark]
> We can always compare the growth speed of numerator and denominator. For example $\lim_{ i \to \infty } \frac{1+3i}{2i}$ in question 5(d), Note that $1+3i$ growth faster than $2i$, thus we can suspect that the limit is $\infty$.


