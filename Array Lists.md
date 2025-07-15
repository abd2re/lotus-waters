---
tags:
  - COMP250
---
# Array Lists

- How many times $k$ do we need to double the length of the array so that it is of length $N$ ?::$$2\times2\times\dots\times2=2^{k}=N\rightarrow k=\log_{2}N$$
<!--SR:!2024-11-30,19,190-->
- How many copy operations are required to add $N$ elements to an empty array list ?::$$1+2+\dots+2^{n-1}=\frac{1-2^{k}}{1-2}=2^{k}-1=N-1$$
<!--SR:!2024-12-16,26,170-->