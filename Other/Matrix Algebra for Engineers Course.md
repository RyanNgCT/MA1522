### Matrix Definitions: Defn of a Matrix
- usually use the symbol $x$ to represent a column vector and hence its elements are $x_i, i \in \mathbb{Z}^+$

### Matrix Definitions E1: Construct some Matrices
The diagonal of a matrix $A$ are the entries $a_{ij}​$ where $i=j$.

(a) Write down the three-by-three matrix with ones on the diagonal and zeros elsewhere.
$n = 3$
$$
A_1 = \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix} = I_3
$$

(b) Write down the three-by-four matrix with ones on the diagonal and zeros elsewhere.
$m = 3, \: n = 4$
$$
A_2 = \begin{pmatrix}
1 & 0 & 0 & 0\\
0 & 1 & 0 & 0\\
0 & 0 & 1 & 0
\end{pmatrix}
$$

(c) Write down the four-by-three matrix with ones on the diagonal and zeros elsewhere.
$m = 4, \: n = 3$
$$
A_3 =
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
0 & 0 & 0
\end{pmatrix}
$$
**Note:** While *all* the matrices above are in Row-Echelon Form, only $A_1$ qualifies as identity matrix, where $n = 3$
### Matrix Definitions: Addition and Multiplication of Matrices
1. Matrix Addition: simply add the corresponding terms, while ensuring that the matrices involve have the same dimensionality.
$$
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix} + 
\begin{pmatrix}
e & f \\
g & h
\end{pmatrix} =
\begin{pmatrix}
a+d & b+f \\
c+g & d+h
\end{pmatrix}
$$
2. Scalar Multiplication: multiple each term of the matrix by the constant $k, \: \forall k \neq 0$
$$
k
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix} =
\begin{pmatrix}
ka & kb \\
kc & kd
\end{pmatrix} 
$$
3. Matrix Multiplication: we have to do it quite specifically. Ensure that no. of columns in $A =$ no. of rows in $B$. 
	- only works if $A$ is $m \times n$ and $B$ is of dimension $n \times p$. Resultant matrix will be of dimension $m \times p$.
	- matrices **do not commute** under multiplication.
	$$
	\begin{aligned}
	B_1 = \begin{pmatrix}
	a & b \\
	c & d
	\end{pmatrix}
	\begin{pmatrix}
	e & f \\
	g & h
	\end{pmatrix} &=
	\begin{pmatrix}
	ae + bg & af + bh \\
	ce + dg & cf + dh
	\end{pmatrix} \\ \\
	B_2 = \begin{pmatrix}
	e & f \\
	g & h
	\end{pmatrix}
	\begin{pmatrix}
	a & b \\
	c & d
	\end{pmatrix}
	&= 
	\begin{pmatrix}
	ea + fc & eb + fd \\
	ga + hc & gb + hd
	\end{pmatrix} \quad \text{and since order of element-wise multiplication commutes,} \\ \\
	&=
	\begin{pmatrix}
	ae + cf & be + df \\
	ag + ch & bg + dh
	\end{pmatrix} \quad \text{with alphabetical order preserved.} \\ \\
	\therefore  \: & \boxed{\: B_1 \neq B_2}
	\end{aligned}
	$$

	- The general formula for matrix multiplication: 
	$$
	\begin{aligned}
	\text{For } c_{ij} \in C,\\
	c_{ij} &= \sum_{k=1}^n a_{ik}\:b_{kj} \quad\text{where we sum by the indices of \(k\).}
	\end{aligned}
	$$

### Matrix Definitions E2a: Matrix Addition and Multiplication
We define the matrices:
$$
\begin{aligned}
A = \begin{pmatrix}
2 & 1 & -1 \\
1 & -1 & 1 
\end{pmatrix}, \:
B = \begin{pmatrix}
4 & -2 & 1 \\
2 & -4 & -2 
\end{pmatrix}, \:
C = \begin{pmatrix}
1 & 2 \\
2 & 1 
\end{pmatrix}, \:
D = \begin{pmatrix}
3 & 4 \\
4 & 3 
\end{pmatrix}, \:
E = \begin{pmatrix}
1 \\
2
\end{pmatrix}
\end{aligned}
$$
Then, compute the following:
$$
\begin{aligned}
\text{(a) } B−2A \\
B - 2A &= 
\begin{pmatrix}
4 & -2 & 1 \\
2 & -4 & -2 
\end{pmatrix} - 2
\begin{pmatrix}
2 & 1 & -1 \\
1 & -1 & 1 
\end{pmatrix} \\
 &= 
 \begin{pmatrix}
 4-4 & -2-2 & 1-(-2) \\
 2-2 & -4-(-2) & -2-2
 \end{pmatrix} \\
 &=
