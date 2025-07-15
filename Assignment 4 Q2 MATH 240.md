# Q2

(a) 
To show that $\sim$ is an equivalence relation on $F$:  
- Reflexivity: For any $\frac{a}{b} \in F$, $ab = ba$, so $\frac{a}{b} \sim \frac{a}{b}$.  
- Symmetry: If $\frac{a}{b} \sim \frac{c}{d}$, then $ad = bc$. This implies $cb = da$, so $\frac{c}{d} \sim \frac{a}{b}$.  
- Transitivity: If $\frac{a}{b} \sim \frac{c}{d}$ and $\frac{c}{d} \sim \frac{e}{f}$, then $ad = bc$ and $cf = de$. Multiplying these equations: $(ad)(cf) = (bc)(de)$. Canceling $c$ and $d$ (since $c, d \neq 0$), we get $af = be$, so $\frac{a}{b} \sim \frac{e}{f}$.  

Thus, $\sim$ satisfies reflexivity, symmetry, and transitivity, making it an equivalence relation.  


(b) 
Every $\frac{a}{b} \in F$ is equivalent to a reduced fraction $\frac{x}{y}$ with $y > 0$ and $\gcd(x, y) = 1$:  
1. We adjust the sign of the denominator: Let $y = |b|$ and $x = a \cdot \frac{b}{|b|}$. This ensures $y > 0$.  
2. We reduce the fraction: Let $d = \gcd(x, y)$. Define $x' = \frac{x}{d}$ and $y' = \frac{y}{d}$. By construction, $\gcd(x', y') = 1$.  
3. Equivalence:  
   - $\frac{a}{b} \sim \frac{x}{y}$ because $a \cdot y = b \cdot x$.  
   - $\frac{x}{y} \sim \frac{x'}{y'}$ because $x \cdot y' = y \cdot x'$.  
   By transitivity, $\frac{a}{b} \sim \frac{x'}{y'}$.  

Hence, $\frac{x'}{y'}$ is the desired reduced fraction. 