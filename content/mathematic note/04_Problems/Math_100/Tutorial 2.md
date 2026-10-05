1)
a) 2 is a factor of n and 3 is a factor of n

b) if p, then q $\equiv \neg p\lor q$
The negation of it: $p\land \neg q$

q is n is old or n is 2
$\neg q$ : Neither n is old nor n is 2

$\therefore$ n is a prime and neither n is old nor n is 2.

2)
a) If this number is divisible by 9 , then it is divisible by 3
   if this number is not divisible by 3, then it is not divisible by 9

b) if temperature is less than 150 degree Celcius, compound X won't boil.
  if compound X boil, then its temperature is at least 150 degree Celcius

3 ) If two circle do not have a common center, they intersect in exactly two point (False)

4)
a) if you are not on time each day, then you cannot keep this job
b) if Jon's team win the rest of its games, then it win the championship

5)
a) 

| p   | q   | r   | $\neg q$ | $p\land \neg q$ | $q\lor r$ | $(p\land \neg q)\to r$ | $p\to(q\lor r)$ |
| --- | --- | --- | -------- | --------------- | --------- | ---------------------- | --------------- |
| T   | F   | F   | T        | T               | F         | F                      | F               |
| F   | T   | F   | F        | F               | T         | T                      | T               |
| F   | F   | T   | T        | F               | T         | T                      | T               |
| T   | T   | F   | F        | F               | T         | T                      | T               |
| T   | F   | T   | T        | T               | T         | T                      | T               |
| F   | T   | T   | F        | F               | T         | T                      | T               |
| T   | T   | T   | F        | F               | T         | T                      | T               |
| F   | F   | F   | T        | F               | F         | T                      | T               |

Since they have same truth value for all combination, thus they are equivalent

b) 
Let p represent "n is prime"
Let q represent "n is old"
Let r represent "n is 2"

$\therefore$ If n is prime and n is not old, then n is 2

6)
a) $\exists s \in D,\ E(s)$ and $M(s)$
b) $\forall s \in D,$ if $C(s)$, then $E(s)$  

7)
By modus tollens, Logic is not easy

8)
a) There are as many rational numbers as there are irrational numbers

b) Yes. An argument is consider valid if the resulting premises are all true, then the conclusion is also true. An conclusion follow by wrong premises doesn't give any idea if the argument is wrong.

9)
The statement p is true by specialization, Sam is not required to take MAT100. Thus, by Modus tollens Sam is not an economic major.

10)
Given p is true and r is true, thus by definition the statement "I'll buy a stereo or I'll buy motorcycle " is true. Since q is true, in order for the disjunction statement to be true, we can conclude that i will buy a stereo.

11)
Let a denote "i get a Christmas bonus"
Let b denote "i sell my motorcycle"
Let c denote "i will buy a stereo"

If a then c is true
If b then c is true
$$
\begin{align}
 (a\to c) \land(b\to c)&\equiv(\neg a\lor c)\land(\neg b\lor c) \\
&\equiv c\lor(\neg a\land \neg b) \\
&\equiv(\neg a\land \neg b)\lor c \\
&\equiv \neg(a\lor b)\lor c \\
&\equiv(a\lor b)\to c
\end{align}
$$
$\therefore$ If i get a Christmas bonus or i sell my motorcycle, then I'll buy a stereo


Tutor answer:
Division by case:
Assume i get a Christmas bonus or i sell my motorcycle.
Case 1: I get a Christmas bonus
Since p is true, it follow that I'll buy a stereo

Since Case 1 and Case 2 cover all the possible case, thus it follow that I will buy a stereo. (Case 1 and Case 2 not necessarily to be negation of each other)

Case 2: I do not get Christmas bonus
Since i do not get Christmas bonus, i will sell my motorcycle. Since q is true, it follow that i will buy a stereo.


[[Chapter 2 THE LOGIC OF COMPOUND STATEMENTS#^Division-into-case]]


12)
Given that the conditional statement is true, and the conclusion is true, thus the hypothesis can be false or true, it does not necessarily to be true.

13)
a) True

b) False ,a=0 and b=1
ab=0, $a=0\land b\neq 0$ 

c) False, a=-5, b=0, c=-6 ,d=0
$ac=30$ and $bd=0$ , thus $ac \not<bd$

14)
a) $p\leftrightarrow q$ means if p then q and if q, then p denoted by:

$$
\begin{align}
(\neg p\lor q)\land(\neg q\lor p)&\equiv(\neg p\lor p)\land(\neg p\lor p)\text{  given p=q}\\
&\equiv t\land t \\
&\equiv t
\end{align}
$$
b) 
$$\begin{align}
\to q)\leftrightarrow (\neg q\to \neg p)&\equiv (\neg(p\to q)\lor(\neg q\to \neg p))\land (\neg(\neg q\to \neg p)\lor(p\to q)) \\
&\equiv(\neg(\neg p\lor q)\lor(q\lor \neg p))\land(\neg(q\lor \neg p)\lor(\neg p\lor q)) \\
&\equiv t\land t \\
&\equiv t

\end{align}
$$



15)
if A is knight , B is a knight, A and B are opposite type (contradiction)
if A is knave, B is knave, A and B are same type
Thus, A and B are knave






$\exists x \in D,P(x)\to Q(x)\equiv \exists x \in D,P(x)\land Q(x)$



