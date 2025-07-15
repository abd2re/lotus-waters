MATH 203: PRINCIPLES OF STATISTICS 1 
FALL 2024 
ASSIGNMENT 3

Abdoul Wahab TOURE
261227818

### Question 1
**(a)** 
The number $Y$, representing the count of people in the sample who have used a fee-based website, follows a **Binomial distribution** because each trial (each interview) has two possible outcomes (used or didn't use a fee-based website), the probability of using the website remains constant at 72% for each person and each response is independent of the others.
**(b)** 
$$P(Y\geq20)=1-P(Y\leq19)$$
$P(Y\leq19)$ can be calculated using the binomial cumulative distribution function $\text{binomcdf}(n, p, y)$.
$$1-\text{binomcdf}(n, p, y)=1-\text{binomcdf}(25, 0.72, 20)=1-0.741=0.259$$
So the probability that at least 20 (that is, 20 or more) people in the sample have used a fee-based website to download music is **0.259**.
**(c)**
$$E(Y)=np=25×0.72=18$$

$$\sigma=\sqrt{\text{Var}(Y)}=\sqrt{np(1−p)​}=\sqrt{25\times 0.72\times 0.28​}\approx2.245$$
- Expected number of people: **18**
- Population standard deviation: approximately **2.245**

### Question 2
**(a)**
The Binomial model is suitable for $Y$ because each missile detection trial is independent, with only two possible outcomes: detection or non-detection. The probability of detection (0.74) is constant across all 15 trials, and we are counting the number of detections. These conditions align with the requirements of a Binomial distribution.
**(b)**
Given that the probability of detecting a missile is 0.74, this is the probability of success for each trial, and the sample size is 15 missile tracks, so
$$p=0.74$$
$$n=15$$
**(c)**
$$P(Y=y)=\binom{n}{y}p^{y}(1−p)^{n−y}$$
$$P(Y=8)=\binom{15}{8}(0.74)^{8}(0.26)^{7}=0.0465$$
**(d)**
$$\begin{split}
P(Y\geq8)&=1-P(Y\leq7)\\
&=1-\text{binomcdf}(15, 0.74, 7)\\
&=1-0.0219\\
&=0.978
\end{split}$$
**(e)**
$$E(Y)=np$$
Given the values $n=15$ and $p=0.74$, we have
$$E(Y)=15\times0.74=11.1$$
So, the expected number of detected missile tracks is **11.1**.

### Question 3
In this scenario, we are dealing with a sequence of trials where each participant experiences pain relief with a probability of 0.92. The study stops as soon as a participant does not report pain relief. This setup follows a **geometric distribution** because we are waiting for the first "failure" (a patient who does not report pain relief) in a sequence of independent trials.

Let $Y$ be the number of patients treated before the study is halted, including the final patient who reports inadequate pain relief. Since each patient reports pain relief with probability $q=0.92$, the probability of a patient not reporting pain relief is $p=1−q=1-0.92=0.08$
Using the expected value for a geometric distribution we have
$$E(Y)=\frac{1}{p}=\frac{1}{0.08}=12.5$$
Therefore, the expected number of patients that will be treated (including the final patient who reports inadequate pain relief) before the study is halted is **12.5**. This means, on average, the study is expected to treat around 12 to 13 patients before encountering a patient who does not report adequate pain relief.

### Question 4
**(a)**
Since each character has an independent probability of being misprinted, we can model the total number of misprints, $Y$, as a binomial distribution:
$$Y\sim\text{Binomial}(n=25000,p=0.0002)$$
and we have $$\begin{split}
P(Y>5)&=1-P(Y\leq5)\\
&=1-\text{binomcdf}(n=25000, p=0.0002, y=5)\\
&\approx1-0.616\\
&\approx0.384
\end{split}$$
Using an exact Binomial calculation, the probability that the total number of misprints exceeds five is **0.384**.
**(b)**
Since $n$ is large and $p$ is very small, we can approximate the Binomial distribution with a Poisson distribution where
$$\lambda=np=25000\times 0.0002=5$$
So now we have $$Y\sim\text{Poisson}(\lambda=5)$$
and we can do $$\begin{split}
P(Y>5)&=1-P(Y\leq5)\\
&=1-\text{poissoncdf}(\lambda=5, y=5)\\
&\approx1-0.616\\
&\approx0.384
\end{split}$$
Using a exact Poisson approximation, the probability that the total number of misprints exceeds five is **0.384** also.

### Question 5
**(a)**
Let's calculate it's z-score for $Y=20$ first $$z=\frac{Y-\mu}{\sigma}=\frac{20-24.1}{6.3}\approx-0.65$$
Using the normal distribution table we have $P(Z\geq-0.65)=P(Z<0.65)=0.7422$.
So the probability that a patient has a maximum oxygen uptake of at least 20 ml/kg is **0.7422**.
**(b)**
We can calculate it's z-score for $Y=10.5$ first $$z=\frac{Y-\mu}{\sigma}=\frac{10.5-24.1}{6.3}\approx-2.16$$
Using the normal distribution table we have $P(Z\leq-2.16)=1-P(z<2.16)=1-9846=0.0154$. 
So the probability that a patient has a maximum oxygen uptake of 10.5 ml/kg or lower is **0.0154**.
**(c)**
The probability of a patient having a maximum oxygen uptake of 10.5 ml/kg or lower is very low (approximately 0.0154, or 1.54%). This low probability indicates that an oxygen uptake value of 10.5 ml/kg is unusual for someone who regularly participates in sports or exercise programs, as it falls well below the mean of 24.1 ml/kg and is more than two standard deviations below the mean.

Therefore, it is **unlikely** that a patient with a maximum oxygen uptake of 10.5 ml/kg participates regularly in sports or exercise programs, as such a low value would be uncommon among those who do.

### Question 6
**(a)**
We can calculate it's z-score for $Y=4000$ first 
$$z=\frac{Y-\mu}{\sigma}=\frac{4000-3500}{600}\approx0.83$$
Using the normal distribution table we have $P(Z>0.83)=1-P(Z<0.83)=1-0.7967=0.2033$. 
The probability it exceeds 4000g is **0.2033**.
**(b)**
We can calculate it's z-score for $Y=3000$ first $$z=\frac{Y-\mu}{\sigma}=\frac{3000-3500}{600}\approx-0.83$$
Using the normal distribution table we have $P(Z>-0.83)=P(Z<0.83)=0.7967$. 
Using the solution from the previous exercise and the solution above we can do $P(-0.83<Z<0.83)=P(Z>-0.83)-P(Z>0.83)=0.7967-0.2033=0.5934$
The probability that it lies between 3000g and 4000g is **0.5934**.
**(c)**
We can calculate it's z-score for $Y=2000$ first $$z=\frac{Y-\mu}{\sigma}=\frac{2000-3500}{600}\approx-2.5$$
Using the normal distribution table we have $P(Z<-2.5)=1-P(Z<2.5)=1-0.9938=0.0062$. 
We can calculate it's z-score for $Y=5000$ next $$z=\frac{Y-\mu}{\sigma}=\frac{2000-3500}{600}\approx2.5$$
Using the normal distribution table we have $P(Z>2.5)=1-P(Z<2.5)=1-0.9938=0.0062$ also. 

Thus the probability is equal to $P(Z<-2.5)+P(Z>2.5)=2\times0.0062=0.0124$ 
So, the probability that the birth weight is either less than 2000g or greater than 5000g is approximately **0.0124**.

### Question 7
**(a)**
z-score for probability that a cork is too small (diameter < 2.85 cm)$$z=\frac{2.85-3}{0.15}=-1$$
Using the normal distribution table we have $P(Z<-1)=1-P(Z<1)=1-0.8413=0.1587$. 
z-score for probability that a cork is too large (diameter > 3.15 cm $$z=\frac{3.15-3}{0.15}=1$$
Using the normal distribution table we have $P(Z>1)=1-P(Z<1)=1-0.8413=0.1587$ also.
Thus the probability is equal to $P(Z<-1)+P(Z>1)=2\times0.1587=0.3174$ 
Therefore, the proportion of defective corks is approximately **0.3174**, or 31.74%.
**(b)**
Let $Y$ be the number of defective corks out of 15. Since we are sampling from a large population with a fixed probability of defect, we can model $Y$ as a Binomial random variable $$Y∼\text{Binomial}(n=15,p=0.3174)$$
We want to calculate $P(Y\leq5)$, using `binomcdf` we have $$\text{binomcdf}(n=15, p=0.3174, y=5)=0.6688$$
So the probability that at most 5 of them (that is, 5 or fewer) will be defective is **0.6688** OR 66.88%.
**(c)**
Since the distribution is symmetric, this probability can be split equally across the two tails: $P(Y<2.85)<0.01$ and $P(Y>3.15)<0.01$

Using the normal distribution table, we find that $P(Z>2.33)≈0.01$, so we need a z-score of $|z|=2.33$ for each tail.

We have for our equations
lower limit: $$-2.33=\frac{2.85-3}{\sigma}\leftrightarrow\sigma=\frac{-0.15}{-2.33}=0.0644$$
upper limit: $$2.33=\frac{3.15-3}{\sigma}\leftrightarrow\sigma=\frac{0.15}{2.33}=0.0644$$

Therefore, to ensure that no more than 2% of the corks are defective, the machine would need to produce corks with a standard deviation of approximately **0.0644 cm**.