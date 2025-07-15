---
tags:
  - MATH240
---
# Permutations and combinations

A $k$-permutation of a set with $n$ elements is:: an ordered arrangement of $k$ elements from that set.
<!--SR:!2025-05-09,57,230-->

The number of $k$-permutations $P(n,k)=$::$n \times (n-1) \times \dots \times (n-k+1)=\frac{n!}{(n-k)!}$
<!--SR:!2025-04-14,51,250-->

The number of $k$-combinations (subsets with $k$ elements) $C(n,k)=$::$\frac{P(n,k)}{k!}=\frac{n!}{(n-k)!k!}=\binom{n}{k}$
<!--SR:!2025-09-15,142,250-->

To determine the number of ways to distribute $n$ identical items into $k$ distinct groups, the formula is::$\binom{n+k-1}{k-1}$ (stars and bars)
<!--SR:!2025-05-14,18,150-->


$\rightarrow$ $\binom{n}{k}=$::$\binom{n}{n-k}$
<!--SR:!2025-05-13,62,230-->
$\rightarrow$ $\binom{n+1}{k}=$::$\binom{n}{k-1}+\binom{n}{k}$ (Pascal's identity)
<!--SR:!2025-05-11,61,230-->