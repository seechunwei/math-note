1) Prove the following formulas by induction.
i) $1^{2}+\dots+n^{2}= \frac{n(n+1)(2n+1)}{6}$

Let $P(n)$ defined as

$$
P(n):1^{2}+\dots+n^{2}= \frac{n(n+1)(2n+1)}{6}
$$

For basis step, $P(1)$ is true because $1= \frac{6}{6}=\frac{1(1+1)(2(1)+1)}{6}$.

For induction step, suppose $n$ is an arbitrary integer where $n\geq 1$ and $P(n)$ is true.

$$
\begin{align}
1^{2}+\dots+n^{2}+(n+1)^{2}&= \frac{n(n+1)(2n+1)}{6}+(n+1)^{2} &&(\text{By IHS}) \\
&= \frac{(n+1)(n(2n+1)+6(n+1))}{6} \\
&= \frac{(n+1)(2n^{2}+7n+6)}{6} \\
&= \frac{(n+1)(n+2)(2n+3)}{6} \\
&= \frac{(n+1)(n+2)(2(n+1)+1)}{6}
\end{align}
$$

Thus, $P(n+1)$ is true. Hence, $P(n)$ is true for all $n\in \mathbb{N}$. $\blacksquare$

ii) $1^{3}+\dots+n^{3}=(1+\dots+n)^{2}$

Proof:
Let $P(n)$ be defined as
$$
P(n):1^{3}+\dots+n^{3}=(1+\dots+n)^{2}
$$

For basis step, $P(1)$ is true because $1^{3}=1=(1)^{2}$.

For induction step, suppose $n$ is an arbitrary natural number and $P(n)$ is true.

$$
\begin{align}
1^{3}+\dots+n^{3}+(n+1)^{3}&=(1+\dots+n)^{2}+(n+1)^{3}&&\text{By IHS} \\
&=1+\dots.+n^{2}+(n^{3}+3n^{2}+3n+1)
\end{align}
$$

$$
\begin{align}
n^{3}+3n(n+1)+1
\end{align}
$$


Does this related to conjugate twins? (i dont think so because it is $n^{3}$)

or $x^{n}+y^{n}$ when $n$ is odd (no because it is not only sum of 2 terms)

$(1+\dots+n)^{2}$ when we expand the first term will be 1 and last term will be $n^{2}$, where does the $n^{3}$ come from? i don't have any idea

wait , earlier we have a formula :
$$
\begin{align}
1+\dots+n &=\frac{n(n+1)}{2} \\
(1+\dots+n)^{2}&= \frac{n^{2}(n+1)^{2}}{4}
\end{align}
$$

Thus,

$$
\begin{align}
(1+\dots+n)^{2}+(n+1)^{3}&= \frac{n^{2}(n+1)^{2}}{4}+(n+1)^{3} \\
&= (n+1)^{2}\left( \frac{n^{2}}{4}+(n+1) \right) \\
&=(n+1)^{2}\left( \frac{n^{2}+4n+4}{4} \right) \\
&=(n+1)^{2}\left( \frac{(n+2)^{2}}{4} \right) \\
&= \left( \frac{(n+1)(n+2)}{2} \right)^{2} \\
&=(1+\dots+n+(n+1))^{2}
\end{align}
$$


> [!NOTE]
> Remark
> I didn't recognize $1+\dots+n$ as an object. By brain treat it as a normal square expand.
> 
> Recursive Form vs Closed Form
> Express a sum written with an ellipsis such as $S_{n}=1+\dots+n$ in to $\frac{n(n+1)}{2}$  

2）Find a formula for
i) $\sum_{i=1}^{n}(2i-1)=1+3+5+\dots+(2n-1)$

Let $S=1+3+5+\dots+(2n-1)$
and $S=(2n-1)+(2n-3)+\dots+3+1$

Notice that $2n-1+1=2n$ and so do other terms and there are $n$ such term. Thus,

$$
\begin{align}
2S&=n(2n) \\
S&=\frac{2n^{2}}{2} \\
S&=n^{2}
\end{align}
$$
ii)
Since the question is about sum of square, let's try find out how we get the formula for $1^{2}+2^{2}+\dots+n^{2}$:
$$
n^{2}+1^{2}=(n+1)^{2}-2n
$$

$$
(n-1)^{2}+2^{2}= (n+1)^{2}-4(n-1)
$$

$$
(n-2)^{2}+3^{2}=(n+1)^{2}-6(n-2)
$$

Notice that the cross term for the $k-th$ pair is:
$2k(n+1-k)=2(n+1)k-2k^{2}$ , notice that when we add up the $k^{2}$ become $1^{2}+2^{2}+\dots+n^{2}$ again. 

Notice that the question sequence is about odd number and

$$
\begin{align}
1^{2}+2^{2}+\dots+2n^{2}=(1^{2}+3^{2}+\dots+(2n-1)^{2})+(2^{2}+4^{2}+\dots+(2n)^{2}) \\
\end{align}
$$

Why it is until $2n^{2}$? because the last number are even number $2n$ while the last odd number is $2n-1$.

Notice that $2^{2}+4^{2}+\dots+(2n)^{2}=(1\cdot 2)^{2}+(2\cdot 2)^{2}+\dots+(2\cdot n)^{2}$. We can factor out the $2^{2}$. Thus, it the sum become

$$
\frac{4(n)(n+1)(2n+1)}{6}
$$

Thus,

$$
\begin{align}
\sum_{i=1}^{n} (2i-1)^{2}&= \frac{2n(2n+1)(4n+1)}{6}- \frac{4n(n+1)(2n+1)}{6} \\
&= \frac{2n(2n+1)(4n+1-2(n+1))}{6} \\
&= \frac{n(2n+1)(2n-1)}{3}
\end{align}
$$

> [!remark]
> I cannot do this question because i didn't notice the even number sequence is just normal sequence multiply 2 and it is from the definition $2n$. It is the same for odd number $2n+1$.

3) If $0\leq k\leq n$, the "Binomial coefficient" $\binom{n}{k}$ is defined by

$$
\begin{align}
\binom{n}{k}&= \frac{n!}{k!(n-k)!} \\
&= \frac{n(n-1)\dots(n-k+1)}{k!} &&\text{ if }k\neq 0,n
\end{align}
$$

Why Spivak write a condition if $k\neq 0$? It is because we haven't define $0!$.

Actually $0!=1$ and the one of the consequence is $\binom{n}{0}=\binom{n}{n}=1$

a) Prove that 
$$
\binom{n+1}{k}=\binom{n}{k-1}+\binom{n}{k}
$$

(The proof does not require an induction argument)

