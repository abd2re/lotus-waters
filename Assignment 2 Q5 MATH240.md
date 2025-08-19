## Q5

Two of the nine points must have an integer coordinate midpoint is to look at parity (even/odd) in each coordinate.  Each point $(x,y,z)$ in the integer grid can be labeled by whether each of $x$, $y$, and $z$ is even or odd.  Since each coordinate has 2 possible parities (even or odd), there are $2^3 = 8$ possible parity classes in total.

By the Pigeonhole Principle, if we place nine points into these eight parity classes, then at least two of the points must lie in the same parity class.  Call these two points $(x_1,y_1,z_1)$ and $(x_2,y_2,z_2)$.  Because they have the same parity in each coordinate, $x_1 + x_2$, $y_1 + y_2$, and $z_1 + z_2$ are all even.  Hence their midpoint
$$
\Bigl(\frac{x_1 + x_2}{2}, \frac{y_1 + y_2}{2}, \frac{z_1 + z_2}{2}\Bigr)
$$
is a point with integer coordinates so it lies on the 3D integer grid.