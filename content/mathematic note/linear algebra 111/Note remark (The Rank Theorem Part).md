
### First the note states that $\alpha' = \alpha \cup \{0\}$ is a valid subspace but in fact $\alpha'\cup \{ 0 \}$ is not a subspace. 

![[Pasted image 20260622224724.png]]
<div class="page-break" style="page-break-before: always;"></div>

For example

Let $A$ be a $1\times 2$ matrix:

$$
A=(1~~~0)
$$
This matrix defines a linear transformation $T: \mathbb{R}^2 \rightarrow \mathbb{R}^1$ given by:

$$T \begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 1 & 0 \end{pmatrix} \begin{pmatrix} x \\ y \end{pmatrix} = x$$
First, let's find the **Kernel** ($\text{Ker } T$). The Kernel consists of all input vectors that get mapped to $0$:

$$\text{Ker } T = \left\{ \begin{pmatrix} x \\ y \end{pmatrix} \in \mathbb{R}^2 \;\middle|\; x = 0 \right\}$$
Let $\alpha$ be the complement of the Kernel and 
Let $\alpha'=\alpha \cup \{ 0 \}$. This means $\alpha'$ contains the zero vector $\begin{pmatrix} 0 \\ 0 \end{pmatrix}$ and **every vector where $x \neq 0$**.

- Let $v_1 = \begin{pmatrix} 1 \\ 2 \end{pmatrix}$ and $v_2 = \begin{pmatrix} -1 \\ 2 \end{pmatrix}$. It is clear that $v_{1},v_{2} \in \alpha'$
    

Now, let's add them:

$$v_1 + v_2 = \begin{pmatrix} 1 \\ 2 \end{pmatrix} + \begin{pmatrix} -1 \\ 2 \end{pmatrix} = \begin{pmatrix} 0 \\ 4 \end{pmatrix}$$

Notice that $v_{1}+v_{2} \not\in \alpha'$. Thus, it is not closed under addition. Thus $\alpha'$ is not a vector space.

<div class="page-break" style="page-break-before: always;"></div>

### Second 

![[Pasted image 20260622224935.png]]

  From first part we know that since $\alpha'$ is not a subspace, then  $ColA \neq \alpha'$. Besides that from the note,  it state that $A\in M_{n\times m}$ , thus, the correct version should be $ColA\subseteq \mathbb{R}^{n}$ (because each column of $A$ is in $\mathbb{R}^{n}$) 

In conclusion the argument is wrong??

<div class="page-break" style="page-break-before: always;"></div>

### The correct version

To turn that intuition into rigorous math without breaking any rules

- $\text{Row } A$ lives in the domain $\mathbb{R}^m$.
    
- $\text{Row } A$ is a perfectly valid subspace.
    
- $\mathbb{R}^m = \text{Ker } T \oplus \text{Row } A$ (Every vector in $\mathbb{R}^{m}$ can be uniquely split between them)(By Fundamental Theorem of Linear Algebra)
    
- $\dim(\text{Row } A) + \dim(\text{Ker } T) = m$.
    
- Because $\dim(\text{Row } A) = \dim(\text{Col } A)$, you can seamlessly substitute it to get the final Rank Theorem: $\text{rank}(A) + \dim \text{Nul } A = m$

## The Direct Sum ($\oplus$)

Because $W$ and $W^\perp$ are so perfectly segregated, they allow us to split the entire vector universe up cleanly. This is called a **Direct Sum**, written with the symbol $\oplus$:

$$\mathbb{R}^n = W \oplus W^\perp$$

This structural blueprint guarantees two extraordinary things:

1. **Total Coverage:** Every single vector $v$ in the entire space $\mathbb{R}^n$ can be broken down into a sum of two pieces: $v = w + w^\perp$, where $w \in W$ and $w^\perp \in W^\perp$.
    
2. **Zero Overlap:** The only vector that lives in both worlds simultaneously is the zero vector itself ($W \cap W^\perp = \{\mathbf{0}\}$).

Because it's a direct sum, their dimensions add up flawlessly to the total size of the domain:

$$\dim(\text{Nul } A) + \dim(\text{Row } A) = m$$