\begin{pmatrix}
0 & -4 & 3 \\
0 & -2 & -4
\end{pmatrix}
\\\\

\text{(b) } 3C−E \\
3C &= 3 
\begin{pmatrix}
1 & 2 \\
2 & 1 
\end{pmatrix} \\
&= \begin{pmatrix}
3 & 6 \\
6 & 3 
\end{pmatrix} \\
&\text{Since 3C and E are of different sizes, thus solution d.n.e.}
\\\\

\text{(c) } AC \\
&\text{A is of size \(2 \times 3\), while C is of size \(2 \times 2\). Since 3 \(\neq\) 2, solution d.n.e.}
\\\\
\text{(d) } CD \\
CD &= \begin{pmatrix}
1 & 2 \\
2 & 1 
\end{pmatrix}
\begin{pmatrix}
3 & 4 \\
4 & 3 
\end{pmatrix} \\
&= 
\begin{pmatrix}
1(3)+2(4) & 1(4)+2(3)\\
2(3)+1(4) & 2(4)+1(3)
\end{pmatrix} \\
&= 
\begin{pmatrix}
11 & 10\\
10 & 11
\end{pmatrix}
\\\\
\text{(e) } CB \\
CB &= \begin{pmatrix}
1 & 2 \\
2 & 1 
\end{pmatrix}
\begin{pmatrix}
4 & -2 & 1 \\
2 & -4 & -2 
\end{pmatrix} \\
&= 
\begin{pmatrix}
1(4)+2(2) & 1(-2)+2(-4) & 1(1)+2(-2)\\
2(4)+1(2) & 2(-2)+1(-4) & 2(1)+1(-2)
\end{pmatrix} \\
&=
\begin{pmatrix}
8 & -10 & -3 \\
10 & -8 & 0
\end{pmatrix}
\\\\
\end{aligned}
$$
### Matrix Definitions E2b: $AB=AC$ Does Not Imply $B=C$
To show that $AB=AC \rlap{\quad\not}\implies B = C:$

$$
\begin{aligned}
AB &= \begin{pmatrix} 1 & 2 \\ 2 & 4 \end{pmatrix}\begin{pmatrix} 2 & 1 \\ 1 & 3 \end{pmatrix}\\
&= \begin{pmatrix} 1(2)+2(1) & 1(1)+2(3) \\ 2(2)+4(1) & 2(1)+4(3) \end{pmatrix} \\
&= \begin{pmatrix} 4 & 7 \\ 8 & 14 \end{pmatrix} \\
\text{and} \\
AC &= \begin{pmatrix} 1 & 2 \\ 2 & 4 \end{pmatrix}\begin{pmatrix} 4 & 3 \\ 0 & 2 \end{pmatrix} \\
&= \begin{pmatrix} 1(4)+2(0) & 1(3)+2(2) \\ 2(4)+4(0) & 2(3)+4(2) \end{pmatrix} \\
&= \begin{pmatrix} 4 & 7 \\ 8 & 14 \end{pmatrix} \\\\
&\therefore AB = AC \text{ by the above computation.} \\\\
\text{However, } \\
&B = \begin{pmatrix} 2 & 1 \\ 1 & 3 \end{pmatrix} \text{ and } C= \begin{pmatrix} 4 & 3 \\ 0 & 2 \end{pmatrix}, \text{where } \forall a_{ij} \in A \neq b_{ij} \in B.\\\\
&\text{Thus, } AB=AC \rlap{\quad\not}\implies B = C. \text{(shown)}
\end{aligned}
$$
### Matrix Definitions: Matrix Multiplication Does Not Commute
$$
\begin{aligned}
A &= \begin{pmatrix} 1 & 1 & 1 \\ 1 & 2 & 3 \\ 1 & 3 & 4 \end{pmatrix} \text{ and } 
D = \begin{pmatrix} 2 & 0 & 0 \\ 0 & 3 & 0 \\ 0 & 0 & 4 \end{pmatrix}. \\\\

