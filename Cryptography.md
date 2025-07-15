---
tags:
  - MATH240
---

# Cryptography (RSA)

RSA protocol
?
1. Key generation (Bob)
   Bob chooses two distinct, large prime numbers $p$ and $q$.
   Let $n=pq$. Find a number $k$ which is coprime with $(p-1)(q-1)$ i.e. $\gcd(k,(p-1)(q-1))=1$.
   Let $s \equiv k^{-1} \bmod (p-1)(q-1)$.
   $s$ is the private key (secret).
   $(n,k)$ is the public key (tell everyone).
2. Encryption (Alice)
   Original message: $M=\text{Some number between }0 \text{ and }n-1$. (if not slice into chunks and send several messages)
   Encrypted message: $\hat{M}=M^{k}\%n$.
3. Decryption (Bob)
   Bob receives $\hat{M}$.
   $\rightarrow M=\hat{M}^{s}\%n$.
<!--SR:!2025-04-20,11,230-->

Let $p,q$ be primes. Then $a \equiv b \bmod pq \iff$::$a \equiv b \bmod p$ and $a \equiv b \bmod q$.
<!--SR:!2025-06-13,48,250-->

With $n=pq$, $k$ such that $\gcd(k,(p-1)(q-1))=1$ and $s=k^{-1}\bmod (p-1)(q-1)$, $\hat{M}=M^{k}\bmod n \implies M=$::$\hat{M}^{s}\bmod n$.
<!--SR:!2025-06-10,45,250-->