$$
\begin{align}
\binom{n+1}{k}&= \frac{(n+1)!}{k!(n+1-k)!} \\
&= \frac{(n+1)(n)\dots(n+2-k)}{k!}
\end{align}
$$
$$
\begin{align}
\binom{n}{k-1}+\binom{n}{k}&= \frac{n(n-1)\dots(n-k+2)}{(k-1)!}+ \frac{n(n-1)\dots(n-k+1)}{k!} \\
&= \frac{n(n-1)\dots(n-k+2)k}{k!}+ \frac{n(n-1)\dots(n-k+1)}{k!} \\
&= \frac{n(n-1)\dots(n+2-k)(k+(n-k+1))}{k!} \\
&= \frac{n(n-1)\dots(n+2-k)(n+1)}{k!} \\
&=\binom{n+1}{k} &&\blacksquare
\end{align}
$$

The identity we just proved earlier explain how we construct the Pascal Triangle.

If we label the rows by $n$ (start from 1) and the position in each row by $k$,(start from 1). Then, the value $\binom{n}{k}$ is exactly the entry for $n+1$ row and $k+1$ position.

The identity we just proved earlier show that a entry in Pascal Triangle obtained by sum up the 2 adjacent entry in previous row.

Notice that it is somehow a recursive definition for binomial coefficient using binomial coefficient (at first we use factorial) 

b) Use part (a) to prove by induction that $\binom{n}{k}$ is always a natural numbers. 

Proof;
Let $P(n)$ defined as
$$
P(n): \binom{n}{k}\in \mathbb{N}
$$
for $0\leq k\leq n$ where $n\in \mathbb{N}$.

For basis step, $P(1)$ is true because $\binom{1}{0}=\binom{1}{1}=1\in \mathbb{N}$.

For induction step, suppose $n$ is an arbitrary natural number and $P(n)$ is true. Thus, by part (a) we have

$$
\begin{align}
\binom{n+1}{k}&= \binom{n}{k-1}+\binom{n}{k} \\
\end{align}
$$
Notice that $\binom{n}{k+1}$ and $\binom{n}{k}$ are natural number by induction hypothesis. Since natural number is closed under addition, it follow that $\binom{n+1}{k}\in \mathbb{N}$ for all $1\leq k\leq n$ (Because if $k=0$, then $\binom{n}{-1}$ does not exist and the identity didn't use $k+1$). 

How about when $k=n+1$? Then $\binom{n+1}{n+1}=1\in \mathbb{N}$. It is the same when $k=0$.

Thus, $P(n+1)$ is true. Hence, $P(n)$ is true for all $n\in \mathbb{N}$. $\blacksquare$

c) Give another proof that $\binom{n}{k}$ is a natural number by showing that $\binom{n}{k}$ is the number of sets of exactly $k$ integers each chosen from $1,\dots,n$.

Notice that from the definition
$$
\binom{n}{k}= \frac{n(n-1)\dots(n-k+1)}{k!}
$$
It is not obvious that $k!$ as a denominator will always divide into the numerator without a remainder. But if we can prove that the binomial coefficient is actually the number of counting way, then it must be natural number.

Suppose there are number $1,2,\dots ,n$. And we need to choose $k$ integer from these number. Thus,

First pick: There are $n$ option to pick
Second pick: There are $n-1$ option to pick
$\vdots$
$k$ pick: There are $n-k+1$ option to pick

Thus, it is simply $\frac{n!}{(n-k)!}$. Notice that the order doesn't matter thus ,one set of integer, there are $k!$ ways to arrange. Thus, the total number of counting is

$$
\frac{n!}{k!(n-k)!}
$$

d) Prove the 'Binomial Theorem': If $a$ and $b$ are any numbers and $n$ is a natural number, then

$$
(a+b)^{n}=\sum_{j=0}^{n} \binom{n}{j}a^{n-j}b^{j}
$$

When $n =2$, $(a+b)^{2}=a^{2}+ab+ba+b^{2}$
When $n =3$, $(a+b)^{3}=a^{3}+3a^{2}b+3ab^{2}+b^{3}$

The coefficient of each term is the total number of way arrange the product. For example, $aab=aba=baa$, so there is total 3 way which is $\frac{3!}{2!}$ because 2 object are identical. 

But spivak want us to prove this theorem.

Proof:
$$
\begin{align}
(a+b)^{n+1}&= (a+b)(a+b)^{n}\\ 
&=a(a+b)^{n}+b(a+b)^{n} \\
&=a\sum_{j=0}^{n}\binom{n}{j}a^{n-j}b^{j}+b\sum_{j=0}^{n} \binom{n}{j}a^{n-j}b^{j}  &&\text{By IHP}\\
&=\sum_{j=0}^{n} \binom{n}{j}a^{n+1-j}b^{j}+\sum_{j=0}^{n}\binom{n}{j}a^{n-j}b^{j+1}  \\
&= a^{n+1}+\sum_{j=1}^{n}\binom{n}{j} a^{n+1-j}b^{j}+\sum_{j=0}^{n-1}\binom{n}{j}a^{n-j}b^{j+1} +b^{n+1}
\end{align}
$$


Notice that the first sum (from multiplying by a):
$$
\binom{n}{0}a^{n+1}+\binom{n}{1}a^{n}b+\binom{n}{2}a^{n-1}b^{2}+\dots+\binom{n}{n}ab^{n}
$$

The second sum (from multiplying by b):
$$
\binom{n}{0}a^{n}b+\binom{n}{1}a^{n-1}b^{2}+\dots+\binom{n}{n-1}ab^{n}+\binom{n}{n}b^{n+1}
$$

Notice that the coefficient of the middle term is $\binom{n}{k}+\binom{n}{k-1}$. For example, $\binom{n}{1}a^{n}b+\binom{n}{0}a^{n}b=\binom{n+1}{1}a^{n}b$ by identity in (a).
And notice that the 2 outer edges are also $\binom{n}{0}=1=\binom{n+1}{0}$ and $\binom{n}{n}=1=\binom{n+1}{n+1}$. Thus, every term from $k=1$ to $k=n+1$ match the form:

$$
\binom{n+1}{k}a^{n+1}b^{k}
$$

$$
\begin{align}
(a+b)^{n+1}=\sum_{j=0}^{n+1}\binom{n+1}{j} a^{n+1-j}b^{j}
\end{align}
$$

> [!remark] 
> What is idea idea behind this proof?
> 
> Still remember the $n$ for $(a+b)^{n}$ is the $n+1-th$ row in Pascal triangle and the $k$ is the $k+1-th$ position. What happen when $n+1$? By the Pascal triangle or the identity, we know that each term coefficient is actually the sum of coefficient at $n-th$ row at $k$ and $k-1$ position. 
> 
> How a term appear in 2 different position? The answer lies in multiplying $a$ and multiplying $b$ by the $n-th$ row. (multiplying $b$ shift all power of b up by one position)

