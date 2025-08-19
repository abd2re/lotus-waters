### Question 1

(a)
$$f(x)=(x-r)(x-\bar{r})$$
$$f(x)=x^{2}-\bar{r}x-rx+r \bar{r}$$
$$f(x)=x^{2}-(\bar{r}+r)x+|r|^{2}$$
$$f(x)=x^{2}-2\text{Re}(r)x+|r|^{2}$$
$\rightarrow 2\text{Re}(r) \in \mathbb{R}$
$\rightarrow |r|^{2}\in \mathbb{R}$
So for every $r \in \mathbb{C}$, the coefficients of the polynomial $f(x)$ all are in $\mathbb{R}$.
---
(b)
Let $f(x)=x^{2}+ax+b$ where $a,b \in \mathbb{R}$.
$$f(r)=0$$
$$r^{2}+ar+b=0$$
Let's take the complex conjugate of the entire equation. 
$$\overline{r^{2}+ar+b}=\bar{0}$$
$$\overline{r^{2}}+\bar{a}\bar{r}+\bar{b}=\bar{0}$$
Because $a,b \in \mathbb{R}$, $\bar{a}=a$ and $\bar{b}=b$, we have
$$\bar{r}^{2}+a \bar{r}+b=0$$
Hence$$f(\bar{r})=0$$