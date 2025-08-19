## Q2

(a)
The fitted model is:  
$$
\text{RFEWIDTH} = 21087.95 + 108.45 \cdot \text{REDSHIFT} + 557.91 \cdot \text{LINEFLUX} - 340.17 \cdot \text{LUMINOSITY} + 85.68 \cdot \text{AB}_{1450}
$$

(b)
- Coefficient Estimate: $\beta_{\text{LUMINOSITY}} = -340.17$.  
- Interpretation: For every 1-unit increase in line luminosity ($X_3$), the equivalent width ($Y$) decreases by 340.17 units, holding other variables constant.  
- Caveat: This relationship is not statistically significant ($p = 0.3016$), so the effect cannot be generalized to the population.  


(c)
- Null Hypothesis ($H_0$): All coefficients (except intercept) are zero.  
- Alternative Hypothesis ($H_a$): At least one coefficient is non-zero.  
- Result:  
  - $F$-statistic = 51.72, $p$-value = $2.87 \times 10^{-10}$.  
  - Conclusion: Reject $H_0$ ($p < 0.05$). The model is statistically adequate for predicting equivalent width.  


(d)
- Null Hypothesis ($H_0$): The coefficient for REDSHIFT is zero.  
- Alternative Hypothesis ($H_a$): The coefficient for REDSHIFT is non-zero.  
- Result:  
  - $p$-value for REDSHIFT = 0.2359 ($> 0.05$).  
  - Conclusion: Fail to reject $H_0$. REDSHIFT is not a useful linear predictor of equivalent width in this model.  

--- 
```R
model <- lm(RFEWIDTH ~ REDSHIFT + LINEFLUX + LUMINOSITY + AB1450, data = quasar)
model_summary <- summary(model)
f_stat <- model_summary$fstatistic

model_pvalue <- pf(f_stat[1], f_stat[2], f_stat[3], lower.tail = FALSE)

redshift_pvalue <- model_summary$coefficients["REDSHIFT", "Pr(>|t|)"]
```