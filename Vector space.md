---
tags:
  - MATH133
---

# Vector space $\mathbb{R}^{n}$

## Subspaces of $\mathbb{R}^{n}$ and spanning sets

A set $U$ of vectors in $\mathbb{R}^{n}$ is called a subspace of $\mathbb{R}^{n}$ if it satisfies:
?
- $\vec{0}\in U$
- If $\vec{v_1},~\vec{v_{2}}\in U$ then $\vec{v_1}+\vec{v_{2}}\in U$ (closed under addition)
- If $\vec{v}\in U$ and $t$ is any scalar, then $t\vec{v}\in U$ (closed under scalar multiplication)
<!--SR:!2024-12-17,10,210-->

Subspaces of $\mathbb{R}^{3}$ are:: $\begin{Bmatrix}0\end{Bmatrix}$, lines/planes through $\mathbb{R}^{3}$ origin.
<!--SR:!2024-12-16,20,230-->

A linear combination of vectors $\vec{v_1},~\vec{v_{2}},~\dots,~ \vec{v_{k}}\in \mathbb{R}^{n}$ is any expression of the form:: $\vec{v}=t_{1}\vec{v_{1}}+t_{2}\vec{v_{2}}+\dots t_{k}\vec{v_{k}}$
<!--SR:!2024-12-16,23,250-->

The set of all in $\mathbb{R}^{n}$ that you can write as linear combinations $\vec{v_1},~\vec{v_{2}},~\dots,~ \vec{v_{k}}$ is called:: the span of these vectors and is denoted $\text{span}\begin{Bmatrix}\vec{v_1},~\vec{v_{2}},~\dots \vec{v_{k}}\end{Bmatrix}$
<!--SR:!2025-01-03,32,230-->

1. Let $U=\text{span}\begin{Bmatrix}\vec{v_1},~\vec{v_{2}},~\dots,~ \vec{v_{k}}\end{Bmatrix}$ of vectors in $\mathbb{R}^{n}$, $U$ is a subspace of:: $\mathbb{R}^{n}$
<!--SR:!2024-12-12,14,230-->
2. Let $U=\text{span}\begin{Bmatrix}\vec{v_1},~\vec{v_{2}},~\dots,~ \vec{v_{k}}\end{Bmatrix}$ of vectors in $\mathbb{R}^{n}$, if $W$ is a subspace of $\mathbb{R}^{n}$ containing $\vec{v_1},~\vec{v_{2}},~\dots,~ \vec{v_{k}}$, then:: $U=\text{span}\begin{Bmatrix}\vec{v_1},~\vec{v_{2}},~\dots,~ \vec{v_{k}}\end{Bmatrix}\subseteq W$
<!--SR:!2024-12-10,19,250-->

- $\text{span}\begin{Bmatrix}\vec{e_{1}},~\dots ,~\vec{e_{n}}\end{Bmatrix}$ where $\vec{e_{i}}$ is the $i$-th column of identity matrix is equal to:: $\mathbb{R}^{n}$
<!--SR:!2024-12-22,17,230-->

## Independence and dimension

### Linear independence

A set $\begin{Bmatrix}\vec{v_1},~\vec{v_{2}},~\dots,~ \vec{v_{k}}\end{Bmatrix}$ is said to be linearly independent if whenever we have $t_{1}\vec{v_{1}}+t_{2}\vec{v_{2}}+\dots t_{k}\vec{v_{k}}=\vec{0}$, then:: all the $t_{1}=\dots =t_{k}=0$
<!--SR:!2024-12-18,25,250-->

If $\vec{v}$, $\vec{w}$ are linearly independent, then $a \vec{v}+c \vec{w}$, $b \vec{v}+d \vec{w}$ are also linearly independent if:: and only if $\begin{pmatrix}a&b\\ c&d\end{pmatrix}$ is invertible.
<!--SR:!2024-12-24,22,230-->

Two vectors that are parallel are:: linearly dependent.
<!--SR:!2024-12-15,22,250-->

Let $\vec{v_{1}},~\vec{v_{2}},~\vec{v_{3}}$ be nonzero vectors in $\mathbb{R}^{3}$, they are linearly dependent if and only if:
?
1. Two of them are parallel
2. The vectors are coplanar (lie on a common plane where one vector is in the spanning of two others)
<!--SR:!2024-12-17,20,230-->

### Relation to linear systems

