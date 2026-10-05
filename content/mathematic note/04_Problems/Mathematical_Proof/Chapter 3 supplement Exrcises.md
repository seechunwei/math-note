3.51
Lemma 1
if $3x^{3}$ is even ,then $x$ is even
Proof:

Suppose $x$ is an arbitrary odd integer. Notice that $x^{3}=x^{2}\cdot x$. Since $x^{2}$ is a product of two odd integer, it follow that $x^{2}$ is odd integer. Thus, it follow that $x^{3}$ is odd because it is a product of 2 odd integer. Thus, by definition $x^{3}=2k+1$ 

$$
\begin{align}
3x^{3}&=3(2k+1) \\
&=6k+3 \\
&=2(3k+1)+1
\end{align}
$$
Since $3k+1$ is integer, it follow that $3x^{3}$ is odd.

Lemma 2
if $5x^{2}$ is even, then $x$ is even.

Proof: 
Suppose $x$ is an arbitrary odd integer. Thus, $x^{2}$ is odd because it is a product of two odd integers. Thus, by definition it follow that $x^{2}=2k+1$ for some integer $k$. Thus,

$$
\begin{align}
5x^{2}&=5(2k+1) \\
&=10k+5 \\
&=2(5k+2)+1
\end{align}
$$
Since, $5k+2$ is integer, it follow that $5x^{2}$ is odd.

Prove that $3x^{3}$ is even if and only if $5x^{2}$ is even.

Proof:
Suppose $x$ is an arbitrary integer such that $3x^{2}$ is even. Thus, by lemma above $x$ is even. 
Thus, $x^{2}$ is even because it is a product of even integers. By definition, $x^{2}=2k$ for some integer $k$. Thus,

$$
\begin{align}
5x^{2}&=5(2k) \\
&=2(5k)
\end{align}
$$
Since $5k$ is integer, it follow that $5x^{2}$ is even.

Conversely, suppose $x$ is an arbitrary integer such that $5x^{2}$ is even. By lemma above $x$ is even. Thus, it follow that $x^{3}$ is even. Therefore, $x^{3}=2k$ for some integer $k$.

$$
\begin{align}
3x^{3}&=3(2k) \\
&=2(3k)
\end{align}
$$
Since $3k$ is an integer, it follow that $3x^{3}$ is even.


3.55
Proof:
Suppose $x$ and $y$ are arbitrary integer such as $x$ is odd or $y$ is even.

Case 1: $x$ is odd
Thus, $x+1$ is even. It follow that $(x+1)y^{2}$ is even because $(x+1)$ is even. 

Case 2: $y$ is even 
Thus, $y^{2}$ is even. It follow that $(x+1)y^{2}$ is even because $y^{2}$ is even.

Conversely
Suppose $x$ and $y$ are arbitrary integer such that $x$ is even and $y$ is odd
Thus, $x+1$ is odd and $y^{2}$ is odd. Thus, $(x+1)y^{2}$ is odd.

==Remark==
Notice that $x$ is odd or $y$ is even cannot generalize to they have same parity because in this case $x$ and $y$ cannot exchange.

3.56
Proof:
Suppose $x$ and $y$ are arbitrary integer such that $x$ is odd or $y$ is odd. We need to show that if $x$ is odd or $y$ is odd, then $xy$ is odd or $x+y$ is odd.

WLOG
Case 1: $x$ is even and $y$ is odd
By definition $x=2k$ and $y=2s+1$ for some integer $k,s$. Thus,
$$
\begin{align}
xy&=2k(2s+1) \\
&=2(2ks+k)
\end{align}
$$

Since $2ks+k$ is an integer, it follow that $xy$ is even.

$$
\begin{align}
x+y&=2k+2s+1 \\
&=2(k+2)+1
\end{align}
$$
Since $k+2$ is an integer, it follow that $x+y$ is odd.


Case 2: $x$ is odd and $y$ is odd
By definition $x=2k+1$ and $y=2s+1$ for some integer $k,s$. Thus,

$xy$ is odd and $x+y$ is even.


In either case $xy$ is odd or $x+y$ is odd.
==Remark== 
Notice that we can use contradiction to prove once we prove $xy$ is odd or $x+y$ is odd we can stop.

3.59
Suppose $a$ and $b$ are arbitrary two distinct real number.

Case 1 $a> b$
$$
\begin{align}
a+b&> 2b \\
\frac{a+b}{2}&> b
\end{align}
$$

Case 2: $b>a$

