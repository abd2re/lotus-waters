Let's work through these step by step:

---

### **1. Convert 0.10101120.101011_2 to decimal**

The value is calculated as:

0.1010112=1⋅2−1+0⋅2−2+1⋅2−3+0⋅2−4+1⋅2−5+1⋅2−60.101011_2 = 1 \cdot 2^{-1} + 0 \cdot 2^{-2} + 1 \cdot 2^{-3} + 0 \cdot 2^{-4} + 1 \cdot 2^{-5} + 1 \cdot 2^{-6} =0.5+0+0.125+0+0.03125+0.015625=0.671875= 0.5 + 0 + 0.125 + 0 + 0.03125 + 0.015625 = 0.671875

**Answer:** 0.6718750.671875

---

### **2. Convert 6.75106.75_{10} to binary and hexadecimal**

#### Binary:

- Convert the integer part 6106_{10}:
    
    610→11026_{10} \rightarrow 110_2
- Convert the fractional part 0.75100.75_{10}:
    
    0.75×2=1.5(take 1)0.75 \times 2 = 1.5 \quad (take\ 1) 0.5×2=1.0(take 1)0.5 \times 2 = 1.0 \quad (take\ 1)

So, 0.7510=0.1120.75_{10} = 0.11_2.

Combining both parts: 6.7510=110.1126.75_{10} = 110.11_2.

#### Hexadecimal:

Group the binary representation into 4-bit chunks:

110.112=00000110.11002110.11_2 = 00000110.1100_2

Convert each group to hex:

00000110.11002=6.C1600000110.1100_2 = 6.C_{16}

**Answer: Binary:** 110.112110.11_2, **Hexadecimal:** 6.C166.C_{16}

---

### **3. Convert 1FA.U06G321FA.U06G_{32} to binary and hexadecimal**

#### Binary:

- Convert 1FA321FA_{32} to binary: Each base-32 digit converts to 5 bits:
    
    1=00001,F=01111,A=101001 = 00001, \quad F = 01111, \quad A = 10100 1FA32=00001 01111 1010021FA_{32} = 00001\ 01111\ 10100_2
- Convert U06G32U06G_{32} to binary:
    
    U=10100,0=00000,6=00110,G=00111U = 10100, \quad 0 = 00000, \quad 6 = 00110, \quad G = 00111 U06G32=10100 00000 00110 001112U06G_{32} = 10100\ 00000\ 00110\ 00111_2

Combining: 1FA.U06G32=00001 01111 10100.10100 00000 00110 0011121FA.U06G_{32} = 00001\ 01111\ 10100.10100\ 00000\ 00110\ 00111_2.

#### Hexadecimal:

Group the binary into 4-bit chunks:

0000 1011 1110 1010.1010 0000 0001 1000 011120000\ 1011\ 1110\ 1010.1010\ 0000\ 0001\ 1000\ 0111_2

Convert to hex:

0BEA.A087160BEA.A087_{16}

**Answer:** Binary: 00001 01111 10100.10100 00000 00110 00111200001\ 01111\ 10100.10100\ 00000\ 00110\ 00111_2, **Hexadecimal:** 0BEA.A087160BEA.A087_{16}

---

### **4. Convert 303100453031004_5 to hexadecimal**

#### Decimal:

Expand 303100453031004_5:

30310045=3⋅56+0⋅55+3⋅54+1⋅53+0⋅52+0⋅51+4⋅503031004_5 = 3 \cdot 5^6 + 0 \cdot 5^5 + 3 \cdot 5^4 + 1 \cdot 5^3 + 0 \cdot 5^2 + 0 \cdot 5^1 + 4 \cdot 5^0 =3⋅15625+0⋅3125+3⋅625+1⋅125+0⋅25+0⋅5+4= 3 \cdot 15625 + 0 \cdot 3125 + 3 \cdot 625 + 1 \cdot 125 + 0 \cdot 25 + 0 \cdot 5 + 4 =46875+0+1875+125+0+0+4=48879= 46875 + 0 + 1875 + 125 + 0 + 0 + 4 = 48879

#### Hexadecimal:

Convert 488791048879_{10} to hexadecimal:

4887910=BEFF1648879_{10} = BEFF_{16}

**Answer:** BEFF16BEFF_{16}

---

### **5. Represent −412878610-4128786_{10} in 24-bit two’s complement and convert to hex**

#### Binary:

Convert 4128786104128786_{10} to binary (24 bits):

412878610=001111 110111 011000 00100024128786_{10} = 001111\ 110111\ 011000\ 001000_2

Invert bits for two’s complement:

110000 001000 100111 1101112110000\ 001000\ 100111\ 110111_2

Add 1:

110000 001000 101000 0000002110000\ 001000\ 101000\ 000000_2

#### Hexadecimal:

Group into 4-bit chunks and convert:

110000 001000 101000 0000002=C28A0016110000\ 001000\ 101000\ 000000_2 = C28A00_{16}

**Answer:** Binary: 110000 001000 101000 0000002110000\ 001000\ 101000\ 000000_2, **Hexadecimal:** C28A0016C28A00_{16}

---

### **6. Represent −2.625-2.625 as IEEE single-precision**

#### Binary representation of 2.625102.625_{10}:

- Integer part 2102_{10}:
    
    210=1022_{10} = 10_2
- Fractional part 0.625100.625_{10}:
    
    0.625×2=1.25(take 1)0.625 \times 2 = 1.25 \quad (take\ 1) 0.25×2=0.5(take 0)0.25 \times 2 = 0.5 \quad (take\ 0) 0.5×2=1.0(take 1)0.5 \times 2 = 1.0 \quad (take\ 1)

So, 2.62510=10.10122.625_{10} = 10.101_2.

#### IEEE format:

1. Normalize:
    
    2.62510=1.01012×212.625_{10} = 1.0101_2 \times 2^1
2. Sign bit:
    
    Negative→1Negative \rightarrow 1
3. Exponent:
    
    Bias=127,1+127=128→100000002Bias = 127, \quad 1 + 127 = 128 \quad \rightarrow 10000000_2
4. Mantissa:
    
    0101000000000000000000001010000000000000000000

Combining:

1 10000000 0101000000000000000000021\ 10000000\ 01010000000000000000000_2

#### Hexadecimal:

Convert to hex:

11000000 01010000 00000000 000000002=C15000001611000000\ 01010000\ 00000000\ 00000000_2 = C1500000_{16}

**Answer:** Binary: 1 10000000 01010000 00000000 0000000021\ 10000000\ 01010000\ 00000000\ 00000000_2, **Hexadecimal:** C150000016C1500000_{16}

---

Let me know if you'd like any part explained further!