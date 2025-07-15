# Q4

(a) 
1. 137 (new) $\to$ rank 1
2. 152 (new) $\to$ rank 2
3. 153 (new) $\to$ rank 3
4. 162 (new) $\to$ rank 4
5. 164 (old) $\to$ rank 5
6. 179 (new) $\to$ rank 6
7. 190 (old) $\to$ rank 7
8. 209 (old) $\to$ rank 8
9. 210 (old) $\to$ rank 9
10. 211 (old)
11. 211 (old)
12. 211 (old) $\to$ each 211 averages ranks 10, 11, 12, so each has rank 11
13. 212 (old)
14. 212 (old) $\to$ each 212 averages ranks 13, 14, so each has rank 13.5
15. 213 (old) $\to$ rank 15
16. 216 (new)
17. 216 (new) $\to$ each 216 averages ranks 16, 17, so each has rank 16.5
18. 217 (new)
19. 217 (new) $\to$ each 217 averages ranks 18, 19, so each has rank 18.5
20. 219 (new) $\to$ rank 20

(b) Sum of the ranks for the 10 old-design bottles:
$$
5 + 7 + 8 + 9 + (11 + 11 + 11) + (13.5 + 13.5) + 15
= 104
$$

(c) Sum of the ranks for the 10 new-design bottles (or simply $210 - 104$):

$$
1 + 2 + 3 + 4 + 6 + (16.5 + 16.5) + (18.5 + 18.5) + 20
= 106
$$

(d) The usual Wilcoxon rank-sum statistic $W$ is taken as the sum of ranks for one group so

$$
W = 104
$$

(e) To test at $\alpha = 0.05$, one compares $W$ (or its standardized $z$-value) against the Wilcoxon rank-sum critical region. Because $W = 104$ is extremely close to its expected value under the null $\bigl[n_1(N+1)/2 = 10 \times 21/2 = 105\bigr]$, the difference is not statistically significant.

At the 5% level, we fail to reject the null hypothesis; there is no evidence of a difference in the distributions of bursting strengths between the two bottle designs.
