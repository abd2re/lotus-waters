---
tags:
  - MATH223
---
# Inner product spaces

$\rightarrow u \cdot v=$::$a_{1}b_{1}+\dots +a_{n}b_{n}$
<!--SR:!2025-06-01,57,250-->
$\rightarrow ||u ||=$::$\sqrt{u \cdot u}$ length
<!--SR:!2025-06-04,59,250-->
$\rightarrow \cos \theta=$::$\frac{u \cdot v}{||u ||||v ||}=\frac{\langle u, v \rangle}{||u ||||v ||}$
<!--SR:!2025-05-17,41,210-->
$\to \theta=\frac{\pi}{2}\iff$::$u \cdot v = 0$ ($u,v \neq 0$)
<!--SR:!2025-05-15,47,250-->


Inner product on $V$ is a function $V \times V \rightarrow \mathbb{F}$, denote $\langle u,v \rangle$, such that:
?
1. $\forall u,v,w \in V$, $\langle u+v,w \rangle=\langle u,w \rangle+\langle v,w \rangle$.
2. $\forall u,v \in V, c \in \mathbb{F}$, $\langle cu,v \rangle=c \langle u,v \rangle$
3. $\langle v,u \rangle=\langle u,v \rangle$ called conjugate symmetry. If $\mathbb{F}=\mathbb{R}$, $\langle v,u \rangle=\langle u,v \rangle$ symmetry.
4. $\forall u \neq \vec{0}$, $\langle u,v \rangle >0$ called positive definite.
((1),(2) called linearity in first component)
$V$ together with an inner product called inner product space.
Note: Definition is both for $F=\mathbb{R}$ and $F=\mathbb{C}$. If $F=\mathbb{C}$, in (4) note $\langle u,u \rangle= \overline{\langle u,u \rangle}$ by (3) so $\langle u,u \rangle \in \mathbb{R}$ so $\langle u,u \rangle$ makes sense.
<!--SR:!2025-04-26,19,170-->


Let $V$ inner product space. Then (2)
?
1. conjugate linearity in second component
	$\forall u,v,w \in V, c \in \mathbb{F}$
	- $\langle u,v+w \rangle=\langle u,v \rangle +\langle u,w \rangle$
	- $\langle u,cv \rangle=\bar{c}\langle u,v \rangle$
2. $\langle u,\vec{0} \rangle=0$
3. $\langle u,u \rangle=0 \iff u = \vec{0}$
4. $\forall u,v \in V$ if $\forall w \in V$, $\langle u,w \rangle=\langle v,w \rangle$ then $u=v$.
5. On $\mathbb{F}^{n}$, the stander inner product (dot product) is $\langle u,v \rangle=\sum\limits_{i=1}^{n}a_{i}\overline{b_{i}}$.
<!--SR:!2025-04-23,21,185-->

- Let $A \in M_{m \times n}(\mathbb{F})$, conjugate of $A$ is:: $\overline{A} \in M_{m \times n}(\mathbb{F})$ where $(\overline{A})_{ij}=\overline{A_{ij}}$.
<!--SR:!2025-04-15,10,182-->
- Let $A \in M_{m \times n}(\mathbb{F})$, adjoint of $A$ is:: $A^{*}=\overline{A}^{T}=\overline{A^{T}}$ (If $\mathbb{F}=\mathbb{R}$, $A^{*}=A^{T}$)
<!--SR:!2025-05-20,39,202-->

On $M_{m \times n}(\mathbb{F})$, define Frobenius inner product by:: $\langle A,B \rangle= \text{trace}(AB^{*})$
<!--SR:!2025-05-11,33,202-->

$\rightarrow \overline{\text{trace}(A)}=$::$\text{trace}(\overline{A})$
<!--SR:!2025-05-05,38,242-->
$\to \text{trace}(A^{T})=$::$\text{trace}(A)$
<!--SR:!2025-04-27,33,242-->


## Norm and angle

