## Q3

(a)
RREF of $V$ is $$\begin{bmatrix}1&0&0&\frac{1}{2}&0&0&\frac{3}{2}&0&0\\ 0&1&0&0&\frac{1}{2}&0&0&\frac{3}{2}&0\\ 0&0&1&0&0&\frac{1}{2}&0&0&\frac{3}{2}\end{bmatrix}$$

RREF of $W$ is $$\begin{bmatrix}1&0&0&0&-1&0&0&0&0\\ 0&1&0&0&-1&0&0&0&0\\ 0&0&1&0&0&-1&0&0&0\\ 0&0&0&1&-1&0&0&0&0\\ 0&0&0&0&0&0&1&-1&0\\ 0&0&0&0&0&0&0&0&1\end{bmatrix}$$


(b)

System for V

A vector $\vec{x} = (x_1,\dots,x_9)$ lies in $V$ precisely if it is a linear combination of the 3 row-vectors given for $V$. Concretely, we can write:

$$
\vec{x} =
a\,(1,0,0,\tfrac12,0,0,\tfrac32,0,0)
\;+\;
b\,(0,1,0,0,\tfrac12,0,0,\tfrac32,0)
\;+\;
c\,(0,0,1,0,0,\tfrac12,0,0,\tfrac32).
$$

Hence, comparing coordinates,

$$
\begin{cases}
x_1 = a, \\
x_2 = b, \\
x_3 = c, \\
x_4 = \tfrac12\,a, \\
x_5 = \tfrac12\,b, \\
x_6 = \tfrac12\,c, \\
x_7 = \tfrac32\,a, \\
x_8 = \tfrac32\,b, \\
x_9 = \tfrac32\,c.
\end{cases}
$$

From these, we see that $x_1, x_2, x_3$ can be treated as free variables $(a,b,c)$, and all other coordinates are determined by them. Rearranging to make them into linear equations of the form $\dots = 0$, we get:

$$
\begin{aligned}
&x_4 - \tfrac12\,x_1 = 0, ~
x_5 - \tfrac12\,x_2 = 0, ~
x_6 - \tfrac12\,x_3 = 0,\\
&x_7 - \tfrac32\,x_1 = 0, ~
x_8 - \tfrac32\,x_2 = 0, ~
x_9 - \tfrac32\,x_3 = 0.
\end{aligned}
$$

These 6 equations (in 9 unknowns) describe precisely those $\vec{x}$ in $\mathbb{R}^9$ that lie in $V$.

System for $W$

Similarly, a vector $\vec{x} = (x_1,\dots,x_9)$ is in $W$ if and only if it is a linear combination of the 6 row-vectors given for $W$. Labeling these 6 vectors as

$$
\begin{aligned}
&r_1 = (\,1,0,0,0,-1,0,\,0,0,0\,), \\
&r_2 = (\,0,1,0,0,-1,0,\,0,0,0\,), \\
&r_3 = (\,0,0,1,0,0,-1,\,0,0,0\,), \\
&r_4 = (\,0,0,0,1,-1,0,\,0,0,0\,), \\
&r_5 = (\,0,0,0,0,0,0,\;1,-1,0\,), \\
&r_6 = (\,0,0,0,0,0,0,\;0,0,1\,),
\end{aligned}
$$

we see that the general element of $W$ has the form

$$
\vec{x} =
a_1\,r_1 + a_2\,r_2 + a_3\,r_3 + a_4\,r_4 + a_5\,r_5 + a_6\,r_6.
$$

- Equation 1: Observing that $x_5$ always appears as $-a_1 - a_2 - a_4$, while $x_1=a_1$, $x_2=a_2$, $x_4=a_4$. Summing them:
  $$
  x_1 + x_2 + x_4 + x_5 = 0.
  $$
- Equation 2: From $r_3$, we see $x_3 = a_3$ and $x_6 = -a_3$. So
  $$
  x_3 + x_6 = 0.
  $$
- Equation 3: From $r_5$, we have $x_7 = a_5$ and $x_8=-a_5$. So
  $$
  x_7 + x_8 = 0.
  $$

Hence the system of equations for membership in $W$ is

$$
\begin{cases}
x_1 + x_2 + x_4 + x_5 = 0, \\
x_3 + x_6 = 0, \\
x_7 + x_8 = 0.
\end{cases}
$$

These three equations describe precisely those $\vec{x}$ in $\mathbb{R}^9$ lying in $W$. The free variables in this description can be taken to be $x_1, x_2, x_3, x_4, x_7, x_9$, giving a 6-dimensional solution space.

