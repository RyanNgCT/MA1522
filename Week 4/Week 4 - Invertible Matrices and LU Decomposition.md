### Section 2.4 Question
**Inverting a (square) matrix**
- We put $A$ on the LHS and $I_3$ on the RHS. (i.e. $(A \:|\: I_3) \xrightarrow[\text{}]{\text{RREF}} (I_3 \:|\: A^{-1})$)
- We attempt to make the LHS into REF.
- In the RREF form, if $A$ is not an identity matrix, then it is not invertible

**Steps**
Let $A$ be a $n \times n$ matrix.
1. Form the $n \times 2n$ augmented matrix, with $I_n$ on the RHS
2. Reduce the augmented matrix into RREF (i.e. $(R | B)$)
3. Check result
	1. If RREF $R \neq I$ **or** REF has a zero row $\implies A$ not invertible.  
	2. If RREF  $R = I$ **or** REF no zero row $\implies A$ invertible with the inverse $A^{-1} = B$
### Elementary matrices
The connection between the identity matrix $I_n$ and the square matrix $E$ of order $n$ is as follows:
- $r$ is one of the elementary row operation (able to express the row operation algebraically)
$$
\begin{aligned}
I_n \xrightarrow[\text{}]{\text{r}} E \\
A \xrightarrow[\text{}]{\text{r}} EA
\end{aligned}
$$
For each elementary row operation, there is a reverse (to cancel the original row operation out). 
- start with $E$ is obtained from the identity by performing some simple e.r.o., $r$
- The inverse of $E$, $E^{-1}$ can be obtained by corresponding reverse of the e.r.o. corresponding to $E$ (i.e. need to modify $r$ in that case).
- is like "pre-multiplying" matrices

All elementary matrices are invertible
### Section 2.5 Question
$$
\begin{aligned}
E =& \begin{pmatrix}
1 & 0 & 0 & 0\\
0 & 1 & 0.5 & 0\\
0 & 0 & 1 & 0\\
0 & 0 & 1 & 1
\end{pmatrix}, \\\\
&\text{Then the e.r.o. used to obtain it is } R_2 - 0.5R_3.
\end{aligned}
$$
### Section 2.6 Question
Assuming we have the LHS of the equation $B = PA$, we can obtain the RHS (i.e. $PA$) from the LHS by performing a series of e.r.o. $r_1, r_2, \ldots r_n$.

Each e.r.o. has a corresponding matrix $E_k, k \in \mathbb{Z}$
- $P$ can be obtained by "pre-multiplying" some invertible matrix to $A$ and it has the be invertible.

Up to now, we have $8$ equivalent statements of invertibility.

### Section 2.7 Question
What is `other row operations` in the question?
**Part A**
Suppose $A = LU$, an $LU$ factorization of $A$
- each e.r.o. $r_i$ is of the form $R_i + cR_j$ for some $i \gt j$ and for some $c, c \in \mathbb{R}, c \neq 0$, **cannot** perform any other types of e.r.o. (row swapping and multiplying by constant $k$).
	- the $(i-j)^{th}$ column is set to $-C$
	- swapping rows $\implies$ makes the resultant matrix non-unit lower triangular
	- multiplying by a nonzero constant $a$ to the row $\implies$ no point if $a=1$ (the row is still the same value, no value add)

Use the $1$ entries of the lower triangular to clear those below, while retaining the fact that the matrix is still unit lower triangular.

There is a unique solution, since $Ax = b$ has a unique solution so long as $A$ is invertible.

**Part B**
- only possible row operation to maintain unit lower triangular matrix is $R_2 + cR_1$, which is of no help to solving for $y$
- Counterexample: $I_2$

##### LU Factorization
- there is some nice properties of $L$.
	- $L$ is the unit lower triangular matrix (see below) $\implies$ can derive many properties.
- $U$ is the REF form of $A$, less control of the shape and properties of $U$.
- if such a $LU$ factorization exists for $A \implies$  then $A$ is $LU$ factorizable.
- perform row operations once to solve linear systems
	$$
	\begin{aligned}
	\textbf{Lower Triangular Matrix:} \\
	L_3 &= \begin{pmatrix} * & 0 & 0 \\ * & * & 0 \\ * & * & * \end{pmatrix} \\\\
	\textbf{Unit Lower Triangular Matrix:} \\
	L_{unit 3} &= \begin{pmatrix} 1 & 0 & 0 \\ * & 1 & 0 \\ * & * & 1 \end{pmatrix} 
	\end{aligned}
	$$
- product of a unit lower triangular matrix is still a unit lower triangular matrix
- Transform $Ax = b$ into $LUx = b$, where $A = LU$, solve for the variable $y$ s.t. $Ay = b$

### Extra Questions
refer to slides
##### Q1. 
(a) for any $\textbf{b}$ 
(b) for some $\textbf{b} \implies$ not invertible $=$ RREF of A has a zero row 
(c) must have $\implies$ might hv unique or $\infty$ many solutions.
(d) must have $\implies$ has a counterexample for 
✅(e) None of the above $\infty$ many solutions and may be inconsistent

##### Q2.
If $A_1, A_2, \ldots, A_k$ are $n \times n$ s.t. $A_1A_2\ldots A_kx = 0$ has non-trivial solutions (i.e. $\neq 0$). 
What can be concluded about $A_k\ldots A_2A_1x = 0$?

Suppose eqn 2 has only trivial solution $\implies$ product of all is invertible.
##### Q3.
Let $A = LU$ be the $LU$ factorization of $A$. Which of the following are true?
(a) If $A$ is square, then $A$ is invertible.
(b) If $A$ is of size $m \times n$, then $m \geq n$
(c) $Ax=b$ is consistent $\forall b$

Answer: all false, all have counterexamples (see slides).

### Other
- any unit lower triangular matrix is invertible (which is row equivalent to identity matrix)
$$
L^{-1}L = I_n \text{ s.t. } Ly = b \to L^{-1}(Ly) = (L^{-1})b 
$$
- Permutation matrix: do some shuffling if there is no $LU$ matrix (not in scope of MA1522)

---
### Notation
- `~` :  the swiggle is used to represent corresponding operations