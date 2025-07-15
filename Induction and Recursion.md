---
tags:
  - COMP250
---

# Induction and Recursion

The steps in mathematical induction involve proving a statement for all natural numbers (or sometimes for integers from a specific starting point onward). Here's a concise outline:
?
1. **Base Case**: Prove that the statement holds for the initial value, usually $n = 1$. This establishes the starting point of the induction.
2. **Inductive Hypothesis**: Assume the statement is true for an arbitrary integer $n = k$. This assumption is not proven but is used to bridge the gap to the next step.
3. **Inductive Step**: Use the inductive hypothesis (i.e., assume the statement is true for $n = k$) to prove that the statement holds for $n = k + 1$. This shows that if the statement is true for $k$, it must also be true for $k + 1$.
4. **Conclusion**: By proving the base case and the inductive step, you conclude that the statement holds for all natural numbers (or integers) from the starting point onward, due to the principle of mathematical induction.
<!--SR:!2024-11-30,19,250-->

