a)
i) 
There exists an element *y* in *Y* such that for all element *x* in *X*, $x-y<0$

ii)
Let y=10, the inequality below show that $P(x,10)$ is true for all element x in X
$$
\begin{align}
\ P(3,10): 3-10<0 \\
\ P(5,10): 5-10<0 \\
\ P(8,10): 8-10<0 
\end{align}
$$

Since $P(x,10)$ is true for all element $x$ in $X$, we can conclude that $\exists y \in Y,\forall x \in X,P(x,y)$ is true.






b)
The first part of the lab policy is defined below:
$$
\begin{align}
A\text{ only if }T\land B\land S\equiv A\to(T\land B\land S) 
\end{align}
$$

The second part of the lab policy is defined below:
$$
\begin{align}
\text{Let P denote (E }\to A) \\
\end{align}
$$
Thus,
$$
\begin{align}
P\ unless\ U&\equiv \text{if not U, then P} \\
 & \equiv \neg U\to P \\
&\equiv \neg U\to(E\to A)
\end{align}
$$
Combine them together:
$$
\begin{align}
(A\to(T\land B\land S)) \ \land \ (\neg U\to(E\to A))
\end{align}
$$

Suppose we don't know whether Carine get access or not, Given that $T\land B\land S$ is true, thus the statement $A\to(T\land B\land S)$ is true regardless of the truth value of $A$ . Thus, A can be false or true in this case. 
Thus, the truth value of the whole statement is depend on the statement below:

$$
\begin{align}
\neg U\to(E\to A)
\end{align}
$$
Given that Carine is suspended, $\neg U$ is false because $U$ is true. Since, the hypothesis is false, the statement is true regardless of the truth of conclusion. In this case A can be true or false.

In conclusion, A can be false or true based on given assumption. It is because the policy doesn't tell us when A must happens, it only set necessary condition for A to happen and when will it happen if it is not suspended. 

There is **no contradiction** between her suspension and being denied access. Thus, the access denial is fair and justifiable.





c)
$$\forall y \in E(y\equiv 2 \text{(mod 3) }\implies\exists z_{1}\neq z_{2}\in F:y+z_{1}\equiv y+z_{2}\equiv 0\text{ (mod 3))}$$
This statement only be true when all element $y\in E:y\equiv 2$ (mod 3) , $\exists z_{1}\neq z_{2}\in F:y+z_{1}\equiv y+z_{2}\equiv 0\text{ (mod 3)}$ hold, if an element $y$ to be found make the existential statement false then the statement is false.



$y\equiv 2 \ (\text{mod 3})$ means there is a remainder 2 when $y$ is divide by 3 
denoted by $y=3q+2$ where q is quotient 
$$
\begin{align} 
y=nq+r \text{ means } y\equiv r \text{ (mod n)} \\        \\
\ 8=(3\cdot 2)+2 \text{ means } 8\equiv 2 \text{ (mod 3)} \\
14=(3\cdot 4)+2 \text{ means } 14\equiv 2 \text{ (mod 3)} \\
20=(3\cdot 6)+2 \text{ means } 20\equiv 2 \text{ (mod 3)}
\end{align}
$$
Thus, all element $y \in E$ satisfy the condition $y\equiv 2$ (mod 3)


$\exists z_{1}\neq z_{2} \in F:y+z_{1}\equiv y+z_{2}\equiv 0$ (mod 3) means there exists two distinct element in $F$ such that  $y+z_{1}$ and $y+z_{2}$  are multiple of 3

$$\begin{array}
\ y+z\equiv 0 \text{ (mod 3)} \\
\text{Since the remainder when y divide by 3 is 2, thus z must have a remainder of 1} \\
z\equiv 1 \text{ (mode 3)}
\end{array}
$$


We need to find at least 2 distinct element in $F$ such that $z\equiv 1$ (mod 3)
$$
\begin{align}
z=nq+r \ means\ y&\equiv r \text{ (mod n)} \\
5=3\cdot 1+2,\ 5&\equiv 2\text{ (mod 3)} \\
8=3\cdot 2+2, \ 8&\equiv 2 \text{ (mod3)} \\
11=3\cdot 3+2, \ 11&\equiv 2 \text{ (mod 3)} \\
14=3\cdot 4+2,\ 14&\equiv 2\text{ (mod 3)} \\
17=3\cdot 5+2, \ 17&\equiv 2 \text{ (mod3)}
\end{align}
$$


We can conclude that that is no such element in $F$ such that $z\equiv 1$ (mod 3)

Let $y=8$, we need to find two distinct element in $F$ such that $y+z_{1}\equiv y+z_{2}\equiv 0\text{ (mod 3)}$ . But there is no element in $F$ that satisfy this property. Since $y=8$ is a counterexample for the statement, we can conclude that the statement is false.






d)
There are 4 statement here which represented by p, q, r, s
p: Astra say that Bolt caused it
q: Bolt say that Coda caused it
r: Coda say that Delta did not cause it
s: Delta say that Bolt caused it



Let's examine each possibility

1) If p is true, then Bolt caused it
	If the statement "Bolt caused it" is true, then s  is true. In this case, there are at least 2 statement true at the same time, it violate the statement "Exactly one is true". Thus, p is false.

