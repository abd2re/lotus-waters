## Q2

(a)
We only need two variables, $p$ and $q$.  We know that $p \Rightarrow q$ is logically equivalent to $\lnot p \lor q$.

| $p$ | $q$ | $p \Rightarrow q$ | $(p \Rightarrow q)\Rightarrow p$ | $\bigl((p \Rightarrow q)\Rightarrow p\bigr)\Rightarrow p$ |
|:----:|:----:|:--------------------:|:-----------------------------------:|:-----------------------------------------------------------:|
|  1   |  1   |          1           |                 1                   |                              1                              |
|  1   |  0   |          0           |                 1                   |                              1                              |
|  0   |  1   |          1           |                 0                   |                              1                              |
|  0   |  0   |          1           |                 0                   |                              1                              |

Since the last column is always 1, the formula is a tautology.

(b)

Here we have three variables, so there are 8 rows. Below is the abbreviated table showing the core columns. Both $p \Rightarrow (q \Rightarrow r)$ and $(p \land q) \Rightarrow r$ evaluate to the same truth value in every row.

| $p$ | $q$ | $r$ | $q \Rightarrow r$ | $p \Rightarrow (q \Rightarrow r)$ | $p \land q$ | $(p \land q)\Rightarrow r$ | $\;\Longleftrightarrow\;$ |
|:----:|:----:|:----:|:--------------------:|:-------------------------------------:|:------------:|:---------------------------:|:--------------------------:|
|  1   |  1   |  1   |          1           |                  1                    |      1       |             1             |             1             |
|  1   |  1   |  0   |          0           |                  0                    |      1       |             0             |             1             |
|  1   |  0   |  1   |          1           |                  1                    |      0       |             1             |             1             |
|  1   |  0   |  0   |          1           |                  1                    |      0       |             1             |             1             |
|  0   |  1   |  1   |          1           |                  1                    |      0       |             1             |             1             |
|  0   |  1   |  0   |          0           |                  1                    |      0       |             1             |             1             |
|  0   |  0   |  1   |          1           |                  1                    |      0       |             1             |             1             |
|  0   |  0   |  0   |          1           |                  1                    |      0       |             1             |             1             |

Every row's final column is 1, so the formula is a tautology.

(c)
With three variables $p, q, r$, we again have 8 rows. We find that $(p \oplus q)\oplus r$ and $p \oplus (q \oplus r)$ also evaluate to the same truth value in every row.

| $p$ | $q$ | $r$ | $p \oplus q$ | $(p \oplus q) \oplus r$ | $q \oplus r$ | $p \oplus (q \oplus r)$ | $\Longleftrightarrow$ |
| :-: | :-: | :-: | :----------: | :---------------------: | :----------: | :---------------------: | :-------------------: |
|  1  |  1  |  1  |      0       |            1            |      0       |            1            |           1           |
|  1  |  1  |  0  |      0       |            0            |      1       |            0            |           1           |
|  1  |  0  |  1  |      1       |            0            |      1       |            0            |           1           |
|  1  |  0  |  0  |      1       |            1            |      0       |            1            |           1           |
|  0  |  1  |  1  |      1       |            0            |      0       |            0            |           1           |
|  0  |  1  |  0  |      1       |            1            |      1       |            1            |           1           |
|  0  |  0  |  1  |      0       |            1            |      1       |            1            |           1           |
|  0  |  0  |  0  |      0       |            0            |      0       |            0            |           1           |

Again, every row yields 1 in the final column, proving this formula is a tautology.