e) 
i) 
$$
\sum_{j=0}^{n} \binom{n}{j}=\binom{n}{0}+\dots+\binom{n}{n}=2^{n}
$$
Proof:
Notice that $2^{n}=(1+1)^{n}$. And by binomial theorem

$$
\begin{align}
(1+1)^{n}&=\sum_{j=0}^{n}\binom{n}{j} 1^{n-j}1^{j} \\
\end{align}
$$

Notice that $1^{n-j}1^{j}=1$ for for all $j,k\in \mathbb{\mathbb{Z}}$. Thus,

$$
\begin{align}
2^{n}=\sum_{j=0}^{n} \binom{n}{j}
\end{align}
$$

ii)
$$
\sum_{j=0}^{n} (-1)^{j}\binom{n}{j}=\binom{n}{0}-\binom{n}{1}+\dots\pm \binom{n}{n}
$$

If we let $a=1$ and $b=1$, then each term is $1\cdot 1=1$, to make alternating sign, we let $b=1$. Thus,

$$
\begin{align}
(1+(-1))^{n}&=\sum_{j=0}^{n} \binom{n}{j}1^{n-j}(-1)^{j} \\
0&=\binom{n}{0}-\binom{n}{1}+\dots\pm \binom{n}{n}
\end{align}
$$
iii)
Notice that 
$$
\begin{align}
\binom{n}{1}+\binom{n}{3}+\dots&=\frac{1}{2}\binom{n}{0}-\binom{n}{0}+\binom{n}{1}-(-\binom{n}{1})+\dots \\
&= \frac{1}{2} (2^{n}-0) \\
&=2^{n-1}
\end{align}
$$

> [!remark]
> To form a odd number series, we can subtract a natural number series with its alternating series and divide by 2.
> 
> If we want even then we just add and divide 2
>
>Why we cannot use the concept of $2,4,\dots=2(1,2,\dots)$? Because the $n$ here is not the sequence, it only control the last number

iv) 
From the remark above, we know that 

$$
\begin{align}
\sum_{j=0}^{n} \binom{n}{j}+ \sum_{j=0}^{n}(-1)^{j}\binom{n}{j}&= 2 \sum_{\text{j even}} \binom{n}{j}   \\
\frac{2^{n}+0}{2}&=\sum_{\text{j even}}\binom{n}{j} \\
\sum_{\text{j even}} \binom{n}{j}  &= 2^{n-1}
\end{align}
$$



Notice that 

$$
\begin{align}
\sum_{\text{i odd}} \binom{n}{i}+\sum_{\text{i even}}\binom{n}{i}&= \sum_{i=0}^{n} \binom{n}{i} \\
2^{n-1}+ \sum_{\text{i even}}\binom{n}{i}&= 2^{n} \\
\sum_{\text{i even}} \binom{n}{i}&=2^{n}-2^{n-1} \\
&=2^{n}\left( 1- \frac{1}{2} \right) \\
&=2^{n}(2^{-1}) \\
&=2^{n-1}  
\end{align}
$$
4) a) Prove that

$$
\sum_{k=0}^{l} \binom{n}{k}\binom{m}{l-k}=\binom{n+m}{l}
$$
Hint: Apply the binomial theorem to $(1+x)^{n}(1+x)^{m}$. (Vandermonde's Identity)

Proof:

$$
\begin{align}
(1+x)^{n}(1+x)^{m}&=(1+x)^{n+m} \\
\sum_{i=0}^{n}\binom{n}{i} x^{i} \cdot \sum_{i=0}^{m}\binom{m}{i} x^{i}&=\sum_{i=0}^{n+m} \binom{n+m}{i} x^{i} 
\end{align}
$$

Let's consider what is the coefficient of $x^{l}$. It is $\binom{n+m}{l}$ on right hand side. For left hand side, it should be $0+l,1+l-1,\dots$.. For example $x^{0}\cdot x^{l}=x^{l}$. 

Notice that there are many possibility and we need to sum up all the coefficient for each possible $x^{l}$. Thus, it is

$$
\begin{align}
\sum_{k=0}^{l} \binom{n}{k}\binom{m}{l-k} x^{k}= \binom{n+m}{i}x^{i}
\end{align}
$$
Thus,


$$
\sum_{k=0}^{l} \binom{n}{k}\binom{m}{l-k}
$$

What if $l>m$ or $l>n$? Then $0+l$ or $l+0$ is impossible, and $\binom{n}{l}$ or $\binom{m}{l}$ is undefined. Hence, it is safe.

b) Prove that

$$
\sum_{k=0}^{n} \binom{n}{k}^{2}=\binom{2n}{n}
$$


Proof:
Notice that $\binom{2n}{n}=\binom{n+n}{n}$. Thus, by 4(a), it follow that

$$
\sum_{k=0}^{n} \binom{n}{k}\binom{n}{n-k}= \binom{2n}{n}
$$

Notice that $\binom{n}{n-k}=\binom{n}{k}$ because

$$
\begin{align}
\binom{n}{n-k}&= \frac{n!}{(n-k)!(n-(n-k))!} \\
&=\frac{n!}{(n-k)!(k)!} \\
&= \binom{n}{k}
\end{align}
$$
Hence,  by substitution

$$
\begin{align}
\sum_{k=0}^{n} \binom{n}{k}^{2}=\binom{2n}{n}
\end{align}
$$

5) a) Prove by induction on $n$ that

$$
1+r+r^{2}+\dots+r^{n}= \frac{1-r^{n+1}}{1-r}
$$
if $r \neq 1$. (if $r=1$, then the sum is simply $n+1$)

Proof:
Suppose $P(n)$ defined as
$$
P(n):1+r+r^{2}+\dots+r^{n}= \frac{1-r^{n+1}}{1-r}
$$

For basis step, notice that
$$
\begin{align}
\frac{1-r^{2}}{1-r}&= \frac{(1-r)(1+r)}{1-r} \\
&=1+r
\end{align}
$$

thus, it is clear that $P(1)$ is true, because $1+r^{1}=1+r= \frac{1-r^{2}}{1-r}$.


For induction step, suppose $n$ is an arbitrary natural number and $P(n)$ is true. Thus,

$$
\begin{align}
1+r+r^{2}+\dots+r^{n}+r^{n+1}&= \frac{1-r^{n+1}}{1-r}+r^{n+1} &&\text{By IHP} \\
&= \frac{1-r^{n+1}+(1-r)(r^{n+1})}{1-r} \\
&= \frac{1-r^{n+1}+(r^{n+1}-r^{n+2})}{1-r} \\
&= \frac{1-r^{n+2}}{1-r}
\end{align}
$$

