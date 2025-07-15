## Q3

1. **At least one black stone**

A direct way to say "there is at least one black stone" is to take the disjunction of all $b_{ij}$:

$$
p_{1} =\bigvee_{i=1}^{4}\,\bigvee_{j=1}^{4} b_{ij}
$$

This is true exactly when at least one $b_{ij}$ is true.

2. **At least two white stones, and at least one is in a corner**

We can break this into two pieces:

1. At least two white stones: one way is to say "there exist two distinct cells $(i_{1}, j_{1})\neq (i_{2}, j_{2})$ both occupied by white stones." In propositional form, we can write a big OR over all pairs:

   $$
   p({\text{twoWhite}}) =\bigvee_{\substack{(i_1,j_1),\, (i_2,j_2)\\(i_1,j_1)\neq(i_2,j_2)}}\!\!(w_{i_{1}j_{1}}\land w_{i_{2}j_{2}})
   $$

   This ensures at least two distinct white-stone positions.

2. At least one white stone in a corner: we have four corners, so
   $$
   p({\text{cornerWhite}})
   =
   (w_{1,1}\lor w_{1,4}\lor w_{4,1}\lor w_{4,4})
   $$

Putting these together:

$$
p_{2}
=
p({\text{twoWhite}})
\land
p({\text{cornerWhite}})
$$
$$p_{2}=(\bigvee_{\substack{(i_1,j_1),\, (i_2,j_2)\\(i_1,j_1)\neq(i_2,j_2)}}\!\!(w_{i_{1}j_{1}}\land w_{i_{2}j_{2}})) \land (w_{1,1}\lor w_{1,4}\lor w_{4,1}\lor w_{4,4})$$

3. **At most one stone (black or white) in any cell**

For each cell $(i,j)$, it cannot simultaneously have a black stone and a white stone. Hence,

$$
p_{3}
=
\bigwedge_{i=1}^{4}\,\bigwedge_{j=1}^{4}
\neg(b_{ij}\,\land\,w_{ij})
$$

This large and ensures that, in every cell, you cannot have both $b_{ij}$ and $w_{ij}$ or is empty.

4. **No two black stones are orthogonally adjacent**

We must ensure that if one black stone is in $(i,j)$, then the cell immediately above/below/left/right cannot also be black. Equivalently, for every pair of adjacent cells, not both can be black.

- Horizontal adjacency: for each row $i$, compare $(i,j)$ and $(i, j+1)$ for $j=1,2,3$.

  $$
    \bigwedge_{i=1}^{4}
    \bigwedge_{j=1}^{3}
    \neg(b_{i,j}\,\land\,b_{i,j+1})
  $$

- Vertical adjacency: for each column $j$, compare $(i,j)$ and $(i+1, j)$ for $i=1,2,3$.
  $$
    \bigwedge_{j=1}^{4}
    \bigwedge_{i=1}^{3}
    \neg(b_{i,j}\,\land\,b_{i+1,j})
  $$

Hence,

$$
p_{4}
=
(
  \bigwedge_{i=1}^{4}\,\bigwedge_{j=1}^{3}
  \neg(b_{i,j}\,\land\,b_{i,j+1})
)
\land
(
  \bigwedge_{j=1}^{4}\,\bigwedge_{i=1}^{3}
  \neg(b_{i,j}\,\land\,b_{i+1,j})
)
$$

**Final Formula $f$**

We combine all four conditions by taking the conjunction:

$$
f
=
p_{1}
\land
p_{2}
\land
p_{3}
\land
p_{4}
$$

This propositional formula $f$ is true if and only if all four conditions are satisfied.
