---
aliases:
---
4.77
$\sqrt{ a^{2} }\sqrt{ b^{2} }=|a|\cdot|b|$. Notice that $|ab|=|a|\cdot|b|$ and $ab\leq|ab|$ it follow that $ab\leq|a|\cdot|b|=\sqrt{ a^{2} }\sqrt{ b^{2} }$

4.78
Proof:
$$
\begin{align}
\frac{a^{2}+b^{2}}{ab}\geq 2 \\
a^{2}+b^{2}\geq 2ab
\end{align}
$$
According to $GM-AM$ inequality, this is true.

4.79
$$
\begin{align}
x^{2}-5x+4= 0 \\
(x-4)(x-1)= 0
\end{align}
$$
$x=4$ or $x=1$

$$
\begin{align}
\sqrt{ 5x^{2}-4 }=1 \\ 
5x^{2}-4=1 \\
5(x^{2}-1)=0 \\
(x+1)(x-1)=0
\end{align}
$$
$x=1$ or $x=-1$

Combining this two condition we can conclude $x=1$. Thus,

$$
\begin{align}
x+ \frac{1}{x}&=1+\frac{1}{1}=2
\end{align}
$$
Q.E.D

4.80
Proof:
Suppose $x \in \mathbb{R}$ and $x< 0$
Case 1:$y\geq 0$
it follow that $x^{3}< 0$ and $-x^{2}y\leq 0$
Thus, $x^{3}-x^{2}y\leq0$ 

$x^{2}y\geq0$ and $-xy^{2}\geq 0$. Thus, $x^{3}-x^{2}y\leq x^{2}y-xy^{2}$

Case 2: $y< 0$
$x^{3}<0$ and $-x^{2}y> 0$
It didn't work so try direct proof.

$$
\begin{align}
x^{2}(x-y)\stackrel{?}{\leq}xy(x-y) \\
x(x-y)(x-y)\stackrel{?}{\leq}0 \\
x(x-y)^{2}\stackrel{?}{\leq}0
\end{align}
$$
Since $x< 0$ and $(x-y)^{2}\geq 0$, it follow that $x(x-y)^{2}\leq 0$. Thus, $x^{3}-x^{2}y\leq x^{2}y-xy^{2}$


4.85
a) if $A\cap B=\emptyset$ , then  $A=(A\cup B)-B$
B) write a conclusion?

4.91
Proof:
$$
\begin{align}
a^{2}<a \\
\sqrt{ a^{2} }<\sqrt{ a } \\
a<\sqrt{ a }
\end{align}
$$

4.94
$n_{1}\equiv n_{2}\equiv n_{3}\equiv 1 \pmod{3}$
Thus, $n_{1}+n_{2}+n_{3}\equiv 0 \pmod{3}$


4.95
Notice that $|x|\equiv x$ Thus,

$$
a-b+a-c+b-c=2a-2c\equiv 0 \pmod{2} 
$$

4.96
$$
\begin{align}
(ac+bd)^{2}&\stackrel{?}{\leq}(a^{2}+b^{2})(c^{2}+d^{2}) \\
(ac)^{2}+2abcd+(bd)^{2}&\stackrel{?}{\leq}(ac)^{2}+(ad)^{2}+(bc)^{2}+(bd)^{2}
\end{align}
$$

Since $(ac)^{2}+(ad)^{2}\geq 2abcd$, thus it is true.

4.102
Here is a clean proof using the AM-GM inequality, which you just explored.

### Method 1: Using AM-GM

**Step 1: Apply AM-GM to the first term**

For the positive numbers $a, b, c$:

$$\frac{a + b + c}{3} \geq \sqrt[3]{abc} \implies (a + b + c) \geq 3\sqrt[3]{abc}$$

**Step 2: Apply AM-GM to the second term**

For the positive numbers $\frac{1}{a}, \frac{1}{b}, \frac{1}{c}$:

$$\frac{\frac{1}{a} + \frac{1}{b} + \frac{1}{c}}{3} \geq \sqrt[3]{\frac{1}{abc}} \implies \left(\frac{1}{a} + \frac{1}{b} + \frac{1}{c}\right) \geq 3\frac{1}{\sqrt[3]{abc}}$$

**Step 3: Multiply the inequalities**

Since all terms are positive, we can multiply the results from Step 1 and Step 2:

