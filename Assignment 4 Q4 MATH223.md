## Q4

(a)
We first construct the four Lagrange‐basis polynomials for the $x$‐values $\{1,2,3,4\}$. By definition,

$$
l_j(x) = \prod_{m=1, m\neq j}^{4} \,\frac{x - x_m}{x_j - x_m}
$$

so in this case:

1.  $$
    l_1(x)=\frac{(x-2)(x-3)(x-4)}{(1-2)(1-3)(1-4)}
    =\frac{(x-2)(x-3)(x-4)}{(-1)(-2)(-3)}
    =\frac{(x-2)(x-3)(x-4)}{-6}.
    $$

    Expanding the numerator $(x-2)(x-3) = x^2 - 5x + 6$ and then multiplying by $(x-4)$ gives

    $$
    (x^2 - 5x + 6)(x-4) = x^3 - 9x^2 + 26x - 24.
    $$

    Dividing by $-6$ yields

    $$
    l_1(x)
    =
    -\tfrac{1}{6}\,x^3 +\tfrac{3}{2}\,x^2
    -\tfrac{13}{3}\,x +4.
    $$

2.  $$
    l_2(x)=\frac{(x-1)(x-3)(x-4)}{(2-1)(2-3)(2-4)}
    =\frac{(x-1)(x-3)(x-4)}{(1)(-1)(-2)}
    =\frac{(x-1)(x-3)(x-4)}{2}.
    $$

    Expanding $(x-1)(x-3) = x^2 - 4x + 3$, then multiplying by $(x-4)$ gives

    $$
    (x^2 - 4x + 3)(x-4) = x^3 - 8x^2 + 19x - 12.
    $$

    Dividing by $2$ gives

    $$
    l_2(x)
    =
    \tfrac12\,x^3 -4\,x^2 +\tfrac{19}{2}\,x -6.
    $$

3.  $$
    l_3(x)=\frac{(x-1)(x-2)(x-4)}{(3-1)(3-2)(3-4)}
    =\frac{(x-1)(x-2)(x-4)}{(2)(1)(-1)}
    =\frac{(x-1)(x-2)(x-4)}{-2}.
    $$

    Expand $(x-1)(x-2) = x^2 - 3x + 2$, then multiply by $(x-4)$ to get

    $$
    (x^2 - 3x + 2)(x - 4) = x^3 - 7x^2 + 14x - 8.
    $$

    Dividing by $-2$ yields

    $$
    l_3(x)
    =
    -\tfrac12\,x^3 +\tfrac72\,x^2 -7\,x +4.
    $$

4.  $$
    l_4(x)=\frac{(x-1)(x-2)(x-3)}{(4-1)(4-2)(4-3)}
    =\frac{(x-1)(x-2)(x-3)}{(3)(2)(1)}
    =\frac{(x-1)(x-2)(x-3)}{6}.
    $$
    Expand $(x-1)(x-2) = x^2 - 3x + 2$, then multiply by $(x-3)$ to get
    $$
    (x^2 - 3x + 2)(x - 3) = x^3 - 6x^2 + 11x - 6.
    $$
    Dividing by $6$ gives
    $$
    l_4(x)
    =
    \tfrac{1}{6}\,x^3 -x^2 +\tfrac{11}{6}\,x -1.
    $$

These are the Lagrange basis polynomials in the form $a x^3 + b x^2 + c x + d$.

(b)
To find the cubic $p(x)$ that passes through $(1,6)$, $(2,-8)$, $(3,2)$, and $(4,12)$, we use

$$
p(x) = \sum_{j=1}^{4} y_j\,l_j(x),
$$

where $y_1=6$, $y_2=-8$, $y_3=2$, and $y_4=12$. That is,

$$
p(x)
=
6\,l_1(x)-8\,l_2(x)+2\,l_3(x)+12\,l_4(x).
$$

Substitute and collect like terms of $x^3$, $x^2$, $x$, and the constant. After simplification, one obtains

$$
p(x)
=
-4\,x^3
+36\,x^2
-94\,x
+68.
$$

This polynomial indeed satisfies $p(1)=6$, $p(2)=-8$, $p(3)=2$, and $p(4)=12$.

(c)

Using desmos, we get this plot for $y=p(x)$
![[Pasted image 20250209181917.png|800]]