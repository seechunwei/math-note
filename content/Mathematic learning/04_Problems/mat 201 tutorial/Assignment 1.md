1) Prove by induction that lim ${ \frac { e ^ { x } } { x ^ { n } } } = \infty$ for every positive integer n. Use L’Hospital’s x→∞ Rule to assist your induction. 
(This shows that the exponential function grows faster than $x ^ { n }$ for any positive integer n.) 

Proof:
We prove by mathematical induction. Let $P(n)$ be the property below:
$$
P(n): \lim_{ x \to \infty } \frac{e^{x}}{x^{n}}=\infty
$$

 For basis step, suppose $n =1$. Consider the limit below
$$
\begin{align}
\lim_{ x \to \infty } \frac{e^{x}}{x^{1}}
\end{align}
$$

Notice that $\lim_{ x \to \infty }e^{x}=\infty$ and $\lim_{ x \to \infty }x=\infty$. Thus, it is an indeterminate form of type $\frac{\infty}{\infty}$. Thus, by L'Hospital's Rule

$$
\begin{align}
\lim_{ x \to \infty } \frac{e^{x}}{x}&= \lim_{ x \to \infty } e^{x} \\
&= \infty
\end{align}
$$
Hence, $P(1)$ is true.

For induction step, suppose $n$ is arbitrary positive integer and $P(n)$ is true. Thus, consider the limit below

$$
\begin{align}
\lim_{ x \to \infty  } \frac{e^{x}}{x^{n+1}} 
\end{align}
$$
Notice that $\lim_{ x \to \infty }e^{x}=\infty$ and $\lim_{ x \to \infty } x^{n+1}=\infty$. It is an indeterminate form of type $\frac{\infty}{\infty}$. Thus, by L'Hospital's Rule, it follow that

$$
\begin{align}
\lim_{ x \to \infty } \frac{e^{x}}{x^{n+1}}&= \lim_{ x \to \infty } \frac{e^{x}}{n+1(x^{n})} \\
&= \frac{1}{n+1}\cdot\lim_{ x \to \infty }  \frac{e^{x}}{x^{n}} \\
\end{align}
$$

By induction hypothesis, it follow that $\lim_{ x \to \infty } \frac{e^{x}}{x^{n}}=\infty$, and since $\frac{1}{n+1}>0$, it follow that
$$
\begin{align}
\frac{1}{n+1}\cdot \lim_{ x \to \infty }  \frac{e^{x}}{x^{n}}=\infty
\end{align}
$$

Therefore,
$$
\begin{align}
\lim_{ x \to \infty } \frac{e^{x}}{x^{n+1}}&=\frac{1}{n+1}\cdot\lim_{ x \to \infty }  \frac{e^{x}}{x^{n}}  \\
&=\infty
\end{align}
$$

Thus, $P(n+1)$ is true. By principle of mathematical induction, it follow that $P(n)$ is true for all $n\in \mathbb{Z}^{+}$.$\blacksquare$

2) Consider the sequence $\langle a _ { n } \rangle _ { n = 1 } ^ { \infty }$ defined recursively by 

$$
a _ {1} = \sqrt [ 3 ]{5} \quad \text { and } \quad a _ {n + 1} = \sqrt [ 3 ]{a _ {n}} \text {   for   all   } n \geq 1.
$$

(a) Argue by induction that $a _ { n } > 1$ for all $n \geq 1$ 

Proof:
We prove by mathematical induction. Suppose the sequence $\langle a _ { n } \rangle _ { n = 1 } ^ { \infty }$ defined recursively by 

$$
a _ {1} = \sqrt [ 3 ]{5} \quad \text { and } \quad a _ {n + 1} = \sqrt [ 3 ]{a _ {n}} \text {   for   all   } n \geq 1.
$$

Let $P(n)$ be the property defined as below:
$$
P(n): a_{n}>1
$$

For basis step, $a_{1}=\sqrt[3]{ 5 }= 5^{1/3}$.  Consider the function $f(x)=x^{1/3}$. Notice that
$$
\begin{align}
f'(x)&= \frac{1}{3}x^{-2/3} \\
&=\frac{1}{3 \sqrt[3]{x^{2}  }}
\end{align}
$$
Notice that $x^{2}\geq 0$, thus it follow that $\sqrt[3]{ x^{2} }\geq 0$. Thus, $f'(x)\geq 0$.

