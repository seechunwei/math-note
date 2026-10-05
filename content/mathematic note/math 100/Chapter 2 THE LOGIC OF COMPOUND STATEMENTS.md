  
An argument is a sequence of statements aimed at demonstrating the truth of an assertion. The assertion at the end of the sequence is called the conclusion, and the preceding statements are called premises. In logic, the form of an argument is distinguished from its content. Analyze an argument’s form help us to determine whether the truth of the conclusion follows necessarily from the truth of the premises.

# 2.1 Logical Form and Logical Equivalence

>==Definition 2.1.1==.A statement (or proposition) is a declarative sentence that is true or false but not both.

Just as we use variables x, y, z, et cetera as placeholders for numbers, we can use statement variables, usually denoted p, q, r, et cetera, as placeholders for statements.

## Compound statement
Three elementary logical operation:
1. $\neg$ or ~ denotes negation, $\neg p$ is read as not p or it is not the case that p
2. $\land$ denotes and/conjunction ,$p\land q$ 
3. $\lor$ denotes or/ disjunction , $p\lor q$

The order of operations specifies that, $\neg$ is performed first.
$\neg p\land q=(\neg p)\land q$

The symbols $\land \lor$ considered coequal in order of operation
An expression such as $p\land q\lor r$ considered ambiguous. This expression must be written as either $(p\land q)\lor r$ or $p\land(q\lor r)$ to have meaning. But by convention, $\land$ has higher precedence compare to $\lor$.

p but q means p $\land$ q 
neither p nor q means $\neg p\land \neg q$

The notation for inequalities involves and and or statements. For instance, if x, a, and b are particular real numbers, then
$$
\begin{array}
\ x\leq a \text{ means } x<a \text{ or } x=a \\
a\leq x\leq b\ means\ a\leq x \text{ and } x\leq b
\end{array}
$$
$\neg(a\leq x\leq b)=x< a \text{ or }x> b$
It is actually De Morgan's Laws

## Truth Values
We now define such compound sentences as statements by specifying their truth values in terms of the statements that compose them.

>==Definition 2.1.2==. If p is a statement variable, the negation of p is “not p” or “It is not the case that p” and is denoted $\neg$p. It has opposite truth value from p: if p is true, $\neg$p is false; if p is false, $\neg$p is true.

Truth table
ctrl +p, search table, insert table

| p   | $\neg p$ |
| --- | -------- |
| T   | F        |
| F   | T        |

>==Definition 2.1.3==. If p and q are statement variables, the conjunction of p and q is “p and q” denoted $p\land q$. It is true when, and only when, **both p and q are true**. If either p or q is false, or if both are false, $p\land q$ is false.

The only way for an and statement to be true is for both components to be true

>==Definition 2.1.4. ==If p and q are statement variables, the disjunction of p and q is “p or q,” denoted p$\lor$q. It is true when either p is true, or q is true, or both p and q are true; it is false only when both p and q are false.

The only way for an or statement to be false is for both components to be false.

>==Definition 2.1.5.== A statement form (or propositional form) is an expression made up of statement variables (such as p, q, and r) and logical connectives (such as $\land \lor$and $\neg$) that becomes a statement when actual statements are substituted for the component statement variables. The truth table for a given statement form displays the truth values that correspond to all possible combinations of truth values for its component state-ment variables.

>==Definition 2.1.6== Note that when or is used in its exclusive sense, the statement “p or q” means “p or q but not both” or “p or q and not both p and q,” which translates into symbols as $(p\lor q)\land \neg(p\land q)$.


| p   | q   | $p\lor q$ | $p\land q$ | $\neg(p\land q)$ | $(p\lor q)\land \neg(p\land q)$ |
| --- | --- | --------- | ---------- | ---------------- | ------------------------------- |
| T   | T   | T         | T          | F                | F                               |
| T   | F   | T         | F          | T                | T                               |
| F   | T   | T         | F          | T                | T                               |
| F   | F   | F         | F          | T                | F                               |
It can be clearly shown by vein diagram 
Exclusive or is often symbolized as p$\oplus$q or p XOR q

The essential point about assigning truth values to compound statements is that it allows you—using logic alone—to judge the truth of a compound statement on the basis of your knowledge of the truth of its component parts


>==Definition 2.1.7==. Two statement forms are called logically equivalent if, and only if, they have identical truth values for each possible substitution of statements for their statement variables. The logical equivalence of statement forms P and Q is denoted by writing P $\equiv$ Q.