\text{And so:} \\
AD &= \begin{pmatrix} 1 & 1 & 1 \\ 1 & 2 & 3 \\ 1 & 3 & 4 \end{pmatrix}\begin{pmatrix} 2 & 0 & 0 \\ 0 & 3 & 0 \\ 0 & 0 & 4 \end{pmatrix} \\
&= \begin{pmatrix} 1(2)+1(0)+1(0) & 1(0)+1(3)+1(0) & 1(0)+1(0)+1(4) \\
1(2)+2(0)+3(0) & 1(0)+2(3)+3(0) & 1(0)+2(0)+3(4) \\
1(2)+3(0)+4(0) & 1(0)+3(3)+4(0) & 1(0)+3(0)+4(4) 
\end{pmatrix} \\
&= \begin{pmatrix} 2 & 3 & 4 \\ 2 & 6 & 12 \\ 2 & 9 & 16 \end{pmatrix} \\\\
DA &= \begin{pmatrix} 2 & 0 & 0 \\ 0 & 3 & 0 \\ 0 & 0 & 4 \end{pmatrix} \begin{pmatrix} 1 & 1 & 1 \\ 1 & 2 & 3 \\ 1 & 3 & 4 \end{pmatrix} \\ &= \begin{pmatrix} 2(1)+0(1)+0(1) & 2(1)+0(2)+0(3) & 2(1)+0(3)+0(4) \\ 0(1)+3(1)+0(1) & 0(1)+3(2)+0(3) & 0(1)+3(3)+0(4) \\ 0(1)+0(1)+4(1) & 0(1)+0(2)+4(3) & 0(1)+0(3)+4(4) \end{pmatrix} \\ &= \begin{pmatrix} 2 & 2 & 2 \\ 3 & 6 & 9 \\ 4 & 12 & 16 \end{pmatrix} \\\\
&\therefore \:, \boxed{AD \neq DA} \text{ and hence matrix multiplication does not commute.}
\end{aligned} \\\\
$$

### Matrix Definitions: Special Matrices
1. Zero Matrix: can be of $m \times n$ size or dimensionality, denoted as $0_{m \times n}$.
	- Shows up in the equation $Ax = 0$, where $x$ is a column vector.
	- Plays the role of zero in multiplication (effectively returns $0_{m \times n}$ for any matrix multiplied to it)

2. Identity Matrix: plays the role of $1$ in multiplication.
	- always of the size $n \times n$ (i.e. a square matrix of **order n**)
	- special commutative property: Given a matrix $A, AI = A = IA$
	- refer to definition in Week 2 material

3. Diagonal Matrix: has only elements on the diagonal, but zero elsewhere, denoted as $D_n$.
	- diagonal entries $d_1, d_2, \ldots, d_n$ are said to be the diagonal entries.
	- all other entries **not along the main diagonal** $= 0$ (we don't follow the other textbook's definition).
	$$
	D_3 = \begin{pmatrix} d_1 & 0 & 0 \\ 0 & d_2 & 0 \\ 0 & 0 & d_3 \end{pmatrix}
	$$
4. Banded Matrix (not covered in MA1522): matrix with not only one diagonal (can have multiple ones).
	- has more than one (main) diagonal
	$$
	\text{Example of a Tri-diagonal Matrix,}\:
	B_3 = \begin{pmatrix} d_1 & a_1 & 0 \\ b_1 & d_2 & a_2 \\ 0 & b_2 & d_3 \end{pmatrix}
	$$

5. Triangular Matrix: A square matrix with elements either above or below the diagonal.
	- the valid-non zero elements are in the upper (lower) part of the matrix
	$$
	\begin{aligned}
	\textbf{Upper Triangular Matrix:} \\
	U_3 &= \begin{pmatrix} * & * & * \\ 0 & * & * \\ 0 & 0 & * \end{pmatrix} \\\\
	\textbf{Lower Triangular Matrix:} \\
	L_3 &= \begin{pmatrix} * & 0 & 0 \\ * & * & 0 \\ * & * & * \end{pmatrix}
	\end{aligned}
	$$

