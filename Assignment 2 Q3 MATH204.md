## Q3

(a)
ANOVA table
```
Response: Y
           Df Sum Sq Mean Sq F value   Pr(>F)   
X           1  3.588  3.5878  9.2402 0.002917 **
Residuals 118 45.818  0.3883                    
--- 
Signif. codes: 0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
```
(b)
Null Hypothesis $H_0:\beta_{1}=0$: The slope $\beta_1$ is zero, meaning $X$ (ACT score) does not predict $Y$ (OPA).
Alternative Hypothesis $H_{a}:\beta_{1}\neq 0$: The slope $\beta_1$ is not zero.

The F-statistic is $9.2402$.

Decision rule: Reject $H_0$ if $\text{Pr}(>F) \leq \alpha = 0.01$.

Since $\text{Pr}(>F) = 0.002917 < 0.01$, we reject $H_0$. This indicates that the ACT score significantly predicts the OPA at the 0.01 significance level.

(c)
$R^2= 0.0726$ (calculated from $\frac{\text{Regression Sum of Squares}}{\text{Total Sum of Squares}}=\frac{3.588}{3.588+45.818}=\frac{3.588}{49.406}$).

$r=0.2695$ (calculated as $\sqrt{R^2}$ with the positive sign due to the positive slope of the regression line).

(d)
$R^2$ represents the proportion of variation in the response variable $Y$ explained by the predictor $X$. In this case, 7.26% of the variation in OPA is explained by the ACT score. This is useful for understanding the strength of the model overall and $r$ represents the strength and direction of the linear relationship between $X$ and $Y$. Here, $r = 0.2695$ indicates a weak positive correlation.

$R^2$ is better for explaining the overall fit of the model, while $r$ is more relevant for understanding the relationship between variables. In operational terms, $R^2$ often has clearer practical relevance in regression contexts.

---

R code

```R
data <- readxl::read_excel("Grade point average.xlsx")

model <- lm(Y ~ X, data = data)

anova_table <- anova(model)
print(anova_table)
```