How to prove 2 statement are logically equivalent ? 
1) using truth value table
2) prove by contradiction, A **proof by contradiction** shows a statement P is true by assuming the opposite ¬P and deriving a logical contradiction (something impossible, e.g. 0=10=10=1 or a statement and its negation). Since ¬P leads to absurdity, P must be true or vice versa.
3) Prove by counter example, find one possible combination that show difference truth value
4) prove by arguments

>==Definition 2.1.8. ==Double Negative Property: $\neg(\neg p)\equiv$p



>==Definition2.1.8==Negations of And and Or: De Morgan’s Laws 
The negation of an and statement is logically equivalent to the or statement in which each component is negated. The negation of an or statement is logically equivalent to the and statement in which each component is negated
$$
\begin{array}
\ \neg(p\land q)\equiv \neg p\lor \neg q \\
\ \neg(p\lor q)\equiv \neg p\land \neg q \\ 
\end{array}
$$
$$
\begin{align}
\ \neg(p\land q\lor r)&\equiv \neg p(\land q\lor r) \\ 
\ &\equiv \neg p\lor(q\lor r) \\
\ &\equiv \neg p\lor \neg q\land \neg r \\
\ &\text{wrong}
\end{align}

$$

The $\land$ binds tighter than $\lor$ by convention.

we already know that the truth value of negation of a statement is opposite the truth value of the statement, p and q only be true for only one combination and be false for other 3 combination, negation of it means 1false3true, we know that the truth value of p or q is 1false3true.So we need to find the relationship between these two open statement.

Besides, we now that either 1 or both statement false then only p and q will be false, the negation of it means either 1 or both statement false then only p and q will be true, let the (p and q)= A , so what disjunction will make the statement be true? apparently we just negate the component statement become not p or not q. It can be clearly shown by the **True Table 2.1.7**

“It is not true that I’m both tired and hungry”
→ means “Either I’m not tired or I’m not hungry.”

>==Definition 2.1.9== A tautology is a statement form that is always true regardless of the truth values of the individual statements substituted for its statement variables. A statement whose form is a tautology is a tautological statement.
>A contradiction is a statement form that is always false regardless of the truth values of the individual statements substituted for its statement variables. A state-ment whose form is a contradiction is a contradictory statement.

$p\lor \neg p\equiv t$ 
$p\land \neg p\equiv c$
$p\land t\equiv p$ , since t always true regardless statement substituted for statement variable, if p false the whole statement false, if p true , the whole statement true
$p\lor t\equiv t$
$p\land c\equiv c$
$p\lor c\equiv p$

**Theorem 2.1.1 Logical Equivalences**

Given any statement variables \(p, q, r\), a tautology \(t\), and a contradiction \(c\),  
the following logical equivalences hold:

$$
\begin{array}{llcll}
\textbf{1.} & \text{Commutative laws:} &\quad& p \land q \equiv q \land p & p \lor q \equiv q \lor p \\[6pt]
\textbf{2.} & \text{Associative laws:} &\quad& (p \land q) \land r \equiv p \land (q \land r) & (p \lor q) \lor r \equiv p \lor (q \lor r) \\[6pt]
\textbf{3.} & \text{Distributive laws:} &\quad& p \land (q \lor r) \equiv (p \land q) \lor (p \land r) & p \lor (q \land r) \equiv (p \lor q) \land (p \lor r) \\[6pt]
\textbf{4.} & \text{Identity laws:} &\quad& p \land t \equiv p & p \lor c \equiv p \\[6pt]
\textbf{5.} & \text{Negation laws:} &\quad& p \lor \neg p \equiv t & p \land \neg p \equiv c \\[6pt]
\textbf{6.} & \text{Double negative law:} &\quad& \neg(\neg p) \equiv p & \\[6pt]
\textbf{7.} & \text{Idempotent laws:} &\quad& p \land p \equiv p & p \lor p \equiv p \\[6pt]
\textbf{8.} & \text{Universal bound laws:} &\quad& p \lor t \equiv t & p \land c \equiv c \\[6pt]
\textbf{9.} & \text{De Morgan’s laws:} &\quad& \neg(p \land q) \equiv \neg p \lor \neg q & \neg(p \lor q) \equiv \neg p \land \neg q \\[6pt]
\textbf{10.} & \text{Absorption laws:} &\quad& p \lor (p \land q) \equiv p & p \land (p \lor q) \equiv p \\[6pt]
\textbf{11.} & \text{Negations of t and c:} &\quad& \neg t \equiv c & \neg c \equiv t
\end{array}
$$


