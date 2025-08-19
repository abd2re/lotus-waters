## Q4

(a)
($\Longrightarrow$) Assume $n$ is a perfect square. Then $n = m^2$ for some integer $m$. Let the prime factorization of $m$ be $m = p_1^{b_1}p_2^{b_2}\cdots p_k^{b_k}$. Squaring $m$:  
$$
n = m^2 = \left(p_1^{b_1}p_2^{b_2}\cdots p_k^{b_k}\right)^2 = p_1^{2b_1}p_2^{2b_2}\cdots p_k^{2b_k}.
$$ 
All exponents $2b_i$ are even.  

($\Longleftarrow$) Assume $n$ has prime factorization $n = p_1^{a_1}p_2^{a_2}\cdots p_k^{a_k}$ with all $a_i$ even. Write $a_i = 2b_i$. Then:  
$$
n = p_1^{2b_1}p_2^{2b_2}\cdots p_k^{2b_k} = \left(p_1^{b_1}p_2^{b_2}\cdots p_k^{b_k}\right)^2.
$$ 
Thus, $n$ is a perfect square.  

(b)
($\Longrightarrow$) If $n$ is a perfect square, $n = m^2$ for some integer $m$. Then $\sqrt{n} = m$, which is an integer and hence rational.  

($\Longleftarrow$) Assume $\sqrt{n}$ is rational. Then $\sqrt{n} = \frac{p}{q}$, where $p, q \in \mathbb{Z}$, $q \neq 0$, and $\gcd(p, q) = 1$. Squaring both sides:  
$$
n = \frac{p^2}{q^2} \implies n q^2 = p^2.
$$ 
In prime factorization, $p^2$ and $q^2$ have all even exponents. Since $\gcd(p, q) = 1$, $p^2$ and $q^2$ share no common primes. Thus, $n$ must absorb all primes in $q^2$, implying $n$ has even exponents in its prime factors (as $n q^2 = p^2$ must have even exponents). By part (a), $n$ is a perfect square.  