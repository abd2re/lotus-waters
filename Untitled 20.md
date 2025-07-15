###### 1  Simple Linear Regression (SLR)

| Item                | Core formula / rule                                                                                                                                                  | Notes & test steps                     |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------- |
| Model               | $y_i = \beta_0+\beta_1x_i+\varepsilon_i,\; E(\varepsilon)=0,\; \operatorname{Var}(\varepsilon)=\sigma^2$                                                             | deterministic + random error framework |
| Estimators          | $b_1=\dfrac{\sum(x_i-\bar x)(y_i-\bar y)}{\sum(x_i-\bar x)^2}$, $b_0=\bar y-b_1\bar x$                                                                               | least‑squares minimizes SSE            |
| ANOVA identity      | $SST=SSR+SSE$; $R^2=SSR/SST$                                                                                                                                         | $R^2=r^2$ in SLR                       |
| Std. error & t‑test | $s=\sqrt{SSE/(n-2)}$; $SE(b_1)=s/\sqrt{S_{xx}}$; $t=\dfrac{b_1}{SE(b_1)}\sim t_{n-2}$                                                                                | test $H_0:β_1=0$                       |
| CI / PI             | $\hat y\pm t_{\alpha/2} s\sqrt{\tfrac1n+\frac{(x_0-\bar x)^2}{S_{xx}}}$ (mean)  $\hat y\pm t_{\alpha/2} s\sqrt{1+\tfrac1n+\frac{(x_0-\bar x)^2}{S_{xx}}}$ (new obs.) |                                        |
| Assumptions         | Linearity, independence, Normality, equal variance                                                                                                                   | check residual plots                   |

###### 2  Multiple Regression & Model Building