Thus, $P(n+1)$ is true. Hence, $P(n)$ is true for all $n\in \mathbb{N}$.$\blacksquare$



> [!remark]
>  Why it is suitable for induction? Because it have a recursive definition
> $$
> S_{1}=1+r \text{ and } S_{n+1}=S_{n}+r^{n+1}
> $$


b) Derive this result by setting $S=1+r+\dots+r^{n}$, multiplying this equation by $r$, and solving the two equations for $S$.

$$
\begin{align}
S&=1+r+\dots+r^{n} \\
rS&=r+r^{2}+\dots+r^{n+1}
\end{align}
$$

Thus,
$$
\begin{align}
S-rS&=1+r^{n+1} \\
S(1-r)&= 1+r^{n+1} \\
S&= \frac{1+r^{n}}{1-r}
\end{align}
$$


6) The formula for $1^{2}+\dots+n^{2}$ may be derived as follows. We begin with the formula

$$
(k+1)^{3}-k^{3}=3k^{2}+3k+1
$$
Writing this formula for $k=1,\dots,n$ and adding, we obtain

$$
\begin{align}
2^{3}-1^{3}&=3\cdot 1^{2}+3\cdot 1+1 \\
3^{3}-2^{3}&=3 \cdot 2^{2}+3 \cdot 2+1 \\
\vdots  \\
(n+1)^{3}-n^{3}&=3\cdot n^{2}+3\cdot n+1
\end{align}
$$
We add from $k=1,\dots,n$ , notice that the intermediate term cancel each other and leave $(n+1)^{3}-1^{3}$. Thus, we get

$$
(n+1)^{3}-1=3(1^{2}+2^{2}+\dots+n^{2})+3\cdot(1+2+\dots+n)+n
$$

Thus, we can find $\sum_{k=1}^{n}k^{2}$ if we already know $\sum_{k=1}^{n}k$ (which could have been found in a similar way). How?

Consider

$$
\begin{align}
(k+1)^{2}-k^{2}=2k+1
\end{align}
$$

Adding from $k=1,\dots,n$ , we get

$$
\begin{align}
(n+1)^{2}-1&=2(1+2+\dots+n)+n \\
1+2+\dots+n&= \frac{(k+1-1)(k+1+1)-n}{2} \\
&= \frac{n(n+2)-n}{2} \\
&= \frac{n(n+1)}{2}
\end{align}
$$

How about $1^{2}+2^{2}+\dots+n^{2}$?
From earlier result, we have

$$
\begin{align}
(n+1)^{3}-1&=3(1^{2}+2^{2}+\dots+n^{2})+3\cdot(1+2+\dots+n)+n \\
(n +1)^{3}-1&= 3 \frac{n(n+1)}{2}+3 \sum_{k=1}^{n} k^{2}+n \\
3\sum_{k=1}^{n}k^{2}&= (n+1)^{3}-1-3 \frac{n(n+1)}{2} -n\\
&= \frac{2(n+1)^{3}-2-3n(n+1)-2n}{2} \\
&= \frac{2(n+1)^{3}-2-(3n^{2}-3n)-2n}{2} \\
\sum_{k=1}^{n} k^{2}&= \frac{2(n+1)^{3}-(3n^{2}+3n+2+2n)}{6} \\
&= \frac{2(n+1)^{3}-(3n^{2}+5n+2)}{6} \\
&= \frac{2(n+1)^{3}-(3n+2)(n+1)}{6} \\
&= \frac{(n+1)(2(n+1)^{2}-(3n+2))}{6} \\
&= \frac{(n+1)(2n^{2}+4n+2-3n-2)}{6} \\
&= \frac{(n+1)(2n^{2}+n)}{6} \\
&= \frac{n(2n+1)(n+1)}{6}
\end{align}
$$

Use this method to find 
i) $1^{3}+\dots+n^{3}$

Consider 
$$
\begin{align}
(k+1)^{4}-k^{4}&=4k^{3}+6k^{2}+4k+1
\end{align}
$$
Adding from $k=1,2,\dots,n$ 

$$
\begin{align}
(n+1)^{4}-1&=4\sum_{k=1}^{n}k^{3}+6 \sum_{k=1}^{n} k^{2}+4\sum_{k=1}^{n} k+n \\
4 \sum_{k=1}^{n} k^{3} &= (n+1)^{4}-1-6\sum_{k=1}^{n} k^{2}-4\sum_{k=1}^{n} k-n \\
&=(n+1)^{4}-1-6 \frac{n(2n+1)(n+1)}{6}-4 \frac{n(n+1)}{2}-n \\
&= (n+1)^{4}-1-n(2n+1)(n+1)-2n(n+1)-n \\
&= (n+1)^{4}-(n+1)-(n+1)(2n^{2}+n+2n) \\
&= (n+1)^{4}-(n+1)(1+2n^{2}+3n) \\
&=(n+1)^{4}-(n+1)(2n+1)(n+1) \\
&=(n+1)^{4}-(n+1)^{2}(2n+1) \\
&=(n+1)^{2}((n+1)^{2}-2n-1) \\
&=(n+1)^{2}(n^{2}+2n+1-2n-1) \\
&=(n+1)^{2}n^{2} \\
\sum_{k=1}^{n} k^{3}&= \frac{n^{2}(n+1)^{2}}{4}
\end{align}
$$

> [!remark]
> Notice that 
> 
> $$
> \left( \sum_{k=1}^{n} k \right)^{2}=\sum_{k=1}^{n}k^{3} 
> $$
> and it is called Nicomachus's Theorem
> 
> [[The Consecutive Difference Principle (Telescoping Sums)]]
^spivak-ch2-prob6

iii)

Let $\triangle f=f(n+1)-f(n)$ where $f(n)= \frac{1}{(n-1)n}$ 

Notice that  $\frac{1}{n(n+1)}= \frac{1}{n}-\frac{1}{n+1}$ by partial fraction.

$$
\begin{align}
\sum_{k=1}^{n} \frac{1}{k(k+1)}&=\sum_{k=1}^{n}  \left( \frac{1}{k}- \frac{1}{k+1} \right) \\
&= 1- \frac{1}{2}+ \frac{1}{2}- \frac{1}{3}+\dots- \frac{1}{n+1} \\
&=1- \frac{1}{n+1} \\
&= \frac{n}{n+1}
\end{align}
$$

