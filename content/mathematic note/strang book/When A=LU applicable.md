
$A=LU$ is not only applicable for invertible matrix.
## 1. Square Invertible Matrices

For an $n \times n$ invertible matrix, $A = LU$ exists if and only if all leading principal minors are non-zero (i.e., you don't need to swap rows).

- **$L$**: Lower triangular with 1s on the diagonal (unit lower triangular).
    
- **$U$**: Upper triangular with **non-zero** entries on the diagonal (the pivots).
    

---

## 2. Square Singular (Non-Invertible) Matrices

If a square matrix is singular, you can still perform Gaussian elimination to reach an upper triangular form.

- **$U$**: Will have at least one **zero** on the diagonal.
    
- **$L$**: Remains a unit lower triangular matrix.
    
- **Example**: If the first column is all zeros, the first "pivot" is zero. While a pure $LU$ might fail here without row swaps ($PA = LU$), the concept of $U$ being the result of elimination still holds.
    

---

## 3. Rectangular Matrices ($m \times n$)

The $LU$ decomposition is also widely used for non-square matrices. If $A$ is an $m \times n$ matrix:

- **$L$**: Is an $m \times m$ unit lower triangular matrix.
    
- **$U$**: Is an $m \times n$ upper trapezoidal matrix (the Row Echelon Form).
    

This is particularly useful in finding the **basis for the Null Space** or solving underdetermined systems.