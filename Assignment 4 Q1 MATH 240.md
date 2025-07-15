# Q1

Let's define $h$ as follows:  
$$
h(n) = 
\begin{cases} 
f\left(\frac{n}{2}\right) & \text{if } n \text{ is even}, \\
g\left(\frac{n + 1}{2}\right) & \text{if } n \text{ is odd}.
\end{cases}
$$

Proof that $h$ is a bijection:  

1. Injectivity:  
   - Suppose $h(a) = h(b)$.  
   - Case 1: Both $a$ and $b$ are even.  
     Then $f\left(\frac{a}{2}\right) = f\left(\frac{b}{2}\right)$. Since $f$ is injective, $\frac{a}{2} = \frac{b}{2} \implies a = b$.  
   - Case 2: Both $a$ and $b$ are odd.  
     Then $g\left(\frac{a + 1}{2}\right) = g\left(\frac{b + 1}{2}\right)$. Since $g$ is injective, $\frac{a + 1}{2} = \frac{b + 1}{2} \implies a = b$.  
   - Case 3: $a$ even, $b$ odd (or vice versa).  
     Then $h(a) \in X$ and $h(b) \in Y$. Since $X \cap Y = \emptyset$, $h(a) \neq h(b)$, which is a contradiction. Hence, this case cannot occur.  
   Thus, $h$ is injective.  

2. Surjectivity:  
   - Let $z \in X \cup Y$.  
   - Case 1: $z \in X$. Since $f$ is surjective, there exists $m \in \mathbb{N}$ such that $f(m) = z$. Then $h(2m) = f\left(\frac{2m}{2}\right) = f(m) = z$.  
   - Case 2: $z \in Y$. Since $g$ is surjective, there exists $m \in \mathbb{N}$ such that $g(m) = z$. Then $h(2m - 1) = g\left(\frac{(2m - 1) + 1}{2}\right) = g(m) = z$.  
   Thus, every element in $X \cup Y$ is mapped to by $h$, making $h$ surjective.  

Since $h$ is both injective and surjective, it is a bijection.  