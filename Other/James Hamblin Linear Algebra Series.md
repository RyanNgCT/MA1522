## I. Introduction to Linear Algebra
- recognise linear equation and a system of linear equations
- identify solutions (or non-solutions) to the system
### Linear and Non-linear equations
> A **linear equation** is an equation that can be written in the form: $a_1x_1 + a_2x_2 + \ldots + a_nx_n = b$
- $a_i \in  [1, n]$ are the *coefficients*
	- possible for coefficients of variables to be $-1, 0$ or $1$ as well, depending on how the equation is written
		- can insert missing coefficient values (i.e. coefficient of $0$)
	- more generally, value of the coefficient is: $a_i \in \mathbb{R}$ (i.e. $\pi, \sqrt{2}$ etc.)
	
- $x_i \in [1,n]$ are the *variables*
- $b$ is the constant

The **standard form** of a linear equation, as mentioned previously, is:
$$
a_1x_1 + a_2x_2 + \ldots + a_nx_n = b
$$
- where the coefficients and variables are on one end
- constant value is on the other end
(from the above, we can write the same equation in different forms $\to$ perform some operation on both sides)

What makes a **non-linear** equation:
$$
\sqrt{x} + \frac{1}{y} = wz - 10
$$
- We don't have square roots of *variables* $\implies$ only square roots of coefficients are allowed
- We can't have division by variable (or reciprocals, i.e. $y^{-1}$)
- We can't have two variables multiplied to each other (should be in the form `coeff` $\times$ `variable`, and **NOT** `variable` $\times$ `variable`)

### Solutions of Linear Equations
> A **solution of a linear equation** is a value for each variable that makes the equation **true**.
- we can check solution of equations by substituting values back and confirming that equality holds true.

> A **system of linear equations** is a collection of $\geq 1$ linear equations involving the *same variables*

> A **solution of a system of linear equations** is a value for each variable that makes *each equation* simultaneously true.
- to check for valid solution(s) to system $\implies$ substitute each variable value into the equation and check that all the equations hold true.
---
## II. Solving Linear Systems by Elimination
- elimination method for solving systems of linear equations
- considering the triangular shape of a system, which is the primary goal of the elimination process

### Substitution Method Algorithm
- solve for one of the equations for **one** of the $n$ variables.
- substitute the solution into other equations, then repeat for as much as necessary until we have a value for the variable
- proceed to then "back-substitute" to find the values of the other variables
- key strategy when applied to back-substitution for REF form

##### Example 1
$$
\begin{aligned}
\textbf{Solve the system of equations} \\
\textbf{by substitution:} \\
&x + 2y = 10 \textemdash \: (1)\\
&0.5x -3y = -11\textemdash\:(2)\\\\

\textbf{Sln: }\\
&x = 10 - 2y \\
&\text{\textit{subs x = 10 - 2y into (2)}} \\
&0.5(10 - 2y) - 3y = -11 \\
&5 - y - 3y = -11 \\
&-4y = -16 \\
&\therefore \: y = 4 \\
&\text{\textit{subs y = 4 into (1)}} \\
& x = 10 - 2(4) \\
&\therefore \: x = 2
\end{aligned}
$$

### Elimination Method Algorithm
- allows us to scale equations by multiplying both sides by an appropriate number
- we then add the scaled equations to eliminate variables
- continue eliminating variables until only one of them remains
- then use back-substitution to find the values of the other variables

##### Example 1
$$
\begin{aligned}
\textbf{Solve the system of equations} \\
\textbf{by elimination:} \\
&x + 2y = 10 \textemdash \: (1)\\
&0.5x -3y = -11\textemdash\:(2)\\\\

\textbf{Sln: }\\
&\text{\textit{Take (3)  as \(\: -0.5 \times\) (1)}} \\
&-0.5(x + 2y) = -0.5(10)\\
& -0.5x-y = -5 \textemdash \: (3)\\
&\text{We can then take (3) + (2) to eliminate \(x\)} \\
&0.5x -3y + (-0.5x-y) = -11 + (-5)\\
& -4y = -16 \\
&\therefore \: y = 4 \\\\
&\text{\textit{subs y = 4 into (1)}} \\
& x = 10 - 2(4) \\
&\therefore \: x = 2
\end{aligned}
$$
**Advantage of Elimination**
- enables us to methodically handle large systems with multiple equations
- start from the first row (ideally leading coefficient of $1$), then use this leading coefficient to eliminate the rest of the coefficients ($c_i \neq 0, 1$) 
	- use a combination of eliminations and replacements

**Drawbacks of Elimination**
- every new step creates a brand new equation
- we should replace the equation in place by the result of doing one of these transform operations
- have to make sure that each operation is *reversible* so that we don't have any information lost from these equations
	- make sure we can obtain the original equation by some means

