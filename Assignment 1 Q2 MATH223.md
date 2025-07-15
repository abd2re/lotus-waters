### Question 2

Let $V = \mathbb{C}^2$ for all the axioms.

$\rightarrow$ (VS1)

We require $u + v = v + u$ for all $u,w \in V.$

Let $u = (z_1,z_2)$ and $v = (z_3,z_4)$. Then:

- By definition,

  $$
  u + v
  = (z_1 + \overline{z_3}, z_2 + \overline{z_4}).
  $$

- Similarly,
  $$
  v + u
  = (z_3 + \overline{z_1}, z_4 + \overline{z_2}).
  $$

In general, these are not equal. For instance, let $z_1 = 1$, $z_3 = 2i$. Then 

$$z_1 + \overline{z_3} = 1 + (-2i) = 1 - 2i,$$$$z_3 + \overline{z_1} = 2i + 1 = 1 + 2i$$ 

and clearly $1 - 2i \neq 1 + 2i$. 

Hence (VS1) fails.

---

$\rightarrow$ (VS2)

We need $(u + v) + w = u + (v + w)$ for all $u,v,w \in V$

Let $u = (z_1,z_2)$, $v = (z_3,z_4)$, $w = (z_5,z_6)$.

$$
u + v = (z_1 + \overline{z_3}, z_2 + \overline{z_4}).
$$

Then

$$
(u+v) + w
= ((z_1 + \overline{z_3}) + \overline{z_5},\; (z_2 + \overline{z_4}) + \overline{z_6})
= (z_1 + \overline{z_3} + \overline{z_5}, \; z_2 + \overline{z_4} + \overline{z_6})
$$

And

$$
v + w = (z_3 + \overline{z_5},  z_4 + \overline{z_6}).
$$

Hence

$$
u + (v + w)
= (z_1 + \overline{(z_3 + \overline{z_5})},\; z_2 + \overline{(z_4 + \overline{z_6})}).
$$

Recall $\overline{(z_3 + \overline{z_5})} = \overline{z_3} + z_5$. So

$$
u + (v + w)
= (z_1 + (\overline{z_3} + z_5),\; z_2 + (\overline{z_4} + z_6))
= (z_1 + \overline{z_3} + z_5,\; z_2 + \overline{z_4} + z_6).
$$

Comparing:

- $(u+v) + w$ has $\overline{z_5}$ in the first coordinate.
- $u + (v+w)$ has $z_5$ in the first coordinate.

They differ unless $z_5$ is real (and similarly $z_6$). Therefore (VS2) fails.

---

$\rightarrow$ (VS3)

We want $\vec{0} \in V$ such that $u + \vec{0} = u$ for all $u \in V$.

Suppose $\vec{0} = (a,b)$. Then for $u = (z_1,z_2)$:

$$
u + \vec{0}
= (z_1, z_2) + (a,b)
= (z_1 + \overline{a}, z_2 + \overline{b}).
$$

We require $(z_1 + \overline{a}, z_2 + \overline{b}) = (z_1,z_2)$ for all $z_1,z_2$. Hence

$$
\overline{a} = 0 ,~ \overline{b} = 0
\;\;\Longrightarrow\;\; a=0,\; b=0.
$$

Thus $\vec{0} = (0,0)$. Indeed:

$$
(z_1,z_2) + (0,0) = (z_1,z_2).
$$

Hence (VS3) holds.

> Note: We only require $u + \vec{0} = u$, not necessarily $\vec{0} + u = u$.

---

$\rightarrow$ (VS4)

For each $u \in V$, we want $-u$ such that

$$
u + (-u) = \vec{0}.
$$

Let $u = (z_1, z_2)$. Suppose $-u = (x,y)$. Then

$$
u + (-u)
= (z_1, z_2) + (x,y)
= (z_1 + \overline{x},\; z_2 + \overline{y}).
$$

We want this to be $(0,0)$. Hence

$$
\overline{x} = -z_1
\;\;\Longrightarrow\;\; x = -\overline{z_1},
\quad
\overline{y} = -z_2
\;\;\Longrightarrow\;\; y = -\overline{z_2}.
$$

Therefore

$$
-u = (-\overline{z_1}, -\overline{z_2}).
$$

Hence (VS4) holds.

---

$\rightarrow$ (VS5)

We need $1 \cdot u = u$ for all $u \in V$. By definition,

$$
c \cdot (z_1, z_2) = (\overline{c}z_1, \overline{c}z_2).
$$

