## Q4

**(a)**
Assume $\beta$ is a linearly independent set in $V$ and that **no** larger linearly independent set $\alpha\supset \beta$ exists. We want to show $\beta$ spans $V$.  

Suppose for contradiction that $\beta$ does **not** span $V$. Then there is some vector $v\in V$ not in $\operatorname{span}(\beta)$.  
Consider $\beta \cup \{v\}$. Since $v$ is outside the span of $\beta$, this new set is still linearly independent.  
But $\beta \cup \{v\}$ is a larger linearly independent set than $\beta$, contradicting our assumption that no such bigger set exists.  

Hence our assumption must be wrong, so $\beta$ **does** span $V$. Because $\beta$ is both independent and spanning, $\beta$ is a basis of $V$.  


**(b)**
Now suppose $\beta$ **is** a basis of $V$. We want to show that no strictly larger set $\alpha\supset \beta$ can remain linearly independent.  

Suppose for contradiction that there **is** a set $\alpha\supset \beta$ that is also linearly independent and any vector $u \in \alpha$ but $u \notin \beta$.  
Since $\beta$ is a basis, it spans $V$. In particular, $u$ can be written as a linear combination of vectors in $\beta$.  
But then $u$ is already in the span of $\beta$, so if we include both $u$ and all of $\beta$, we get a linear dependence (because $u$ is "redundant"). This contradicts the assumption that $\alpha$ is linearly independent.  

Therefore no larger linearly independent set containing $\beta$ can exist, completing the proof.