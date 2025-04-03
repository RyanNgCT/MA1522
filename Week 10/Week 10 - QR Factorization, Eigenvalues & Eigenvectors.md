## QR Factorization
- process of simplifying a matrix $A$ into $QR$
	- $Q$ is an orthogonal matrix
	- $Q^TQ = I_n$
	- $Q$ is the same size as $A$
	- $R$ is an upper triangular matrix (positive diagonal entries)

- Restrictions
	- $A$ **must have** *linearly independent columns*
	- Required to use Gram-Schmidt process
	- If columns not linearly independent, then we end up with zero vectors

- origination of $Q$ and $R$
	- $Q \implies$ apply Gram-Schmidt process on matrix $A$'s columns, normalize the vectors
		- we obtain the $Q_i$ step by step (we only require $A_i$) $\implies$ it grows gradually
		- we can derive than $span\{q_1, \ldots, q_j\} = span\{a_1, \ldots, a_j\}$ or $span(Q) = span(A)$
		- we can write $a_j$ as a linear combination of $q_1, \ldots, q_j$
		- property of $Q$: 
			- they have orthonormal columns
			- size of $m \times n$
			- $Q$ is an orthogonal matrix, $\therefore Q^TQ = I_n$  
	- $R \implies$ of order $n$

### Algorithm for QR Factorization
1. perform  Gram-Schmidt  on the columns of $A$ to obtain an orthonormal set $\{q_1, \ldots, q_j\}$
2. Set $Q = \{q_1, \ldots, q_j\}$
3. Compute $R = Q^T A$

### Section 5.4 Exercise 1 Part 1
**Prove that $Q^TQ = I_n$.**

Since $Q$ is of size $m \times n$, $Q^T$ is of size $n \times m$, so by block multiplication, the resultant matrix is of the form $\begin{pmatrix}q_i^T & q_j\end{pmatrix} = \begin{pmatrix}q_i \cdot q_j\end{pmatrix} = I_n$

### Section 5.4 Exercise 1 Part 2
**Prove that the diagonal entries of $R$ are positive, $r_{ii} \gt 0$, $\forall i = 1, \ldots, n$**
- know that $a_i = r_{1i}q_1 + \ldots + r_{ii}q_i$
- we can use $q_i$ to dot multiply both sides to obtain $r_{ii} = a_i \cdot q_i$
- since $q_j \times q_i = 0$ for $i = j$
### Section 5.4 Exercise 1 Part 3
- diagonal entries are positive, so $det(R) \gt 0$
### Section 5.4 Exercise 2
- Invertible Matrix $\implies$ square matrix
- Not square, then we use the terms left or right inverse

- We use QR factorization to prove that if $A$ is an $m \times n$ matrix with linearly independent columns, then $A^TA$ is invertible
$$
A^T A = (QR)^T (QR) = R^T Q^T QR = R^T I_n R = R^T R
$$
- $R$ is invertible, then $R^T$ also invertible, thus $A^TA$ is invertible

---
## Least Square Solution
**Motivation**
- usefulness of least square solution, when we have variables $x, y, z$, then:
	- we can form the equations $a_ix + b_iy + c_iz = d_i$
	- it is very likely that these system of equations are usually inconsistent, with no solutions (but we can find some "best approximation")

**Least Square Solution**
- required to fulfil the equation as follows:
	- $u$ is the least square solution if $Au$ which is a projection in the column space of $A$
	- vector $v \in \mathbb{R}^n$
$$
\lVert Au - b \rVert \leq \lVert Av - b \rVert 
$$

- Note that the vector $b' = Au$ is unique, but $u$ itself may not be unique
- In general $Au \neq b$
### Section 5.5 Question 1
Suppose that the system $Ax =b$ is **consistent** (somewhat anomalous).
Suppose $u$ is a solution to $Ax = b$ (which is a linear system). Is $u$ a least square solution to $Ax =b$?

**Answer:** Yes, because we assume that $Au =b$ in this case and hence $\lVert b - b \rVert = \textbf{0}_n$
$$
\lVert Au - b \rVert  = 0\leq \lVert Av - b \rVert 
$$

### Section 5.5 Question 2
Suppose $u$ is a least square solution to $Ax =b$? Can we conclude that $u$ is a solution to $Ax = b$?

**Answer**
$$
\lVert Au - b \rVert \leq \lVert Av - b \rVert  = 0
$$

### Section 5.5 Challenge 1
Proof ($\impliedby$)
Start from $u$ is a solution to get $b$ is a projection

### Section 5.5 Challenge 2
- We want to show $\forall w \in \mathbb{R}^n$, the projection of $w$ onto the subspace $V$ is $QQ^Tw$
- using $w_1, w_2$ and $w$ to obtain the projection

---
## Eigenvalues & Eigenvectors
- A real number $\lambda$ is an eigenvalue of $A$ if $\exists$ non-zero vector $\textbf{v} \in \mathbb{R}^{n}$ s.t.
$$
Av = \lambda v
$$
- the non-zero vector $v$ is called the eigenvector associated to $\lambda$ (require the eigenvector $v \neq 0$ for it to be interesting)

Think of a matrix as an action on $\mathbb{R}^{n}$ (i.e. a linear transformation)
- eigenvectors are the vectors being scaled when acted upon by $A$
	- for each eigenvector, there is a fixed eigenvalue (association from eigenvalue to eigenvector)
- eigenvalues are the amount to be scaled
## Eigenspace
- Recall that eigenvectors of $A$ associated to eigenvalue $\lambda$ are non-trivial solutions to:
$$
(\lambda I - A)x = 0
$$

### Characteristic Polynomial
- is a determinant of a $n \times n$ matrix
$$
det(x\textbf{I} - \textbf{A})
$$
- we equate $det(x\textbf{I} - \textbf{A}) = 0$ then solve for $x$. $x$ will be the eigenvalues of the matrix $A$

### Section 6.1 Part 2
- cannot just perform row operations on the matrix $A$ itself
- After computing $x\textbf{I} - \textbf{A}$, then we can perform row reductions

### Challenge 6.1 Part 1
What is geometric multiplicity of $\lambda$?
- will be used later on in the diagonalization portion
	- algebraic
	- geometric (dimension of $E_{\lambda}$ or the eigenspace, which is also the dimension of the nullspace -- i.e. nullity)

### Challenge 6.1 Part 2
We can make it such that:
$$
\text{Geometric multiplicity of } A = \text{nullity}(\lambda I - A) = \:\ldots \:= \text{Geometric multiplicity of } \lambda \text{ for } A^T
$$