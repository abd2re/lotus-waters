MATH 203: PRINCIPLES OF STATISTICS 1 
FALL 2024 
ASSIGNMENT 2

Abdoul Wahab TOURE
261227818

### Question 1
**(a)** Using `NumPy` library in Python, we compute $\bar{x}=119.35$, $s=13.40$.
**(b)**
	(i) One deficiency in this interval as representation of the spread of the sample data, is that the upper bound of the second standard deviation is greater than the maximum grade of 128 ($146.16>128$).
	(ii) The interval may not contain approximately 95% of the data because the Empirical Rule does not  work in this case where the grades are not symmetrically distributed.
**(c)** $$z\text{-score}(120)=
\frac{120-\bar{x}}{s}=\frac{120-119.35}{13.40}=0.04851$$
### Question 2
**(a)** Using `NumPy` library in Python, we get $\bar{x}=69.03$, $s=26.44$.
**(b)** 95% of data is included between -2 and 2 standard deviations of the mean so$$\bar{x}\pm2s=69.03\pm2\times26.44=(16.16,\,121.91)$$**(c)**  $$\text{IQR}=q_{\text{upper}}-q_{\text{lower}}=88-52=36$$ (*upper and lower quantile computed using `NumPy` library in Python*)

### Question 3
**(a)** 
	(i) The central tendency is approximately 3 ng/L because the median line is approximately in the middle of 2 and 4 ng/L.
	(ii) If we use the range (without outliers) as a measure of spread or variability of the data, then $$\text{Range}=x_{\text{upper}}-x_{\text{lower}}\approx8.5-(-2)=10.5$$
	(iii) The shape is roughly symmetric with a slight positive skewness because the upper quartile is slightly farther from the median line than the lower quartile is from the median line, the upper whisker is much longer than the lower whisker, and the outliers are above the box.
	(iv) There is one outlier visible in the plot, above the upper whisker at a value around 11. Outliers are defined as values that fall outside 1.5 times the IQR from the quartiles.
	(v) It's not possible to compute how many of the log-transformed numerical values are negative because we cannot take the logarithm of a negative number, so all values are positive real numbers.
**(b)** The two boxplots show distinct differences between the distributions of log-transformed antibiotic concentrations for Regions A and B. In terms of central tendency, Region B has a higher median concentration (around 4) compared to Region A (around 3), indicating that typical antibiotic concentrations are higher in Region B. Regarding spread, both regions have similar variability, with a range  of approximately 10. Both distributions are positively skewed, as seen by the longer upper whiskers. However, Region A shows a more pronounced right skew, with a much shorter lower whisker, suggesting that the data in Region A is more concentrated in the lower range, while Region B is slightly more balanced. In terms of outliers, Region A has two high outliers, both above a concentration of 8, while Region B has one outlier, slightly higher, around 9. Overall, Region B has a higher concentration, similar variability, and fewer extreme outliers compared to Region A.

### Question 4
**(a)**
	(i) $$P(A_{2})=\frac{A_{2}}{n}=\frac{\sum\limits_{i=1}^{4}(A_{2}\cap B_{i})}{n}=\frac{69+388+766+309}{7645}=\frac{1532}{7645}$$
	(ii) $$\begin{split}P(B_{1}\cup B_{2})=P(B_{1})+P(B_{2})&=\frac{B_{1}+B_{2}}{n}\\
	 &=\frac{\sum\limits_{i=1}^{5}(A_{i}\cap B_{1})+\sum\limits_{i=1}^{5}(A_{i}\cap B_{2})}{n}\\ 
	 &=\frac{(7+69+161+58+84)+(315+388+514+207+486)}{7645}\\ &=\frac{2289}{7645}\end{split}$$
	(iii) $$\begin{split}
	P(A_{1}\cup B_{1})
	&=P(A_{1})+P(B_{1})-P(A_{1}\cap B_{1})\\
	&=\frac{A_{1}+B_{1}-(A_{1}\cap B_{1})}{n}\\ 
	&=\frac{\sum\limits_{i=1}^{4}(A_{1}\cap B_{i})+\sum\limits_{i=1}^{5}(A_{i}\cap B_{1})-(A_{1}\cap B_{1})}{n}\\
	&=\frac{(7+315+671+506)+(7+69+161+58+84)-7}{7645}\\
	&=\frac{1871}{7645}
	\end{split}$$
	(iv) $$P(A_{5}\cap B_{4})=\frac{A_{5}\cap B_{4}}{n}=\frac{87}{7645}$$
 **(b)** We know that $$
 P(A_{4})=\frac{A_{4}}{n}
 =\frac{\sum\limits_{i=1}^{4}(A_{4}\cap B_{i})}{n}
 =\frac{58+207+1240+32}{7645}
 =\frac{1537}{7645}\approx0.2010$$
 and $$\begin{split}
 P(A_{4}|B_{2})
 =\frac{P(A_{4}\cap B_{2})}{P(B_{2})}
 &=\frac{A_{4}\cap B_{2}}{B_{2}}\\
 &=\frac{A_{4}\cap B_{2}}{\sum\limits_{i=1}^{5}(A_{i}\cap B_{2})}\\
 &=\frac{207}{315+388+514+207+486}\\
 &=\frac{207}{1910}\approx0.1084\neq P(A_{4})
 \end{split}$$
 Because $P(A_{4})\neq P(A_{4}|B_{2})$, then $A_{4}$ and $B_{2}$ are not independent so ‘Person is from the U.K.’ and ‘Person’s maximum level of education is College’ are not independent.
 **(c)** $$\begin{split}
 P(B_{3}|A_{3})
 =\frac{P(A_{3}\cap B_{3})}{P(A_{3})}
 &=\frac{A_{3}\cap B_{3}}{A_{3}}\\
 &=\frac{A_{3}\cap B_{3}}{\sum\limits_{i=1}^{4}(A_{3}\cap B_{i})}\\
 &=\frac{622}{161+514+622+227}\\
 &=\frac{311}{762}
 \end{split}$$
 Given that the selected person is observed to be from India, the probability that they completed their education at high school is $\frac{311}{762}$.
 **(d)** $$\begin{split}
 P(A_{5}|B_{2})
=\frac{P(A_{5}\cap B_{2})}{P(B_{2})}
&=\frac{A_{5}\cap B_{2}}{B_{2}}\\
&=\frac{A_{5}\cap B_{2}}{\sum\limits_{i=1}^{5}(A_{i}\cap B_{2})}\\
&=\frac{486}{315+388+514+207+486}\\
&=\frac{243}{955}
 \end{split}$$
 Given that the selected person is observed to have completed their education at the college level, the probability that they originated from the U.S.A is $\frac{243}{955}$.