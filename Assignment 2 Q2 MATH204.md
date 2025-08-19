## Q2

(a)
95% Confidence Interval for Mean OPA (when ACT score = 28):$$(3.061,3.341)$$

This means we are 95% confident that the mean freshman OPA for students with an ACT score of 28 lies within this interval.

(b)
95% Prediction Interval for Mary's OPA (when ACT score = 28): $$(1.959,4.443)$$
This means we are 95% confident that Mary Jones's freshman OPA lies within this range.

(c)
The prediction interval is wider than the confidence interval. This is expected because the prediction interval accounts for both the uncertainty in estimating the mean and the variability of individual observations around the mean.

---

R code

```R
data <- readxl::read_excel("Grade point average.xlsx")

model <- lm(Y ~ X, data = data)

X_target <- data.frame(X = 28)
confidence_interval <- predict(model, newdata = X_target, interval = "confidence", level = 0.95)

prediction_interval <- predict(model, newdata = X_target, interval = "prediction", level = 0.95)

confidence_interval
prediction_interval
```