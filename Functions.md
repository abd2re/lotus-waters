---
tags:
  - MATH240
---
# Functions

Given two sets $A$ (the domain) and $B$ (the codomain), a function $f:A \to B$ is:: a process which takes an input $x \in A$ and returns and output $y=f(x)\in B$.
<!--SR:!2025-06-13,62,250-->

Range $\subseteq$::Codomain.
<!--SR:!2025-05-23,27,230-->

1. A function $f: A \to B$ is injective (one-to-one) if:: $\forall a,b \in A,~f(a)=f(b) \implies a=b$.
<!--SR:!2025-06-12,62,250-->
2. A function $f: A \to B$ is surjective (onto) if:: $\forall y \in B,~\exists x \in A,~f(x)=y$.
<!--SR:!2025-06-21,56,230-->
3. A function $f: A \to B$ is bijective (or a bijection) if:: it is injective and surjective.
<!--SR:!2025-05-18,45,250-->
If $f: A \to B$ and $g: B \to C$, their composite is:: $g \circ f: A \to C$, $(g \circ f)(x)=g(f(x))$.
<!--SR:!2025-05-17,45,250-->

4. Let $f: A \to B$, $g: B \to C$. If $f$ and $g$ are injective, then $g \circ f$ is:: injective.
<!--SR:!2025-04-30,30,246-->
5. Let $f: A \to B$, $g: B \to C$. If $f$ and $g$ are surjective, then $g \circ f$ is:: surjective.
<!--SR:!2025-07-17,82,286-->
6. Let $f: A \to B$, $g: B \to C$. If $f$ and $g$ are bijective, then $g \circ f$ is:: bijective.
<!--SR:!2025-05-04,36,286-->

If $f: A \to B$ is bijective, then $\forall y \in B$, there exists:: a unique $x \in A$ such that $f(x)=y$.
<!--SR:!2025-05-01,34,230-->

Give $f: A \to B$, the inverse function (if it exists) is:: the unique function $f^{-1}:B \to A$ such that $$\forall x \in A,~(f^{-1} \circ f)(x)=x$$ $$\forall y \in B,~(f \circ f^{-1})(y)=y$$
<!--SR:!2025-07-03,68,230-->

Bijective function $\iff$:: function is invertible.
<!--SR:!2025-06-12,64,270-->