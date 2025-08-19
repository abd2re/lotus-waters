# Q6

(a) 
Null and alternative hypotheses.  
Because this is a paired (same subject) experiment comparing treatments A and B, the Wilcoxon signed rank test focuses on the differences.

- Null hypothesis $H_0$: The typical (median) difference is zero.  Equivalently, neither treatment is systematically larger.  
- Alternative $H_a$: The median difference is positive (A > B on average).  


(b)
Conducting the signed rank test at $\alpha = 0.025$.  


| Pair | A   | B   | $d_i$ = A–B | abs($d_i$) |
|-----:|----:|----:|-------------:|---------:|
| 1    | 54  | 45  | $+9$       | 9        |
| 2    | 60  | 45  | $+15$      | 15       |
| 3    | 98  | 87  | $+11$      | 11       |
| 4    | 43  | 31  | $+12$      | 12       |
| 5    | 82  | 71  | $+11$      | 11       |
| 6    | 77  | 75  | $+2$       | 2        |
| 7    | 74  | 63  | $+11$      | 11       |
| 8    | 29  | 30  | $-1$       | 1        |
| 9    | 63  | 59  | $+4$       | 4        |
|10    | 80  | 82  | $-2$       | 2        |


$$
|d_i|: 1, 2, 2, 4, 9, 11,11,11,12,15 
$$
- 1 $\to$ rank 1  
- 2, 2 $\to$ ranks 2 and 3; each gets average rank $2.5$.  
- 4 $\to$ rank 4  
- 9 $\to$ rank 5  
- 11, 11, 11 $\to$ ranks 6, 7, 8; each gets average rank 7.  
- 12 $\to$ rank 9  
- 15 $\to$ rank 10  


- Positive differences (Pairs 1, 2, 3, 4, 5, 6, 7, 9) have ranks:
    $$
    5,10,7,9,7,2.5,7,4 \quad \rightarrow \quad \text{sum} = 51.5
    $$
- Negative differences (Pairs 8, 10) have ranks:
    $$
    1,2.5 \quad \rightarrow \quad \text{sum} = 3.5
    $$

The usual Wilcoxon test statistic $T$ is the smaller of these two sums, so  
$$
    T = 3.5
$$

From standard tables, for $n=10$, $T_{\text{crit}}= 8$.  Since  
$$
   T = 3.5 < 8,
$$  
we reject the null hypothesis at the 2.5% level. The data provide strong evidence that treatment A yields systematically larger responses than treatment B.