1. Let $A=[\vec{c_{1}},~\dots ,~\vec{c_{k}}]$ be an $m \times k$ matrix with columns $\vec{c_{1}}\in \mathbb{R}^{m}$ then columns $\vec{c_{1}},~\dots ,~\vec{c_{k}}$ are linearly independent if:: and only if $A \vec{v}=\vec{0}$ only has the trivial solution $\vec{v}=\vec{0}$.
<!--SR:!2024-12-10,11,170-->
2. Let $A=[\vec{c_{1}},~\dots ,~\vec{c_{k}}]$ be an $m \times k$ matrix with columns $\vec{c_{i}}\in \mathbb{R}^{m}$ then columns $\vec{c_{1}},~\dots ,~\vec{c_{k}}$ span $\mathbb{R}^{m}$ if:: and only if $A \vec{v}=\vec{b}$ has a solution for any $\vec{b}\in \mathbb{R}^{m}$
<!--SR:!2024-12-09,4,170-->

Let $A$ be an $n \times n$ matrix, the following 5 properties are equivalent:
?
1. $A$ is invertible (rank of $A$ is equal $n$ or $\det(A)\neq0$)
2. Columns of $A$ are linearly independent
3. Columns of $A$ span $\mathbb{R}^{n}$
4. Rows of $A$ are linearly independent
5. Rows of $A$ span $\mathbb{R}^{n}$
<!--SR:!2024-12-10,14,210-->

- $\text{Null}(A)=$::$\begin{Bmatrix}{\vec{x}\in \mathbb{R}^{n}~|~A \vec{x}=\vec{0}}\end{Bmatrix}$
<!--SR:!2024-12-20,16,213-->
- $\text{Im}(A)=$::$\begin{Bmatrix}{\vec{y}\in \mathbb{R}^{m}~|~\vec{y}=A \vec{x}~\text{for some}~\vec{x}\in \mathbb{R}^{n}}\end{Bmatrix}=\text{col}(A)$
<!--SR:!2024-12-14,7,213-->

### Dimension

Let $U$ be a subspace of $\mathbb{R}^{n}$. If $U=\text{span}\begin{Bmatrix}\vec{v_{1}},~\dots,~ \vec{v_{k}}\end{Bmatrix}$ and $U$ contains some linearly independent vectors $\vec{w_{1}},~...,~\vec{w_{m}}$. Then:: $m\leq k$
<!--SR:!2025-01-18,42,250-->

$U$ be a subspace of $\mathbb{R}^{n}$. A set of vectors $\vec{v_{1}},~\dots ,~\vec{v_{k}}$ such that $U=\text{span}\begin{Bmatrix}{\vec{v_{1}},~\dots ,~\vec{v_{k}}}\end{Bmatrix}$ and vectors $\vec{v_{1}},~\dots ,~\vec{v_{k}}$ are linearly independent is called:: a basis of $U$.
<!--SR:!2024-12-09,5,190-->

By the property of linear independence, we can write any vectors $\vec{v}\in U$ uniquely as:: a linear combination of vectors in the basis.
<!--SR:!2024-12-15,17,230-->

If $\begin{Bmatrix}{\vec{v_{1}},~\dots ,~\vec{v_{k}}}\end{Bmatrix}$ and $\begin{Bmatrix}{\vec{w_{1}},~\dots ,~\vec{w_{m}}}\end{Bmatrix}$ are two different bases of $U$, then:: $k=m$.
<!--SR:!2024-12-24,24,230-->

The dimension of $U$ is:: the number of bases vectors in any basis of $U$.
<!--SR:!2024-12-15,8,150-->

1. Let $U\subseteq \mathbb{R}^{n}$ be a subspace (we exclude the case $U=\{\vec{0}\}$), then $U$ has basis and $\dim(U)\leq n$
2. Let $U\subseteq \mathbb{R}^{n}$ be a subspace (we exclude the case $U=\{\vec{0}\}$), then we can obtain a basis from any set of linearly independent vectors by adding some vectors
3. Let $U\subseteq \mathbb{R}^{n}$ be a subspace (we exclude the case $U=\{\vec{0}\}$), then we can obtain a basis from any set of spanning vectors $U$ by removing some vectors

Let $U\subseteq \mathbb{R}^{n}$ a subspace of dimension $\dim(U)=m$. A set of $m$ vectors $\vec{v_{1}},~\dots,~ \vec{v_{m}}$ in $U$ are linearly independent if:: and only if they span $U$
<!--SR:!2024-12-09,18,250-->

Let $U\leq W\leq \mathbb{R}^{n}$ be two subspaces, then:
?
- $\dim(U)\leq\dim(W)$
- If $\dim(U)=\dim(W)$, then $U=W$
<!--SR:!2025-01-03,31,230-->

## Rank of matrices and dimension

