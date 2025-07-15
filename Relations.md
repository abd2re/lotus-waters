---
tags:
  - MATH240
---
# Relations

Given a set $A$, a (binary) relation is:: a set $\mathbb{R}\subseteq A \times A$. (ex, unit circle).
<!--SR:!2025-05-07,32,230-->

Instead of writing $(x,y) \in \mathbb{R}$ we can write::$x \mathbb{R}y$ (Infix notation).
<!--SR:!2025-05-20,42,250-->

- A relation $\mathbb{R}$ on a set $A$ is **reflexive** if:: $\forall x \in A, x \mathbb{R}x$.
<!--SR:!2025-05-23,43,250-->
- $\mathbb{R}\subseteq A \times A$ is **transitive** if:: $\forall x \in A, \forall y \in A, \forall z \in A$, $(x \mathbb{R}y \land y \mathbb{R}z)\implies (x \mathbb{R}z)$.
<!--SR:!2025-05-23,39,230-->
- $\mathbb{R}\subseteq A \times A$ is **symmetric** if:: $\forall x \in A, \forall y \in A, x \mathbb{R}y \implies y \mathbb{R}x$.
<!--SR:!2025-06-04,39,210-->
- An **equivalence relation** is a relation which:: is **reflexive**, **transitive**, and **symmetric**.
<!--SR:!2025-05-01,29,230-->

Let $\sim$ be an equivalence relation on $A$. For $a \in A$, the **equivalence class** of $a$ is:: the set $[a]_{\sim}=\{x \in A ~|~a \sim x\}$.
<!--SR:!2025-06-08,54,250-->


1. $a \in [a]_{\sim}$. In particular $[a]_{\sim} \neq$::$\emptyset$
<!--SR:!2025-06-27,62,250-->
2. $a \sim b \iff$::$[a]_{\sim }=[b]_{\sim }$
<!--SR:!2025-05-03,30,230-->
3. $a \nsim b \iff$::$[a]_{\sim }\land [b]_{\sim }=\emptyset$
<!--SR:!2025-06-06,41,210-->

Given an equivalence relation $\sim$ on $A$, the **quotient set** $A/\sim$ is:: $A/\sim=\{[a]_{\sim }~|~a \in A\}$
<!--SR:!2025-06-08,43,230-->
