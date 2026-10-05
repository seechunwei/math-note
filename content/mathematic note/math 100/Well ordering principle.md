To prove the **Principle of Mathematical Induction (PMI)** using the **Well-Ordering Principle (WOP)**, we use a technique called **proof by contradiction**.

This proof is fundamental in discrete mathematics because it shows that these two concepts are logically equivalent; if you accept the Well-Ordering Principle as an axiom of the integers, Mathematical Induction is a necessary consequence.

Here is the step-by-step proof.

---

### 1. Definitions

Before starting, let's clearly state the two principles we are working with.

- **The Well-Ordering Principle (WOP):** Every non-empty set of positive integers (natural numbers) has a least (smallest) element. (Suppose that S is a nonempty set containing integers all of which are greater than some fixed integer. Then S has a least element)

$$
\forall S \subseteq \mathbb{N},[S\neq \emptyset\to \exists m \in S \text{ s.t }\forall x \in S, m\leq x]
$$


- The Principle of Mathematical Induction (PMI):
    
    Let $P(n)$ be a statement about the integer $n$. If:
    
    1. **Base Case:** $P(1)$ is true.
        
    2. **Inductive Step:** For all $k \ge 1$, if $P(k)$ is true, then $P(k+1)$ is true.
        
    
    Then $P(n)$ is true for all integers $n \ge 1$.
    

---

### 2. The Proof

We will assume that the conditions of Mathematical Induction are met, but the conclusion is false. We will then show that this assumption leads to a contradiction using the Well-Ordering Principle.

#### Step 1: Assume the Hypothesis

Assume that for a proposition $P(n)$:

1. $P(1)$ is true.
    
2. For all $k \ge 1$, $P(k) \implies P(k+1)$.
    

#### Step 2: Assume the Conclusion is False (Contradiction Setup)

Assume that $P(n)$ is **not** true for all $n \ge 1$.

#### Step 3: Construct the Set of Counterexamples

Let $S$ be the set of all positive integers for which $P(n)$ is false.

$$S = \{ n \in \mathbb{Z}^+ \mid P(n) \text{ is false} \}$$

Because we assumed in Step 2 that $P(n)$ is not true for all $n$, the set $S$ must be **non-empty**.

#### Step 4: Apply the Well-Ordering Principle

Since $S$ is a non-empty set of positive integers, by the **Well-Ordering Principle**, $S$ must contain a **least element**. Let's call this least element $m$.

This means:

- $P(m)$ is false (because $m \in S$).
    
- For any integer $x < m$, $P(x)$ is true (because $m$ is the _smallest_ failure).
    

#### Step 5: Analyze the Least Element $m$

Now we check if $m$ could be the base case.

- We know $P(1)$ is true (from our hypothesis in Step 1).
    
- Since $P(m)$ is false, $m$ cannot be equal to $1$.
    
- Therefore, **$m > 1$**.
    

#### Step 6: Derive the Contradiction

Since $m > 1$, the number $m - 1$ is a valid positive integer.

Because $m - 1 < m$, and $m$ is the least element in the set of falsehoods ($S$), $m - 1$ cannot be in $S$.

- Therefore, **$P(m - 1)$ is true.**
    

Now, apply the **Inductive Step** hypothesis (from Step 1):

- We know that if $P(k)$ is true, then $P(k+1)$ is true.
    
- Let $k = m - 1$.
    
- Since $P(m - 1)$ is true, then $P((m - 1) + 1)$ must be true.
    
- Simplifying, this means **$P(m)$ is true.**
    

#### Step 7: The Contradiction

We have arrived at two contradictory statements:

1. $P(m)$ is false (because $m \in S$).
    
2. $P(m)$ is true (implied by $P(m-1)$ and the inductive step).
    

This is a logical contradiction.

---

### 3. Conclusion

The contradiction arose because we assumed that the set $S$ was non-empty (i.e., that $P(n)$ fails for some integers).

Therefore:

1. The assumption that $S$ is non-empty must be false.
    
2. $S$ must be an empty set.
    
3. There are no integers for which $P(n)$ is false.
    
4. **$P(n)$ is true for all $n \ge 1$.**
    

Q.E.D.

---

### Summary of Logic

| **Concept**   | **Role in Proof**                                                                                                              |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| **Set $S$**   | Represents "The set of numbers that break the rule."                                                                           |
| **WOP**       | Guarantees that if rules are broken, there is a _first_ number ($m$) that breaks them.                                         |
| **Induction** | Guarantees that if the rule works for the number before ($m-1$), it must work for the number after ($m$).                      |
| **Conflict**  | The "first number to break the rule" cannot exist because the induction step would have fixed it based on the previous number. |

To prove the **Well-Ordering Principle (WOP)** using the **Principle of Mathematical Induction (PMI)**, we typically use the **contrapositive** approach.

Instead of directly proving "Every non-empty set has a least element," we prove the logically equivalent statement: **"If a set has _no_ least element, it must be empty."**

Here is the step-by-step proof.

---

### 1. The Setup

We start by defining a set $S$ of positive integers ($\mathbb{Z}^+$) that has no least element.

Our goal is to prove that $S$ is the empty set (i.e., it contains no numbers).

To do this using Induction, we define a proposition $P(n)$ as follows:

$$P(n): \text{"The integer } n \text{ is not in } S. \text{"}$$

However, standard induction works best here if we strengthen the statement slightly to include all previous numbers. Let's define $Q(n)$ as:

$$Q(n): \text{"None of the integers } 1, 2, ..., n \text{ are in } S. \text{"}$$