- Let $A$ be and $n \times m$ matrix. The column space $\text{col}(A)\subseteq \mathbb{R}^{m}$ is:: the subspace of $\mathbb{R}^{m}$ spanned by the columns of $A$.
<!--SR:!2024-12-20,16,190-->
- Let $A$ be and $n \times m$ matrix. The row space $\text{row}(A)\subseteq \mathbb{R}^{m}$ is:: the subspace of $\mathbb{R}^{n}$ spanned by the rows of $A$.
<!--SR:!2024-12-25,24,230-->
- Let $A$, $B$ be two $m \times n$ matrices, if $A \rightarrow B$ are related by a sequence of row operations, then:: $\text{row}(A)=\text{row}(B)$
<!--SR:!2024-12-09,7,190-->
- Let $A$, $B$ be two $m \times n$ matrices, if $A \rightarrow B$ are related by a sequence of column operations, then:: $\text{col}(A)=\text{col}(B)$
<!--SR:!2024-12-09,11,230-->
- If a matrix $R$ is in REF form, then nonzero rows of $R$ form:: a basis of $\text{row}(R)$
<!--SR:!2024-12-22,18,230-->
- If a matrix $R$ is in REF form, then columns of $R$ that contain a leading 1 form:: a basis of $\text{col}(R)$
<!--SR:!2024-12-09,9,150-->
- A basis of $\text{row}(R)$ can be formed by:: the nonzero rows of $R$ in REF form.
<!--SR:!2024-12-09,13,233-->
- A basis of $\text{col}(R)$ can be formed by:: then columns of $R$ that contain a leading 1 in REF form.
<!--SR:!2024-12-09,5,213-->
- Can $\vec{0}$ be a basis vector ?:: Absolutely not because it's linearly dependent.
<!--SR:!2024-12-11,10,227-->

If we perform row/column operations on a matrix $R$, it doesn't change:: $\text{row}(R)$/$\text{col}(R)$.
<!--SR:!2025-01-01,25,233-->

Let $A$ be an $m \times n$ matrix, then the theorem of rank of matrices and dimension states that:: $$\dim(\text{col}(A))=\dim(\text{row}(A))=\text{rank}(A)$$
<!--SR:!2024-12-12,6,193-->

1. $A$ is $m \times n$ matrix of $\text{rank}(A)=r$, then $\dim(\text{Im}(A))+\dim(\text{Null}(A))=$::$\text{rank}(A)+\text{nullity}(A)=n$.
<!--SR:!2024-12-10,14,233-->
2. $A$ is $m \times n$ matrix of $\text{rank}(A)=r$, then the $n-r$ basic solutions of the system $A \vec{x}=\vec{0}$ that we get after gaussian elimination form:: a basis of $\text{Null}(A)$.
<!--SR:!2024-12-11,14,233-->
3. $A$ is $m \times n$ matrix of $\text{rank}(A)=r$, then, the basis of $\text{Im}(A)$ is just:: $\text{col}(A)$.
<!--SR:!2024-12-08,12,233-->

## Linear transformations

A transformation (function) $T:~\mathbb{R}^{n}\rightarrow \mathbb{R}^{m}$ is said to be linear if
?
1. $T(\vec{v}+\vec{w})=T(\vec{v})+T(\vec{w})$ for all $\vec{v},~\vec{w}\in \mathbb{R}^{n}$
2. $T(\lambda \vec{v})=\lambda T(\vec{v})$ for all $\vec{v}\in \mathbb{R}^{n}$ and scalars $\lambda \in \mathbb{R}$
<!--SR:!2024-12-12,15,233-->

If $T$ is a linear transformation, there exists:: an $m \times n$ matrix $A$ such that $T(\vec{x})=A \vec{x}$.
<!--SR:!2024-12-09,13,233-->

The matrix $A$ that corresponds to a linear transformation $T$ can be constructed by:: applying $T$ to the the standard basis vectors of $\mathbb{R}^{n}$ ($\begin{bmatrix}1\\ 0\\ \vdots\\0\end{bmatrix}\dots \begin{bmatrix}0\\ \vdots\\0\\1\end{bmatrix}$).
<!--SR:!2024-12-27,22,233-->

General formula for matrix rotation $R(\theta)$ is ::$\begin{bmatrix}\cos\theta&-\sin\theta\\\sin\theta&\cos\theta\end{bmatrix}$
<!--SR:!2024-12-14,13,227-->

In general if $\begin{Bmatrix}\vec{v_{1}},~\dots ,~\vec{v_{n}}\end{Bmatrix}$ is basis of $\mathbb{R}^{n}$, and $\begin{Bmatrix}\vec{w_{1}},~\dots ,~\vec{w_{n}}\end{Bmatrix}$ is any set of vectors $\vec{w_{i}}\in \mathbb{R}^{m}$, then there exists a unique linear transformation $T:\mathbb{R}^{n}\rightarrow \mathbb{R}^{m}$ such that:: $T(\vec{v_{i}})=\vec{w_{i}}$.
<!--SR:!2024-12-10,7,203-->

