---
tags:
  - MATH203
---
# Random variables and probability distributions

The mapping $Y$ is termed:: a random variable; it is just a way of recording the outcome in a numerical fashion.
<!--SR:!2025-01-24,62,250-->

Random variable notation:: $P(Y=y)$
<!--SR:!2025-01-18,59,250-->

A random variable $Y$ is termed discrete if:: the possible values that $Y$ can take is a countable set.
<!--SR:!2025-02-02,69,250-->

Write the set of values that carry positive probability:: $\mathcal{Y}$.
<!--SR:!2024-12-13,15,250-->

The probabilities assigned to the individual points in the set $\mathcal{Y}$ in must carry all the probability::$\sum\limits_{y\in \mathcal{Y}}P(Y=y)=1$.
<!--SR:!2024-12-11,32,226-->

The probability mass function (pmf) for $Y$, $p()$ is:: the mathematical function that records how probability is distributed.
<!--SR:!2024-12-22,29,186-->

$p(y)=$::$P(Y=y)$
<!--SR:!2025-01-23,61,250-->
- if $y\in\mathcal{Y}$, then $p(y)$::$>0$
<!--SR:!2024-12-15,36,246-->
- if $y\notin\mathcal{Y}$, then $p(y)$::$=0$
<!--SR:!2025-01-01,47,250-->

## Expectation
The expectation (or expected value) of a discrete random variable $Y$, denoted $E(Y)$, is defined as::$$E(Y)=\sum\limits_{y\in\mathcal{Y}}yp(y)$$ whenever this sum is finite; if it is not finite, we say that the expectation does not exist.
<!--SR:!2024-12-12,5,130-->

The discrete uniform distribution is:: a distribution with constant $p(y)$, that is $p(y)=c$ $y\in\mathcal{Y}$ for some finite set $\mathcal{Y}$. It follow that $\frac{1}{c}$ equals the number of elements in $\mathcal{Y}$.
<!--SR:!2024-12-10,10,146-->

The variance of random variable $Y$ is denoted $\text{Var}(Y)$, and is defined by (2)
?
.$$\begin{split}
\text{Var}(Y)&=E[(Y-\mu)^{2}]=\sum\limits_{y}(y-\mu)^{2}p(y)\\
&=E(Y^{2})-\mu^{2}=\sum\limits_{y\in\mathcal{Y}}\left(y^{2}p(y)\right)-\mu^{2}
\end{split}$$ where $\mu=E(Y)$. The standard deviation of $Y$ is $\text{sd}(Y)=\sqrt{\text{Var}(Y)}$.
<!--SR:!2024-12-12,10,146-->


## Binomial Distribution (Bernoulli distribution)
Notation:: $Y\sim \text{Binom}(n,\,p)$
<!--SR:!2024-12-13,35,246-->
- $p(y)\equiv P(Y=y)=$::$\binom{n}{y}p^{y}(1-p)^{n-y}$, $y\in\{0,\,1,\,2,\,\dots,\,n\}$
<!--SR:!2025-01-05,45,230-->
- $\mu\equiv E(Y)=$::$np$
<!--SR:!2025-02-13,72,246-->
- $\text{Var}(Y)=$::$np(1-p)$
<!--SR:!2024-12-16,37,246-->

## Geometric Distribution
Notation:: $Y\sim \text{Geometric}(p)$
<!--SR:!2025-01-19,53,226-->
The pmf of the geometric distribution states that if:: random variable Y records the number of trials carried out up to an including the first success, then $p(y)=P(Y=y)=(1-p)^{y-1}p$, $y\in\{0,\,1,\,\dots\}$
<!--SR:!2024-12-15,12,130-->
- $E(Y)=$::$\frac{1}{p}$
<!--SR:!2024-12-18,32,210-->
- $\text{Var}(Y)=$::$\frac{1-p}{p^{2}}$
<!--SR:!2024-12-11,5,130-->


## Cumulative Probability

We can define all probabilities such as  $P(Y \leq a)$, $P(Y \geq b)$, $P(c \leq Y \leq d)$  etc. via $F(y)$. This is because for discrete distributions $P(Y \in A)=$::$\sum_{y \in A} p(y)$ for set $A$.
<!--SR:!2024-12-09,14,166-->


$p(y) = P(Y = y)=$:: $P(Y \leq y) - P(Y \leq y - 1)= F(y) - F(y - 1)$
<!--SR:!2024-12-15,9,146-->


$F(y)$ must have the following properties:
?
1. ‘Starts at 0’
   $F(-\infty) = P(Y \leq -\infty) = 0$
