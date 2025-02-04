Key Objective: how to systematically solve a system of equations

In secondary school, we use the "substitution" and "elimination methods"
- **Substitution** (make one of the variables on one side $\implies$ express one in terms of the other)
- **Elimination**
	- Multiply by LCM, if not already done) then add or subtract one equation from the other
	- Gaussian Elimination (i.e. the ***main preferred method*** of solving linear system of equations)

- *General Method (for both types)*: manipulate the equation to eliminate one of the variables
### Linear Systems
- finite number if linear equations
	- only involves scalar multiples (no trigo functions involved)
	- $\text{degree} = 1$ (no power $n, \text{where } n \gt 1$)

- $N$ variables and $M$ equations in standard form
	- $x_1, x_2, ..., x_n$ are the variables, which are somewhat like coefficients
	- The equations can be represented as a matrix
### Elementary Row Operations
In elimination, we need three types of operations (i.e. elementary row operations)
1. Exchanging two rows, $R_i \leftrightarrow R_j$
2. Adding a multiple of a row to another, $R_i + cR_j, \: c \in \mathbb{R}$
3. Multiplying a row by a nonzero constant, $aR_j, \: a \neq 0$

These three operations help to preserve the solutions of the linear system.
### Row-Echelon Form (REF)
**Some definitions**
1. Zero-row is a row with all entries of zero.
2. Non-zero is a row that includes non-zero entries.
3. **First nonzero entry from the left** of a **nonzero row** is called the **leading entry** (i.e. the first $*$ in a row, where $* \neq 0$)
	1. can also be in the constants column

- Echelon is derived from the French word "stairs".

> Augmented matrix is in **row-echelon form** if:
> - zero rows exists and they are the *bottom of the matrix*, AND
> - leading entries are **further to the right**, as we move down the rows

If we have the REF of the system of equations, it is very simple to solve the equation
- sometimes, the system of equations can have multiple solution (each variable $x_1, x_2, ..., x_n$ has more than one answer)

**Pivot Columns**
- columns that contain leading entries (the horizontal one)

**True Statements**
### Reduced Row-Echelon Form (RREF)
> Augmented matrix is in **reduced row-echelon form** if:
> - zero rows exists and they are the bottom of the matrix, AND
> - leading entries are **further to the right**, as we move down the rows AND
> - all the leading entries are $1$.
> - in each **pivot column**, all entries (above and below) other than the leading entry is $0$.

- Identity matrices are in both REF and RREF
### Gaussian Elimination
- enables one to transform the matrix to fulfil the definition and hence become into row-echelon form.

---
### Solutions to Linear Systems
- solution of linear system if the equations are simultaneously satisfied after making the substitution

**Three possibilities** ($0, 1 \text{ or } \infty$)
- inconsistent, i.e. no solutions or contradictory (the lines are parallel and have the same gradient, no intersection or common points)
- one unique solution
- infinitely many solutions (when one is a **scalar multiple** of another $\implies$ they are essentially the same equation)

Why not other possibilities
- 2 straight lines only intersect at one point, cannot be 2 or 255 or an arbitrary number of solutions.

In 3D space, linear equation makes a plane.
- \# Pivot columns = \#pivot rows
