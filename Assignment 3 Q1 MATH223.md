## Q1

Any function in the set can be rewritten using the standard trigonometric identities:
$$
\sin(x + c) = \sin x \cos c + \cos x \sin c
$$
and
$$
\cos(x + d) = \cos x \cos d - \sin x \sin d.
$$
So a typical element
$$
a \sin(x + c) + b \cos(x + d)
$$
becomes
$$a \sin x \cos c + a \cos x \sin c +b \cos x \cos d - b \sin x \sin d$$
$$
[a \cos c - b \sin d]\,\sin x 
\;+\;
[a \sin c + b \cos d]\,\cos x.
$$
This shows that every function of the given form is just a linear combination of $\sin x$ and $\cos x$. It follows that $S$ is spanned by $\sin x$ and $\cos x$, and these two functions are linearly independent. Hence $S$ is exactly the two‐dimensional subspace $\mathrm{span}\{\sin x,\cos x\}$, and a natural basis is $\{\sin x,\cos x\}.$

To see that $S$ is a subspace, we notice that the sum of two such functions can also be written as a linear combination of $\sin x$ and $\cos x$, and any scalar multiple of such a function remains in the span of $\sin x$ and $\cos x$.