3.26
Proof:
Suppose $n$ is arbitrary integer.

Case 1: $n$ is even
By definition $n =2k$ for some integer $k$. Thus,
$$
\begin{align}
(2k)^{2}-3(2k)+9&=4k^{2}-6k+9 \\
&=2(2k^{2}-3k+4)+1
\end{align}
$$

Since $2k^{2}-3k+4$ is integer, it follow that $n^{2}-3n+9$.


Case 2: $n$ is odd
By definition $n =2k+1$ for some integer $k$. Thus,
$$
\begin{align}
n^{2}-3n+9&=(2k+1)^{2}-3(2k+1)+9 \\
&=4k^{2}+4k+1-6k-3+9 \\
&=4k^{2}-2k+7 \\
&=2(2k^{2}-k+3)+1
\end{align}
$$
Since $2k^{2}-k+3$ is integer, it follow that $n^{2}-3n+9$ is odd.

In either case $n^{2}-3n+9$ is odd, thus the statement is true.

3.31
Proof:
Suppose $a,b$ are arbitrary integer.  WLOG

Case 1: $a$ is odd and b is even
Thus, $a+b$ is odd and $ab$ is even

Case 2: $a,b$ are odd
$a+b$ is even and $ab$ is odd

Thus in either case $a+b$ and $ab$ have different parity.

How to understand it intuitively?
if $ab$ is odd then $a,b$ must be odd
Thus, $a+b$ is even 

if $ab$ is even then one of them must be even 
Thus, $a+b$ is even when $a,b$ is even.

3.33
Proof:
If $2n^{2}-5n$ is (positive and even) or (negative and odd) then $n \not\in A\cap B$

Suppose $n \in A\cap B$, thus $n \in \{ 2,3 \}$

Case 1: $n ={2}$
$$
\begin{align}
2n^{2}-5n&=2(2)^{2}-5(2) \\
&=-2
\end{align}
$$
Thus, $2n^{2}-5n$ is negative and even.

Case 2: $n =3$
$$
\begin{align}
2n^{2}-5n&=2(3)^{2}-5(3) \\
&=3
\end{align}
$$
Thus, $2n^{2}-5n$ is positive and odd.

In either case $2n^{2}-5n$ is not (positive and even) or not(negative and odd).

Conversely, suppose $n \not\in A\cap B$. Thus, $n \in \{ 1,4 \}$.


3.35
Proof:
Suppose $n$ is an arbitrary nonnegative integer. 

Case 1: $n =0$
$$
\begin{align}
2^{n}+6^{n}&=2^{0}+6^{0} \\
&=2
\end{align}
$$
Thus, $2^{n}+6^{n}$ is even.


Case 2: $n > 0$
Since $n \ge 1$, $2^n$ is the product of $n$ factors of 2, which makes it even. Similarly, $6^n$ is the product of $n$ factors of 6, which is also even. The sum of two even integers is always even.


Alternative way

$$
\begin{align}
2^{n}+6^{n}&=2^{n}+2^{n}\cdot 3^{n} \\
&=2(2^{n-1}+2^{n-1}\cdot 3^{n})
\end{align}
$$
Since $n> 0$, it follow that $n-1\geq 0$. Since $2^{n-1}+2^{n-1}\cdot 3^{n}$ is integer, it follow that $2^{n}+6^{n}$ is even.

3.36
How we set up a question?
We know that $a+b$ is even when both of them are odd or both of them are even. 

Thus, we set something that make $a+b$ must even to implies that $a,b$ are even?

Let $a,b$ be a product of even and odd like 
$a+b=3x+5y$
or more complicated make it a system of equation
$a+b=3x+4y$ and $a+b=2x+7y$

3.40
Prove by cases not necessarily divide the cases into mutually disjoint cases. In this situation the the collection of cases (or subsets) is call ==cover==

For example 
Let $a,b \in \mathbb{Z}$, if $a$ is even or $b$ is even, then $ab$ is even.
Case 1: $a$ is even
Case 2: $b$ is even 

Notice that 
1) $a$ is even and $b$ is odd
These subcases is belong to case 1 and case 2. Let $(a,b)\in \mathbb{Z}$. Thus, we say that element $(a,b)$ is belong to 2 of the subsets.

Thus, in this case we divide the cases by cover. What if we want to determine cases by partition?

Case 1: One if them is even and another is odd
Case 2: Both of them are even

A collection of a nonempty subsets of a nonempty set S is called a cover of S if every element of S belongs to ==at least one== of the subsets.

If we let true: even and false: odd. Then the addiction of parity is like logically equivalent statement because both $a,b$ must have same parity so that $a+b$ is even (true)

On the other hand , the multiplication of parity is like or statement. If one of them is even ,then the $ab$ is even.

