## Q6

(a)
![[Pasted image 20250119195314.png|center|500]]
The scatter plot is showing a generally positive trend. As solar radiation increases, ozone tend to rise, suggesting a positive correlation between the two variables. However, the data points are widely dispersed, indicating significant variability or noise in the relationship. This spread suggests that while solar radiation influences the ozone's air quality, other factors might also play a role. Additionally, the relationship appears to be non-linear, with the variability increasing at higher levels of solar radiation. Overall, there seems to be a positive but weak to moderate correlation, potentially with non-linear characteristics.

(b)
![[Pasted image 20250119195119.png|center|500]]
Intercept: $18.5987277720233\approx18.60$
Slope: $0.127165271647512\approx0.1272$

(c)

Sum of the residuals = $1.03972386256146^{-13}\approx0$
Sum of residuals times estimated value = $1.07505115920503^{-11}\approx0$

R code used for all computations:
```R
# a
plot(airquality$Solar.R, airquality$Ozone, 
     xlab = "Solar Radiation", ylab = "Ozone", 
     main = "Ozone vs. Solar Radiation",
     col="blue"
     )
     
# b
model <- lm(Ozone ~ Solar.R, data = airquality)
abline(model, col = "red")
coefficients(model)

# c
residuals <- model$residuals

sum_residuals <- sum(residuals)

estimated <- model$fitted.values

sum_residuals_estimated <- sum(residuals * estimated)

sum_residuals
sum_residuals_estimated
```