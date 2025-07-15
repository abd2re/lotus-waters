---
tags:
  - MATH204
---
# Simple linear regression

Regression analysis is:: a statistical methodology that utilizes the relation between two or more **quantitative variables** so that a response or outcome variable can be predicted from the other, or others.
<!--SR:!2025-04-27,54,210-->

A functional relation between two variables is expressed by a mathematical formula. If $X$ denotes the independent variable and $Y$ the dependent variable, a functional relation is of the form:: $$Y=f(X)$$
<!--SR:!2025-07-04,118,290-->

- Deterministic models are models that:: hypothesize exact relationships and are suitable when prediction error is negligible. The form is $y=\beta_{0}+\beta_{1}x$ for linear regression.
<!--SR:!2025-07-05,107,250-->
- Probabilistic models are models that:: hypothesize two components: **deterministic** and **random error**.
<!--SR:!2025-05-06,58,210-->

General form of probabilistic models is::$$y=\text{Deterministic component} + \text{Random error}$$ where $y$ is the variable interest.
<!--SR:!2025-05-08,77,270-->

- The expected value of the random error $E(\epsilon)$ equals:: 0 (general assumption).
<!--SR:!2025-07-14,127,290-->
- If $y=\beta_{0}+\beta_{1}x+\epsilon$, $E(y)=$::$\beta_{0}+\beta_{1}x$ (the mean value of a probabilistic model is its deterministic component because $E(\epsilon)=0$).
<!--SR:!2025-07-22,118,250-->

Deterministic and Probabilistic Graphs example
?
![[image-20250108164307831.png|center]]
<!--SR:!2025-05-14,80,270-->


## A First-Order (Straight Line) Probabilistic Model

Formula and explanation:
?
$$y=\beta_{0}+\beta_{1}x+\epsilon$$
where
- $y$ = Dependent or response variable (variable to be modeled)
- $x$ = Independent or predictor variable (variable used as a predictor of y)
- $E(y)=\beta_{0}+\beta_{1}x$ = Deterministic component
- $\epsilon$ =  Random error component
<!--SR:!2025-08-18,134,250-->

When describing the line of a first-order probabilistic model, it is important to:: use $E(y)$(the deterministic component) and not $y$.
<!--SR:!2025-05-27,43,150-->

Five steps to build a first-order probabilistic model are:
?
1. Hypothesize the deterministic component of the model that relates the mean, $E(y)$, to the independent variable $x$.
2. Use the sample data to estimate unknown parameters in the model.
3. Specify the probability distribution of the random error term and estimate the standard deviation of this distribution.
4. Statistically evaluate the usefulness of the model.
5. When satisfied that the model is useful, use it for prediction, estimation, and other purposes.
<!--SR:!2025-04-27,21,130-->


## Fitting the model: least squares approach

The least squares line $\hat{y}=\hat{\beta}_{0}+\hat{\beta}_{1}x$ is one that has the following two properties:
?
- The sum of their errors equals 0, the mean error is null
- The sum of squared errors (SSE) is smaller than for any other straight-line model, the error variance is minimum.
Important to use $\hat{y}$ (estimator of $E(y)$) and not $E(y)$ because we're just estimating the least squares lines.
<!--SR:!2025-05-13,56,205-->

The "hats": $\hat{}$ , indicate:: that the derived values are estimates
<!--SR:!2025-05-02,63,245-->


- Slope: $\hat{\beta}_{1}=$::$\frac{\text{SS}_{xy}}{\text{SS}_{xx}}$
<!--SR:!2025-04-23,18,145-->
- $y$-intercept: $\hat{\beta}_{0}=$::$\bar{y}-\hat{\beta}_{1}\bar{x}$
<!--SR:!2025-04-17,2,130-->
- $n=$ sample size

$\rightarrow SS_{xy}=$(3)::$\sum{(x_{i}-\bar{x})(y_{i}-\bar{y})}=\sum{x_{i}y_{i}}-\frac{(\sum{x_{i}})(\sum{y_{i}})}{n}=\sum{x_{i}y_{i}}-n \bar{x}\bar{y}$
<!--SR:!2025-04-19,49,227-->
$\rightarrow SS_{xx}=$(3)::$\sum{(x_{i}-\bar{x})^{2}}=\sum{x_{i}^{2}}-\frac{(\sum{x_{i}})^{2}}{n}=\sum{x_{i}^{2}}-n \bar{x}^{2}$
<!--SR:!2025-04-18,8,167-->

The sum of squared errors (SSE) formula is (2)::$$\text{SSE}=\sum(y_{i}-\hat{y}_{i})^{2}=\sum{[y_{i}-(\hat{\beta}_{0}+\hat{\beta}_{1}x_{i})]^{2}}$$$$\text{SSE}=\text{SS}_{yy}-\hat{\beta}_{1}\text{SS}_{xy}$$
<!--SR:!2025-04-14,2,150-->

The value of $\hat{B}_{0}$ and $\hat{B}_{1}$ is only meaningful:: if $x$-values are within the range of the sample data. (avoid extrapolation)
<!--SR:!2025-06-11,78,225-->

## Model assumptions

The basics assumptions of the probability distribution of the random error are:
?
1. The mean of the probability distribution of $\epsilon$ is 0. $E(\epsilon)=0$.
2. The variance of the probability distribution of $\epsilon$ is constant for all settings of the independent variable $x$. $\forall x:~\text{Var}(\epsilon)=\sigma^{2}$.
3. The probability distribution of $\epsilon$ is normal. $\epsilon\sim N(0,\sigma^{2})$.
4. The values of $\epsilon$ associated with any two observed values of $y$ are independent–that is, the value of $\epsilon$ associated with one value of $y$ has no effect on the values of $\epsilon$ associated with other $y$ values.
<!--SR:!2025-04-23,37,182-->

