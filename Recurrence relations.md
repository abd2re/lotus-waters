---
tags:
  - MATH240
---
# Recurrence relations

A recursive definition of an infinite sequence $(a_{n})_{n \in \mathbb{N}}$ is a definition in two steps:
?
1. Base case: Define the first numbers of the sequence.
2. Recursive step: A general definition of $a_{n}$ in terms of $a_{k}$ ($k<n$).
<!--SR:!2025-05-16,20,210-->

If $(p_{n})_{n \in \mathbb{N}}$ and $(q_{n})_{n \in \mathbb{N}}$ are two particular solutions to the RR $a_{n}=f(n)a_{n-1}+g(n)$, then $(h_{n})_{n \in \mathbb{N}}$ defined as::$$h_{n}=p_{n}-q_{n}$$is a solution to the homogenous RR $$a_{n}=f(n)a_{n-1}$$
<!--SR:!2025-05-22,26,230-->

- Let $a_{n}=f(n)a_{n-1}+g(n)=h_{n}+p_{n}$, if $g(n)$ is a polynomial of degree $d$. Guess $p_{n}=$::$A_{0}+A_{1}n+\dots +A_{d}n^{d}$.
<!--SR:!2025-05-25,29,230-->
- Let $a_{n}=f(n)a_{n-1}+g(n)=h_{n}+p_{n}$, if $g(n)$ is an exponential with base $b$. Guess $p_{n}=$::$C\cdot b^{n}$.
<!--SR:!2025-05-27,31,230-->
- Let $a_{n}=f(n)a_{n-1}+g(n)=h_{n}+p_{n}$, if $g(n)$ is a sum/product of polynomial of degree $d$ and exponential with base $b$. Guess $p_{n}=$:: sum/product of them.
<!--SR:!2025-05-01,21,250-->


## Higher order recurrence relations

A linear recurrence relation of order $k$ is of the form:: $$a_{n}=f_{1}(n)a_{n-1}+f_{2}a_{n-2}+\dots +f_{k}(n)a_{n-k}+g(n)$$ with $k$ base cases: $$a_{0},a_{1},\dots ,a_{k-1}$$ that determines a unique sequence.
<!--SR:!2025-04-27,1,182-->

The set of solutions to a linear, homogenous, recurrence relation of order 2 is:: a vector subspace of dimension 2.
<!--SR:!2025-04-27,1,202-->