$$
\begin{align}
b+a> 2a \\
\frac{b+a}{2}>a
\end{align}
$$
Thus, it is either $\frac{a+b}{2}>a$ or $\frac{a+b}{2}>b$ or we can say In both cases, we find that $\frac{a+b}{2} > \min(a,b)$.


3.62
Proof:
%%We argue by contradiction.
Suppose x is an arbitrary in $S$ such that at least one pair of integers of $S$ are of the different parity. Suppose $S=\{ a,b,c,d \}$ which $a$ and $b,c,d$ have different parity.

Case 1: $x=a$
Subcase 1.1: $a$ is even and $b,c,d$ are odd
WLOG, let $t=b+c$ and $t$ is even because it is a sum of 2 odd integers. 
Thus, $a$ and $t$ have different parity.

Notice that $t+d$ is odd because it is a sum of odd and even integers.
Thus, $a$ and $b$ have different parity 

Thus it contradict our supposition either (1) for each $x \in S$, the integer x and the sum of any two of the remaining three integers of S are of the same parity or (2) for each $x \in S$, the integer x and the sum of any two of the remaining three integers of S are of opposite parity


Case 2: $x \in \{ b,c,d \}$
WLOG let $x=b$. Thus,%%

This problem can be elegantly solved by analyzing the parity (evenness or oddness) of the sums using modular arithmetic (modulo 2).

Let the set be $S = \{a, b, c, d\}$.

We define parity as $x \pmod 2$.

- If $x \equiv 0 \pmod 2$, $x$ is even.
    
- If $x \equiv 1 \pmod 2$, $x$ is odd.
    

We will prove that in Case 1, all integers must be **even**, and in Case 2, all integers must be **odd**. In both scenarios, all elements of $S$ share the same parity.

---

### **Case 1: The integer $x$ and the sum of remaining pairs have the SAME parity**

1. Analyze a specific element (e.g., $a$):

The problem states that for a fixed $x=a$, the sum of any two of the remaining integers $\{b, c, d\}$ has the same parity as $a$.

This gives us three congruences:

$$\begin{align} a &\equiv b + c \pmod 2 \\ a &\equiv c + d \pmod 2 \\ a &\equiv b + d \pmod 2 \end{align}$$

2. Deduce the relationship between $b, c,$ and $d$:

From the first two equations, since both sums are congruent to $a$:

$$b + c \equiv c + d \pmod 2 \implies b \equiv d \pmod 2$$

From the last two equations:

$$c + d \equiv b + d \pmod 2 \implies c \equiv b \pmod 2$$

Thus, the remaining three integers must have the same parity:

$$b \equiv c \equiv d \pmod 2$$

3. Determine the parity of $a$:

Substitute $b \equiv c$ back into the first equation ($a \equiv b+c$):

$$a \equiv b + b \equiv 2b \equiv 0 \pmod 2$$

Since $a \equiv 0$, $a$ must be even.

4. Generalize:

Since $a$ was chosen arbitrarily, this logic applies to every element in $S$.

- Choosing $b$ as the focus proves $b$ is even.
    
- Choosing $c$ as the focus proves $c$ is even.
    
- Choosing $d$ as the focus proves $d$ is even.
    

**Conclusion for Case 1:** All elements of $S$ are **even**.

---

### **Case 2: The integer $x$ and the sum of remaining pairs have OPPOSITE parity**

1. Analyze a specific element (e.g., $a$):

The problem states that for $x=a$, the sum of any pair from $\{b, c, d\}$ has the opposite parity of $a$.

In modular arithmetic, "opposite parity" means not equal ($\not\equiv$), or equivalent to adding 1.

$$\begin{align} a &\not\equiv b + c \pmod 2 \\ a &\not\equiv c + d \pmod 2 \\ a &\not\equiv b + d \pmod 2 \end{align}$$

2. Deduce the relationship between $b, c,$ and $d$:

Since all three sums ($b+c, c+d, b+d$) are congruent to the same value ($a+1$), they are congruent to each other:

$$b + c \equiv c + d \pmod 2 \implies b \equiv d \pmod 2$$

$$c + d \equiv b + d \pmod 2 \implies c \equiv b \pmod 2$$

Just like in Case 1, the remaining three integers must have the same parity:

$$b \equiv c \equiv d \pmod 2$$

3. Determine the parity of $a$:

Substitute $b \equiv c$ into the condition $a \not\equiv b+c$:

$$a \not\equiv b + b \pmod 2$$

$$a \not\equiv 2b \pmod 2$$

$$a \not\equiv 0 \pmod 2$$

Since $a$ is not congruent to 0, $a$ must be odd.

4. Generalize:

