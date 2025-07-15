---
tags:
  - MATH240
---
# Modular arithmetic

Let $a,b,n \in \mathbb{Z}$, $n \geq 2$. $a$ is **congruent** to $b$ **modulo** if:: $a=b+kn$, for some $k \in \mathbb{Z}$. Equivalently $a-b = kn \implies n \mid (a-b)$. We then write $a \equiv b \bmod n$.
<!--SR:!2025-05-03,23,230-->

$a \equiv b \bmod n \iff a \%n=$::$b\%n$.
<!--SR:!2025-06-17,52,250-->

$\equiv \bmod n$ is compatible with $+$ and $\cdot$, that means if $a \equiv x \bmod n$ and $b \equiv y \bmod n$, then:
?
1. $a+b \equiv x+y \bmod n$
2. $ab \equiv xy \bmod n$
That is why it is called a **congruence**.
<!--SR:!2025-04-30,26,230-->

Given $a,b,n \in \mathbb{Z}$, $b$ is an inverse of $a \bmod n$ if:: $ab \equiv 1 \bmod n$.
<!--SR:!2025-05-17,32,210-->

Inverses are:: unique $\bmod n$. Denoted $a^{-1} \bmod n$.
<!--SR:!2025-05-21,25,190-->


1. $(a^{-1})^{-1}\equiv$::$a \bmod n$
<!--SR:!2025-05-16,3,240-->
2. $(ab)^{-1}\equiv$::$a^{-1}b^{-1}\equiv b^{-1}a^{-1}\bmod n$
<!--SR:!2025-05-08,12,200-->


$a$ has an inverse $\bmod n \iff$::$\gcd(a,n)=1$.
<!--SR:!2025-04-29,17,200-->

$a \equiv b \bmod n \implies a^{k}\equiv$::$b^{k}$.
<!--SR:!2025-05-02,22,220-->

## Modulo prime

Let $p$ be prime. $\forall a \in \mathbb{Z}$, $p |a$ or $\gcd(a,p)=1$. If $a \not\equiv0 \bmod p$, then:: $a$ is invertible $\bmod p$.
<!--SR:!2025-04-30,4,180-->

$ab \equiv 0 \bmod p \implies$::$a \equiv 0 \bmod p$ or $b \equiv 0 \bmod p$ (integrity).
<!--SR:!2025-05-21,8,220-->

Fermat's Little Theorem (FLT)
?
v1. If $a\not\equiv0\bmod p$, then $a^{p-1}\equiv 1 \bmod p$
v2. $a^{p}\equiv a \bmod p$
<!--SR:!2025-04-30,21,220-->

