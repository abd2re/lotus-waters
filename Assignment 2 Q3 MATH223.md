## Q3

**Base Case**
For $n = 1$, the matrix $J_1$ is simply $\begin{pmatrix}1\end{pmatrix}$. Clearly, $\det(J_1) = 1$. The formula for odd $n$ says

$$
(-1)^{\frac{1-1}{2}}
\;=\;
(-1)^0
\;=\;
1,
$$

so it holds for $n=1$.

**Inductive Step**

Assume for some integer $k \ge 1$ that

$$
\det(J_k)
\;=\;
\begin{cases}
(-1)^{\tfrac{k}{2}}, & \text{if $k$ is even},\\
(-1)^{\tfrac{k-1}{2}}, & \text{if $k$ is odd}.
\end{cases}
$$

We will show it also holds for $k+1$. That is,

$$
\det\bigl(J_{k+1}\bigr)
\;=\;
\begin{cases}
(-1)^{\tfrac{k+1}{2}}, & \text{if $k+1$ is even},\\
(-1)^{\tfrac{k}{2}}, & \text{if $k+1$ is odd}.
\end{cases}
$$

Consider the $(k+1)\cdot(k+1)$ matrix $J_{k+1}$. By definition, its last row is

$$
\bigl(1,\,0,\,0,\,\dots,\,0\bigr)
$$

because the entry $(k+1, 1)$ is $1$, and all other entries in the last row are $0$.

To compute $\det(J_{k+1})$, perform a cofactor expansion along this last row:

1. The only nonzero entry in the $(k+1)$-th row is the $1$ in column $1$.
2. Its cofactor has the sign factor $(-1)^{(k+1)+1} = (-1)^{k+2}$.
3. The submatrix obtained by removing the last row $(k+1)$ and the first column is exactly $J_k$.

Hence,

$$
\det\bigl(J_{k+1}\bigr)
\;=\;
1 \;\cdot\; (-1)^{k+2} \;\cdot\; \det\bigl(J_k\bigr)
\;=\;
(-1)^{k+2}\,\det(J_k).
$$

By the inductive hypothesis,

$$
\det(J_k)
=
\begin{cases}
(-1)^{\tfrac{k}{2}}, & \text{if $k$ is even},\\
(-1)^{\tfrac{k-1}{2}}, & \text{if $k$ is odd}.
\end{cases}
$$

Thus,

$$
\det(J_{k+1})
\;=\;
(-1)^{k+2}
\cdot
\det(J_k)
\;=\;
\begin{cases}
(-1)^{k+2}\,(-1)^{\tfrac{k}{2}}, & \text{if $k$ is even},\\
(-1)^{k+2}\,(-1)^{\tfrac{k-1}{2}}, & \text{if $k$ is odd}.
\end{cases}
$$

- First case: $k$ even. Then $k = 2m$ for some $m$. So $k+1 = 2m+1$ is odd. Hence,

  $$
  \det(J_{k+1})
  \;=\;
  (-1)^{(2m)+2} \, (-1)^{m}
  \;=\;
  (-1)^{2m+2} \, (-1)^{m}
  \;=\;
  (-1)^{3m+2}.
  $$

  Since $(-1)^{3m+2} = (-1)^{m}$, we get $\det(J_{k+1}) = (-1)^m$. Now, for $k+1$ odd, the formula says

  $$
  \det(J_{k+1}) = (-1)^{\frac{(k+1)-1}{2}}
  \;=\;
  (-1)^m,
  $$

  matching perfectly.

- Second case: $k$ odd. Then $k = 2m+1$. So $k+1 = 2m+2$ is even. Then

  $$
  \det(J_{k+1})
  \;=\;
  (-1)^{(2m+1)+2}\,(-1)^{\tfrac{(2m+1)-1}{2}}
  \;=\;
  (-1)^{2m+3}\,(-1)^{m}
  \;=\;
  (-1)^{3m+3}.
  $$

  Since $(-1)^{3m+3} = (-1)^{m+1}$, we get $\det(J_{k+1}) = (-1)^{m+1}$. Now, for $k+1$ even, the formula says

  $$
  \det(J_{k+1}) = (-1)^{\frac{k+1}{2}}
  \;=\;
  (-1)^{m+1},
  $$

  again a perfect match.

Hence in both cases, $\det(J_{k+1})$ matches the desired formula, completing the inductive step.

**Conclusion**

By the principle of mathematical induction:

1. **Base case**: $\det(J_1) = 1$ agrees with the formula for odd $n$.
2. **Inductive step**: If $\det(J_k)$ follows the given formula, then so does $\det(J_{k+1})$.

Therefore, for all $n \ge 1$,

$$
\det(J_n)
\;=\;
\begin{cases}
(-1)^{\tfrac{n}{2}}, & \text{if $n$ is even},\\
(-1)^{\tfrac{n-1}{2}}, & \text{if $n$ is odd}.
\end{cases}
$$
