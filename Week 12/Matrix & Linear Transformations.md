Given an $m \times n$ matrix $A$, the matrix transformation corresponding to $A$ is the function $T:\mathbb{R}^n \to \mathbb{R}^m$ that is defined using the rule $T(x) = Ax$
- domain of $T$ is $\mathbb{R}^n$, where $n$ is the **number of columns** of $A$
- codomain of $T$ is $\mathbb{R}^m$, where $m$ is the **number of rows** of $A$ (i.e. the targeted space)

Example: for the matrix $A = \begin{pmatrix}1 & -3 & 1 \\ 2 & 5 & -2\end{pmatrix}$ and $T:\mathbb{R}^3 \to \mathbb{R}^2$ is defined by $T(x) = Ax$
- can do simple matrix multiplication to obtain the resultant function of $T$
### Notation and Sub-concepts
- $\forall T:\mathbb{R}^n \to \mathbb{R}^m$ (any function $T$ is a transformation)
- matrix transformations are a specific type of transformation
- given $x \in \mathbb{R}^n$, the **image of $x$ under $T$** is the vector $T(x)$
- if we take all the outputs of the function $T$ (i.e. the set of all images), we will obtain the range of $T$
	- this range / image of $T$ is a subset of the codomain $\mathbb{R}^m$ (or may be equivalent to the full set, depending on the mapping function $T$)
	- $\text{range}(T) \subseteq \mathbb{R}^m$

- may be sometimes asked to solve for the vector $x$