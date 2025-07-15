# Q2

Symmetry:

1. For $A^T A$:  
   Compute the transpose:  
   $$
   (A^T A)^T = A^T (A^T)^T = A^T A.
   $$  
   Thus, $A^T A$ is symmetric.  

2. For $AA^T$:  
   Compute the transpose:  
   $$
   (AA^T)^T = (A^T)^T A^T = AA^T.
   $$  
   Thus, $AA^T$ is symmetric.  

Positive Semi-Definiteness:

1. For $A^T A$:  
   Let $u \in \mathbb{R}^n$. Then:  
   $$
   u^T (A^T A) u = (A u)^T (A u) = \|A u\|^2 \geq 0.
   $$  
   Since the squared norm is non-negative, $A^T A$ is positive semi-definite.  

2. For $AA^T$:  
   Let $v \in \mathbb{R}^m$. Then:  
   $$
   v^T (AA^T) v = (A^T v)^T (A^T v) = \|A^T v\|^2 \geq 0.
   $$  
   Similarly, this is non-negative, so $AA^T$ is positive semi-definite.  

Both $A^T A$ and $AA^T$ are symmetric and positive semi-definite.  