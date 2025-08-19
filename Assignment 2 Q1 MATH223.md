## Q1

**(a)**
Let $u \in V$ and $c \in F$ be such that $$cu=\vec{0}$$
We want to show that $c=0$ or $u=\vec{0}$.

Assume for contradiction that $c\neq 0$. Since $c\neq 0$, we can multiply both sides of $cu=\vec{0}$ by the scalar $\frac{1}{c}$
$$\frac{1}{c}(cu)=\frac{1}{c}\vec{0}$$
$$\left(\frac{1}{c}c\right)u=\vec{0}$$
$$1\cdot u=\vec{0}$$
$$u=\vec{0}$$
Therefore if $c \neq 0$, we necessarily have $u=\vec{0}$.

If $c=0$, then $cu=0u=\vec{0}$, so the statement holds.

Hence whenever, $cu=\vec{0}$, either $c=0$ or $u=\vec{0}$.

**(b)**
Let $u \in V$ and $a,b \in F$ with $u \neq \vec{0}$ and $a \neq b$. We want to prove that $$au \neq bu$$
Assume for contradiction, that $au=bu$
$$au-bu=(a-b)u=\vec{0}$$
By this equation, either $a-b=0$ or $u=\vec{0}$
But by the hypothesis $a \neq b$, so $a-b \neq 0$ and therefore we cannot have $a-b=0$. 
Also by the hypothesis $u \neq \vec{0}$, hence we cannot have $u = \vec{0}$.
This is contradiction.

Therefore our assumption $au=bu$ must be false, which implies $au \neq bu$.

**(c)**
Let $u,v \in V$ and $c \in F$ with $u \neq v$ and $c \neq 0$. We want to show that $$cu \neq cv$$
Assume for contradiction, that $cu=cv$ $$cu-cv=c(u-v)=\vec{0}$$
By this equation, either $c=0$ or $u-v=\vec{0}$.
By hypothesis, $c \neq 0$, so we cannot have $c=0$.
Also $u \neq v$ so $u-v \neq \vec{0}$.
This is contradiction.

Therefore our assumption $cu=cv$ must be false, which implies that $cu \neq cv$.