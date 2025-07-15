## Q3

**(a)**
Let $A$ be the set of permutations containing the block "OUT" and $B$ the set of permutations containing the block "DIG".

We want to find $|A \cup B|$. 
$$|A \cup B| = |A|+|B|-|A \cap B|$$
$|A|$ and $|B|$ are both equal to $(26-3+1)!=24!$, and $|A \cap B|=(26-6+2)!=22!$ because "OUT" and "DIG" are disjoint.
$$|A \cap B|=24!+24!-22!=2(24!)-22!$$

Hence, there are $2(24!)-22!$ permutations of the 26 letters of the alphabet are there that contain the pattern "OUT" or the pattern "DIG" (or both).

**(b)**
Let $U$ be the set containing all permutations of the alphabet, $A$ be the set of permutations containing the block "MAN" and $B$ be the set of permutations containing the block "ANT".

We want to find $|U|-|A \cap B|$
$$|U|-|A \cap B|=|U|-|A|-|B|+|A \cap B|$$
$|U|$ is equal to $26!$, $|A|$ and $|B|$ are both equal to $(26-3+1)!=24!$, and $|A \cap B|=(26-4+1)!=23!$ because "MAN" and "ANT" are not disjoint and together form a block "MANT".
$$|U|-|A \cap B|=26!-24!-24!+23!=26!-2(24!)+23!$$

Hence, there are $26!-2(24!)+23!$ permutations of the 26 letters of the alphabet are there that contain neither the pattern "MAN" nor the pattern "ANT".