- General model: $\mathbf y=X\boldsymbol\beta+\boldsymbol\varepsilon$; $\hat{\boldsymbol\beta}=(X'X)^{-1}X'y$
- Error variance: $s^2=SSE/(n-k-1)$
- Overall F‑test: $F=\dfrac{(SSR/k)}{s^2}\sim F_{k,n-k-1}$ tests $H_0:β_1=\dots=β_k=0$
- Partial (nested) F: $F=\dfrac{(SSE_R-SSE_F)/r}{s_F^2}$ for $r$ extra terms.
- Individual terms: $t=β_j/SE(β_j)$ ($SE(β_j)=s\sqrt{c_{jj}}$; $c_{jj}$ from $(X'X)^{-1}$).
- Interaction: include $x_1x_2$; effect of $x_1$ on $E(y)$ becomes $β_1+β_3x_2$.
- Quadratic: add $x^2$; curvature tested with $H_0:β_2=0$.
- Diagnostics: residual‑vs‑fitted (non‑linearity), Normal Q–Q, Scale‑Location (hetero‑sced), Residuals vs Leverage & Cook’s D (> 4/n) for influence.

###### 3  ANOVA (Completely Randomized) 

| Source    | df    | SS        | MS              | F‑ratio     |
| --------- | ----- | --------- | --------------- | ----------- |
| Treatment | $k-1$ | $SST$     | $MST=SST/(k-1)$ | $F=MST/MSE$ |
| Error     | $n-k$ | $SSE$     | $MSE=SSE/(n-k)$ |             |
| Total     | $n-1$ | $SST+SSE$ |                 |             |

- $H_0: μ_1=⋯=μ_k$; reject if $F>F_{α,k-1,n-k}$.
- Post‑hoc: Tukey HSD or Bonferroni on pairwise means.
- Assumptions: independent r.s. observations, Normality in each group, equal σ².

Randomized Block ANOVA

- Extra factor “Block”; df_block =$b-1$; df_error =$(k-1)(b-1)$.
- F‑treat =$MST/MSE$ tests treatments given blocks.
- Test blocks similarly to justify blocking.

Two‑Factor Factorial (A×B)

- Partition into SSA, SSB, SSAB, SSE.
- Test interaction first; if non‑sig, test main effects.

###### 4  Chi‑Square Tests (Categorical Data) 

| Situation                       | df           | Test statistic                               |
| ------------------------------- | ------------ | -------------------------------------------- |
| Goodness‑of‑fit (1‑way, k cats) | $k-1$        | $\chi^2=\sum\frac{(O-E)^2}{E}$               |
| Independence (r × c)            | $(r-1)(c-1)$ | same formula with $E_{ij}=\dfrac{R_iC_j}{n}$ |

Conditions: expected counts ≥ 5; random sample.

###### 5  Rank‑Based / Non‑Parametric Tests

| Test                             | Purpose                        | Statistic (small‑n)                                 | Large‑n z‑approx                  |
| -------------------------------- | ------------------------------ | --------------------------------------------------- | --------------------------------- |
| Sign test                        | median $η$                     | S = # ‘+’ (or larger of ±)                          | $z=\dfrac{S-n/2-0.5}{\sqrt{n/4}}$ |
| Wilcoxon Rank‑Sum (Mann–Whitney) | 2 indep. samples               | smaller rank‑sum T                                  | $z=\dfrac{T-μ_T}{σ_T}$            |
| Wilcoxon Signed‑Rank             | paired diff. median 0          | W = sum ranks (+)                                   | $z=(W-μ_W)/σ_W$                   |
| Kruskal–Wallis H                 | $k≥3$ indep. groups            | $H=\dfrac{12}{n(n+1)}\sum\dfrac{R_j^2}{n_j}-3(n+1)$ | $χ^2_{k-1}$                       |
| Friedman Fr                      | randomized‑block alt. to 2‑way | $F_r=\dfrac{12}{bk(k+1)}\sum R_j^2-3b(k+1)$         | $χ^2_{k-1}$                       |

###### 6  Design‑of‑Experiments Vocabulary 

- Factor: variable studied (quantitative or qualitative).
- Level: specific value/category of a factor.
- Treatment: factor‑level combination.
- Experimental unit: object receiving a treatment.
- Completely Randomized Design (CRD): random assignment of units to treatments.
- Randomized Block Design (RBD): homogeneous blocks; each block receives every treatment once.
- Factorial Design: all combinations of ≥2 factors.

###### 7  Fast ANOVA & Regression Computation Keys

| Task                              | “One‑line” arithmetic you should memorize                                                                                  |
| --------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Missing MS or F in an ANOVA table | $MS=\dfrac{SS}{df}$; $F=\dfrac{MS_{treat}}{MS_{error}}$                                                                    |
| SST (one‑way)                     | $SST=\sum n_j(\bar y_{j\!•}-\bar y_{••})^2$ _(or given in table)_                                                          |
| SSE (one‑way)                     | $SSE=\sum (n_j-1)s_j^{2}$                                                                                                  |
| Regression $S_{xx}$               | $S_{xx}=(s/s_{b_1})^{2}$ _(from R output)_                                                                                 |
| Convert t‑slope ↔ F‑global (SLR)  | $F=t^2$                                                                                                                    |
| Residual SE                       | $s=\sqrt{MSE}$                                                                                                             |
| R‑squared quick                   | $R^2=1-\dfrac{SSE}{SST}$                                                                                                   |
| df cheat‑table                    | <n rows> • CRD: treat $k-1$ / error $n-k$ • RBD: treat $k-1$ / block $b-1$ / error $(k-1)(b-1)$ • SLR: reg 1 / error $n-2$ |

_If one number is blank in the exam table, work downward (compute MS) then sideways (compute F)._

###### 8  Universal “Exam‑Style” Hypothesis & Conclusion Templates

| Situation               | Null / Alt                                | Decision sentence stem                                                                            |
| ----------------------- | ----------------------------------------- | ------------------------------------------------------------------------------------------------- |
| SLR slope utility       | $H_0:β_1=0$ vs $H_a:β_1≠0$ _(or $>0/<0$)_ | “Since $p\;<\;α$, we reject $H_0$ and conclude a significant linear association.”                 |
| Overall multiple‑reg F  | $H_0:β_1=⋯=β_k=0$                         | “The model explains (or fails to explain) variation in $y$ ($F$=…, $p=$…).”                       |
| One‑way ANOVA           | $H_0:μ_1=⋯=μ_k$ vs “at least two differ”  | “Because $F_{\text{obs}}\;>\;F_{α}$, treatment means are not all equal.” _(follow with post‑hoc)_ |
| Two‑factor interaction  | $H_0:β_{AB}=0$                            | “…no evidence of interaction; proceed to main‑effect ranking.”                                    |
| Chi‑square independence | $H_0:$ variables independent              | “$χ^2$=…, df=…, $p$=… ⇒ variables are / are not associated.”                                      |
| Wilcoxon rank‑sum       | $H_0:$ distributions identical            | “$T$=…, $p$=…; hence median (or location) difference is / is not supported.”                      |
