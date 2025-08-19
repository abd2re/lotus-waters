## Q5

(a)
ANOVA table
```
Response: Y
          Df Sum Sq Mean Sq F value    Pr(>F)    
X          1 5297.5  5297.5  506.51 2.159e-12 ***
Residuals 14  146.4    10.5                      
---
Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
```

(b)
Null Hypothesis $H_{0}:\beta_1 = 0$: There is no linear association between hardness $Y$ and elapsed time $X$
Alternative Hypothesis $H_{a}:\beta_1 \neq  0$: There is a linear association
F-statistic is 506.51 and p-value: $2.16 \times 10^{-12}$.

Decision Rule: Reject $H_0$ if $\text{Pr}(>F) \leq \alpha$.

Since $\text{Pr}(>F) = 2.16 \times 10^{-12} < 0.01$, we reject $H_0$. This indicates there is a significant linear association between the hardness of the plastic and elapsed time.

(c)
$R^2= 0.9731$ (calculated from $\frac{\text{Regression Sum of Squares}}{\text{Residuals Sum of Squares}}=\frac{5297.5}{5297.5+146.4 }=\frac{5297.5}{5443.9}$), indicating that 97.31% of the variation in hardness $Y$ is explained by the elapsed time $X$.

$r=0.9865$ indicating a strong positive linear correlation between elapsed time and hardness.

--- 
R code
```r
data <- readxl::read_excel("_Plastic_Hardness.xlsx")

model <- lm(Y ~ X, data = data)

anova_table <- anova(model)
print(anova_table)
```
