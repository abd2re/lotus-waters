## Q3

First, observe that
$$T\circ T = Z
\implies
T(T(v)) =\vec{0}$$ 

for every $v$ in $V$.

But $T\bigl(T(v)\bigr)=\vec{0}$ is precisely the statement that every vector in the image of $T$ lies in the kernel of $T$. Concretely:

- **$\Rightarrow$** Suppose $T\circ T=Z$. Then for any $v\in V$,

  $$
  T(T(v)) =\vec{0}
  $$

  which shows $T(v)\in\ker(T)$. Hence $\mathrm{Im}(T)\subseteq \ker(T)$.

- **$\Leftarrow$** Conversely, if $\mathrm{Im}(T)\subseteq \ker(T)$, then for any $v\in V$, the vector $T(v)$ is in $\ker(T)$. That is,
  $$
  T(v)\in \ker(T)\implies T\bigl(T(v)\bigr)=\vec{0}
  $$
  Hence $T\circ T$ sends every $v$ to $\vec{0}$. Thus $T\circ T=Z$.

