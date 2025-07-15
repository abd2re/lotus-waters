---
tags:
  - MATH204
---
# Multiple linear regression

## Multiple regression models

- Present several different multiple regression models involving:; both quantitative and qualitative independent variables

## Estimating and making inferences about the $\beta$ parameter

First-order model in $k$ quantitative independent (predictor) variables $E(y)=\beta_{0}+\beta_{1}x_{1}+\dots +\beta_{n}x_{n}$ where $x_{1},\dots ,x_{k}$ are all:: quantitative variables that are not functions of other independent variables.
<!--SR:!2025-07-31,109,250-->

$\beta_{i}$ represents:: the slope of the line relating $y$ to $x_{i}$ when all other $x$'s are held fixed.
<!--SR:!2025-06-23,85,250-->

Estimator of $\sigma^{2}$ for a multiple regression model with $k$ independent variables is::$$s^{2}=\frac{\text{SSE}}{n-\text{number of estimated $\beta$ parameters}}=\frac{SSE}{n-(k+1)}$$
<!--SR:!2025-04-21,19,170-->

## Evaluating overall model utility

It is dangerous to conduct $t$-tests on the individual $\beta$ parameters in a first-order linear model for the purpose of determining which independent variables are useful for predicting y and which are not. If you fail to reject $H_{0}: \beta_{i}=0$, several conclusions are possible:
?
1. There is no relationship between $y$ and $x_i$.
2. A straight-line relationship between $y$ and $x$ exists (holding the other $x$’s in the model fixed), but a Type II error occurred.
3. A relationship between $y$ and $x_{i}$ (holding the other $x$’s in the model fixed) exists but is more complex than a straight-line relationship (e.g., a curvilinear relationship may be appropriate)
The most you can say about a $\beta$ parameter test is that there is either sufficient (if you reject $H_0: \beta_i = 0$) or insufficient (if you do not reject $H_0: \beta_i = 0$) evidence of a linear (straight-line) relationship between $y$ and $x_i$
<!--SR:!2025-05-30,64,230-->

$\rightarrow R^{2}=$::$1-\frac{\text{SSE}}{SS_{yy}}=\frac{\text{Explained variability}}{\text{Total variability}}$
<!--SR:!2025-05-02,33,210-->

The multiple coefficient of determination, $R^{2}$ is:: the proportion of variation in $y$ ‘explained’ by all $x$ variables taken together. Never decreases when new $x$ variable is added to model. Only $y$ values determine $SS_{yy}$, disadvantage when comparing models.
<!--SR:!2025-04-16,7,130-->

Adjusted multiple coefficient of determination takes into account:: $n$ and number of parameters. Similar interpretation to $R^{2}$. Is better for multiple coefficient.
<!--SR:!2025-04-24,28,230-->

Adjusted multiple coefficient of determination $R^{2}_{a}$ formula(2)::$$R^{2}_{a}=1-\left[\frac{n-1}{n-(k+1)}\right]\frac{\text{SSE}}{SS_{yy}}=1-\left[\frac{n-1}{n-(k+1)}\right](1-R^{2})$$
<!--SR:!2025-04-16,17,150-->

Testing Global Usefulness of the Model: The analysis of Variance F-Test
?
![[Pasted image 20250204172615.png]]
<!--SR:!2025-04-21,11,130-->

Recommendation for Checking the Utility of a Multiple Regression Model
?
![[Pasted image 20250206141951.png]]![[Pasted image 20250206142012.png]]
<!--SR:!2025-04-16,4,130-->


## Interaction Models

Effect of interaction
?
![[Pasted image 20250206150841.png|700]]![[Pasted image 20250206152315.png|700]]
<!--SR:!2025-04-18,25,173-->

## Quadratic and Other Higher-Order Models

Graphs for Two Quadratic Models
?
![[Pasted image 20250211163108.png]]
![[Pasted image 20250211163115.png|500]]
<!--SR:!2025-05-25,60,228-->

## Qualitative (Dummy) Variable Models

A Model Relating $E(y)$ to a Qualitative Independent Variable with Two Levels
?
![[Pasted image 20250211165924.png]]
<!--SR:!2025-04-22,7,130-->

A Model Relating $E(y)$ to One Qualitative Independent Variable with $k$ Levels
?
![[Pasted image 20250211170019.png]]
<!--SR:!2025-04-26,11,130-->

## Nested Models

Two models are nested if:: one model contains all the terms of the second model and at least one additional term. The more complex of the two models is called the complete (or full) model, and the simpler of the two is called the reduced model.
<!--SR:!2025-04-23,31,200-->

F-Test for Comparing Nested Models
?
![[Pasted image 20250218113852.png]]
![[Pasted image 20250218114254.png]]
![[Pasted image 20250218114301.png]]
<!--SR:!2025-04-16,2,130-->

## Stepwise regression

Forward Stepwise Regression
?
In simple terms, we start with a model containing no predictors (mpg ~ 1) and iteratively add the most statistically significant variables until no improvement is observed. (Backward you remove).
<!--SR:!2025-05-09,37,212-->


# Multiple Regression Diagnostics

A regression residual, $e=\hat{\epsilon}=(y-\hat{y})$ , is defined as:: the difference between an observed $y$ value and its corresponding predicted value.
<!--SR:!2025-05-07,36,212-->

$\sum{e}=$::$0$
<!--SR:!2025-05-12,39,212-->
$\sum{e^{2}}=$::$SSE$
<!--SR:!2025-04-29,31,212-->

A regression outlier is:: a residual that is larger than $3s$ (in absolute value).
<!--SR:!2025-04-27,22,152-->

Multicollinearity exists when:: two or more of the independent variables used in regression are correlated.
<!--SR:!2025-04-26,11,172-->

Using the Correlation Coefficient r to Detect Multicollinearity
?
![[Pasted image 20250228173104.png]]
<!--SR:!2025-05-01,30,192-->

Extrapolation is"" the prediction of y-values of the independent variables that are outside the region in which the model was developed. This is a dangerous practice.![[Pasted image 20250228173215.png]]

Analysis of Residuals
?
1. Detect misspecified model: plot residuals vs. quantitative x (look for trends, e.g., curvilinear trend)
2. Detect nonconstant error variance: plot residuals vs. (look for patterns, e.g., cone shape)
3. Detect nonnormal errors: histogram, stem-leaf, or normal probability plot of residuals (look for strong departures from normality)
4. Identify outliers: residuals greater than 3s in absolute value (investigate outliers before deleting)
<!--SR:!2025-05-09,28,172-->
