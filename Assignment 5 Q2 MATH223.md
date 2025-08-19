## Q2

First, note that $T_B$ is linear because for any $X,Y\in M_{n\times n}(F)$ and any scalar $c\in F$,
$$
T_B(X+Y) =B^{-1}(X+Y)B =B^{-1}XB + B^{-1}YB 
        =T_B(X)+T_B(Y)
$$
and
$$
T_B(cX)=B^{-1}(cX)B =c\bigl(B^{-1}XB\bigr) =cT_B(X)
$$
Hence $T_B$ is a linear transformation.

Next, to show $T_B$ is bijective, observe:

- Injectivity: If $T_B(X)=0$, then
  $$
  B^{-1} XB =0
  \implies
  XB =B0 =0
  \implies
  X =0
  $$
  (multiplying by $B$ on the left and $B^{-1}$ on the right shows $X=0$)  
  Thus the only matrix taken to $0$ by $T_B$ is the zero matrix, so $T_B$ is injective.

- Surjectivity: Given any matrix $Y\in M_{n\times n}(F)$, we can solve $T_B(X)=Y$ by setting
  $$
    B^{-1}XB =Y
    \implies
    X = BYB^{-1}.
  $$
  That $X$ indeed lies in $M_{n\times n}(F)$, so every matrix $Y$ has a preimage under $T_B$.  Hence $T_B$ is surjective.

Because $T_B$ is a linear map that is both injective and surjective, it is an isomorphism of the vector space $M_{n\times n}(F)$.