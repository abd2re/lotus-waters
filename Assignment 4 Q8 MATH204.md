# Q8

Let  
$$
d_i = (\text{Science score}) - (\text{Math score})
$$ 
for each student $i$.

| Student | Science | Math | $d_i = \text{Sci} - \text{Math}$ |
|---------|---------|------|------------------------------------|
| 1       | 0       | 2    | $-2$                             |
| 2       | 4       | 3    | $+1$                             |
| 3       | 3       | 0    | $+3$                             |
| 4       | 1       | 1    | $0$                              |
| 5       | 3       | 1    | $+2$                             |
| 6       | 2       | 3    | $-1$                             |
| 7       | 4       | 0    | $+4$                             |
| 8       | 2       | 1    | $+1$                             |
| 9       | 3       | 1    | $+2$                             |
| 10      | 4       | 1    | $+3$                             |

Student 4's difference is 0, so we drop that pair from the signed-rank procedure.  That leaves 9 nonzero differences.


The nonzero absolute differences are:  
$$
1,\ 1,\ 1,\ 2,\ 2,\ 2,\ 3,\ 3,\ 4.
$$ 

- Three 1's $\rightarrow$ average rank = $(1+2+3)/3=2,$ so each $|d|=1$ gets rank 2.  
- Three 2's $\rightarrow$ next ranks 4, 5, 6 $\rightarrow$ average rank = 5, so each $|d|=2$ gets rank 5.  
- Two 3's $\rightarrow$ next ranks 7, 8 $\rightarrow$ average rank = 7.5, so each $|d|=3$ gets rank 7.5.  
- One 4  $\rightarrow$ next rank 9, so $|d|=4$ gets rank 9.


$$
\begin{array}{c|c|c|c|c}
\text{Student} & d_i & |d_i| & \text{Rank} & \text{Sign}\\\hline
2 & +1 & 1 & 2 & + \\
6 & -1 & 1 & 2 & - \\
8 & +1 & 1 & 2 & + \\
1 & -2 & 2 & 5 & - \\
5 & +2 & 2 & 5 & + \\
9 & +2 & 2 & 5 & + \\
3 & +3 & 3 & 7.5 & + \\
10 & +3 & 3 & 7.5 & + \\
7 & +4 & 4 & 9 & + 
\end{array}
$$

- Sum of the positive ranks, $T^+$, is  
  $$
  2+2+5+5+7.5+7.5+9 \;=\; 38.
  $$
- Sum of the negative ranks, $T^-$, is  
  $$
  2+5 \;=\; 7.
  $$

$$
T = \min(T^+,\,T^-) = 7.
$$



For $n=9$ nonzero differences and a two-tailed $\alpha=0.05$, $T_{\text{crit}} = 6$. Since our observed $T=7$ is greater than 6, we do not reject $H_{0}$​. Thus, based on this particular critical‐value table, the data do not provide sufficient evidence (at $\alpha=0.05$) to conclude that the median level of family involvement differs between science and math homework for these students.