2) If q is true, then Coda caused it
	The statement "Coda cause it" is true, it doesn't violate the rule "Exactly one is true" because the statement  doesn't implies anything about Astra, Bolt and Delta.
	

3) If r is true, then Delta did not cause it.
	The statement "Delta did not cause it" doesn't violate the rule "Exactly one is true" because the statement  doesn't implies anything about Astra, Bolt and Coda.

4) s and p declare the same thing which is Bolt caused it. Thus, $p\equiv s$ .Since p is false, s is also false.


We can conclude that it's either q true or r true but not both denoted by $q\oplus r$ 

Since the question didn't declare that there is exactly one robot caused the fault, there are possibility more than 1 robot caused the fault. The question only state that exactly one statement is true. 

Let defined truth value =$\{ 0,1 \}$, where 0 is false and 1 is true
"Exactly one statement is true" means the sum of truth value for the all statement is 1


$$
p+q+r+s=1
$$
Let 
a= Astra caused it
b= Bolt caused it
c= Coda caused it
d= Delta caused it

Let defined the statement p, q, r, s in term of a, b, c, d.
$p\equiv b$
$q\equiv c$
$r\equiv \neg d$
$s\equiv b$

The truth value of $\neg d$ is defined as ($1-d$) since we will get 0 if $d=1$ and 1 if $d=0$ 

Thus , the constraint "Exactly one is true" can be denoted by:
$$\begin{array}
\ b+c+(1-d)+b=1 \\
2b+c+(1-d)=1
\end{array}
$$


From previous result, $q\oplus r$ is true, lets examine each case in term of statement $a, b,c,d$

1) $q\equiv c$
If q is true, then c is true. Thus, the truth value of c is 1 means $c=1$
$$\begin{align}
2b+1+(1-d)=1 \\
2b+(1-d)=0
\end{align}
$$


Since $b\in \{ 0,1 \}$ and $d\in \{ 0,1 \}$ . Thus, in order to make this equality true, $2b=0$ and $(1-d)=0$
$$
\begin{align}
2b=0 \\
b=0 \\
(1-d)=0 \\
d=1
\end{align}
$$


Notice that $a$ can be 1 or 0 because it doesn't affect the truth of equality. Thus, we can conclude that when q is true, $c=1$ , $b=0$ , $d=1$ , $a\in \{ 0,1 \}$

Thus, the possible culprit set is $\{ c,d \}$ or $\{ a,c,d \}$



2) $r\equiv \neg d$
If r is true, then $\neg d$ is true. Since $\neg d$ is true, thus $d$ is false denoted by $d=0$
$$
\begin{align}
2b+c+(1-0)=1 \\
2b+c=0
\end{align}
$$
Since $b\in \{ 0,1 \}$ and $c\in \{ 0,1 \}$ . Thus, in order to make this equality true, $2b=0$ and $c=0$
$$
\begin{align}
2b=0 \\
b=0 \\
c=0
\end{align}
$$


In this case, $d=0$ , $b=0$ , $c=0$ , $a\in \{ 0,1 \}$ . Thus, the possible culprit set is $\{ \emptyset\}$ or $\{ a \}$


Let the possible culprit set denoted by C, thus:
$$
C=\{ \{ c,d \},\{ a,c,d \},\{ \emptyset \},\{ a \} \}
$$
It means that there are 4 possible combination of culprit which is
1) $\{ c,d \}$ : Coda and Delta caused it
2) $\{ a,c,d \}$ : Astra, Coda and Delta caused it
3) $\{ \emptyset \}$ : No one caused it
4) $\{ a \}$ : Astra caused it






e)
Given that Arin is informed about the month and Bryan is informed about the day. Let A denote the possible month and B denote the possible date
$$\begin{array}
\ A\in \{ May,Jun,Jul,Aug \} \\
B\in \{ 14,15,16,17,18 \}
\end{array}
$$
The possible date for each month:
$$\begin{array} \\
May=\{ 15,16,19 \} \\
Jun =\{ 17,18 \} \\
Jul =\{ 14,16 \} \\
Aug =\{ 14,15,17 \}
\end{array}
$$


There are 3 statement here which arrange in order. Let's examine one by one.

1) The first statement state that Arin don't know the date and he know Bryan doesn't know.  What is the possible month that Arin informed that can implies Bryan doesn't know. 
- If Arin get May and Jun .Since, May and Jun have unique date which is 19 and 18 respectively, if Bryan get these two date, then he would know the exact month. Thus, we can eliminate May and Jun.

2) The second statement state that Bryan know the exact date after he know that "Arin know that he doesn't know.". It means after we eliminate May and Jun, Bryan know the exact date. It means that Bryan get unique date which is 15, 16 or 17. Thus, we can eliminate date 14.

3) The third statement state that Arin know the exact date after he know that Bryan know the exact date. The possible month is Jul or Aug. 
- If Arin get Aug, he would not know the exact date since there are 2 date which is 15,17.
- If Arin get Jul, he would know the exact date since there is only one possibility which is 16.

Thus, we can conclude that the concert date is on 16 Jul.
