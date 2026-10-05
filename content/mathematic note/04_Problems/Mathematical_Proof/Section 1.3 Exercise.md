1.23
$A=\{ 1,2,3,4,5,6 \}$
$B=\{ 1,2,3,7,8,9 \}$

$A-B=\{ 4,5,6 \}$
$B-A=\{ 7,8,9 \}$
$A\cap B=\{ 1,2,3 \}$
Cardinality of these 3 set are 3.

1.24
$A=\{ 1 \}$
$B=\{ 1,2 \}$
$C=\{ 2 \}$

Thus, $B\neq C$ but $B-A=C-A$


Why this happen
The delete is not like minus, if $A\cap B=\emptyset$ , then $A-B=A$. Thus, it is a neutral move that do nothing.

1.25
a)$A=\{ 1 \}$ $B=\{ \{ 1 \} \}$ $C=\{ 1,2 \}$

in and subset are different concept , in means the whole set is an element , subset means the element is in another set. Which mean that, in is with braces and subset is without braces.

1.30
a)
$A=\{ x \in \mathbb{R}|-1\leq x\leq 3 \}$
$A=[-1,3]$
$B=(-\infty,-1]\cup[1,\infty)$
$C=[-5,1]$

$A \cup B=(-\infty,\infty)$
$A\cap B=\{ -1 \}\cup[1,3]$
$B\cap C=[-5,-1]\cup \{ 1 \}$
$B-C=(-\infty,-5)\cup(1,\infty)$

1.31
$A\cup B=\{ 1,2 \}$
$C\cap D=\{ 2,3 \}$
$A\cap C=\{ 1,2 \}$
$B\cup D=\{ 2,3 \}$

$A=\{ 1,2 \}$
$C=\{ 1,2,3 \}$
$D=\{ 2,3 \}$
$B=\emptyset$
More general 
$B\subseteq \{ 1,2 \}\cap \{ 2,3 \}$
$B\subseteq \{ 2 \}$

intersection reveal the lower boundary , union reveal the upper boundary

$A \cap C\subseteq A\subseteq A\cup B$
Thus, $\{ 1,2 \}\subseteq A\subseteq \{ 1,2 \}$
Thus, $A=\{ 1,2 \}$

$C\cap D\subseteq D\subseteq B\cup D$
Thus, $\{ 2,3 \}\subseteq D\subseteq \{ 2,3 \}$
$D=\{ 2,3 \}$

$C \cap D \subseteq C$ and $C \cap A \subseteq C$
$\{2, 3\} \subseteq C$ and $\{1, 2\} \subseteq C$
Thus, $C=\{ 1,2,3 \}$

$B\subseteq \{ 1,2 \}\cap \{ 2,3 \}$
$B\subseteq \{ 2 \}$

1.32
$A_{i}\cap A_{j}$ such that $i \neq j$ are different $i,j \in \{ 1,2,3,4 \}$
$U=\{ a,b,c,d \}$
So total got 4 set. All intersections of two subsets are different. Thus, $\binom{4}{2}=6$, We need to have 6 distinct intersection.

Since $A_{i}\cap A_{j}\subseteq \{ a,b,c,d \}$ and the intersection are different. 
Suppose $|A_{i}|=2$
Thus, $A_{i}\cap A_{j}$ are permutation of $\{ a,b,c,d,\emptyset \}$ 
But notice that there are only 5 distinct intersection

Thus we need to take $|A_{i}|=3$

Thus, 
$A=\{ a,b,c \}$
$B=\{ b,c,d \}$
$C=\{ c,d,a \}$
$D=\{ d,a,b \}$

![[Pasted image 20260118131725.png]]

1.33
$A=\{ 1 \}$
$B=\{ 2 \}$
Thus the $P(\{ 1,2 \})=\{ A\cap B,A-B,B-A,A\cup B \}$
$=\{ \emptyset,\{ 1 \},\{ 2 \},\{ 1,2 \} \}$

This is a elegance way to express $P(\{ a,b \})$ where $|A|=1$ and $|B|=1$ and $A\cap B=\emptyset$


1.34
Given $U=\{ 1,2,3 \}$
$A\cup B$, $A\cup \bar{B},\bar{A}\cup B,A\cap B,\bar{A}\cap B,A\cap \bar{B}$
 are different 
 Example:
$A=\{ 1 \}$
$B=\{ 2 \}$

==Remark==
Imagine the vein diagram $A$ and $B$ within $U$. Thus, there are 4 fundamental region which form the 8 regions(question) by combination.
1) $A\cap B$
2) $A\cap \bar{B}$(only A)
3) $\bar{A}\cap B$ (only $B$)
4) $\bar{A}\cap \bar{B}$ (neither)

For example, $A\cup \bar{B}=(A\cap \bar{B}) \cup(\bar{A}\cap \bar{B})$

Thus, to make sure the 8 region is distinct we need to ensure the $4$ region is distinct which is the permutation of $\{ \emptyset,1,2,3 \}$.

Minimum Requirement for $U$

Because you need at least 3 non-empty regions, and each region must contain at least one element:

The Universal Set $U$ must have at least 3 elements ($|U| \ge 3$).

The cardinality of $P(\{ a,b,c \})$ is $2^{3}=8.$ That means there is 8 subset(region) that are different. Notice that these subset is actually correspondence with the region in vein diagram. Thus, we can construct the subset with the operation of 4 fundamental region


Now we are thinking how to construct a power set with different cardinality of set, and what is the relationship between the number of distinct non empty region

$|P(\{ a,b \})|=4$
We need to construct 4 distinct subset, to do so how many region is enough, 

$A=\{ 1 \}$
$B=\{ 2 \}$
We need 2 set to construct though combination (these 2 set have 2 distinct non empty region )

$|P(\{ a,b ,c\})|=8$
We need 2 set to construct but this time we need 3 distinct non empty region. Thus,
$A=\{ 1,2 \}$
$B=\{ 2,3 \}$

Thus, we need $\log_{2}|P(A)|$ distinct non empty region to construct power set

For $4\leq|A|\leq 7$. We can use 3 set to construct. Because we can use 3 set to construct maximum 7 different non empty region


How about $|A|=5$. Then we need 5 distinct non empty region using 3 set
![[set.png]]

For example
- **Set A** (contains 1, 4, 5):
$$A = \{ 1, 4, 5 \}$$
- **Set B** (contains 2, 4):
$$B = \{ 2, 4 \}$$
- **Set C** (contains 3, 5):
$$C = \{ 3, 5 \}$$
With $N$ starting sets, you can generate the Power Set for a cardinality of up to **$2^N - 1$**.