### Matrix Definitions E3a: $AB=0$ When $A$ and $B$ Are Not zero
Let $A = \begin{pmatrix} -1 & 2 \\ 4 & -8 \end{pmatrix}.$ Construct a two-by-two matrix $B$ such that $AB$ is the zero matrix. Use *two different nonzero columns* for $B$.
$$
\begin{aligned}
A &= \begin{pmatrix} -1 & 2 \\ 4 & -8 \end{pmatrix} \\
B &= \begin{pmatrix} z_1 & z_2 \\ z_3 & z_4 \end{pmatrix} \\\\
AB &=  0_{2 \times 2} \\
&= \begin{pmatrix} -1 & 2 \\ 4 & -8 \end{pmatrix}\begin{pmatrix} z_1 & z_2 \\ z_3 & z_4 \end{pmatrix} \\
&= \begin{pmatrix} (-1)(z_1)+2(z_3)  & (-1)(z_2)+(2)(z_4) \\ 
4(z_1)+(-8)(z_3) & 4(z_2)+(-8)(z_4) \end{pmatrix} \\\\
\text{So, we have:} \\
&2z_3 - z_1 = 0 \implies z_1 = 2z_3\\
&2z_4 - z_2 = 0 \implies z_2 = 2z_4\\
&4z_1 - 8z_3 = 0 \\
&4z_2 - 8z_4 = 0 \\\\
&\text{We can pick arbitrary values of \(z_1, z_2, z_3\) and \(z_4\), provided they are different.} \\
&\text{Initial idea: \(z_1 = z_2 = 2\) and \(z_3 = z_4 = 1\) but \(z_1 \neq z_2\) and \(z_3 \neq z_4\) as required by the question, so the final matrix is:} \\
&\boxed{B = \begin{pmatrix} 2 & -2 \\ 1 & -1 \end{pmatrix}}
\end{aligned}
$$

### Matrix Definitions E3b: Product of Diagonal Matrices
Verify that $\begin{pmatrix} a_1 & 0 \\ 0 & a_2 \end{pmatrix}\begin{pmatrix} b_1 & 0 \\ 0 & b_2 \end{pmatrix} = \begin{pmatrix} a_1 b_1 & 0 \\ 0 & a_2 b_2 \end{pmatrix}.$ Prove in general that the product of two diagonal matrices is a diagonal matrix, with elements given by the product of the diagonal elements.

$$
\begin{aligned}
	\begin{pmatrix} a_1 & 0 \\ 0 & a_2 \end{pmatrix}
	\begin{pmatrix} b_1 & 0 \\ 0 & b_2 \end{pmatrix} &= 
	\begin{pmatrix} (a_1)(b_1)+(0)(0) & (a_1)(0)+(0)(b_2) \\(0)(b_1)+(a_2)(0) & (0)(0)+(a_2)(b_2)\end{pmatrix} \\\\
	&= \begin{pmatrix} a_1 b_1 & 0 \\ 0 & a_2 b_2 \end{pmatrix}
\end{aligned}
$$
Proof not continued as we have different defn.

---
### Transpose and Inverses: Transposing Matrix
We can say the transpose of matrix $A, A^T$is when the rows of the matrix become the columns and the columns become the rows.
- a matrix of size $m \times n$ is **transposed** to become a matrix of $n \times m$ instead (size is "flipped").
- transposing the matrix can be seen as a **reflection** along the main diagonal.
	$$
	\begin{aligned}
	A = \begin{pmatrix} 
	a_{11} & a_{12} & \cdots & a_{1n} \\ 
	a_{21} & a_{22} & \cdots & a_{2n} \\ 
	\vdots & \vdots & \ddots & \vdots \\ 
	a_{m1} & a_{m2} & \cdots & a_{mn} 
	\end{pmatrix}
	\text{  becomes  }
	A^T = \begin{pmatrix} 
	a_{11} & a_{21} & \cdots & a_{m1} \\ 
	a_{12} & a_{22} & \cdots & a_{m2} \\ 
	\vdots & \vdots & \ddots & \vdots \\ 
	a_{1n} & a_{2n} & \cdots & a_{mn} 
	\end{pmatrix}
	\end{aligned}
	$$