> [!remark]
> The fundamental challenge of telescoping summation is: **How to express the summand as a consecutive difference?**
> * **For Power Sums ($k^p$):** When we cannot easily find $f(k)$ directly for $k^p$, we manufacture the difference by expanding the higher-degree binomial $(k+1)^{p+1} - k^{p+1}$.
> * **For Rational Fractions ($\frac{1}{k(k+1)}$):** We split the term using partial fractions into $\frac{1}{k} - \frac{1}{k+1}$ (where $f(k) = \frac{1}{k}$).
> 
> See [[The Consecutive Difference Principle (Telescoping Sums)]]

iv) Notice that

$$
\begin{align}
\frac{2n+1}{n^{2}(n+1)^{2}}&=  \frac{A}{n}+ \frac{B}{n^{2}}+ \frac{C}{(n+1)}+ \frac{D}{(n+1)^{2}}
\end{align}
$$
But there is faster way to do this. Notice that
$$
\begin{align}
(n+1)^{2}-n^{2}=+2n+1
\end{align}
$$
Thus,

$$
\begin{align}
\frac{2n+1}{n^{2}(n+1)^{2}}&= \frac{(n+1)^{2}-n^{2}}{n^{2}(n+1)^{2}} \\
&= \frac{1}{n^{2}}- \frac{1}{(n+1)^{2}}
\end{align}
$$

Notice that it is the consecutive difference of $f(n)= \frac{1}{n^{2}}$. Thus, again by the same method

$$
\begin{align}
\sum_{k=1}^{n}  \frac{2n+1}{n^{2}(n+1)^{2}}&= \sum_{k=1}^{n} \frac{1}{k^{2}}- \frac{1}{(k+1)^{2}} \\
&= 1- \frac{1}{(n+1)^{2}} \\
&= \frac{(n+1)^{2}-1}{(n+1)^{2}} \\
&= \frac{(n+1-1)(n+1+1)}{(n+1)^{2}} \\
&= \frac{n(n+2)}{(n+1)^{2}}
\end{align}
$$

> [!remark]
> Notice that for 6)iii) and 6)iv) 
> 
> $$
> \begin{align}
> \sum_{k=1}^{\infty}f(k)= 1 
> \end{align}
> $$
> because of the telescoping collapse, the middle term collapse together and leave the initial term and last term. Notice that as $n\to \infty$, $\frac{1}{n+1}\to 0$ and $\frac{1}{(n+1)^{2}}\to 0$. 

7) Use the method of Problem 6 to show that $\sum_{k=1}^{n}k^{p}$ can always be written in the form

$$
\frac{n^{p+1}}{p+1}+An^{p}+Bn^{p-1}+Cn^{p-2}+\dots
$$

Notice that the ellipsis here means continue descending though all remaining lower power of $n$. 

Proof:
We prove by using induction. Let $P(p)$ be the statement below:
$\sum_{k=1}^{n} k^{p}$ can be written as $\frac{n^{p=1}}{p+1}+An^{p}+Bn^{p-1}+Cn^{p-2}+\dots$
or
$\sum_{k=1}^{n}k^{p}$ is a polynomial in $n$ of degree $p+1$ with leading term $\frac{n^{p+1}}{p+1}$.

For basis step, $P(1)$ is true because

$$
\sum_{k=1}^{n} k= \frac{n(n+1)}{2}= \frac{1}{2}n^{2}+\frac{1}{2}n
$$

For induction step, suppose $p$ is an arbitrary natural number and $P(p)$ is true for all $1,2,3,\dots,p$. Thus, notice that

$$
\begin{align}
(k+1)^{p+1}-k^{p+1}= \binom{p+1}{1}k^{p}+\binom{p+1}{2}k^{p-1}+\dots+\binom{p+1}{p+1}k^{0}
\end{align}
$$

Now we sum both side from $k=1$ to $n$:

$$
\begin{align}
(n+1)^{p+1}-1&= (p+1)\sum_{k=1}^{n} k^{p}+\binom{p+1}{2}\sum_{k=1}^{n} k^{p-1}+\dots+ \sum_{k=1}^{n} k+n \\
(p+1)\sum_{k=1}^{n} k^{p}&= (n+1)^{p+1}-1-\binom{p+1}{2}\sum_{k=1}^{n} k^{p-1}-\dots-\sum_{k=1}^{n} k-n \\
\sum_{k=1}^{n} k^{p}&= \frac{(n+1)^{p+1}-1}{p+1}+An^{p}+\dots &&(1) \text{ By IHP}
\end{align}
$$

Justification for (1): Notice that $\binom{p+1}{2}\sum_{k=1}^{n}k^{p-1}-\dots-n$ is a summation of power less than $p$. Thus, by induction hypothesis each term can be express as a polynomial up to their degree and a summation of polynomial is still a polynomial. Thus, the final result will be $An^{p}+\dots$ for some constant $\mathbf{A}\dots$.

Besides, notice that 

$$
\begin{align}
(n+1)^{p+1}-1&=n^{p+1}+ (p+1)n^{p}+\dots n \\
\end{align}
$$
Notice that when we divide it by $p+1$, the leading term is $\frac{n^{p+1}}{p+1}$ while other term will be combined into the polynomial. Thus, 

$$
\sum_{k=1}^{n} k^{p}= \frac{n^{p+1}}{p+1}+A'n^{p}+\dots
$$
Thus $P(p+1)$ is true, and by mathematical induction $P(p)$ is true for all $p\in \mathbb{N}$. $\blacksquare$ 


> [!remark]
> Notice that this theorem reveals: for large $n$, the sum of $p-th$ power is dominated entirely by its leading term:
> 
> $$
> \sum_{k=1}^{n} k^{p}\approx \frac{n^{p+1}}{p+1}
> $$
> which is the discrete origin of the fundamental calculus rule:
> 
> $$
> \int t^{p}dt= \frac{t^{p+1}}{p+1}
> $$


8) Prove that every natural number is either even or odd.

We prove by mathematical induction. Let $P(n)$ be the statement: $n =2k+1$ or $n =2k$ but not both for some $k\in \mathbb{Z}$.
For basis step, $P(1)$ is true, because $1=2(0)+1$.

For induction step, suppose $n$ is an arbitrary natural number and $P(n)$ is true. Thus,

Case 1: $n =2k$ for some $k\in \mathbb{Z}$.
Thus, $n+1=2k+1$.

Case 2: $n =2k+1$ for some $k\in \mathbb{Z}$
Thus, $n+1=2k+2=2(k+1)=2m$ where $m=k+1\in \mathbb{Z}$.

For the sake of contradiction, suppose $n+1=2k=2j+1$ for some $k,j\in \mathbb{Z}$. Thus,

