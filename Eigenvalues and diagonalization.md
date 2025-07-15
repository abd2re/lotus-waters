---
tags:
  - MATH223
---
# Eigenvalues and diagonalization

## Eigenvalues and eigenvectors

$T:V \to V$ linear operator. A vector $u \in V, u \neq 0$ is called an **eigenvector** of $T$ if::$$T(u)=\lambda u$$ for some $\lambda \in \mathbb{F}$. Scalar $\lambda$ called **eigenvalue** associated to $u$.
<!--SR:!2025-04-17,14,230-->


If $\lambda$ eigenvalue for $T$, define the eigenspace $E_{\lambda}$ as::$$E_{\lambda}=\{u \in V \mid T(u) = \lambda u\}$$
<!--SR:!2025-04-30,18,210-->

$T:V \to V$ linear operator, $n=\dim V$ finite. The **characteristic polynomial of $T$** is::$$c_{t}(x)=\det([T]_{\alpha}^{\alpha}-x I)$$ where $\alpha$ is any basis of $V$.
<!--SR:!2025-04-16,8,170-->



1. $T:V \to V$ linear operator, $n=\dim V$ finite. $c_{T}(x)$ does not depend on:: $\alpha$.
<!--SR:!2025-04-26,21,250-->
2. $T:V \to V$ linear operator, $n=\dim V$ finite. $c_{T}(x)$ is a:: polynomial of degree $n$.
<!--SR:!2025-04-16,13,230-->
3. $T:V \to V$ linear operator, $n=\dim V$ finite. $\lambda$ is an eigenvalue of $T \iff c_{T}(\lambda)=$::$0$.
<!--SR:!2025-04-16,12,230-->
4. $E_{\lambda}=\ker(T- \lambda I)$ and hence $E_{\lambda}$ is:: a subspace.
<!--SR:!2025-04-22,18,250-->

## Diagonalization (eigenvector bases)

$T: V \to V$ linear operator called diagonalizable if:: $\exists$ basis $\alpha$ of $V$ such that every vector of $\alpha$ is an eigenvector of $T$.
<!--SR:!2025-04-14,7,178-->

$T: V \to V$ linear operator, $n = \dim V$ finite. Then $T$ is diagonalizable $\iff$::$\exists$ basis of $\alpha$ of $V$ such that $[T]_{\alpha}^{\alpha}$ is diagonal $\iff$ $\forall$ basis $\beta$ of $V$, $[T]_{\beta}^{\beta}$ is similar to a diagonal matrix.
<!--SR:!2025-04-14,3,138-->

Let $A \in M_{m \times n}(\mathbb{F})$. Then $A$ called diagonalizable if:: $\exists Q,D \in M_{m \times n}(\mathbb{F})$, $Q$ invertible, $D$ diagonal such that $Q^{-1}AQ=D$.
<!--SR:!2025-04-14,3,158-->

## Diagonalizability

