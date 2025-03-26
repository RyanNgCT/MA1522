### Finding the basis for $row(A)$
- Reduce $A$ into RREF form
- Non-zero rows of $R =$ a basis for $row(A)$
- works since row operations preserve the row space (is a critical fact for this theorem)
- basis for rows of $A$ must be taken from the rows of the RREF and **not from** $A$ itself.
	- suppose we want a basis that is from the original matrix $A$
		- can go about it by transposing

### Challenge 1 in Section 4.1
- Could have taken the original rows of $A$ (i.e. the Non-RREF form) as the basis
- Why is this so?
	- We can use span
		- dimension is $3$
		- there are only $3$ vectors originally, if they are linearly independent $\implies$ basis for the subspace

	- Alternatively: We know $dim(V) = n$ (it might be an easier method)
		- if we have a set of $n$ vectors in $\mathbb{R}^n$
		- Definition of Basis (recap)
			- span
			- independence
		- Because $B = {u_1, u_2, \ldots, u_n}$, so in this settings we need to check for either span or independence 

### Algorithm of Finding a Basis for the Column Space
- Find a basis of $\text{Col(A)}$
- Identify columns of $A$ that can form a basis of $\text{Col(A)}$
	- instead of the columns of the RREF(A)
	- "go back to the original matrix A" for the basis vectors

**Steps**
1. Reduce $A$ to its RREF form, notated as $R$
2. The columns of $A$ corresponding to the pivot columns in $R$ form a basis for $\text{Col(A)}$
- basis for column space method works since row operations preserve linear relations between columns
- suffices to just reduce the matrix to REF and do step $2$, instead of RREF (since we only need to identify pivot columns)
- Back to the row space of $A$, if we apply the above algo for $A^T$, we obtain $\text{Col\((A^T)\)}$

**Preserving the Linear relations of columns**
- If $A$ has $R_1 = \frac{1}{2}R_2$, then $R$ would also have the same relation.

### Challenge 2 in Section 4.1
- can choose anything other than $\{v_1, v_2\}$, because they are linearly dependent
- know that $dim(Col(A)) = 2 \implies$ can just check that any $2$ such columns are linearly independent
	- besides the above condition
	- by reducing $A$ to RREF/REF form, to be able to identify $2$ pivot columns (how we derive that $v_1, v_2$ are dependent)
		- for $v_4$ and $v_5$, might be good to reduce a few more steps to make the pivot columns more obvious.

### Notes
- row operations **do not preserve** column space
- row operations **do not preserve** linear relations between rows.

### Section 4.1 Question 1
Part i) unlike the algo, the columns are picked from the RREF form $R$, instead of from $A$. $\begin{pmatrix}1 & 0 & 0\end{pmatrix}$
Part ii) We can see that first two rows of $R$ (i.e. the RREF form of $A$) are linearly independent, can we imply that first two rows of $A$ are also linear independent?

### Null Space
- null space $\implies$ the solution space of zeroes

> The **nullspace** of a $m \times n$ matrix $A$ is the solution space to the homogeneous system $Ax = 0$ with coefficient matrix $A$. It is denoted as:
> $Null(A) = \{v \in \mathbb{R}^n | Av = 0\}$

### Section 4.1 Question 2
- assign parameters $r, s, t$ to the non-pivot columns
- obtain the general solution in the form $x = r \cdot \begin{pmatrix}a_1 \\ a_2 \\ a_3\end{pmatrix} + s \cdot \begin{pmatrix}b_1 \\ b_2 \\ b_3\end{pmatrix} + t \cdot \begin{pmatrix}c_1 \\ c_2 \\ c_3\end{pmatrix}$
- the above vectors form

### Rank
- row space and column space are totally different, but somehow they have the same dimension
$$
\text{rank(A)} = \text{dim(Col(A))} = \text{dim(Row(A))}
$$

### Challenge 1 in Section 4.2
Prove that $Ax =b$ is consistent $\iff rank(A) = rank((A | B))$ 
- consistent $\implies$ it has a valid solution to $x$
- $A = \begin{pmatrix}v_1 & v_2 \ldots & v_n\end{pmatrix}$, where $v_i$ are column vectors.
$$
\begin{aligned}
&\begin{pmatrix}v_1 & v_2 & \ldots & v_n\end{pmatrix} \cdot \begin{pmatrix}c_1 \\ c_2\\ \vdots \\ c_n\end{pmatrix} = b \\\\
&(\implies) \\
&1. \quad c_1v_1 + \ldots + c_nv_n = b, \text{ where }b \in \text{Col(A)} \\
&2. \quad \therefore  \:\text{rank(A)} = \text{dim(Col(A))} = \text{dim(Col(A | B))} = \text{rank((A | B))} \\\\
&(\impliedby) \\
& 1. \quad \text{Let \(W\) be a set of basis of Col(A)} \implies W \text{ linearly independent and also } W \subseteq \text{Col(A)}
\end{aligned}
$$

### Section 4.2 Question
Since the e.r.o. does not change the row space, 


### Challenge 2 in Section 4.2
Want to prove:
$$
rank(A + B) \leq rank(A) + rank(B)
$$
The proof is too complicated for the reader.

### Challenge 3 in Section 4.2
- using an $m \times n$ matrix s.t. $\text{rank(A)} = m$. Suppose $m \gt n$
- reasoning behind (1) holds because of the equivalent statements of full rank
- Dimension of row $=$ Dimension of columns $\implies$ can use the equivalent statements of rank (with the condition of $m \geq n$)
- mistake in argument: Using the assumption of $m \gt n$ to imply full rank $=$ # rows
	- can only use the fact that when we use the assumption of $m \gt n$ to imply full rank $=$ # **columns**

