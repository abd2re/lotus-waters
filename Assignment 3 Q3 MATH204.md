# Q3

- Null Hypothesis ($H_0$): All coefficients are zero ($\beta_1 = \beta_2 = \ldots = \beta_{18} = 0$).  
- Alternative Hypothesis ($H_a$): At least one coefficient is non-zero.  
 
The formula for the F-statistic is:  
$$
F = \frac{R^2 / k}{(1 - R^2) / (n - k - 1)}
$$  
Where:  
- $R^2 = 0.95$,  
- $k = 18$ (number of predictors),  
- $n = 20$ (sample size).  

$$
F = \frac{0.95 / 18}{(1 - 0.95) / (20 - 18 - 1)} = \frac{0.05278}{0.05 / 1} = 1.0556
$$  

- Degrees of freedom: $(k, n - k - 1) = (18, 1)$.  
- Critical F-value at $\alpha = 0.05$: $F_{0.05}(18, 1) = 4.41$.  

Since $1.0556 < 4.41$, we fail to reject $H_0$.  

At $\alpha = 0.05$, there is insufficient evidence to conclude that the model is useful. The high $R^2 = 0.95$ is likely due to overfitting caused by too few observations ($n = 20$) relative to the number of predictors ($k = 18$).  