---
tags:
  - MATH133
---
# Determinants
## Cofactor expansion

The determinant $\text{det}(A)$ or $|A|$ of an $n\times n$ matrix $A$ is a number that determines if:: $A$ is invertible.
<!--SR:!2025-01-12,57,250-->

For a $3\times 3$ matrix $\begin{bmatrix}a&b&c\\ d&e&f\\ g&h&i\end{bmatrix}$, the determinant is::$$a\begin{vmatrix}e&f\\ h&i\end{vmatrix}-b\begin{vmatrix}d&f\\ g&i\end{vmatrix}+c\begin{vmatrix}d&e\\ g&h\end{vmatrix}$$ *ps: $|x|$ means determinant and the $2\times 2$ determinants are called cofactors*
<!--SR:!2025-01-14,57,250-->

Given a matrix $A$, the cofactor of the element $c_{ij}(A)$ is:: a scalar obtained by multiplying together the term $(-1)^{i+j}$ and the submatrix obtained from $A$ by removing the $i$-th row and $j$-th column.
<!--SR:!2025-01-29,61,230-->

- $c_{ij}(A)=$::$(-1)^{i+j}|A_{ij}|$ where $A_{ij}$ is the matrix obtained from $A$ by removing the $i$-th row and $j$-th column.
<!--SR:!2024-12-08,31,230-->



Let $A$ be an $n\times n$ matrix. Then $\det(A)$ is obtained as follow:
?
- Pick any row (or column) in the matrix
- Sum all entries in this row (or column), each multiplied by the corresponding cofactor.
<!--SR:!2024-12-13,37,230-->

General determinant formula of an $n\times n$ matrix $A$ along $i$-th row or $j$-th column is::$$\begin{split}|A|&=a_{i1}c_{i1}(A)+\dots +a_{in}c_{in}(A)\\&=a_{i1}(-1)^{i+1}|A_{i1}|+\dots + a_{in}(-1)^{i+n}|A_{in}|\\&=a_{1j}(-1)^{1+j}|A_{1j}|+\dots + a_{nj}(-1)^{n+j}|A_{nj}|\end{split}$$
<!--SR:!2025-01-07,31,190-->
- If $A$ has a row or column of $0$, then $|A|=$::$0$
<!--SR:!2025-01-09,54,250-->
- If $A$ has two identical rows or columns then $|A|=$::$0$
<!--SR:!2025-01-02,51,250-->
- Let $B$ be the matrix obtained by interchanging the two rows or columns of $A$. Then $|B|=$::$-|A|$
<!--SR:!2025-02-06,63,230-->
- Let $B$ be the matrix obtained by multiplying a row or column by a scalar $k$. Then $|B|=$::$k|A|$
<!--SR:!2025-01-17,59,250-->
- Let $B$ be the matrix obtained by adding a multiple of a row or column to another row or column respectively. Then $|B|=$::$|A|$
<!--SR:!2025-01-24,59,230-->

An $n\times n$ matrix is called upper/lower triangular if:: it has only zeroes below/above the first diagonal.
<!--SR:!2024-12-09,14,225-->

The determinant of an upper or lower triangular matrix is:: the product of the first diagonal elements.
<!--SR:!2025-01-02,40,225-->

- $R_{2}\leftrightarrow R_{3}$, $\det\begin{pmatrix}1 & 0 & 0\\ 0 & 0 & 1\\ 0 & 1 & 0\end{pmatrix}=$::$-1$
<!--SR:!2025-02-08,68,245-->
- $R_{1}\rightarrow kR_{1}$, $\det\begin{pmatrix}k & 0 & 0\\ 0 & 1 & 0\\ 0 & 0 & 1\end{pmatrix}=$::$k$
<!--SR:!2025-02-07,68,245-->
- $R_{1}\rightarrow R_{1}+cR_{2}$, $\det\begin{pmatrix}1 & c & 0\\ 0 & 1 & 0\\ 0 & 0 & 1\end{pmatrix}=$::$1$
<!--SR:!2025-01-04,46,245-->

If $E$ is the elementary matrix corresponding to the ERO, then $|B|=$::$|EA|=|E|\times|A|$.
<!--SR:!2024-12-09,34,245-->

- $k\begin{vmatrix}a & b\\ c & d\end{vmatrix}=$::$\begin{vmatrix}ka & kb\\ c & d\end{vmatrix}=\begin{vmatrix}a & b\\ kc & kd\end{vmatrix}$
<!--SR:!2024-12-11,34,245-->
- $-\begin{vmatrix}a & b\\ c & d\end{vmatrix}=$::$\begin{vmatrix}b & a\\ d & c\end{vmatrix}$
<!--SR:!2024-12-17,33,225-->

If $A$ is $n\times n$, then $|kA|=$::$k^{n}|A|$.
<!--SR:!2024-12-17,24,205-->

Consider block matrices $\begin{bmatrix}A & X\\ 0 & B\end{bmatrix}$ or $\begin{bmatrix}A & 0\\ Y& B\end{bmatrix}$ where $A$ and $B$ are square, then $\det\begin{pmatrix}A & X\\ 0 & B\end{pmatrix}=\det\begin{pmatrix}A & 0\\ Y& B\end{pmatrix}=$::$\det(A)\det(B)$. ($X$ and $Y$ are not necessarily square)
<!--SR:!2025-02-14,73,245-->

Is $\det(A+B)=\det(A)+\det(B)$ ?:: False.
<!--SR:!2025-01-20,62,265-->

## Determinants and inverses

If $A$ and $B$ are $n\times n$ matrices, then $\det(AB)=$::$\det(A)\det(B)$
<!--SR:!2024-12-17,38,245-->
- $\det(A_{1}\dots A_{k})=$::$\det(A_{1})\dots\det(A_{k})$
<!--SR:!2025-01-03,46,245-->
- $\det(A^{k})=$::$\det(A)^{k}$
<!--SR:!2024-12-12,16,205-->
- $\det(E)\neq$::$0$
<!--SR:!2025-01-16,51,225-->
- $\det(A^{T})=$::$\det(A)$
<!--SR:!2025-01-26,60,245-->

The cofactor matrix of an $n\times n$ matrix $A$, is $c(A)=$::$[c_{ij}(A)]_{n\times n}$
<!--SR:!2024-12-14,36,245-->
The adjugate matrix is $\text{adj}(A)=$::$c(A)^{T}$
<!--SR:!2025-02-19,75,245-->
Let $A$ be $n\times n$ an invertible matrix, then $A^{-1}=$::$\frac{1}{\det(A)}\text{adj}(A)$.
<!--SR:!2025-01-05,30,185-->
- $\text{adj}(A)A=$::$A\cdot\text{adj}(A)=\det(A)I_{n}$
<!--SR:!2024-12-12,24,205-->

A Vandermonde matrix is:: a matrix with terms in a geometric progression in each row. For a vector of values $x_1, x_2, \ldots, x_n$, a Vandermonde matrix $V$ is defined as$$V = \begin{bmatrix} 1 & x_1 & x_1^2 & \dots & x_1^{n-1} \\ 1 & x_2 & x_2^2 & \dots & x_2^{n-1} \\ \vdots & \vdots & \vdots & \ddots & \vdots \\ 1 & x_n & x_n^2 & \dots & x_n^{n-1} \end{bmatrix}$$
<!--SR:!2024-12-08,26,240-->

The determinant of a Vandermonde matrix for distinct values $x_1, x_2, \ldots, x_n$ is given by:: the product of the differences between each pair of values:$$\det(V) = \prod_{1 \le i < j \le n} (x_j - x_i)$$
<!--SR:!2024-12-16,21,220-->
