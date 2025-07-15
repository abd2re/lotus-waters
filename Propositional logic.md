---
tags:
  - MATH240
---
# Propositional logic

$\rightarrow$ Propositional logic studies:: propositions; true or false statements.
<!--SR:!2025-07-03,97,250-->

Propositions are represented by variables which range take values in the set:: `Bool = {FALSE,TRUE} = {0,1}`.
<!--SR:!2025-05-18,75,270-->

## Logical connectives

Logical connectives are:: operations on propositions.
<!--SR:!2025-04-29,54,230-->

- Negation:: $\neg p$ = "Not $p$"
<!--SR:!2025-06-15,93,270-->
- Conjunction:: $p \land q$ = "$p$ and $q$"
<!--SR:!2025-08-12,122,250-->
- Disjunction:: $p \lor q$ = "$p$ or $q$ (or both)" (inclusive or)
<!--SR:!2025-05-10,67,250-->
- Exclusive or:: $p \oplus q$ = "p xor q"
<!--SR:!2025-06-25,92,250-->

Two propositions $p$, $q$ are logically equivalent ($p\equiv q$) if:: they have the same truth table.
<!--SR:!2025-05-16,63,230-->

De Morgan laws for propositions
?
$\neg (p \land q)\equiv \neg p \lor \neg q$
$\neg (p \lor q)\equiv \neg p \land \neg q$
<!--SR:!2025-09-02,129,250-->

Absorption law for propositions
?
$p \lor (p \land q)\equiv p$
$p \land (p \lor q)\equiv p$
<!--SR:!2025-07-23,109,250-->

- Conditional:: $p \implies q$ = "$p$ implies $q$", "if $p$, then $q$", "$p$ only if $q$" $=\neg p \lor q$
<!--SR:!2025-08-15,122,250-->

Truth table of $p\implies q$
?
![[Pasted image 20250123124558.png]]
<!--SR:!2025-09-14,141,250-->

- Biconditional:: $p \iff q$ = "$p$ if and only if $q$" = $(p \implies q)\land (q \implies p)$
<!--SR:!2025-06-02,60,190-->

Truth table of $p \iff q$
?
![[Pasted image 20250123125519.png]]
<!--SR:!2025-05-28,71,230-->

- A logical formula is **satisfiable** if:: its truth table has at least one `1`.
<!--SR:!2025-07-15,100,247-->
- A logical formula is a **contradiction** if:: it's not satisfiable (only `0`s in the truth table).
<!--SR:!2025-07-02,92,247-->
- A logical formula is **falsifiable** if:: its truth table has at least one `0`.
<!--SR:!2025-06-02,72,247-->
- A logical formula is a **tautology** if:: it's not falsifiable (only `1`s in the truth table).
<!--SR:!2025-06-19,84,247-->
- A logical formula is a **contingency** if:: it's satisfiable and falsifiable (has `0`s and `1`s in the truth table).
<!--SR:!2025-05-24,28,187-->

$\rightarrow \text{Tautology}\equiv$::$1$
<!--SR:!2025-06-20,94,287-->
$\rightarrow \text{Contradiction}\equiv$::$0$
<!--SR:!2025-06-07,85,287-->


A syllogism is:: a form of argument such that, when all premises are true, then the conclusion is true. The opposite is sophism.
<!--SR:!2025-05-08,37,167-->

The Socrates human mortal example (hypothetical syllogism) is a syllogism because:: $((H \implies M) \land (S \implies H)) \implies (S \implies M)\equiv1$ is a tautology.
<!--SR:!2025-04-16,37,207-->

Syllogism examples
?
![[Pasted image 20250129141913.png]]
<!--SR:!2025-04-27,16,165-->

