## Q2

(a)
By definition of the trace and matrix multiplication,
$$
\mathrm{tr}(AB) 
=
\sum_{i=1}^n (AB)_{ii}
=
\sum_{i=1}^n \sum_{k=1}^n A_{ik}\,B_{k i}.
$$
If we swap the indices $i\leftrightarrow k$ in the double sum, we get
$$
\sum_{i=1}^n \sum_{k=1}^n A_{ik}\,B_{k i}
=
\sum_{k=1}^n \sum_{i=1}^n A_{k i}\,B_{i k}
=
\sum_{k=1}^n (BA)_{kk}
=
\mathrm{tr}(BA)
$$
Thus $\mathrm{tr}(AB) = \mathrm{tr}(BA)$.


(b)
Suppose $A$ and $B$ are similar, so that 
$$
B = P^{-1}\,A\,P
$$
for some invertible matrix $P$.  Then
$$
\mathrm{tr}(B) 
=
\mathrm{tr}\bigl(P^{-1} A\,P\bigr)
$$
Using part (a) and the cyclic property of the trace, observe
$$
\mathrm{tr}\bigl(P^{-1} A\,P\bigr)
=
\mathrm{tr}\bigl(A\,P\,P^{-1}\bigr)
=
\mathrm{tr}(A)
$$
Hence similar matrices $A$ and $B$ always share the same trace.  

