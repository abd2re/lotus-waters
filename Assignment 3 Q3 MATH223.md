## Q3

**(a)**  
1. Zero Vector: The vector $\vec{0}=(0,0,\dots,0)$ clearly reads the same forward and backward, so $\vec{0}\in W_n$.  
2. Closed under Addition: Suppose $u, v\in W_n$. That means each of them is "palindromic", so $u_i = u_{n+1-i}$ and $v_i = v_{n+1-i}$. If we define $w = u+v$, then
   $$
   w_i \;=\; u_i + v_i 
       \;=\; u_{n+1-i} + v_{n+1-i} 
       \;=\; w_{n+1-i}.
   $$
   Thus $w$ is also palindromic, so $u+v \in W_n$.  
3. Closed under Scalar Multiplication: If $u\in W_n$ and $c\in \mathbb{R}$, then $(cu)_i = cu_i$. Because $u_i = u_{n+1-i}$, we get $(cu)_i = cu_i = cu_{n+1-i} = (cu)_{n+1-i}$. So $cu$ is also palindromic, hence in $W_n$.  

Since all three conditions are satisfied, $W_n$ is a subspace of $\mathbb{R}^n$.  


**(b)**  
A vector $(x_1, x_2, \dots, x_n)$ in $W_n$ must satisfy  
$$
x_1 = x_n,\quad x_2 = x_{n-1}, \quad \dots 
$$
Essentially, the first half of the coordinates determine the entire vector.  

- If $n$ is **even**, say $n = 2m$, then the "free" entries are $x_1, x_2, \dots, x_m$. Once those are chosen, the rest of the vector is fixed because $x_{m+1} = x_m, x_{m+2} = x_{m-1},\dots$. A convenient basis is given by the $m$ vectors:
  $$
    (1,0,0,\dots,0,1),\; (0,1,0,\dots,0,1,0),\;\dots,\;(0,\dots,0,1,1,0,\dots,0),
  $$
where each basis vector has 1’s in the $i$th and $(n+1-i)$th positions and 0’s elsewhere (for $i=1,\ldots,m$). In this case, $\dim(W_n) = m = \tfrac{n}{2}$.  

- If $n$ is **odd**, say $n = 2m+1$, then the "free" entries are $x_1, x_2, \dots, x_m, x_{m+1}$. A basis can be taken as:
  $$
    (1,0,0,\dots,0,0,1),\; (0,1,0,\dots,0,1,0),\;\dots,\;(0,\dots,0,1,0,1,0,\dots,0),
  $$
plus the one "middle" basis vector that has a 1 in the $(m+1)$th (middle) position and 0 elsewhere:
  $$
    (0,\dots,0,1,0,\dots,0).
  $$
Here, $\dim(W_n) = m+1 = \frac{n+1}{2}$.  

So
$$
\dim(W_n) \;=\; 
\begin{cases}
\frac{n}{2},~~~~\text{if $n$ is even},\\
\frac{n+1}{2},~~~~\text{if $n$ is odd}.
\end{cases}
$$