2. ‘Ends at 1’
   $F(\infty) = P(Y \leq \infty) = 1$
3. ‘Non-decreasing’
   $\text{If } y_1 < y_2 \text{ then } F(y_1) \leq F(y_2)$
4. ‘Lies in the range $[0,\, 1]$
   $0 \leq F(y) \leq 1 \quad \text{for all } y.$
<!--SR:!2024-12-10,17,186-->

## Poisson Distribution

Notation::$Y\sim \text{Poisson}(\lambda)$
<!--SR:!2024-12-21,27,226-->

If $n \rightarrow \infty$ with $p = \lambda / n$ for fixed $\lambda$, we have that the binomial pmf converges to $p(y) =$::$\frac{\lambda^y}{y!} e^{-\lambda} \quad y \in \{0, 1, 2, \dots\}$ with $p(y) = 0$ for other values of $y$. This is the pmf for the Poisson distribution.
<!--SR:!2024-12-22,15,166-->

- $E(Y)=$::$\lambda$
<!--SR:!2024-12-08,18,206-->
- $\text{Var}(Y)=$::$\lambda$
<!--SR:!2025-01-07,32,206-->

$\lambda=$::$np$
<!--SR:!2024-12-08,17,206-->

The Poisson distribution is widely used to model the distribution of count data, and acts as an approximation to the binomial when:
?
- $n$ is large
- $p$ is small
<!--SR:!2024-12-31,33,226-->

## Continuous Random variables

A random variable Y with distribution function $F(y)$ is called continuous if:: $F(y)$ is continuous for all y.
<!--SR:!2024-12-08,10,206-->

$f(y)=\frac{dF(y)}{dy}$ is known as:: the probability density function (pdf).
<!--SR:!2024-12-08,17,206-->

$F(y)=$::$\int_{-\infty}^{y}f(t)dt$
<!--SR:!2024-12-19,16,206-->

We compute probabilities as
?
“area under $f(y)$” calculations:
- the pdf measures ‘density’, not probability, that is $f(y)\neq P(Y=y)$
- $f(y)$ displays the "shape" of the distribution
<!--SR:!2024-12-11,18,186-->

From the definition, we have two properties of the pdf $f(y)$:
?
1. Non-negative:
   $f(y) \geq 0 \quad -\infty < y < \infty$
   – this follows as $F(y)$ is non-decreasing.
2. Integrates to 1:
   $\int_{-\infty}^{\infty} f(y) \, dy = 1$
	– this follows as $F(\infty) \equiv \lim_{y \rightarrow \infty} F(y) = 1.$
<!--SR:!2024-12-08,18,206-->


For a continuous random variable $P(a < Y \leq b) =$::$P(a \leq Y \leq b) = P(a \leq Y < b) = P(a < Y < b)$
<!--SR:!2024-12-27,30,226-->

- $E(Y) =$:: $\int_{-\infty}^{\infty} y \, f(y) \, dy = \int y \, f(y) \, dy = \mu$
<!--SR:!2025-01-06,32,206-->
- $\text{Var}(Y) =$:: $E \left[ (Y - \mu)^2 \right] = \int_{-\infty}^{\infty} (y - \mu)^2 f(y) \, dy$
<!--SR:!2024-12-19,26,226-->

## Normal Distribution

Notation::$Y\sim \text{Normal}(\mu, \sigma^{2})$
<!--SR:!2024-12-09,16,216-->
The Normal (or Gaussian) distribution has pdf defined on the whole real line by::$$f(y)=\frac{1}{\sigma\sqrt{2\pi}}\exp \begin{Bmatrix}-\frac{1}{2\sigma^{2}}(y-\mu)^{2}\end{Bmatrix}$$ $-\infty < y < \infty$, where $\mu$ and $\sigma >0$ are parameters
<!--SR:!2024-12-20,23,216-->

- $E(Y)=$::$\mu$
<!--SR:!2024-12-18,14,206-->
- $\text{Var}(Y)=$::$\sigma^{2}$
<!--SR:!2024-12-11,17,206-->

If $\mu=0$ and $\sigma=1$ then we have:: the standard Normal pdf.
<!--SR:!2024-12-11,20,206-->


If $Y$ has a Normal distribution with parameters $\mu$ and $\sigma$, and we consider the random variable $Z$ where $Z=$::$\frac{Y - \mu}{\sigma}$ then $Z$ has a standard Normal distribution.
<!--SR:!2024-12-22,16,206-->
