## Q1

(a)
The estimated regression function is $$\hat{Y}=-0.5802+15.0352X$$

(b) 
Plot of estimated regression function
![[Pasted image 20250207142228.png|750]]
The line fits the data well, as indicated by the high $R^{2}$ value ($0.9575$).

(c)
The intercept ($\hat{\beta}_{0}=-0.5802$) represents the estimated total time spent when no copiers are serviced ($X=0$). While this value exists mathematically, it may not provide meaningful information since servicing 0 doesn't make sense.

(d)
The estimated mean service time when $X=5$ copiers are serviced is $\approx 74.59$ minutes.

--- 

R code used
```R
data <- readxl::read_excel("Copier_Maintenance.xlsx")

model <- lm(Y ~ X, data = data)

summary(model)

coefficients <- coef(model)

x_values <- seq(min(data$X), max(data$X), length.out = 100)
y_values <- coefficients[1] + coefficients[2] * x_values

plot(data$X, data$Y,
     xlab = "Number of Copiers Serviced (X)", ylab = "Total Minutes Spent (Y)",
     pch = 16, col = "blue", xlim = range(data$X), ylim = range(data$Y))
lines(x_values, y_values, col = "red", lwd = 2)

point_estimate <- predict(model, newdata = data.frame(X = 5))
point_estimate

```