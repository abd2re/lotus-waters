MATH 203: PRINCIPLES OF STATISTICS 1 
FALL 2024 
ASSIGNMENT 4

Abdoul Wahab TOURE
261227818

### Question 1
**(a)**
The population parameter of interest is the mean power consumption of all 42-inch, large-screen plasma TVs and the point estimate for this parameter is $\hat{u}=\overline{X}=353.8$ watts.
**(b)**
The population parameter of interest is the proportion of professional marathon runners with very high haemoglobin counts and the point estimate for this parameter is $\hat{p}=\frac{X}{n}=\frac{48}{150}=0.32$ or 32%.

### Question 2
We have $\alpha=1-0.95=0.05$, $\overline{X}=6.74$, $S=4.4$ and $n=411$. Because we know the sample standard deviation $S$ and the sample size $n>30$, then we can use the $z$-distribution formulas where we have $z_{\alpha/2}=z_{0.025}=1.96$ according to the the normal distribution table. 
$$L=\overline{X}-z_{\alpha/2}\frac{S}{\sqrt{n}}=6.74-1.96\times \frac{4.4}{\sqrt{411}}\approx6.315$$
$$R=\overline{X}+z_{\alpha/2}\frac{S}{\sqrt{n}}=6.7+-1.96\times \frac{4.4}{\sqrt{411}}\approx7.165$$
The 95% confidence interval for the population mean time spent studying is $(6.315,~7.164)$ (rounded to three decimal places).
The assumptions I've made are:
- The sample is representative of the population of students taking the introductory psychology course.
- The sampling distribution of the sample mean is approximately normal because the sample size ($n=411>30$) is large enough (Central Limit Theorem applies).
- The data are independent (students' study times are not influencing each other).

### Question 3
**(a)**
We have $\alpha=1-0.95=0.05$, $\overline{X}=6.74$, $S=4.4$ and $n=20$. Because we know the sample standard deviation $S$, then we can use the $z$-distribution formulas where we have $z_{\alpha/2}=z_{0.025}=1.96$ according to the the normal distribution table. 
$$L=\overline{X}-z_{\alpha/2}\frac{S}{\sqrt{n}}=49.3-1.96\times \frac{9.14}{\sqrt{20}}\approx45.29$$
$$R=\overline{X}+z_{\alpha/2}\frac{S}{\sqrt{n}}=49.3+1.96\times \frac{9.14}{\sqrt{20}}\approx53.31$$
Thus, the 95% confidence interval for the population mean perceived elapsed time is $(45.29,~53.31)$ (rounded to two decimal places).
The assumptions I've made are:
- The sample is representative of the population of smokers abstaining from nicotine for 24 hours.
- The sampling distribution of the sample mean is not approximately normal because the sample size ($n=20<30$) is not large enough .
- The standard deviation $S$ is sufficient to approximate the population mean using the $z$-distribution (even if $n<30$).
- Observations are independent (one smoker's perception does not influence another's).

**(b)**
The two plots (a histogram and a Q-Q plot) provide information about the assumptions made in Part (a).
- The histogram shows a relatively symmetrical distribution centered around 50-70 seconds, with no extreme outliers. The shape of the histogram is approximately bell-shaped, supporting the assumption that the population distribution is **approximately normal**.
- The Q-Q plot shows that most of the data points lie close to the diagonal reference line, with no major deviations. This indicates that the sample data closely follow a normal distribution.

The plots support the assumptions made in Part (a). Specifically:
1. The **normality assumption** is reasonable based on the histogram and Q-Q plot.
2. The data appear to be a random sample, as no significant anomalies or patterns suggest bias or non-independence.

### Question 4
**(a)**
We are calculating a confidence interval for the population proportion $p$, using the where $\hat{p}$ is the sample proportion, $n$ is the sample size. $z_{0.025} = 1.96$ (for 95% confidence).
$$\hat{p} = \frac{\text{Number of successes}}{\text{Total sample size}} = \frac{31}{49} \approx 0.6327$$
So $$L=\hat{p} - z_{0.025}\sqrt{\frac{\hat{p}(1 - \hat{p})}{n}}=0.6327-1.96\sqrt{\frac{0.6327\times (1-0.6327)}{49}}=0.4978$$
and $$R=\hat{p} + z_{0.025}\sqrt{\frac{\hat{p}(1 - \hat{p})}{n}}=0.6327-+.96\sqrt{\frac{0.6327\times (1-0.6327)}{49}}=0.7676$$
The 95% confidence interval for $p$ is $(0.4978, 0.7677)$ (rounded to four decimal places).
**(b)**
- The sample of 49 adults should be randomly selected to ensure representativeness. Based on the description, it seems reasonable to assume random sampling.
- Observations should be independent (one participant’s improvement should not influence another’s outcome). Assuming each participant used the cream independently, this assumption is valid.
- The sample size should be large enough for the sampling distribution of $\hat{p}$ to be approximately normal. Specifically, both $n\hat{p} \geq 15$ and $n(1 - \hat{p}) \geq 15$.
    - $n\hat{p} = 49 \cdot 0.6327 \approx 31$ and $n(1 - \hat{p}) = 49 \cdot 0.3673 \approx 18$ Both values are greater than 15.
    - So the normal approximation is valid.

### Question 5
**(a)**
The parameter of interest $\theta$, is the population mean fuel consumption (miles per gallon) for the new model of the car.
**(b)**
The hypotheses for testing the manufacturer’s claim are as follows:
- Null hypothesis ($H_{0}$): The population mean fuel consumption is equal to 47 miles per gallon.$$H_{0}:\mu=45$$
- Alternative hypothesis ($H_{a}$): The population mean fuel consumption is lower than 47 miles per gallon. $$H_{a}:\mu<47$$

### Question 6
**(a)**
The parameter of interest, $\theta$, is the proportion of high school graduates in the state who attend a two-year or four-year college within a year of graduation.
**(b)**
The hypotheses for testing whether the college-going rate for high school graduates in the state differs from the national figure are:
- Null hypothesis ($H_{0}$​): The proportion of high school graduates in the state who go to college is equal to the national figure of 61%. $$H_0:p=0.61$$
- Alternative hypothesis ($H_{a}$): The proportion of high school graduates in the state who go to college is different from the national figure of 61%. $$H_{a}:p\neq0.61$$

## Question 7
**(a)**
For a one-sided test with $\alpha = 0.1$, the critical value from the standard normal distribution is:$$z_{0.1} = 1.28$$

The rejection region is:$$z > 1.28$$
**(b)**
For a two-sided test with $\alpha = 0.05$, the critical values from the standard normal distribution are:$$z_{0.025} = \pm 1.96$$
The rejection region is:$$z < -1.96 \quad \text{or} \quad z > 1.96$$

**(c)**
For a one-sided test with $\alpha = 0.1$ and $n = 22$, the critical value from the $t$-distribution with $v = n - 1 = 21$ is:$$t_{0.1, 21} = -1.323$$

The rejection region is:$$t < -1.323$$
**(d)**
For a two-sided test with $\alpha = 0.05$ and $n = 22$, the critical values from the $t$-distribution with $v = n - 1 = 21$ are:$$t_{0.025, 21} = \pm 2.080$$

The rejection region is:$$t < -2.080 \quad \text{or} \quad t > 2.080$$
**(e)** 
Experimental conditions or assumptions for (d):
1. The data are randomly sampled from the population.
2. The population distribution is approximately normal.
3. The sample size ($n = 22$) is small, so the $t$-distribution is used instead of the normal distribution.