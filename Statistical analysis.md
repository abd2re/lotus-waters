---
tags:
  - MATH203
---

# Statistical analysis

## Sampling distributions

Suppose we have a random sample of size $n$ $$X_{1},\dots,X_{n}$$ from this distribution. The sample mean random variable is::$$\overline{X}=\frac{1}{n}\sum\limits_{i=1}^{n}X_{i}$$
<!--SR:!2025-01-02,30,230-->

can $\overline{X}$ be a random variable ?:: Yes.
<!--SR:!2024-12-20,27,250-->

If $X_{1}$ and $X_{2}$ are independent and identically distributed random variable from the same population, this mathematically means that:: Independence: $$P(X_{1}=x_{1}\text{ and }X_{2}=x_{2})=P(X_{1}=x_{1})\times P(X_{2}=x_2$$ for all values $(x_{1},x_{2})$ and Identically distributed $$P(X_{1}=x)=P(X_{2}=x)$$ for any $x$.
<!--SR:!2024-12-21,28,250-->

## Central Limit Theorem

Let $X_{1},X_{2},\dots X_{n}$ be independent and identically distributed random variables with expectation $\mu$ and population standard deviation $\sigma$. Then if $$S_{n}=X_{1}+X_{2}+\dots +X_{n}$$ we have that:: $$S_{n}\backsim N(n\mu ,n\sigma^{2})$$
<!--SR:!2024-12-18,12,210-->
$P(1<S_{n}\leq x)\approx$::$F\left(\frac{x-n\mu}{\sqrt{n\sigma^{2}}}\right)-F\left(\frac{1-n\mu}{\sqrt{n\sigma^{2}}}\right)$
<!--SR:!2024-12-09,4,170-->

Alternatively, if $$\overline{X}=\frac{1}{n}(X_{1}+X_{2}+\dots +X_{n})$$ we have that::$$\overline{X}\backsim N\left(\mu,\frac{\sigma^{2}}{n}\right)$$ In practice, "large" is often taken to be $n\geq30$.
<!--SR:!2024-12-13,18,230-->
$Z_{n}=$::$\frac{\overline{X}-\mu}{\sigma/\sqrt{n}}\backsim \text{Normal}(0,1)$
<!--SR:!2024-12-10,19,250-->

If the individual random variables $X_1, \ldots, X_n$ are themselves Normally distributed, then $\overline{X}$ and $S_n$ are:: in fact exactly Normally distributed, no matter the value of $n$.
<!--SR:!2024-12-09,19,250-->

The Central Limit Theorem does not mean that a large number of independent random variables magically become Normal themselves - it’s:: their sum/average that becomes (approximately) Normal.
<!--SR:!2025-01-07,35,230-->

## Point estimators
Suppose we have a population which is described through a distribution that depends on a parameter $\theta$.
In this course we will take $\theta$ to be:: $\mu$ (population mean), or ‚ $p$ in the Binomial set-up (population proportion).
<!--SR:!2024-12-23,26,244-->

Let $X_{1},X_{2},\dots X_{n}$ be the random variables which compromise the sample. We call any function of $X_{1},X_{2},\dots X_{n}$ which does not depend on any unknown quantities:: an estimator of $\theta$.
<!--SR:!2024-12-17,13,184-->

- We denote the estimator function by:: $$\hat{\theta}=\hat{\theta}(X_{1},X_{2},\dots X_{n})$$ $\hat{\theta}$ must be independent of any unknown parameters, otherwise we could not use it as an estimator of $\theta$
<!--SR:!2025-01-15,40,244-->

- An estimator is a random variable since:: it depends n the random variables $X_{1},X_{2},\dots X_{n}$. $\theta$ itself is a constant (despite being unknown)
<!--SR:!2024-12-11,16,224-->

Statisticians have agreed on two properties that indicate a “good” estimator:: Unbiasedness and Minimum variance.
<!--SR:!2024-12-09,10,224-->

Unbiasedness
?
Estimator $\hat{\theta}$ is unbiased of $\theta$ if and only if
$$ E(\hat{\theta}) =\theta$$ for all $\theta$
 - $\hat{\theta}$ is a random variable
 - $\hat{\theta}$ has its own distribution
 - this distribution has a population mean
 - for unbiasedness, this population mean must be $\theta$
<!--SR:!2024-12-12,9,184-->

Minimum variance
?
if $\hat{\theta}_1$ and $\hat{\theta}_2$ are two unbiased estimators for the same target parameter $\theta$, $$ E(\hat{\theta}_1) = E(\hat{\theta}_2) = \theta $$ we will always prefer the estimator with the smaller variance.
<!--SR:!2024-12-24,25,224-->

## Estimating a population mean
It turns out that in almost all cases, the “best” estimator for $\mu$ (i.e. unbiased with the minimum variance among all the unbiased estimators) is::$$\hat{\mu}=\overline{X}$$
<!--SR:!2024-12-25,22,204-->

## Estimating a population proportion
Let $X_1, \ldots, X_n$ be i.i.d. Bernoulli random variables $$P(X_i = 1) = p \quad P(X_i = 0) = 1 - p$$with unknown “success” probability $p$. The best estimator for $p$ (i.e., unbiased with the minimum variance among all the unbiased estimators) is::$$ \hat{p} = \frac{X}{n} = \frac{1}{n} \sum_{i=1}^{n} X_i $$where $X$ is the total number of successes in the sample.
<!--SR:!2024-12-23,16,204-->

- $\hat{p}$ is:: the observed proportion of success in the sample.
<!--SR:!2024-12-15,19,244-->

## Interval estimation

$P(L<\theta <R)=$::$1-\alpha$
<!--SR:!2024-12-17,16,199-->

The interval $(L,~R)$ is called:: a $100(1-\alpha)\%$ confidence interval (CI) for $\theta$.
<!--SR:!2024-12-21,21,215-->


Once we use the observed data $x_{1},~\dots ,~x_{n}$ to compute the observed interval $(l,~r)$, this interval has fixed endpoints and is:: no longer random.
<!--SR:!2024-12-12,14,199-->

The value of $\alpha$ will be given; if it is not, take:: $\alpha=0.05$.
<!--SR:!2024-12-15,18,235-->


## The $t$-distribution
- The $t$-distribution is specified through:: a parameter $v$ called its degrees of freedom (df)
<!--SR:!2024-12-19,20,219-->
- Each $v$ gives a different curve, but this curve is always:: symmetric about 0.
<!--SR:!2024-12-20,21,219-->
- The $t$-distribution allocates more probability to:: tail regions
<!--SR:!2024-12-29,27,235-->
- The standard Normal and the $t$-distribution get more similar as:: $v$ gets larger
<!--SR:!2024-12-31,27,219-->
- As $v \rightarrow \infty$, the $t$-distribution becomes identical to:: the standard Normal
<!--SR:!2025-01-07,34,239-->
- $v=$::$n-1$
<!--SR:!2024-12-28,23,230-->

In order to calculate confidence intervals we first define
?
The notation $z_{a}$ and $t_{a,v}$, the “upper a point” of these distributions
- The upper a point of a standard Normal distribution is the point on the horizontal axis, $z_{a}$ such that $P(Z>z_{a})=a$.
- The upper a point of a $t$-distribution with $v$ degrees of freedom is the point on the horizontal axis, ta,ν such that$P(T>t_{a,v})=a$, where the random variable $T$ has a $t$-distribution with $v$ degrees of freedom.
<!--SR:!2024-12-21,19,199-->

## Experiment scenarios

To determine the correct strategy, we need to identify
?
(A) the assumed probability model/parameter of interest
- Normal $\mu$
- Binomial $p$.
(B) the sample size assumption
- n small ($n<30$)
- n large ($n\geq30$)
(C) the variance assumption for the Normal case
- $\sigma$ known
- $\sigma$ unknown
<!--SR:!2024-12-08,4,179-->

Suppose that $X_{1},~\dots ,~X_{n}$ are a random sample from a Normal distribution with unknown $\mu$ and $\sigma$, and $n<30$.
A $100\%$ confidence interval for $\mu$ is $(L,~R)$ where:
?
$$L=\overline{X}-t_{\alpha/2,n-1}\frac{S}{\sqrt{n}}$$
$$R=\overline{X}+t_{\alpha/2,n-1}\frac{S}{\sqrt{n}}$$
$S$ is the sample standard deviation random variable
<!--SR:!2024-12-12,15,219-->


Suppose that $X_{1},~\dots ,~X_{n}$ are a random sample from a Normal distribution with unknown $\mu$, with $\sigma$ known.
A $100\%$ confidence interval for $\mu$ is $(L,~R)$ where:
?
$$L=\overline{X}-z_{\alpha/2}\frac{S}{\sqrt{n}}$$
$$R=\overline{X}+z_{\alpha/2}\frac{S}{\sqrt{n}}$$
<!--SR:!2024-12-22,23,239-->

Suppose that $X_{1},~\dots ,~X_{n}$ are a random sample from a Normal distribution with unknown $\mu$ and $\sigma$, and $n\geq30$.
A $100\%$ confidence interval for $\mu$ is $(L,~R)$ where:
?
$$L=\overline{X}-z_{\alpha/2}\frac{S}{\sqrt{n}}$$
$$R=\overline{X}+z_{\alpha/2}\frac{S}{\sqrt{n}}$$
Note: Normality of the $X$s is not required
<!--SR:!2025-01-15,39,235-->

Let $X_{1},~\dots ,~X_{n}$ be a random sample of Bernoulli random variables with unknown probability of success $p$.
A $100\%$ confidence interval for $p$ is $(L,~R)$ where:
$$L=\hat{p}-z_{\alpha/2}\sqrt{\frac{\hat{p}(1-\hat{p})}{n}}$$
$$R=\hat{p}+z_{\alpha/2}\sqrt{\frac{\hat{p}(1-\hat{p})}{n}}$$
Note: can be used if $n$ is large where large sample size in this scenario means $n\hat{p}\geq15$ and $n(1-\hat{p})\geq15$.

## The assumption of Normality and assessing normality

When estimating a population mean $\mu$ if the sample size is small $(n<30)$, it can only be done under the assumption that:: the population has a Normal distribution.
<!--SR:!2024-12-30,23,210-->

One way to show some evidence to support an assumption is:: to use the descriptive methods to assess Normality like histograms and boxplots.
<!--SR:!2024-12-13,16,230-->

If the data are approximately Normal, the shape of the histogram will be:: mound shape and symmetric, similar to the Normal probability density function.
<!--SR:!2024-12-31,24,230-->

A more reliable method for checking normality is:: normal probability plot (also called a quantile-quantile (Q-Q) plot.)
<!--SR:!2024-12-08,7,210-->

A Q-Q plot compares:: the quantiles from the sample with the theoretical quantiles from the normal distribution.
<!--SR:!2024-12-11,14,230-->


## Hypothesis Testing

The two hypotheses are called:
?
- the null hypothesis $H_{0}$
- the alternative hypothesis $H_{a}$
<!--SR:!2024-12-10,4,205-->

$H_0$ generally represents:: the perceived “status quo”.
<!--SR:!2024-12-10,5,225-->
$H_a$ generally represents:: a deviation from the “status quo”.
<!--SR:!2024-12-10,5,225-->

Hypothesis Testing steps are:
?
1. Determine $H_{0}$ and $H_{a}$ from the question (null hypothesis and alternative hypothesis)
2. Determine an appropriate Test Statistic $T$: $T$ is a random variable whose value is determined by the individual sample random variables
3. Identify the (sampling) distribution of $T$ assuming $H_0$ is true.
4. Determine the Rejection Region: this will be a set of possible values of the Test Statistic $T$ for which we will “reject” $H_{0}$ “in favor” of $H_{a}$
5. Compute the observed value of $T$ from the observed data
6. Compare the observed value of the $T$ to the Rejection Region
7. Decide and conclude “Reject $H_0$ in favor of $H_a$”, or “Do not reject $H_0$”
<!--SR:!2024-12-10,5,225-->


When we make a decision on the hypotheses, we have the potential to make one of two possible errors:
?
- A Type 1 error occurs when we reject $H_0$ when, in fact, $H_0$ is true.
- A Type 2 error occurs when we fail to reject $H_0$ when, in fact, H0 is not true ($H_a$ is true).
<!--SR:!2024-12-11,6,225-->

The probability of a Type 1 error is denoted:: $\alpha$
<!--SR:!2024-12-11,6,225-->
The probability of a Type 2 error is denoted:: $\beta$
<!--SR:!2024-12-10,5,225-->

We will study three types of sets of hypotheses regarding a parameter $\theta$ (i.e. $\mu$ or $p$):
?
- One-sided: $$H_{0}:\theta=\theta_{0}$$ $$H_a:\theta>\theta_{0}$$
- One-sided: $$H_{0}:\theta=\theta_{0}$$ $$H_a:\theta<\theta_{0}$$
- Two-sided: $$H_{0}:\theta=\theta_{0}$$ $$H_{a}:\theta \neq \theta_{0}$$
<!--SR:!2024-12-10,4,205-->

$\alpha=$::$P_{0}(\text{T lies in rejection region})$
<!--SR:!2024-12-10,4,205-->

- If $T_{obs}$ falls within RR, we will:: reject $H_0$ in favor of $H_a$
<!--SR:!2024-12-10,5,225-->
- If $T_{obs}$ does not fall within RR, we will:: not reject $H_0$.
<!--SR:!2024-12-11,6,225-->



Suppose that $X_1, \dots, X_n$ are a random sample from a Normal distribution with unknown $\mu$ and $\sigma$, and $n < 30$.
$$H_0 : \mu = \mu_0$$
and
?
$$
T = \frac{\overline{X} - \mu_0}{S / \sqrt{n}} \sim t_{n-1}
$$
$$
\begin{aligned}
H_a : \mu > \mu_0 &~~~~~~~~ H_a : \mu < \mu_0 & H_a : \mu \neq \mu_0 \\
\{ T \geq t_{\alpha, n-1} \} & ~~~~~~\{ T \leq -t_{\alpha, n-1} \} & \{ |T| \geq t_{\alpha/2, n-1} \}
\end{aligned}
$$
<!--SR:!2024-12-11,4,185-->

Suppose that $X_1, \dots, X_n$ are a random sample from a Normal distribution with unknown $\mu$, with $\sigma$ known.
$$H_0 : \mu = \mu_0$$
so we have
?
$$
T = \frac{\overline{X} - \mu_0}{\sigma / \sqrt{n}} \sim Normal(0, 1)
$$
$$
\begin{aligned}
H_a : \mu > \mu_0~~~~~~~ & H_a : \mu < \mu_0 & H_a : \mu \neq \mu_0 \\
\{ T \geq z_{\alpha}\}~~~~~~~~~ & \{ T \leq -z_{\alpha} \} & \{ |T| \geq z_{\alpha/2} \}
\end{aligned}
$$
Note: Here $T$ is often denoted $Z$, as it is a z-score.
<!--SR:!2024-12-09,4,225-->


Suppose that $X_1, \dots, X_n$ are a random sample from a distribution with unknown $\mu$ and $\sigma$, where $n \geq 30$.
$$H_0 : \mu = \mu_0$$
so we have
?
$$T = \frac{\overline{X} - \mu_0}{S / \sqrt{n}} \approx Normal(0, 1)$$
$$
\begin{aligned}
H_a : \mu > \mu_0~~~~~~~ & H_a : \mu < \mu_0 & H_a : \mu \neq \mu_0 \\
\{ T \geq z_{\alpha}\}~~~~~~~~~ & \{ T \leq -z_{\alpha} \} & \{ |T| \geq z_{\alpha/2} \}\end{aligned}
$$
Normality of the $X$s is not required.
<!--SR:!2024-12-11,4,185-->

Let $X_1, \dots, X_n$ be a random sample of Bernoulli random variables with unknown probability of success $p$.
$$H_0 : p = p_0$$
so we have
?
$$T = \frac{\hat{p} - p_0}{\sqrt{\frac{p_0 (1 - p_0)}{n}}} \approx Normal(0, 1)$$
$$
\begin{aligned}
H_a : p > p_0~~~~~~~ & H_a : p < p_0 & H_a : p \neq p_0 \\
\{ T \geq z_{\alpha}\}~~~~~~~~~ & \{ T \leq -z_{\alpha} \} & \{ |T| \geq z_{\alpha/2} \}\end{aligned}
$$
Note: $np_{0}\geq 15$ and $n(1-p_{0})\geq 15$
<!--SR:!2024-12-11,4,185-->


- If $H_{a}:\theta>\theta_{0}$, $p\text{-value}=$::$P_{0}(T \geq T_{obs})$
<!--SR:!2024-12-10,4,205-->
- If $H_{a}:\theta<\theta_{0}$, $p\text{-value}=$::$P_{0}(T \leq T_{obs})$
<!--SR:!2024-12-10,4,205-->
- If $H_{a}:\theta \neq \theta_{0}$, $p\text{-value}=$::$2P_{0}(T \geq |T_{obs}|)$
<!--SR:!2024-12-10,4,205-->

$p\text{-value}$ and evidence against $H_{0}$ table
?
![[image-20241130221058279.png]]
<!--SR:!2024-12-10,4,205-->



### Rest

$s_{p}=$::$\sqrt{\frac{(m-1)s_{1}^{2}+(n-1)s_{2}^{2}}{m+n-2}}$
<!--SR:!2024-12-08,2,219-->

$s_{d}=$::$\frac{1}{n-1}\sum\limits_{i=1}^{n}(d_{i}-\overline{d})^{2}$
<!--SR:!2024-12-08,2,219-->


