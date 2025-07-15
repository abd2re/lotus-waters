---
tags:
  - MATH240
---
# Predicate logic

A predicate is:: something that is true about a subject.
<!--SR:!2025-05-12,35,210-->

Mathematically, the subject is variable, and a predicate is:: simply a function. $P: x$.
<!--SR:!2025-04-21,49,250-->

We can use logical connectives (same as in propositional logic) to form:: new proposition functions like $P(x) \land Q(x)$ = "$x>9000$ and $x$ is even".
<!--SR:!2025-06-10,45,230-->

Multivariable predicates are called:: relations.
<!--SR:!2025-05-25,52,190-->

Once a variable has been "quantified" (bound to a quantifier like $\forall$ or $\exists$), the resulting proposition no longer:: "depends" on it $\implies$ It has one less "variable".
<!--SR:!2025-04-17,46,250-->

## Logical equivalences

$\forall x .P(x)$ is true $\iff$::$P(x)$ is always true (no matter what the value of $x$ is) $\iff$ $P(x)$ is never false $\iff$ there is no value $x$ which makes $P(x)$ false $\iff$ It is not the case that there exists an $x$ which makes $P(x)$ false. $\iff$ $\neg \exists x. \neg P(x)$. Therefore $$\neg \forall x.P(x)\equiv \neg \neg \exists x.\neg P(x)\rightarrow \neg (\forall x.P(x))\equiv \exists x.(\neg P(x))$$
<!--SR:!2025-05-15,19,150-->

$\forall \approx$:: Infinite conjunction
<!--SR:!2025-04-30,54,250-->
$\exists \approx$:: Infinite disjunction
<!--SR:!2025-05-21,69,250-->

$\rightarrow~\neg (\exists x.P(x))\equiv$::$\forall x.(\neg P(x))$
<!--SR:!2025-06-14,79,250-->

The truth of a quantified proposition may depend on:: the universe of the discourse.
<!--SR:!2025-06-22,75,210-->

- Given a set $A \subseteq U$, we can write $\forall x \in A.P(x)=$::$\forall x.((x \in A)\implies P(x))$
<!--SR:!2025-08-30,126,250-->
- Given a set $A \subseteq U$, we can write $\exists x \in A.P(x)=$::$\exists x.((x \in A)\land P(x))$
<!--SR:!2025-06-06,41,190-->

Order of quantifiers:: matters.
<!--SR:!2025-07-06,95,250-->

