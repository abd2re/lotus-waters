---
tags:
  - MATH133
---

# Matrix Algebra

- An $m\times n$ matrix is:: a rectangular array of numbers with $m$ rows and $n$ columns.
<!--SR:!2025-04-02,138,290-->
- The $(i,j)$ entry of a matrix is:: the number in the i-th row and j-th column.
<!--SR:!2024-12-20,57,230-->
- Shorter notation for a $m\times n$ matrix $A$ is:: $[a_{ij}]_{m\times n}$.
<!--SR:!2025-02-14,94,250-->
- $(A^{T})^{T}=$::$A$
<!--SR:!2025-02-21,97,250-->
- $(kA)^{T}=$::$kA^{T}$
<!--SR:!2025-02-03,87,250-->
- $(A+B)^{T}=$::$A^{T}+B^{T}$
<!--SR:!2025-01-13,79,270-->
- A matrix is called symmetric if:: $A=A^{T}$
<!--SR:!2025-02-05,72,230-->
- $(AB)^{T}=$::$B^{T}A^{T}$
<!--SR:!2025-03-15,109,251-->

## Matrix-vector multiplication

- If $A$ is an $m\times n$ matrix and $\vec{v_{n}}=\begin{bmatrix}a_{1n}\\ a_{2n}\\ \vdots\\ a_{mn}\end{bmatrix}$ is an $n$-vector then the multiplication of $A$ by an $n$-vector $\vec{x}=\begin{bmatrix}x_{1}\\ x_{2}\\ \vdots\\ x_{n}\end{bmatrix}$, then $A\vec{x}=$::$[v_{1}x_{1}+v_{2}x_{2}+\dots+v_{n}x_{n}]$
<!--SR:!2024-12-14,21,230-->
- To multiply a matrix with a vector, the requirements are:: that the number of matrix columns is equal to the number of vector rows.
<!--SR:!2024-12-23,61,251-->
- The result of a product between a matrix with a vector will have as rows and columns:: the number of matrix rows and the number of vector columns (1).
<!--SR:!2025-04-05,129,271-->
- Dot product is just:: matrix multiplication but we transpose the first matrix.
<!--SR:!2024-12-21,59,251-->
- An identity matrix $I_{n}$ is:: a matrix a zero matrix of size $n\times n$ where there is a diagonal of ones.
<!--SR:!2024-12-18,57,251-->
- $I_{n}\vec{x}=$::$\vec{x}$ where $\vec{x}$ is an $n$-vector.
<!--SR:!2025-03-29,117,251-->

## Matrix multiplication

- If $A$ is an $m\times n$ matrix and $B$ is and $n\times k$ matrix then $AB=$::$$\large{AB=[A\vec{b_{1}}\,A\vec{b_{2}}\,\dots \, A\vec{b_{n}}]}$$ where $\vec{b_{i}}$ is a column of the B matrix and $AB$ is a $m\times k$ matrix.
<!--SR:!2025-03-30,117,251-->
- A matrix-vector multiplication is essentially:: a matrix multiplication where the second matrix has only 1 column.
<!--SR:!2024-12-12,59,271-->
- To multiply two matrices, the requirements are:: that the number of columns of the first matrix is equal to the number of rows of the second matrix.
<!--SR:!2025-02-12,89,251-->
- The result of a matrix multiplication will have as rows and columns:: the number of rows of the first matrix and the number of columns of the second matrix.
<!--SR:!2025-03-17,109,251-->

In general $AB\neq$::$BA$.
<!--SR:!2025-02-16,75,246-->

<!--SR:!2024-10-16,18,251-->

## Matrix inverses

- If $A$ and $B$ are $n\times n$ matrices, $B$ is an **inverse of** $A$ if:: $AB=BA=I_{n}$. $A$ is said to be invertible.
<!--SR:!2024-12-31,28,151-->
- If $A$ is an invertible matrix, then it has a unique inverse denoted by:: $A^{-1}$.
<!--SR:!2025-01-30,85,271-->
- For $2\times 2$ matrices, if $A=\begin{bmatrix}a&b\\ c&d\end{bmatrix}$, the determinant is the number $\det(A)=$::$ad-bc$
<!--SR:!2025-02-08,83,251-->
- For a $2\times 2$ matrix, we can know if $A$ is invertible if::$\det(A)\neq 0$
<!--SR:!2024-12-22,52,231-->
- If $A=\begin{bmatrix}a& b\\ c& d\end{bmatrix}$, then $A^{-1}=$::$\frac{1}{\det(A)}\begin{bmatrix}d&-b\\ -c&a\end{bmatrix}$
<!--SR:!2024-12-27,54,231-->
- $AA^{-1}=$::$I_{n}$
<!--SR:!2025-01-09,69,251-->
- $A\vec{x}=\vec{b}\iff\vec{x}=$::$A^{-1}\vec{b}$
<!--SR:!2025-02-01,79,251-->
- Algorithm to get $n\times n$ matrix' inverse:: $[A|I_{n}]\rightarrow^{\text{RREF}}[I_{n}|A^{-1}]$
<!--SR:!2024-12-25,59,251-->
- An $n\times n$ matrix has has inverse if and only if:: its rank is $n$
<!--SR:!2024-12-08,20,211-->
- If $A$ and $B$ are both invertible, then $(AB)^{-1}=B^{-1}A^{-1}$
- $(A^{T})^{-1}\iff$::$(A^{-1})^{T}$
<!--SR:!2025-04-02,117,251-->
- $I^{-1}_{n}=$::$I_{n}$
<!--SR:!2024-12-26,61,251-->

## Elementary matrices

- An $n\times n$ matrix $E$ is called an elementary matrix if:: it can be obtained from identity matrix $I_{n}$ by a single ERO.
<!--SR:!2024-12-23,38,230-->
- If an ERO is performed on an $m\times n$ matrix $A$, say $A\rightarrow^{\text{ERO}}B$, then $B=$::$EA$ where $E$ is the $m\times m$ matrix elementary matrix obtained by applying the same ERO to $I_{n}$.
<!--SR:!2025-01-07,51,210-->
- Every elementary matrix $E$ is invertible and $E^{-1}$ corresponds to:: the inverse of the ERO corresponding to $E$.
<!--SR:!2025-01-28,70,230-->
- In the context of elementary matrices, an $n\times n$ matrix is invertible if:: and only if it can be written as a product of elementary matrices.
<!--SR:!2025-02-12,70,210-->

