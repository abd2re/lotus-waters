---
tags:
  - MATH203
---
# Data

## Major elements of statistics

- Experimental (or observational) unit:: An “object” about which we collect data, e.g. person, thing, transaction, tree, event
<!--SR:!2025-04-25,142,250-->
- Population:: the set of all units (people, transactions, trees, animals etc.) that we want to study
<!--SR:!2024-12-13,64,250-->
- Variable:: A characteristic or property of an individual experimental (or observational) unit in the population, e.g. age, weight, counts etc.
<!--SR:!2025-03-16,117,250-->
- Sample:: a subset of units in a population
<!--SR:!2025-03-27,124,250-->
- Statistical inference:: An estimate, prediction, or some other generalization about a population based on information contained in a sample
<!--SR:!2024-12-08,28,150-->
- Measure of reliability:: A statement (usually quantitative) about a degree of uncertainty associated with a statistical inference
<!--SR:!2024-12-10,19,190-->

## Elements of a good statistical analysis

In any study we need to determine (7):
?
1. Objective(s) of a study: what question(s) do we want to answer in our study?
2. Experimental units: people, machines, transactions, …, that we want to study
3. Population under study: a set of experimental units
4. Characteristic(s) of interest: variable(s) measured on the experimental units
5. Sample: a subset of a population under study
6. Inference(s) of interest about the population based on the sample
7. Measure(s) of reliability of the inference(s)
<!--SR:!2024-12-18,22,190-->

## Types of Data

- Quantitative data:: Measurements are recorded on a naturally occurring numerical scale
<!--SR:!2024-12-24,61,230-->
- Qualitative data:: Measurements cannot be made in a natural numerical scale. Can only be ascertained and classified into one of several groups or categories
<!--SR:!2025-02-13,85,210-->

## Data collection
Once we have decided on the units, population, sample and the quantities of interest, we need to collect data There are in general three methods of obtaining data:
?
1. Published sources: books, journals, government publications etc..
2. Designed experiments.
3. Observational studies.
<!--SR:!2024-12-08,21,190-->

Designed experiments
- In a **designed experiment** we have the researcher design:: the experiment and has control over the experimental units sampled
<!--SR:!2025-03-04,109,250-->
- In a **designed experiment**, the two types of groups are:: a group of experimental units **assigned to a treatment**, a group of experimental units that are **untreated**;
<!--SR:!2025-01-11,75,230-->
- In a **designed experiment**, it may involve more than:: two groups.
<!--SR:!2024-12-25,72,270-->


Observational studies
- We are obligated to use **observational studies** sometimes because::  it is either unethical or not possible to assign a treatment or group to a subject.
<!--SR:!2025-04-13,134,250-->
- In an **observational study**, the researcher can only:: observe (directly or indirectly) the experimental units and record the variables of interest
<!--SR:!2025-03-17,130,290-->

## Methods for describing qualitative data

Some methods for describing qualitative data are (4):: Graphical Methods (Histograms, Boxplots) (*quantitative data*), Pie Chart, Bar Plot, Numerical Methods (Table, Class...)
<!--SR:!2024-12-30,68,230-->

## Simpson's Paradox

Simpson's Paradox occurs when:: a trend that appears in several different groups of data disappears or reverses when the groups are combined.
<!--SR:!2024-12-19,13,130-->

This paradox often arises due to the presence of a third variable, known as a:: **confounding factor**, which affects the interpretation of the relationship between the other two variables.
<!--SR:!2025-01-30,77,210-->

The confounding factor can change the direction or strength of the association, leading to:: misleading conclusions if not properly accounted for.
<!--SR:!2025-01-16,77,230-->

## Graphical methods for quantitative data
Two graphical methods for quantitative data are:: histograms and boxplots.
<!--SR:!2025-02-07,85,220-->

A bar graph is used to compare discrete or categorical variables in a graphical format (qualitative data) whereas a histogram depicts:: the frequency distribution of variables in a dataset*
<!--SR:!2025-01-24,74,220-->

## Numerical methods for quantitative data

Sample mean formula::$$\large{\bar{x}=\frac{1}{n}\sum_{i=1}^{n}x_{i}}$$
<!--SR:!2025-02-17,93,234-->
- If $n$ is odd, the sample median $m$ is:: the number in the $\frac{n+1}{2}$ position.
<!--SR:!2025-02-05,86,234-->
- If $n$ is even, the sample median $m$ is:: the average of the number in the $\frac{n}{2}$ position and the number in the $\frac{n}{2}+1$ position.
<!--SR:!2025-01-17,74,234-->

The sample mode is:: the most frequently observed value.
<!--SR:!2025-04-10,129,254-->