(c)

A vector $\vec{x}$ is in $V \cap W$ if and only if it satisfies both the system for $V$ and the system for $W$. Concretely:

1. From $V$, we have

   $$
   x_4 = \tfrac12 x_1,~ x_5 = \tfrac12 x_2,~ x_6 = \tfrac12 x_3,~
   x_7 = \tfrac32 x_1,~ x_8 = \tfrac32 x_2,~ x_9 = \tfrac32 x_3.
   $$

2. From $W$, we additionally require
   $$
   \begin{cases}
   x_1 + x_2 + x_4 + x_5 = 0,\\
   x_3 + x_6 = 0,\\
   x_7 + x_8 = 0.
   \end{cases}
   $$

Substitute the expressions from (1) into (2):

- $x_1 + x_2 + x_4 + x_5 = x_1 + x_2 + \tfrac12 x_1 + \tfrac12 x_2 = \tfrac32(x_1 + x_2) = 0$.
  Hence $x_2 = -x_1.$

- $x_3 + x_6 = x_3 + \tfrac12 x_3 = \tfrac32 x_3 = 0.$
  Hence $x_3 = 0$. Then automatically $x_6=0$ and $x_9 = \tfrac32 x_3 = 0.$

- $x_7 + x_8 = \tfrac32 x_1 + \tfrac32 x_2 = \tfrac32(x_1 + x_2) = 0.$
  But we already have $x_2=-x_1$, so $x_7 + x_8=0$ is automatically satisfied.

Collecting these results:

$$
\begin{aligned}
&x_2 = -x_1,~ x_3=0,\\
&x_4 = \tfrac12\,x_1,~ x_5 = \tfrac12\,x_2 = \tfrac12(-x_1) = -\tfrac12\,x_1,\\
&x_6=0,~ x_7 = \tfrac32\,x_1,~ x_8 = \tfrac32\,x_2 = -\tfrac32\,x_1,~ x_9=0.
\end{aligned}
$$

All coordinates are determined by a single free parameter $x_1$. Let $x_1 = t$. Then

$$
\vec{x} =
\bigl(t,\,-t,\,0,\,\tfrac12 t,\,-\tfrac12 t,\,0,\,\tfrac32 t,\,-\tfrac32 t,\,0\bigr).
$$

Factoring out $t$,

$$
\vec{x} = t\;\bigl(1,\,-1,\,0,\,\tfrac12,\,-\tfrac12,\,0,\,\tfrac32,\,-\tfrac32,\,0\bigr).
$$

Thus $V \cap W$ is 1-dimensional, and a convenient basis is given by the single vector

$$
\bigl(1,\,-1,\,0,\;\tfrac12,\,-\tfrac12,\,0,\;\tfrac32,\,-\tfrac32,\,0\bigr)
$$

(d)

We know from general dimension formulas that

$$
\dim(V + W) = \dim(V)\;+\;\dim(W)\;-\;\dim(V\cap W)
=3 \;+\; 6 \;-\; 1 = 8.
$$

Thus $V+W$ is an 8-dimensional subspace of $\mathbb{R}^9$.

1. A basis for $V$ (the 3 row-vectors) is:
   $$
   v_1 = (1,0,0,\tfrac12,0,0,\tfrac32,0,0),~
   v_2 = (0,1,0,0,\tfrac12,0,0,\tfrac32,0),~
   v_3 = (0,0,1,0,0,\tfrac12,0,0,\tfrac32).
   $$
2. A basis for $W$ (the 6 row-vectors) is:
   $$
   w_1=(1,0,0,0,-1,0,0,0,0),\;
   w_2=(0,1,0,0,-1,0,0,0,0),\;
   w_3=(0,0,1,0,0,-1,0,0,0),
   $$
   $$
   w_4=(0,0,0,1,-1,0,0,0,0),\;
   w_5=(0,0,0,0,0,0,1,-1,0),\;
   w_6=(0,0,0,0,0,0,0,0,1).
   $$

Putting all 9 vectors together into rows of a $9 \times 9$ matrix and calculating it's RREF, the last row is all zeroes so we can remove $w_6$ and keep the rest. So a perfectly good choice of basis for $V+W$ is:

$$
\{v_1,\;v_2,\;v_3,\;w_1,\;w_2,\;w_3,\;w_4,\;w_5\}.
$$

These 8 vectors are linearly independent and span $V+W$. Thus they form the desired basis of $V+W$.
