## Q7

(a)
![[Pasted image 20250119204448.png|center|500]]
There is a clear positive linear trend, indicating that as the YouTube advertising budget increases, sales tend to rise proportionally. However, the variability in sales also increases as the advertising budget grows, with data points becoming more dispersed at higher budget levels. This suggests that while the overall relationship is strong and positive, the predictability of sales becomes less consistent as the advertising budget increases. This increasing variability could imply the influence of additional factors at higher budget levels.

(b)
![[Pasted image 20250119205247.png|center|500]]
Intercept: $8.43911225895323\approx8.440$
Slope: $0.0475366404330198\approx0.04754$

(c)
The intercept provides a baseline level of sales without advertising which is approximately 8.440 thousand of dollars.
The slope highlights the positive relationship between the advertising budget and sales.

(d)
$\sigma^{2}=15.2911315136826\approx15.29$

R code used for the question
```R
# a
plot(marketing$youtube, marketing$sales, 
     main = "Sales vs YouTube Advertising Budget",
     xlab = "YouTube Advertising Budget (in $1000s)", 
     ylab = "Sales (units)",
     col = "blue")


# b, c
model <- lm(sales ~ youtube, data = marketing)
abline(model, col = "red")

coef(model)

# d
residuals <- residuals(model)

n <- nrow(marketing)       # Number of observations
sigma_squared <- sum(residuals^2) / (n - 2)
sigma_squared
```