$$(a + b + c) \left(\frac{1}{a} + \frac{1}{b} + \frac{1}{c}\right) \geq (3\sqrt[3]{abc}) \cdot \left(3\frac{1}{\sqrt[3]{abc}}\right)$$

**Step 4: Simplify**

The term $\sqrt[3]{abc}$ cancels out:

$$\text{Left Side} \geq 9 \cdot 1$$

$$(a + b + c) \left(\frac{1}{a} + \frac{1}{b} + \frac{1}{c}\right) \geq 9$$


---

### Method 2: Cauchy-Schwarz Inequality (Faster)

If you are familiar with vectors, this is a "one-line" proof using Cauchy-Schwarz: $|\mathbf{u} \cdot \mathbf{v}|^2 \leq \|\mathbf{u}\|^2 \|\mathbf{v}\|^2$.

Let $\mathbf{u} = (\sqrt{a}, \sqrt{b}, \sqrt{c})$ and $\mathbf{v} = (\frac{1}{\sqrt{a}}, \frac{1}{\sqrt{b}}, \frac{1}{\sqrt{c}})$.

1. **Calculate the Dot Product:**
    
    $\mathbf{u} \cdot \mathbf{v} = \sqrt{a}\cdot\frac{1}{\sqrt{a}} + \sqrt{b}\cdot\frac{1}{\sqrt{b}} + \sqrt{c}\cdot\frac{1}{\sqrt{c}} = 1 + 1 + 1 = 3$.
    
2. **Calculate the Norms:**
    
    $\|\mathbf{u}\|^2 = a + b + c$
    
    $\|\mathbf{v}\|^2 = \frac{1}{a} + \frac{1}{b} + \frac{1}{c}$
    
3. **Apply Inequality:**
    
    $3^2 \leq (a + b + c)(\frac{1}{a} + \frac{1}{b} + \frac{1}{c})$
    
    $9 \leq (a + b + c)(\frac{1}{a} + \frac{1}{b} + \frac{1}{c})$
    

4.103^123
a) $A=\{ 2,4,8,7,0,1,2,\dots \}$
b) $B=\{ 5,7,8,4,2,1 \}$ ^3f45a9

c) Notice that $A=B$. $A$ and $B$ repeat the circle. Why it happen?

$2\equiv 5^{-1} \pmod{ 9}$ means that 2 and 5 are multiplicative inverse in modulo 9. 
$2\cdot 5=1 \pmod{ 9}$

Thus the formal definition
$$
a\cdot b\equiv 1 \pmod{n} 
$$

If such an integer $b$ exists, we write $b=a^{-1}$ and we say $a$ is invertible modulo n


How to know if it exist?
### The Existence Theorem (The Most Important Rule)

Mathematicians don't just guess; they use a specific criterion to know if an inverse exists before looking for it.

**Theorem:** An integer $a$ has a multiplicative inverse modulo $n$ **if and only if** $a$ and $n$ are coprime.

$$\text{Inverse exists} \iff \gcd(a, n) = 1$$

- **Example (from your problem):**
    
    $\gcd(2, 9) = 1$, so $2$ has an inverse (which is $5$).
    
- **Counter-Example:**
    
    $\gcd(3, 9) = 3 \neq 1$, so $3$ has **no** inverse. There is no integer $x$ such that $3x \equiv 1 \pmod 9$. (Because $3x$ will always be a multiple of 3, but 1 is not).

If $a$ and $n$ is coprime the $a^{m}\equiv S \pmod{9}$ , then $S$ is repeated set with cycle.


### 3. Key Properties

If $a$ and $b$ are invertible modulo $n$, the following properties hold (these look very similar to standard algebra):

**A. Uniqueness**

If an inverse exists, it is **unique** modulo $n$.

- _Proof:_ If $x$ and $y$ are both inverses of $a$, then $ax \equiv 1$ and $ay \equiv 1$.
    
    $$x \equiv x \cdot 1 \equiv x(ay) \equiv (xa)y \equiv 1 \cdot y \equiv y$$
    

**B. Symmetry (Reflexive)**

The inverse of the inverse is the original number.

$$(a^{-1})^{-1} \equiv a \pmod n$$

- _Example:_ In Mod 9, the inverse of 2 is 5. The inverse of 5 is 2.
    

