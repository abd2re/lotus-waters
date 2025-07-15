## Q1

To show that $T$ is the differentiation operator, it suffices to check that $T$ and $\tfrac{d}{dx}$ agree on a basis and then use linearity. Concretely, let us check $T$ on each of the basis vectors in

$$
\beta =\{1,1+x,1+x+x^2,1+x+x^2+x^3\}
$$

1. $T(1)$.  
   The first column of $\bigl[T\bigr]_{\beta}^{\beta}$ gives the coordinates of $T(1)$ relative to $\beta$. Looking at the given matrix,

   $$
   \bigl[T\bigr]_{\beta}^{\beta}
   =
   \begin{pmatrix}
   0 & 1 & -1 & -1 \\
   0 & 0 & 2  & -1 \\
   0 & 0 & 0  &  3 \\
   0 & 0 & 0  &  0
   \end{pmatrix},
   $$

   the first column is $\begin{pmatrix}0\\0\\0\\0\end{pmatrix}$, which means

   $$
   T(1) = 0\cdot 1 + 0\cdot (1+x) + 0\cdot (1+x+x^2) + 0\cdot (1+x+x^2+x^3)
   = 0
   $$

   Since $\frac{d}{dx}(1)=0$, this matches the action of the derivative.

2. $T(1+x)$.  
   The second column is $\begin{pmatrix}1\\0\\0\\0\end{pmatrix}$. Hence

   $$
   T(1+x)
   = 1\cdot 1 + 0\cdot (1+x) + 0\cdot (1+x+x^2) + 0\cdot (1+x+x^2+x^3)
   = 1
   $$

   This matches $\frac{d}{dx}(1+x)=1$

3. $T(1+x+x^2)$.  
   The third column is $\begin{pmatrix}-1\\2\\0\\0\end{pmatrix}$, so

   $$
   T(1+x+x^2)
   =
   -1\cdot 1
   +2\cdot(1+x)
   +0\cdot(1+x+x^2)
   +0\cdot(1+x+x^2+x^3)
   = -1 + (2 + 2x)
   = 1 + 2x
   $$

   Again, that is exactly $\frac{d}{dx}(1+x+x^2) = 0 + 1 + 2x$

4. $T(1+x+x^2+x^3)$.  
   The fourth column is $\begin{pmatrix}-1\\-1\\3\\0\end{pmatrix}$. Hence
   $$
   T(1+x+x^2+x^3)
   =
   -1\cdot 1
   + (-1)\cdot(1+x)
   + 3\cdot(1+x+x^2)
   + 0\cdot(1+x+x^2+x^3)
   $$
   A quick expansion shows this is $1+2x+3x^2$, which is precisely the derivative of $1+x+x^2+x^3$.

Because $T$ and the usual derivative $\tfrac{d}{dx}$ agree on the basis $\beta$ and both are linear operators, they must agree on all polynomials in $P_3(\mathbb{R})$. Consequently, $T(f) = f'$ for every polynomial $f$ of degree at most 3.


Thus $T$ is the differentiation operator.
