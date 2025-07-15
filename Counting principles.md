---
tags:
  - MATH240
---
# Counting principles

## Product principle

$|A \times B|=$::$|A| \times |B|$. (Product principle)
<!--SR:!2025-04-18,56,250-->

We use the product principle to:: count "simultaneous choices".
<!--SR:!2025-04-28,62,250-->

$|\wp(A)|=$::$2^{|A|}$, because we have two choices for each element to $A$ include it or not in a subset.
<!--SR:!2025-09-18,145,250-->

## Sum principle

If $A \cap B=\emptyset$, then $|A \cup B|=$::$|A|+|B|$ (Sum principle)
<!--SR:!2025-08-08,123,250-->

To use the sum principle, you need:: disjoint sets.
<!--SR:!2025-08-18,129,250-->

## Complement principle

If $A \subseteq B$, then $|B \setminus A|=$::$|B|-|A|$ (Complement principle)
<!--SR:!2025-06-30,86,230-->

## Inclusion-Exclusion principle

$|A \cup B|=$::$|A|+|B|-|A \cap B|$ (Inclusion-Exclusion principle)
<!--SR:!2025-08-28,135,250-->
$|A_{1} \cup A_{2} \cup \dots \cup A_{n}|=$::$\sum\limits_{i=1}^n |A_i| - \sum\limits_{1 \leq i < j \leq n} |A_i \cap A_j| + \sum\limits_{1 \leq i < j < k \leq n} |A_i \cap A_j \cap A_k| - \cdots + (-1)^{n+1} \left| A_1 \cap A_2 \cap \cdots \cap A_n \right|$
<!--SR:!2025-08-03,118,250-->
