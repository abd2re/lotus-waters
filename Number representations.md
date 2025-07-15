---
tags:
  - COMP273
---
# Number representations

## Bits, Bytes, and Words
- a byte is:: a group of 8 bits
<!--SR:!2025-07-25,132,290-->
- a nibble/nybble (a small bite) is:: a group of 4 bits
<!--SR:!2025-07-29,135,290-->
- a word (MIPS) is:: a group of 4 bytes, or 32 bits
<!--SR:!2025-07-21,130,290-->

What is the largest decimal number with $n$ digits?:: $10^{n}-1$
<!--SR:!2025-07-13,124,290-->
What is the largest binary number with $m$ digits?:: $2^{m}-1$
<!--SR:!2025-06-30,115,290-->
## Number bases and base conversion

Base conversion for integers, decimal to base $b$ steps:
?
- Divide by $b$
- Remainder of result is least significant bit
- Repeat with the quotient, stop when quotient is zero
<!--SR:!2025-06-08,89,258-->

Base conversion, Base $b$ to decimal steps:
?
$N=a_{n}b^{n}+a_{n-1}b^{n-1}+\dots +a_{1}b+a_{0}$
<!--SR:!2025-05-15,80,278-->

Conversion from base $𝑎$ to base $𝑏$
?
- First convert base $𝑎$ to decimal
- Then convert decimal to base $𝑏$
(for hexadecimal-binary or octal-binary, use groups of 4 or 3)
<!--SR:!2025-09-03,143,258-->


## Binary arithmetic and data representation

How to Represent Signed Numbers?
?
Two’s complement – Invert bits and add one where 1 is negative and 0 is positive.
<!--SR:!2025-06-03,94,278-->

- $𝑛$-bit negative numbers are defined as $\text{NEGATIVE}(N)=$::$2^{n}-N$. (same as inverting bits adding one).
<!--SR:!2025-04-30,59,238-->
- Two's complement technique that is easily implement hardware ranges for $n$ bits from:: $-2^{n-1}$ to $2^{n-1}-1$.
<!--SR:!2025-08-01,124,258-->

Arithmetic overflow can occur during:: two's complement addition (both positive or both negative).
<!--SR:!2025-08-13,132,258-->

Can overflow happen when adding positive and negative numbers?:: No, because the answer will be in the range.
<!--SR:!2025-05-18,82,278-->

Packed decimal (Binary Coded Decimal, BCD) is when:: we replace each digit of a decimal number, with its 4-bit equivalent, user friendly but wastes storage, cannot be signed and hard to implement.
<!--SR:!2025-05-31,91,278-->

Parity is used to:: check for corrupt data in storage or transmission, with two kinds: even and odd.
<!--SR:!2025-07-27,111,238-->