Hence, $f(x)$ is a strictly increasing function. By definition it follow that $x_{1}>x_{2}\implies f(x_{1})> f(x_{2})$.
 
Notice that $5>1=1^{3}$. Thus, it follow that 
$$
f(5)>f(1^{3})\implies \sqrt[3]{ 5 }>\sqrt[3]{ 1^{3} }=1
$$

For induction step, suppose $n$ is arbitrary positive integer and $P(n)$ is true. Thus, by definition

$$
\begin{align}
a_{n+1}&= \sqrt[3]{ a_{n} }  \\
\end{align}
$$
By induction hypothesis $a_{n}>1$. Thus, it follow that 
$$
\begin{align}
a_{n}>1\implies \sqrt[3]{ a_{n} }> \sqrt[3]{ 1}=1
\end{align}
$$

Hence, $P(n+1)$ is true. By principle of mathematical induction, it follow that $a_{n}>1$ for all $n\in \mathbb{Z}^{+}$.


(b) Assuming the fact that the sequence $\langle a _ { n } \rangle _ { n = 1 } ^ { \infty }$ is decreasing, deduce that the sequence is convergent. 

Notice that from (a), we know that the sequence $\langle a_{n} \rangle_{n=1}^{\infty}$ is bounded below by $1$ because $a_{n}\geq1$ for all $n\geq 1$. Thus, by The Monotone Convergence Theorem, it follow that it is convergent.

(c) Determine the limit of the sequence $\langle a _ { n } \rangle _ { n = 1 } ^ { \infty }$

From (c) we know that the $\lim_{ n \to \infty }a_{n}$ exist. Let $\lim_{ n \to \infty }a_{n}=L$. Then note that $\lim_{ n \to \infty }a_{n+1}=L$. From the recursive definition, we get
$$
\begin{align}
L&=\lim_{ n \to \infty } a_{n+1} \\
&=\lim_{ n \to \infty } \sqrt[3]{ a_{n} } \\
L&= \sqrt[3]{\lim_{ n \to \infty } a_{n}  } &&\text{By continuity}\\
L&=\sqrt[3]{ L } \\
L^{3}&=L \\
L(L^{2}-1)&=0 \\
L(L-1)(L+1)&=0
\end{align}
$$

Thus, $L=0$ or $L=1$ or $L=-1$. Since $a_{n}>1$ for all $n\geq 1$. Thus, it follow that $L\geq 1$ by Order Limit Theorem, thus the only possibility is $\lim_{ n \to \infty }a_{n}=1$.


3) A subsequence for a sequence $\langle a _ { n } \rangle _ { n = 1 } ^ { \infty }$ is a sequence of the form $\langle a _ { n _ { k } } \rangle _ { k = 1 } ^ { \infty }$ for some positive integers $n _ { 1 } < n _ { 2 } < n _ { 3 } < \cdots$ . For example, if $n _ { k } = 2 ^ { k }$ for all $k \geq 1$ , then we get the subsequence $\langle a _ { 2 } , a _ { 4 } , a _ { 8 } , a _ { 1 6 } , a _ { 3 2 } , . . . \rangle$ 

Suppose $\langle a _ { n } \rangle _ { n = 1 } ^ { \infty }$ is an increasing sequence and suppose $\langle a _ { n _ { k } } \rangle _ { k = 1 } ^ { \infty }$ is a subsequence such that $\operatorname* { l i m } _ { k \to \infty } a _ { n _ { k } } = \infty$ . Prove that $\lim_{ n \to \infty }a_{n}=\infty$. 

We want to trap the interval between the consecutive step $a_{n_{k}}$ and $a_{nk+1}$ 

Proof:
For any integer $n$, there exist a integer $n_{k}$ such that $n_{k}<n$ for some $k\in \mathbb{Z}^{+}$. Since $\langle a_n \rangle_{n=1}^{\infty}$ is an increasing sequence, it follow that
$$
a_{n_{k}}\leq a_{n}
$$
Note that $\lim_{ k \to \infty }a_{n_{k}}=\infty$. By Comparison Theorem, it follow that $\lim_{ n \to \infty }a_{n}=\infty$.

