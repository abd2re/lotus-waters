---
tags:
  - MATH133
---
# Systems of Linear Equations

- An augmented matrix is inconsistent (no solution) if:: the last row has all zeroes and a non-zero at the end.
<!--SR:!2025-03-19,116,250-->
- An augmented matrix has infinitely many solutions if:: the rank is less than the number of variables.
<!--SR:!2025-03-07,109,250-->
- An augmented matrix has one solution if:: the rank is equal to the number of variables
<!--SR:!2024-12-15,62,250-->

The rank of a matrix is (2):: the number of leading non-zero entries in REF form or the number of leading ones in RREF form.
<!--SR:!2024-12-27,47,230-->

A matrix is in row echelon form (REF) if it satisfies the following four properties:
?
- Rows of zeros have to be at the bottom
- Leading entries must equal 1
- As you go down, leading entries must move to the right
- Entries below leading entries must be zero
<!--SR:!2025-02-25,104,250-->

A matrix is in reduced row echelon form (RREF) if it satisfies the following two properties:
?
- It has to be in REF form
- Entries above leading entries must also be zero
<!--SR:!2025-04-27,142,250-->

Variables that are not leading ones are called:: free variables.
<!--SR:!2024-12-14,62,250-->


- A homogenous system is a system of linear equations where the constant is equal to zero.
- A homogeneous linear system may have one or infinitely many solutions. But it never has:: no solutions.
<!--SR:!2024-12-18,64,250-->
- Since there is no constant term present in the homogeneous systems, $(x_{1},x_{2},\dots,x_{n})$ = $(0, 0, \dots, 0)$ is obviously a solution to the system and is called:: the **trivial solution**
<!--SR:!2025-05-20,166,270-->


The three types of ERO are:
?
- Row swapping ($R_{i}\leftrightarrow R_{j}$)
- Row scaling ($kR_{i}$)
- Row additions ($R_{i}+kR_{j}\rightarrow R_{i}$)
<!--SR:!2025-02-13,84,250-->