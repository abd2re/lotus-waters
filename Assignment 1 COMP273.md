Winter 2025
Abdoul Wahab Toure
261227818

## 1 Number Representation, 2s Complement, and Floating Point

(1) *Convert positional notation $0.101011_{2}$ from binary to decimal using any appropriate algorithm that was seen in class.*
$$0.101011_{2}=0\times 2^{0}+1 \times 2^{-1}+0\times 2^{-2}+1\times 2^{-3}+0\times 2^{-4}+1\times 2^{-5}+1\times 2^{-6}$$
$$0.101011_{2}=0.671875_{10}$$
(2) *Convert positional notation $6.7510$ from decimal to binary and hexadecimal using algorithms that were seen in class.*
Decimal $\rightarrow$ Binary
$$6_{10} = 110_{2}$$
$$0.75 \times 2=1.5 \rightarrow 1$$
$$0.5 \times 2=1.0 \rightarrow 1$$
$$0.75_{10}=0.11_{2}$$
$$6.75_{10}=110.11_{2}$$
Binary $\rightarrow$ Hexadecimal
$$110.11_{2}\equiv0110.1100_{2}$$
$$0110.1100_{2}=6.C_{16}$$

Binary: $110.11_{2}$, Hexadecimal: $6.C_{16}$

(3) *Convert positional notation $1FA.U06G_{32}$ from base 32 to binary and then to hexadecimal.*
Base 32 $\rightarrow$ Binary
$$1FA_{32}=00001~01111~01010_{2}$$
$$1FA_{32}=10111101010_{2}$$
$$U06G_{32}=11110~00000~00110~10000_{2}$$
$$U06G_{32}=11110000000011010000_{2}$$
$$1FA.U06G_{32}=10111101010.11110000000011010000_{2}$$
Binary $\rightarrow$ Hexadecimal
$$10111101010.11110000000011010000_{2}\equiv0101~1110~1010.1111~0000~0000~1101~0000_{2}$$
$$0101~1110~1010.1111~0000~0000~1101~0000_{2}=5EA.F00D0_{16}=5EA.F00D_{16}$$
Binary: $10111101010.11110000000011010000_{2}$, Hexadecimal: $5EA.F00D_{16}$

(4) *Convert the base 5 number $3031004_5$ to hexadecimal.*
Base 5 $\rightarrow$ Decimal
$$3031004_{5}=3 \cdot 5^6 + 0 \cdot 5^5 + 3 \cdot 5^4 + 1 \cdot 5^3 + 0 \cdot 5^2 + 0 \cdot 5^1 + 4 \cdot 5^0$$
$$3031004_{5}=46875 + 0 + 1875 + 125 + 0 + 0 + 4$$
$$3031004_{5}=48879_{10}$$

Decimal $\rightarrow$ Hexadecimal
$$(48879)/16=3054\rightarrow F$$
$$(3054)/16=190\rightarrow E$$
$$(190)/16=11\rightarrow E$$
$$(11)/16=0\rightarrow B$$
$$48879_{10}=BEEF_{16}$$

(5) *Represent the base 10 number $−4128786_{10}$ as a 24 bit signed binary number using two’s complement format. Convert the binary bit pattern in your answer to hexadecimal using 6 symbols.*

Convert $4128786_{10}$ to binary
$$(4128786)/2 = 2064393 \rightarrow 0$$
$$(2064393)/2 = 1032196 \rightarrow 1$$
$$(1032196)/2 = 516098 \rightarrow 0$$
$$(516098)/2 = 258049 \rightarrow 0$$
$$(258049)/2 = 129024 \rightarrow 1$$
$$(129024)/2 = 64512 \rightarrow 0$$
$$(64512)/2 = 32256 \rightarrow 0$$
$$(32256)/2 = 16128 \rightarrow 0$$
$$(16128)/2 = 8064 \rightarrow 0$$
$$(8064)/2 = 4032 \rightarrow 0$$
$$(4032)/2 = 2016 \rightarrow 0$$
$$(2016)/2 = 1008 \rightarrow 0$$
$$(1008)/2 = 504 \rightarrow 0$$
$$(504)/2 = 252 \rightarrow 0$$
$$(252)/2 = 126 \rightarrow 0$$
$$(126)/2 = 63 \rightarrow 0$$
$$(63)/2 = 31 \rightarrow 1$$
$$(31)/2 = 15 \rightarrow 1$$
$$(15)/2 = 7 \rightarrow 1$$
$$(7)/2 = 3 \rightarrow 1$$
$$(3)/2 = 1 \rightarrow 1$$
$$(1)/2 = 0 \rightarrow 1$$

