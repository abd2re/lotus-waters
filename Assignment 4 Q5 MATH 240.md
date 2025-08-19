# Q5

(a)
Encryption in RSA is
$$
\hat{M} = M^k \bmod n = 9^7 \bmod 209
$$
We can compute $9^7 \bmod 209$ step by step:

1. $9^2 = 81 \equiv 81\bmod{209}.$  
2. $9^3 = 81 \times 9 = 729 \equiv 102\bmod{209}$ (since $729 - 3\times 209=729-627=102$).  
3. $9^4 = 102 \times 9=918 \equiv 82\bmod{209}$.  
4. $9^5 = 82 \times 9=738 \equiv 111\bmod{209}$.  
5. $9^6 = 111 \times 9=999 \equiv 163\bmod{209}$.  
6. $9^7 = 163 \times 9=1467 \equiv 4\bmod{209}$.  

Hence 
$$
\hat{M} = 4
$$



(b)

We need $s$ such that  
$$
7s \equiv 1 \bmod{180}.
$$
Equivalently, we want integers $s$ and $t$ satisfying  
$$
7s -180t =1.
$$

1.  $180 = 7\times 25 + 5$  
2.  $7 = 5 \times 1 + 2$  
3.  $5 = 2 \times 2 + 1$  
4.  $2 = 1 \times 2 + 0$

So $\gcd(7, 180) = 1$ Now back‐substitute to express 1 as a combination of 7 and 180:

1. From step (3):  
   $$
   1 = 5 - 2\times 2.
   $$
2. But from step (2), $2 = 7 - 5$. Substituting yields:  
   $$
   1 = 5 - 2(7 - 5)
         = 5 - 2\cdot7 + 2\cdot5
         = 3\cdot5 - 2\cdot7.
   $$
3. From step (1), $5=180 - 7\times 25$. Substituting:  
   $$
   1 = 3(180 - 25\cdot7)-2\cdot7 
         = 3\cdot180 - 75\cdot7 - 2\cdot7 
         = 3\cdot180 - 77\cdot7.
   $$
Hence 
$$
1 = 3\cdot180 - 77\cdot7 \implies
7(-77) - 180(-3) =1.
$$
Thus one valid solution is $s = -77$.  Since we want $s$ modulo 180, observe that 
$$
-77 \equiv 180 - 77=103 \bmod{180}.
$$
So 
$$
s = 103
$$

(c)

The decryption formula is
$$
M =\hat{M}^{s}\bmod n
=4^{103} \bmod 209.
$$

1.  We compute powers of 4 by squaring (all modulo 209):
   - $4^1 = 4$.  
   - $4^2 = 16$  
   - $4^4 = (4^2)^2 = 16^2 = 256 \equiv 47 \bmod{209}$.  
   - $4^8 = 47^2 = 2209 \equiv 119 \bmod{209}$.  
   - $4^{16} = 119^2 = 14161 \equiv 158 \bmod{209}$.  
   - $4^{32} = 158^2 = 24964 \equiv 93 \bmod{209}$.  
   - $4^{64} = 93^2 = 8649 \equiv 80 \bmod{209}$.

2.  Next, express $103$ in binary or as a sum of powers of 2:
   $$
   103 = 64 + 32 + 6 + 1.
   $$
   Hence
   $$
   4^{103} =4^{64}\cdot4^{32}\cdot4^6\cdot4^1.
   $$

3.  We already have $4^{64}=80$ and $4^{32}=93$. Also,
   - $4^6 = (4^3)^2$.  Directly:  
     $4^2=16,4^3=64,4^6=64^2=4096$  
     Mod 209, $4096 \equiv 125$. 
   - $4^1 = 4$

4.  Multiply everything mod 209:
   $$
   4^{103} 
      = 80 \times 93 \times 125 \times 4 \bmod 209.
   $$
   -  $80 \times 93 = 7440 \equiv 125\bmod{209}$ 
   -  $125 \times 125 = 15625 \equiv 159\bmod{209}$  
   -  $159 \times 4 = 636 \equiv 9 \bmod{209}$

Therefore,
$$
4^{103} \equiv 9 \bmod{209}.
$$
This means the decrypted message is
$$
M = 9
$$