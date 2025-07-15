## Q1

(a)
We prove the contrapositive: If $\sqrt[3]{x}$ is rational, then $x$ is rational.  

Assume $\sqrt[3]{x}$ is rational. Then, $\sqrt[3]{x} = \frac{a}{b}$ for integers $a, b$ ($b \neq 0$) with $\gcd(a, b) = 1$. Cubing both sides:  
$$
x = \left(\frac{a}{b}\right)^3 = \frac{a^3}{b^3}.
$$  
Since $a^3$ and $b^3$ are integers, $x$ is a ratio of two integers, hence rational. Thus, the contrapositive holds, proving that if $x$ is irrational, $\sqrt[3]{x}$ is irrational.  

(b)
Assume $\log_2 5$ is rational. Then, $\log_2 5 = \frac{p}{q}$ for integers $p, q$ ($q \neq 0$). Rewriting in exponential form:  
$$
2^{p/q} = 5 \implies 2^p = 5^q.
$$  
The left side $2^p$ is a power of 2, and the right side $5^q$ is a power of 5. By the uniqueness of prime factorization, $2^p \neq 5^q$ unless $p = q = 0$. However, $q = 0$ is invalid in $\frac{p}{q}$. This contradiction implies $\log_2 5$ is irrational.