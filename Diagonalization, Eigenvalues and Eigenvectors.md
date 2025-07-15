---
tags:
  - MATH133
---
# Diagonalization, Eigenvalues and Eigenvectors

An $n \times n$ matrix $D$ is said to be diagonal if:: all its entries off the diagonal are 0: $$D=\begin{bmatrix}\lambda_{1}&0&\dots &0 \\ 0&\lambda _{2}&\dots &0 \\ \vdots&\vdots&\ddots&\vdots \\ 0&\dots &0&\lambda _{n}\end{bmatrix}$$
<!--SR:!2024-12-09,10,250-->
Notation of a diagonal matrix $D$ is:: $D=\text{diag}(\lambda_{1},~\dots ,~\lambda_{n})$
<!--SR:!2024-12-19,15,248-->

$D^{k}=$::$D \cdot \dots \cdot  D=\begin{bmatrix}\lambda_{1}^{k}&0&\dots &0 \\ 0&\lambda _{2}^{k}&\dots &0 \\ \vdots&\vdots&\ddots&\vdots \\ 0&\dots &0&\lambda _{n}^{k}\end{bmatrix}$
<!--SR:!2024-12-28,21,250-->

An $n \times n$ matrix $A$ is said to be diagonalizable if:: there exists a diagonal matrix $D$ and an invertible matrix $P$ such that $A=PDP^{-1}$.
<!--SR:!2024-12-20,16,248-->

$A^{k}=$::$PD^{k}P^{-1}$
<!--SR:!2024-12-13,9,208-->

Let $A$ be an $n \times n$ matrix. A nonzero vector $\vec{v}\in \mathbb{R}^{n}$ is said to be an **eigenvector** of $A$ to the **eigenvalue** $\lambda$ if:: $A \vec{v}=\lambda \vec{v}$.
<!--SR:!2024-12-13,6,210-->

$\vec{v}$ eigenvector to the eigenvalue $\lambda$ if:: and only if $\vec{v}$ is a nontrivial solution of $(\lambda I_{n}-A)\vec{v}=\vec{0}$.
<!--SR:!2024-12-08,1,205-->

$C \vec{x}=\vec{0}$ has nontrivial solution if:: and only if $\det(C)=0$.
<!--SR:!2024-12-11,5,245-->

$\lambda$ is an eigenvalue if:: and only if $\det(\lambda I_{n}-A)=0$.
<!--SR:!2024-12-11,5,245-->

The eigenvectors are all nonzero solutions of:: $(\lambda I_{n}-A)\vec{v}=\vec{0}$.
<!--SR:!2024-12-08,3,245-->

The characteristic polynomial of $A$ is:: $c_{A}(x)=\det(x I_{n}-A)$.
<!--SR:!2024-12-08,1,205-->

The roots $\lambda$ of $c_{A}$ are precisely the eigenvalues. We say that $\lambda$ is a root if $c_{A}(\lambda)=$::$0$.
<!--SR:!2024-12-12,5,225-->

$c_{A}(x)$ is a polynomial of degree $n$ if:: $A$ is $n \times n$.
<!--SR:!2024-12-12,5,225-->

$E_{\lambda}=$::$\begin{Bmatrix}\vec{v}\in \mathbb{R}^{n}~|~A \vec{v}=\lambda \vec{v}\end{Bmatrix}$
<!--SR:!2024-12-08,2,205-->

There are infinitely many eigenvectors for:: each eigenvalue.
<!--SR:!2024-12-10,4,245-->

$P=$::$\begin{bmatrix}\vec{v_{1}}&~\dots &~\vec{v_{n}}\end{bmatrix}$ (equivalent eigenvector for the eigenvalues $\lambda_{1},~\dots ,~\lambda_{n}$).
<!--SR:!2024-12-11,5,245-->

$A$ is diagonalizable if and only if:: $P$ is invertible. If it is, then $A=PDP^{-1}$.
<!--SR:!2024-12-12,5,225-->

The steps to diagonalize a matrix $A$ of size $n \times n$ are:
?
1) Find all the eigenvalues $\lambda_{i}$ by solving $\det(x I_{n}-A)=0$
2) For each eigenvalue $\lambda_{i}$, find the basic eigenvectors to the eigenvalue $\lambda_{i}$ ($(\lambda_{i} I_{n}-A)\vec{v}=\vec{0}$)
3) If at the process we find $n$ basic eigenvectors $\{\vec{v_{1}},~\dots ,~\vec{v_{n}}\}$ in total (for all the eigenvalues) then $A$ is diagonalizable and $A=PDP^{-1}$ where $P=\begin{bmatrix}\vec{v_{1}}&\dots &\vec{v_{n}}\end{bmatrix}$ and $D=\text{diag}(\lambda_{1},~\dots ,~\lambda_{n})$.
<!--SR:!2024-12-12,5,225-->

If we get less than $n$ basic eigenvectors then $A$ is:: not invertible.
<!--SR:!2024-12-12,6,245-->

For a triangular matrix, the eigenvalues are:: the diagonal entries.
<!--SR:!2024-12-10,4,245-->

