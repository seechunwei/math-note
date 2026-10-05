In linear algebra, both terms describe a relationship between two matrices, but **"row equivalent"** is a stricter condition than just being **"equivalent."** Here is the breakdown of the difference:

### 1. Row Equivalent (Strict Relationship)

Two matrices, $A$ and $B$, are **row equivalent** if you can transform $A$ into $B$ using a sequence of **strictly elementary row operations** (swapping rows, multiplying a row by a non-zero scalar, or adding a multiple of one row to another).

- **Mathematical Definition:** $A$ and $B$ are row equivalent if there exists an invertible matrix $P$ such that $B = PA$.
    
- **What it means in practice:** They represent the same system of linear equations. If you are solving $Ax = 0$ and $Bx = 0$, both systems will yield the exact same solutions.
    
- **What is preserved:** * The **Row Space** (the span of the row vectors) is identical.
    
    - The **Null Space** (the set of all solutions) is identical.
        
    - The row rank is the same.
        

### 2. Equivalent (Looser Relationship)

Two matrices, $A$ and $B$, are simply **equivalent** if you can transform $A$ into $B$ using a sequence of elementary row operations **AND/OR elementary column operations**.

- **Mathematical Definition:** $A$ and $B$ are equivalent if there exist invertible matrices $P$ and $Q$ such that $B = PAQ$.
    
- **What it means in practice:** They do _not_ necessarily represent the same system of equations anymore, because column operations mix up the variables (e.g., swapping column 1 and column 2 swaps the $x$ and $y$ variables).
    
- **What is preserved:** * Only the **Rank** (the dimension of the vector space spanned by its rows or columns) is preserved.
    
    - The actual row space and null space will likely change.
        

---

### Summary Comparison

|**Feature**|**Row Equivalent**|**Equivalent**|
|---|---|---|
|**Operations Allowed**|Row operations ONLY|Row AND Column operations|
|**Equation**|$B = PA$|$B = PAQ$|
|**Do they have the same solutions?**|Yes|No (variables get mixed up)|
|**Same Row Space?**|Yes|No|
|**Same Rank?**|Yes|Yes|

**The Golden Rule:** All row equivalent matrices are equivalent, but _not_ all equivalent matrices are row equivalent.