## Kernel and image

- Let $T:\mathbb{R}^{n}\rightarrow \mathbb{R}^{m}$ be a linear transformation. We define the kernel of $T$, $\ker(T)=$::$\begin{Bmatrix}\vec{v}\in \mathbb{R}^{n}~|~T(\vec{v})=\vec{0}\end{Bmatrix}$
<!--SR:!2024-12-13,11,225-->
- Let $T:\mathbb{R}^{n}\rightarrow \mathbb{R}^{m}$ be a linear transformation. We define the image of $T$, $\text{Im}(T)=$::$\begin{Bmatrix}\vec{w}\in \mathbb{R}^{m}~|~T(\vec{v})=\vec{w}~\text{for some}~\vec{v}\in \mathbb{R}^{n}\end{Bmatrix}$
<!--SR:!2024-12-11,7,206-->
- If $A$ is the $m \times n$ matrix associated with $T$ then $\ker(T)=$::$\text{Null}(A)=\begin{Bmatrix}\vec{v}\in \mathbb{R}^{n}~|~A \vec{v}=\vec{0}\end{Bmatrix}$
<!--SR:!2024-12-12,9,225-->
- If $A$ is the $m \times n$ matrix associated with $T$ then $\text{Im}(T)=$::$\text{col}(A)=\text{span}\begin{Bmatrix}\text{colums of}~A\end{Bmatrix}$
<!--SR:!2024-12-11,9,225-->

1) We say that $T:\mathbb{R}^{n}\rightarrow \mathbb{R}^{m}$ is surjective (or "onto") if:: $\text{Im}(T)=\mathbb{R}^{m}$ (ever vector in $\mathbb{R}^{m}$ can be hit by $T$)
<!--SR:!2024-12-12,7,205-->
1) We say that $T:\mathbb{R}^{n}\rightarrow \mathbb{R}^{m}$ is injective (or "one-to-one") if:: $T(\vec{v_{1}})=T(\vec{v_{2}})$ implies $\vec{v_{1}}=\vec{v_{2}}$ (ever vector is only hit by a single vector)
<!--SR:!2024-12-12,10,226-->

- $T:\mathbb{R}^{n}\rightarrow \mathbb{R}^{m}$ is injective if:: and only if $\ker(T)=\begin{Bmatrix}\vec{0}\end{Bmatrix}$
<!--SR:!2024-12-13,6,166-->


Diagrams of strictly surjective, strictly injective and surjective and injective (bijective):
?
Strictly surjective
![[image-20241126133140211.png]]
Strictly injective
	![[image-20241126133202314.png]]
surjective and injective (bijective)
![[image-20241126133219454.png]]
<!--SR:!2024-12-11,9,225-->


1) Let $A$ be an $m \times n$ matrix and $T_{A}:\mathbb{R}^{n}\rightarrow \mathbb{R}^{m}$ the associated linear transformation (so $T_{A}(\vec{v})=A \vec{v}$) then $\text{rank}(A)=m$ if:: and only if $T_{A}$ is surjective.
<!--SR:!2024-12-09,6,205-->
2) Let $A$ be an $m \times n$ matrix and $T_{A}:\mathbb{R}^{n}\rightarrow \mathbb{R}^{m}$ the associated linear transformation (so $T_{A}(\vec{v})=A \vec{v}$) then $\text{rank}(A)=n$ if:: and only if $T_{A}$ is injective.
<!--SR:!2024-12-10,6,163-->


- Suppose $m>n$ then $\text{rank}(A)\leq n<m$, by previous theorem since $\text{rank}(A)\neq m$, $T_{A}:\mathbb{R}^{n}\rightarrow \mathbb{R}^{m}$ is not surjective if $m>n$.
- Suppose $m<n$ then $\text{rank}(A)\leq m<n$, by previous theorem since $\text{rank}(A)\neq m$, $T_{A}:\mathbb{R}^{n}\rightarrow \mathbb{R}^{m}$ is not injective if $m>n$.
- $T_{A}:\mathbb{R}^{n}\rightarrow \mathbb{R}^{n}$ is surjective and injective if:: and only if $A$ is invertible.
<!--SR:!2024-12-14,10,225-->

Suppose $T:\mathbb{R}^{n}\rightarrow \mathbb{R}^{m}$ is a linear transformation then $n=$::$\dim(\ker(T))+\dim(\text{Im}(T))$
<!--SR:!2024-12-10,7,205-->

$(T_{1}\circ T_{2})(\vec{v})=$::$T_{1}(T_{2}(\vec{v}))=A_{1}A_{2}\vec{v}$
<!--SR:!2024-12-17,13,226-->
