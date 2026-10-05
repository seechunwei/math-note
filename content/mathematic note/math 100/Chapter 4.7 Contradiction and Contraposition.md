argument by contradiction, is based on the fact that either a statement is true or it is false but not both. 

Proof by contradiction is indicated if you want to show that there is no object with a certain property, or if you want to show that a certain object does not have a certain property.

Method of Proof by Contradiction
1) Suppose the statement to be proved is false. That is, suppose that the negation of the statement is true.
2) Show that this supposition leads logically to a contradiction.
3) Conclude that the statement to be proved is true.

==Theorem==
There is no greatest integer.

Proof:
Suppose there is a greatest integer N. Then, $N\geq n$ for every integer n. Let $M=N+1$. Now M is an integer since it is a sum of integers. Also, $M>N$ since $M=N+1$. Thus $M$ is an integer greater than $N$. So $N$ is the greatest integer and $N$ is not the greatest integer, which is a contradiction. Hence the supposition is false and the theorem is true. Q.E.D


After a contradiction has been reached, the logic of the argument is always the same: “This is a contradiction. Hence the supposition is false and the theorem is true.

==Theorem==
There is no integer that is both even and odd.
Proof:
Suppose there is one integer $n$ that is both even and odd. By definition of even, $n =2a$ for some integer a, and by definition of odd, $n ={2}b+1$ for some integer b. Consequently,
$$
2a=2b+1
$$
and so 
$$
\begin{align}
2a-2b&=1 \\
2(a-b)&= 1 \\
a-b=\frac{1}{2}
\end{align}
$$
Now, since $a$ and $b$ are integers, the difference $a-b$ must be an integer. But $a-b=\frac{1}{2}$ and $\frac{1}{2}$ is not an integer. Then $a-b$ is an integer and $a-b$ is not an integer, which is a contradiction.

==Theorem==
The sum of any rational number and any irrational number is irrational.

Proof:
Suppose there exists a rational number $r$ and irrational number $s$ such that the sum any rational number and any irrational number is rational. By definition, $r=\dfrac{a}{b}$ and $r+s=\dfrac{c}{d}$ for some integer $a,b,c,d$ and $d\neq 0$ and $b\neq 0$
Thus, by substitution
$$
\begin{align}
\frac{a}{b}+s&=\frac{c}{d} \\
s&=\frac{c}{d}-\frac{a}{b} \\
&=\frac{bc-ad}{bd}
\end{align}
$$
Now, $bc-ad$ and $bd$ are all integers because the product and difference of integers are integers and $bd\neq 0$ by zero product property. Thus, $s$ is a quotient of two integers with $bd\neq 0$. Thus, by definition $s$ is a rational number which contradicts the supposition that $s$ is irrational.

Remark: often properties about sum also hold analogously for difference, Thus is because $x-y=x+(-y)$ for all real number x and y. Of course, this is not always true, for example, addition is both commutative and associative, but subtraction is neither.

Method of Proof by Contraposition
1. Express the statement to be proved in the form
$$
\forall x \in D,P(x)\to Q(x)
$$
2. Rewrite this statement in the contrapositive form
$$
\forall x \in D, \neg Q(x)\to \neg P(x)
$$
3. Prove the contrapositive by a direct proof.
a. Suppose x is a (particular but arbitrarily chosen) element of D such that Q(x) is false.
b. Show that P(x)is false.

==Proposition ==
For every integer $n$, if $n^{2}$ is even then $n$ is even.
Proof:
Suppose n is an arbitrary odd integer. By definition of odd, $n =2k+1$ for some integer k. By substitution,
$$
\begin{align}
n^{2}&=(2k+1)^{2} \\
&=4k^{2}+2k+1 \\
&=2(2k^{2}+k)+1
\end{align}
$$
Now, $2k^{2}+k$ is an integer because the product and sum of integers are integers. So, by definition of odd, $n^{2}$ is odd.

What is the relation between proof by contradiction and proof by contraposition?

The only thing that changes is the context in which the steps are written down.

$$
\forall x \in D.P(x)\to Q(x)
$$

Proof by contradiction
Suppose
$$
\exists x \in D, P(x)\land \neg Q(x)
$$
you then follow the steps of the proof by contraposition to deduce the statement $\neg P(x)$. But , $\neg P(x)$ is a contradiction to the supposition that $P(x) \land \neg Q(x)$. (Because to contradict a conjunction of two statements, it is only necessary to contradict one of them.)

==Question==
Prove that for all prime numbers a, b and c, $a^{2}+b^{2}\neq c^{2}$
Proof:
We prove by contradiction. Suppose there exists some prime numbers $a,b,c$ such that $a^{2}+b^{2}=c^{2}$

Case 1: $a$ is even and $b$ is even
Thus, $a^{2}$ and $b^{2}$ are even because the product of even integers are even. Since, the only even prime is 2. By substitution,
$$
\begin{align}
a^{2}+b^{2}&=2^{2}+2^{2} \\
&=8
\end{align}
$$
Since 8 is not a perfect square. Thus, $a^{2}+b^{2}\neq c^{2}$. This contradict our supposition.


Case 2: $a$ is odd and $b$ is odd
In this case, $a^{2}$ and $b^{2}$ are odd because the product of odd is odd. Thus, $c^{2}$ is even because the sum of odd integers is even.
Since, the only even prime is 2. By substitution
$$
\begin{align}
a^{2}+b^{2}&=2^{2}=4 \\ 
\end{align}
$$
Since $a$ and $b$ are odd primes, the smallest possible value for each is $3$.

$$a^2 + b^2 \ge 3^2 + 3^2 = 9 + 9 = 18$$
Since $18>4$
$$
a^{2}+b^{2}>c^{2}
$$
Thus, $a^{2}+b^{2}\neq c^{2}$ which contradict our supposition.

Case 3 One of the prime is odd and the other is even
WLOG, suppose $a$ is even and $b$ is odd. Thus, $a^{2}$ is even and $b^{2}$ is odd. Since, the only even prime is 2. By substitution
$$
\begin{align}
2^{2}+b^{2}=c^{2} \\
c^{2}-b^{2}=4 \\
(c-b)(c+b)=4
\end{align}
$$
Since $b$ and $c$ are primes (and thus integers), $(c-b)$ and $(c+b)$ must be integer factors of $4$. Since $b, c > 0$, we know $c+b > 0$. The possible positive factor pairs of $4$ are $(1, 4)$ and $(2, 2)$.

Subcase 3a: Factors are 2 and 2

$$c - b = 2$$
$$c + b = 2$$

Adding the equations gives $2c = 4 \Rightarrow c = 2$. Substituting back gives $b = 0$. Since $0$ is not a prime number, this is a contradiction.

- Subcase 3b: Factors are 1 and 4
$$c - b = 1$$
$$c + b = 4$$
Adding the equations gives $2c = 5 \Rightarrow c = 2.5$. Since $2.5$ is not an integer (and thus not prime), this is a contradiction.


Since the cases above exhaust all the possible cases, we can conclude that our supposition is false thus the statement is true. $\square$

The main idea of this proof is parity. Since 2 is the only even prime, if we can force any variable to be even, we instantly know its value must be 2. This collapses a problem with infinite possibilities into a problem with just one number.

In general: **Modular Arithmetic (The Fancy Version) **Mathematicians call this "checking modulo 2." It's a way of simplifying the universe so that only two numbers exist: 0 (even) and 1 (odd). It helps us quickly see if an equation is even _possible_ before we do hard work. (it can be modulo 3,4,5,..)
