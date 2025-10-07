# MATH 531: Proofs Definitions

## Terminology

**bac** - "by a calculation"

**ifc** - "it follows that"

**... dots** - "therefore"

**wma** - "we may assume"

## Def. - Rational

A real number x is called _rational_ if:

$x = \frac{m}{n}$

Where m & n are integers, and n =/ 0.

## Def. - Integer Operations

The sum, difference, or product of 2 integers is **also an integer**.

## Def. - Even/Odd

An integer is _odd_ if **n = 2k + 1**

An integer is _even_ if **n = 2k**

Where **k is an integer**

## Def. - Set

> A set is a well defined collection of unique elements.

## Def. - Null/Empty Sets

> The null/empty set is the set having **no elements**.

It is represented with this symbol: $\emptyset$

## Def. - Common Sets

**These are the definitions for very common sets/symbols:**

$\mathbb{N}$ - natural

$\mathbb{Z}$ - integers

$\mathbb{Q}$ - Rational

$\mathbb{Q}  = \{x \ of \ \mathbb{R}: x = m/n \ where \ m \ of \ \mathbb{Z} \ and \ n \ of \ \mathbb{Z}, \ n \neq 0 \}$

Big R - Real

## Def. - Subsets

> Given 2 sets $A$ and $B$. $A$ is described as a subset of $B$ if for every element of $A$, that element is also in $B$.

Let A and B be sets.

A is a subset of B.

$A \subseteq B$

Every $x \in A$ is in $B$

#

This also means that:

$A \subsetneq B$

Which mean there is SOME x that DOES NOT obey $x \in B$

## Def. - Set Equality

A and B are 2 sets.

We say A and B are equal.

if $A \subseteq B$ and $B \subseteq A$

This can be represented with

## Def. - Empty Set Theorem

Let A be a set.

Then, $\emptyset \subseteq A$

## Def. - Union of Sets

Given A, B are 2 sets.

$$
A \cup B = \{x: either \ x \in A \ or \ x \in B\}
$$

## Def. - Intersection of Sets

Given A, B are 2 sets.

$$
A \cap B = \{x: x \in A \ and \ x \in B\}
$$

## Def. - Theorem Distributive Property

Let A, B, C be sets.

Then

$$
A \cap (B \cup C) = (A \cap B) \cup (A \cap C).
$$

## Def. - Theorem Transitive Property

If $A \subseteq B$ and $B \subseteq C.$

Then

$$
A \subseteq C.
$$

## Def. - Set Difference

Given set A and B.

The Difference is defined as,

$$
A - B = \{x: x \in A \ and \ x \notin B\}.
$$

## Def. - Universal Set

The universal set is $\mathbb{U}$.

In **some** discussion, ALL sets are subsets of $\mathbb{U}.$

## Def. - Set Compliments

The **compliment** of A written as $\overline A$, is defined as:

$$
\overline A = \mathbb{U} - A
$$

## Def. - De Morgans Laws

## Def. - Generalized Union

The generalized union is written:

$U^5_{n-1} A_n = A_1 \cup A_2 \cup .. \cup A_5$

This is effectively summations but for unions.

## Def. - Generalized Intersection

Given $N \in \mathbb{N}$, $N \geq 2$.

The generalized intersection is written:

$$
\cap^N_{n=1} A_n = \{x: x \in A_n \ for \ all \ n, 1 \leq n \leq N\}
$$

## Def. - Cartesian Products

> Given 2 sets $A$ and $B$. The cartesian product of these sets is defined as:
>
> $$
> A \times B = \{z = (a, b): a \in A \ and \ b \in B\}
> $$

NOTE: Order matters for cartesian products.

## Def. - Statements

> An assertion is a declarative sentence or assertion that is either true or false.

A statement (often called P, Q, R, etc.) is an assertion or declarative sentence that is TRUE or FALSE (boolean).

NOTE: Statements must have a singular answer (If the answer is an opinion it can't be a statement)

EX:

-   3 is even (truth value: false)
-   My car is red (truth value: true)

An **open sentence** is a **statement** that involves a variable.

## Def. - Negation

> The negation of a statement $X$ is a statement that is only true exactly when $X$ is false, and is only false exactly when $X$ is true.

We define the negation of a statement using the tilde (~) symbol.

-   ~P is TRUE exactly when P is FALSE.
-   ~P is FALSE exactly when P is TRUE.

## Def. - Conjunction & Disjunction

Given STATEMENTs P and Q.

The conjuction (AND) of P and Q is defined as:

$$
P \land Q
$$

The disjunction (OR) of
P and Q is defined as:

$$
P \lor Q
$$

## Def. - Tautology

A statement such as:

$$
P \lor \~\ P.
$$

(ie. A statement that is always TRUE)

Is called a **Tautology**.

## Def. - Implication

> An implication is a statement written as $P \Rightarrow Q$ where $P$ and $Q$ are statements, and the truth value of $Q$ is dependant upon $P$.

The implication ("if - then") of statements $P \implies Q$ is TRUE if:

-   P is TRUE and Q is TRUE
-   P is FALSE and Q is TRUE
-   P is FALSE and Q is FALSE

$P \implies Q$ is FALSE is only one case:

-   P is TRUE and Q is FALSE

## Def. - Vacuously True vs. Trivially True

> A statement is vacuously true if its hypothesis is always false.

> A statement is trivially true if its hypothesis is always true.

## Def. - Double Implication

The double implication ("if and only if"),

$P \Leftrightarrow Q$

is defined as:

$P \Rightarrow Q \ AND \ Q \Rightarrow P$.

## Def. - Contrapositive

> Let $P$ and $Q$ be statements. The contrapositive of the implication $P \Rightarrow Q$ is $\neg Q \Rightarrow \neg P$.

## Def. - Absolute Value

> Let $x \in \mathbb{R}$ and:
>
> $|x| = \{x, x \geq 0 \ AND \ -x, x < 0\}$

If the definition is piece-wise, we should be using cases to solve.

## Def. -

Fix $K >0$.

Then

$$
|x| < K \Leftrightarrow -K < x < K.
$$

## Def. - Divisibility

Let $a, b \in \mathbb{Z}$, and $a \neq 0$.

We say a divides b.

We write $a|b$.

If $\exists K \in \mathbb{Z}$ such that $b = ak$.
