## Q3

(a)
$$
\langle u,v\rangle =\sum_{i=1}^n ia_ib_i,
\quad
u=(a_1,\dots,a_n),v=(b_1,\dots,b_n)
$$

1. Additivity in the first argument
   $$
   \langle (u+v),w\rangle
   = \sum_{i=1}^n i\bigl((a_i + b_i)\bigr)w_i
   = \sum_{i=1}^n ia_iw_i +\sum_{i=1}^n ib_iw_i
   = \langle u,w\rangle +\langle v,w\rangle
   $$
2. Homogeneity in the first argument
   $$
   \langle cu,v\rangle
   = \sum_{i=1}^n i(ca_i)b_i
   = c \sum_{i=1}^n ia_ib_i
   = c\langle u,v\rangle
   $$
3. Symmetry (real field):
   $$
   \langle u,v\rangle
   = \sum_{i=1}^n ia_ib_i
   = \sum_{i=1}^n ib_ia_i
   = \langle v,u\rangle
   $$
4. Positive-definiteness
   $$
   \langle u,u\rangle
   = \sum_{i=1}^n ia_i^2
   \ge0,
   $$
   and is zero iff every $a_i=0$. Hence $u=0$.

All four properties hold, so this is indeed an inner product on $\mathbb{R}^n$.

(b)

$$
\langle A,B\rangle =\mathrm{tr}(AB)
$$

1. Additivity in the first argument  
   $\mathrm{tr}((A_1 + A_2)B)
   = \mathrm{tr}(A_1B) + \mathrm{tr}(A_2B)$.
2. Homogeneity in the first argument  
   $\mathrm{tr}((cA)B) = c\mathrm{tr}(AB)$.
3. Symmetry  
   $\mathrm{tr}(AB) = \mathrm{tr}(BA)$, so $\langle A,B\rangle = \langle B,A\rangle$.
4. Positive-definiteness requires $\langle A,A\rangle = \mathrm{tr}(A^2)\ge0$ with equality only if $A=0$.
   - Counterexample: let
     $$
       A = \begin{pmatrix} 0 & 1 \\ -1 & 0 \end{pmatrix}.
     $$
     Then
     $$
       A^2 = \begin{pmatrix} -1 & 0 \\ 0 & -1 \end{pmatrix},
       \quad
       \mathrm{tr}(A^2) = -2 < 0.
     $$
     So $\langle A,A\rangle<0$.

Because it can give negative values on $\langle A,A\rangle$, this fails positive-definiteness. Therefore it is not an inner product.

(c)

$$
\langle f,g\rangle
= f(1)\overline{g(1)}
+ f(i)\overline{g(i)}
+ f(1+i)\overline{g(1+i)}
$$

Since we are over $\mathbb{C}$, we use conjugate symmetry in property (3).

1. Additivity in the first argument
   $$
   \langle f+h,g\rangle
   = (f+h)(1)\overline{g(1)} + (f+h)(i)\overline{g(i)} + (f+h)(1+i)\overline{g(1+i)}
   $$
   splits up as $\langle f,g\rangle + \langle h,g\rangle$.
2. Homogeneity in the first argument  
	   For any $c \in \mathbb{C}$,
	$$
	\begin{aligned}
	\langle c f,g\rangle 
	&= (c f(1))\overline{g(1)} + (c f(i))\overline{g(i)} + (c f(1+i))\overline{g(1+i)}\\
	&= c[f(1)\overline{g(1)} + f(i)\overline{g(i)} + f(1+i)\,\overline{g(1+i)}]\\
	&=c\langle f,g\rangle
	\end{aligned}
	$$
3. Conjugate symmetry
	$$
	\langle f,g\rangle 
	= f(1)\overline{g(1)} + f(i)\overline{g(i)} + f(1+i)\overline{g(1+i)},
	$$
	while
	$$
	\langle g,f\rangle
	= g(1)\overline{f(1)} + g(i)\overline{f(i)} + g(1+i)\overline{f(1+i)}.
	$$
	Taking the complex conjugate of $\langle g,f\rangle$ swaps each factor:
	$$
	\overline{\langle g,f\rangle}
	= \overline{g(1)}f(1) + \overline{g(i)}f(i) + \overline{g(1+i)}f(1+i),
	$$
	which is exactly $f(1)\overline{g(1)} + f(i)\overline{g(i)} + f(1+i)\overline{g(1+i)} = \langle f,g\rangle$
	
	Thus $\langle f,g\rangle = \overline{\langle g,f\rangle}$.
4. Positive-definiteness
   $$
   \langle f,f\rangle
   = |f(1)|^2 +|f(i)|^2 +|f(1+i)|^2
   $$
   This is zero iff $f(1)=f(i)=f(1+i)=0$. A nonzero polynomial of degree $\le2$ cannot have three distinct roots, so that forces $f\equiv0$. Otherwise, the sum of mod-squares is positive.

Hence all four axioms are satisfied for $\langle f,g\rangle$ on $P_2(\mathbb{C})$, so this is a valid inner product.