$$
\begin{align}
2k&=2j+1 \\
2k-2j&=1 \\
2(k-j)&=1 \\
k-j&=\frac{1}{2}
\end{align}
$$
Notice that $k-j\not\in{Z}$ which contradict the fact.

Thus, $P(n+1)$ is true, by mathematical induction it follow that $P(n)$ is true for $n\in \mathbb{N}$. $\blacksquare$

> [!question]
> Prove $\mathbb{N}$ is closed under addition (Hint: Define a set $m\in \mathbb{N}$ such that $m+n\in \mathbb{N}$) 
> Prove $\mathbb{Z}$ is closed under addition, subtraction and multiplication
> 


9) Prove that if a set $A$ of natural numbers contains $n_{0}$ and contains $k+1$ whenever it contains $k$, then $A$ contains all natural numbers$\geq n_{0}$ (Shifted mathematical induction)

Proof:
If a set $B$ of natural numbers contains 1 and $m\in B\implies m+1\in B$. Then, $B=\mathbb{N}$. Lets define a set of natural number $B'$ whereby
$$
B'=\{ m\in \mathbb{N}:n_{0}+m-1\in A \}
$$

Notice that $1\in B'$ because $n_{0}+1-1=n_{0}\in A$. Suppose $m\in B'$, then $n_{0}+m-1\in A$. Let $k=n_{0}+m-1$, thus by our supposition $k+1=n_{0}+m\in A$. Since $n_{0}+m\in A$, it follow that $m+1\in B'$. $B'=\mathbb{N}$.

Suppose $x$ is an arbitrary natural number such that $x\geq n_{0}$.
Let $x=n_{0}+m-1$. Notice that $x=n_{0}+m-1\implies x-n_{0}=m-1$. Since $x-n_{0}\geq 0$, it follow that $m-1\geq 0\implies m\geq 1$. Thus, $m\in B'$. Thus $x=n_{0}+m-1\in A$. 


10) Prove the principle of mathematical induction from the well-ordering principle.
[[Well ordering principle]]

11) Prove the principle of complete induction from the ordinary principle of induction. Hint: If $A$ contains $1$ and $A$ contains $n+1$ whenever it contains $1,\dots,n$ consider the set $B$ of all $k$ such that $1,\dots,k$ are all in $A$. (Prove strong induction using weak induction)
Proof:
Consider the set
$$
B=\{ k\in \mathbb{N}:1,\dots,k\in A \}
$$

$1\in B$ because $1\in A$. Suppose $k\in B$, then $1,2,\dots,k\in A$. Thus, by the induction hypothesis of strong induction, $k+1\in A$. Since $1,\dots,k\in A$ and $k+1\in A$, it follow that $k+1\in B$. Hence, $B=\mathbb{N}$. 

We need to prove $A=\mathbb{N}$. Notice that since $B=\mathbb{N}$, for any $n\in \mathbb{N}$, it follow that $1,\dots,n\in A$. Thus, $A=\mathbb{N}$.

> [!remark]
> Notice that the strong induction is the ordinary induction with extra condition which is the $1,\dots,n$  need to be true. But notice that from the strong induction hypothesis, we already have $n\in A\implies n+1\in A$, but this $n\in A$ need a extra condition where $1,\dots,n\in A$. That's why we define a set on this (and notice that we can prove the set is actually natural number using ordinary induction) 
> 
>  it is like we convert the strong induction problem to a ordinary induction problem (prove $k\in B\implies k+1\in B$)

12) a) If $a$ is a rational and $b$ is irrational, is $a+b$ necessarily irrational? What if $a$ and $b$ are both irrational?

Proof:
Suppose for the sake of contradiction $a+b$ is rational. Thus,

$$
a+b= \frac{p}{q}
$$
for $p,q\in \mathbb{Z}$. Thus

$$
\begin{align}
b= \frac{p}{q}-a
\end{align}
$$
Since $a\in \mathbb{Q}$, it follow that $a= \frac{m}{n}$ for some $m,n\in \mathbb{Z}$. Thus,

$$
b= \frac{pn-mq}{nq}
$$
It is clear that $pn-mq\in \mathbb{Z}$ and $nq\in \mathbb{Z}$. Thus, $b\in \mathbb{Q}$ which contradict out supposition.

> [!remark]
> We also prove that rational number is closed under addition and subtraction

 What if $a$ and $b$ are both irrational?
 Considering $\sqrt{ 2 }$ and $-\sqrt{ 2 }$. Notice that $\sqrt{ 2 }+(-\sqrt{ 2 })=0\in \mathbb{Q}$.

b) If $a$ is rational and $b$ is irrational, is $ab$ necessarily irrational? 

No for example $0\cdot \sqrt{ 2 }=0$

> [!remark]
> Even though both are irrational, the product is not necessary to be irrational. For example $\sqrt{ 2 }\cdot \sqrt{ 2 }=2$ 
> 

c)Is there a number $a$ such that $a^{2}$ is irrational, but $a^{4}$ is rational?

$\sqrt[4]{ 2 }\cdot \sqrt[4]{ 2 }= \sqrt[4]{ 4 } \not\in \mathbb{Q}$ but $(\sqrt[4]{ 2 })^{4}=2\in \mathbb{Q}$

d) Are there two irrational numbers whose sum and product are both rational?

$\sqrt{ 2 }$ and $-\sqrt{ 2 }$

13) Prove that $\sqrt{ 3 },\sqrt{ 5 },$ and $\sqrt{ 6 }$ are irrational. Hint: To treat $\sqrt{ 3 }$ for example, use the fact that every integer is of the form $3n$ or $3n+1$ or $3n+2$. Why doesn't this proof work for $\sqrt{ 4 }$?


Proof:
Suppose for the sake of contradiction. $\sqrt{ 3 }$ is rational. Thus,

$$
\sqrt{ 3 }= \frac{p}{q}
$$
for some $p,q\in \mathbb{Z}$. Hence,

$$
\begin{align}
3&= \frac{p^{2}}{q^{2}} \\
3q^{2}&=p^{2}
\end{align}
$$
Thus, by Euclid lemma $3|p$. Thus, $p=3n$ for some $n\in \mathbb{Z}$. Thus,

$$
\begin{align}
3q^{2}&=(3n)^{2} \\
3q^{2}&= 9n^{2} \\
q^{2}&=3n^{2}
\end{align}
$$

Notice that by Euclid lemma, $3|q$ , Thus, $p$ and $q$ have same common factor 3 which contradict our supposition that it is the simplest form. $\blacksquare$ (We can use the generalize Euclid lemma to prove that $\sqrt[n]{ p } \not\in \mathbb{Q}$) 


Since the Spivak don't want us to use Euclid lemma, then we prove the special case of Euclid lemma: $3|m^{2}\implies 3|m$. (The converse is trivial)

