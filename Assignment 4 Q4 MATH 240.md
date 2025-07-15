# Q4

We note that
$$
2409 \div 19 = 126
$$
since $126 \times 19 = 2394$,
and the remainder is $2409 - 2394 = 15$. Thus 
$$
2409 \equiv 15 \bmod{19}
$$

Hence
$$
2409^{1335} \equiv 15^{1335} \bmod{19}
$$

Since $15$ and $19$ are coprime, Fermat’s Little Theorem tells us $15^{18} \equiv 1 \bmod{19}$. So we can reduce the exponent $1335$ modulo $18$:

$$
1335 \div 18 = 74
$$
with remainder $1335 - 74 \cdot 18 = 1335 - 1332 = 3$.
Hence
$$
1335 \equiv 3 \bmod{18}
$$
Therefore,
$$
15^{1335} \equiv 15^3 \bmod{19}
$$


1. $15^2 = 225$. Reducing modulo 19:
   $$
   225 \div 19 = 11
   $$
   with remainder $225 - 19\times 11 = 225 - 209 = 16$.
   So $15^2 \equiv 16 \bmod{19}$.

2. Then $15^3 = 15^2 \times 15 \equiv 16 \times 15 = 240\bmod{19}$. Reducing 240:
   $$
   240 \div 19 = 12
   $$
   with remainder $240 - 19\times 12 = 240 - 228 = 12$.
   So $15^3 \equiv 12 \bmod{19}$.

Thus
$$
2409^{1335} \equiv 12 \bmod{19}
$$
The remainder when $2409^{1335}$ is divided by 19 is 12.