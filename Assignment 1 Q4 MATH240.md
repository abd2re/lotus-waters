## Q4

- Let $T_{n}$ be the set of all possible passwords of length $n$ in which we use the four categories of character.
- Let $L_{n}$, $U_{n}$, $D_{n}$ and $S_{n}$ be the individual sets containing all possible passwords of length $n$ in which we use their respect character category (lowercase, uppercase, digits, special).
- Let $LU_{n}$, $LD_{n}$, $LS_{n}$, $UD_{n}$, $US_{n}$ and $DS_{n}$ be the individual sets containing all possible passwords of length $n$ in which we use two of the character categories of these groups.

So what we want is the total number of possible password of length $n$ minus the  sets consisting one of category minus the the sets containing two categories (exactly two categories, so we remove cases where all characters are from only one of the categories) for $n=8,9,10$
$$
\sum\limits_{n=8}^{10}\Bigg(|T_{n}|
-\Big(|L_{n}|+\dots +|S_{n}|\Big)
-\Big((|LU_{n}| -|L_{n}|-|U_{n}|)+\dots +(|DS_{n}| -|D_{n}|-|S_{n}|)\Big)
\Bigg)$$
because we find each single category set in $3$ different two category sets, we can rearrange the equation to
$$
\sum\limits_{n=8}^{10}\Bigg(|T_{n}|
-\Big(|L_{n}|+\dots +|S_{n}|\Big)
-\Big((|LU_{n}| +\dots +|DS_{n}|)-3(|L_{n}|+\dots +|S_{n}|)\Big)
\Bigg)
$$
$$
\sum\limits_{n=8}^{10}\Bigg(|T_{n}|
+2\Big(|L_{n}|+\dots +|S_{n}|\Big)
-\Big(|LU_{n}| +\dots +|DS_{n}|\Big)
\Bigg)
$$

- $|T_{n}|$ is the number of arrange the number of possible characters into a password of length $n$. So 
$$|T_{n}|=(26+26+10+10)^{n}$$
$$|T_{n}|=72^{n}$$
- For the size of the sets of one category type, we have
$$|L_{n}|+|U_{n}|+|D_{n}|+|S_{n}|=26^{n}+26^{n}+10^{n}+10^{n}$$
$$|L_{n}|+|U_{n}|+|D_{n}|+|S_{n}|=2(26^{n})+2(10^{n})$$
- For the cardinality of the sets of two character type, we have
$$|LU_{n}|+|LD_{n}|+|LS_{n}|+|UD_{n}|+|US_{n}|+|DS_{n}|=52^{n}+4(36^{n})+20^{n}$$

So we have
$$\sum\limits_{n=8}^{10}\Bigg(72^{n}+2\Big(2(26^{n})+2(10^{n})\Big)-\Big(52^{n}+4(36^{n})+20^{n}\Big)\Bigg)$$
$$\sum\limits_{n=8}^{10}\Bigg(72^{n}+4(26^{n})+4(10^{n})-52^{n}-4(36^{n})-20^{n}\Bigg)$$

Hence, there are $\sum\limits_{n=8}^{10}\Bigg(72^{n}+4(26^{n})+4(10^{n})-52^{n}-4(36^{n})-20^{n}\Bigg)$ ways a password can be chosen in order to meet the requirements.