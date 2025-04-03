Quite difficult, no shortcut so have to get use to it.
- the questions are beyond scope of the course

Logical Structure of the definitions are rather complex
### Linear Combination
Have some u vectors $u_1, u_2 \ldots u_k$ in the Euclidean vector space $\mathbb{R}^n$. Then linear combination of the vectors is:
$$
c_1u_1 + c_2u_2 + c_3u_3
$$
- assumes that $k \in \mathbb{Z}^+$
- also define $span({}) = \{\vec{0}^{\,}\}$

### Linear Span
- collection of all possible linear combinations given a set of vectors, $U$
- result is the subset of $\mathbb{R}^n$, where the vectors $u_i$ are vectors in the Euclidean space
- size of a span $\implies$ infinitely many possible vectors, with varying coefficients
- $u_i \in \mathbb{R}^n, u_i = \begin{pmatrix}a_1\\ a_2 \\ \vdots \\ a_n\end{pmatrix}$ 

### Checking for linear combinations
- Given set if vectors $U$, want to check if the vector $V$ is in the span of $U$
- Form the augmented matrix such as $\begin{pmatrix}u_1 & u_2 & \ldots & u_k \: | \:v\end{pmatrix}$

### Section 3.2 Question 1
For part 3, we choose column 3 as the parametric column since it is non-pivotal.

### Section 3.3 Question
#### Part 1
$$
\begin{aligned}
&\text{Let \( S = \{ v_1, v_2, \dots, v_m \} \) be a set of vectors in \( \mathbb{R}^n \).} \\
&1. \text{ Show that if \( \text{span}(S) = \mathbb{R}^n \), then \( m \geq n \).} \\
&2. \text{ If \( m \geq n \), can we make any conclusion about \( \text{span}(S) \)?}
\end{aligned}
$$

$$
\begin{aligned}
&\text{For Example: } n = 3, \: k = 2 \\
&\text{Any two vectors in } \mathbb{R}^3 \text{ cannot span } \mathbb{R}^3. \\\\

&\text{In a 2-dimension space, we have k (3) vectors.} \\
&{u_1, u_2, u_3} \subseteq \mathbb{R}^3 ? \\\\

&\textbf{Checking for span} \\
&\text{Don't care anout \(v\), but rather focus on the matrix \(n \times k\) matrix \(A\)}
\end{aligned}
$$

#### Part 2
If $k > n \implies$ simply more columns than the number or rows (2 vectors cannot span $\mathbb{R}^3$, hence $k$ vectors cannot span $\mathbb{R}^n$).
- direct proof

Generate basis vectors on the x and y axes
### Section 3.3 Challenge (Optional)
We have a set $S \subseteq \mathbb{R}^n,$ where $V = span(S)$

Goal is to show $span(S)$ satisfies span axioms (i), (ii), (iii)

---
### Section 3.4 Question 1
#### Part ii
Subspace is defined by three conditions (where all needs to be met)
1. $V$ contains the zero vector, i.e. $\textbf{0} \in V$
	1. also can be replaced by the property of (1'), i.e. $V$ is non-empty 
	2. (i) $\iff$ (i')
		1. $\{\vec{w}^{\,}\} \in V \implies 0 \cdot \{\vec{w}^{\,}\} \in V\implies \{\vec{0}^{\,}\} \in V$
2. $V$ is closed under scalar multiplication. $\forall$ vector $v \in V$ and scalar $\alpha$, the vector $\alpha v \in V$
3. $V$ is closed under addition, i.e. $\forall$ vectors $u, v \in V$, the sum $u + v$ is in $V$.

**The idea of closure in algebra**
- cannot go out of one of the smaller subset $V$ that is contained in the universal set $U$.
##### Subspace
- is someone a subset of structures (a.k.a. substructure, in algebraic terminology)
- has the same structure as a "euclidean space" but is just smaller, hence the name
- if universal property holds for the euclidean space, then it will hold for subspaces as wel
- the zero vector set is also a subspace containing zeroes


How to think of an example that fulfils conditions (i) and (ii) of subspace property, but **not** (iii)
- remains in the axis after scalar multiplication is already done.

#### Part iii
Suppose $S \subseteq span(S) \subseteq V \subseteq \mathbb{R}^n$
- Note even though we notate subspace as a subset, $V \subseteq \mathbb{R}^n$ is read as "V subspace Euclidean space"
- properties of linear combinations can be applied outside of $\mathbb{R}^n$

### Section 3.4 Question 2
As sets, $\mathbb{R}^2 \not \subseteq \mathbb{R}^3$, because every element $\in \mathbb{R}^2$ has two coordinates, while each element $\mathbb{R}^3$ has three coordinates.
- however, $\mathbb{R}^2$ can be "embedded" in $\mathbb{R}^3$ by $(x, y) \to (x,y,0)$
- but strictly speaking, two are not triples

### Section 3.4 Challenge
- Axioms 1 and 6 are already covered by axioms of span
- With axioms in universal form (using $\forall$) holds for a bigger set $X$, then we can determine that it also holds for the smaller subset $Y, Y \subseteq X$
- Only need to therefore prove the existential statements, axioms 3 and 4 (which are existential statements)
	- Axiom 4: holds because $-u = (-1)u \in V$

---
### Section 3.5 Question 1
Show linear independence of $\{v_1, v_2, v_3\}$
#### Linear Independence
- the linear combination $c_1u_1 + c_2u_2 + \ldots + c_ku_k = 0 \implies$ linear independence, linear dependence otherwise
	- the only coefficient is zero (i.e. $c_1u_1 + c_2u_2 + \ldots + c_ku_k = 0 \implies c_1 = c_2 = \ldots = c_k = 0$)
- the only solution is the zero solution.
#### Linear dependence
- the negation of independence ($\forall \to \exists$)
- basically, not all the coefficients are zero, but the result of the linear combination is zero.
### Section 3.5 Question 2
- some of the vectors **have to be redundant** if we have an $n$-dimensional space, but $\geq n$ vectors
- count the number of equations and unknowns

- we have $\infty$ many solutions for the homogeneous system $Ax = 0$, since the augmented matrix in RREF has a non-pivotal column


