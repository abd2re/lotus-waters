## Q5

(a)
The hypothesized model for transcript copy number ($Y$) is:  
$$
Y = \beta_0 + \beta_1 X_1 + \beta_2 \text{GeneMSOD} + \beta_3 (X_1 \cdot \text{GeneMSOD}) + \epsilon
$$ 
- Variables:  
  - $X_1$: Proportion of RNA extracted.  
  - $\text{GeneMSOD}$: Indicator variable ($1$ for MnSOD, $0$ for PLD).  
  - Interaction term $X_1 \cdot \text{GeneMSOD}$: Captures how the effect of RNA proportion differs between genes.  

(b)  
The estimated regression equation is:  
$$
\text{Copies} = 86.03 + 114.49 \cdot \text{RNA} + 266.39 \cdot \text{GeneMSOD} + 806.66 \cdot (\text{RNA} \cdot \text{GeneMSOD})
$$ 
- Interpretation:  
  - Intercept ($\beta_0 = 86.03$): Expected copies for PLD gene when RNA proportion = 0.  
  - RNA ($\beta_1 = 114.49$): Rate of increase in copies per unit RNA proportion for PLD.  
  - GeneMSOD ($\beta_2 = 266.39$): Baseline difference in copies between MnSOD and PLD at RNA = 0.  
  - Interaction ($\beta_0 = 806.66$): Additional rate of increase in copies for MnSOD compared to PLD.  

(c)
- Null Hypothesis ($H_0$): No interaction ($\beta_3 = 0$).  
- Alternative Hypothesis ($H_a$): Interaction exists ($\beta_3 \neq 0$).  
- Result:  
  - $p$-value $= 6.14 \times 10^{-16}$ ($< \alpha = 0.01$).  
  - Conclusion: Reject $H_0$. The interaction between RNA proportion and gene type is statistically significant.  

(d)
The rate of increase in copies per unit RNA proportion for MnSOD is:  
$$
\beta_1 + \beta_3 = 114.49 + 806.66 = 921.15
$$ 
Interpretation: For every 1-unit increase in RNA proportion, the transcript copy number increases by 921.15 copies (in thousands) for the MnSOD gene. 

---

```R
data <- read.csv("WHEATRNA.csv")

data$Gene <- factor(data$Gene, levels = c("PLD", "MSOD"))

model <- lm(Copies ~ RNA * Gene, data = data)

model_summary <- summary(model)
interaction_pvalue <- model_summary$coefficients["RNA:GeneMSOD", "Pr(>|t|)"]

beta_RNA <- coef(model)["RNA"]
beta_interaction <- coef(model)["RNA:GeneMSOD"]
rate_MnSOD <- beta_RNA + beta_interaction
```
