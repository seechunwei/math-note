
4.43 c)
**Part 1: Show that $B \subseteq C$**

Let $x$ be an arbitrary element of $B$ ($x \in B$). We must show that $x$ is also in $C$.

We consider two possible cases for $x$: it is either inside $A$ or outside $A$.

- **Case 1: $x \in A$**
    
    Since we know $x \in B$ and $x \in A$, then $x \in A \cap B$.
    
    We are given that $A \cap B = A \cap C$.
    
    Therefore, $x \in A \cap C$. By definition of intersection, this implies **$x \in C$**.
    
- **Case 2: $x \notin A$**
    
    Since $x \in B$, it is automatically true that $x \in A \cup B$.
    
    We are given that $A \cup B = A \cup C$.
    
    Therefore, $x \in A \cup C$. This means $x$ is in $A$ or $x$ is in $C$.
    
    Since we assumed in this case that $x \notin A$, it must be true that **$x \in C$**.
    

In both cases, $x \in C$. Thus, **$B \subseteq C$**.

**Part 2: Show that $C \subseteq B$**

This argument is symmetric to Part 1. Let $y$ be an arbitrary element of $C$ ($y \in C$).

- **Case 1: $y \in A$**
    
    Then $y \in A \cap C$. Since $A \cap C = A \cap B$, then $y \in A \cap B$, so **$y \in B$**.
    
- **Case 2: $y \notin A$**
    
    Then $y \in A \cup C$. Since $A \cup C = A \cup B$, then $y \in A \cup B$.
    
    Since $y \in A \cup B$ but $y \notin A$, it must be that **$y \in B$**.
    

In both cases, $y \in B$. Thus, **$C \subseteq B$**.

**Conclusion**

Since $B \subseteq C$ and $C \subseteq B$, we have proven that **$B = C$**. **Q.E.D.**

==Remark==
Analysis why we split the cases into $x \in A$ or $x \not\in A$. Because each condition tell you what if $x \in A$ and $x \not\in A$ respectively. The vein diagram should be $B,C$ is a big circle containing the small circle $A$.

4.45
Proof:
Suppose $x \in B$. Thus, $x=4q+3$ for some $q \in \mathbb{Z}$. Hence
$$
\begin{align}
x&=2(2q+1)+1 \\
x-1&=2(2q+1)
\end{align}
$$

Since $2q+1$ is an integer it follow that 
$$
x\equiv 1 \pmod{ 2} 
$$
Thus, $x \in A$. Hence $B \subseteq A$.

4.47
a) $n \in 2\mathbb{Z}$ and $n \equiv 2 \pmod{3}$
by Chinese remainder theorem

b)
Proof
Suppose $n \in A\cap B$, we need to show that $n^{2} \equiv 1 \pmod{ 12}$. Since $gcd(3,4)=1$. It follow that , we need to show $n^{2}\equiv 1\pmod{3}$ and $n^{2} \equiv 1 \pmod{ 4}$

Since $n \in A$ , it follow that $n^{2}\equiv 1 \pmod{3}$

Since $n \in B$, it follow that $n^{2}\equiv 1 \pmod{4}$
Thus, $n^{2}\equiv 1 \pmod{ 12}$

4.51
e