Estimated standard error of the regression model $s=$::$\sqrt{\frac{\text{SSE}}{\text{deg. of freedom for error}}}=\sqrt{\frac{\text{SSE}}{n-2}}$
<!--SR:!2025-05-03,48,182-->


## Assessing the utility of the model: making inferences about the slope $\beta_{1}$

If we make the four assumptions about $\epsilon$, the sampling distribution of the least squares estimator $\hat{\beta}_{1}$ of the slope will be normal with mean $\beta_{1}$ (the true slope) and standard deviation::$$\sigma_{\hat{\beta}_{1}}=\frac{\sigma}{\sqrt{\text{SS}_{xx}}}$$
<!--SR:!2025-04-27,49,216-->

$\rightarrow \hat{\beta}_{1}\sim$::$N(\beta_{1},~\frac{\sigma^{2}}{\text{SS}_{xx}})$
<!--SR:!2025-04-20,31,162-->
$\rightarrow s_{\hat{\beta}_{1}}=$::$\frac{s}{\sqrt{\text{SS}_{xx}}}$ where $s$ is the estimated standard error of the regression model.
<!--SR:!2025-04-17,9,130-->


Test statistic $t_{c}=$::$\frac{\hat{\beta}_{1}-\beta_{1}}{s_{\hat{\beta}_{1}}}$
<!--SR:!2025-04-17,3,130-->

Test of model utility for simple linear regression table with rejection and p-value formulas:
?
![[Pasted image 20250116154831.png]]
<!--SR:!2025-04-25,11,130-->

Almost all statistical computer software packages report a two-tailed $p$-value for each of the $\beta$ parameters in the regression mode. If you want to conduct a one-tailed test of hypothesis, you will need to adjust the $p$-value reported on the printout as follows:
?
![[Pasted image 20250116154929.png|475]]
<!--SR:!2025-04-28,47,182-->

Confidence interval for $\beta_{1}\rightarrow$::$\hat{\beta}_{1}\pm t_{\alpha/2}s_{\hat{\beta}_{1}}$
<!--SR:!2025-04-16,47,227-->

Estimating slope $\beta_{1}$ using a confidence interval:
?
![[Pasted image 20250121163830.png]]
<!--SR:!2025-04-21,11,167-->

## Coefficients of correlation and determination

4 facts about coefficient of correlation
?
- Sample correlation coefficient denoted $r$
- Values range from $-1$ to $+1$
- Measures degree of association
- Does not indicate cause-effect relationship
<!--SR:!2025-06-13,73,207-->

$\rightarrow$ Positive correlation:: $X$ increases, and $Y$ tends to increase.
<!--SR:!2025-06-18,88,247-->
$\rightarrow$ Negative correlation:: $X$ increases, and $Y$ tends to decrease
<!--SR:!2025-05-21,73,247-->


Coefficient of correlation $r$ formula::$$r=\frac{SS_{xy}}{\sqrt{SS_{xx}SS_{yy}}}$$
<!--SR:!2025-04-19,4,130-->

Using $\text{Var}(y)$, $SS_{yy}=$::$(n-1)\text{Var}(y)$
<!--SR:!2025-05-22,53,183-->

Test for linear correlation
?
![[Pasted image 20250123162249.png]]
<!--SR:!2025-04-14,1,130-->

The coefficient of determination represents:: the proportion of the total sample variability around $\bar{y}$ that is explained by the linear relationship between $y$ and $x$.
<!--SR:!2025-04-17,2,130-->

Coefficient of determination formula (2)::$$r^{2}=\frac{SS_{yy}-\text{SSE}}{SS_{yy}}=1-\frac{\text{SSE}}{SS_{yy}}=r^{2}$$
<!--SR:!2025-04-23,10,130-->

## Using the model for estimation and prediction

Used to make inferences in two general categories:
?
- Estimate the mean value of $y$, $E(y)$, for a specific $x$.
- Predict a new individual $y$ value for given $x$.
<!--SR:!2025-04-27,36,175-->

1. The standard deviation of the sampling distribution of the estimator $\hat{y}$ of the  mean value of y at a specific value of $x$, say $x_p$, is
?
$$
\sigma_{\hat{y}} = \sigma \sqrt{\frac{1}{n} + \frac{(x_p - \bar{x})^2}{SS_{xx}}}
$$
where $\sigma$ is the standard deviation of the random error $\epsilon$. We refer to $\sigma_{\hat{y}}$ as the standard error of $\hat{y}$.
<!--SR:!2025-06-25,73,195-->

2. The standard deviation of the prediction error for the predictor $\hat{y}$ of an
individual new $y$-value at a specific value of $x$ is
?
$$
\sigma_{(y - \hat{y})} = \sigma \sqrt{1 + \frac{1}{n} + \frac{(x_p - \bar{x})^2}{SS_{xx}}}
$$
where $\sigma$ is the standard deviation of the random error $\epsilon$. We refer to $\sigma_{(y - \hat{y})}$ as the standard error of the prediction.
<!--SR:!2025-04-22,26,175-->

Confidence Intervals for Mean Values and Prediction Intervals for New Values graph (95%)
?
![[Pasted image 20250129160113.png]]
<!--SR:!2025-05-29,50,175-->