Sample variance formula (2)::$$\large{s^{2}=\frac{1}{n-1}\sum_{i=1}^{n}(x_{i}-\bar{x})^{2}=\frac{1}{n-1}\left(\sum_{i=1}^{n}x_{i}^{2}-n\bar{x}^{2}\right)}$$
<!--SR:!2024-12-20,33,214-->

The sample standard deviation is defined as:: $s=\sqrt{s^{2}}$
<!--SR:!2025-01-26,78,234-->

- We say that a sample has a (perfectly) symmetric distribution if:: its histogram has a symmetric shape around some x value, mean $\approx$ median.
<!--SR:!2025-01-15,72,234-->
- Positively (right) skewed data means:: median $\lt$  mean
<!--SR:!2024-12-12,53,234-->
- Negatively (left) skewed data means:: median $\gt$  mean
<!--SR:!2024-12-18,56,234-->

Mean is influenced by large values but the median is:: not.
<!--SR:!2025-01-16,84,274-->

We cannot compute the sample mean, sample median and sample variance if:: we only have access to the histogram plot.
<!--SR:!2024-12-09,19,174-->


## From samples to populations

A simple interpretation of the “population” is to think of it as a sample with:: an extremely large sample size
<!--SR:!2025-01-27,65,213-->
### Empirical rule
- Roughly 68% of the observations will lie in the range:: mean $\pm$ s.d. ($\mu\pm\sigma$)
<!--SR:!2025-01-09,45,213-->
- Roughly 95% of the observations will lie in the range:: mean $\pm$ (2 $\times$ s.d.) ($\mu\pm2\sigma$)
<!--SR:!2025-01-09,62,233-->
- Roughly 99.7% of the observations will lie in the range:: mean $\pm$ (3 $\times$ s.d.) ($\mu\pm3\sigma$)
<!--SR:!2025-01-11,64,233-->

The Empirical rule does not always work well if the distribution is:: not symmetric.
<!--SR:!2024-12-21,50,233-->

### Chebyshev’s rule
The rule states that:: for any distribution and any number k $k>1$: at least $$\left(1-\frac{1}{k^{2}}\right)\times100\%$$ of observations will fall into the interval $(\bar{x}\pm ks)$ regardless of the "shape" of the histogram.
<!--SR:!2024-12-08,11,153-->

If the data have an approximately mound-shape and symmetric distribution it is better to use the Empirical rule. Otherwise, we can only use:: Chebyshev’s rule.
<!--SR:!2025-01-28,74,233-->

### Z-score

Z-score formula (for sample and population) is::$$\text{z-score}=\frac{x-\bar{x}}{s}=\frac{x-\mu}{\sigma}$$
<!--SR:!2024-12-15,46,233-->
If the data have a roughly symmetric, mound-shaped distribution, from the Empirical rule the conversions would be: 68% of the z-scores will lie between -1 and 1 ‚ 95% of the z-scores will lie between -2 and 2 ‚ 99.7% of the z-scores will lie between -3 and 3.

## Graphical methods: Boxplots
Boxplots are another graphical tool for describing quantitative data, and are useful for assessing (4):: center, spread‚ skewness, and outliers.
<!--SR:!2025-01-23,63,213-->
- The 1st sample quartile is:: the number $q_{L}$, such that 25% of the observations are $\le q_{L}$. This the lower quartile.
<!--SR:!2025-03-11,97,233-->
- The 2nd sample quartile is:: the median $m$, such that 50% of the observations are $\le m$.
<!--SR:!2025-01-06,60,233-->
- The 3rd sample quartile is:: the number $q_U$ , such that 75% of the observations are $\le q_{U}$. This is the upper quartile.
<!--SR:!2024-12-20,49,233-->
- In general, for $0\le p\le 1$, the $p^{\text{th}}$ sample quantile is:: the number $q_p$, such that $(100\times p)$% of the observations are $\le q_{p}$.
<!--SR:!2025-01-18,69,233-->

The interquartile range (IQR) is:: the distance between the lower quartile and the upper quartile. $$\text{IQR}=q_{U}-q_{L}$$
<!--SR:!2025-02-21,93,253-->

Boxplots vary slightly from software to software, but the basic components are (6) (with details):
?
- Median line
- Box (lower to upper quartile) or lower and upper hinge
- Inner fences
	- The upper inner fence is $q_{U}+1.5\times \text{IQR}$
	- The lower inner fence is $q_{L}-1.5\times \text{IQR}$
- Outer fences
	- The upper outer fence is $q_{U}+3\times \text{IQR}$
	- The lower outer fence is $q_{L}-3\times \text{IQR}$
- Whiskers, placed at data points less extreme than inner fences
- Outliers that fall outside of the whiskers are also plotted (as points)
![[image-20240921164642288.png|center|500]]
<!--SR:!2025-01-13,64,233-->


Skew representations of box plots:
?
![[image-20240921164908219.png|center|500]]
<!--SR:!2025-02-10,78,233-->

