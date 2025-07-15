## Q1

(a)
We want to show
$$
k \binom{n}{k} = n \binom{n-1}{k-1}.
$$

Starting from the left‐hand side:

$$
k \binom{n}{k}
=
k \cdot \frac{n!}{k!\,(n-k)!}
=
\frac{k \cdot n!}{k!\,(n-k)!}.
$$

$n!$ can be rewritten as $n \cdot (n-1)!$ and we can divide $k!$ by $k$

$$
\frac{k \cdot n!}{k! \,(n-k)!}
= \frac{n!}{(k-1)!\,(n-k)!}
= n \cdot \frac{(n-1)!}{(k-1)!\,\bigl((n-1)-(k-1)\bigr)!}
= n \binom{n-1}{k-1}
$$

Hence,

$$
k \binom{n}{k} = n \binom{n-1}{k-1}.
$$

(b)
1. $k \binom{n}{k}$:

   - First choose a $k$-element subset from $n$ objects (this can be done in $\binom{n}{k}$ ways).
   - Then, from within those chosen $k$ objects, pick one special element (this can be done in $k$ ways).
   - So the total number of ways to perform this two-step process is $k \binom{n}{k}$.

2. $n \binom{n-1}{k-1}$:
   - First choose 1 distinguished object out of the $n$ (there are $n$ ways).
   - Then choose the remaining $k-1$ objects from the remaining $n-1$ (there are $\binom{n-1}{k-1}$ ways).
   - So the total number of ways to do this is $n \binom{n-1}{k-1}$.

Because these two descriptions count exactly the same set of $k$-element subsets with one distinguished element, we must have

$$
k \binom{n}{k} = n \binom{n-1}{k-1}.
$$

This completes the combinatorial argument.