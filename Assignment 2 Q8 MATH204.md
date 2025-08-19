## Q8

(a)
The 90% confidence interval for the slope is:

$$
(4.1335, 15.8474)
$$

We are 90% confident that the mean service time increases between 4.1335 and 15.8474 minutes for each additional copier serviced. Since the interval is above 0, it suggests a positive association between the number of copiers and the service time.

(b)
Null Hypothesis $H_0 : \beta_1 = 0$: There is no linear association.
Alternative Hypothesis $H_a : \beta_1 \neq 0$: There is a linear association.
P-value: $2 \times 10^{-16}$.

At $\alpha = 0.10$, since $p < 0.10$, we reject $H_0$. 

There is very strong evidence of a linear association between the number of copiers serviced and the time spent.

(c)

Null Hypothesis $H_0:\beta_1 \leq 14$: The mean required time does not increase by more than 14 minutes.
Alternative Hypothesis $H_a:\beta_1 > 14$: The mean required time increases by more than 14 minutes.
T-statistic: $t=\frac{\hat{\beta}_{1}-14}{s_{\hat{\beta}_{1}}}=\frac{15.0352−14​}{0.4831}=2.143$.
P-value: $0.0189$ (computed with R).

At $\alpha = 0.05$:
- Decision Rule: Reject $H_0$ if  $p \leq \alpha$.
- Here, $p = 0.019 < 0.05$.

So we reject $H_0$. There is sufficient evidence to suggest that the mean required time increases by more than 14 minutes for each additional copier serviced.

(d)
The intercept $\beta_0 = -0.5802$ represents the estimated service time when no copiers are serviced $X = 0$.

This value does not have practical meaning because servicing 0 copiers is not realistic.

---
R code

```r
data <- readxl::read_excel("Copier_Maintenance.xlsx")
model <- lm(Y ~ X, data = data)

confint_90 <- confint(model, level = 0.90)

summary_model <- summary(model)

t_stat <- (coef(model)["X"] - 14) / summary_model$coefficients["X", "Std. Error"]
p_value_slope_14 <- pt(t_stat, df = summary_model$df[2], lower.tail = FALSE)

confint_90
summary_model
p_value_slope_14
```