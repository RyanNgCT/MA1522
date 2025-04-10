## What is Single Value Decomposition?
- SVD *brings everything together* (eigenvalues, orthogonal basis, diagonalization, linear transformation etc.)
	- need some theory of matrices by rank, null space and eigenvalues

- SVD applies to arbitrary matrices (not limited to only a certain subset of matrices) $\implies$ apply to $m \times n$ matrices (which eigenvalues do not apply to -- only square matrices)
	- restrictions could include "orthogonally diagonalizable" (does not apply to all square matrices)

- should watch the video on SVD to get a better geometric idea of SVD
### Singular Values
- For $m \times n$ matrix A, since $A^TA$ is order $n$ symmetric, it is orthogonally diagonalizable.
- Let $\{v_1, v_2, \ldots v_n\}$ be an *orthonormal basis* for $\mathbb{R}^n$ consisting of eigenvalues of $A^TA$ which the associated eigenvalues $\mu_i$ are not necessarily distinct

- eigenvalues of $A^TA$ are non-negative $\implies \mathbb{R}_{\geq 0}$ 
	- can take the square root of each value
	- then we let the singular values of $A$ to be $\sqrt{\mu_i}, \forall i = 1, \ldots, n$
	- the matrix $\Sigma$ is defined to be the same size as $A$ (i.e. $m \times n$, or optionally of order $n$)
		- matrix $\Sigma$ is almost like a diagonal matrix
	- we can only find nonzero entries in the upper left component of $D$
### Single Value Decomposition
- $\sigma_i$ = square root of eigenvalue of $A^TA$ (i.e. $\sqrt{\mu_i}$)

- we extend $\{u_1, u_2, \ldots, u_r\}$ (basis of the column space) to an orthonormal basis $\{u_1, u_2, \ldots, u_r, \ldots, u_m\}$ for $\mathbb{R}^m$ if $r \neq m$ (if more rows than columns)
- we likely have to deal with $0$ eigenvalues if we have more columns than rows (fat matrix)

- can be turned into an algorithm
	1. find $A^TA$ using matrix multiplication, based on the value of $A$ provided

	2. find the eigenvalues of $A^TA$ and arrange them in descending order *counting multiplicity* $\implies \mu_1 \gt \mu_2 \gt \ldots$
		1. use the characteristic polynomial to find eigenvalues and then find the orthonormal basis for the eigenspace using the RREF form (see step $4$ below)

	3. take the single value $\sigma_i$
		1. note that $\Sigma$ (matrix) is the same size as $A$, but its component $D$ is like a diagonalizable square matrix

	4. we need to find an orthonormal basis for each eigenspace and let $v_i$ be a unit vector associated to $\mu_i$ (which is square root eigenvalue of $A^TA$)
		1. putting the basis vectors together to obtain $V$ (i.e. $V = \begin{pmatrix}v_1 & \ldots & v_n\end{pmatrix}$)

	5. find a bunch of $u_i$s before the "cut-off point" (let $u_i = \frac{1}{\sigma_i}Av_i$)
		1. not that the third vector that we are obtaining must be orthogonal to the previous $2$ vectors (is a solution to the homogeneous system) $\implies$ if orthogonal, then they are linearly independent

	6. Then $A = U \Sigma V^T$
### Section 6.5 Exercise 
- show that the product of $\Sigma^T \Sigma$ is a diagonalizable, where the diagonal entries are $\mu_1, \mu_2, \: \ldots, \mu_n$ (are eigenvalues of $A^TA$)

- solution steps
	- When we take $\Sigma^T$, we need to consider that:
		- the top right goes down to the bottom left, and the dimensionality gets swapped as well. (bottom left goes to top right)
		- $D \to D^T$ (but since $D$ is diagonalizable, it is just $D$)
			- entries for $D$ are $\sigma_1, \sigma_2, \ldots, \sigma_n$
		- for the bottom right matrix, we just need to swap the dimensionality (as the zero matrix components are transposed)
		- we can do the product as blocks

	- we note that $\mu_i = (\sigma_i)^2$

	- show that $Av_i \neq 0, \forall i \leq r$ and $Av_i = 0, \forall i \geq r$
		- note that the diagonal entry $\sigma_i$ can fall outside the top left component of $D$
		- $r$ is the "cut off" point for when $\sigma_{r + 1} = 0$ and $\sigma_r \geq 0$ (is the last nonzero entry)

	- can use the more general fact that $\text{Null}(A) = \text{Null}(A^TA)$
$\subseteq$
1. so if $Ax = 0 \implies A^TAx = 0$ 

$\supseteq$
1. if $A^TAx = 0 \implies(Ax)^T(Ax) = 0$, which says that $\lVert Ax \rVert^2 = 0$
(incomplete)

### Section 6.5 Question
- Let $A$ be an $m \times n$ matrix.
	- (1) Prove that $\text{rank}(A) = n \iff$ all singular values of $A$ are positive (i.e. $\sigma_i \in \mathbb{R}^+$)
	- (2) Prove that $\text{rank}(A) = m \iff$ the singular values of $A^T$ are positive
		- rank is invariant under transpose

	- By rank-nullity theorem, we know that $\text{rank}(A) + \text{nullity}(A) = n$

(1) 
($\implies$)
if $\text{rank}(A) = n \implies \text{rank}(A^TA) = n$.
$\therefore D = P^T(A^T A)P$ also has rank $n$ (P is invertible)
every eigenvalue $\sigma_i \gt 0 \implies$ every singular value $\forall \sigma_i \gt 0$

($\impliedby$)
if all singular values are positive, then all the eigenvalues of $A^TA$ are positive, in other words, $0$ is not an eigenvalue of $A^TA$, hence $\text{Nullity}(A^TA) = 0$ (we have no non-pivots)

(2)
Trivial to prove, based on what was described in (1)

---
## Linear Transformation
- in many textbooks, linear transformation is taught before eigenvalues and eigenvectors etc.
- a matrix is a way of moving points (a matrix is sort of like a transformation)

- is a special kind of function (or mapping)
	- idea of "linear" $=$ preserving addition and scalar multiplication
		- everything should have a degree of $1$, no cube roots, trig functions (unless they add up to $0$ or $1$)

- to make sense of matrix multiplication, we need the matrix $A$, as well as the column vector $\textbf{x}$
	- we have to choose the number that matches the domain

- finding formula of matrix $\implies$ just do the computation first (of matrix multiplication)

- how to tell that something is not a linear transformation if the following don't hold
	- $T$ does not map the zero vector to itself
	- $T$ does not preserve scalar multiplication in the space $\mathbb{R}^n$
	- $T$ does not preserve vector addition in the space $\mathbb{R}^n$

- as long as no violation, then the function $T$ is a linear transformation
### Standard Matrix
- unique $m \times n$ matrix $A$ s.t. $T(u) = A(u)$ (must satisfy the condition)
- Given a linear transformation $T$, we can obtain a matrix $A$ (i.e. a matrix can be viewed as a linear transformation)
### Section 7.1 Question 3 
**Part 1: Recommended method**
- is $T$ a linear transformation (does not violate the 3 conditions)
	- if it is a linear transformation, then we find the standard matrix

**Part 1: Yang Yue way**
- check definition for each map and apply them to standard basis
- reformat it as a linear transformation and factorize until we get the unknown vector

**Part 2**
Is $T$ a linear transformation of $a_1x_1 + a_2x_2 + \ldots +a_nx_n$
- rewrite the expression as a matrix multiplication instead

**Part 3**
The standard matrix it the identity matrix $I_n$