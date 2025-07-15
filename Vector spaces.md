---
tags:
  - MATH223
---
 # Vector spaces

## Vector space axioms

In a field we can:: add/substract, multiply and divide by non-zero elements. $\mathbb{Q}$, $\mathbb{R}$, $\mathbb{C}$ are called fields. $\mathbb{Z}$ is not a field because of division. In this course $\mathbb{F}$ denotes a field which is always $\mathbb{R}$ or $\mathbb{C}$.
<!--SR:!2025-06-21,83,210-->

Let $\mathbb{F}$ be a field, $V$ is a set. Elements of $\mathbb{F}$ called scalars, elements of $V$ called vectors. Assume we have defined:
- addition: given $u,~w \in V$, there is a vector $u+w \in V$
- scalar multiplication: given $u \in V$, $c \in \mathbb{F}$, there is a vector $cu$
If the following 8 axioms (properties) hold, $V$ is called vector space over $\mathbb{F}$:
?
1) $\forall ~u,~w \in V$: $u+w=w+u$ (commutativity)
2) $\forall ~u,~v,~w \in V$: $(u+v)+w=u+(v+w)$ (associativity)
3) $\exists$ vector denoted $\vec{0}\in V$ called the zero vector which satisfies $\forall ~u \in V$: $u+\vec{0}=u$
4) $\forall ~u\in V$: $\exists$ a vector denoted $-u\in V$, called additive inverse, which satisfies: $u+(-u)=\vec{0}$
5) $\forall ~u\in V$: $1u=u$
6) $\forall ~a,~b \in \mathbb{F},~u\in V$: $(ab)u=a(bu)$
7) $\forall ~a \in \mathbb{F},~u,~w \in V$: $a(u+w)=au+aw$
8) $\forall ~a,~b \in \mathbb{F},~u\in V$: $(a+b)u=au+bu$
<!--SR:!2025-06-03,73,210-->

- $\mathbb{F}^{n}=$::$(\mathbb{R}^{n},~\mathbb{C}^n)$
<!--SR:!2025-06-06,83,241-->
- $M_{m \times n}(\mathbb{F})=$:: all $m \times n$ matrices with entries from $\mathbb{F}$.
<!--SR:!2025-04-14,56,261-->
- $P(\mathbb{F})=$:: all polynomials (one variable) with coefficients from $\mathbb{F}$
<!--SR:!2025-08-10,120,241-->
- $F(\mathbb{F},~\mathbb{F})=$:: set of all functions $f:~\mathbb{F}\rightarrow \mathbb{F}$
<!--SR:!2025-06-11,88,241-->

Basic vector space properties. Let $V$ be a vector space over $\mathbb{F}$, the properties are:
?
1) $\forall~u,~v,~w \in V: u+w=v+w \rightarrow u=v$
2) $\vec{0}$ is unique
3) $\forall ~u \in V$: $-u$ is unique
4) $\forall ~u \in V:0u=\vec{0}$
5) $\forall ~c\in \mathbb{F}:c\vec{0}=\vec{0}$
6) $\forall ~c\in \mathbb{F},~u \in V:(-c)u=c(-u)=-(cu)$
<!--SR:!2025-04-18,54,241-->

## Linear combinations and subspaces

A linear combination of vectors $u_{1},~u_{2},~\dots ,u_{n}\in V$ is:: a vector of form $$c_{1}u_{1}+c_{2}u_{2}+\dots +c_{n}u_{n}$$
<!--SR:!2025-07-07,95,221-->
Let $S=\{u_{1},~u_{2},~\dots ,~u_{n}\}\subseteq V$. The span of $S$ is:: the set of all linear of combinations of $S$, $$\text{span}\{c_{1}u_{1}+c_{2}u_{2}+\dots +c_{n}u_{n}~|~c_{1},~c_{2},~\dots ,~c_{n}\in \mathbb{F}\}$$. As a special case, if $S=\emptyset$, we define $\text{span}(\emptyset)=\{\vec{0}\}$.
<!--SR:!2025-05-14,70,241-->


Let $A \in M_{m \times n}(\mathbb{F})$ denoted $A=\begin{pmatrix}r_{1}\\ r_{2}\\ \vdots \\ r_{m}\end{pmatrix}$, $r_{i}$ = $i$th row of $A$, $r_{i}\in \mathbb{F}^{n}$.
The row space of $A$ is:
?
$$\text{row}(A)=\text{span}\{r_{1},~\dots ,~r_{m}\}$$
<!--SR:!2025-05-26,76,240-->