If we can prove $Q(n)$ is true for all $n$, then no integer exists in $S$, making $S$ empty.

---

### 2. The Proof

#### Step 1: The Base Case ($n = 1$)

We need to check if $Q(1)$ is true. This means determining if $1 \in S$.

- We know $1$ is the smallest positive integer.
    
- If $1$ were in $S$, it would automatically be the **least element** of $S$ (since no positive integer is smaller than 1).
    
- However, our premise is that $S$ has **no least element**.
    
- Therefore, $1$ cannot be in $S$.
    

Thus, $Q(1)$ is **true**.

#### Step 2: The Inductive Step

Hypothesis: Assume $Q(k)$ is true.

This means: $1, 2, ..., k \notin S$. (None of the numbers from 1 to $k$ are in $S$).

Goal: Prove $Q(k+1)$ is true.

We need to determine if $k+1$ is in $S$.

Consider the integer $k+1$:

1. From our hypothesis, we know the numbers $1, 2, ..., k$ are **not** in $S$.
    
2. If $k+1$ **were** in $S$, it would be the smallest integer in $S$ (because all smaller integers are excluded).
    
3. But $S$ has **no least element**.
    
4. Therefore, $k+1$ cannot be in $S$.
    

Since $k+1 \notin S$, and we already knew $1...k \notin S$, the statement $Q(k+1)$ is true.

#### Step 3: Conclusion

By the Principle of Mathematical Induction, $Q(n)$ is true for all $n \ge 1$.

- This means for every positive integer $n$, $n \notin S$.
    
- Therefore, $S$ contains no elements.
    
- **$S$ is the empty set.**
    

---

### 3. Final Logic Connection

We have proven: **"If a set $S$ has no least element, then $S$ is empty."**

The logical contrapositive of this statement is:

"If set $S$ is not empty, then $S$ has a least element."

This is exactly the definition of the **Well-Ordering Principle**. Q.E.D.

---

### Summary of Differences

It is helpful to see how the logic flows in both directions:

| **Proof Direction** | **Logic Used** | **Key Mechanism**                                                                                                      |
| ------------------- | -------------- | ---------------------------------------------------------------------------------------------------------------------- |
| **PMI using WOP**   | Contradiction  | Assume a set of "failures" exists; WOP finds the _first_ failure, which contradicts the induction step.                |
| **WOP using PMI**   | Contrapositive | Assume a set has no "first" element; Induction shows that if you can't start, you can't exist (the set must be empty). |


The PMI and WOP is the fundamental structure of the natural numbers ($\mathbb{N}$). which is the set of $\{ 1,2,3,\dots,n \}$

Mathematical induction is like building a ladder from $P(1)\to P(2)\to\dots\to P(n)$. $P(1)$ here is the starting point which is floor, if $P(1)$ is true and if $P(n)$ is true then $P(n+1)$. Thus $P(n)$ is true for all integer $n\geq 1$


The well ordering principle is like grab a set of failure and there must exists a smallest failure because the natural integer start from 1 which is the floor. 

==Proof of QR Theorem==
For any integer $a$ (the dividend) and any positive integer $d$ (the divisor), there exist integers $q$ (quotient) and $r$ (remainder) such that:

$$a = dq + r \quad \text{and} \quad 0 \le r < d$$
We will use WOP to prove the existence part of this theorem. Notice that WOP is for non empty set for positive integer and $r\geq 0$ fit the property of WOP that it has a floor(least element). Thus, we start by defined all the possible r in a set.

Let S defined as the set that containing all possible non-negative numbers of $r$.

Suppose $a$ is an arbitrary integer and $d$ is an arbitrary positive integer. 
$$
S=\{ a-dq \mid q \in \mathbb{Z} \text{ and } a-dq\geq 0 \}
$$
Notice that $S \in \mathbb{Z}$ but we cannot apply WOP to find the least r in this set because we need to show that $S$ is exist for any $a$ and $d$.(Show $S$ is not an empty set)
Thus, we need to split $a$ into 2 cases.

Case 1: $a\geq0$
Let $q=0$. Then $a-d(0)=a$. Since $a\geq 0$, this value is in $S$.

Case 2: $a< 0$ . (We need to choose a more negative value q to make it positive)
Let $q=a$. Then, $a-d(a)=a(1-d)\geq  0$ , this value is in $S$

In either case, $S$ is nonempty set. Thus, by WOP $S$ contain a least element, say $r$.

By the definition of $S$ we know that $r\geq 0$ and $r=a-dq$ for some integer $q$.

Now we need to show that $r<d$. We argue by contradiction.
Assume $r\geq d$ and let $r'=r-d$
$$
\begin{align}
r-d&\geq 0 \\
a-dq-d&\geq 0 \\
a-d(q-1)&\geq 0
\end{align}
$$
Since $r-d\geq 0$, Thus, $r'\geq 0$ and since $q-1$ is integer thus $r'\in S$ . Notice that $r'<r$ , thus $r'$ is the least element in $S$ which contradict the fact that $r$ is the least element in $S$.

(We already proved the uniqueness part in Section 4.5.)
[Problem Solving for Proofs: Division Algorithm Proof Idea (use Well-Ordering Principle)](https://www.youtube.com/watch?v=cC7hPTyrGu4)

---
### Related Architecture
- [[Logical Architecture from WOP to FTA]] — Master logical chain connecting WOP, Mathematical Induction, Remainder Theorem, Euclidean Algorithm, Bézout's Identity, Euclid's Lemma, and FTA.
