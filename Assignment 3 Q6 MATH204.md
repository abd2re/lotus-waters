## Q6

(a) 
The hypothesized model for desire to undergo cosmetic surgery ($Y$) is:  
$$
Y = \beta_0 + \beta_1 \text{GENDER} + \beta_2 \text{SELFESTM} + \beta_3 \text{BODYSAT} + \beta_4 \text{IMPREAL} + \beta_5 (\text{GENDER} \cdot \text{IMPREAL}) + \beta_6 (\text{SELFESTM} \cdot \text{IMPREAL}) + \beta_7 (\text{BODYSAT} \cdot \text{IMPREAL}) + \epsilon
$$ 
This includes interaction terms between impression of reality TV ($X_4$) and each of the other predictors.  

(b)  
The estimated coefficients are:  
$$
\begin{align}
\text{Intercept} &= 13.09, \\
\text{GENDER} &= -1.89, \\
\text{SELFESTM} &= -0.09, \\
\text{BODYSAT} &= 0.13, \\
\text{IMPREAL} &= 0.75, \\
\text{GENDER:IMPREAL} &= -0.06, \\
\text{SELFESTM:IMPREAL} &= 0.01, \\
\text{BODYSAT:IMPREAL} &= -0.11.
\end{align}
$$ 
None of the interaction terms are statistically significant (all $p$-values > 0.05).  

(c) 
- F-statistic: 24.40, $p$-value $= 1.72 \times 10^{-22}$.  
- Conclusion: The model is statistically useful ($p < 0.05$) for predicting desire for cosmetic surgery.  

(d)
- Null Hypothesis ($H_0$): $\beta_5 = \beta_6 = \beta_7 = 0$ (no interaction effects).  
- Alternative Hypothesis ($H_a$): At least one interaction coefficient is non-zero.  

(e) 
- Test Result:  
  - $F$-statistic $= 1.74$, $p$-value $= 0.1614$.  
  - Conclusion: Fail to reject $H_0$ at $\alpha = 0.01$. There is no evidence that interactions improve the model.  
---

```R
full_model <- lm(DESIRE ~ GENDER + SELFESTM + BODYSAT + IMPREAL +
                  GENDER:IMPREAL + SELFESTM:IMPREAL + BODYSAT:IMPREAL, 
                data = data)

model_summary <- summary(full_model)
f_stat <- model_summary$fstatistic
p_value <- pf(f_stat[1], f_stat[2], f_stat[3], lower.tail = FALSE)

reduced_model <- lm(DESIRE ~ GENDER + SELFESTM + BODYSAT + IMPREAL, data = data)
nested_test <- anova(reduced_model, full_model)
```