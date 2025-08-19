## Q1

(a)  
The fitted quadratic model is:  
$$\text{Years} = -8.93 + 0.704 \cdot \text{Age} - 0.00341 \cdot \text{Age}^2$$ 
(b)
- Null Hypothesis ($H_0$): The model has no predictive utility (all coefficients are zero).  
- Alternative Hypothesis ($H_a$): At least one coefficient is non-zero.  
- Result:  
  - $F$-statistic = 13.15, $p$-value = $5.49 \times 10^{-5}$.  
  - Conclusion: Reject $H_0$ at $\alpha = 0.01$. The quadratic model is statistically useful for predicting years of shopping.  


(c)
- Null Hypothesis ($H_0$): The linear model is sufficient (quadratic term adds no improvement).  
- Alternative Hypothesis ($H_a$): The quadratic model is significantly better.  
- Result:  
  - ANOVA comparison $p$-value = 0.6151 ($> 0.01$).  
  - Conclusion: Fail to reject $H_0$. The quadratic term does not significantly improve the model. The linear model is sufficient.  

---

```R

quad_model <- lm(YEARS ~ AGE + I(AGE^2), data = data)

quad_summary <- summary(quad_model)
f_stat <- quad_summary$fstatistic
p_value <- pf(f_stat[1], f_stat[2], f_stat[3], lower.tail = FALSE)

linear_model <- lm(YEARS ~ AGE, data = data)
model_comparison <- anova(linear_model, quad_model)

```