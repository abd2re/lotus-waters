# Q7

(a)

- Null hypothesis $H_0$: The typical (median) difference is zero, so neither population is systematically larger.
- Alternative hypothesis $H_a$: The median difference is positive, meaning Population 1 is located to the right of Population 2.

(b)
We are given $n=30$ paired differences and the sum of positive ranks $T_+ = 354$. For $n=30$, the expected value of $T_+$ under $H_0$ is

$$
E[T_+] = \frac{n(n+1)}{4} = \frac{30 \cdot 31}{4} = 232.5,
$$

and the variance is

$$
\mathrm{Var}(T_+) = \frac{n(n+1)(2n+1)}{24}
= \frac{30 \cdot 31 \cdot 61}{24}
\approx 2363.75.
$$

Hence, the standard deviation of $T_+$ is

$$
\sqrt{2363.75} \approx 48.6.
$$

We convert $T_+$ to a $z$-score (without continuity correction) via

$$
z
= \frac{T_+ - E[T_+]}{\sqrt{\mathrm{Var}(T_+)}}
= \frac{354 - 232.5}{48.6}
\approx 2.50.
$$

For a one-sided test at $\alpha=0.05$, the critical $z$-value is about +1.645. Since our observed $z \approx 2.50$ exceeds 1.645, we reject $H_0$. The data indicate that Population 1's distribution is significantly shifted to the right of Population 2's.

(c)
With $z \approx 2.50$, the (one-sided) $p$-value is roughly 0.006 (a bit less than 0.01). This is well below 0.05, consistent with rejecting $H_0$.

(d)

1. Paired data are independent of each other .
2. The measurement scale is at least ordinal, so that ranking differences makes sense.
3. Under the null, the distribution of differences is symmetrically centered around zero.

Given those conditions, the Wilcoxon signed-rank procedure is appropriate, and we conclude that Population 1 tends to produce larger (to the right) measurements than Population 2.
