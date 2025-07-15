# Q3

We use the Euclidean algorithm:

1. $421 = 2\times148 + 125$
2. $148 = 1\times125 + 23$
3. $125 = 5\times23 + 10$
4. $23 = 2\times10 + 3$
5. $10 = 3\times3 + 1$
6. $3 = 3\times1 + 0$

So $\gcd(148,421) = 1$. Because they are coprime, an inverse exists.

We backtrack to express $1$ as a combination of $148$ and $421$.

- From step (5): 
  $$
  1 = 10 - 3\times3
  $$
- But from step (4), $3 = 23 - 2\times10$. Substitute:
  $$
  1 = 10 - 3(23 - 2\times10)
          = 7\times10 - 3\times23
  $$
- From step (3), $10 = 125 - 5\times23$. Substitute:
  $$
  1 = 7(125 - 5\times23) - 3\times23
          = 7\times125 - 38\times23
  $$
- From step (2), $23 = 148 - 125$. Substitute:
  $$
  1 = 7\times125 - 38(148 - 125)
          = 45\times125 - 38\times148
  $$
- From step (1), $125 = 421 - 2\times148$. Substitute:
  $$
  1 = 45(421 - 2\times148) - 38\times148 
          = 45\times421 - 128\times148
  $$

Hence,
$$
1 \equiv -128 \times 148 \bmod{421}.
$$
That is, 
$$
-128 \cdot 148 \equiv 1 \bmod{421}
$$
Since $-128 \equiv 293 \bmod{421}$ (because $293 = 421 - 128$), we obtain
$$
293 \cdot 148 \equiv 1 \bmod{421}
$$
Thus, 
$$
148^{-1} \equiv 293 \bmod{421}
$$

Returning to the original equation,
$$
148x \equiv 12 \bmod{421} 
\quad\Longrightarrow\quad
x \equiv 12 \times (148^{-1}) 
       \equiv 12 \times 293 \bmod{421}
$$
Compute $12 \times 293 = 3516$. We reduce $3516 \bmod 421$:

$$
3516 \div 421 = 8
$$
and the remainder is $3516 - 3368 = 148$. Therefore,
$$
x \equiv 148 \bmod{421}
$$

Hence
$$
x = 148
$$