Let $V$ be finite-dimensional vector space over $\mathbb{R}$, $T:V \to V$ linear operator if:: $\exists r \in C, r \notin \mathbb{R}$ such that $c_{T}(r)=0$. (i.e. $c_{T}(x$ has a complex non-real root then $T$ not diagonalizable).
<!--SR:!2025-04-13,1,130-->

$T: V \to V$ linear operator, $\lambda_{1}\neq \lambda_{2}$ eigenvalues of $T$, then $E_{\lambda_{i}} \cap E_{\lambda_{2}}=$::$\{\vec{0}\}$.
<!--SR:!2025-04-20,12,229-->

$T:V \to V$ linear operator, $\lambda_{1},\lambda_{2},\dots ,\lambda_{n}$ distinct eigenvalues of $T$. Let $\beta_{i}$ be basis of (independent set) of $E_{\lambda_{i}}$. Set $\beta=\beta_{1}\cup \beta_{2}\cup \dots \cup \beta_{n}$, then $|\beta|=$::$|\beta_{1}|+|\beta_{2}|+\dots +|\beta_{n}|$ and $\beta$ is linearly independent.
<!--SR:!2025-04-20,12,229-->


If $T: V \to V$ linear operator, $n=\dim V$ and $T$ has $n$ distinct eigenvalues, then $T$ is:: diagonalizable automatically.
<!--SR:!2025-04-19,11,229-->

1. Let $\lambda$ eigenvalue of $T$. The geometric multiplicity of $\lambda$ is:: $\dim E_{\lambda}$.
<!--SR:!2025-04-15,5,169-->
2. Let $\lambda$ eigenvalue of $T$. The algebraic multiplicity of $\lambda$ is:: the power to which the factor $(x-\lambda)$ appears in $c_{T}(x)$.
<!--SR:!2025-04-20,12,229-->

$T: V \to V$ linear operator, $V$ finite dimensional, $\lambda$ eigenvalue of $T$. then $1\leq \text{geom. mult. of }\lambda \leq$::$\text{alg. mult. of }\lambda$.
<!--SR:!2025-04-19,11,229-->

1. $T: V \to V$ linear operator, $n=\dim V$ finite. If $\mathbb{F}=\mathbb{R}$ and $c_{T}(x)$ has a non-real root, $T$ is:: not diagonalizable.
<!--SR:!2025-04-18,7,209-->
2. $T: V \to V$ linear operator, $n=\dim V$ finite. If $\mathbb{F}=\mathbb{R}$ and all roots $c_{T}(x)$, or, if $\mathbb{F}=\mathbb{C}$, then $T$ is:: diagonalizable $\iff$ For every eigenvalue $\lambda$ of $T$, geom. mult. of $\lambda$ = alg. mult. of $\lambda$.
<!--SR:!2025-04-17,7,209-->
3. $T: V \to V$ linear operator, $n=\dim V$ finite. If $T$ is diagonalizable, $\lambda_{1},\dots ,\lambda_{k}$ are all eigenvalues of $T$ and for each $i=1,2,\dots ,k$, $\beta_{i}$ is a basis of $E_{\lambda_{i}}$ the $\beta=\beta_{1}\cup \dots \cup \beta_{k}$ is:: a basis of $V$ composed of eigenvectors of $T$.
<!--SR:!2025-04-13,2,169-->


## Orthogonal diagonalization

- $A \in M_{n \times n}(\mathbb{R})$ called symmetric if:: $A^{T}=A$.
<!--SR:!2025-04-15,4,185-->
- $A \in M_{n \times n}(\mathbb{R})$ called orthogonal if:: columns of $A$ form ONB of $\mathbb{R}^n$
<!--SR:!2025-04-18,6,165-->
- $A \in M_{n \times n}(\mathbb{\mathbb{C}})$ called self-adjoint (Hermitian) if:: $A^{*} =A$ ($\bar{A}^{T}=A$)
<!--SR:!2025-04-13,3,165-->
- $A \in M_{n \times n}(\mathbb{\mathbb{C}})$ called unitary if:: columns of $A$ form ONB of $\mathbb{C}^{n}$ (with inner product on $\mathbb{C}$)
<!--SR:!2025-04-16,4,185-->

1. $A \in M_{n \times n}(\mathbb{R})$, $A$ orthogonal $\iff$::$A^{T}=A^{-1}$.
<!--SR:!2025-04-16,4,185-->
2. $A \in M_{n \times n}(\mathbb{C})$, $A$ unitary $\iff$::$A^{*}=A^{-1}$.
<!--SR:!2025-04-22,12,225-->

$A \in M_{n \times n}(\mathbb{R})$ orthogonally diagonalizable if:: $\exists$ ONB of $\mathbb{R}^{n}$ composed of eigenvectors of $A$ $\iff$ $\exists$ orthogonal $Q$, diagonal $D$ such that $Q^{T}AQ=D$ or $QAQ^{T}=D$.
<!--SR:!2025-04-13,3,165-->

$A \in M_{n \times n}(\mathbb{C})$ unitary diagonalizable if:: $\exists$ ONB of $\mathbb{C}^{n}$ composed of eigenvectors of $A$ $\iff$ $\exists$ unitary $Q$, diagonal D such that $Q^*AQ=D$ or $QAQ^*=D$.
<!--SR:!2025-04-13,1,130-->

1. For $A \in M_{m \times n}(\mathbb{R})$, $A$ orthogonally diagonalizable $\iff$::$A$ symmetric ($A^{T}=A$).
<!--SR:!2025-04-13,2,155-->
2. For $A \in M_{m \times n}(\mathbb{C})$, $A$ unitary diagonalizable $\iff$::$A^{*}A=AA^{*}$.
<!--SR:!2025-04-13,4,195-->

$A \in M_{m \times n}(\mathbb{C})$ called normal if:: $A^{*}A=AA^{*}$. Self-adjoint $\implies$ normal, unitary $\implies$ normal.
<!--SR:!2025-04-13,4,195-->


1. Let $A \in M_{m \times n}(\mathbb{R})$, $u,v \in \mathbb{R}^{n}$ then $\langle Au,v \rangle=$::$\langle u, A^{T}v \rangle$, $\langle u, Av \rangle=\langle A^{T}u, v \rangle$.
<!--SR:!2025-04-22,10,215-->
2. Let $A \in M_{m \times n}(\mathbb{C})$, $u,v \in \mathbb{C}^{n}$ then $\langle Au,v \rangle=$::$\langle u, A^{*}v \rangle$, $\langle u, Av \rangle=\langle A^{*}u, v \rangle$.
<!--SR:!2025-04-20,8,215-->

Let $A \in M_{m \times n}(\mathbb{R})$ be symmetric or let $A \in M_{m \times n}(\mathbb{C})$ be self-adjoint. Then all roots of characteristic polynomial $c_{A}(x)$ are in:: $\mathbb{R}$, i.e. all eigenvalues of a real symmetric or complex self-adjoint matrix are in $\mathbb{R}$.
<!--SR:!2025-04-13,2,155-->

Let $A \in M_{m \times n}(\mathbb{R})$ symmetric or $A \in M_{m \times n}(\mathbb{C})$ normal. Then the eigenspaces of $A$ are mutually:: orthogonal, that is if u in $E_{\lambda_{1}}$ and $w \in E_{\lambda_{2}}$ ($\lambda_{1}\neq \lambda_{2}$) then $\langle u,w \rangle=0$.
<!--SR:!2025-04-13,1,131-->

$A \in M_{m \times n}(\mathbb{R})$ symmetric is positive definite if:: $\forall u \in \mathbb{R}^{n}$, $u \neq \vec{0}$, $u^{T}Au>0$. Positive semi-definite if $u^{T}Au \geq 0$. Negative definite if $u^{T}Au<0$. Negative semi-definite if $u^{T}Au \leq 0$. (indefinite otherwise).
<!--SR:!2025-04-14,4,191-->

Let $A \in M_{m \times n}(\mathbb{R})$ symmetric. Then $A$ positive definite $\iff$:: all eigenvalues of $A$ are positive.
<!--SR:!2025-04-14,2,165-->

## Singular value decomposition (SVD)

1. Let $A \in M_{m \times n}(\mathbb{R})$ then $A^{T}A$ ($n \times n$) and $AA^{T}$ ($m \times m$) are:: symmetric and positive semi-definite.
<!--SR:!2025-04-13,1,130-->
2. Let $A \in M_{m \times n}(\mathbb{R})$ then $\text{rank}(A^{T}A)=$::$\text{rank}(A)=\text{rank}(AA^{T})$.
<!--SR:!2025-04-14,4,205-->

Let $A \in M_{m \times n}(\mathbb{R})$, consider $L_{A}:\mathbb{R}^{n}\to \mathbb{R}^{m}$, denote $r=\text{rank}(A)$. Then ONB $\beta=\{v_{1},\dots ,v_{n}\}$ of $\mathbb{R}^{n}$ and $\gamma=\{w_{1},\dots ,w_{m}\}$ of $\mathbb{R}^{m}$ and positive scalars $\delta_{1}\geq \delta_{2}\geq ...\geq \delta_{r}>0$ such that $L_{A}(v_{i})=$::$\begin{cases}\delta_{i}w_{i}\;\text{ for }\;i=1,\dots ,r\\ \vec{0}\;\text{ for }\;i=r+1,\dots ,n\end{cases}$. Consequently $[L_{A}]_{\beta}^{\gamma}=\begin{pmatrix}\delta_{1}\\ & \delta_{2}\\  &  & \ddots \\  &  &  & \delta_{r} \\ &  &  &  & \ddots \end{pmatrix}$ where the emptiness are zeroes. The numbers $\delta_{1},\delta_{2},\dots ,\delta_{r}$ called the singular values of $A$.
<!--SR:!2025-04-13,1,145-->

For any matrix $A \in M_{m \times n}(\mathbb{F})$, the SVD is:
?
$$A=U \Sigma V^{T}$$
where
- $V$ is eigenvectors of $A^{T}A$
- $\Sigma$ is the square roots of the eigenvalues of $A^{T}A$
- $U$ is composed of $u_{i}=\frac{1}{\sqrt{\lambda_{i}}}A v_{i}$
<!--SR:!2025-04-13,2,163-->