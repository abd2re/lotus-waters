## Q2

$\rightarrow$ Let's show $(A \cap B) \times C\subseteq (A \times C) \cap (B \times C)$

If $(x, y) \in (A \cap B) \times C$, by definition of Cartesian product and intersection, this means:
- $x \in A \cap B$, so $x \in A$ and $x \in B$,
- $y \in C$

Hence, $(x, y)$ belongs to both $A\times C$ (since $x\in A$ and $y\in C$) and $B\times C$ (since $x\in B$ and $y\in C$). Therefore, $(x, y) \in (A\times C) \cap (B\times C)$.

$\rightarrow$ Let's show $(A\times C)\cap(B\times C) \;\subseteq\; (A \cap B)\times C$

Take any element $(x, y) \in (A\times C) \cap (B\times C)$. Then $(x, y)$ is in both $A\times C$ and $B\times C$, which implies:
- From $(x, y) \in A\times C$, we get $x \in A$ and $y \in C$.
- From $(x, y) \in B\times C$, we get $x \in B$ and $y \in C$.

Combining these, $x \in A \cap B$ and $y \in C$. Hence, $(x, y) \in (A \cap B)\times C$.

Since we have shown both inclusions, the two sets are equal:
$$
(A \cap B)\times C \;=\; (A\times C) \;\cap\; (B\times C).
$$