Proof: Suppose $3\nmid m$, thus By QR Theorem, there are 2 cases.

Case 1: $m=3n+1$ for some $n\in \mathbb{Z}$
Then,
$$
\begin{align}
m^{2}&=(3n+1)^{2} \\
&=9n^{2}+6n+1 \\
&=3(3n^{2}+2n)+1
\end{align}
$$

Thus, $3 \nmid m^{2}$.

Case 2: $m=3n+2$ for some $n\in \mathbb{Z}$.
Then,

$$
\begin{align}
m^{2}&=(3n+2)^{2} \\
&= 9n^{2}+12n+4 \\
&=3(3n^{2}+4n+1)+1
\end{align}
$$

Thus, $3 \nmid m^{2}$. $\blacksquare$

> [!question]
> Why it didn't work for $\sqrt{ 4 }$?
> It is because $4$ is not the prime number.

14) Prove that
a) $\sqrt{ 2 }+\sqrt{ 6 }$ is irrational

Suppose for the sake of contradiction $\sqrt{ 2}+\sqrt{ 6 }\in \mathbb{Q}$. Thus,
Let
$$
\begin{align}
\sqrt{ 2 }+\sqrt{ 6 }&= r
\end{align}
$$
for some $r\in \mathbb{Q}$. Thus, we square both side 

$$
\begin{align}
2+2\sqrt{ 12 }+6&=r^{2} \\
2\sqrt{ 12 }&=r^{2}-8 \\
4\sqrt{ 3 }&=r^{2}-8 \\
\sqrt{ 3 }&= \frac{r^{2}-8}{4}
\end{align}
$$

Notice that $\frac{r^{2}-8}{4}\in \mathbb{Q}$. Thus $\sqrt{ 3 }\in \mathbb{Q}$ which contradict the fact.

15)
a) Prove that if $x=p+\sqrt{ q }$ where $p$ and $q$ are rational, and $m$ is natural number, then $x^{m}=a+b\sqrt{ q }$ for some rational $a$ and $b$. (This is the generalize version of the technique we use in question 14)

Proof:
$$
\begin{align}
x^{m} &=\sum_{k=0}^{m}\binom{m}{k}p^{m-k}(\sqrt{ q })^{k} \\
&=p^{m}+ m p^{m-1}\sqrt{ q }+\binom{m}{2}p^{m-2}q+\dots+(\sqrt{ q })^{m}
\end{align}
$$

Notice that
When $k$ is even, then $(\sqrt{ q })^{k}=q^{k/2}\in \mathbb{Q}$
When $k$ is odd, then $(\sqrt{ q })^{k}=q^{(k-1)/2}\sqrt{ q }$. For example $(\sqrt{ q })^{3}=\sqrt{ q }\sqrt{ q }\sqrt{ q }=q\sqrt{ q }$.  Notice that $q^{(k-1)/2}\in \mathbb{Q}$

> [!remark]
> Rational number is closed under addition and multiplication but this is not the case for irrational 

Thus,
$$
\begin{align}
x^{m}&=\sum_{\text{k is even}} \binom{m}{k}p^{m-k}q^{k/2}+ \sqrt{ q }\sum_{\text{k is odd}} \binom{m}{k}p^{m-k}q^{(k-1)/2}  
\end{align}
$$

Since $p,q\in \mathbb{Q}$, and rational number is closed under addition and multiplication, it follow that the both summation are rational number. Let $a= \sum_{\text{k is even}}\binom{m}{k}p^{m-k}q^{k/2}$ and $b=\sum_{\text{k is odd}} \binom{m}{k}p^{m-k}q^{(k-1)/2}$. Thus, the statement is true. $\blacksquare$

b) Prove also that $(p-\sqrt{ q })^{m}=a-b\sqrt{ q }$

Notice that $(p-\sqrt{ q })^{m}=(p+(-\sqrt{ q }))^{m}$, By (a) it follow that

$$
\begin{align}
(p+(-\sqrt{ q }))^{m}&= a+b(-\sqrt{ q }) \\
&=a-b\sqrt{ q }
\end{align}
$$
But we need to prove they have the same $a$ and $b$.

$$
\begin{align}
(p+(-\sqrt{ q }))^{m}=\sum_{k=1}^{m}\binom{m}{k}p^{m-k}(-\sqrt{ q })^{k}  
\end{align}
$$

Notice that when $k$ is even, $(-\sqrt{ q })^{k}=(-1)^{k}q^{k/2}=q^{k/2}$. So $a$ is the same.

when $k$ is odd, $(-\sqrt{ q })^{k}=(-1)^{k}q^{(k-1)/2}\sqrt{ q }=-q^{(k-1)/2}\sqrt{ q }$. Hence it is $-b$. $\blacksquare$

16)
a)
Proof:
Notice that
$$
\begin{align}
\frac{(m+2n)^{2}}{(m+n)^{2}}-2&= \frac{(m+2n)^{2}-2(m+n)^{2}}{(m+n)^{2}} \\
&= \frac{m^{2}+4mn+4n^{2}-2m^{2}-4mn-2n^{2}}{(m+n)^{2}} \\
&= \frac{-m^{2}+2n^{2}}{(m+n)^{2}} \\
&= \frac{2n^{2}-m^{2}}{(m+n)^{2}}
\end{align}
$$

Since $\frac{m^{2}}{n^{2}}<2\implies m^{2}<2n^{2}$. Thus, $2n^{2}-m^{2}> 0$. Since $(m+n)^{2}> 0$, it follow that 

$$
\frac{(m+2n)^{2}}{(m+n)^{2}}-2= \frac{2n^{2}-m^{2}}{(m+n)^{2}}> 0
$$
$\blacksquare$

Proof for second inequality:

$$
\begin{align}
\frac{(m+2n)^{2}}{(m+n)^{2}}-2&= \frac{2n^{2}-m^{2}}{(m+n)^{2}} 
\end{align}
$$

$$
\begin{align}
2-\frac{m^{2}}{n^{2}}&= \frac{2n^{2}-m^{2}}{n^{2}}
\end{align}
$$

Since $m,n\in \mathbb{N}$, it follow that $m>0\implies m+n>n \implies (m+n)^{2}>n^{2}$ since $m+n>0$ and $n>0$. Thus, it follow that $\frac{1}{(m+n)^{2}}< \frac{1}{n^{2}}$. Hence,

$$
\begin{align}
\frac{(m+2n)^{2}}{(m+n)^{2}}-2= \frac{2n^{2}-m^{2}}{(m+n)^{2}}< \frac{2n^{2}-m^{2}}{n^{2}}= 2- \frac{m^{2}}{n^{2}} &&\blacksquare
\end{align}
$$


