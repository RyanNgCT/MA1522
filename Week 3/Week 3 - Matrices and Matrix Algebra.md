Highlighting the important points in the lecture material

### General Formula for Matrix Multiplication
$\textbf{AB} = (a_{ij})_{m \times p} \cdot(b_{ij})_{p \times n} = (\sum_{k = 1}^p a_{ik}b_{kj})_{m \times n}$
- $\textbf{A}$ is a matrix of dimension $m$ rows and $p$ columns
- we have to make sure dimensionality of $p$ columns in the first matrix is the same as $p$ rows in the second matrix

**Cautions**
1. Matrix multiplication is not commutative (cannot change the order)
$$
\left(
\begin{array}{cc}
0 & 1 \\
1 & 0
\end{array}
\right)
\cdot
\left(
\begin{array}{cc}
1 & 2 \\
3 & 4
\end{array}
\right) 

\neq
\left(
\begin{array}{cc}
1 & 2 \\
3 & 4
\end{array}
\right) 
\cdot
\left(
\begin{array}{cc}
0 & 1 \\
1 & 0
\end{array}
\right)
$$
	- In general for two matrices $A \times B \neq B \times A$.
	
2. Two non-zero matrices (have non-zero entries), could theoretically have a product equal to zero
	- could have zero divisors

3. We do **not** have cancellation laws
	- from $AB = AC, \: A \neq 0$ cannot conclude that $B = C$

### Invertible Matrices
- an invertible matrix needs to be a square (i.e. has the dimensions of $n \times n$)
	- by right, need to check $A \times B$ and $B \times A$ (using the identity law), but for square $n \times n$, checking **one side suffices**
	$$
		\textbf{AB} = \textbf{\(I_n\)} = \textbf{BA}
	$$
- then we can perform either left or right cancellation.

- Many equivalent definitions for invertibility $\implies$ can use any of them to describe invertibility of a matrix $A$.
	- A is invertible
	- Transpose of $A$ is also invertible (flip w.r.t. the unknown)
	- under the definition of invertible, have to check both side (but in case of square matrix, only need to check one side)
	- RREF of $A$ is a identity matrix
	- $A$ can be expressed as product of elementary matrices
	- (7) and (8) mentions some system and equation

### Section 2.1 Questions
Concepts of 
- **row equivalent:** ability to apply elementary row operations to get from one to another

- **upper triangular matrix:** if below the *main diagonal*, all values have to be zero. All important data are stored in the upper triangle

- **strictly upper triangular matrix:** not only the condition above, even things on the main diagonal is pivotal (i.e. all other values are zero in the pivot columns)

- **symmetric matrix:** symmetric w.r.t. the main diagonal (imagine the main diagonal as a mirror) $\implies a_{ij} = a{ji}$ 

$$
\left(
\begin{array}{ccc}
1 & 2 & 3 \\
2 & 0  & 4 \\
3 & 4 & 5
\end{array}
\right)
$$
##### Q1i. Every square matrix is row equivalent to an upper triangular matrix. T or F?
**T**. If a square matrix is in REF, it has to be an upper triangular matrix.
- have two non-zero rows, since in REF, it has to be ***to the left*** of second row $\implies$ violates defn of REF.
##### Q1ii. Every square matrix is row equivalent to a strictly upper triangular matrix. T or F?
**F**. Counterexample being:
$$
\left(
\begin{array}{cc}
1 & 0 \\
0 & 1
\end{array}
\right)
$$

Notice in the above that it is not row equivalent to any strictly upper triangular matrix.

General form of a $2 \times 2$ strictly triangular matrix is:
$$
\left(
\begin{array}{cc}
0 & * \\
0 & 0
\end{array}
\right)
$$
##### Q2. Is it true that a symmetric upper triangular matrix is a zero matrix?
**F**. Counterexample:
$$
\left(
\begin{array}{cc}
1 & 0 \\
0 & 1
\end{array}
\right)
$$
Is both symmetric upper triangular and non-zero.

Any such matrix $A = \left(a_{ij}\right)$ must be diagonal.

#### Section 2.2 Question
Show that for diagonal matrices $A$ and $B$,
$$
(A + B)^2 = A^2 + 2AB + B^2.
$$
Suffice to prove that $AB (a_{ii} \times b_{ii})= BA (b_{ii} \times a_{ii})$ for **diagonal matrices** $A$ and $B$.

$AB$ and $BA$ combine to give $2 \times AB$.

**Follow up Question**
What if only of $A$ or $B$ is diagonal?
- $AB \neq BA$ (have different product) $\implies$ counterexample is an exercise for the reader.

#### Section 2.3 Question
- homogenous in terms of matrix equations.
	- $A$ is a matrix, $x$ is a vector of $n$ dimensionality (of $n$ rows)
	- homogenous linear system $\implies$ **RHS are all zeroes.**

- Trivial solutions to the system
	- set $x_1 = x_2 = \ldots = x_i = 0$, then that is the solution (no effort needed, no need to go through Gaussian Elimination)

- Non-Trivial solutions
	- need to go through some steps to derive the solutions

##### If homogeneous system has unique solution, must be the trivial solution? (T or F)
**T**, "by logic".

##### If homogeneous system has trivial solution, must be the unique solution? (T or F)
**F**, not necessarily. Counterexample:

#### Section 2.4 Question
##### Q1.
- Quite Straightforward $\implies$ perform Gaussian Elimination, followed by back-substitution.

##### Q2i. If product of square matrices $AB$ is invertible $\implies$ both $A$ and $B$ are invertible?
- refer back to statement (iv) of the concept of invertibility.
> If $B$ is an invertible matrix of order $n$, then $(AB)$ is invertible with the inverse $(AB)^{-1} = B^{-1} \times A^{-1}$

> Transposition of $A$, somewhat like a mirror of A, where the point of reflection is at the diagonal.
> - refer to the properties of transpose
> - square matrix $A$ is symmetric $\iff$ $A = A^T$

**Key Question to ask:** for two invertible matrices, their *product is also invertible*?


**T**. By defn, Invertibility is that one matrix has a partner. Invertibility through associativity.
- having one side of a square matrix being invertible is as good as having both sides being invertible.

##### Q2ii. Is the inverse of an invertible symmetric matrix symmetric?
$$
(A^T)^{-1} = (A^{-1})^T
$$

#### Section 2.1 Challenge
##### If $A$ and $B$ are symmetric matrices of the same order, then so is $AB$?
$$
\begin{aligned}
(AB)^T & \neq AB \text{ ?} \\
\text{LHS} &= B^TA^T \\
& \neq BA \\
\\
\therefore, (AB)^T & \neq AB
\end{aligned}
 $$

#### Section 2.3 Challenge
- one is homogeneous, one is not
- make the non-homogeneous one homogeneous.
- the solution of the non-homogenous solution $= v + \text{solution of homogeneous system}$
	- $v$ is a particular solution to the system (show iff both directions are tautologies).

$\left(\implies\right)$
Show that $z$ is a solution of the non-homogenous system $Ax = b$.

$\left(\impliedby \right)$
Show that $y +b$ is a solution for the non-homogeneous system.
- any non-homogeneous solution must be the form $b + \ldots$ 