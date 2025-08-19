## Q2

**Base Case:** For $n = 1$:  
$$
7^1 - 3^1 = 7 - 3 = 4 \implies 4 \mid 4.
$$  
**Inductive Step:** Assume $4 \mid 7^k - 3^k$ for some $k \geq 1$. Then $7^k - 3^k = 4m$ for integer $m$. 
For $n = k+1$:  
$$
7^{k+1} - 3^{k+1} = 7 \cdot 7^k - 3 \cdot 3^k = 7(7^k - 3^k) + 4 \cdot 3^k = 7(4m) + 4 \cdot 3^k = 4(7m + 3^k).
$$  
Thus, $4 \mid 7^{k+1} - 3^{k+1}$. By induction, $4 \mid 7^n - 3^n$ for all $n \in \mathbb{N}$.  