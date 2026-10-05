In general, matrix multiplication is **non-commutative**, meaning $AB \neq BA$. However, there are specific conditions and special classes of matrices where commutativity holds.

For $AB = BA$ to even be possible, both $A$ and $B$ must be **square matrices** ($n \times n$) of the same dimension. Beyond that, here are the primary conditions:

---

## **1. Scalar and Identity Matrices**

The most trivial case is when one of the matrices is a multiple of the Identity matrix $I$.

- If $B = cI$ (where $c$ is a scalar), then $A(cI) = c(AI) = cA$ and $(cI)A = c(IA) = cA$.
    
- Therefore, **scalar matrices commute with all square matrices** of the same size.
    

## **2. Powers and Polynomials of the Same Matrix**

Matrices always commute with themselves and their own powers.

- $A^k A^m = A^m A^k = A^{k+m}$
    
- If $B$ is a polynomial function of $A$, such as $B = a_n A^n + \dots + a_1 A + a_0 I$, then $AB = BA$.
    

## **3. Diagonal Matrices**

If both $A$ and $B$ are **diagonal matrices**, they will always commute.

- Multiplying two diagonal matrices simply involves multiplying their corresponding diagonal entries. Since scalar multiplication is commutative ($a_{ii}b_{ii} = b_{ii}a_{ii}$), the matrices commute.
    

## **4. Simultaneous Diagonalizability**

This is a more advanced condition used in linear algebra proofs. Two diagonalizable matrices $A$ and $B$ commute **if and only if** they are **simultaneously diagonalizable**.

- This means there exists a single invertible matrix $P$ such that both $P^{-1}AP$ and $P^{-1}BP$ are diagonal matrices.
    
- In terms of eigenvectors: $A$ and $B$ commute if they share a **complete set of common eigenvectors**.
    

## **5. Inverse Matrices**

By definition, a square matrix $A$ commutes with its inverse $A^{-1}$:

$$AA^{-1} = A^{-1}A = I$$