---
tags:
  - MATH240
---
# Set theory

A set is:: a collection of objects of the same nature.
<!--SR:!2025-05-16,73,230-->

$\mathbb{Q}=$::$\begin{Bmatrix}\frac{a}{b}~|~a \in \mathbb{Z},~b \in \mathbb{N}^{+},~\text{GCD}(a,~b)=1\end{Bmatrix}$
<!--SR:!2025-09-06,147,250-->

Equality: $A=B$ when they have the same elements, that means:
?
1) If $x \in A$, then $x\in B$. $$A \subseteq B$$, $A$ is a subset of $B$.
2) If $x \in B$, then $x\in A$. $$B \subseteq A$$, $B$ is a subset of $A$.
Order does not matter and repetitions don't count.
<!--SR:!2025-05-29,73,210-->

$|A|$ means:: the cardinality of the set $A$, the number of unique elements in $A$.
<!--SR:!2025-06-10,75,210-->

- If $A \subseteq B$, then $|A|$::$\leq |B|$, but not conversely.
<!--SR:!2025-09-09,148,250-->
- If $A=B$, then $|A|$::$=|B|$, but not conversely.
<!--SR:!2025-09-07,147,270-->

- $A=\begin{Bmatrix}1,~3,~5\end{Bmatrix}=\begin{Bmatrix}1,~3,~1,~5\end{Bmatrix}$, $|A|=$::$3$
<!--SR:!2025-08-02,138,290-->
- $|\emptyset|=$::$0$
<!--SR:!2025-06-29,114,290-->
- $|\{\emptyset\}|=$::$1$
<!--SR:!2025-05-04,35,190-->
- $|\mathbb{Z}|=$::$\infty$
<!--SR:!2025-07-09,121,290-->


Set theory is always relative to:: context.
<!--SR:!2025-09-09-02,142250-->


## Set operations
Assuming a universe $U$
- Set intersection: $A \cap B=$::$\begin{Bmatrix}x \in U ~|~x \in A \land x \in B\end{Bmatrix}$
<!--SR:!2025-06-06,94,270-->
- Set union: $A \cup B=$::$\begin{Bmatrix}x \in U ~|~x\in A \lor x \in B \lor x \in (A \cap B)\end{Bmatrix}$
<!--SR:!2025-07-27,107,230-->
- Set difference: $A \setminus B=$::$\begin{Bmatrix}x \in U ~|~x \in A \land x \notin B\end{Bmatrix}$
<!--SR:!2025-05-19,66,230-->
- Complement: $\neg A=$::$\{x \in U ~|~x \notin A\}$
<!--SR:!2025-07-12,109,250-->
- Symmetric difference: $A \triangle B=$::$(A \setminus B) \cup (B \setminus A)=(A \cup B)\setminus (A \cap B)$
<!--SR:!2025-07-03,104,250-->

If two sets, $A$ and $B$, have the same Venn diagram, then:: $A=B$.
<!--SR:!2025-05-14,79,270-->

Which of intersection or union has higher precedence?:: intersection.
<!--SR:!2025-07-24,117,250-->

- Cartesian product: $A \times B=$::$\{(x,y) ~|~x \in A \land y \in B\}$. Note that it's not commutative $A \times B \neq B \times A$.
<!--SR:!2025-04-29,62,230-->
- Powerset: $\wp(A)=$::$\{a ~|~a \subseteq A\}$, the set of all possible subsets of $A$ including $\emptyset$.
<!--SR:!2025-06-29,102,250-->

