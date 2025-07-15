---
tags:
  - COMP273
---
# MIPS arithmetic

- Assembly cannot:: use arbitrary variables.
<!--SR:!2025-06-03,66,230-->
- Assembly operands are:: registers. Since registers are directly in hardware, they are very fast. Drawback: : Since registers are in hardware, there are a predetermined number of them.
<!--SR:!2025-06-09,70,230-->

MIPS has how many registers?::32. Each MIPS register is 32 bits wide (word). Registers are numbered from 0 to 31 ($0, $1, $2, … $30, $31).
<!--SR:!2025-04-24,47,250-->


## Addition and Subtraction

Addition and Subtraction
?
![[Pasted image 20250205180352.png]] ![[Pasted image 20250205180447.png]]
<!--SR:!2025-04-17,42,250-->

Immediates (addition and subtraction)
?
![[Pasted image 20250205180850.png]]
<!--SR:!2025-04-17,38,230-->

Register zero (applications)
?
![[Pasted image 20250205180934.png]] ![[Pasted image 20250205180949.png]]
<!--SR:!2025-04-16,42,250-->

## Data Transfer Instructions

Use Data transfer instructions to:: transfer data between registers and memory. We need to specify – Register: specify this by number (0 - 31) – Memory address: more difficult.
<!--SR:!2025-06-09,71,230-->

Memory Address
?
![[Pasted image 20250205181626.png]]
<!--SR:!2025-04-19,31,190-->

Data Transfer: Memory to Register
?
![[Pasted image 20250205182449.png]]![[Pasted image 20250205182456.png]]
![[Pasted image 20250205182744.png]]
![[Pasted image 20250205183012.png]]
lb for byte instead of word, lbu for unsigned byte
<!--SR:!2025-06-15,64,210-->


<!--SR:!2025-02-12,1,220-->