**C. The "Socks and Shoes" Property**

The inverse of a product is the product of the inverses (order matters in matrices, but in modular arithmetic, it's commutative, so order is less critical, but formally):

$$(ab)^{-1} \equiv a^{-1}b^{-1} \pmod n$$
### How to Find It (The Algorithm)

For small numbers, you can guess. For huge numbers (like in cryptography), mathematicians use the **Extended Euclidean Algorithm**.

Since $\gcd(a, n) = 1$, Bezout's Identity states that there exist integers $x$ and $y$ such that:

$$ax + ny = 1$$

If you look at this equation modulo $n$, the term $ny$ becomes 0:

$$ax + 0 \equiv 1 \pmod n$$

$$ax \equiv 1 \pmod n$$

Thus, the coefficient $x$ from Bezout's Identity **is** the multiplicative inverse.

The multiplicative inverse allows us to "divide" by turning the operation into multiplication.

### 1. Solving Linear Equations (The "Algebra" Use)

This is the most direct mathematical application.

Suppose you need to solve for $x$:

$$2x \equiv 7 \pmod 9$$

**The Problem:** You cannot just "divide by 2" because $7/2 = 3.5$, which doesn't exist in integers.

**The Solution:** Multiply both sides by the **inverse** of 2.

(Recall from our previous step: the inverse of 2 mod 9 is **5**).

$$5 \cdot (2x) \equiv 5 \cdot 7 \pmod 9$$

$$(5 \cdot 2)x \equiv 35 \pmod 9$$

$$1 \cdot x \equiv 35 \pmod 9$$

$$x \equiv 8 \pmod 9$$

_(Check: $2 \times 8 = 16$. And $16 \equiv 7 \pmod 9$. It works!)_

Without the inverse, you would have to plug in numbers $0, 1, 2...$ until one worked. With the inverse, you can solve it algebraically.


### how to understand this intuitively In modular arithmetic,
if $g$ generates a set of numbers (a group), its inverse $g^{-1}$ will generate the exact same set of numbers, just in a different order

The best way to understand this intuitively is to stop thinking about **arithmetic** and start thinking about **movement on a circle**.

### 1. The "Circular Train" Analogy

Imagine the numbers $\{1, 2, 4, 8, 7, 5\}$ are stations on a circular train track.

- **The Generator ($g=2$):** This is a train that moves **Clockwise**.
    
    Every time you multiply by 2, you move to the _next_ station.
    
    $1 \to 2 \to 4 \to 8 \dots$
    
- **The Inverse ($g^{-1}=5$):** This is a train that moves **Counter-Clockwise**.
    
    Every time you multiply by 5, you move to the _previous_ station.
    
    $1 \to 5 \to 7 \to 8 \dots$
    

**The Intuitive Leap:**

If you have a circular track, it doesn't matter if the train goes forward or backward. **It will still visit the exact same stations.** It just visits them in the reverse order.

It is physically impossible for the "backward train" to discover a new station that the "forward train" missed, because they are stuck on the same rails.

---

### 2. The "Undo" Button

Think of the inverse as an "Undo" button.

- If you start at **1** and multiply by **2** (Press _Do_), you get **2**.
    
- If you take **2** and multiply by **5** (Press _Undo_), you get **1** again.
    

If you keep pressing "Do" ($2, 4, 8, 7, 5, 1...$), you map out a specific path.

If you keep pressing "Undo" ($5, 7, 8, 4, 2, 1...$), you are just walking back down that exact same path. You cannot stray from the path just by walking backwards.

### 3. Visual Verification (From your problem)

Let's look at the cycle you calculated in the previous step.

**The Path of 2 (Forward):**

$$1 \xrightarrow{\times 2} 2 \xrightarrow{\times 2} 4 \xrightarrow{\times 2} 8 \xrightarrow{\times 2} 7 \xrightarrow{\times 2} 5 \xrightarrow{\times 2} 1$$

**The Path of 5 (Reverse):**

Look at the arrows above. If you want to go from $1$ back to $5$, what do you do? You follow the arrow _backwards_.

$$1 \xleftarrow{\times 5} 2 \xleftarrow{\times 5} 4 \xleftarrow{\times 5} 8 \xleftarrow{\times 5} 7 \xleftarrow{\times 5} 5 \xleftarrow{\times 5} 1$$

See? The set of numbers is identical because the inverse just traces the arrows in the opposite direction.

4.104
a)
$$
\begin{align}
t^{2}&\equiv 4 \pmod{ 5} \\
t&\equiv \pm 2 \pmod{ 5} \\
t\equiv 2 &\text{ or }t\equiv 3 \pmod{ 5} 
\end{align}
$$
Thus let $t \in \{ 2,3,7,8 \}$