> [!remark] Remark
> Flaw 1:
> here exist a integer $n_{k}$ such that $n_{k}<n$ .
> This sentence is not good because what is the $k$? We need to tie $k$ with $n$ (express $k$ in term of $n$), so that when we push $k$ to $\infty$ , $n$ also approach to $n$.
> 
> To clearly see why it didn't work. Since the $k$ didn't depend on $n$, so for any $n$ i can just choose $k=1$. Then my inequality become $a_{n_{1}}<a_{n}$. Note that $a_{n_{1}}$ is just a constant, so i am basically just prove that it is larger than a constant.
> 
> Flaw 2:
> Define a function $f:\mathbb{Z}^{+}\to \mathbb{R}$ such that 
> $$
> \begin{matrix}
> f(n)=a_{n} &\text{for all }n\in \mathbb{Z}^{+}
> \end{matrix}
> $$
> Since $\langle a_n \rangle_{n=1}^{\infty}$ is an increasing sequence it follow that $f(n)$ is also an increasing function
> 
> This is redundant because $\langle a_n \rangle_{n=1}^{\infty}$ itself is a function in domain $\mathbb{Z}^{+}$. No need to write again as it didn't change anything 

Proof:
*(Note: To avoid confusion between the running index $n$ and the subsequence indices $n_k$, we denote the subsequence indices by $m_k$ instead of $n_k$.)*

Since $m_{1}<m_{2}<m_{3}<\dots$ is a strictly increasing sequence of integers, for any integer $n\geq m_{1}$, we can define: $k(n)=\max\{ j\in \mathbb{Z}^{+} \mid m_{j}\leq n \}$. 

Construct the bounding sequence:
By definition of $k(n)$, we have $m_{k(n)}\leq n$. Since $\langle a_n \rangle_{n=1}^{\infty}$ is an increasing sequence, it follow that
$$
a_{m_{k(n)}}\leq a_{n}
$$

Thus, as $n\to \infty$, the index $n$ eventually surpasses every $m_{j}$. Therefore, $k(n)\to \infty$, which means $\lim_{ n \to \infty }a_{m_{k(n)}}=\lim_{ k \to \infty }a_{m_{k}}=\infty$.

Since $a_{m_{k(n)}}\leq a_{n}$ for all $n\geq m_{1}$ and $\lim_{ n \to \infty }a_{m_{k(n)}}=\infty$, by the Comparison Theorem, it follow that $\lim_{ n \to \infty }a_{n}=\infty$. $\blacksquare$

---
What if we want to prove convergent? 
Proof:
Since $m_{k}<m_{k+1}$. For any integer $n$, it follow that $m_{k}\leq n\leq m_{k+1}$ for some $k\in \mathbb{Z}^{+}$. 
Since $\langle a_n \rangle_{n=1}^{\infty}$ is an increasing sequence, it follow that
$$
a_{m_{k}}\leq a_{n}\leq a_{m_{k+1}}
$$
Note that $\lim_{ k \to \infty }a_{m_{k}}=L$ and $\lim_{ k \to \infty }a_{m_{k+1}}=L$. By Squeeze Theorem, it follow that
$$
\lim_{ n \to \infty } a_{n}=L
$$




Note: For any sequence $\langle a _ { n } \rangle _ { n = 1 } ^ { \infty } .$ , we write lim $a _ { n } = \infty$ if for every number $M > 0$ , there exists n→∞ an integer N such that $a _ { n } > M$ whenever $n > N$ . This problem would provide the required justification in the proof that the harmonic series is divergent in Lecture 9. Furthermore, it is worth pointing out that if a sequence is convergent, then all its subsequences also converge to the same limit. 


 



Remark for q2:
By contrapositive, it follow that $f(x_{1})\leq f(x_{2})\implies x_{1}\leq x_{2}$. Notice that by the definition of function $x_{1}=x_{2}\implies f(x_{1})=f(x_{2})$.

Thus, combine both direction, it follow that

$$
a\geq b \iff f(a)\geq f(b)
$$


$$
\begin{align}
(1+4)^{1/3}&= \left[ 4\left( 1+\frac{1}{4} \right) \right]^{1/3} \\
&= \sqrt[3]{ 4 }\left( 1+ \frac{1}{4} \right)^{1/3}
\end{align}
$$
We can also use function $f(x)=x^{3}$ 