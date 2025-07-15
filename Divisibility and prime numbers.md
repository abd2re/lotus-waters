---
tags:
  - MATH240
---
# Divisibility and prime numbers

Given $a,b \in \mathbb{Z}$, we say $a$ is a divisor of $b$ ("$a$ divides $b$", "$b$ is a multiple of $a$", "$a|b$") iff:: there exists an integer $k \in \mathbb{Z}$ such that $$b=ak$$.
<!--SR:!2025-05-15,52,250-->


$a|b$ is:: a proposition (something that is true or false). $\rightarrow |$ is a relation symbol. So it's not the same as writing $\frac{b}{a}$: is a rational number.
<!--SR:!2025-07-19,84,250-->

1. If $a |b$ then $\forall c \in \mathbb{Z}$, then:: $a |bc$.
<!--SR:!2025-05-26,59,250-->
1. If $a |b$ and $a |c$, then:: $a |b \pm c$ and $a|\gcd(b,c)$.
<!--SR:!2025-06-05,59,230-->
3. If $a |b$ and $b |c$, then:: $a |c$.
<!--SR:!2025-05-24,58,250-->

The greatest common divisor of $a$ and $b$, written $\gcd(a,b)$ is:: a number $d \in \mathbb{Z}$ such that $d|a$ and $d |b$ and such that for all $c \in \mathbb{Z}$, $c|a \land c|b \implies c \leq d$.
<!--SR:!2025-05-03,39,210-->

$\forall a,b \in \mathbb{Z}$, $b \neq 0$ ($a$ dividend and $b$ divisor), there exists $q,r \in \mathbb{Z}$ called quotient and remainder respectively such that $a$ is equal to::$$a=qb+r$$ and $0 \leq r <|b|$.
<!--SR:!2025-05-10,49,250-->

If $a=qb+r$, then $\gcd(a,b)$ is equal to::$$\gcd(a,b)=\gcd(b,r)$$
<!--SR:!2025-06-12,47,230-->

Euclid's algorithm (to find gcd)
?
To find $\gcd(a,b)$...
1. If $b=0$, then $\gcd(a,b)=a$.
2. Otherwise, write $a=qb+r$ as above and then:$$\gcd(a,b)=\gcd(b,r)$$ which you find using Euclid's algorithm (recursion),
<!--SR:!2025-05-02,45,250-->

Let $d=\gcd(a,b)$, then there exist $s,t \in \mathbb{Z}$ such that $d=$::$sa+tb$.
<!--SR:!2025-07-16,81,248-->

Two numbers $a,b \in \mathbb{Z}$ are coprime if::$$\gcd(a,b)=1$$.
<!--SR:!2025-05-04,27,168-->

$a,b$ are coprime $\iff$:: There exists $s,t \in \mathbb{Z}$ such that $sa+tb=1$.
<!--SR:!2025-04-18,5,130-->

An integer $p \geq 2$ is prime $\iff$:: its only positive divisors are 1 and $p$,
<!--SR:!2025-06-19,67,228-->

An integer $n \geq 2$ which is not prime is called:: composite.
<!--SR:!2025-07-28,93,248-->

For all $n \geq 2 \in \mathbb{N}$, there exists a prime number $p$, such that $n=$::$px$ ($x \in \mathbb{Z}$)
<!--SR:!2025-07-15,80,228-->

If $p$ is prime and $p|ab$, then:: $p|a$ or $p|b$.
<!--SR:!2025-06-21,67,228-->

Let $n \geq 2$ be an integer, then we can find prime numbers: $p_{1} \leq p_{2}\leq \dots \leq p_{k}$ such that $n=$::$p_{1}p_{2}\dots p_{k}$. Moreover, this decomposition is unique.
<!--SR:!2025-04-27,34,238-->

Let $n=p_{1}^{a_{1}}p_{2}^{a_{2}}\dots p_{n}^{a_{n}}$ and $m=p_{1}^{b_{1}}p_{2}^{b_{2}}\dots p_{n}^{b_{n}}$, where $p_{i}$ is prime, and $a_{i},b_{i}\geq 0$. Then $n|m \iff$::$a_{i}\leq b_{i}$ for all $i$.
<!--SR:!2025-05-31,35,178-->

Let $n=p_{1}^{a_{1}}p_{2}^{a_{2}}\dots p_{n}^{a_{n}}$ and $m=p_{1}^{b_{1}}p_{2}^{b_{2}}\dots p_{n}^{b_{n}}$. Then $\gcd(n,m)=$::$p_{1}^{d_{1}}p_{2}^{d_{2}}\dots p_{n}^{d_{n}}$ where $d_{i}=\min(a_{i},b_{i})$.
<!--SR:!2025-04-28,35,238-->

Let $\pi(n)$ be the number of primes $p \leq n$, then $\pi(n)\approx$::$\frac{n}{\log(n)}$
<!--SR:!2025-06-06,54,218-->