Since $t\equiv 2$, it follow that $t-2=5a$ for some $a \in \mathbb{Z}$. Thus,

When $t=2$
$$
\begin{align}
\frac{4(t-2)(t+2)}{5}+3&=\frac{4(0)(4)}{5}+3 \\
&=3
\end{align}
$$
$P(3):5(3)+1=16$


When $t=3$
$$
\begin{align}
\frac{4(t-2)(t+2)}{5}+3&=\frac{4(1)(5)}{5}+3 \\
&=7
\end{align}
$$
$P(7):5(7)+1=36$


When $t=7$
$$m = \frac{4(7^2 - 4)}{5} + 3 = \frac{4(49 - 4)}{5} + 3 = \frac{4(45)}{5} + 3$$

$$m = 4(9) + 3 = 36 + 3 = 39$$

- **Verify $P(39)$:**

$$5(39) + 1 = 195 + 1 = 196$$
    Since $196 = 14^2$, $5(39) + 1$ is a perfect square.
    **$P(39)$ is True.**

Let $t = 8$

- **Calculate $m$:**
$$m = \frac{4(8^2 - 4)}{5} + 3 = \frac{4(64 - 4)}{5} + 3 = \frac{4(60)}{5} + 3$$

$$m = 4(12) + 3 = 48 + 3 = 51$$

- **Verify $P(51)$:**
- 
$$5(51) + 1 = 255 + 1 = 256$$
    Since $256 = 16^2$, $5(51) + 1$ is a perfect square.
    **$P(51)$ is True.**

b) $S$ contain infinitely many element. Let $t=5k+2$ or $t=5k+2$ for every $k \in \mathbb{Z}$. 

c)
$$
\begin{align}
5\left( \frac{4(5c)}{5}+3  \right)+1 &=5(4c+3)+1 \\
&=20c+16
\end{align}
$$

We no need to substitute

$$
\begin{align}
20\left( \frac{t^{2}-4}{5} \right)+16&=4(t^{2}-4)+16 \\
&=4t^{2} \\
&=(2t)^{2}
\end{align}
$$
Q.E.D

==Remark==
So at first we need to prove that $M=\{ m \in \mathbb{N}:5m+1 \text{ is a perfect square} \}$ have infinitely many element. Thus, we need to find first what m will make $P(m)$ true?

Let $m=\frac{4(t^{2}-4)}{5}+3$ . Since $m\in \mathbb{N}$, thus, $m\geq 1$. We want to find a $t$ that make $m \in \mathbb{N}$.

Let $t\in \{ t \in \mathbb{Z}:t ^{2}\equiv 4 \pmod{ 5} \}$. Thus, we can prove the set have infinitely many element to prove that $M$.

How we know $m=\frac{4(t^{2}-4)}{5}$

We start from first let
$$
\begin{align}
a^{2}=5m+1 \\
a^{2}\equiv 1 \pmod{ 5} 
\end{align}
$$
Thus, $a\equiv 1$ or $a\equiv 4 \pmod{ 5}$. 

Notice that if $a\equiv 4$ then
$a^{2}\equiv 16\equiv 1 \pmod{ 5}$.
Notice that 16 is a perfect square.

The mathematician thinks: _"If I just ask students to find $a$, it's too easy. I want to make it harder. I will hide $a$ inside a new variable called $t$."_

If $t^{2}\equiv 4$ and $a=2t$
Then, $a^{2}=(2t^{2})=4(t)^{2}=4(4)=16\equiv 1 \pmod{ 5}$

Now substitute $a=2t$
$$m = \frac{(2t)^2 - 1}{5} = \frac{4t^2 - 1}{5}$$
where $t^{2}\equiv 4 \pmod{ 5}$.

To make the divisibility obvious, the mathematician used a clever algebraic trick to force the term $(t^2 - 4)$ to appear, since they knew $t^2 - 4$ is a multiple of 5.