Question
Determine whether the statements in (a) and (b) are logically equivalent.
a. Bob is both a math and computer science major and Ann is a math major, but Ann is not both a math and computer science major.
b. It is not the case that both Bob and Ann are both math and computer science majors, but it is the case that Ann is a math major and Bob is both a math and computer science major.

Let p = Bob is math major
Let q = Bob is computer science major
Let r = Ann is a math major
Let s = Ann is a computer major

Statement  a
$p\land q\land r\land \neg(r\land s)\equiv p\land q\land r\land(\neg r\lor \neg s)$  
This compound statement can only be true if p, q, r and $(\neg r\lor \neg s)$ true. Since r is true $\neg r$ must be false, thus the truth value of this compound statement is based on $p\land q\land r\land \neg s$
Another way to prove:
$$
\begin{align}
\ r\land(\neg r\lor \neg s)&\equiv (r\land \neg r)\lor(r\land \neg s)\text{ by distributive law} \\
&\equiv c\lor(r\land \neg s) \text{ by negation law}\\
&\equiv r\land \neg s \\  
\end{align}
$$



Statement b
$$\begin{align}
\ \neg((p\land q)\land(r\land s))\land r\land p\land q&\equiv \neg(p\land q)\lor \neg(r\land s)\land r\land p\land q \\
&\equiv(\neg p\lor \neg q)\lor (\neg r\lor \neg s)\land r\land p\land q \\
\end{align}

$$
This compound statement can only be true if p, q, r, and the or statement are true. Since p and q are true, $(\neg p\lor \neg q)$ will be false. Thus, in order to make the or statement true, the $(\neg r\lor \neg s)$ must be true. Since r is true, not r is false. In conclusion, the truth value depends on $(\neg s\land p\land q\land r)$ .(Shown)

Notice that these two compound statement is $p\land q\land r\land s\land\dots$ statement, where p, q, r, s are statement variable substituted in the component statement. In such case the only possible combination to make this statement true is all of the statement variable are true, to make this compound statement false either one or more statement false will do , if want to make the compound statement false $\neg s$ and $\neg r$ is not the sufficient condition of it, it means $\neg s$ and $\neg r$ doesn't affect the falsity of statement , thus we cannot simplify the statement by assuming it is false, so if we assume the statement is true we can see that $\neg s$ play important role while we can just eliminate $\neg r$ because it doesn't affect the truth of statement.

# 2.2 Conditional Statement

>==Definition2.2.1== If p and q are statement variables, the conditional of q by p is “If p then q” or “p implies q” and is denoted $p\to q$. It is false when p is true and q is false; other-wise it is true. We call p the hypothesis (or antecedent) of the conditional and q the conclusion (or consequent).

Such a sentence is called conditional because the truth of statement q is conditioned on the truth of statement p. The statement only say what happen if p take place, i doesn't say what happen if p doesn't take place, thus it's always true when p (hypothesis) is false regardless the truth of q. It is only false when p is true and q is false.

>==Definiton2.2.2==Representation of If-Then as Or
Thus, it obvious that if p then q is the same as not p or r
$$
p\to q\equiv \neg p\lor q
$$


| p   | q   | $p\to q$ |
| --- | --- | -------- |
| T   | T   | T        |
| T   | F   | F        |
| F   | T   | T        |
| F   | F   | T        |



In expressions that include $\to$ well as other logical operators such as $\land ,\lor, \neg$ the order of operations is that $\to$ performed last


==Definition 2.2.3== Division into Cases: Showing That $p\lor q\to r\equiv(p\to r)\land(q\to r)$

$p\lor q\to r$ means if p or q is true, then r is true, it means that if p is true, then r is true and if q is true, then r is true  

$$
\begin{align}
\ p\lor q\to r&\equiv \neg(p\lor q)\lor r \\
&\equiv(\neg p\land \neg q)\lor r \\
&\equiv(\neg p\lor r)\land(\neg q\lor r) \\
&\equiv (p\to r)\land(q\to r)
\end{align}
$$