If $A,~B \in M_{m \times n}(\mathbb{F})$ and $B$ is obtained from $A$ by elementary row operation (ERO), then $\text{row}(A)=$::$\text{row}(B)$
<!--SR:!2025-07-14,111,260-->

Span properties, let $S \subseteq V$, then:
?
1. $\forall ~u,~w \in \text{span}(S):u+w \in \text{span}(S)$ (closed under addition)
2. $\forall u \in \text{span}(S),~c \in \mathbb{F},~cu \in \text{span}(S)$ (closed under scalar multiplication)
3. $\vec{0}\in \text{span}(S)$
<!--SR:!2025-04-26,18,200-->

Let $W \subseteq V$, $W$ called a subspace of $V$ if we have these properties:
?
1. $\forall ~w_{1},~w_{2} \in W:w_{1} +w_{2} \in W$ (closed under addition)
2. $\forall w \in W,~c \in \mathbb{F},~cw \in W$ (closed under scalar multiplication)
3. $\vec{0}\in W$
If so, we write  $W \leq V$
<!--SR:!2025-07-09,94,220-->

$\rightarrow$ Every $\text{span}(S)$ is a:: subspace.
<!--SR:!2025-07-18,99,220-->
$\rightarrow$ A subspace is a:: vector space, because it satisfies the 3 span properties from its parent by default. A subspace is also a span.
<!--SR:!2025-04-26,58,240-->


Let $A \in M_{m \times n}(\mathbb{F}),~b \in \mathbb{F}^{m},~x=\begin{pmatrix}x_{1}\\ x_{2}\\ \vdots\\ x_{n}\end{pmatrix}$ (variables). Let $S$ be all solutions to the linear system $Ax=b$. Then $S$ is:: a subspace of $\mathbb{F}^{n}\iff b=\vec{0}_{n}$. (system is homogenous).
<!--SR:!2025-04-25,40,179-->


$\rightarrow$ Span and subspaces are:: the same thing.
<!--SR:!2025-06-06,80,239-->
$\rightarrow$ $\text{span}(S)$ is the smallest:: subspace containing $S$.
<!--SR:!2025-05-22,59,199-->


## Linear independence and dependence

When one vector is a linear combination of others, that vector is:: unnecessary.
<!--SR:!2025-06-12,83,239-->

Let $S \subseteq V$. $S$ is called linearly dependent if:: $\exists$ distinct $u_{1},u_{2},\dots ,u_{n}\in S$ and scalars $c_{1},c_{2},\dots ,c_{n}\in \mathbb{F}$ not all $0$ such that $c_{1}u_{1}+c_{2}u_{2}+\dots c_{n}u_{n}=\vec{0}$.
<!--SR:!2025-04-19,50,219-->


$S \subseteq V$ is linearly independent if:: not dependent. Equivalent $\forall u1,\dots ,u_{n}\in S$ (distinct) if $c1,\dots ,c_{n}\in \mathbb{F}$ such that $c_{1}u_{1}+\dots +c_{n}u_{n}=\vec{0}$ then $c_{i}=0$ for all $i$.
<!--SR:!2025-06-01,75,236-->

## Basis and dimension

Let $W\leq V$, $\beta \subseteq W$. $\beta$ called a basis of $W$ if:
?
1) $W=\text{span}(\beta)$ ($\beta$ has enough vectors to create/describe $W$)
2) $\beta$ is independent (no excess vectors in $\beta$)
<!--SR:!2025-04-20,17,156-->

Let $W=\text{span}(S)$, with $S$ finite. Then $W$ has a finite basis and all bases of $W$ have:: the same size.
<!--SR:!2025-04-21,48,216-->

If vector $V$ (or subspace) has finite bases, we call $V$:: finite dimensional.
<!--SR:!2025-05-29,72,236-->

Dimension of $V$, $\dim(V)$, is the size of:: any basis. If not finite basis, $V$ is called infinite dimensional.
<!--SR:!2025-05-04,33,216-->

- $\dim(\mathbb{F}^{n})=$::$n$
<!--SR:!2025-05-11,36,216-->
- $\dim(M_{m \times n}(\mathbb{F}))=$::$mn$
<!--SR:!2025-05-05,57,236-->
- $\dim(P_{n}(F))=$::$n+1$
<!--SR:!2025-06-23,79,216-->
- $\dim(P(F))=$::$\infty$ (infinite dimensional)
<!--SR:!2025-06-08,87,276-->
- $\dim(F(\mathbb{F},\mathbb{F}))=$::$\infty$ (infinite dimensional)
<!--SR:!2025-05-14,63,236-->

