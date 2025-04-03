## Exam Format
- Pen and paper, no MATLAB
- have to due row reduction by hand
	- $2 \times 2$ or $3 \times 3$ matrices only
	- doing this computation under time constraint is a challenge
## Diagonalization, Algebraic and Geometric Multiplicity
- an application of eigenvalues and eigenvectors in Week 10

> The **Algebraic Multiplicity** of $\lambda$ is the largest integer $r_{\lambda}$ s.t. $det(xI - A) = (x- \lambda)^{r_{\lambda}}p(x)$
- both the geometric and algebraic multiplicities will help us to determine if the matrix is diagonalisable
- in the best and most ideal case, we can break the determinant down into the characteristic polynomial
	- we can factorise a linear polynomial into something $\times$ quadratics that cannot be factorised further etc. (degree $2$)
		- quadratic has no real root and hence no real eigenvalues

> **Geometric Multiplicity** is bounded **above** the **Algebraic multiplicity** (i.e. $1 \leq dim(E_{\lambda}) \leq r_{\lambda}$

> Square matrix of order $n$ is **diagonalizable** if $\exists$ invertible matrix $P$ s.t. $P^{-1}AP = D$, where $D$ is a diagonal matrix
- equivalently, $A = PDP^{-1}$ (one way of writing it)
- $P$ is an eigenvector of the matrix $A$
- each diagonal entry corresponds to the eigenvector (i.e. $A_{ii} = \lambda_i$)

**3 Equivalent Statements for Diagonalizability**
1. The square matrix $A$ is diagonalizable
2. $\exists$ basis $\{u_1, u_2, \ldots, u_n\}$ of $\mathbb{R}^n$ of the eigenvectors of $A$
3. Characteristic Polynomial of $A$ splits into linear factors (of degree $1$)
	1. For all the factors, if geometric multiplicity $=$ algebraic multiplicity $\implies$ diagonalizable
### Section 6.2 Question 1
Suppose $\textbf{A}$ is a square matrix of order $n$, with distinct eigenvalues $\lambda_1, \ldots, \lambda_p$ and algebraic multiplicities $r_1, \ldots, r_p$ respectively. What can we conclude about the sum of the algebraic multiplicities?

$det(xI - A) = (x- \lambda)^{r_1}(x- \lambda)^{r_2}\ldots(x- \lambda)^{r_k}$
- know that degree of characteristic polynomial $= n$
- Then $r_1 + r_2 + \ldots + r_p = n$
- If cannot factorize into linear factors (i.e. have quadratics, then $r_1 + r_2 + \ldots + r_p \leq n$)
### Section 6.2 Question 2
Is it possible for the geometric multiplicity to be $0$, $dim(E_{\lambda}) = 0$?
- for $dim(x) = 0 \implies$ set can only contain the zero vector
- then there is only one eigenvector (a.k.a. the $0$ vector)

A: No, if $\lambda$ is an eigenvalue of $A$, then $\exists$ some $v \neq 0$
### Section 6.2 Exercise
Show (i) Diagonalizability and that it is (ii) a square matrix

### Section 6.2 Question 3
Part 1: Fix $D$, can $P$ be variable?
**False.** Can find counterexample.

Part 2: Fix $P$, then is $D$ variable?
**True**

If we fix eigenvalue, eigenvector is free. But if fix eigenvector, eigenvalue cannot change.

---
## Markov Chains
- Probability Vector: vector $v$ with non-negative coordinates that add up to $1$ (summation of everything is $1$)
	- each component represents a sum of events
	- must be positive and add to $1$
	- example: $\begin{pmatrix} 0.3 \\ 0.3 \\ 0.4\end{pmatrix}$

- Stochastic matrix is a matrix whose columns are probability vectors

- Markov Chain is a sequence of probability vectors together with a stochastic matrix $P$
	- Markov chain converges $\implies$ converges to an equilibrium vector
	- $x_0 = \ldots, \: x_1 = Px_0, \: x_2 = Px_1,\: \ldots, \:x_k = Px_{x-1}$

- Equilibrium Vector (for a stochastic matrix $P$)
	- there is no incentive for $v$ to change (i.e. it is stable)
### Section 6.4 Challenge Part 1
- every row of the matrix has $-p_{ij}$, the diagonal entries are $x-p_{ij}$
- we perform the row operations: $R_1 + R_2$, $R_1 + R_3, \ldots R_1 + R_n$ to obtain a resultant matrix. 
- can extract the factors $(x-1)$ from the matrix $\implies$ we have $x = 1$ as an eigenvalue of the stochastic matrix $P$
### Section 6.4 Challenge Part 2
- manipulation of symbols (since it is just summations)

### Section 6.4 Challenge Part 3
- show that if Markov chain converges, then the state vectors will converge into a equilibrium vector

---
## Orthogonally Diagonalizable
- order $n$ square matrix $A$ is orthogonally diagonalizable if $A = PDP^T$ for some orthogonal matrix $P$ and diagonal matrix $D$

**Equivalent Statements**
1. Orthogonally Diagonalizable
2. $A$ is a Symmetric Matrix
3. $\exists$ orthonormal basis of $\mathbb{R}^n$, consisting of eigenvectors of $A$
### Section 6.3 Question 
(a) $A\cdot B$ may not be symmetric
(b) $(A + B)$ is symmetric? $\implies$Sum of symmetric matrices are symmetric
(c) Orthogonal matrices may not be symmetric. Can find counterexample.
(d) $A + A^T$, where is is of order $n$. $\implies (A + A^T)^T = A^T + (A^T)^T = A^T + A = A + A^T$
(e) $A^TA$ for any matrix $A \implies$ is symmetric. Related to single value decomposition 

**Algo**
- between eigenspaces, they are already orthogonal
- can perform Gram-Schmidt process within each eigenspace