$$4128786_{10}=001111110000000000010010_{2}$$
Invert the bits
$$\rightarrow 110000001111111111101101_{2}$$
Add $1$
$$\rightarrow 110000001111111111101101+1=110000001111111111101110_{2}$$

Binary $\rightarrow$ Hexadecimal
$$1100~0000~1111~1111~1110~1110_{2}=C0FFEE_{16}$$

(6) *Represent $-2.625$ as an IEEE single precision floating point number. Give your answer in both binary and hexadecimal and show your work. Is the representation exact?*

Convert $-2.625$ to scientific notation
$$-2.625 \times 10^{0}$$
Transform the power of $10$ into a power of $2$
$$-2.625 \times 2^{0}$$

Convert the numeral part into binary
$$2_{10}=10_{2}$$
$$0.625 \times 2=1.25 \rightarrow 1$$
$$0.25 \times 2=0.5 \rightarrow 0$$
$$0.5 \times 2=1.0 \rightarrow 1$$
$$2.625_{10}=10.101_{2}$$

Normalize it
$$-2.625_{10}=-1.0101_{2} \times 2^{1}$$
$$\text{sign bit}\rightarrow 1$$
$$\text{exponent}\rightarrow 1+127=128_{10}=10000000$$
$$\text{fractional part}\rightarrow 01010000000000000000000$$
Result in binary
$$1~10000000~01010000000000000000000_{2}$$

Binary $\rightarrow$ Hexadecimal
$$1100~0000~0010~1000~0000~0000~0000~0000_{2}=C0280000_{16}$$

Binary: $1~10000000~01010000000000000000000_{2}$, Hexadecimal: $C0280000_{16}$

---
```



```
## 2 Seven Segment Decoder

(1) *Write out a truth table for your circuit and include this with your written answers.*

My student ID: 261227818

| A3  | A2  | A1  | A0  | S6  | S5  | S4  | S3  | S2  | S1  | S0  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 0   | 0   | 0   | 0   | 0   | 1   | 1   | 1   | 1   | 0   | 1   |
| 0   | 0   | 0   | 1   | 1   | 1   | 1   | 0   | 1   | 1   | 1   |
| 0   | 0   | 1   | 0   | 1   | 0   | 0   | 1   | 0   | 0   | 0   |
| 0   | 0   | 1   | 1   | 0   | 1   | 1   | 1   | 1   | 0   | 1   |
| 0   | 1   | 0   | 0   | 0   | 1   | 1   | 1   | 1   | 0   | 1   |
| 0   | 1   | 0   | 1   | 1   | 0   | 0   | 1   | 1   | 0   | 0   |
| 0   | 1   | 1   | 0   | 1   | 1   | 1   | 1   | 1   | 1   | 1   |
| 0   | 1   | 1   | 1   | 1   | 0   | 0   | 1   | 0   | 0   | 0   |
| 1   | 0   | 0   | 0   | 1   | 1   | 1   | 1   | 1   | 1   | 1   |
| 1   | 0   | 0   | 1   | x   | x   | x   | x   | x   | x   | x   |
| 1   | 0   | 1   | 0   | x   | x   | x   | x   | x   | x   | x   |
| 1   | 0   | 1   | 1   | x   | x   | x   | x   | x   | x   | x   |
| 1   | 1   | 0   | 0   | x   | x   | x   | x   | x   | x   | x   |
| 1   | 1   | 0   | 1   | x   | x   | x   | x   | x   | x   | x   |
| 1   | 1   | 1   | 0   | x   | x   | x   | x   | x   | x   | x   |
| 1   | 1   | 1   | 1   | x   | x   | x   | x   | x   | x   | x   |

