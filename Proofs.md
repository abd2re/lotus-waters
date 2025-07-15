---
tags:
  - MATH240
---
# Proofs

## Direct proofs

$\exists$ve wants to prove a conjecture, by making choices on the $\exists$ variables. $\forall$dam has control over $\forall$... Proof =:: Winning strategy for $\exists$ve.
<!--SR:!2025-05-10,60,250-->

$\rightarrow$ To prove $\exists .p(x)$:: find an example which makes $p(x)$ true.
<!--SR:!2025-04-29,52,250-->
$\rightarrow$ To prove $\forall x.p(x)$:: need a general argument. Let $x$ be given, and prove $p(x)$ for that $x$.
<!--SR:!2025-05-11,59,250-->
$\rightarrow$ To prove $p \implies q$:: assume $p$, prove $q$.
<!--SR:!2025-05-06,56,250-->
$\rightarrow$ To prove $p \land q$:: prove $p$ and prove $q$.
<!--SR:!2025-05-01,52,250-->
$\rightarrow$ To prove $p \lor q$:: prove $p$ or prove $q$ (you choose) (this can also be $p \lor q \equiv \neg p \implies q$).
<!--SR:!2025-05-04,55,250-->
$\rightarrow$ To prove $p \iff q$:: prove $p \implies q$ and prove $q \implies p$.
<!--SR:!2025-08-21,117,250-->
$\rightarrow$ To prove $\neg p$:: negate $p$ (using De Morgan) and prove the resulting conjecture.
<!--SR:!2025-04-28,43,210-->

Once a conjecture is proven, it becomes:: a theorem.
<!--SR:!2025-05-14,61,250-->

## Proofs by contrapositive

To prove $p \implies q$, you can instead prove:: $\neg q \implies \neg p$ (the contrapositive). $p \implies q \equiv \neg q \implies \neg p$
<!--SR:!2025-05-13,60,250-->

$\rightarrow$ Contrapositive $\neq$:: converse. The converse of $p \implies q$ is $q \implies p$ which is not equivalent.
<!--SR:!2025-05-05,54,250-->


$\rightarrow$ Floor $x=$::$\lfloor{x}\rfloor=$ Greatest integer $\leq x$
<!--SR:!2025-06-04,83,289-->
$\rightarrow$ Ceiling $x=$::$\lceil{x}\rceil=$ Least integer $\geq x$
<!--SR:!2025-06-07,80,289-->

General Pigeonhole Principle (GPHP) theorem says:: if we have $n$ pigeons, $k$ holes, then there is at least one hole which contains at least $\lceil{\frac{n}{k}}\rceil$ pigeons.
<!--SR:!2025-05-05,31,229-->

## Proof by contradiction

To prove $p$:: assume $\neg p$, and prove a contradiction, $p \equiv \neg p \implies 0$
<!--SR:!2025-05-12,52,229-->

## Proof by cases

To prove $(A_{1}\lor A_{2}\lor \dots \lor A_{n})\implies C$, you need to prove the following:
?
case $1$. $A_{1} \implies C$
case $2$. $A_{2} \implies C$
$\vdots$
case $n$. $A_{n} \implies C$
The catch is that the cases to consider are generally not explicitly specified (you need to figure them out).
<!--SR:!2025-06-13,76,249-->

## Proof by induction

For proving statements of the form:: $\forall n \in \mathbb{N}.P(n)$ (not $\mathbb{Z},\mathbb{R},\mathbb{Q},\text{etc..}$)
<!--SR:!2025-05-11,54,250-->

Two steps are
?
1. **Base case**: Prove $P(0)$ (or $P$ of the first number considered)
2. **Induction step**: For a given $n$, prove $$P(n) \implies P(n+1)$$ or $P(n-1)\implies P(n)$
Then we can conclude $P(n)$ is true for all $n$.
<!--SR:!2025-05-03,50,250-->


Strong induction steps
?
1. Base case
2. Induction step but you give a strong induction hypothesis. Assume $P(k)$ is true for all $k<n$ and the goal is to prove $P(n)$.
Conclusion $P(n)$ is true for all $n$.
<!--SR:!2025-07-07,84,230-->