They rewrote the numerator like this:

$$4t^2 - 1 = 4t^2 - 16 + 16 - 1$$

$$4t^2 - 1 = 4(t^2 - 4) + 15$$

Now, substitute this new numerator back into the fraction:

$$m = \frac{4(t^2 - 4) + 15}{5}$$

Split the fraction into two parts:

$$m = \frac{4(t^2 - 4)}{5} + \frac{15}{5}$$

$$m = \frac{4(t^2 - 4)}{5} + 3$$
---
if we did it **your way** (substituting $a = t$), the problem would have been much simpler. Let's see how much easier your version is:

### The "User's Version" (Simpler)

1. **Target:** We want $5m + 1 = t^2$.
    
2. **Modular Rule:** This implies $t^2 \equiv 1 \pmod 5$.
    
3. **Solve for m:**
    
    $$m = \frac{t^2 - 1}{5}$$
    

That's it! If the question setter had used your method, the problem would be:

> _"Let $t$ be an integer where $t^2 \equiv 1 \pmod 5$. Show that $m = \frac{t^2-1}{5}$ makes $5m+1$ a perfect square."_ 

4.105
$a_{1}<k<a_{n}$
$k=\{  a_{2},a_{3},\dots a_{n-1}\}$

Let $I=\{ 2,3,4,\dots,n-1 \}$ for $n\geq 3$
,Thus, $k=a_{i\in I}$
Wrong because $a_{1}<k<a_{n}$ doesn't necessarily mean it is an integer between the sequence.

Notice that the sequence consist consecutive integer as term either going to negative side or positive side or both
$1,2,3,4,5,\dots$
$1,0,-1,-2,-3$

Notice that $k$ is an integer between $a_{1}$ and $a_{n}$ that means that  $|a_{n}-a_{1}|> 1$ because they are not 2 consecutive integer in the sequence.

Thus, there must be some integer that its subscript is between $1<j<n$ for some $a_{j}$.. Thus, let $k=a_{j}$ 

Proof:
WLOG suppose $a_{n}>a_{1}$ and $k$ is an arbitrary integer such that $a_{1}<k<a_{n}$. Notice that $k-a_{1}\geq 1$ and $a_{n}-k\geq 1$. Thus, $a_{n}-a_{1}> 1$. Thus, $a_{1}\neq a_{n-1}$. It follow that there exists an integer $a_{n-1}$ which is the term before $a_{n}$. 


It is not formal because the last sentences is a circular proof.

Formal Proof:
Let 
$$
S=\{ i|1\leq i\leq n-1 \text{ and }a_{i}\leq k \}
$$




Proof analysis:
We know that the sequence is a integer where each step can only move by one integer (consecutive integer). Given that $a_{1}<k<a_{n}$. Thus, $a_{n}-a_{1}\geq 2$. It follow that there exist some step between $a_{1}$ and $a_{n}$. 

WLOG let $a_{n}>a_{1}$, $a_{1}$ is lower boundary and $a_{n}$ is upper boundary. What is the last step before upper boundary?

Think $k$ as the step before $a_{n}$. Consider the set below,

$$
S=\{ i|1\leq i\leq n-1 \text{ and }a_{i}\leq k \}
$$
$S$ is not empty set because $a_{1}<k$. Thus, by  WOP let $j=max(S)$. Thus, $a_{j}\leq k$. Thus, $a_{j+1}\geq k+1$. (because $j+1\not\in S$, thus it is strictly greater than $k$)

(Why we suddenly think of $a_{j+1}$ because the condition which is the inequality consist $a_{j}$ and $a_{j+1}$ , thus we need $a_{j+1}$ to find $a_{j}$)

in other word, we already know that $a_{j}\leq k$  and we need to prove that $a_{j}$ cannot be $k-1,k-2,\dots$ it only can be k because of the inequality. To use the inequality we need to find $a_{j+1}$.

$a_{j+1}-a_{j}\leq 1$
$(k+1)-a_{j}\leq 1$
$a_{j}\geq 1$
 Thus, the only possibility us $a_{j}=k$

Thus, $j \in S$ and $1\leq j\leq n-1$
Since $a_1 < k$ (so $a_j \ne a_1$) and $a_n > k$ (so $a_j \ne a_n$), the index $j$ must satisfy $1 < j < n$.