## Motivation
- can linear algebra help us to study geometry $\implies$ yes, they can
- use of dot product, angles, distances etc. even beyond the 3D space
	- dot product is the main tool we use (to talk about angle between two vectors)
## Orthogonality
- if two vectors are perpendicular to each other
- Normal: of length $1$ (a unit vector)

### Question in Section 5.1
(i) Can an orthogonal set contain the zero vector $\textbf{0}$?
A: `Yes` $\{\textbf{0}, \textbf{v}\}, \text{for any non-zero v is an orthogonal set}$

(ii) Can an orthonormal set contain the zero vector $\textbf{0}$?
A: `No`, the zero vector does not have length of $1$

## Orthogonal Basis
- can be done by finding individual coordinates in the linear combination of the vector $v$ in subspace V.
- can calculate the coordinates relative to the basis, using the dot product
- only applies to orthogonal bases (the dot product needs to be $0$)

### Question 1 in Section 5.2
- with a set of orthonormal vectors, we can calculate basis by taking the dot product

## Orthogonal Matrices
- order $n$ square matrix where $A^T = A^{-1}$ or equivalently, $A^TA = I = AA^T$

## Orthogonal Component
- Given the subspace $\mathbb{R}^n$, the orthogonal complement of $V$ is the **set of all vectors** that are orthogonal to V, denoted as:
$$
V^{\perp} = \{\textbf{w} \in \mathbb{R}^n | \textbf{w} \cdot \textbf{v} = 0, \forall \textbf{v} \in V\}
$$
- we don't need to multiply $w$ with every $v$, not an infinite number of $v$
	- just need to check that the vector is orthogonal to all elements of the spanning set that we determine

- $w \perp v \implies w \in Null(A^T)$
	- $A$ is the spanning set of $V$ as columns
	- $v^{\perp} = Null(A^T)$, as provided by the theorem
	- $V = span\{u_1, \ldots, u_k\}$
### Question 2 in Section 5.2
$A \to 4 \times 3$
$A^T \to 3 \times 4$
$A \cdot A^T = B_{4 \times 4}$

### Challenge in Section 5.1
$Row(A)^{\perp} = Null(A)$
- row space of $A^T =$ column space of $A$

### Challenge in Section 5.2
- V is a subspace of $\mathbb{R}^n$
	- $dim \: V = k \leq n$

- $u \cdot v = [u]_s \cdot [v]_s$, which occurs in $\mathbb{R}^n$
- $\lVert u - v \rVert = \lVert [u]_s - [v]_s \rVert$

**Part 1**
- we assume that $S$ is an orthonormal basis.
- $u, v \in V$, so $u$ can be written as a linear combination of the basis $S$

- we know that length of $w_i = 1$
	- for $w$, indices are different $\implies$ become $0$, indices are the same $\implies$ become $1$
- we want to show that $u \cdot v = [u]_s \cdot [v]_s$

**Part 2**
- we know that $v \cdot v = \lVert v \rVert^2$
- we can claim that $\lVert u - v \rVert^2 = \lVert [u]_s - [v]_s \rVert^2$
	- one may be positive, one may be negative theoretically, but we are talking about length, which is always positive
	- show that $LHS^2 = RHS^2$

### Challenge in Section 5.3
**Orthogonal Projection Theorem**
- very important theorem, used in many algorithms (Gram–Schmidt and Least Squares)

- $w = w_p + w_n$
	- $w$ can be decomposed to two vectors, one in the plane and one outside, but orthogonal to the plane itself

**Objectives**
1. Find $w_p, \: w_p \in V$ (ref Slide 43 of lecture materials)
	1. we can write $w_p$ as a linear combination, check that $w_p \in V$, $w_p$ is in the span of the basis 

2. Find $w_n, w_n \in V^{\perp}$
	1. define $w_n = w - w_p$ and $w_n$ *needs to be orthogonal* to $V$
	2. just need to dot product with the elements of the spanning set

3. $w = w_p + w_n$

4. Check uniqueness
	1. Suppose we have $2$, disprove as such.
		1. Have $z_p + z_n$
		2. Domain is $V^{\perp} \cap V$, but $V^{\perp} \cap V$ must be $=0$ because $\lVert x \rVert^2 = x \cdot x = 0$
	2. Then we have $w_p = z_p$ and $w_n = z_n$, hence it is unique

---
## Nonzero Orthogonal Vectors that are Linearly Independent
- we cannot have a vector being orthogonal to its multiple.
- suppose we have $S = \{u_1, u_2 \ldots, u_k\}$ which is an orthogonal set of nonzero vectors
- want to show $c_1 = c_2 = \ldots = c_n = 0$

### Exercise on Orthogonal matrices
$A$ and $B$ orthogonal, which of the following are also orthogonal.

> $A$ is orthogonal iff $A \cdot A^T = A^T \cdot A = I$
- its row vector has to form an orthonormal basis
## Gram-Schmidt Process
- used for QR Decomposition
- built on the basis of the orthogonal projection theorem in Section 5.3
- steps in converting linearly independent set to an orthogonal set
	- find the orthonormal basis for the column space of $A$
