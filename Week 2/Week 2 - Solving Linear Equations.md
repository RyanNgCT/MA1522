- First need to write the system in standard form (variables on one side and constants on the other side)
- Secondly, we need to reduce either to REF or RREF and use Gaussian Elimination
- Thirdly, we can decide the consistency of the system
	- consistent: has solutions
	- inconsistent: no solutions (is contradictory)
		- If the last column is a pivot column $\implies$ inconsistent solution (i.e. last column should be a  non-pivot column)

- parameters chosen should be **different** from the variables used, such as $s, t \in \mathbb{R}$

### Consistency
- **No solution:** if bottom row's LHS is all zeros but the RHS is $\neq 0 \implies$ not consistent / no solution
- **Unique Solution:** all the columns of coefficients of the matrix are pivot columns (one equation for each variable)
	- If # variables $\geq$ # equations $\implies$ then it is not a unique solution (i.e. not possible for 1 solution only)
	- There are not enough equations for each variable

- **Infinitely Many Solutions:** when there is a non-pivot column before the bar (i.e. in the variable domain)
	- set some parameters
	- \# of parameter = # of non-pivot columns before the bar

### Parameters and Solutions
- easy to obtain solutions of augmented matrix is in REF (back-substitution) or RREF (directly read)
- linear system is inconsistent $\iff$ RHS (last column) of the matrix in REF is a pivot column (see above)
- assign parameters to the variables corresponding to the non-pivot columns in the LHS.

#### Example: 3 variables, general solution with 2 parameters
Step 1: Transform Equation to standard form. $x + 2y + 3z = 4 \implies$
$$
\left(
\begin{array}{ccc|c}
1 & 2 & 3 & 4
\end{array}
\right)
$$
Step 2: Make sure they are all non-pivot columns

Step 3: General solution with 3 parameters, need 3 non-pivot columns
- Use degenerated case
$$
\left(
\begin{array}{ccc|c}
0 & 0 & 0 & 0
\end{array}
\right)
$$
- In the case where degenerated case not applicable, then not possible

### REF and RREF
- augmented matrix in REF
	- zeros sink the the bottom, no need to check if all are non-zero rows
	- leading entries are further to the right

- augmented matrix in RREF
	- REF as the base condition (on top of the REF conditions)
	- leading entries are one
	- in each pivot column, all entries except leading entry is zero.
#### Slide Example:
**Q1: What are the possible value of $g$**
A: Violates leading entry further to the right rule. 
- Since the first entry of row number two is 0, the leading entry can either be $e, e \neq 0$, or $f$ if $e = 0, f \neq 0$ or the the fourth entry, if $e = f = 0$. 
- By condition 2 of the definition of REF, the leading entry of the third row cannot be the second element. $\therefore g = 0$.

**Q2: If the matrix is in REF and h = 0, what are the possible values of $i$?**
A: There are many possible values, but we need to check if it is already a pivot column
- need to ask oneself if column 4, row 2 is already a leading entry (it is dependent on $e$ and $f$).
	- no? $\implies i$ can be arbitrary
	- yes? $\implies i$ must be zero. 

**Q3: If the matrix is in RREF and $f = -1$ what are the possible values of $e$?**
- $e \neq 0$ because the leading entry is $-1$ otherwise
- By condition 3, $e$ must be the leading entry and $\therefore \: e = 1$

**Q4: If the matrix is in RREF and $f = -1$ what are the possible values of $h$ and $i$?**
By Q1, $g = 0$. Now $h$ cannot be a leading entry because of condition 4 (since $f = -1$)

### Elementary Row Operations
Three elementary types that Gaussian Elimination uses:
1. Exchanging two rows, $R_i \leftrightarrow R_j$
2. Adding a multiple of a row to another, $R_i + cR_j, \: c \in \mathbb{R}$
	1. $R_i := R_i + cR_j \implies$ the constant $c$ is applied to the value being added
	2. don't swap the order
3. Multiplying a row by a nonzero constant, $aR_j, \: a \neq 0$

Reverse of these operations:
1. Reverse if just exchanging the rows back
2. Subtracting a multiple of a row to another, $R_i - cR_j, \: c \in \mathbb{R}$
3. Reverse of multiplying (i.e. dividing by $a$), obtaining the reciprocal of the constant $\frac{1}{a}R_j, a \neq 0$
#### Slide Example
**Q1: What is the reverse of the elementary row operation $R_2 -\frac{1}{2}R_1$**

### Section 1.2 Challenge
For matrix $n \times m$
Q1: 
$$
\begin{aligned}
P &= \{\text{pivot columns}\}, \:  N = \{\text{non-zero rows}\} \\
\# P &= \# N
\end{aligned}
$$

Q2:
- ask the question: is $m = n$?
	- if $m = n, \: \#\text{ non-piv rows} = \#\text{ zero rows}$ 
	-  if $m \neq n, \: \#\text{ non-piv rows} \neq \#\text{ zero rows}$ 
$$
m  - \# P = n = \#N
$$
### Section 1.4 Question
1. We can still perform Gaussian Elimination. Using cases, the unknown coefficient, $a = 0 \text{ and } a \neq 0$.
	 - need to be careful when dividing something by constant $a$, cannot divide by zero (operation invalid in first case that $a = 0$).

2. Can also swap row $1$ with row $2$ (performing some of the operations involved in Gaussian Elimination)
	- might be easier as we split into cases fewer times.

### Section 1.4 Challenge
- Is the REF and RREF of matrix $A$ unique? $\implies$ are there two different combinations  of the Gaussian Elimination operations.
	- *REF is not unique (can have multiple), RREF is unique*

- **Lemma 2:** If we have two matrices $A$ and $B$ in RREF for two homogenous system of $m$ equations, then the two systems have exactly the same solutions and thus $A = B$.
### Misc Notes
We are not tested on sophisticated proofs






