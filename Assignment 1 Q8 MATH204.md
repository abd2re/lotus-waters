## Q8

(a)
The 99% confidence interval for $\beta_{1}$​(the slope) is $[0.005386,~0.072269]$. (Computed using R, appendix at the end of the question).
This interval does not include zero, which suggests that there is evidence of a linear relationship between $X$ (ACT score) and $Y$ (GPA). The director of admissions would be interested in whether the interval includes zero because it indicates whether there is a significant predictive relationship.

(b)
$H_{0}$: $\beta_{1}=0$ (no linear association)
$H_{a}:\beta_{1}\neq 0$ (linear association)

$t$-statistic: $3.04$
Critical value (two-tailed, $\alpha=0.01$) ($t_{0.005,118}$): $2.62$

So we reject $H_{0}$.
In conclusion, there is sufficient evidence at the $1\%$ significance level to conclude that there is a linear association between the ACT score and GPA at the end of the freshman year.

(c)
$P$-value: $0.0029$
The $P$-value is less than the significance level ($\alpha=0.01$), which supports rejecting $H_{0}$​. This confirms the conclusion reached in part (b), indicating a significant linear relationship between ACT scores and GPA

R-code used
```R
library(readxl)
library(broom)
data <- read_excel("G:/My Drive/mcgill/2/math204/Grade point average.xlsx")

# a
model <- lm(Y ~ X, data = data)
conf_int <- confint(model, level = 0.99)
conf_int

# b
summary_model <- summary(model)
t_stat <- summary_model$coefficients["X", "t value"]
df <- summary_model$df[2]
critical_value <- qt(1 - 0.01 / 2, df = df)
t_stat
critical_value

# c
p_value <- summary_model$coefficients["X", "Pr(>|t|)"]
p_value
```