#### Properties of Transpositions
In other notation, each element, $a_{ij}$ goes through the phase of transposition to become $a_{ji}$, i.e. the indices get swapped.
$$
a^{\scriptscriptstyle{T}}_{ij} = a_{ji}
$$
We can also make the observation that we obtain the original matrix after two such transpositions
$$
(A^T)^T = A
$$
In addition, $(A + B)^T = A^T + B^T$ (if both $A$ and $B$ of order $n$).

Another rule is that $(AB)^T = B^T \cdot A^T$ (reverse the order of multiplication).
#### Other Special Matrices
1. Symmetric Matrix: a matrix is of this type if $A^T = A$.
2. Skew-Symmetric Matrix a matrix where $A^T = -A$ and the **diagonal entries are zero** (since $+0 = -0$).
$$
A = \begin{pmatrix}0 & b & c \\ -b & 0 & e\\ -c & -e & 0\end{pmatrix}
$$

### Transpose and Inverses: Inner (Dot) and Outer products
##### The Inner Product
Given two column vectors $U =\begin{pmatrix}u_1 \\ u_2 \\ u_3\end{pmatrix}, V =\begin{pmatrix}v_1 \\ v_2 \\ v_3\end{pmatrix}$,
1. The dot (or inner) product *between two vectors* is calculated as: $U^TV$ (since row and columns don't line up in this case to produce a well-defined result).
	$$
	\begin{aligned}
	U^TV &= \begin{pmatrix}u_1 & u_2 & u_3\end{pmatrix}\begin{pmatrix}v_1 \\ v_2 \\ v_3\end{pmatrix} \\
	&= u_1v_1 + u_2v_2 + u_3v_3 \\\\
	&\text{In the case where \(U^TV\) = 0} \implies u, v \textbf{ are orthogonal.}
	\end{aligned}
	$$
2. The **norm of the vector** $U$, $\| U \|$ is the length of $U$.
	$$
	\begin{aligned}
	\| U \| &= (U^T \cdot U)^{\frac{1}{2}} \\
	&= \sqrt{(u_1)^2 + (u_2)^2 + (u_3)^2 + \ldots + (u_i)^2}
	\end{aligned}
	$$

3. We say that $U$ is normalized if $\| U \| = 1$ (i.e. the unit vector).
4. If two vectors are **orthogonal** (i.e. perpendicular) **and normalized**, then the vectors are then said to be **orthonormal**.
	1. a set of vectors has this property.

##### The Outer Product
Given two column vectors $U =\begin{pmatrix}u_1 \\ u_2 \\ u_3\end{pmatrix}, V =\begin{pmatrix}v_1 \\ v_2 \\ v_3\end{pmatrix}$,
1. The outer product between two vectors is calculated as: $UV^T$
	$$
	\begin{aligned}
	UV^T &= \begin{pmatrix}u_1 \\ u_2 \\ u_3\end{pmatrix}\begin{pmatrix}v_1 & v_2 & v_3\end{pmatrix} \qquad \text{(Of dimensionality \(3 \times 3\))}\\
	&= \begin{pmatrix} u_1 v_1 & u_1 v_2 & u_1 v_3 \\ u_2 v_1 & u_2 v_2 & u_2 v_3 \\ u_3 v_1 & u_3 v_2 & u_3 v_3 \end{pmatrix} \\\\
	\end{aligned}
	$$
### Transpose and Inverses: Inverse of a Matrix
If a matrix is **invertible**, we mean that it has a corresponding inverse matrix.
- not all matrices are invertible.

$A \cdot A^{-1} = I_n = A^{-1} \cdot A$, where the order commutes. 

#### Properties of Invertible Matrices
1. For $A$ to be invertible, it has to be a square matrix of **order $n$**.
2. The inverse of the product of two square matrices is:
$$
(AB)^{-1} = B^{-1}A^{-1}
$$
3.  *Theorem:* Inverse of the transposed matrix
$$
(A^T)^{-1} = (A^{-1})^T
$$

Strategy is to use the homogeneous equations to solve for variables $x, y, z, \ldots$
We can use the formula $\text{det}A = ad - bc$