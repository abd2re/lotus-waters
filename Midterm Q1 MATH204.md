## Q1

**(a)**
The regression output tells us the fitted model (with labor hours as the dependent variable) is:
$$
\hat{\text{Labor}} = 132 + 2.73\,(\text{Pounds}) + 0.0472\,(\text{Units}) - 2.59\,(\text{Weight}).
$$

That is the least-squares prediction equation obtained from the data.

**(b)**
- Hypothesis:
  - $H_0$: All slope coefficients are 0 $(\beta_1 = \beta_2 = \beta_3 = 0)$.
  - $H_a$: At least one slope coefficient $\neq 0$.
- Test statistic & p-value: From the ANOVA table, the F-value is 17.87 and the p-value is 0.000.
- Decision: Because $p = 0.000 < 0.05$, we reject $H_0$.

So there is strong evidence that at least one of the predictors (Pounds, Units, Weight) helps explain variation in labor hours, so the overall regression model is useful.

**(c)**
Here, $\beta_2$ is the slope for the "Units" predictor.

- Coefficient for Units: 0.04722
- Standard error: 0.09335
- t-value: 0.51
- p-value: 0.620

Because $p = 0.620 > 0.05$, we fail to reject $H_0$. So we do not have evidence that "Units" has a statistically significant impact on labor hours. Its effect appears small or negligible given these data.

**(d)**
From the output, $R^2 = 77\%$.

So about 77% of the variation in labor hours is explained by the combined linear effects of Pounds, Units, and Weight. In other words, this model accounts for most of the variability in the labor-hour requirement.

**(e)**
From the fitted equation, the coefficient on "Weight" (which is taken here as $X_3$) is $-2.59$.

- This means that if "Weight" goes up by 1 pound, the predicted labor changes by $-2.59$ hours.
- At \$7.50 per hour, the corresponding change in cost is:

$$
-2.59 \text{ hours} \times \$7.50 \text{ per hour} = -\$19.43.
$$

So the company would spend about \$19.43 less per week in labor costs (on average) when weight per shipment increases from 20 to 21 pounds, holding the other variables constant.

**(f)**
The standard error of the estimate, $S$, is 9.81. Roughly speaking, the typical prediction error for labor hours is about $\pm 10$ hours. That is how precise (or imprecise) our labor-hour predictions are likely to be.

**(g)**
No. Regression analysis identifies associations (correlations) but does not by itself prove causation. To establish causality, one usually needs either an experimental design or additional evidence. Simply finding a significant relationship in a regression does not guarantee one variable causes changes in another.