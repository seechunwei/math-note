1)
a) 
Explanation
Notice that $r$ is real number in the set of $[0,\infty]$ and 
$A_{r}$ is the set of all possible 2-tuple $(x,y)$ which is the cartesian product of $\mathbb{R}$ and $\mathbb{R}$ (It means that $x \in \mathbb{R}$ and $y\in \mathbb{R}$) that satisfy the equation $x^{2}+y^{2}=r^{2}$

Notice that this is a circle in cartesian plane where the $r$ represent the distance from the origin $(0,0)$ to the point $(x,y)$. $r=\sqrt{ x^{2}+y^{2} }$. 

Since _every_ point in the plane belongs to a specific set $A_r$, the union of all these sets covers the entire plane. Therefore, $\bigcup_{r\in I}A_{r} = \mathbb{R}^2$."

Graphically, imagine a circle that spread until infinity from the origin and add these circle together it become the whole cartesian plane

Justification
Suppose an arbitrary 2-tuple $P = (x_0, y_0)$ in the Cartesian plane $\mathbb{R}^2$.

We can calculate the distance of this point from the origin using the formula $d = \sqrt{x_0^2 + y_0^2}$.

Let us choose a radius $r$ exactly equal to this distance ($r = d$). Since $x_0$ and $y_0$ are real numbers, $d$ must be a non-negative real number, which means $r$ is inside our interval $l=[0,\infty )$

Because $x_0^2 + y_0^2 = r^2$, this point $P$ belongs to the set $A_{r}$.

**Conclusion:** Since _every_ point in the plane belongs to a specific set $A_r$, the union of all these sets covers the entire plane. Therefore, $\bigcup_{r\in I}A_{r} = \mathbb{R}^2$."


The second part 

$$
\bigcap_{r\in I}A_{r}
$$
Notice that

$$
A_{i}\cap A_{j}=\emptyset \text{ which } i,j \in I \text{ and }i\neq j
$$
It is because a 2-tuple $(x,y)$ cannot have different distance from origin, thus each 2-tuple satisfy the equation $x^{2}+y^{2}=r^{2}$ for a unique $r$. Thus, the solution is $\emptyset$.

b)
$$
\bigcup_{r\in I} B_{r}
$$
Let $s,j \in I$. Notice that $B_{r}$ is a nested set with property as follow.
$$
B_{s}\subseteq B_{j} \text{ for }0\leq s\leq j
$$
Thus,
$$
B_{s}\cup B_{j}=B_{j} \text{ for } 0\leq s\leq j
$$

Thus,
$$
\bigcup_{r\in I}B_{r}=\lim_{R \to \infty} B_R
$$

Notice that
$$
\begin{align}
B_{j}&= \bigcup_{r\in[0,j]}A_{r} \\
\lim_{R \to \infty} B_R&=\bigcup_{r\in{[0,\infty)}}A_{r} \\
\bigcup_{r\in I}B_{r}&=\mathbb{R}^{2}
\end{align}
$$
Thus, the answer is $\mathbb{R}^{2}$

The second part,
$$
\bigcap_{r\in I}B_{r}=B_{0}
$$
This is because $B_{0}$ is the subset of all the other set.
It means that every element in $B_{0}$ is in $B_{r}$ for $r\in I$. Thus, $B_{0}$ is the only common intersection for all set $B_{r}$ where $r\in I$
$B_{0}=\{ (x,y)\in \mathbb{R}\times \mathbb{R}:x^{2}+y^{2}\leq 0^{2} \}$

Since $x^{2}\geq 0$ and $y^{2}\geq 0$. Thus, the only cases that satisfy this inequality is $x^{2}=0$ and $y^{2}=0$, Thus, $(0,0)$ is the solution.

c)
Notice that thia is a collection of nested set which $Cr_{1}\subseteq Cr_{2}$ iff $r_{1}\geq r_{2}$. Thus, the union of this set is simply the set contain all other subset in this case which is the set of smallest number of $r$.
Thus,

$$
\begin{align}
\bigcup_{r\in I}C_{r}&= C_{0} \\ 
&=\{ (x,y)\in \mathbb{R}\times \mathbb{R}:x^{2}+y^{2}>0 \} \\
&=\mathbb{R}^{2}\setminus \{ (0,0) \}
\end{align}
$$
Why?
$$
C_{0}=\{ (x,y)\in \mathbb{R}\times \mathbb{R}:x^{2}+y^{2}>0 \}
$$
This indicate that the origin is not included in the set.

