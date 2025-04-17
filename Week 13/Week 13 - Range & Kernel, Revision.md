### Linear Transformation
Linear Transformation: $\{T: T: \mathbb{R}^n \to \mathbb{R}^m\}$
- Matrices and Linear Transformations have a one-to-one correspondence
	- linear transformation can be thought of as a problem that matrices have (are uniquely represented by a standard matrix)
	- matrix terminology and expressions can be used to describe transformations as well

- can use matrices to describe linear transformation
### Range
- is the subspace of the codomain
- $R(T) = T(\mathbb{R}^n) = \{v \in \mathbb{R}^n \: | \: v = T(u) \text{ for some } u \in \mathbb{R}^n\}$
### Kernel
> Let $T : \mathbb{R}^n \to \mathbb{R}^m$ be a linear transformation. The **kernel of $T$** is defined by $ker(T) = \{\textbf{u} \in \mathbb{R}^n | T(\textbf{u}) = 0\}$
- we have that $Nullity(T) = dim(ker(T)) = dim(Null(A)) = Nullity(A)$

- We get the zero vector $\textbf{0}, \textbf{0} \in W$ when mapping a subset of the vectors in the set $V$ to the set $W$ via function $T$
- essentially, need to solve the equation $T(\textbf{v}) = \textbf{0}_W$
	- find the values of the vector $\textbf{v}$, i.e. $v_i$
	- set of vectors that make $\textbf{v}$ the zero matrix is called the kernel
### Injectivity of L.T.
- if $T(u_1) = T(u_2) \implies u_1 = u_2$
- Property of Injective Linear Transformation: iff the kernel is **trivial**, i.e. $ker(T) = \{\textbf{0}\}$
#### Full Rank = \# Columns Theorem
Equivalent Statements for an $m \times n$ matrix $A$
(i) full rank, where the rank is equal to the number of **columns**, i.e. $rank(A) = n$
(vii) The linear transformation $T : \mathbb{R}^n \to \mathbb{R}^m$ defined by $A$ is **injective**
### Surjectivity of L.T.
- mapping is surjective or onto if $\forall \mathbb{v} \in \mathbb{R}^m$ (i.e. the codomain), $\exists \textbf{u} \in \mathbb{R}^n$ s.t. $T(\textbf{u}) = \textbf{v}$
#### Full Rank = \# Columns Theorem
Equivalent Statements for an $m \times n$ matrix $A$
(i) full rank, where the rank is equal to the number of **rows**, i.e. $rank(A) = m$
(vii) The linear transformation $T : \mathbb{R}^n \to \mathbb{R}^m$ defined by $A$ is **surjective**
### Bijectivity of L.T.
- for two sets $\mathbb{R}^n$ and $\mathbb{R}^m$, we have that $S$ is a mapping from $\mathbb{R}^n$ to $\mathbb{R}^m$ and $T$ is a mapping from $\mathbb{R}^m$ to $\mathbb{R}^n$
	- $T(S(\textbf{v})) = S(T(\textbf{v})) = \textbf{v}$

### Section 7.2 Question
**What are the rank and nullity of the linear transformations?**
(i) By observation, $ker(T) = \mathbb{R}^n$ and $R(T) = \{\textbf{0}\}$ and we have $rank(T) = 0$ and $nullity(T) = n$
(ii) By observation, we have the range to be $\mathbb{R}^n$ and the $ker(T) = 0$ and we have $rank(T) = n$ and $nullity(T) = 0$ (null space is zero because we only have the trivial solution)
### Section 7.2 Exercise 1
Let $T : \mathbb{R}^n \to \mathbb{R}^m$ be a linear transformation. Show that if $T$ is **injective**, then necessarily $n \leq m$

using (i) $\iff$ (vii) in the Full Rank = # Columns Theorem on Slide 36, we have $n = rank(A) \leq m$
(because $A$ is $m \times n \implies rank(A) \leq min\{n, m\}$)

- rank is equal to $dim(Col(A)) = dim(Row(A))$
- (recap) $nullity(A) + rank(A) =$ number of columns in $A$
### Section 7.2 Exercise 2
Let $T : \mathbb{R}^n \to \mathbb{R}^m$ be a linear transformation. Show that if $T$ is **surjective**, then necessarily $n \geq m$

using (i) $\iff$ (vii) in the Full Rank = # Rows Theorem on Slide 40, we have $n = rank(A) \leq m$

