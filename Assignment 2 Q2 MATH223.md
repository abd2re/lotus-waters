## Q2

**(a)**
Suppose $A$ is in the span of $B, C, D$. Then there exist complex scalars $\alpha, \beta, \gamma \in \mathbb{C}$ such that

$$
\alpha B + \beta C + \gamma D = A.
$$

That is,

$$
\alpha \begin{pmatrix} i & 1 \\ 1 & i \end{pmatrix}
\;+\;
\beta \begin{pmatrix} 1 & i \\ i & 1 \end{pmatrix}
\;+\;
\gamma \begin{pmatrix} 1 & 1 \\ 1 & 1 \end{pmatrix}
\;=\;
\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}.
$$

$$
\alpha
\begin{pmatrix} i & 1 \\ 1 & i \end{pmatrix}
+
\beta
\begin{pmatrix} 1 & i \\ i & 1 \end{pmatrix}
+
\gamma
\begin{pmatrix} 1 & 1 \\ 1 & 1 \end{pmatrix}
=
\begin{pmatrix}
\alpha i + \beta + \gamma & \alpha + \beta i + \gamma \\
\alpha + \beta i + \gamma & \alpha i + \beta + \gamma
\end{pmatrix}.
$$

Thus, effectively we have three distinct equations:

- $\alpha i + \beta + \gamma = 1$ $\quad (1)$
- $\alpha + \beta i + \gamma = 1$ $\quad (2)$
- $\alpha + \beta i + \gamma = 0$ $\quad (3)$

$\alpha + \beta i + \gamma$ must be simultaneously equal to $1$ (from equation (2)) and $0$ (from equation (3)). This is clearly impossible unless $1=0$ in $\mathbb{C}$, which is absurd. Hence, there is no solution $(\alpha, \beta, \gamma)$ that satisfies these equations.

This contradiction implies that the matrix $A$ cannot be written as a linear combination of $B, C, D$. Hence,

$$
A \not\in \text{span}\{B, C, D\}.
$$

**(b)**
Let $u=\begin{pmatrix}1\\1\\ \vdots\\1\end{pmatrix}$ and $v_1 = \begin{pmatrix} 0 \\ 1 \\ 1 \\ \vdots \\ 1 \\ 1 \end{pmatrix}, v_2 = \begin{pmatrix} 1 \\ 0 \\ 1 \\ 1 \\ \vdots \\ 1 \end{pmatrix}, v_3 = \begin{pmatrix} 1 \\ 1 \\ 0 \\ 1 \\ \vdots \\ 1 \end{pmatrix}, \ldots, v_n = \begin{pmatrix} 1 \\ 1 \\ \vdots \\ 1 \\ 1 \\ 0 \end{pmatrix}$ in $\mathbb{R}^{n}$ where $n \geq 2$.

Let $w$ be the sum of every vectors $v_{i}$ in $\mathbb{R}^{n}$, because every vector $v_{i}$ has $1$ in all its rows except its $i$th row, $w=\sum{v_{i}}=(n-1)\begin{pmatrix}1\\1\\ \vdots\\1\end{pmatrix}$, and by the hypothesis, we can rewrite $w$ as $$w=(n-1)u$$
and we can rearrange this equation to have $$u=\frac{1}{n-1}w$$

Because $w$ is a linear combination of the vectors in $\mathbb{R}^n$ (the sum of all of them), $u$ is also a linear combination of the vectors in $\mathbb{R}^{n}$ where $u=c_{1}v_{1}+c_{2}v_{2}+\dots +c_{n}v_{n}$ where $c_{1}=c_{2}=...=c_{n}=\frac{1}{n-1}$.

Hence $u$ is in the span of $\{v_{1},v_{2},...,v_{n}\}$.
