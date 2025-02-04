- how to find the linear set of vectors to form another vector.
- determine whether matrix is invertible, find its inverse.

### Question 1
(a)
$$
\begin{aligned}
A \implies m \times n \\
B \implies n \times p \\
Bx = 0 \text{  has infinitely many solutions.} \\
\therefore ABx = 0
\end{aligned}
$$

Possibilities: 0 solution or $\infty$ many solutions

(b)
Consider $u$ s.t. $Bu = 0$
$$
\begin{aligned}
AB \cdot u = A(Bu) = A0 = 0 \\
\therefore \: \text{Solution set of } B \cdot x=0 \subset AB \cdot x = 0
\end{aligned}
$$

(c)
$$
\begin{aligned}
\text{Suppose \(Bx = 0\) has only the trivial solution (i.e. all zeroes)} \\
\text{Counterexample: } \boxed{A = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix}, \: B = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}}
\end{aligned}
$$


### Question 2a
In this course, we only find invertibility for square matrices.
$A$ is of $4 \times 3$ dimensionality, however, we want $A$ to be $3 \times 3$ identity matrix form.

Take $X$ as the columns where $[Ax_1 \: Ax_2 \: Ax_3]$ where $x_i$ are column vectors containing the coefficients.

So $Ax_1 = w_1 \cdot a_1 + w_2 \cdot a_2 + w_3 \cdot a_3$

Has only one general solution.

### Question 2b
For all the elementary row operations, we also have elementary column operations, but we are not concerned with that since we can just take the transpose of the matrix and thereafter perform e.r.o., to obtain the same effect.
$$
\begin{aligned}
YB = I_3 \iff (YB)^T = (I_3)^T = I_3 \\
\therefore B^TY^T = I_3
\end{aligned}
$$


### Question 3c
$$
A = \begin{bmatrix} 1 & -1 & 0 \\ 2 & -2 & 1 \\ 1 & 2 & 3 \end{bmatrix} \longrightarrow I_3
$$
How to use e.r.o. for $n \times n$ matrix?
1. Make identity matrix of dimensionality $i \times j$
2. Add $k$ at $i^{th}$ row, $j^{th}$ column (or $A_{ij} = k$)
3. Set $A_{ii} = A_{jj}$

$I_3 = E_6 \ldots E_2 E_1 A$
So $A = (E_1)^{-1}(E_2)^{-1} \ldots (E_6)^{-1}I_3$


Rest of the parts left as an exercise for the reader.

### Question 4
Do elimination to find invertible matrices
Square matrix only invertible if **REF** = identity matrix.

### Question 5
Goal: transform to its REF form first

**Steps**
$R_2 - aR_1, R_3 - a^2R_1$
$R_3 - (b + a)R_2$

In the resultant matrix, $A_{3,3} \neq 0$  and $A_{2, 2} \neq 0$, $\therefore a \neq b, b \neq c \text{ and } a \neq c$

### Question 6
(a) $A^2 = AA \ldots = 0$

(b) $A^3 = 0$
So $I - A^3 = (I - A)(I + A + A^2)$

Follows the formula: $(1- x^n) = (1 - x)(1+ x + x^2 + \ldots + x^{n-1})$ 

(c) $A^n = 0$
$I = I - A^n = (I - A)(I + A + A^2 + \ldots + A^{n-1})$