### Types of Elimination Operations (or Row Operations)
1. Scale the equation by multiplying on both sides by a non-zero constant, i.e.  $e_1 = c \cdot e_1, \: c \neq 0$
2. Replace an equation by the sum of itself and the multiple of another equation, i.e. $e_1 = e_1 + d \cdot e_2$
3. Swap the positions of two equations or rows $e_1 \leftrightarrow e_2$
##### Example 1
$$
\begin{aligned}
\textbf{Solve the system of equations} \\
\textbf{by elimination with operations:} \\
&x + 2y = 10 \textemdash \: (1)\\
&0.5x -3y = -11\textemdash\:(2)\\\\

\textbf{Sln: }\\
&\text{\textit{Replace (2) by (2) \(-\) 0.5(1)}} \\
&0.5x -3y - 0.5(x + 2y) = -11 + -0.5(10)\\
& -4y = -16 \\\\
&\text{\textit{Scale (2) by \(-\frac{1}{4}\): }} \\
&\therefore \: y = 4 \\\\
&\text{\textit{subs y = 4 into (1)}} \\
& x = 10 - 2(4) \\
&\therefore \: x = 2
\end{aligned}
$$

If the any one of the equations within the system of equations has the form $0 = b, b \neq 0 \implies$ the system is inconsistent (i.e. no solutions to the system)

### Matrix Notation
- can express the coefficients and constants in the system of equation conveniently, as an **augmented matrix**, where each row represents an equation
- in the form:
$$
\begin{pmatrix}c_1 & c_2 & \ldots & c_n \: | \: b\end{pmatrix}
$$
---
## III. Echelon Form
- understand the definitions for Row Echelon Form and Reduced Row Echelon Form
- identify if (an augmented) matrix is in REF or RREF, or neither

- goal of row operations is to put a matrix into triangular form $\implies$ gives rise to the notion of echelon form
	- each subsequent leading entry is behind and to the right of the previous row's leading entry

> A **leading entry** in a row is the first non-zero entry as we go from left the right
- certain rows might not have a leading entry (also called as zero rows) and these rows should be parked at the bottom of the matrix for both REF and RREF

### REF
We follow the definition of REF in MA1522 (all 2 conditions must be satisfied).
- useful to also know that all entries in a column below a leading entry is zero (additional condition)

Condition 1: Any rows of all zeroes are below any other rows
- make sure that zero rows are all at the bottom of the augmented matrix to qualify to be in REF (not forgetting condition 2)
- if there aren't any zero rows $\implies$ vacuous truth (truth by default)

Condition 2: Leading entries go down and to the right 
- automatically fulfils the 3rd condition that leading entries should have zero below them

### RREF
- Again, We follow the definition of RREF in MA1522 (all 4 conditions must be satisfied).
- RREF makes it even easier for us to determine any possible solutions to the corresponding system of linear equations.

**Condition 1:** Any rows of all zeroes are below any other rows
**Condition 2:** Leading entries go down and to the right (hence implicitly, Condition 3 is fulfilled by 1 and 2)
**Condition 4:** The leading entry of each row is $1$
**Condition 5:** Each leading entry is the only non-zero entry in its column (rest *above and below* are $0$, which includes Condition 3 by definition)

---
## IV. Row Reductions
- learn to perform row operations to transform a matrix into REF or RREF
- identify pivot columns of a matrix

> **Row Reduction** is the process of applying row operations to a matrix such that it takes the Row-Echelon Form or RREF.

> Two matrices are said to be **row equivalent** if one matrix can be converted into another matrix by using row operations.
- Note that for the same (augmented) matrix it can have multiple row-equivalent REFs, but only has one unique RREF.
- Note that $\text{row equivalence} \neq \text{equivalent matrices}$
### Pivot Columns
> When a matrix is in REF, the location of the leading entry of each row in that matrix is called a **pivot**
- easier to **see the pivot columns** when the *augmented matrix is in REF form*.
- REFs will all have the same pivot points, even though matrix have different unique REFs
- each column that contains a pivot is called a pivot column

### Reducing a Matrix to REF
1. Identify the **pivots** from left to right
	1. The $1^{\text{st}}$ pivot is at the **top of the first column** that is not all zeroes. Perform swap operation on the first pivot column and then to subsequent ones (where each pivot is below its previous predecessor) while necessary to obtain a non-pivot entry in that position, without disturbing the leading entries of the previous rows.
	
2. **(Optional)** Use scaling operations to make the pivot equal to one
	- may be helpful at times
	-  $\times \frac{1}{a}$ or $\times a$ operation 

3. Use *replacement operations* (various e.r.o.) to create zeroes in all positions below the pivot. Always replace the row where we want there to be a zero, using a multiple of the row containing the pivot. 
	- $\times \frac{1}{a}$ or $\times a$ operation 

4. Repeat steps $1$ to $3$ until there are no more pivots.