### Section 7.2 Exercise 3
- Linear Transformation $T : \mathbb{R}^n \to \mathbb{R}^m$ is bijective if it is **both** injective and surjective.
$$
\begin{aligned}
&\textbf{Equivalent Statements of Invertibility}\\\\
&\textbf{(i)}\ \mathbf{A} \text{ is \textcolor{blue}{invertible}.} \implies AB = BA = I_n\\
&\textbf{(ii)}\ \mathbf{A}^T \text{ is \textcolor{blue}{invertible}.} \\
&\textbf{(iii)}\ \text{(\textcolor{blue}{left inverse}) There is a matrix } \mathbf{B} \text{ such that } \mathbf{BA} = \mathbf{I}. \\
&\textbf{(iv)}\ \text{(\textcolor{blue}{right inverse}) There is a matrix } \mathbf{B} \text{ such that } \mathbf{AB} = \mathbf{I}. \\
&\textbf{(v)}\ \text{The \textcolor{orange}{reduced row-echelon form} of } \mathbf{A} \text{ is the \textcolor{orange}{identity matrix}.} \\
&\textbf{(vi)}\ \mathbf{A} \text{ can be expressed as a \textcolor{blue}{product} of \textcolor{orange}{elementary matrices}.} \\
&\textbf{(vii)}\ \text{The \textcolor{blue}{homogeneous system} } \mathbf{Ax = 0} \text{ has \textcolor{red}{only the trivial solution}.} \\
&\textbf{(viii)}\ \text{For \textbf{any} } \mathbf{b}, \text{ the system } \mathbf{Ax = b} \text{ has a \textcolor{blue}{unique solution}.} \\
&\textbf{(ix)}\ \text{The \textcolor{blue}{determinant} of } \mathbf{A} \text{ is \textcolor{red}{nonzero}, } \det(\mathbf{A}) \neq 0. \\
&\textbf{(x)}\ \text{The \textcolor{brown}{columns/rows} of } \mathbf{A} \text{ are \textit{\textcolor{brown}{linearly independent}}.} \\
&\textbf{(xi)}\ \text{The \textcolor{brown}{columns/rows} of } \mathbf{A} \text{ \textcolor{brown}{span} } \mathbb{R}^n. \\
&\textbf{(xii)}\ \text{\textcolor{blue}{rank}(} \mathbf{A} \text{) = n (\textcolor{brown}{\(\mathbf{A}\) has full rank}).} \\
&\textbf{(xiii)}\ \text{\textcolor{blue}{nullity}(} \mathbf{A} \text{) = 0.} \\
&\textbf{(xiv)}\ \text{0 is \textcolor{red}{not} an \textcolor{brown}{eigenvalue} of } \mathbf{A}. \\
&\textbf{(xv)}\ \text{The \textcolor{brown}{linear transformation} } T \text{ defined by } \mathbf{A} \text{ is \textcolor{red}{injective}.} \\
&\textbf{(xvi)}\ \text{The \textcolor{brown}{linear transformation} } T \text{ defined by } \mathbf{A} \text{ is \textcolor{red}{surjective}.}
\end{aligned}
$$

---
### Practice Problem 1a
- Given a matrix $A = L \begin{pmatrix}-1 & 1 & 7 & -1 \\ 0 & 4 & 12 & 2 \\ 0 & 0 & 0 & 1\end{pmatrix}$
	- find $A$

- we have that $dim(U) = dim(A)$
- medium difficulty

- we have that $L$ is a $3 \times 3$ unit lower triangular matrix
	- solve for $x, y, z$
$$
\begin{aligned}
A &= \begin{pmatrix}
1 & 0 & 0 \\ x & 1 & 0 \\ y & z & 1
\end{pmatrix}\begin{pmatrix}-1 & 1 & 7 & -1 \\ 0 & 4 & 12 & 2 \\ 0 & 0 & 0 & 1\end{pmatrix} \\\\
A \begin{pmatrix}1 \\ -1 \\ 1 \\ 1\end{pmatrix}  &= \begin{pmatrix}
1 & 0 & 0 \\ x & 1 & 0 \\ y & z & 1\end{pmatrix}
\begin{pmatrix}-1 & 1 & 7 & -1 \\ 0 & 4 & 12 & 2 \\ 0 & 0 & 0 & 1\end{pmatrix} \begin{pmatrix}1 \\ -1 \\ 1 \\ 1\end{pmatrix}  \\
&= \begin{pmatrix}4 \\ 14 \\ 17\end{pmatrix} \\\\
A \begin{pmatrix}0 \\ 1 \\ 0 \\ -1\end{pmatrix}  &= \begin{pmatrix}
1 & 0 & 0 \\ x & 1 & 0 \\ y & z & 1\end{pmatrix}
\begin{pmatrix}-1 & 1 & 7 & -1 \\ 0 & 4 & 12 & 2 \\ 0 & 0 & 0 & 1\end{pmatrix} \begin{pmatrix}0 \\ 1 \\ 0 \\ -1\end{pmatrix}  \\
&= \begin{pmatrix}2\\ 4 \\ 7\end{pmatrix}

\end{aligned}
$$

### Practice Problem 1b
- least square solution itself is not unique
- but if we project it them it is unique

- least square solution
	- for least square solution, if the solution is consistent then it is the actual solution (based on Week 10 Slide 15)

- alternative is to calculate $A^TA$ and use inverse (very tedious)
- is one of the more difficult question

### Practice Problem 3a
- singular value decomposition
	- characteristic polynomial $(x-3)(x-6)(x-10)$
- find $\Sigma$ in $\mathbf{A} = \textbf{U}\Sigma \textbf{V}^T$
	- eigenvalue of $\mathbf{A}^T\mathbf{A}$ are 3, 6, 10, reverse and square root to obtain the diagonal $\textbf{D}$
 $$
 \Sigma = \begin{pmatrix}\sqrt{10} & 0 & 0 \\ 0 &\sqrt{6} & 0 \\ 0 & 0 & \sqrt{3} \\ 0 & 0 & 0\end{pmatrix}
 $$
### Practice Problem 3b
- find $\textbf{U}$

### Practice Problem 3c
- use info in 3b to find $\mathbf{A}$.
### Problem 4
- linear transformation
	- write down the standard matrix of the linear transformation $T$
		- $\begin{pmatrix}1 &-1 & -2 \\ -2 & 2 & 2 \\ 0 & -1 & -1\end{pmatrix} \implies$ just write $T(e_1), T(e_2), T(e_3)$ 
	- find a nonzero vector in $\mathbb{R}^3$ s.t. $T(\textbf{u}) = \textbf{u}$. Explain how the answer is derived
		- Since $T(\textbf{u}) = \textbf{u} \implies (A - I)(u) = 0$
		- $I - A$ then RREF the result.
	- Find a vector $\textbf{u}$ s.t. $T(\textbf{u}) = \begin{pmatrix}5 \\-4 \\ 1\end{pmatrix}$ 
- easy difficulty