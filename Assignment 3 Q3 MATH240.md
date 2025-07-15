## Q3

(a) 
Let $s = \gcd(b, c)$. Let $d = \gcd(a, b, c)$.  
- $d$ divides $a, b, c$, so $d \mid \gcd(b, c) = s$. Hence, $d \mid \gcd(a, s)$.  
- Conversely, let $e = \gcd(a, s)$. Since $e \mid a$ and $e \mid s$, $s \mid b$, and $s \mid c$, $e$ divides $a, b, c$. Thus, $e \mid d \implies \gcd(a,s)\mid d$.  

Therefore, $d = e$, so $\gcd(a, b, c) = \gcd(a, s)$.  

(b)
By part (a), $\gcd(a, b, c) = \gcd(a, s)$ where $s = \gcd(b, c)$.  
- We know that $s = bv + cw$ for some integers $v, w$.  
- Also, $\gcd(a, s) = au + st$ for integers $u, t$.  
Substitute $s$:  
$$
\gcd(a, s) = au + (bv + cw)t = au + b(vt) + c(wt).
$$  
Let $u' = u$, $v' = vt$, $w' = wt$. Hence, $\gcd(a, b, c) = au' + bv' + cw'$.  