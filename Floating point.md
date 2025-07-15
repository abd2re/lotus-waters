---
tags:
  - COMP273
---
# Floating point

Number $N$ written in base $b$ positional notation consists of:: a sequence of digits and a radix point separating integer and fractional parts. $$N=a_{n}a_{n-1}\dots a_{1}a_{0}.a_{-1}a_{-2}\dots a_{-m}=\sum\limits_{i=-m}^{n}a_{i}b^{i}$$
<!--SR:!2025-05-09,75,270-->
Fixed point representation properties:
?
- Choose $n$ and $m$
- Radix point is always in the same position
- Easy to implement
- Limited range
<!--SR:!2025-05-01,85,250-->

Binary point format is:: $1.xx \dots x_{2} \times 2^{yy \dots y_{2}}$
<!--SR:!2025-05-31,81,248-->

The two representations of binary point (IEEE 754) is:
?
- single precision (32 bits)
- double precision (64 bits)
<!--SR:!2025-05-03,63,248-->

IEE 754 divides a single 32-bit word into 3 fields:
?
![[Pasted image 20250115212621.png]]
IEE 754 doesn't use 2's complement where if $S=0$ for positive and $S=1$ for negative. Numbers are in normalized scientific form.
<!--SR:!2025-08-05,126,268-->

In IEEE 754, actual representation formula is:: $(-1)^{\text{Sign}}\times (1+\text{Fraction})\times 2^{\text{Exponent}-\text{Bias}}$ where Bias = 127.
<!--SR:!2025-04-22,47,208-->

Special symbols table for IEEE 754
?
![[Pasted image 20250115220216.png]]
with bias = 127, and 0 and 255 reserved for special cases
- the maximum exponent is 127
- the minimum exponent is -126
<!--SR:!2025-04-17,11,188-->

Repartition of double precision:
?
![[Pasted image 20250115221839.png]]
<!--SR:!2025-04-29,61,248-->

Floating point addition steps:
?
- Align the radix points
    - Make the smaller number to match the larger
- Add the significands
- Normalize the result
    - What if one number is positive and the other negative?
    - May need to shift a lot!
    - Check for overflow or underflow when shifting!
- Round so number fits in available digits/bits
    - If bad luck when rounding, renormalize
<!--SR:!2025-05-15,71,248-->

Floating point multiplication  steps:
?
- Add exponents
- Multiply the significands (decimal part will be double the precision and same for whole part)
- Normalize the result (check for overflow)
- Round to fit in available digits/bits
    - Normalize again if necessary
- Compute sign of result
    - Positive if signs of operands match, negative otherwise
<!--SR:!2025-05-16,71,248-->

IEEE Has Four Rounding Modes
?
![[Pasted image 20250303140815.png]]
<!--SR:!2025-04-28,34,249-->