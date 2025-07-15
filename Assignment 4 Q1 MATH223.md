## Q1

(a)
 If $U = \mathrm{span}(\alpha)$ and $W = \mathrm{span}(\beta)$, then every vector in $U+W$ looks like 
$$
u + w = \bigl(\text{linear combination of vectors in }\alpha\bigr)\;+\;\bigl(\text{linear combination of vectors in }\beta\bigr).
$$
That is precisely a linear combination of all the vectors in $\alpha \cup \beta$. Hence, 
$$
U + W \;\subseteq\; \mathrm{span}(\alpha \cup \beta).
$$
On the other hand, any linear combination of vectors in $\alpha\cup\beta$ is clearly in $\mathrm{span}(\alpha)\,+\,\mathrm{span}(\beta)$. Thus,
$$
\mathrm{span}(\alpha \cup \beta)\;\subseteq\; U + W.
$$
So we conclude $U+W = \mathrm{span}(\alpha \cup \beta)$.



(b)
 We want an example where $U = \mathrm{span}(\alpha)$ and $W = \mathrm{span}(\beta)$ but
$$
U \,\cap\, W \;\neq\; \mathrm{span}\bigl(\alpha \,\cap\, \beta\bigr).
$$
A simple one is to take $V = \mathbb{R}^2$ and define
$$
\alpha = \{(1,0),\, (1,1)\},\quad \beta = \{(0,1),\, (1,1)\}.
$$
- Note that $\alpha$ spans all of $\mathbb{R}^2$ (because $(1,0)$ and $(1,1)$ are linearly independent and together they can generate any $(x,y)\in \mathbb{R}^2$).
- Similarly, $\beta$ also spans all of $\mathbb{R}^2$.

Hence $U = W = \mathbb{R}^2$. So 
$$
U \,\cap\, W = \mathbb{R}^2.
$$
However, if we just look at the sets $\alpha$ and $\beta$, their intersection as sets is
$$
\alpha \,\cap\, \beta =\{(1,1)\}.
$$
Thus
$$
\mathrm{span}(\alpha \,\cap\, \beta) = \mathrm{span}\bigl(\{(1,1)\}\bigr),
$$
which is all multiples of $(1,1)$. That is only a 1‐dimensional subspace, while $U \cap W$ turned out to be all of $\mathbb{R}^2$. Clearly,
$$
\mathbb{R}^2 \;\neq\; \mathrm{span}\bigl(\{(1,1)\}\bigr).
$$
So this shows $U \cap W \neq \mathrm{span}(\alpha \cap \beta)$ in this example.


(c)
 Suppose $U \cap W = \{\vec{0}\}$, $\alpha$ is a basis for $U$, and $\beta$ is a basis for $W$.

1. Why $\alpha \cap \beta = \varnothing$
   If there were a nonzero vector $v$ in both $\alpha$ and $\beta$, then that vector $v$ would lie in both $U$ and $W$, contradicting $U \cap W = \{\vec{0}\}$. So no nonzero vector can be in both $\alpha$ and $\beta$. Hence as sets, $\alpha \cap \beta$ must be empty.

2. Why is $\alpha \cup \beta$ a basis of $U+W$
   - First, spanning: Any vector in $U + W$ is a sum $u + w$ with $u \in U$, $w \in W$. Since $u$ can be written using the vectors in $\alpha$ and $w$ can be written using the vectors in $\beta$, it follows that $u+w$ is in the span of $\alpha \cup \beta$.  
   - Second, linear independence: Suppose a linear combination of vectors in $\alpha \cup \beta$ equals zero:
     $$
     c_1 a_1 + \cdots + c_m a_m \;+\; d_1 b_1 + \cdots + d_n b_n = 0,
     $$
     where $a_i \in \alpha$ and $b_j \in \beta$.  Group the terms to see that
     $$
     (c_1 a_1 + \cdots + c_m a_m) = -\,\bigl(d_1 b_1 + \cdots + d_n b_n\bigr).
     $$
     The left side is in $U$ and the right side is in $W$, so this vector is in $U \cap W$.  By hypothesis $U \cap W = \{\vec{0}\}$, so the common vector must be the zero vector.  Because $\alpha$ and $\beta$ are each bases for their respective subspaces, all the coefficients $c_i$ and $d_j$ must be zero.  This proves that $\alpha \cup \beta$ is linearly independent.

Combining these two facts, $\alpha \cup \beta$ is a linearly independent set that spans $U+W$, hence it is a basis for $U+W$.