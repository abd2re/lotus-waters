# Q3

(a)  
($\implies$) Suppose $\lambda$ is an eigenvalue of $T$. Then there exists a non-zero $v \in V$ such that $Tv = \lambda v$. Applying $T^{-1}$ to both sides:  
$$
v = \lambda T^{-1}v \implies T^{-1}v = \lambda^{-1}v.
$$  
Thus, $\lambda^{-1}$ is an eigenvalue of $T^{-1}$.  

($\impliedby$) Conversely, if $\lambda^{-1}$ is an eigenvalue of $T^{-1}$, there exists a non-zero $w \in V$ such that $T^{-1}w = \lambda^{-1}w$. Applying $T$ to both sides:  
$$
w = \lambda^{-1}Tw \implies Tw = \lambda w.
$$  
Hence, $\lambda$ is an eigenvalue of $T$.  

(b)  
We use induction on $n$.  

- Base case ($n=1$): Trivial, as $T^1 = T$ and $\lambda^1 = \lambda$.  

- Inductive step: Assume $T^k v = \lambda^k v$ for some $k \geq 1$. Then:  
$$
T^{k+1}v = T(T^k v) = T(\lambda^k v) = \lambda^k (Tv) = \lambda^k (\lambda v) = \lambda^{k+1}v.
$$  
By induction, $\lambda^n$ is an eigenvalue of $T^n$ for all $n \geq 1$.  