[[#^Division-into-case]]

==Definition 2.2.4== The negation of “if p then q” is logically equivalent to “p and not q.”
$$
\neg(p\to q)\equiv p\land \neg q
$$

==Definition 2.2.5== The Contrapositive of a conditional statement of the form "If p then q" is if ~q then ~p. They are equivalent
$$
p\to q\equiv \neg q\to \neg p
$$
$$
\begin{align}
\ p\to q&\equiv \neg p\lor q \\
&\equiv q\lor \neg p \\
&\equiv \neg q\to \neg p
\end{align}
$$
This logical equivalence is also the basis for one of the most important laws of deduction, modus tollens (to be explained in Section 2.3), and for the contrapositive method of proof

[mudus tollens]
[contrapositive method of proof]

==Definition 2.2.6== If p then q denoted by $p\to q$ means p is the sufficient condition for q and if not q then not p denoted by $\neg q\to \neg p$  means q is the necessary condition for p.

Imagine the arrow diagram below
![[arrow diagram.png]]
The circle indicate lamp, if one or more than one small lamp light up, the big lamp will light up, it means the small lamp is sufficient condition for big lamp, on the other hand, if big lamp doesn't light up, no small lamp will light up, it show that big lamp is the necessary condition for small lamp

>==Definition 2.2.7.== Suppose a conditional statement of the form “If p then q” is given.
1. The converse is “If q then p.”
2. The inverse is “If $\neg$p then $\neg$q.”
$$\begin{array}
\ \text{The converse of }p\to q\text{ is }q\to p \\
\text{The inverse of }p\to q\text{ is }\neg p\to \neg q
\end{array}
$$
3. A conditional statement and its converse are not logically equivalent.
4. A conditional statement and its inverse are not logically equivalent.
5. The converse and the inverse of a conditional statement are logically equivalent to each other.


>==Definition 2.2.8== if p and q are statements, p only if q means “if not q then not p, ”or, equivalently,“ if p then q.”
>
>To say “p only if q” means that p can take place only if q takes place also. That is, if q does not take place, then p cannot take place. it means $\neg q\to \neg p$ thus it's equivalent with $p\to q$


==Definition 2.2.9== Given statement variables p and q, the biconditional of p and q is “p if, and only if, q” and is denoted p$\leftrightarrow$q. It is true if both p and q have the same truth values and is false if p and q have opposite truth values. The words if and only if are sometimes abbreviated iff.

$\neg(p\leftrightarrow q)\equiv p\oplus q$
$\equiv(p\lor q)\land \neg(p \land q)$
$\equiv(p \land \neg q)\lor(\neg p\land q)$

How to understanding this, the $\neg(p \iff q)$ means $p$ and $q$ have different truth value. Thus, 
1) it is or but not both 
2) it is either (p true and q false) or (p false and q true)

In logic, a hypothesis and conclusion are not required to have related subject matters.

# 2.3 Valid and Invalid Arguments

An argument form is called valid if, and only if, whenever statements are substituted that make all the premises true, the conclusion is also true.

>==Definition 2.3.1== An argument is a sequence of statements, and an argument form is a sequence of statement forms. All statements in an argument and all statement forms in an argument form, except for the final one, are called premises (or assumptions or hypotheses). The final statement or statement form is called the conclusion. The $\therefore$ symbol  which is read “therefore,” is normally placed just before the conclusion.
>
To say that an argument form is valid means that no matter what particular statements are substituted for the statement variables in its premises, if the resulting premises are all true, then the conclusion is also true. To say that an argument is valid means that its form is valid

Testing an Argument Form for Validity
1. Identify the premises and conclusion of the argument form
2.  Construct a truth table showing the truth values of all the premises and the conclusion.
3. A row of the truth table in which all the premises are true is called a **critical row**. If there is a critical row in which the conclusion is false, then it is possible for an argument of the given form to have true premises and a false conclusion, and so the argument form is invalid. If the conclusion in every critical row is true, then the argument form is valid.

==Definition 2.3.2== Modus ponens 
$$
\begin{align}
\ &\text{if p then q.} \\
&p \\
\therefore q
\end{align}
$$

When $p\to q$ is true and p is true the only possibility for q is true

An argument form consisting of two premises and a conclusion is called a **syllogism**. The first and second premises are called the **major premise** and **minor premise**, respectively. The most famous form of syllogism in logic is called modus ponens


