## Q2

**(a)**
From the regression output, the fitted model is:

$$
\hat{\text{DDT}}
 = -108.07
       + 0.0851\,(\text{Mile})
       + 3.77\,(\text{Length})
       - 0.0494\,(\text{Weight})
$$

**(b)**
From the output, the standard deviation of the error is 97.48.

So on average, the predicted DDT level differs from the actual measured level by about 97.48 parts per million.

**(c)**
- Hypothesis
	- $H_0: \beta_1 = \beta_2 = \beta_3 = 0$
	- $H_a:$ at least one $\beta_i \neq 0$
- From the ANOVA table:
  - $F = 1.89$,
  - $p\text{-value} = 0.135$.
- Because $p = 0.135 > 0.05$, we fail to reject $H_0$.

So at the 5% level, we do not have enough evidence to say the model (with all three predictors) is statistically significant.

**(d)**
- We look at the slope for Weight, $\beta_3$, which is estimated as $-0.0494$.
- The two-sided p-value for $\beta_3 \neq 0$ is 0.094.
- Specifically, if we were testing $\beta_3 > 0$, we would note that the estimated slope is actually negative, making it even less likely that $\beta_3$ is truly positive.

Since the two-sided p-value (0.094) is greater than 0.05, we do not reject $H_0$. In fact, the estimate suggests a slight negative association, not a positive one. Hence, there is no evidence that DDT level increases with weight, at least not at the 5% significance level.

**(e)**
- Point estimate for $\beta_3$ (Weight slope): $-0.0494$.
- Standard error (SE): $0.02926$.
- Degrees of freedom for error: $140$. The 95% t-critical value is approximately $1.98$.

A 95% confidence interval is:

$$
\beta_3 \pm t_{0.975} \times \text{SE}
 = -0.0494 \pm 1.98 \times 0.02926
 \approx -0.0494 \pm 0.058.
$$

Numerically, that gives an interval roughly from $-0.107$ to $0.009$.

Since 0 is within this interval, we do not have sufficient evidence to claim the true slope is definitely positive or definitely negative. The actual effect of Weight on DDT could be slightly negative, near zero, or even a small positive value.
