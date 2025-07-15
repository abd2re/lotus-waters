# Q3

To prove the inequality using the Cauchy-Schwarz inequality, consider the vectors $u = \left( \frac{1}{\sqrt{a_1}}, \frac{1}{\sqrt{a_2}}, \ldots, \frac{1}{\sqrt{a_n}} \right)$ and $v = \left( \sqrt{a_1}, \sqrt{a_2}, \ldots, \sqrt{a_n} \right)$. By Cauchy-Schwarz:  
$$
\left( u \cdot v \right)^2 \leq \left( \sum_{i=1}^n u_i^2 \right) \left( \sum_{i=1}^n v_i^2 \right)
$$
Calculate $u \cdot v$:  
$$
u \cdot v = \sum_{i=1}^n \left( \frac{1}{\sqrt{a_i}} \cdot \sqrt{a_i} \right) = \sum_{i=1}^n 1 = n
$$
The inequality becomes:  
$$
n^2 \leq \left( \sum_{i=1}^n \frac{1}{a_i} \right) \left( \sum_{i=1}^n a_i \right)
$$
Rearranging gives:  
$$
\frac{1}{a_1} + \frac{1}{a_2} + \ldots + \frac{1}{a_n} \geq \frac{n^2}{a_1 + a_2 + \ldots + a_n}
$$