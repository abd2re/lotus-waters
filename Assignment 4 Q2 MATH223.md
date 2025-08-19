## Q2

(a)
A $3 \times 3$ matrix $A$ is symmetric if $A^T = A$. In other words, the entry in row $i$, column $j$ equals the entry in row $j$, column $i$. For $3 \times 3$ matrices, this means:

Hence there are 6 independent entries in total:

$$
(a_{11}),~ (a_{22}),~ (a_{33}),~ (a_{12} = a_{21}),~ (a_{13} = a_{31}),~ (a_{23} = a_{32}).
$$

A convenient choice of basis for $U$ is to take the matrices that have a 1 in exactly one of those symmetric positions and 0 in all others. We can use:

$$
\begin{bmatrix}1&0&0\\0&0&0\\0&0&0\end{bmatrix},\begin{bmatrix}0&0&0\\0&1&0\\0&0&0\end{bmatrix},\begin{bmatrix}0&0&0\\0&0&0\\0&0&1\end{bmatrix},
\begin{bmatrix}0&1&0\\1&0&0\\0&0&0\end{bmatrix},\begin{bmatrix}0&0&1\\0&0&0\\1&0&0\end{bmatrix},\begin{bmatrix}0&0&0\\0&0&1\\0&1&0\end{bmatrix}.
$$

Since there are 6 of these basis matrices,

$$
\dim(U) = 6.
$$

(b)
Let $S$ be the function that transform any $3 \times 3$ matrix into a symmetric matrix

$$
S : M_{3\times 3}(\mathbb{R}) \to U,
~ S(A) = A + A^T.
$$

This function's image lies in the space $U$ of symmetric matrices. Suppose, for contradiction, that $\,S(A) = 0$ for every nonzero $A \in W$. Then every $A \in W$ would satisfy $A + A^{T} = 0\iff A=-A^T$, making $A$ skew‐symmetric.

But the set of all skew‐symmetric $3\times 3$ matrices has dimension 3. No 4‐dimensional subspace $W$ can sit entirely inside a 3‐dimensional subspace. Hence there must be at least one matrix $A\in W$ for which $S(A)\neq 0$. Because $S(A)$ is symmetric and nonzero, this shows that $W$ does indeed contain a nonzero symmetric matrix.
