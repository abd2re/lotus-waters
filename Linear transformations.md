---
tags:
  - MATH223
---
# Linear transformations

Let $U$, $V$ be vector spaces over $\mathbb{F}$, and let $T:U \rightarrow V$ be a linear transformation if
?
(a) $\forall u_{1},u_{2}\in U$ $$T(u_{1}+u_{2})=T(u_{1})+T(u_{2})$$
(b) $\forall u \in U, c \in \mathbb{F}$ $$T(cu)=cT(u)$$
<!--SR:!2025-04-16,26,190-->

- Let $T: U \rightarrow V$ be a linear transformation, $T(\vec{0})=$::$\vec{0}$
<!--SR:!2025-05-09,60,250-->
- Let $T: U \rightarrow V$ be a linear transformation, $T(\sum\limits_{i=1}^{n}c_{i}u_{i})=$::$\sum\limits_{i=1}^{n}c_{i}T(u_{i})$
<!--SR:!2025-04-30,47,230-->


For any $A \in M_{m \times n}(\mathbb{F})$, define function $L_{A}: \mathbb{F}^{n} \rightarrow \mathbb{F}^{n}$ by:: $$L_{A}(v)=Av$$ for all $v \in F^{n}$.
<!--SR:!2025-04-17,29,170-->

## Kernel and image

- Let $T: U \rightarrow V$ be a linear transformation, the kernel or null space, $\ker(T)=$::$\{u \in U ~|~T(u)=\vec{0}\}\subseteq U$.
<!--SR:!2025-04-14,27,203-->
- Let $T: U \rightarrow V$ be a linear transformation, the image or range of $T$, $\text{Im}(T)=$::$\{v \in V ~|~\exists u \in U\text{ s.t. }v=T(u)\}\subseteq V$.
<!--SR:!2025-05-04,28,150-->


Let $T: U \rightarrow V$ be a linear transformation, then
?
1. $\ker(T)\leq U$ (subspace)
2. $\text{Im}(T)\leq V$ (subspace)
<!--SR:!2025-04-26,27,174-->


$\rightarrow \dim(\text{Im}(T))=$::$\text{rank}(T)$
<!--SR:!2025-04-30,52,263-->
$\rightarrow \dim(\ker(T))=$::$\text{nullity}(T)$
<!--SR:!2025-05-23,68,263-->
$\rightarrow \dim(T)=$::$\dim(\text{Im}(T))+\dim(\ker(T))=\text{rank}(T)+\text{nullity}(T)$
<!--SR:!2025-07-04,89,243-->

$T:U \rightarrow V$ linear, $U=\text{span}(\alpha)$. Denote $T(\alpha)=\{T(u) ~|~u \in \alpha\}$. Then $T(\alpha)$ spans:: $\text{Im}(T)$.
<!--SR:!2025-04-22,17,163-->

### Injective, Surjective

- $f:X \rightarrow Y$ function ($X$, $Y$ any sets) called injective (or one-to-one) if:: $\forall x_{1},x_{2} \in X.x_{1}\neq x_{2} \implies f(x_{1})\neq f(x_{2})$ or equivalently $\forall x_{1},x_{2}\in X.f(x_{1})=f(x_{2})\implies x_{1}=x_{2}$.
<!--SR:!2025-04-17,32,178-->
- $f:X \rightarrow Y$ function ($X$, $Y$ any sets) called surjective (or onto) if:: $\forall y \in Y \exists x \in X.f(x)=y$ or equivalently $\text{Im}(f)=Y$.
<!--SR:!2025-05-11,35,182-->
- $f:X \rightarrow Y$ function ($X$, $Y$ any sets) called bijective if:: injective and surjective.
<!--SR:!2025-05-14,54,238-->

1. For $X$, $Y$ finite, if $|X|>|Y|$, $f$ is:: not injective.
<!--SR:!2025-04-15,16,222-->
2. For $X$, $Y$ finite, if $|X|<|Y|$, $f$ is:: not surjective.
<!--SR:!2025-04-14,40,242-->
3. For $X$, $Y$ finite, if $|X|=|Y|$, $f$ injective $\iff$:: $f$ surjective.
<!--SR:!2025-05-20,60,242-->
4. For any $X,~Y$ (finite or infinite), $f$ bijective $\iff$:: $f$ invertible i.e. $\exists f^{-1}:Y \rightarrow X$.
<!--SR:!2025-05-16,35,198-->


$\rightarrow T:U \rightarrow V$ linear, $U,V$ finite dimensional, $T$ injective $\iff$ $\ker(T)=$::$\{\vec{0}\}\implies \text{nullity}(T)=0$
<!--SR:!2025-05-05,50,242-->
$\rightarrow T:U \rightarrow V$ linear, $U,V$ finite dimensional, $T$ injective $\iff \text{Im}(T)=$::$V \implies \text{rank}(T)=\dim V$.
<!--SR:!2025-04-29,19,218-->


### Isomorphism and coordinates

If $T:U \rightarrow V$ is linear and bijective, $T$ is called an:: isomorphism.
<!--SR:!2025-04-25,32,194-->
If $U$, $V$ are vector spaces and $\exists T:U \to V$ isomorphism, say $U$ isomorphic to $V$, write::$$U \cong V$$.
<!--SR:!2025-04-13,30,194-->

