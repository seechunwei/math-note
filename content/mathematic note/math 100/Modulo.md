Modulo is a system of arithmetic of integer that wrap around the integer into several group

In formal way
Suppose $a,b$ and n are integer for $n> 1$
$a\equiv b\text{ (mod n)}$ iff $a-b=nk$ for some integer k

Why $n>1$ because every number is divisible by 1, thus the only remainder is 0.

It is a congruence statement , a is said to be congruence to b mod n

b is said to be the residue modulo n

Modular arithmetic deal with remainder, it is associated with QR Theorem that is
$a=nq+r$ implies that $a\equiv r \text{ (mod n)}$ (Notice that vice versa is not correct because r can be negative value)

in this case a is dividend and r is remainder thus 
$0\leq r<n$

![[qr number line.png]]
Thus, $n-dq=r$ or we said that $n-r=dq$ which is the formal definition of congruence. Imagine r is something that left over or extra when you take multiple step of size n.

The definition of congruence also apply to negative value. For example:
$2\equiv-3 \text{ (mod 5)}$ 
$2-(-3)=5$ and $5\mid 5$

In this case remainder is something left over when you take extra one step denote as $r'$ and $r'$ is negative integer.

==Propetry 1==
Notice that, $-r'+r=n$
Thus,  $x\equiv 2 \text{ (mod 5)}$ iff $x\equiv -3 \text{ (mod 5)}$

We can use addiction, subtraction, and multiplication but division is problematic.

Exp:
Solve $x^{2}+3\equiv 0 \text{ (mod 7)}$
By subtract 3 from both side, we get 
$$
x^{2}\equiv-3 \text{ (mod 7)}
$$
and by the Property 1
$$
x^{2}\equiv 4 \text{ (mod 7)}
$$
Thus, 
$$
x\equiv\pm 2 \text{ (mod 7)}
$$
Why?
$4^{2} \equiv 4 \text{ (mod 6)}$
Thus, $4\equiv \pm2 \text{ (mod 6)}$
Which is true.

==Notice that== This is not true, the statement only true when $4\equiv-2 \pmod 6$ Why this happen?


Why?
Consider
$4=6(0)+2$ or $4= 6(1)-2$ 

What happen when we multiply these 2 equation 
$$
4^{2}=\dots(2)(2)
$$
Thus the remainder is 4 which is $2^{2}$. Notice that $(-2)(-2)$ will work.

==Property 2==
$n \equiv 0 \text{ (mod n)}$
$nk\equiv 0 \text{ (mod n)}$
Thus, if we plus 7 earlier it is actually equal to
$$
x^{2}\equiv 4 \text{ (mod 7)}
$$

How about division?
$n =dq+r$ what if the whole equation divide 2. Then it become
$\dfrac{n}{2}=\dfrac{1}{2}(dq)+\dfrac{r}{2}$

Since n is divisible by 2 

$33\equiv 3 \text{ (mod 6)}$
divide 3 become
$11\equiv 1 \text{ (mod 2)}$
Just imagine the number line being shrink 3 times as before, thus each of the gap shrink 3 times as well.

Why we cannot divide the congruence statement when the modulo class does not have common factor? Actually we can, just imagine the number line shrink but the gap n is remained.

Solve $x^{2}\equiv 2 \text{ (mod 4)}$
Notice that the possible residue modulo 4 is $\{ 0,1,2,3 \}$

$nx^{2}$ is multiple of 4 for some  integer n. Thus, square of it is also divisible by 4. So, the remain part is remainder.

Notice that if we square the remainder it will never give us remainder of 2

$x\to \{ 0,1,2,3 \}$
$x^{2}=\{ 0,1,0,1 \}$

What about negative exponents?
Let say we need to solve 
$3x\equiv 1 \text{ (mod 5)}$

In this case that is no common factor, thus we will multiply both side by inverse of 3
$$
\begin{align}
3^{-1}\times 3x&\equiv 3^{-1}\cdot 1 \text{ (mod 5)} \\
x&\equiv 3^{-1}
\end{align}
$$

What is $3^{-1}$ mod 5?
Consider this 
$$
\begin{align}
3x\equiv 6 \text{ (mod 5)} \\
x\equiv 2 \text{ ( mod 5)}
\end{align}
$$

In this case we say that the inverse of 3 is 2 and vice versa.

==Chinese Remainder Theorem==?
How to solve a system of congruence?

==question==
Find  
(Assignment 3)
Noticed that 5 and 2 have same remainder in modulo 3 which is 2.

The question use $a+b$ but not $a-b$ because in modulo 2 $-1 \equiv 1$
$$a - b \equiv a + (-b) \equiv a + (b) \equiv a + b \pmod 2$$

[Basics of Modular Arithmetic](https://www.youtube.com/watch?v=Q_V_itu_kbs)

[[Chapter 3 supplement Exrcises#^ama]]

[[Divisibility#^37055d]]