| p   | q   | ==$p\to q$== | ==p== | q   |
| --- | --- | ------------ | ----- | --- |
| **T**   | **T**   | **T**            | **T**     | **T**   |
| T   | F   | F            | T     |     |
| F   | T   | T            | F     |     |
| F   | F   | T            | F     |     |
The first row is critical row because all the premises are true, and the last column is conclusion.

==Definition 2.3.3== Modus tollens
$$
\begin{align}
&\text{ if p then q.} \\
& \neg q \\
\therefore &\neg p
\end{align}
$$
$p\to q$ is true and $\neg q$ is true. Since, $p\to q\equiv \neg q\to \neg p$ , thus $\neg q\to \neg p$ is also true, therefore $\neg p$ is true.

Note that the to apply modus ponens and modus tollens the statement must be an universal statement. Thus the proof should use Universal Instantiation.



A **rule of inference** is a form of argument that is valid. Thus modus ponens and modus tollens are both rules of inference

1. Generalization
$$
\begin{array}
\ p \\
\therefore p\lor q
\end{array}
$$
$$
\begin{array}
\ q \\
\therefore p\lor q
\end{array}
$$
2. Specialization
$$
\begin{array}
\ p\land q \\
\therefore p
\end{array}
$$
$$
\begin{array}
\ p\land q \\
\therefore q
\end{array}
$$
These argument forms are used for specializing. When classifying objects according to some property, you often know much more about them than whether they do or do not have that property. When this happens, you discard extraneous information as you concentrate on the particular property of interest.

Both generalization and specialization are used frequently in mathematics to tailor facts to fit into hypotheses of known theorems in order to draw further conclusions (转化为已知条件)

3. Elimination
$$
\begin{array}
\ p\lor q \\
\neg q \\
\therefore p
\end{array}
$$
4. Transitivity
$$
\begin{array}
\ p\to q \\
q\to r \\
\therefore p\to r
\end{array}
$$
Many arguments in mathematics contain chains of if-then statements. From the fact that one statement implies a second and the second implies a third, you can conclude that the first statement implies the third.


5. Proof by Division into Cases
^Division-into-case
$$
\begin{array}
\ p\lor q \\
p\to r \\
q\to r \\
\therefore r
\end{array}
$$

You list out all the possibility (Make sure they are _mutually exclusive_ and _collectively exhaustive_ — no overlaps and nothing left out), if you prove in either case a certain conclusion follows, then this conclusion must also be true. 

Formally, if you want to prove P, and you know:
1) One of these cases must happen
$$
Q_{1}\lor Q_{2}\lor Q_{3}\lor\dots \lor Q_{n}
$$
2) and for each $i,Q_{i}\to P$

Then we can conclude that P is true.



Given x is nonzero real number.
x is positive or x is negative.
if x is positive, $x^{2}>0$,
if x is negative, $x^{2}>0$,
$\therefore x^{2}>0$.

Question
You are about to leave for class in the morning and discover that you don’t have your glasses. You know the following statements are true:
a. If I was reading my class notes in the kitchen, then my glasses are on the kitchen table.
b. If my glasses are on the kitchen table, then I saw them at breakfast.
c. I did not see my glasses at breakfast.
d. I was reading my class notes in the living room or I was reading my class notes in the kitchen
.e. If I was reading my class notes in the living room then my glasses are on the coffee table.
Where are the glasses?

Fallacies
A fallacy is an error in reasoning that results in an invalid argument. Three common fallacies are using ambiguous premises, and treating them as if they were unambiguous, circular reasoning (assuming what is to be proved without having derived it from the premises), and jumping to a conclusion (without adequate grounds). In this section we discuss two other fallacies, called converse error and inverse error

Converse Error
$$
\begin{array}
\ p\to q \\
q \\
\therefore p
\end{array}
$$
the conclusion of the argument would follow from the premises if the premise $p\to q$ were replaced by its converse. Such a replacement is not allowed, however, because a conditional statement is not logically equivalent to its converse

Inverse Error
$$
\begin{array}
\ p\to q \\
\ \neg p \\
\therefore \neg q
\end{array}
$$

==Definition 2.3.4== An argument is called sound if, and only if, it is valid and all its premises are true. An argument that is not sound is called unsound.

==Contradiction Rule==
if you can show that the supposition that statement p is false leads logically to a contradiction, then you can conclude that p is true.
$$
\begin{array}
\ \neg p\to c \\
\therefore p
\end{array}
$$
# 2.4 Application: Digital Logic Circuits
