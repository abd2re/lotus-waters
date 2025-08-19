## Q2

We can transform these four $2\times 2$ matrices in the form
$$
\begin{pmatrix} a & b \\ c & d \end{pmatrix}
$$
into the vector $\bigl(a,b,c,d\bigr)$ in $\mathbb{C}^4.$  Writing out each of the given matrices in that format and placing them as columns of a $4\times 4$ matrix, we find

$$
\begin{pmatrix}
1 & 0 & 0 & c\\
c & i & 0 & 0\\
0 & c & 2 & 0\\
0 & 0 & c & -i
\end{pmatrix}
$$
Let's now take its determinant

$$
\begin{vmatrix}
1 & 0 & 0 & c\\
c & i & 0 & 0\\
0 & c & 2 & 0\\
0 & 0 & c & -i
\end{vmatrix}
=
\begin{vmatrix}
i & 0 & 0\\
c & 2 & 0\\
0 & c & -i
\end{vmatrix}
-c
\begin{vmatrix}
c & i & 0 \\
0 & c & 2 \\
0 & 0 & c 
\end{vmatrix}
=
i
\begin{vmatrix}
2 & 0\\
c & -i
\end{vmatrix}
-c^{2}
\begin{vmatrix}
c & 2 \\
0 & c 
\end{vmatrix}
=2-c^{4}
$$

So its determinant is $2 - c^4.$  Since four vectors in a four‐dimensional space form a basis precisely when the corresponding determinant is nonzero, we see that these matrices form a basis of $M_{2\times 2}(\mathbb{C})$ exactly when 
$$
2 - c^4 \; \neq \; 0,
$$
so when $c^4 \neq 2.$  So it's a basis if $c \neq \pm \sqrt[4]{2}$ and $c \neq \pm i \sqrt[4]{2}$. Equivalently, they fail to be a basis precisely for the solutions of $c^{4}=2$ in the complex plane.

