## Q1

(a)
To check that $T_A$ is linear, simply verify the two defining properties of linearity. For any $X,Y\in M_{2\times 2}(F)$ and any scalar $c\in F$:

1.  $$\begin{split}
    T_A(X+Y) &= A(X+Y)-(X+Y)A = AX + AY - XA - YA\\
     &= (AX - XA)+(AY - YA)\\
     &= T_A(X)+T_A(Y)
    \end{split}$$

2.  $$
    T_A(cX) = A(cX)-(cX)A
     = cAX - cXA
     = c\bigl(AX - XA\bigr)
     = cT_A(X)
    $$

Hence $T_A$ is linear.

(b)
We want the matrix of $T_B$ in the basis

$$
\alpha =\bigl\{E_{11}E_{12}E_{21}E_{22}\bigr\}
$$

where $E_{ij}$ is the matrix with a 1 in the $(i,j)$ position and 0 elsewhere. We know that

$$
T_B(X) = BX - XB,
$$
where
$$
B =\begin{pmatrix}1 & 2\\ 2 & 1\end{pmatrix}
$$

- For $E_{11}=\begin{pmatrix}1&0\\0&0\end{pmatrix}$:

  $$
  BE_{11}
   =\begin{pmatrix}1&2\\2&1\end{pmatrix}\begin{pmatrix}1&0\\0&0\end{pmatrix}
   =\begin{pmatrix}1 & 0\\ 2 & 0\end{pmatrix}
   =E_{11}+2E_{21}
  $$

  $$
  E_{11}B
   =\begin{pmatrix}1&0\\0&0\end{pmatrix}\begin{pmatrix}1&2\\2&1\end{pmatrix}
   =\begin{pmatrix}1 & 2\\ 0 & 0\end{pmatrix}
   =E_{11}+2E_{12}
  $$

  Hence

  $$
  T_B(E_{11})
    = BE_{11}-E_{11}B
    =(E_{11}+2E_{21}) -(E_{11}+2E_{12})
    =-2E_{12} +2E_{21}
  $$

  In coordinates relative to $\alpha$ this is $(0,-2,2,0)$.

- For $E_{12}=\begin{pmatrix}0&1\\0&0\end{pmatrix}$:

  $$
  BE_{12}
   =\begin{pmatrix}1&2\\2&1\end{pmatrix}\begin{pmatrix}0&1\\0&0\end{pmatrix}
   =\begin{pmatrix}0 & 1\\ 0 & 2\end{pmatrix}
   =E_{12}+2E_{22}
  $$

  $$
  E_{12}B
   =\begin{pmatrix}0&1\\0&0\end{pmatrix}\begin{pmatrix}1&2\\2&1\end{pmatrix}
   =\begin{pmatrix}2 & 1\\ 0 & 0\end{pmatrix}
   =2E_{11} + E_{12}
  $$

  Hence

  $$
  T_B(E_{12})
   = BE_{12}-E_{12}B
   =(E_{12}+2E_{22}) -(2E_{11}+E_{12})
   =-2E_{11}+2E_{22}
  $$

  In coordinates: $(-2,0,0,2)$.

- For $E_{21}=\begin{pmatrix}0&0\\1&0\end{pmatrix}$:

  $$
  BE_{21}
   =\begin{pmatrix}1&2\\2&1\end{pmatrix}\begin{pmatrix}0&0\\1&0\end{pmatrix}
   =\begin{pmatrix}2 & 0\\ 1 & 0\end{pmatrix}
   =2E_{11}+ E_{21}
  $$

  $$
  E_{21}B
   =\begin{pmatrix}0&0\\1&0\end{pmatrix}\begin{pmatrix}1&2\\2&1\end{pmatrix}
   =\begin{pmatrix}0 & 0\\ 1 & 2\end{pmatrix}
   =E_{21} + 2E_{22}
  $$

  Hence

  $$
  T_B(E_{21})
   = (2E_{11}+E_{21}) - (E_{21}+2E_{22})
   =2E_{11}-2E_{22}
  $$

  Coordinates: $(2,0,0,-2)$.

- For $E_{22}=\begin{pmatrix}0&0\\0&1\end{pmatrix}$:
  $$
  BE_{22}
   =\begin{pmatrix}1&2\\2&1\end{pmatrix}\begin{pmatrix}0&0\\0&1\end{pmatrix}
   =\begin{pmatrix}0 & 2\\ 0 & 1\end{pmatrix}
   =2E_{12}+E_{22}
  $$
  $$
  E_{22}B
   =\begin{pmatrix}0&0\\0&1\end{pmatrix}\begin{pmatrix}1&2\\2&1\end{pmatrix}
   =\begin{pmatrix}0 & 0\\ 2 & 1\end{pmatrix}
   =2E_{21}+E_{22}
  $$
  Hence
  $$
  T_B(E_{22})
   = (2E_{12}+E_{22}) -(2E_{21}+E_{22})
   = 2E_{12}-2E_{21}
  $$
  Coordinates: $(0,2,-2,0)$.

Putting these four coordinate‐vectors as columns gives
$$
[T_B]_{\alpha}^{\alpha}
 =
 \begin{pmatrix}
   0 & -2 & 2 & \phantom{-}0\\
  -2 & \phantom{-}0 & 0 & 2\\
   2 & \phantom{-}0 & 0 & -2\\
   0 & 2  & -2 & 0
 \end{pmatrix}
$$

(c)
The kernel of $T_B$ is

$$
\ker(T_B) =\{X\in M_{2\times 2}(F)\mid T_B(X)=0\}
 =\{X\mid BX = XB\}
$$

That is, $\ker(T_B)$ is precisely the set of matrices that commute with $B$. Both $I$ (identity matrix) and $B$ itself commute with $B$, and since

$$
T_B(I) =BI - IB = 0,
 \quad
T_B(B) =BB - BB=0,
$$

we see that $I$ and $B$ lie in $\ker(T_B)$ and that they are linearly independent. Thus a suitable basis for $\ker(T_B)$ is $\{I,B\}$.

(d)
From the above we see that

$$
\ker(T_B) =\{aI + bB \mid a,b \in F\}
$$

But $\ker(T_B)$ _is_ exactly the set of all matrices $X$ that commute with $B$. Therefore

$$
\{X\in M_{2\times 2}(F)\mid BX = XB\}
 =
 \{aI + bB \mid a,b\in F\}
$$

The matrices that commute with $B$ are all linear combinations of $I$ and $B$.