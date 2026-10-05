Probability measures the likelihood that an event will occur.

A probability experiment is a process that leads to one of many results or outcomes, each with some possibility of occurring.

Sample Space
The set of all possible outcomes of a probability experiment is known as the sample space, denoted by S.

Sample Point 
Each possible outcome of a statistical experiment is an element of the sample space and is therefore called a sample point.

A tree diagram is a display that shows all possible outcomes of a probability experiment.

Events
An event is any subset of the sample space. It may contain one, some, or none of the outcomes in the sample space

- If an event contains only one sample point, it is called a simple event.
- contains two or more sample points is known as a compound event.
- A null event, denoted by $\emptyset$, contains no sample points (or is empty).


#### 4.2 Set Operations with Events

1) The union of events A and B, denoted by $A\cup B$, is the set of all sample points in S that belong to event A, event B, or both.

2) The intersection of events A and B, denoted by $A\cap B$, is the set of all sample points in S that belong to both event A and event B.

3) Each time an experiment is performed, one and only one outcome will result. Thus, all outcomes of an experiment are mutually exclusive. If two event is mutually exclusive, then that is impossible for both event to happen at the same time.
	Mutually exclusive events are events whose intersection is the null space, i.e., if event A and event B are mutually exclusive, then $A\cap B=\emptyset$.


4) The complement of event A (with respect to S), denoted by A' (or $\bar{A}$), is the set of all sample points in S that do not belong to event A.

5) A partition of the sample space Si s a set of events A1, A2,....., An such that the following two conditions are true:
- $A_{i}\cap A_{j}=\emptyset$ for $i,j \in \{ 1,2,3,\dots,n \}$ $i\neq j$
- $(A_{1}\cup A_{2}\cup\dots \cup A_{n})=S$

#### 4.3 Concept of Probability of Events
The probability of an event may be obtained in three different ways:
-Empirically
-Theoretically
-Subjectively

A. Empirical (or Experimental ) Probability
- An empirical probability is the observed relative frequency with which an event occurs.
- $P(A)=\dfrac{n(A)}{n}$ 

$P(H)=\dfrac{1}{2}$
This does not mean exactly one head will occur in every two tosses of the coin. It means that, in the long run, the proportion of times that a head will occur is approximately $\dfrac{1}{2}$


Long-run behavior:
graph of the relative frequency versus number of trials,

cumulative relative frequency of occurrence of a head versus number of trials.

Law of Large Numbers
If the number of times an experiment is repeated is increased, the ratio of the number of successful occurrences to the number of trials will tend to approach the theoretical probability of the outcome for an individual trial

2) Theoretical Probability
- Uses a sample space S where all sample points are equally likely to occur
- The probability of an event A is the ratio of the number of sample points in set A to the number of sample points in S.
- $P(A)=\dfrac{n(A)}{n(S)}$

3) Subjective Probability
Suppose the elements of a sample space are not equally likely, and empirical probabilities cannot be used. The only method available for assigning probabilities to events may be by personal judgment.


Probabilities as Odds
Another way of expressing probabilities is by using odds. If the odds in favour of an event A are a to b, then:
1) The odds against A are b to a
2) The probability of event A is: $P(A)=\dfrac{a}{a+b}$


#### 4.4 Properties of Probability
1) The probability of any event A, denoted by P(A), is the summation of the probabilities of all the sample points in A
$$
0\leq P(A)\leq 1
$$if $A=\emptyset$ , then $P(A)=0$ , 
if $A=S$ , then $P(A)=1$

#### 4.5 Rules of Probability

All conditional event are independence event 

$$
P(A\mid B)=\frac{P(A\cap B)}{P(B)}
$$
The probability of an event A given event B has occurred. It means that both event have already occurred and the total number of experiment become the sample point in event B 

Note that if $A$ depend on $B$ then $B$ depend on $A$.
Proof:
Suppose  $A$ and $B$ are non-empty set and $A$ depend on $B$. Thus,
$$
P(A|B)=\frac{P(A\cap B)}{P(B)}
$$
Thus,
$$
\begin{align}
P(B|A)&=\frac{P(B\cap A)}{P(A)} \\
&=\frac{P(A|B)\times P(B)}{P(A)}
\end{align}
$$
Since $P(A|B)\neq P(A)$ it follow that $P(B|A)\neq P(B)$. 


General multiplication rule
To find the probability that **A, B, and C all occur**:

1. Find the chance that A happens.
2. Then, given A happened, find the chance B happens.
3. Then, given both A and B happened, find the chance C happens.
4. Multiply all three together.
$$
P(A\cap B\cap C)=P(A)\times P(B \mid A)\times P(A\cap B\mid C)
$$

Since, $P(A\mid B)\neq P(B\mid A)$ . Thus, the order is important in conditional probability.

The conditional probabilities are **based on what comes before**. If we switch the order, we must **change the conditioning** accordingly.

General addiction rule is under the assumption that it is not mutually exclusive

General multiplication rule is under the assumption that it is dependent event (conditional probability)


#### 4.7 Bayes' Rule

If the set of events A1, A2, ....., An constitutes a partition of the sample space S, and event B is a subset of S, then
$$
\begin{array}
\ B=B\cap S= B\cap(A_{1}\cup A_{2}\cup\dots \cup An) \\
=(B\cap A_{1})\cup(B\cap A_{2})\dots \cup(A\cap A_{n})
\end{array}
$$

$P(B)=P(A_{1})P(B|A_{1})+P(A_{2})P(B|A_{2})+\dots$

The probability of event A given B, C, D which $S=B\cup C\cup D$ . It means that B, C, D is all the possible condition. Event A is a subset of S, thus $A=A\cap S=$ 
In this case, we can calculate $P(A)$ using Bayes' rule



Explain why nonempty, mutually exclusive events A and B must be dependent.

We assume the statement is true. 
Let A and B be an arbitrary nonempty, mutually exclusive event. It is suffices to prove that A and B must be dependent.

By definition, 
$$\begin{align}
P(A\cap B)&=P(A)\cdot P(B) \\
&=0
\end{align}
$$
By zero product property, I's either P(A) or P(B) is 0.  Thus, either A or B is empty events. But, we told A and B are non-empty events. Contradiction occurred. Hence, A and B are dependent.

Intuitive explanation
Suppose A and B are mutually exclusive events, if A happen , then B didn't happen. So $P(B\mid A)=0$

Example:
A: Roll a 2 on a die
B: Roll a 6 on die

$$
P(B\mid A)=0\neq P(B)=\frac{1}{6}
$$



We toss 3 coins and to see how many head we get? (with the assumption that each iteration is independent)

$A=\{ 0,1,2,3 \}$, why cannot list out like this because there are not equally likely to occur. For example, $A_{0}=\{ H H H \}$, and $A_{1}=\{ HTT,THT,TTH \}$



#### Fundamental principle of counting

- deals with the counting of sample points in a sample space. Also known as the **multiplication rule for choices**


>If an operation can be performed in n1 ways, and for each of these a second operation can be performed in n2 ways, and for each of the latter a third operation can be performed in n3 ways,......, and for each of the latter a kth operation can be performed in nk ways, then the entire sequence of k operations can be performed in n1n2n3.... nk ways.

#### Permutations and Combinations

permutation is an ordered arrangement of every or some elements of a set of objects. Order is important in a permutation; therefore, permutations with the same objects in a different order are considered distinct arrangements.