b) It is identical as (a). We want to prove

$\frac{m^{2}}{n^{2}}>2\implies \frac{(m+2n)^{2}}{(m+n)^{2}}<2$ and 

$$
2-\frac{(m+2n)^{2}}{(m+n)^{2}}< \frac{m^{2}}{n^{2}}-2
$$

> [!remark] Remark 16(a) and (b):
> Question 16 impose a mechanism where 
> Part (a): if we start below $2$, the next fraction is guaranteed to jump above 2
> Part (b): If we start above $2$, the next fraction is guaranteed to bounce back below 2.
> 
> The Shrinking Error Rule:
> Part (a) show:
> $$
> \begin{align}
> \frac{(m+2n)^{2}}{(m+n)^{2}}-2&<2- \frac{m^{2}}{n^{2}} \\
> \text{New error}&< \text{Old error}
> \end{align}
> $$
> It is something like when you approach to 2 from left side, the next fraction will approach to 2 from right side, and again when we approach to 2 from right side then the next fraction approach to 2 from left side. (and the error inequality make sure that the last fraction is more near than 2 from left side, $2-x_{3}<2-x_{1}\implies x^{3}>x_{1}$)

c) Prove that if $\frac{m}{n}<\sqrt{ 2 }$, then there is another rational number $\frac{m'}{n'}$ with $\frac{m}{n}< \frac{m'}{n'}<\sqrt{ 2 }$

Proof:
Suppose $\frac{m}{n}<\sqrt{ 2 }$. Since $\frac{m}{n}>0$ and $\sqrt{ 2 }>0$, it follow that $\frac{m^{2}}{n^{2}}<2$. Thus, by part (a), it follow that 

$$
\begin{align}
\frac{(m+2n)^{2}}{(m+n)^{2}}&>2 \\

\end{align}
$$

It follow that from part (b) first inequality (It is a chain reaction),

$$
\begin{align}
\frac{(m+2n+2(m+n))^{2}}{(m+2n+m+n)^{2}}&<2 \\
\frac{(3m+4n)^{2}}{(2m+3n)^{2}}&<2 \\
\frac{3m+4n}{2m+3n}&< \sqrt{ 2 }
\end{align}
$$


To prove $\frac{m}{n}< \frac{m'}{n'}< \sqrt{ 2 }$. We need 2 inequality (error inequality)

Part (b) error inequality:
$$
\sqrt{ 2 }-\frac{3m+4n}{2m+3n}< \frac{(m+2n)}{(m+n)}- \sqrt{ 2 }
$$

Part (a) error inequality:
$$
\begin{align}
\frac{(m+2n)}{(m+n)}- \sqrt{ 2 }&< \frac{m}{n}- \sqrt{ 2 } \\
\sqrt{ 2 }- \frac{m+2n}{m+n}&< \sqrt{ 2 }- \frac{m}{n}
\end{align}
$$
Thus, combine together

$$
\begin{align}
\sqrt{ 2 }- \frac{3m+4n}{2m+3n}&< \sqrt{ 2 }- \frac{m}{n} \\
\frac{3m+4n}{2m+3n}&> \frac{m}{n}
\end{align}
$$

Thus, $\frac{m}{n}< \frac{3m+4n}{2m+3n}< \sqrt{ 2 }$. $\blacksquare$

> [!question]
> Why Spivak don't want to let us prove the without square version?
> 
> The foundational reason:
> The existence of $\sqrt{ 2 }$ cannot be proved at this stage. If we want to state problem 16(c) with 100% mathematical honesty, we should use the square version.
> 
> The Algebraic Miracle (The Cross Terms Disappear):
> Notice that $(m+2n)^{2}-2(m+n)^{2}=(m^{2}+4mn+4n^{2})-(2m^{2}+2mn+n^{2})=2n^{2}-m^{2}$


> [!question]
> Where did the $\frac{m+2n}{m+n}$ comes from?
> It is the famous Continued Fraction of $\sqrt{ 2 }$. We want a number $x$ such that $x^{2}=2$. Thus
> 
> $$
> \begin{align}
> x^{2}-1&=1 \\
> (x-1)(x+1)&=1 \\
> x-1&= \frac{1}{x+1} &&\text{Since }x>0 \\
> x&= \frac{x+2}{x+1}
> \end{align}
> $$
> We assume $x=\frac{m}{n}$ for some $m.n\in \mathbb{N}$. Thus, next fraction is $\frac{m+2n}{m+n}$.
> 
> Why we didn't divide $(x-1)$. Lets try
> $$
> \begin{align}
> x+1&= \frac{1}{x-1} \\
> x&= \frac{2-x}{x-1}
> \end{align}
> $$
> 
> Plug in 1.4, $x_{1}=1.5$ . Notice that the new error become big. Why does this happen?
> Notice that $\sqrt{ 2 }\approx 1.4$.
> Case 1: Dive by $x+1$: Thus $1.4+1=2.4$, hence the denominator is very big and can shrink the error.
> 
> Case 2: Divide by $x-1$: Tus. $1.4-1=0.4$ which magnifies the error.
> 

19）Prove Bernoulli's inequality: If $h>-1$, then
$$
(1+h)^{n}\geq 1+nh
$$
for $n\in \mathbb{N}$.
Why is this trivial if $h>0$?

Proof:
We prove by mathematical induction, suppose $P(n)$ defined as
$$
P(n):h>-1\implies(1+h)^{n}\geq{1}+nh
$$

For basis step, $P(1)$ is true because $(1+h)^{1}=1+h= 1+(1)h$.

For induction step, suppose $n$ is an arbitrary number and $P(n)$ is true, Thus,

$$
\begin{align}
(1+h)^{n}&\geq 1+nh \\
(1+h)^{n}(1+h)&\geq (1+nh) (1+h) &&\text{Since }h>-1\implies h+1>0\\
(1+h)^{n+1}&\geq 1+h+nh+nh^{2} \\
&\geq 1+h(n+1)+nh^{2}
\end{align}
$$

Since $nh^{2}\geq 0$, it follow that $1+(n+1)h+nh^{2}\geq1+(n+1)h$. Thus, by transitivity law

$$
(1+h)^{n+1}\geq 1+(n+1)h
$$
Thus, $P(n+1)$ is true. Hence $P(n)$ is true for all $n\in \mathbb{N}$.$\blacksquare$


Why is this trivial if $h>0$?
By binomial theorem
$$
(1+h)^{n}=1+nh+\dots+h^{n}
$$
Since each term of the summation is equal or greater than 0. It follow that $(1+h)^{n}>1+nh$ 

[[Tutorial 9#^018e17]]

17，18