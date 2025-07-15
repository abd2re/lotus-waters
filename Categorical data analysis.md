---
tags:
  - MATH204
---
# Categorical data analysis

## Categorical Data and the Multinomial Experiment

Nonparametric methods properties
?
- Do not depend on any assumptions about the parameters of the parent population.
- Generally, assume data are only measured at the nominal or ordinal level.
<!--SR:!2025-04-17,9,210-->

Qualitative data that fall in more than two categories often result from:: a multinomial experiment
<!--SR:!2025-04-25,29,230-->

Properties of the Multinomial Experiment
?
1. The experiment consists of $n$ identical trials.
2. There are $k$ possible outcomes to each trial. These outcomes are called classes, categories, or cells.
3. The probabilities of the $k$ outcomes, denoted by $p_{1}, p_{2},\dots , p_{k}$, remain the same from trial to trial, where $p_1 + p_2 + \dots  + p_k = 1$.
4. The trials are independent.
5. The random variables of interest are the cell counts, $n_1, n_2,\dots , n_k$, of the number of observations that fall in each of the k classes.
<!--SR:!2025-04-28,31,230-->

## Testing Category Probabilities: One-Way Table

One-Way Contingency Table
?
![[Pasted image 20250304143522.png]]
<!--SR:!2025-05-29,54,250-->

A Test of a Hypothesis about Multinomial Probabilities: One-Way Table
?
![[Pasted image 20250304143632.png]]
![[Pasted image 20250304144107.png]]
<!--SR:!2025-04-14,2,150-->

Conditions Required for a Valid Test: One-way Table
?
1. A multinomial experiment has been conducted. This is generally satisfied by taking a random sample from the population of interest.
2. The sample size $n$ is large. This is satisfied if for every cell, the expected cell count $E_i$ will be equal to 5 or more.
<!--SR:!2025-05-07,38,230-->

$\chi^{2}$ Test Basic Idea
?
1. Compares observed count to expected count assuming null hypothesis is true
2. Closer observed count is to expected count, the more likely the $H_0$ is true. Measured by squared difference relative to expected count - reject large values
<!--SR:!2025-04-17,4,150-->


## Testing Category Probabilities:Two-Way (Contingency) Table

A two-way table , called a contingency table, shows:: the multinomial count data classified on two scales, or dimensions, of classification. ![[Pasted image 20250306142337.png]]
<!--SR:!2025-04-24,27,236-->

The estimate of the expected number of observations falling into the cell in row i and column j is given by
?
![[Pasted image 20250306143023.png]]
where Ri = total for row i, Cj = total for column j, and n = sample size.
<!--SR:!2025-04-21,17,176-->


General Form of a Two-Way (Contingency) Table Analysis: c2 -Test for Independence
?
![[Pasted image 20250306143840.png]]
<!--SR:!2025-04-18,9,196-->