$V$ inner product space. For $u \in V$, the norm (or length) of $u$ by:: $||u||=\sqrt{\langle u,u \rangle}$. Note: $\langle u,u \rangle \in \mathbb{R}$ and $\langle u,u \rangle \geq 0 \to ||u ||\in \mathbb{R}\geq 0$. $||u || \iff u=\vec{0}$.
<!--SR:!2025-05-22,43,222-->

$\to |\langle u,v \rangle| \leq$::$||u ||||v ||$ (Cauchy-Schwarz Inequality)
<!--SR:!2025-05-08,31,212-->

Let $u,v \in V$ (inner product space). Then:
1) $|\langle u,v \rangle| \leq ||u ||||v ||$
2) $|\langle u,v \rangle| = ||u ||||v ||$
$$\iff $$
?
$u=cv$ or $v=cu$ for some $c \in \mathbb{F}$.
<!--SR:!2025-05-12,35,202-->


$\forall u,v \in V$ (inner product space), $||u+v || \leq$::$||u ||+ ||v ||$.
<!--SR:!2025-05-05,29,212-->

## Orthogonal sets and orthogonal complements

1. $u,v \in V$ are orthogonal if:: $\langle u,v \rangle=0$. Note $u=\vec{0}$ or $v=\vec{0}$ allowed, so $\vec{0}$ orthogonal to all $v \in V$, if $u \neq \vec{0}, v \neq 0$, orthogonal $\iff$ $\theta=\pi/2$.
<!--SR:!2025-04-18,20,209-->
2. $X \subseteq V$ is orthogonal if:: $\langle u,v \rangle=0$ all $u,v \in X$, $u \neq v$ and $\vec{0} \notin X$. If also $||u ||=1$ all $u \in X$ (i.e. $\langle u,u \rangle=1$), $X$ called orthonormal.
<!--SR:!2025-04-25,18,169-->
3. Basis $\beta$ that is orthogonal called:: orthogonal basis (OB), orthonormal called orthonormal basis (ONB).
<!--SR:!2025-04-28,28,229-->

$X=\{v_{1},v_{2},\dots ,v_{n}\}$ is orthonormal $\iff$ $\langle v_{i},v_{j}\rangle=\delta_{ij}$.

Let $X \subseteq V$ orthogonal set. Then $X$ is:: linearly independent.
<!--SR:!2025-04-26,14,169-->

Fourier coefficients. Let $\alpha=\{v_{1},\dots ,v_{n}\}$ OB of $V$. For all $u \in V_{n}$, $u$ is equal to::$$u=\sum\limits_{i=1}^{n}\left(\frac{\langle u, v_{i}\rangle}{\langle v_{i}, v_{i}\rangle}\right)v_{i}$$ i,e, coordinates computed by formula $$[u]_{\alpha}=\begin{pmatrix}\langle u, v_{1}\rangle/\langle v_1, v_{1}\rangle\\\vdots\\\langle u, v_{n}\rangle/\langle v_n, v_{n}\rangle\end{pmatrix}$$
<!--SR:!2025-04-13,5,149-->
Let $X \subseteq V$. The orthogonal complement of $X$ is:: all of $v \in V$ such that $\langle v,x \rangle=0$ all $x \in X$. $X^{\perp}=\{v \in V ~|~\forall x \in X, \langle v,x \rangle=0\}$
<!--SR:!2025-05-07,28,209-->

1. Let $W \leq V$. $W^{\perp}$ is:: a subspace.
<!--SR:!2025-05-08,26,203-->
2. Let $W \leq V$. If $\alpha=\{w_{1},\dots ,w_{n}\}$ is a basis of $W$ then $\forall u \in V$, $u \in W^{\perp} \iff$::$\langle u,w_{i}\rangle=0$ for all $i=1,\dots ,n$,
<!--SR:!2025-04-21,14,163-->
3. Let $W \leq V$. $W \cap W^{\perp}=$::$\{\vec{0}\}$.
<!--SR:!2025-04-22,22,223-->

## Orthogonal projection and Gram-Schmidt algorithm

