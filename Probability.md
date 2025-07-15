---
tags:
  - MATH203
---
# Probability

Uncertainty corresponds to:: a lack of perfect knowledge.
<!--SR:!2025-01-08,59,230-->
Uncertainty could be a consequence of (3):: incomplete observation of a system, unpredictable variation, and simple lack of knowledge of the “state of nature” (current state of future state).
<!--SR:!2025-01-10,37,150-->

## Basics of probability

By probability, we generally mean:: a numerical assessment of the chance of a particular event occurring, given a particular set of circumstances.
<!--SR:!2025-01-05,34,150-->

A set $S$ is:: a collection of individual elements, such as $s$ $$s\in S$$
<!--SR:!2025-02-20,77,210-->

A set $S$ may be (3):
?
- **finite** if it contains a finite number of elements. ex: $\{1,2,3,4\}$
- **countable** if it contains an infinite number of elements that can be listed. ex: $\{1,2,3,4,\dots\}$ or $\mathbb{R}^+$
- **uncountable** if it contains an infinite number of elements that cannot be listed. ex: $[0,1]$ or $(0,1)$
<!--SR:!2024-12-27,38,190-->

$A$ is a subset of $S$ if:: it contains some, all, or none of the elements of $S$.
<!--SR:!2024-12-17,50,250-->
- Expression for $A$ contains some elements of $S$::$A\subset S$
<!--SR:!2025-02-19,95,270-->
- Expression for $A$ contains some or all elements of $S$::$A\subseteq S$
<!--SR:!2024-12-15,49,250-->

The empty set $\emptyset$, is:: a subset that contains no elements.
<!--SR:!2025-02-01,83,270-->

- The intersection of two sets $A$ and $B$ is:: the collection of elements that are elements of both $A$ and $B$. $s\in A\cap B$ means $s\in A$ and $s\in B$.
<!--SR:!2024-12-11,47,250-->
- The union of two sets $A$ and $B$ is:: the set of distinct elements that are either in $A$, or in $B$, or in both $A$ and $B$. $s\in A\cup B$ means $s\in A$ or $s\in B$ or $s\in A\cap B$.
<!--SR:!2024-12-11,46,250-->
- The complement of set $A$ is:: the collection of elements of $S$ that are not elements of $A$. $s\in A^{c}$ means $s\in S$ but $s\notin A$.
<!--SR:!2025-01-08,69,270-->

- $A\cup(B\cap C)=$::$(A\cup B)\cap(A\cup C)$
<!--SR:!2025-02-17,86,250-->
- $A\cap(B\cup C)=$::$(A\cap B)\cup(A\cap C)$
<!--SR:!2025-03-26,109,250-->

Probability Venn diagram
?
![[image-20240925163655470.png|center|500]]
<!--SR:!2025-03-02,94,250-->

We all $A_{1},A_{2},\dots,A_{k}$ a partition of $S$ if:: these sets are (2):: pairwise disjoint (or mutually exclusive): $A_{j}\cap A_{k}=\emptyset$ for all $j\neq k$; exhaustive: $\bigcup_{k=1}^{K}A_{k}=S$.
<!--SR:!2024-12-30,59,250-->

- $(A\cap B)^{c}=$::$A^{c}\cup B^{c}$
<!--SR:!2025-01-09,69,270-->
- $(A\cup B)^{c}=$::$A^{c}\cap B^{c}$
<!--SR:!2025-01-30,74,250-->


- An event $A$ is:: a collection of sample outcomes. That is, $A$ is a subset of $S$, $A\subseteq S$.
<!--SR:!2025-01-19,47,170-->
- We say that event $A$ occurs if:: the actual outcome $s$, is an element of A.
<!--SR:!2025-01-18,43,150-->
- The event $S$ is termed:: the certain event.
<!--SR:!2024-12-22,54,250-->
- The event $\emptyset$ is termed:: the impossible event.
<!--SR:!2025-01-28,80,270-->

### Probability

- For any $A$, $P(A^{c})=$::$1-P(A)$
<!--SR:!2025-02-17,94,270-->
- $P(\emptyset)=$::$0$
<!--SR:!2024-12-20,66,310-->
- $P(S)=$::$1$
<!--SR:!2024-12-26,71,310-->
- For two events $A$ and $B$, if $A\subseteq B$, then:: $P(A)\leq P(B)$
<!--SR:!2025-02-21,89,250-->
- $P(A\cup B)=$::$P(A)+P(B)-P(A\cap B)$
<!--SR:!2025-02-04,85,270-->

Boole's Inequality states that $P(\bigcup_{k=1}^{K}A_{k})\leq$::$\sum_{k=1}^{K}P(A_{k})$
<!--SR:!2024-12-22,16,183-->

### Counting rules

- $P_{r}^{n}=$::$\frac{n!}{(n-r)!}=r!C_{r}^{n}$
<!--SR:!2025-02-18,79,241-->
- $C_{r}^{n}=$::$\binom{n}{r}=\frac{n!}{r!(n-r)!}$
<!--SR:!2025-02-06,71,241-->
- $(a+b)^{n}=\sum_{r=0}^{n}\binom{n}{r}a^{r}b^{n-r}$

### Conditional probability
- $P(A/B)=$::$\frac{P(A\cap B)}{B}$
<!--SR:!2025-02-09,71,239-->

### Independence
Two events $A$ and $B$ in sample space $S$ are **independent** if:: $P(A/B)=P(A)$ and equivalently $P(A\cap B)=P(A)P(B)$.
<!--SR:!2024-12-13,13,181-->

### General Multiplication Rule
- For events $A_{1}$, $A_{2}$, $\dots$, $A_{K}$, we have the general result that $P(A_{1}\cap A_{2}\cap \dots\cap A_{K})=$::$P(A_{1})\times P(A_{2}|A_{1})\times P(A_{3}|A_{1}\cap A_{2})\times \dots \times P(A_{K}|A_{1}\cap A_{2} \cap \dots \cap A_{k-1})$ (Chain rule)
<!--SR:!2024-12-07,14,130-->
- For events $A_{1}$, $A_{2}$, $\dots$, $A_{K}$, if the events are mutually exclusive, we have the general result that $P(A_{1}\cap A_{2}\cap \dots\cap A_{K})=$::$\prod_{k=1}^{K}P(A_{k})$
<!--SR:!2024-12-27,40,201-->

Probability tree::![[image-20241007153151546.png|center|500]]
<!--SR:!2025-02-20,79,241-->

### Theorem of Total Probability

For two events $A$ and $B$ in sample space $S$, we have the partition of $A$ as $A=$::$(A\cap B)\cup (A\cap B^{c})$. Which equates to $P(A)=P(A\cap B)\cup P(A\cap B^{c})=P(A/B)P(B)+P(A/B^{c})P(B^{c})$
<!--SR:!2024-12-14,19,181-->

### Bayes Theorem
For  two event $A$ and $B$ with $P(A)>0$ and $P(B)>0$, $$P(B/A)=\frac{P(A\cap B)}{P(A)}$$, if $0<P(B)<1$, then we may expand the numerator and denominator using the theorem of total probability to have::$$P(B/A)=\frac{P(A/B)P(B)}{P(A/B)P(B) +P(A/B^C )P(B^C)}$$
<!--SR:!2024-12-16,20,201-->