The second part
%%Notice that thus is a collection of nested set which $Cr_{1}\subseteq Cr_{2}$ iff $r_{1}\geq r_{2}$. Thus, the intersection of this collection of nested set is simply the set that is subset for all other set which is the set with largest $r$. We need to prove that there exist such largest $r$ for $r\in I$.  We assume that $r_{0}$ is the greatest number in the set. Let $r_{1}=r_{0}+1$. Thus, $r_{1}$ is in the set $I$ and $r_{1}>r_{0}$. Thus, it lead to contradiction. Thus, the solution for this question is $\emptyset$.

It is wrong because consider the set $$D_r = \{(x,y) \in \mathbb{R}^2 : x^2 + y^2 \ge 0\}$$
Even though that is no largest r. The intersection is $\mathbb{R}^{2}$

%%



Explaination
Notice that this is a collection of nested set which $Cr_{1}\subseteq Cr_{2}$ iff $r_{1}\geq r_{2}$. Thus, the intersection of this collection of nested set is simply the set that is subset for all other set which is the set as $r\to \infty$.

"Since any specific point $(x,y)$ has a finite distance $d$, it will eventually be excluded from the set $C_r$ once $r > d$. Because this happens for _every_ point, no point remains. Thus, the intersection is empty."


Justification by Contradiction
- **Assumption:** Assume there exists a point $P=(x_0, y_0)$ that is inside the intersection $\bigcap_{r\in I}C_{r}$.
    
- Definition: This means $P$ must belong to $C_r$ for every possible $r \in [0, \infty)$. 
    
    $$x_0^2 + y_0^2 > r^2 \quad \text{for all } r \in [0, \infty)$$
    
- The Flaw: Let $d = \sqrt{x_0^2 + y_0^2}$ be the fixed distance of point $P$ from the origin.
    
    We can simply choose a radius $r_{0}$ that is larger than this distance (e.g., let $r_{0} = d + 1$). By our assumption, $d^{2}>r_{0}^{2}$.
    
- Contradiction:
	It is clear that $r_{0}^{2}\in I$ and $r_{0}> d$ because $d+1>d$. Thus, $r_{0}^{2}\geq d^{2}$ which contradict the assumption that $d^{2}> r_{0}^{2}$.
    
- Conclusion: Therefore, the statement is false which mean that there is no point inside the intersection $\bigcap_{r\in I}C_{r}$. 
    
    $$\therefore \bigcap_{r\in I}C_{r} = \emptyset$$
2)
Mathematical induction
Proof:
We argue by mathematic induction. Let property $P(n)$ defined as follow.
$$
P(n):n^{3}+5n
 \text{ is divisible by 6}$$
For basis step, it is clear that $P(1)$ is true because $(1)^{3}+5(1)=6$ and 6 is divisible by 6.

For induction step, suppose $n$ is arbitrary positive number and suppose $P(n)$ is true. Thus,
$$
\begin{align}
(n+1)^{3}+5(n+1)&=n^{3}+3n^{2}+3n+1+5n+5 \\
&=n^{3}+3n^{2}+8n+6 \\
&=n^{3}+5n+3n^{2}+3n+6
\end{align}
$$
By definition $n^{3}+5n =6k$ for some integer $k$.Thus, by substitution
$$
\begin{align}
(n+1)^{3}+5(n+1)&=6k+3n^{2}+3n+6 \text{ (By Induction Hypothesis )} \\
&=6k+3n(n+1)+6 \\
\end{align}
$$
Note that $n(n+1)$ is the product of two consecutive integers, so it must be even. Thus, by definition $n(n+1) = 2p$ for some integer $p$. Thus,
$$
\begin{align}
(n+1)^{3}+5(n+1)&=6k+3(2p)+6 \\
&=6(k+p+1) 
\end{align}
$$
Therefore, $P(n+1)$ is true. By principle of mathematical induction, $P(n)$ is true for all n with $n \in \mathbb{N}$.

