## Q1

**(a)**
![[Pasted image 20250128115055.png|center]]
$A \setminus B =\{x \in U ~|~x \in A \land x \notin B\}$
$\rightarrow x \in A= \{a,b\}$
$\rightarrow x \notin B= \{b,c\}$
$\rightarrow x \in A \setminus B = \{a\}$

$A \cap \overline{B}=\{x \in U ~|~x \in A \land x \in \bar{B}\}$
$\rightarrow x \in A=\{a,b\}$
$\rightarrow x \in \overline{B}=\{a,d\}$
$\rightarrow x \in A \cap B = \{a\}$

Hence, $$A \setminus B=A \cap \overline{B}$$

**(b)**

Using the identity proved in (a), we can rewrite the following $$(C\setminus B) \setminus (B \setminus A)=(C\cap \overline{B})\cap \overline{(B \cap \overline{A})}$$
We use De Morgan's law to simply the right hand part
$$(C\setminus B) \setminus (B \setminus A)=(C\cap \overline{B})\cap (\overline{B} \cup A)$$
$$(C\setminus B) \setminus (B \setminus A)=C\cap \overline{B}\cap (\overline{B} \cup A)$$
We use absorption law to simplify $\overline{B}$
$$(C\setminus B) \setminus (B \setminus A)=C\cap \overline{B}$$
Reusing the identity in (a) we have
$$(C\setminus B) \setminus (B \setminus A)=C\setminus B$$

Hence, $(C\setminus B) \setminus (B \setminus A)=C\setminus B$  is true.

