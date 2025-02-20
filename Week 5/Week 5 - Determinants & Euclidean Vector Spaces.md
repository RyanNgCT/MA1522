Concept of determinants come before concept of matrices
- can be recursively defined

**Examples**
If $A =\begin{pmatrix}3\end{pmatrix} \implies det(A) = 3$

If $B = \begin{pmatrix}1 & 2 \\ 3 & 4\end{pmatrix} \implies det(A) = 4 - 6 = -2$

If $C = \begin{pmatrix}1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9\end{pmatrix} \implies det(C) = 45 + 96 + 84 - 105 - 48 - 72 = 0$

- only up to size of $3 \times 3 \to$ can use shortcut, but above $3 \times 3$ then we have to use the definition.
- Alternative use the *cofactor expansion* or recursive definition
	- expansion of $det(C)$ will have $24$ terms in total

For $A_{4 \times 4} \implies det(A)?$
- The $(i,j)$-th cofactor of $A$
	- refers to row $i$ and column $j$ (to be removed)
	- dimensionality of the $(i,j)$-th matrix minor is $(n-1) \times (n-1)$, can be denoted as $M_{ij}$ (for a order $n$ matrix)
	- Then we determine that the cofactor $A_{ij} = (-1)^{i + j} det(M_{ij})$

Given $\textbf{A}_{n \times n}$
- the cofactor expression of $det(\textbf{A})$ along **row 1** is $det(\textbf{A}) = a_{11}A_{11} + a_{12}A_{12} + \ldots + a_{1n}A_{1n}$
	- bold face $\textbf{A}$ is a matrix while $A{ij}$ is a number.

**Important Property of Determinants**
- a matrix $A$ is invertible iff $det(A) \neq 0$
	- the determinant number tells us if a matrix is invertible or not.

### Section 2.8 Questions
**Conclusion:** Non-zero row, $det(A) = 0 \implies A$ is not invertible.

### Section 2.9 Questions
If matrix $A$ has two equal columns or rows then $det(A) = 0$, since the row can be reduced to a zero row using Gaussian Elimination

### Section 2.10 Q1
Suppose matrix $A$ is $LU$ factorizable
- for $L$ the diagonal has to be one
- for $U$ it is a unit upper triangular matrix
- Then $det(A) = det(LU) = det(L) \times det(U) = u_{11} \times u_{22} \times \ldots \times u_{nn}$ (product of the diagonal entries)

- transform to REF to enable the matrix to look like $U$ (which is upper triangular)

### Section 2.10 Q2i
- $det(A) = det(A^T)$
- we can obtain $det(3A^T) = 3^4det(A^T)$, where $4$ is the size of the matrix $A$.

- note that $det((3B)^{-1}) = \frac{1}{det(3B)}$

> Singular matrix $=$ not invertible
- $A$ is singular iff $det(A) = 0$

> adjoint of $A \implies$ order $n$ square matrix whose $(i, j)$ entry is the $(j, i)$ cofactor

### Section 2.10 Q2ii
$adj(A)^T = adj(A^T)$
- order of taking adjoint and transpose is different, but the resultant matrix is the same.
	- $A_{ij}^T$ is the cofactor of A transpose.

The proof is left as an exercise for Yang Yue.

For diagonal matrix, the transpose is itself.

### 3.1
- only limited to Euclidean Vector Spaces (i.e. $\mathbb{R}^n$), but Vector Spaces $\subset \mathbb{R}^n$.
	- In abstract vector space, we may have concept of distance, parallel and perpendicular (or orthogonal concepts).
	- producer for the scalar in scalar multiplication comes from $\mathbb{R}$ (i.e. real numbers)
	- zero vector $\implies \textbf{0} + \textbf{u} = \textbf{u}$

**Subtleties in Distributive Law** (scalar multiplication, then vector addition)
- (5) addition inside $\textbf{v}$
- (6) addition of two real numbers $a + b, \forall a, b \in \mathbb{R}$

(7) Associativity of Scalar Multiplication
- multiplication of real numbers
- then scalar multiplication of the result.

$\forall u_1, u_2 \in U, U$ is closed under addition $u_1 + u_2$.
- result will still be in the set $U$

$\forall a \in \mathbb{R}, \:a \cdot \textbf{u} \in U$