If $c = 1$, then $\overline{1} = 1$, so

$$
1 \cdot (z_1,z_2)
= (\overline{1}z_1,\; \overline{1}z_2)
= (z_1,z_2).
$$

Thus (VS5) holds.

---

$\rightarrow$ (VS6)

We want $(ab)u = a(bu)$ for all $a,b \in \mathbb{C}$ and $u\in V$.

Let $u=(z_1,z_2)$. Then:

1. Left-hand side $(ab)u$:

   $$
   (ab)(z_1,z_2)
   = (\overline{ab}z_1,\;\overline{ab}z_2)
   = (\overline{a}\overline{b}z_1,\;\overline{a}\overline{b}z_2).
   $$

2. Right-hand side $a(bu)$:
   $$
   bu
   = (\overline{b}z_1,\;\overline{b}z_2),
   $$
   so
   $$
   a(\overline{b}z_1,\;\overline{b}z_2)
   = (\overline{a}\overline{b}z_1,\;\overline{a}\overline{b}z_2).
   $$

They coincide, so (VS6) holds.

---

$\rightarrow$ (VS7)

We need $a(u+v) = au + av$ for all $a\in \mathbb{C}, u,v \in V$.

Let $u=(z_1,z_2)$ and $v=(z_3,z_4)$.

- Left-hand side:

  $$
  u+v = (z_1 + \overline{z_3}, z_2 + \overline{z_4}),
  $$

  so

  $$
  a(u+v)
  = a(z_1 + \overline{z_3}, z_2 + \overline{z_4})
  = (\overline{a}(z_1 + \overline{z_3}),\; \overline{a}(z_2 + \overline{z_4})).
  $$

  That is

  $$
  = (\overline{a}z_1 + \overline{a}\overline{z_3},\; \overline{a}z_2 + \overline{a}\overline{z_4}).
  $$

- Right-hand side:
  $$
  au = (\overline{a}z_1,\;\overline{a}z_2),
  \quad
  av = (\overline{a}z_3,\;\overline{a}z_4).
  $$
  Then
  $$
  au + av
  = (\overline{a}z_1,\;\overline{a}z_2)
    + (\overline{a}z_3,\;\overline{a}z_4).
  $$
  $$
  au+av
  = (\overline{a}z_1 + \overline{(\overline{a}z_3)},\;
           \overline{a}z_2 + \overline{(\overline{a}z_4)}).
  $$
  But $\overline{(\overline{a}z_3)} = a\overline{z_3}$. Hence
  $$
  au + av
  = (\overline{a}z_1 + a\overline{z_3},\; \overline{a}z_2 + a\overline{z_4}).
  $$

Comparing with $a(u+v)$:

$$
\overline{a}\overline{z_3} \quad \text{vs.} \quad a\overline{z_3}.
$$

They match only if $\overline{a} = a$ (i.e., $a$ is real). For general $a\in \mathbb{C}$, they differ. Thus (VS7) fails.

---

$\rightarrow$ (VS8)

We need $(a + b)u = au + bu$ for all $a,b \in \mathbb{C},\; u\in V$.

Let $u=(z_1,z_2)$. Then:

- Left-hand side:

  $$
  (a+b)u
  = (\overline{(a+b)}z_1,\; \overline{(a+b)}z_2)
  = ((\overline{a}+\overline{b})z_1,\;(\overline{a}+\overline{b})z_2).
  $$

- Right-hand side:
  $$
  au = (\overline{a}z_1,\;\overline{a}z_2),
  \quad
  bu = (\overline{b}z_1,\;\overline{b}z_2).
  $$
  Hence
  $$
  au + bu
  = (\overline{a}z_1,\;\overline{a}z_2) + (\overline{b}z_1,\;\overline{b}z_2).
  $$
  $$
  au+bu= (\overline{a}z_1 + \overline{(\overline{b}z_1)},\;
           \overline{a}z_2 + \overline{(\overline{b}z_2)}).
  $$
  And $\overline{(\overline{b}z_1)} = b\overline{z_1}$. So
  $$
  au + bu
  = (\overline{a}z_1 + b\overline{z_1},\; \overline{a}z_2 + b\overline{z_2}).
  $$

Compare this with $$ (\overline{a}+\overline{b})z_1 \quad \text{vs.} \quad \overline{a}z_1 + b\overline{z_1}. $$ They are not generally equal. Hence (VS8) fails.