Direct Proof:
Proof:
Suppose $n$ is an arbitrary natural number. 
$$
\begin{align}
n^{3}+5n &=n^{3}-n+6n \\
&=n(n^{2}-1)+6n \\
&=(n-1)(n)(n+1)+6n
\end{align}
$$
Notice that The term $(n-1)n(n+1)$ is the product of three consecutive integers.

In any three consecutive integers, at least one is divisible by 2 and exactly one is divisible by 3. Therefore, their product is divisible by $2 \times 3 = 6$. Thus, by definition, 
$$
(n-1)(n)(n+1)=6k \text{ for some integer k}
$$
Thus, by definition
$$
\begin{align}
n^{3}+5n &=6k+6n \\
&=6(k+n)
\end{align}
$$
Since $(k+n)$ is integer, it follow that $n^{3}+5n$ is divisible by 6. Since $n$ is arbitrary natural number, it follow that the statement is true for all $n$ with $n \in \mathbb{N}$.

Contradiction:
Proof:
We argue by contradiction.

Assume that the statement is false. That is, assume there exists some integer $n$ such that $6 \nmid (n^3 + 5n)2$.

Since $6 = 2 \times 3$, for a number not to be divisible by 6, it must fail to be divisible by 2 or fail to be divisible by 3.

Mathematically, our assumption implies:

$$2 \nmid (n^3 + 5n) \quad \lor \quad 3 \nmid (n^3 + 5n)$$

We will now show that $n^3 + 5n$ is, in fact, always divisible by both 2 and 3, which will lead to a contradiction.

---

Step 1: Check Divisibility by 2

Let us analyze the parity of $n$. There are two cases:

- Case 1a: $n$ is Even 
    
    Let $n = 2k$ for some integer $k$.
    
    Substitute $n$ into the expression:
    
    $$ \begin{aligned} n^3 + 5n &= (2k)^3 + 5(2k) \\ &= 8k^3 + 10k \\ &= 2(4k^3 + 5k) \end{aligned}$$
    
    Since $4k^3 + 5k$ is an integer, the result is divisible by 25.
    
- Case 1b: $n$ is Odd 
    
    Let $n = 2b + 1$ for some integer $b$.
    
    Substitute $n$ into the expression:
    
    $$ \begin{aligned} n^3 + 5n &= (2b+1)^3 + 5(2b+1) \\ &= (8b^3 + 12b^2 + 6b + 1) + (10b + 5) \\ &= 8b^3 + 12b^2 + 16b + 6 \\ &= 2(4b^3 + 6b^2 + 8b + 3) \end{aligned}$$
    
    Since the term in the brackets is an integer, the result is divisible by 27777.
    

**Result:** In all cases, $2 \mid (n^3 + 5n)$.

---

Step 2: Check Divisibility by 3

We check the three possible residues for $n$ modulo 38:

- **Case 2a: $n \equiv 0 \pmod 3$** 9
    
    $$0^3 + 5(0) = 0 \equiv 0 \pmod 3$$
    
- **Case 2b: $n \equiv 1 \pmod 3$** 10
    
    $$1^3 + 5(1) = 1 + 5 = 6 \equiv 0 \pmod 3$$
    
- **Case 2c: $n \equiv 2 \pmod 3$** 11
    
    $$2^3 + 5(2) = 8 + 10 = 18 \equiv 0 \pmod 3$$
    

**Result:** In all cases, $3 \mid (n^3 + 5n)$12.

---

Conclusion

In either case, $3\mid (n^{3}+5n)$ and $2\mid (n^{3}+5n)$. It follow that $6\mid (n^{3}+5n)$ which contradicts the assumption that $6 \not\mid(n^{3}+5n)$. 
%%
We argue by contradiction. Suppose not which is there exists an $n \in \mathbb{N}$ such that $n^{3}+5n$ is not divisible by 6.
Suppose $n$ is an arbitrary natural number. By quotient remainder theorem, there exists a unique integer d and unique integer r such that $n =6d+r$ for $0\leq r<6$.

Case 1: $r=0$
$0^3 + 5(0) = 0 \equiv 0 \text{ (mod 6)}$ 

Case 2: $r=1$
$1^3 + 5(1) = 6 \equiv 0$

Case 3: $r=2$
$2^3 + 5(2) = 8 + 10 = 18 \equiv 0$

Case 4: $r=3$
$3^3 + 5(3) = 27 + 15 = 42 \equiv 0$

