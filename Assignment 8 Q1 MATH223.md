# Q1

(a)
Assume $W_1 \subseteq W_2$. Let $x \in W_2^\perp$. By definition, $\langle x, w \rangle = 0$ for all $w \in W_2$. Since $W_1 \subseteq W_2$, every $w_1 \in W_1$ is also in $W_2$. Thus, $\langle x, w_1 \rangle = 0$ for all $w_1 \in W_1$, which implies $x \in W_1^\perp$. Hence, $W_2^\perp \subseteq W_1^\perp$, proving $W_2^\perp \leq W_1^\perp$.


(b)
We show both inclusions:  
1. **$(W_1 + W_2)^\perp \subseteq W_1^\perp \cap W_2^\perp$:**  
   Let $x \in (W_1 + W_2)^\perp$. Then $\langle x, w_1 + w_2 \rangle = 0$ for all $w_1 \in W_1, w_2 \in W_2$.  
   - Set $w_2 = 0$: $\langle x, w_1 \rangle = 0$ for all $w_1 \in W_1$, so $x \in W_1^\perp$.  
   - Set $w_1 = 0$: $\langle x, w_2 \rangle = 0$ for all $w_2 \in W_2$, so $x \in W_2^\perp$.  
   Hence, $x \in W_1^\perp \cap W_2^\perp$.  

2. **$W_1^\perp \cap W_2^\perp \subseteq (W_1 + W_2)^\perp$:**  
   Let $x \in W_1^\perp \cap W_2^\perp$. Then $\langle x, w_1 \rangle = 0$ and $\langle x, w_2 \rangle = 0$ for all $w_1 \in W_1, w_2 \in W_2$. For any $v = w_1 + w_2 \in W_1 + W_2$:  
   $$
   \langle x, v \rangle = \langle x, w_1 + w_2 \rangle = \langle x, w_1 \rangle + \langle x, w_2 \rangle = 0 + 0 = 0.
   $$  
   Thus, $x \in (W_1 + W_2)^\perp$.  

Both inclusions hold, so $(W_1 + W_2)^\perp = W_1^\perp \cap W_2^\perp$.  