For $A \in M_{m \times n}(\mathbb{F})$, the null space or kernel of $A$ is:: $$\text{Null}(A)=\{u \in \mathbb{F}^{n} ~|~Au=\vec{0}\}$$. Fact: $\text{Null}(A)$ is a subspace of $\mathbb{F}^{n}$
<!--SR:!2025-04-25,27,156-->

- Suppose $\dim(W)=n$ (finite), $S \subseteq W$. If $W=\text{span}(S)$, then $|S|$::$\geq n$ and $\exists ~\beta \subseteq S$ s.t. $\beta$ is a basis of $W$. (spanning sets can be reduced to a basis)
<!--SR:!2025-04-11,28,156-->
- Suppose $\dim(W)=n$ (finite), $S \subseteq W$. If $S$ is independent, $|S|$::$\leq n$ and $\exists$ basis $\beta$ s.t. $S \subseteq \beta$ ($S$ can be extended to a basis).
<!--SR:!2025-06-08,79,236-->
- Suppose $\dim(W)=n$ (finite), $S \subseteq W$. If $|S|=n$, $W=\text{span}(S)\iff$::$S$ independent.
<!--SR:!2025-04-20,27,216-->

## Subspaces

- Let $W \leq V$, $\dim(V)=n$ finite. $\dim W$ is:: $\leq n$
<!--SR:!2025-05-11,60,232-->
- Let $W \leq V$, $\dim(V)=n$ finite. $\dim W=n \iff$::$W=V$
<!--SR:!2025-04-19,16,172-->

$A \in M_{m \times n}(\mathbb{F})$. The columns space of $A$ is the span of the columns of $A$.$$\text{col}(A) \leq \mathbb{F}^{m}$$

- Let $A \in M_{m \times n}(\mathbb{F})$, $R$ the row-reduce echelon form of $A$. Then a basis for $\text{row}(A)$ is given by:: the non-zero rows of R.
<!--SR:!2025-06-01,64,212-->
- Let $A \in M_{m \times n}(\mathbb{F})$, $R$ the row-reduce echelon form of $A$. The columns of $A$ that correspond to:: leading entries (pivots) in $R$ form basis of $\text{col}(A)$.
<!--SR:!2025-05-14,54,212-->


Let $U \leq V$, $W \leq V$ (subspaces). Then $U \cap W=$::$\{v \in V ~|~v \in U \land v \in W\}$ is a subspace of $V$.
<!--SR:!2025-05-27,47,172-->

$U \cup W$ is not usually a:: subspace
<!--SR:!2025-05-01,50,230-->

$U$, $W$ be subspaces of $V$, the sum of $U$ and $W$ is $$U+W=\{u+w ~|~u \in U, w \in W\}$$
If $V=U+W$, where $U$, $W$ are subspaces of $V$, and every $v \in V$ has unique decomposition in form $v=u+w$, $u \in U$, $w \in W$, then $V$ is:: direct sum of $U$ and $W$, write $V=U \oplus W$.
<!--SR:!2025-05-19,46,170-->

$\rightarrow V=U \oplus W \iff$::$V=U+W \land U \cap W = \{\vec{0}\}$
<!--SR:!2025-04-20,33,169-->

Let $U$, $W$ be finite-dimensional subspaces of $V$. Then $\dim(U+W)=$::$\dim U + \dim W - \dim(U \cap W)$.
<!--SR:!2025-05-23,63,229-->

## Lagrange interpolation

For any $a_{0},a_{1},\dots ,a_{n} \in \mathbb{R}$ distinct define the Lagrange polynomials:: $l_{i}(x)$, $i=0,1,\dots ,n$ by $l_{i}(x)=\frac{(x-a_{0})}{(a_{i}-a_{0})}\frac{(x-a_{1})}{(a_{i}-a_{1})}\cdot ...\frac{(x-a_{n})}{(a_{i}-a_{n})}$ (omit for $a_{i}$), that is $l_{i}(x)=\prod\limits_{j=0,j \neq i}^{n}\frac{x-a_{j}}{a_{i}-a_{j}}$. Note each each $l_{i}(x)$ has degree $n$.
<!--SR:!2025-04-19,7,130-->

$\rightarrow \delta_{ij}=\begin{cases}1 &\text{if }i=j\\0 &\text{if }i \neq j\end{cases}$

1. $l_{i}(a_{j})=$::$\delta_{ij}=\begin{cases}1 &\text{if }i=j\\0 &\text{if }i \neq j\end{cases}$
<!--SR:!2025-04-23,14,166-->
2. $l_{0}(x),\dots ,l_{n}(x)$ form:: a basis of $P_{n}(\mathbb{R})$
<!--SR:!2025-05-08,53,226-->