Case 5: $r=4$
$4^3 + 5(4) = 64 + 20 = 84 \equiv 0$

Case 6: $r=5$
$5^3 + 5(5) = 125 + 25 = 150 \equiv 0$

Since the cases above exhaust all the possibility, it follow that $n^{3}+5n$ is divisible by 6 for $n \in \mathbb{N}$ which lead to contradiction.
%%
The **Direct Proof** generally provides the best "insight" because it reveals the algebraic structure (consecutive integers) that _causes_ the divisibility. 

Induction confirms the truth but it didn't show why $P(n)$ is true directly.

Contradiction is effectively an exhaustive check here, which is less elegant and it doesn't show any property of $n^{3}+5n$.

3)
Proof:
Let $S = a+b+c \pmod 3$.  
We are proving: $S \equiv 0 \text{ ( mod 3)} \iff (a \equiv b \equiv c) \lor (a \not\equiv b \land b \not\equiv c \land a \not\equiv c)$
Part 1:
We need prove
$$
(a \equiv b \equiv c) \lor (a \not\equiv b \land b \not\equiv c \land a \not\equiv c) \implies S\equiv 0 \text{ (mod 3)}
$$

Assume a, b and c are arbitrary integer and $(a \equiv b \equiv c) \lor (a \not\equiv b \land b \not\equiv c \land a \not\equiv c)$

Case 1: $a\equiv b\equiv c$
Then, the residue for $a,b$ and $c$ are the same. Let $k$ denote the residue of each of it. Thus, 
$a+b+c \equiv 3k \equiv 0 \pmod 3$

Case 2: $(a \not\equiv b \land b \not\equiv c \land a \not\equiv c)$
The only possible residue in Modulo 3 is $\{ 0,1,2 \}$
Thus, since $a,b$ and $c$ have different residue. Thus, the residue of a, b and c must be equal to one of these value in $\{ 0,1,2 \}$ and each of it are distinct. Thus , 

$$a + b + c \equiv 0 + 1 + 2 = 3 \equiv 0 \pmod 3$$
Thus, in either case $a+b+c \equiv 0 \pmod 3$.

Part 2
We need to prove
$$
S \equiv 0 \text{ ( mod 3)} \implies (a \equiv b \equiv c) \lor (a \not\equiv b \land b \not\equiv c \land a \not\equiv c)
$$
We prove by contrapositive.

$$
(a \not\equiv b \not\equiv c)\land(a\equiv b\lor b\equiv c\lor a\equiv c)\implies S\not\equiv 0 \text{ (mod 3)}
$$
This implies that. **Exactly two integers are congruent modulo 3**

**Proof:**

1. Without loss of generality, let us assume $a$ and $b$ are the congruent pair, and $c$ is the different integer.

    $$a \equiv b \equiv k \pmod 3$$
    
    $$c \not\equiv k \pmod 3$$
    
2. Now, examine the sum $S = a + b + c \pmod 3$.
    
    Substitute the known congruences:
    
    $$S \equiv k + k + c \equiv 2k + c \pmod 3$$
    
3. To determine if $S \equiv 0$, let us test the possible values for $c$.
    
    Since $c \not\equiv k$, there are two sub-cases for $c$ relative to $k$:
    
    - Sub-case 1: $c \equiv k + 1 \pmod 3$
        
        $$S \equiv 2k + (k+1) \equiv 3k + 1 \equiv 1 \pmod 3$$
        
        Since $1 \not\equiv 0$, the sum is not divisible by 3.
        
    - Sub-case 2: $c \equiv k + 2 \pmod 3$
        
        $$S \equiv 2k + (k+2) \equiv 3k + 2 \equiv 2 \pmod 3$$
        
        Since $2 \not\equiv 0$, the sum is not divisible by 3.
        
4. **Conclusion:** In all possible scenarios where exactly two integers are congruent, the sum $a+b+c \not\equiv 0 \pmod 3$.



$5\equiv 2 \text{ (mod 3)}$
$5-2\equiv 0 \text{ (mod 3)}$

Noticed that 5 and 2 have same remainder in modulo 3 which is 2.

The question use $a+b$ but not $a-b$ because in modulo 2 $-1 \equiv 1$
$$a - b \equiv a + (-b) \equiv a + (b) \equiv a + b \pmod 2$$