1. $V$ inner product space, $W \leq V$ a finite-dimensional subspace. For all $v \in V$, $\exists$ unique vectors $w \in W$, $w' \in W^{\perp}$ such that $v=$::$w+w'$. i.e. $V=W \oplus W^{\perp}$.
<!--SR:!2025-04-16,17,203-->
2. $V$ inner product space, $W \leq V$ a finite-dimensional subspace. If $\alpha=\{w_{1},\dots ,w_{n}\}$ is an orthogonal basis of $W$, then $w$ above given by $w=$::$\sum\limits_{i=1}^{n}\frac{\langle v,w_{i}\rangle}{\langle w_{i}, w_{i}\rangle}w_{i}$
<!--SR:!2025-05-07,25,183-->
3. $V$ inner product space, $W \leq V$ a finite-dimensional subspace. $\dim V=$::$\dim W + \dim W^{\perp}$ (for $V$ finite- dimensional).
<!--SR:!2025-05-06,26,203-->


If $W \leq V$, define $P_{w}:V \to V$, orthogonal projection onto $W$, by:: $P_{w}(u)=w$ where $u=w+w'$, $w \in W$, $w' \in W^{\perp}$. $P_{w}$ is a linear operator.
<!--SR:!2025-04-15,12,176-->

If $u,v$ orthogonal then $||u+v ||^{2}=$::$||u ||^{2}+||v ||^{2}$.
<!--SR:!2025-04-21,18,216-->

Let $W \leq V$ finite-dimensional, $u \in V$, $u=w + w'$ the decomposition ($w=P_{w}(u)$). Then $w$ is the closest vector in $W$ to $u$, in the sense that for all $z \in W$,:: $||u-w ||\leq ||u -z ||$.
<!--SR:!2025-04-20,15,176-->

Gram-Schmidt Algorithm:
Given basis $\alpha=\{w_{1},\dots , w_{n}\}$ of $W$, construct orthogonal basis $\beta=\{v_{1},\dots ,v_{n}\}$ of $W$ inductively by:
?
1. $v_{1}=w_{1}$
2. For each $k=2,\dots ,n$, define $v_{k-1}=\text{span}\{v_{1},\dots ,v_{k-1}\}$. Set $v_{k}=w_{k}-P_{v_{k-1}}(w_{k})$ (i.e. decompose $w_{k}=P_{v_{k-1}}(w_{k})+v_{k}$ where $P_{v_{k-1}} \in V_{k-1}$ and $v_{k} \in V_{k-1}^{\perp}$). That is $$v_{k}=w_{k}-\sum\limits_{i=1}^{k-1}\frac{\langle w_{k},v_{i}\rangle}{\langle v_{i},v_{i}\rangle}v_{i}$$ Note: If we want ONB, normalize (rescale to 1) the $v_{i}$ at the end or during the algorithm.
<!--SR:!2025-04-23,11,156-->



## Inner products defined by matrices

Let $u= \begin{pmatrix}a_{1}\\ \vdots \\ a_{n}\end{pmatrix},v= \begin{pmatrix}b_{1}\\ \vdots \\ ab_{n}\end{pmatrix} \in \mathbb{R}^{n}$. $u^{T}v=$::$\langle u,v \rangle$.
<!--SR:!2025-04-22,19,216-->


Conditions needed on $A$ so that $\langle u, v \rangle=u^{T}Av$
?
1. $\langle u+v,w \rangle=(u+v)^{T}Aw$
2. $\langle cu,v \rangle=(cu)^{T}Av$
3. $\langle v, u \rangle =v^{T}Au$
4. For every $u \in \mathbb{R}^{n}, u \neq \vec{0}$ need $\langle u,u \rangle>0$, $u^{T}Au >0$
<!--SR:!2025-04-20,12,192-->

Let $A \in M_{n \times n}(\mathbb{R})$ be symmetric. $A$ called positive definite if:: for all $u \in \mathbb{R}^{n}, u \neq 0$, $$u^{T}Au>0$$
<!--SR:!2025-04-28,18,192-->

Let $A \in M_{m \times n}(\mathbb{R})$ be symmetric and positive definite. Then the formula $\langle u,v \rangle=u^{T}Av$ defines:: an inner product.
<!--SR:!2025-04-27,18,212-->