Let $\beta=\{v_{1},\dots ,v_{n}\}$ basis of $V$. Then every $v \in V$ has a unique expression $v=\sum\limits_{i=1}^{n}c_{i}v_{i}$ as linear combination of basis elements. The vector $(c_{1},c_{2},\dots ,c_{n}) \in \mathbb{F}^{n}$ of coefficients called:: the coordinate vector of $v$ relative to $\beta$, denoted $[v]_{\beta}=[c_{1},\dots ,c_{n}]$.
<!--SR:!2025-04-15,32,194-->

$V$ vector space, $\dim V=n$ finite, $\beta$ basis. The function which computes coordinates $[-]_{\beta}:V \to \mathbb{F}^{n}$ is an isomorphism. Hence:: $V \cong \mathbb{F}^{n}$ ($n= \dim V$)
<!--SR:!2025-04-26,23,154-->


1. Let $S:U \to V$, $T: V \to W$ linear, the composition $T \circ S:U \to W$  is:: linear.
<!--SR:!2025-06-01,58,225-->
2. Let $S:U \to V$, $T: V \to W$ linear, if $S$, $T$ both isomorphisms, $T \circ S$ is:: also an isomorphism.
<!--SR:!2025-05-29,56,226-->
3. Let $S:U \to V$, $T: V \to W$ linear, if $T$ is an isomorphism, $\exists$ inverse:: $T^{-1}: W \to V$ and $T^{-1}$ is an isomorphism.
<!--SR:!2025-05-14,46,205-->


Let $U$, $V$ finite dimension vector spaces over $\mathbb{F}$. Then $U \cong V \iff$::$\dim U = \dim V$.
<!--SR:!2025-06-02,51,206-->

$\to \mathbb{R}^{n}\cong \mathbb{R}^{m}\iff$::$n=m$
<!--SR:!2025-05-21,53,225-->


### Matrix of a linear transformation

$T: U \to V$ linear, $\alpha=\{u_{1},\dots ,u_{n}\}$, $\beta=\{v_{1},\dots ,v_{n}\}$ bases of $U$, $V$. The matrix of $T$ relative to $\alpha$ and $\beta$ is:: the $m \times n$ matrix $[T]_{\alpha}^{\beta}$ whose matrix $i$-th column is $$[T(u_{i})]_\beta$$ (ie. apply $T$ to a basis $\alpha$, put results in $\beta$-coordinates as columns).
<!--SR:!2025-04-15,7,130-->


Let $T: U \to V$ linear, $\alpha$, $\beta$ basis of $U$, $V$. Then $\forall u \in U$, $[T]_{\alpha}^{\beta}[u]_{\alpha}=$::$[T(u)]_{\beta}$.
<!--SR:!2025-05-26,47,205-->

$T:V \to V$ (same $V$) linear transformation is called:: linear operator. If $\dim v = n$, $[T]$ is $n \times n$. Usually, use same basis $\alpha$ for both $V$, write $[T]_{\alpha}^{\alpha}=[T]_{\alpha}$.
<!--SR:!2025-04-29,20,150-->

1. $T:U \to V$ linear operator, $\alpha$ and $\beta$ bases of $V$, $\dim V$ finite. Then $T$ invertible $\iff [T]_{\alpha}^{\beta}$ and if $T$ invertible then $[T^{-1}]_{\beta}^{\alpha}=$::$([T]_{\alpha}^{\beta})^{-1}$.
<!--SR:!2025-05-28,47,202-->
2. $T:U \to V$ linear with bases $\alpha, \beta, \gamma$ bases of $U$, $V$, $W$. Let $A=[T]_{\alpha}^{\beta}$, $B=[S]_{\beta}^{\gamma}$, Then $[S \circ T]=$::$BA=[S]_{\beta}^{\gamma}[T]_{\alpha}^{\beta}$
<!--SR:!2025-04-19,29,202-->

### Change of basis

The change-of-coordinates matrix from $\alpha$ to $\beta$ is:: the $n \times n$ matrix ($n=\dim V$) $$Q_{\alpha}^{\beta}=[I]_{\alpha}^{\beta}$$ i.e. columns of $Q_{\alpha}^{\beta}$ are the $\alpha$ basis vectors in $\beta$-coordinates.
<!--SR:!2025-04-13,13,150-->

$T:V \to V$ linear operator, $\alpha, \beta$, bases of $V$, then $Q_{\alpha}^{\beta}[T]_{\alpha}^{\alpha}Q_{\beta}^{\alpha}=$::$[T]_{\beta}^{\beta}$
<!--SR:!2025-04-20,26,177-->

$A,B \in M_{n \times n}(\mathbb{F})$ called similar matrices if:: $\exists$ invertible $Q \in M_{n\times n}(\mathbb{F})$ such that $Q^{-1}AQ=B$
<!--SR:!2025-04-17,8,130-->

Let $U, W$ be vector spaces over $\mathbb{F}$. Denote $L(V,W)=$::$\{T:V \to W ~|~T \text{ linear}\}$
<!--SR:!2025-04-16,9,150-->

If $\dim V=n$, $\dim W = m$, then $L(V,W)\cong$::$M_{m \times n}(\mathbb{F})$ and if $\alpha$ basis of $V$, $\beta$ bases of $W$, then $\phi:L(V,W)\to M_{m\times n}(\mathbb{F})$ defined by $\phi(T)=[T]_{\alpha}^{\beta}$ is an isomorphism.
<!--SR:!2025-04-15,4,130-->

