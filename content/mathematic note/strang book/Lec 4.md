Inverse of matrix $AB$, $A^{T}$
Cost of elimination
Product of elimination matrix $A=LU$
Permutation matrix


### Inverse of matrix $AB$, $A^{T}$

We say a matrix $A$ is invertible iff

$$
AA^{-1}=I=A^{-1}A
$$

(It is also equivalent of saying a square matrix have every pivot in the row$\to$ every pivot in column$\to$ no free variable $\to$ Solution of $Ax=b$ is unique)

Thus, we need to find a matrix where 
$$
AB()=I=()AB
$$

Naturally we will think about does it consists of each of the inverse which is $A^{-1}$ and $B^{-1}$? If yes what is the order to satisfy the condition? 

Think like the process of wearing the shoe ,
1) First we need to wear the socks 
2) Second, we wear the shoe. 

What if we want to take out the shoes?
1) First, we take off the shoe
2) Second, we take off the socks

Notice that it is reverse order, so do the inverse of $AB$.

$$
AB(B^{-1}A^{-1})=I=(B^{-1}A^{-1})AB
$$The fact that we can move around the parenthesis make this easy to understand. 

#### What about the inverse of transpose

$$
\begin{align}
AA^{-1}&=I \\
(A^{-1})^{T}A^{T}&=I
\end{align}
$$

It is the same idea as inverse of $AB$. (reverse order)m but why?


To prove $AB=B^{T}A^{T}$, we need to prove that every entry of them are same. Suppose $A$ is a $m\times n$ matrix and $B$ is a $n\times p$ matrix.

Thus,

$$
(AB)_{ij}=\sum_{k=1}^{n}a_{ik}b_{kj} 
$$

By the definition of a **transpose**, the $(i, j)$ entry of $(AB)^T$ is the $(j, i)$ entry of $AB$. Therefore:

$$
((AB)^{T})_{ij}=(AB)_{ji}=\sum_{k=1}^{n}a_{jk}b_{ki} 
$$

Now, let’s look at the entry in the $i$-th row and $j$-th column of $B^T A^T$. By the definition of matrix multiplication:

$$
(B^{T}A^{T})_{ij}=\sum_{k=1}^{n} (B^{T})_{ik}(A^{T})_{kj}
$$

Using the definition of the transpose again ($(M^T)_{ab} = M_{ba}$):

- $(B^T)_{ik} = b_{ki}$
    
- $(A^T)_{kj} = a_{jk}$

Substituting these back into the summation:

$$(B^T A^T)_{ij} = \sum_{k=1}^n b_{ki} a_{jk}$$

Since scalar multiplication is commutative ($B_{ki} A_{jk} = A_{jk} B_{ki}$), we have:

$$(B^T A^T)_{ij} = \sum_{k=1}^n a_{jk} b_{ki}$$

Q.E.D


#### Go back to the question
$$
\begin{align}
AA^{-1}&=I \\
(A^{-1})^{T}A^{T}&=I
\end{align}
$$

So what is the inverse of $A^{T}$. From the equation above we know that 
$$
(A^{-1})^{T}
$$
is the inverse for $A^{T}$.


### Product of elimination matrix $A=LU$

Suppose a good matrix $A$, no row exchange, all pivot is non zero, i can perform a sequence of row operation to reach $U$.

So the question is what is the relation between $A$ and $U$.

Suppose 
$$
A=\begin{bmatrix}
2 & 1 \\
8 & 7
\end{bmatrix}
$$
Thus,

$$
E_{21}A=\begin{bmatrix}
1 & 0 \\
-4 & 1
\end{bmatrix}\begin{bmatrix}
2 & 1 \\
8 & 7
\end{bmatrix}=\begin{bmatrix}
2 & 1 \\
0 & 3
\end{bmatrix}=U
$$

Since $E_{21}$ is invertible, thus there exist a matrix $L=E_{21}^{-1}$ such that

$$
A=LU
$$
Thus, we want to find such $L$ (lower triangle matrix)

What is the inverse of each row operation?

The inverse of 
$R_{1}(\alpha)$ is $R_{1}\left( \frac{1}{\alpha} \right)$
$R_{1}^{2}$ is $R_{2}^{1}$
$R^{1}_{2}(\alpha)$ is $R_{2}^{1}(-\alpha)$

Thus,
$$
A=\begin{bmatrix}
1 & 0 \\
4 & 1
\end{bmatrix}\begin{bmatrix}
2 & 1 \\
0 & 7
\end{bmatrix}
$$


And notice that is a product of lower triangle and upper triangle.

Notice that we can also separate the pivots

$$
A=A=\begin{bmatrix}
1 & 0 \\
4 & 1
\end{bmatrix}\begin{bmatrix}
2 & 0 \\
0 & 7
\end{bmatrix}\begin{bmatrix}
1 & \frac{1}{2} \\
0 & 1
\end{bmatrix}
$$

The third matrix come from divide the row by first non zero entry. This is called
$$
A=LDU
$$
---
How about $3\times{3}$ matrix?

Suppose  no row exchange , since we know the step we can assume a sequence of row operation

$$
E_{32}E_{31}E_{21}A=U
$$$$
A=E_{21}^{-1}E_{31}^{-1}E_{32}^{-1}U=LU
$$
The $L$ which is the inverse is better than the row operation matrix. Why?

