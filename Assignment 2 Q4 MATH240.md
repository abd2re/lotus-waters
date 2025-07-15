## Q4

(a)

We want to show

$$
\forall x.\forall y. \left(x<y \Rightarrow \frac{x+y}{2}<y\right)
$$

If $x<y$ then $x+y<y+y=2y$. Dividing both sides by 2 gives $\frac{x+y}{2}<y$. Hence the statement is true.

(b)
The statement to check is  

$$
\forall x.\forall y.\exists z.(zx > y)
$$

We can disprove this by providing a counterexample. Take $x=0$ and $y=1$. Then $zx = z \cdot 0 = 0$. No matter what real $z$ we choose, $0 \not> 1$. Thus the statement fails for $(x,y)=(0,1)$, so it is false.

(c)
We are given

$$
\neg (\exists x.\forall y.(y\neq x \Rightarrow y<x))
$$

We note that $\exists x.\forall y.(y\neq x \Rightarrow y<x)$ would mean "there is a largest real number $x$" that is, every other real $y$ would have to be smaller than $x$. We know no largest real number exists.

To make the negation clearer, we can rewrite it as
$$
\forall x.\exists y.(y \neq x\ \land  y \ge x)
$$
A natural choice is $y = x + k$ for some $k>0$. Then clearly $y \neq x$ ($x+k \neq x \implies k \neq 0$) and $y \ge x$ ($x+k \geq x \implies k>0$). This proves that for every real $x$ there is a (bigger) real $y$, so no largest real exists, and the original statement (that there is a largest real) must be false. Thus

$$
\neg(\exists x.\forall y.(y\neq x \Rightarrow y<x))
$$

is true.