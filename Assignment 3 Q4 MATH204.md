## Q4

(a)
The hypothesized model for recall score $Y$ as a function of viewer group is:  
$$
Y = \beta_0 + \beta_1 \cdot \text{GroupVIOLENT} + \beta_2 \cdot \text{GroupSEX} + \epsilon
$$ 
- Indicator Variables:  
  - $\text{GroupVIOLENT}$:  
    - $1$ if participant is in the violent-content group, $0$ otherwise.  
  - $\text{GroupSEX}$:  
    - $1$ if participant is in the sex-content group, $0$ otherwise.  
- Reference Group: NEUTRAL (both indicators are $0$).  


(b) 
The estimated regression coefficients are:  
$$
\text{Recall} = 3.1667 - 1.0833 \cdot \text{GroupVIOLENT} - 1.4537 \cdot \text{GroupSEX}
$$ 
- Interpretation:  
  - NEUTRAL group mean: $\beta_0 = 3.17$.  
  - VIOLENT group mean: $\beta_0 + \beta_1 = 2.08$.  
  - SEX group mean: $\beta_0 + \beta_2 = 1.71$.  


(c)
- Null Hypothesis ($H_0$): No group differences ($\beta_1 = \beta_2 = 0$).  
- Alternative Hypothesis ($H_a$): At least one group differs.  
- Result:  
  - $F$-statistic $= 20.45$, $p$-value $= 4.36 \times 10^{-9}$.  
  - Conclusion: Reject $H_0$ at $\alpha = 0.01$. The model is statistically useful.  


(d)
Using the $\beta$-estimates:  
- NEUTRAL: $\beta_0 = 3.1667 \approx 3.17$.  
- VIOLENT: $\beta_0 + \beta_1 = 3.1667 - 1.0833 = 2.0834 \approx 2.08$.  
- SEX: $\beta_0 + \beta_2 = 3.1667 - 1.4537 = 1.7130 \approx 1.71$.  

These match the sample means $\bar{y}_V = 2.08$, $\bar{y}_S = 1.71$, and $\bar{y}_N = 3.17$.  

---

```R
data_wide <- read.csv("TVADRECALL.CSV")
data_long <- pivot_longer(data_wide, 
                         cols = c(VIOLENT, SEX, NEUTRAL),
                         names_to = "Group",
                         values_to = "Recall")

data_long$Group <- factor(data_long$Group,
                         levels = c("NEUTRAL", "VIOLENT", "SEX"))

model <- lm(Recall ~ Group, data = data_long)

model_summary <- summary(model)
f_stat <- model_summary$fstatistic
p_value <- pf(f_stat[1], f_stat[2], f_stat[3], lower.tail = FALSE)

beta <- coef(model)
group_means <- c(
  NEUTRAL = beta["(Intercept)"],
  VIOLENT = beta["(Intercept)"] + beta["GroupVIOLENT"],
  SEX = beta["(Intercept)"] + beta["GroupSEX"]
)
```