Since $a$ was arbitrary, we repeat the logic for every element:

- Applying to $b$ proves $b$ is odd.
    
- Applying to $c$ proves $c$ is odd.
    
- Applying to $d$ proves $d$ is odd.
    

**Conclusion for Case 2:** All elements of $S$ are **odd**.

---

### **Final Proof Statement**

We have shown that:

1. If Condition (1) holds, all integers in $S$ are **even**.
    
2. If Condition (2) holds, all integers in $S$ are **odd**.
    

Therefore, under either condition, every pair of integers in $S$ has the same parity. $\square$ ^ama

3.63
Proof:
Suppose $a$ and $b$ are arbitrary positive integer. We need to show that $a^{2}b+a^{2}+ab^{2}+b^{2}-4ab\geq 0$
$$
\begin{align}
a^{2}b+a^{2}+ab^{2}+b^{2}&=(a^{2}b+ab^{2})+(a^{2}+b^{2}) \\
\end{align}
$$

Notice that
$$
\begin{align}
a^{2}+b^{2}&=(a-b)^{2}+2ab \\
\end{align}
$$
Since $(a-b)^{2}\geq 0$. It follow that $a^{2}+b^{2}\geq2ab$. (Or we can just use AM-GM)

Notice that
$a+b\geq 2$ because $a\geq{1}$ and $b \geq 1$. Thus
$ab(a+b)\geq2ab$

Thus,

$$
\begin{align}
a^{2}+b^{2}=ab(a+b)&\geq 2ab+2ab \\
&\geq 4ab
\end{align}
$$
==Remark==
The key idea of this proof is
$a^{2}+b^{2}=(a-b)^{2}+2ab$

3.64
$a,b \in \mathbb{Z}$. Prove that if $ab=4$, then $(a-b)^{3}-9(a-b)=0$

Proof:
Suppose $a$ and $b$ are arbitrary integer such that $ab=4$

If you prefer algebra, you must factor the _target_ expression first.

$$\begin{align} (a-b)^3 - 9(a-b) &= (a-b)[(a-b)^2 - 9] \\ &= (a-b)(a-b-3)(a-b+3) \end{align}$$

To prove this is zero, you just need to show that for any integer factors of 4, the difference $a-b$ is always either $0$, $3$, or $-3$.
- Factors $2,2 \rightarrow$ diff is $0$.
- Factors $4,1 \rightarrow$ diff is $3$.
- Factors $1,4 \rightarrow$ diff is $-3$.
Since $a-b$ is always one of these three values, one of the brackets is always zero. Thus the whole product is zero.

3.65
Proof:
$c^{2}=a^{2}+b^{2}$

Let $c^{6}=(a^{2}+b^{2})^{3}$

$(a^{2}+b^{2})(a^{4}-a^{2}b^{2}+b^{4})$

$(x+y)(x^{2}-xy+y^{2})$

$x^{3}+3x^{2}y+3xy^{2}+y^{3}$

$a^{6}+3a^{4}b^{2}+3a^{2}b^{4}+b^{6}$

it left $\dfrac{3a^{4}b^{2}+3a^{2}b^{4}}{3}$

$a^{4}b^{2}+a^{2}b^{4}=a^{2}b^{2}(a^{2}+b^{2})$

$=a^{2}b^{2}c^{2}$

3.67

3.70
Proof:
Suppose $a$ and $b$ are arbitrary positive integer.

$$
\begin{align}
(a+b)\left( \frac{a+b}{ab} \right)&=\frac{(a+b)^{2}}{ab} \\
&=\frac{a^{2}+2ab+b^{2}}{ab} \\
&=\frac{a^{2}+b^{2}}{ab}+2
\end{align}
$$

Notice that 
$$
\begin{align}
\frac{a^{2}+b^{2}}{2}&\geq ab \\
a^{2}+b^{2}&\geq2ab
\end{align}
$$
Thus,
$$
\begin{align}
(a+b)\left( \frac{a+b}{an} \right)&\geq \frac{2ab}{ab}+2 \\
&\geq 4
\end{align}
$$

3.71
Let $x \in \mathbb{Z}$. Prove $3x-2$ and $5x-1$ have different parity.

To prove this statement we suppose 2 cases
1) $3x-2$ is even
2) $3x-2$ is odd
And we prove a lemma to find out the parity of $x$.

Notice that this can be done by proving a biconditional statement
$3x-2$ is even iff $x$ is even 
1) If $3x-2$ is even, then $x$ is even 
We prove by contrapositive
2) If $x$ is even, $3x-2$ is even

