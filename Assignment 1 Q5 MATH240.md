## Q5

**(a)**
We can visualize this statement by thinking of how many ways we can distribute $20$ identical units into $4$ distinct groups (stars and bars).

So we have $\binom{20+4-1}{4-1}=\binom{23}{3}=1771$ integer solutions to the equation $x_{1}+x_{2}+x_{3}+x_{4}=20$ if we only require $x_{i}\geq 0$ for all $i$.

**(b)**

Let $A_{i}$ be the set of solutions with $x_{i}\geq 10$. So we want to exclude the total number of ways we found in (a) to $|A_{1} \cup A_{2} \cup A_{3} \cup A_{4}|$. We will do it until two pairs because if more than two $x_{i}\geq 10$, it will exceed $20$. $$|A_{1} \cup A_{2} \cup A_{3} \cup A_{4}|=|A_{1}| + \dots  +|A_{4}|-|A_{1}\cap A_{2}|-\dots -|A_{3}\cap A_{4}|$$

For single violations, if we have $x_{1}=10+t$, then $t+x_{2}+x_{3}+x_{4}=20-10$ and we can use stars and bars like in the previous question, so we have $\binom{10+4-1}{4-1}=\binom{13}{3}=286$. Since every $A_{i}$ is disjoint for single violations, each $|A_{i}|=286$.

For double violations, if we have $x_{1}=10+t$ and $x_{2}=10+u$, then $t+u+x_{3}+x_{4}=20-20=0$, the only solution to this equation is $0$. So for our 6 pairs $|A_{i}\cap A_{j}|=1$.

$$|A_{1} \cup A_{2} \cup A_{3} \cup A_{4}|=4\times 286-6 \times 1=1138$$

And so we have $1771-1138=633$ integer solutions to the equation $x_{1}+x_{2}+x_{3}+x_{4}=20$ if we only require $0\leq x_{i}\leq 9$ for all $i$.
 