Suppose we no need $E_{31}$ for the sake of simplicity.

$$
\begin{align}
E_{32}E_{21}&=\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & -5 & 1
\end{bmatrix}\begin{bmatrix}
1 & 0 & 0 \\
-2 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix} \\
&=\begin{bmatrix}
1 & 0 & 0 \\
-2 & 1 & 0 \\
10 & -5 & 1
\end{bmatrix}
\end{align}
$$

Notice that each entry of new matrix form by combining each entry of $E_{32}$ and $E_{21}$ except 10. Where the 10 come from? $-2\times-5=10$. 

This happen because, we subtract 2 row 1 from row 2. Then, we subtract 5 row 2 from row 3. Notice that the row 2 had been change before row 3 change. 


Thus, when we combine 2 operation together it is equal to 10 row 1-5 row 2+ row 3. Think of the part that subtract 2 row 1 have been separated and multiply with -5 and apply to row 3.

#### Now lets consider the inverse

$$
E_{21}^{-1}=\begin{bmatrix}
1 & 0 & 0 \\
2 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix}
$$
and 

$$
E_{32}^{-1}=\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 5 & 1 \\
\end{bmatrix}
$$

Since $(AB)^{-1}=B^{-1}A^{-1}$. Thus,

$$
\begin{align}
(E_{32}E_{21})^{-1}&=E_{21}^{-1}E_{32}^{-1} \\
&=\begin{bmatrix}
1 & 0 & 0 \\
2 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix}\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 5 & 1 \\
\end{bmatrix} \\
&=\begin{bmatrix}
1 & 0 & 0 \\
2 & 1 & 0 \\
0 & 5 & 1
\end{bmatrix}
\end{align}
$$

Notice that each entry of new matrix form by combining each entry of 2 inverse matrix. This happen because no row operation interfere each other. We change row 3 from row 2 and then we change row2 from row 1.

The multipliers`i j(taken from elimination)are below the diagonal.

From A to U there are subtractions of rows. From U to A there are additions of rows.

==Conclusion==
$$
A=LU
$$
if no row exchanges, the multiplier go directly to $L$. 

$L$ is the inverse matrix of the product of row operations.

$EA=U$
$LEA=LU$
$A=LU$ since $E$ is the inverse of $L$.

[[2.2 exercise  Lay#^be07a8]]
## 1. The Core Idea: $A = LU$

The text explains that if you take a matrix $A$ and perform elimination to get it into its upper triangular form $U$, the matrix $L$ "brings back" $A$.

In formula (7), you see:

$$A = \begin{bmatrix} 1 & 0 & 0 \\ \ell_{21} & 1 & 0 \\ \ell_{31} & \ell_{32} & 1 \end{bmatrix} \begin{bmatrix} \text{row 1 of } U \\ \text{row 2 of } U \\ \text{row 3 of } U \end{bmatrix}$$

- **The Multipliers ($\ell_{ij}$):** These are the exact numbers you used during elimination. For example, $\ell_{21}$ is the multiplier used to subtract a multiple of row 1 from row 2 to create a zero in the $(2,1)$ position. (the inverse we just add back the same multiplier)

![[Pasted image 20260528161256.png]]
(The inverse of elementary row operation didn't interfere each other)


Why the diagonal of $L$ is 1?
It is because is the reverse of row operation which remain the row and added by multiple of another row.

### Cost of elimination
[[1.3   An Example of Gaussian Elimination]]

### Permutation

### The 6 Permutation Matrices

These are categorized by how they "shuffle" the standard basis vectors.

#### 1. The Identity (No Permutation)

The identity matrix leaves all rows in their original order.

$$P_1 = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix}$$

#### 2. Row Exchanges (Swapping Two Rows)

These matrices swap two rows while leaving one row fixed.

- **Swap Row 1 and Row 2:**
    
    $$P_2 = \begin{bmatrix} 0 & 1 & 0 \\ 1 & 0 & 0 \\ 0 & 0 & 1 \end{bmatrix}$$
    
- **Swap Row 1 and Row 3:**
    
    $$P_3 = \begin{bmatrix} 0 & 0 & 1 \\ 0 & 1 & 0 \\ 1 & 0 & 0 \end{bmatrix}$$
    
- **Swap Row 2 and Row 3:**
    
    $$P_4 = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 0 & 1 \\ 0 & 1 & 0 \end{bmatrix}$$
    

#### 3. Cyclic Permutations (Shifting All Rows)

These matrices shift every row to a new position.

- **Shift Rows (1→2, 2→3, 3→1):**
    
    $$P_5 = \begin{bmatrix} 0 & 0 & 1 \\ 1 & 0 & 0 \\ 0 & 1 & 0 \end{bmatrix}$$
    
- **Shift Rows (1→3, 3→2, 2→1):**
    
    $$P_6 = \begin{bmatrix} 0 & 1 & 0 \\ 0 & 0 & 1 \\ 1 & 0 & 0 \end{bmatrix}$$

Notice that if we multiply any 2 matrix in the list, the result is still in the list. (It is a group!!!)

We have identity matrix
We have the inverse, for 1-4 the inverse is themself , 5 and 6 is inverse for each other

$$
P^{-1}=P^{T}
$$

---
If $4\times{4}$ matrix how many $P$. The answer is 24