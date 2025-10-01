---
header-includes:
    - \pagenumbering{gobble}
    - \usepackage{setspace}
    - \linespread{1.5}
---

# MATH 531: Project 1

By: Dan McCarthy

Date: 9/18/2025

\newpage

## Problem 1:

Given: $A = \{\emptyset, \{\emptyset\}, \{2\}, 4\}$

### A:

$$
A \cap \{\emptyset\} = \{\emptyset\}
$$

Since $\{\emptyset\} \subseteq A$ the intersection of $A$ and $\{\emptyset\}$ would just be $\{\emptyset\}$ .

### B:

$$
A \cap \{2\} = \emptyset
$$

Since $2 \notin A$ the intersection of $A$ and $\{2\}$ is the $\emptyset$.

### C:

$$
A \cap \{4\} = \{4\}
$$

Since $\{4\} \subseteq A$ the intersection of $A$ and $\{4\}$ is just $\{4\}$ .

### D:

$$
A \cup \{2\} = \{\emptyset, \{\emptyset\}, \{2\}, 4, 2\}
$$

As $2 \notin A$, the union of $A$ and $\{2\}$ would contain all the elements of $A$ as well as $2$.

### E:

$$
A \cup \{4\} = A
$$

Since $4 \in A$ the union of $A$ and $\{4\}$ is just $A$.

### F:

$$
A \cup \{\{\emptyset\}\} = A
$$

Since $\{\emptyset\} \in A$ the union of $A$ and $\{\{\emptyset\}\}$ is just A.

\newpage

## Problem 2:

Given: $x \in \mathbb{R}$ and $y \in \mathbb{R}$ with $x < y$.

Prove: $x < \frac{x + y}{2} < y$.

### Idea:

$x < \frac{x + y}{2}$

$2x < x + y$

$x < y$

So the first part is true.

$\frac{x + y}{2} < y$

$x + y < 2y$

$x < y$

So the other part is also true.

### Proof:

Let $x \in \mathbb{R}$ and $y \in \mathbb{R}$ with $x < y$. $ \ $ (Goal: $x < \frac{x + y}{2} < y$)

**Case 1:**

Since $x < y$, ift

$$
x - y < 0.
$$

Therefore

$$
x - y + 2y < 2y.
$$

Ift

$$
x + y < 2y.
$$

Therefore

$$
\frac{x + y}{2} < y.
$$

Done Case 1.

**Case 2:**

Since $x < y$, ift

$$
y - x > 0.
$$

Therefore

$$
y - x + 2x > 2x.
$$

Ift

$$
x + y > 2x.
$$

Therefore

$$
\frac{x + y}{2} > x.
$$

Done Case 2.

Conclude

$$
x < \frac{x + y}{2} < y.
$$

Done Proof.

\newpage

## Problem 3:

### A:

The sets obey $\emptyset \in A$, $A \subseteq B$, and $A \cap B = \emptyset$.

**Not Possible.**

Since $A \cap B = \emptyset$ there cannot be any elements in A that are also in B besides the null set. This contradicts the condition that $A \subseteq B$, since this would mean for every element in A, that element would also have to be in B.

### B:

The sets obey $A \in B$, $B \in C$, and $B \subseteq C$.

**Possible.**

$A = \emptyset$

$B = \{\emptyset\}$

$C = \{\emptyset, \{\emptyset\}\}$

Since $A = \emptyset$ in this case it is always true that $A \in B$.

Then $\{\emptyset\} \in C$ so the second condition is met.

Additionally since $\emptyset \in C$ that would mean all elements of B are in A so the final condition is met.

### C:

$A \in B$ and $A \cap B = \emptyset$.

**Possible.**

$A = \{2\}$

$B = \{\{2\}\}$

Since $\{2\} \in B$ the first condition is met.

Additionally since sets A and B have none of the same elements the second condition is met.

\newpage

## Problem 4:

Given: $A_n = [0, n]$ for $n =  1, 2, ...$

Find: $\bigcup^7_{n=1} A_n$

### Idea:

$\bigcup^7_{n=1} A_n = [0, 7]$

### Proof:

($\subseteq$) Let $x \in \cup^7_{n=1} A_n$. (Goal: $x \in [0, 7]$)

Ift $x \in A_{n*}$ for some $n*$, $1 \leq n* \leq 7$.

Therefore

$$
x \in [0, n*].
$$

Note that $0 \leq x$ and $x \leq n*$.

Since $x \leq n*$ and $n* \leq 7$, itf

$$
x \leq 7.
$$

Recall that $x \geq 0$.

Therefore

$$
0 \leq x \leq 7
$$

or

$$
x \in [0, 7].
$$

Done ($\subseteq$).

($\supseteq$) Let $x \in [0, 7]$. (Goal: $x \in \bigcup^7_{n=1} A_n$)

Since $A_7 = [0, 7]$, ift

$$
x \in A_7.
$$

Since $x \in A_7$, ift

$$
x \in \bigcup^7_{n=1} A_n
$$

Done ($\supseteq$).

Since $x \in [0, 7]$ and $x \in \bigcup^7_{n=1} A_n$, ift

$$
\bigcup^7_{n=1} A_n = [0, 7].
$$

Done Proof.
