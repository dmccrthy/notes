# MATH 531: Proofs Lecture Notes

## Lecture 1:

### General Structure of Proofs

For the most part proofs problem will give you 2 things: a Given, and then something to Prove.

When solving these problems we want to break up are work into 2 sections: the Idea Phase, and the actual Proof. It will look something like this

```
(idea):

x - 1 > 0
...
...
x > 1

Proof:

Given that ...

Therefore ...
```

The Idea part isn't _necessarily required_ but it helps show your thought process and can get you points back if you mess up the actual proof.

In the Idea phase we start with the given equation and work backwards to find basic equation that can be used to prove or disprove the original question. Then in the Proof section we start with that basic building block and work are way back to the original equation.

### Completing the Square

Given some quadratic in the form:

$ax^2 + bx + c = 0$

You can get the following variables like so:

$d = \frac{b}{2a}$

$e = c − \frac{b^2}{4a}$

With these you can create the square:

$a(x+d)^2 + e = 0$

### Pascal's Triangle

**This isn't super important, but it was mentioned in a proof**. Basically you can figure out the coefficients for complex power (like $(x-1)^8$) by doing some basic addition .

### Basics of Sets

A set

#

## Lecture 2:

### Defining a Set

There are 2 main methods to define a set: by roster, and by rule.

-   By roster means that you list out all members of the set.

-   By rule means you define a set by a certain pattern or property.

**Given a set in roster form, WE SHOULD BE ABLE to write it in rule form (and vice versa)**

**The order of elements in a set DOES NOT matter**

### Example 1: (By rule to roster)

$A = \{ x \in real: x^2-5x+6=0 \}$

Factor out the quadratic:

$A = \{ 2, 3 \}$

### Example 2:

Construct a Set B, such that:

$\{ 2 \} \in B, 2 \in B, \{ 3 \} \in B, \ and \ 3 \notin B$

$B = \{ \{2\}, 2, \{3\} \}$

### Example 3:

Given: $A = \{1, 2, 3\}$ and $B = \{m \in \mathbb{Z}: 0 < m < 5\}$

Prove: $A \subseteq B$

**Proof**

Let $x \in A$

if $x = 1$: Then $x \in \mathbb{Z}$

Conclude that $1 \in B$

If $x = 2$, and $x = 3$:

Similar. done.

### Example 4:

Given: $A = \{x \in \mathbb{R}: x^3 + 3x^2 + 3x + 1 = 0\}$ and $B = \{-1\}$

Prove: $A = B$ ($A \subseteq B$ and $B \subseteq A$)

**Proof**

Let $x \in A$.

Therefore,

$$
\begin{align*}
x^3 + 3x^2 + 3x + 1 = 0.
\end{align*}
$$

Bac,

$$
(x+1)^3 = x^3 + 3x^2 + 3x + 1
$$

$$
x = -1
$$

### Example 5:

Given: $A = \{x \in \mathbb{R}: x > -3\}$ and $B = \{x \in \mathbb{R}: x^3 + 3x^2 + x + 3 > 0\}$

Prove: $A = B$

**(Idea):**

$x^3 + 3x^2 + x + 3$

$(x^3 + 3x^3) + (x + 3)$

$x^2(x+3) + (x+3) = (x+3)(x^2+1)$

**Proof**

Claim $A \subseteq B$.

Let $x \in A$.

Therefore,

$$
x > -3.
$$

Therefore,

$$
x+3 > -3 + 3 = 0.
$$

Clearly,

$$
x^2+1>0.
$$

Therefore,

$$
(x^2+1)(x+3) > 0.
$$

Bac,

$$
(x^2+1)(x+3) = (x^3+3x^2)+(x+3)
$$

$$
(x^3+3x^2)+(x+3)>0.
$$

Therefore,

$$
x \in B.
$$

#

## Lecture 3:

Later on we will be asked a true or false question. The expectation is you provide a proof for your answer.

When doing set equality problems (ie. $A = B$) we want to break it up into 2 claims. ($A \subseteq B$ and $B \subseteq A $)

### Example 1:

**Proof (1A)**

Let x be greater than 1.

Since $\ x > 0$, multiplication by x gives

$$
x^2 > x.
$$

Therefore $\ x^2 > x.$

**Proof (1B)**

Choose $x = -1$.

Bac,

$$
x^2 = 1.
$$

Note, $x^2 > x.$

Clearly $\ x \notin (1, \infin).$

### Example 2:

Given: $A = \{x \in \mathbb{R}: 2x^2 + 5x - 3 = 0\}$

Goal: Rewrite in roster form.

**Proof**

Let,

$$
B = \{\frac{1}{2}, -3\}
$$

# DO THIS

#

### Example 3:

Prove: $\{x \in \mathbb{R}: 2x^3 + 2x^2 + x + 1 > 0\} = (-1, \infin)$

**(Idea):**

$(2x^3 + 2x^2) + (x + 1)$

$2x^2(x + 1)+(x+1)$

$(2x^2+1)(x+1)$

**Proof**

Claim 1,

$$
B \subseteq A.
$$

Let $x \in B.$

Therefore,

$$
x > -1.
$$

Therefore,

$$
x+1 > 0.
$$

Note that $\ 2x^2 + 1 > 0.$

Therefore,

$$
(2x^2 + 1)(x + 1) > 0.
$$

Therefore,

$$
2x^3 + 2x^3 + x + 1 > 0.
$$

Therefore,

$$
x \in A.
$$

#

Claim 2,

$$
A \subseteq B.
$$

Let,

$$
x \in A.
$$

Therefore,

$$
2x^3 + 2x^3 + x + 1 > 0.
$$

Therefore,

$$
(2x^2 + 1)(x + 1) > 0.
$$

Note that $\ 2x^2 + 1 > 0$.

Therefore,

$$
x + 1 > 0.
$$

Therefore,

$$
x > -1.
$$

Therefore,

$$
x \in B.
$$

Done.

### Unions and Intersections

**Theorem 1:**

Let A, and B be sets.

$A \cup B = B \cup A$

$A \cap B = B \cap A$

This is effecticely just the commutative property.

**Theorem 2:**

$\emptyset \cup A = A = A \cup \emptyset$

$\emptyset \cap A = \emptyset = A \cap \emptyset$

**Theorem 3:**

How about combining terms,

$A \subseteq A \cup B$

$B \subseteq A \cup B$

**Theorem 4:**

$A \cap B \subseteq A$

$A \cap B \subseteq B$

**Theorem 5:**

If A, B, and C are sets.

$A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$

#

Sometimes when constructing sets it may not be possible based on the conditions. Consider:

### Example 4:

Construct a set D with $\ 2 \in D$ and $\{2\} \subsetneq D$.

Notice the conditions are inverse of each other.

**No such set D exists.**

## Lecture 4:

We ended class last time with an example we hadn't finished. Here it is:

### Example ~0:

Prove: $A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$

**Proof**

Let $x \in A \cap (B \cup C)$.

Therefore

$$
x \in A \ and \ x \in B \cup C.
$$

Since $x \in B \cup C$, itf

$$
either \ x \in B \ or \ x \in C.
$$

**Case 1:** Assume $x \in B$.

Therefore

$$
x \in A \cap B.
$$

Therefore

$$
x \in (A \cap B) \cup (A \cap C).
$$

Done Case 1.

**Case 2:** Assume $x \in C.$

Therefore

$$
x \in A \cap C.
$$

Therefore

$$
x \in (A \cap B) \cup (A \cap C).
$$

Done Case 2.

#

Let $x \in (A \cap B) \cup (A \cap C).$

Therefore

$$
either \ x \in A \cap B \ or \ x \in A \cap C.
$$

**Case 1:** Assume $x \in A \cap B.$

Therefore

$$
x \in A \ and \ x \in B.
$$

Since $x \in B$, ift

$$
x \in B \cup C.
$$

Therefore

$$
x \in A \cap (B \cup C).
$$

Done Case 1.

**Case 2:** Assume $x \in A \cap C.$

Similar to Case 1. **(You could have done is for Case 2 of PT. 1)**

Done Case 2.

Done.

#

### Example 1:

Sets A, B with $A \in B$ and $A \subseteq B$.

$A = \{2\}$

$B = \{2, \{2\}\}$

Done.

### Example 2:

Sets A, B, and C with $(A \cap B) \cup (A \cap C) \neq A \cap (B \cup C)

Not possible.

Known theorem,

"Let A, B, C be sets.

Then

$A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$"

### Example 3:

Sets A, B, C with

$A \in B$, $A \subseteq C$, $B \subsetneq C$.

**Proof**

Let $A = \{2\}.$

Let $B = \{\{2\}\}.$

Let $C = \{ 2 \}.$

Clearly $A \in B$ and $A \subseteq C$.

Note that $\{2\} \in B$ and $\{2\} \notin C.$

Therefore $B \subsetneq C.$

Done.

### Example 4:

Construct a set A with $\{3\} \subseteq A$ and $A \cap \{2, 3, 5\}.$

Not Possible.

Note that $3 \in A$ and $3 \in \{2, 3, 5\}.$

Therefore $3 \in A \cap \{2, 3, 5\}.$

Done.

### Example 5:

Give an example of set A with $\emptyset \subseteq A$ and $\{\emptyset\} \cap A = A.$

**Proof**

Let $A = \emptyset.$

Bac,

$$
\{\emptyset\} \cap A = \{\emptyset\} \cap \emptyset = \emptyset.
$$

### Example 6:

Give an example with $A \neq \emptyset$, $\emptyset \subseteq A$ and $ \{\emptyset\} \cap A = A.$

**Proof**

Let $A = \{\emptyset\}$

Clearly $A \neq \emptyset.$

Remember that $\emptyset \subseteq A$ is always true.

Finally

$$
\{\emptyset\} \cap A = \{\emptyset\} \cap \{\emptyset\} = \{\emptyset\} = A.
$$

Done.

### Example 7:

Given $A = \{ \emptyset, \{\emptyset\}\}.$

-   $\emptyset \cup A = A$ (General Fact)

-   $\{\emptyset\} \cup A = A$

-   $\emptyset \cap A = \emptyset$ (General Fact)

-   $\{\emptyset\} \cap A = \{\emptyset\}$

### Example 8:

Find A, B, C with $A \subseteq B$, $B \subseteq C$, and $\{3\} \subseteq A$, $3 \notin C.$

Not Possible.

**Proof**

Note that $3 \in A.$

Since $3 \in A$ and $A \subseteq B$, ift

$$
3 \in B.
$$

Since $3 \in B$ and $B \subseteq C$, ift

$$
3 \in C.
$$

But $3 \notin C$ was required.

Done.

## Lecture 5:

$\mathbb{U}$ represents the universal set (set of everything).

We can use U to find the complement of sets.

### Example 1:

**Given:**

$U = \{1, 2, 3, ..., 9, 10\}$

$A = \{3\}$

$B = \{1, 3, 4\}$

Prove: $\overline{A \cup B} = \overline A \cap \overline B$ (This is just De Morgans Law)

**Proof:**

# DO THIS

## Lecture 6:

import notes from other computer

## Lecture 7:

We spent this class finding generalized intersections. Similiar to what we did last class, but for intersections instead of unions.

### Problem Overview:

Given $A_1, A_2, A_3, ...$.

Fix $N \in \mathbb{N}$.

$\cup^N_{k=1} A_k = \{x: x \in A_{k*} \ for \ some \ k*, 1 \leq k* \leq N\}$

$\cap^N_{k=1} A_k = \{x: x \in A_{k*} \ for \ all \ k = 1, 2, ..., N\}$

(Notice the difference between the union and intersection)

### Part 1: (Union)

**Idea:**

$\cup^3_{n=1} A_n = (0, 3)$

**Proof:**

$(\supseteq)$ Let $x \in (0, 3)$. (Goal: $x \in \cup^3_{n=1} A_n$)

Note that $(0, 3) = A_3$.

Since $x \in A_3$, ift

$$
x \in \cup^3_{n=1} A_n
$$

Done $(\supseteq)$.

#

$(\subseteq)$ Let $x \in \cup^3_{n=1} A_n$. (Goal: $x \in (0, 3)$)

Ift $x \in A_{n*}$ for some $n*, 1 \leq n* \leq 3$.

Therefore

$$
x \in (0, n*).
$$

Note $0 < x$ and $x < n*$.

Since $x < n*$ and $n* \leq 3$, ift

$$
x < 3.
$$

Therefore

$$
0 < x < 3.
$$

Done.

### Part 2: (Intersection)

**Idea:**

$A_n = (0, n)$

$n = 1, 2, ...$

$\cap^5_{n=1} A_n = (0, 1)$.

**Proof:**

$(\subseteq)$ Let $x \in \cap^5_{n=1} A_n$. (Goal: $x \in (0, 1)
$)

Therefore $x \in A_n$ for $n = 1, 2, 3, 4, 5$.

In particular $x \in A_1$.

Remember $A_1 = (0, 1)$.

Done $(\subseteq)$.

$(\supseteq)$ Let $x \in (0, 1)$. (Goal: $x \in \cap^5_{n=1} A_n$)

## Lecture 8:

The focus of this class was on Cartesian Products which we started at the end of last class.

### Example 1:

If possible, construct sets A and B such that: $A \in B$ and $A \subseteq B$.

If possible, construct sets A and B such that: $A \in B$ and $A \subseteq B$ and $A \cap B = \{\emptyset\}$.

If possible, construct sets A and B such that: $A \in B$ and $A \subseteq B$ and $A \cap B = \emptyset$.

**1:**

$A = \emptyset$

$B = \{\emptyset\}$

**2:**

$A = \{\emptyset\}$

$B = \{\{\emptyset\} , \emptyset\}$

**3:**

This IS ACTUALLY possible!

$A = \emptyset$

$B = \{\emptyset\}$

### Example 2:

Given sets A, B, and C with $B \subseteq C$.

Prove: $A \times B \subseteq A \times C$.

**Proof:**

Let $z \in A \times B$.

Therefore $z = (a, b) \ where \ a \in A \ and \ b \in B$.

Since $B \subseteq C$, ift $b \in C$.

Therefore $(a, b) \in A \times C$.

Done.

### Example 3:

Given A, B, and C are generic sets.

Prove: $(A \cup B) \times C = (A \times C) \cup (B \times C)$.

**Proof:**

$(\subseteq)$ Let $z \in (A \cup B) \times C$.

Therefore $z = (\gamma, c)$ where $\gamma \in A \cup B$ and $c \in C$.

Since $\gamma \in A \cup B$, ift

$$
\gamma \in A \ or \ \gamma \in B.
$$

**Case 1:**

Assume $\gamma \in A$.

Ift $(\gamma, c) \in A \times C$.

Therefore $(\gamma, c) \in (A \times C) \cup (B \times C)$.

Done Case 1.

**Case 2:**

Assume $\gamma \in B$.

Similiar to Case 1.

Done Case 2.

Done $(\subseteq)$.

##

$(\supseteq)$ Let $z \in (A \times C) \cup (B \times C).$

Finish this...

##

We will be skipping:

-   Partitions
-   Power Sets P(A)
-   Cadinality |A|

At this point we start on chapter 2 (Logic).

Given an open sentence, we can describe truth table relating its inputs to its truth vale.

## Lecture 9:

This class focused on logic and logical operations as well as how to draw truth tables.

### Example 1:

Some example negations:

**P:** Every function is either differentiable or continuous

**~P:** There is a function such that the function is not differentiable and is not continuous.

### Example 2:

Given: $P \lor \~\ P$ is true.

Cannot be determined.

P is either TRUE or FALSE.

### Exmaple 3:

This introduces the $\implies$ symbol.

## Lecture 10:

Missed this one :(

## Lecture 11:

Today was focused on reviewing old problems for exam next week.

### Example 1:

Given: $A = (-\infin, -2)$ and $B = \{x \in \mathbb{R}: x^3 + 2x^2 + 4x +8 < 0\}$

Prove: $A = B$

**Proof:**

($\subseteq$) Let $x \in A$.

Therefore

$$
x < -2.
$$

Therefore

$$
x + 2 < 0
$$

Note that $x^2 + 4 < 0$ for all $x \in \mathbb{R}.$

Therefore

$$
(x + 2)(x^2 + 4) < 0.
$$

Bac

$$
x^3 + 2x^2 + 4x +8 < 0.
$$

Therefore

$$
x \in B
$$

Done ($\subseteq$).

($\supseteq$) Let $x \in B$.

Therefore

$$
x^3 + 2x^2 + 4x +8 < 0.
$$

Therefore

$$
(x + 2)(x^2 + 4) < 0.
$$

Since $x^2 + 4 > 0$, ift

$$
x + 2 < 0.
$$

Therefore

$$
x < -2.
$$

Therefore

$$
x \in A.
$$

Done ($\supseteq$).

Done Proof.

### Example 2:

Given:

Prove:

**Idea:**

$n^2 + 3n = n(n + 3)$

**Proof:**

Assume $n = 2k + 1$.

Bac

$$
n^2 + 3n = (2k + 1)^2 + 3(2k + 1)
$$

$$
= 4k^2 + 10k + 4
$$

$$
= 2(2k^2 + 5k + 2).
$$

Let $L = 2k^2 + 5k + 2$.

Note that $L \in Z$.

Done Proof.

### Example 3:

Given: $n \in \mathbb{Z}$

Prove: If $n > 13$ and $n \leq 255$ then $n^2 + 3n$ is even.

**Proof:**

The implication is trivially true.

CLAIM: $\forall \ n \in \mathbb{Z}$, ift $n^2 + 3n$ is even.

Proof of CLAIM: In class.

### Exam 2 Concepts: (DON'T study these)

Given the implication

$P \Rightarrow Q$

the contrapositive implication is

$(\neg Q) \Rightarrow (\neg P)$.

## Lecture 12:

Implications practice problems for Exam 1:

### Solution 1:

> $x \in \emptyset \Rightarrow x > 4$ and $x$ is rational.

The implication is vacuously true.

CLAIM: ($x \notin \emptyset$)

PROOF: $\emptyset$ has no elements. $\blacksquare$

### Solution 2:

> $x$ is pluripositive $\Rightarrow x \in \emptyset$.

The implication is trivially true.

CLAIM: For every $x$, ift $x \notin \emptyset$

PROOF: Recall $\emptyset$ has no elements. $\blacksquare$

### Solution 3:

Let $n \in \mathbb{Z}.$

Prove: If $n$ is even, then $4n + 3$ is odd.

> Can't be vacuously true.
>
> 4n + 3 is always true.
>
> So vacuously true.

CLAIM: For ANY integer $n$, ift $4n + 3$ is odd.

PROOF:

Note that $4n + 3 = 2(2n+1) + 1$.

Let $L = 2n + 1$.

Note that $L \in \mathbb{Z}$. $\blacksquare$

### Solution 4:

Let $n \in \mathbb{Z}$.

Prove: If $16n^4 + 8n^2 - 6$ is odd, then $n$ is even.

IDEA:

The implication is vacuously true.

> DO THIS YOURSELF

CLAIM:

PROOF:

### Proof By Contrapositive

> Proving that $\neg Q \Rightarrow \neg P$

### Solution 5::

Let $n \in \mathbb{Z}$.

Prove: $5n  + 3$ is odd $\Leftrightarrow 9n - 4$ is even. (**Lemma - A helping statement**)

**Idea:**

$n=0$ we get $3$ and $-4$.

$n=1$ we get $8$ and $5$.

$n=2$ we get $13$ and $14$.

-   Direct Proof (Not possible)
-   Contrapositive Proof (Too hard)
-   Contrapositive or Vacuously (YES)

Lemma:

If $5n + 3$ is odd, then n is even.

**Proof:**

DO IT YOURSELF

## Lecture 13:

Not here.

## Lecture 14:

This is coming off the first exam. Coming up we have:

-   Project 2 posted 10/3
-   No class 10/13
-   Project 2 drafts 10/15
-   Project 2 due 10/20

Going into some review from the past few sections.

### Example 1:

Prove: If $1 < n^2 < 3$, then $sin(\pi*n + 3) \geq -1$.

#### Idea:

Vacuously true since the first condition is false.

It is also trivially true since the second condition is true.

#### Proof:

The implication is vacuously true.

CLAIM: $\nexists n \in \mathbb{N}$ such that $1 < n^2 < 3$.

PROOF OF CLAIM:

Let $n \in \mathbb{N}$.

If $n = 1$, then $n^2 = 1$.

Conclude ~$[1 < n < 3]$.

If $n \geq 1$, then $n^2 \geq 4$.

Conclude ~$[1 < n < 3]$.

This proves the claim. $\blacksquare$

### Example 2:

Prove: $3n - 4$ is odd $\Leftrightarrow 5n + 1$ is even.

#### Idea:

We need to prove both of these:

$3n - 4$ is odd $\Rightarrow 5n + 1$ is even.

$3n - 4$ is odd $\Leftarrow 5n + 1$ is even.

Consider this,

$$
5n + 1 = (3n -4) + (2n + 5).
$$

$$
= (2k + 1) + (2L + 1)
$$

$$
= 2(K + L + 1)
$$

There is no way to prove this by vacuously true or trivially true. We need to come up with a lemma.

#### Proof:

Lemma: If $3n - 4$ is odd, then $n$ is odd.

Proof of Lemma: (By Contrapositive)

Assume $n = 2k$ where $k \in \mathbb{Z}$.

Bac

$$
3n - 4  = 3(2k) - 4
$$

$$
= 6k - 4
$$

$$
= 2(3k - 2)
$$

$$
= 2L
$$

Done Lemma.

Assume $3n - 4$ is odd.

By the Lemma, $n = 2k + 1 \ (k \in \mathbb{Z})$.

Bac

$$
5n + 1 = 5(2k + 1) + 1
$$

$$
= 10k + 6
$$

$$
= 2(5k + 3)
$$

$$
= 2L \ (L \in \mathbb{Z})
$$

Therefore $5n + 1$ is even.

Done Proof 1.

Assume $3n - 4 = 2k + 1$.

Note that $2n + 5 = 2L + 1$.

$$
(3n - 4) + (2n + 5) = (2k + 1) + (2L + 1)
$$

$$
5n + 1 = 2K + 2L + 2
$$

$$
= 2(K + L + 1)
$$

$$
= 2Q
$$

Conclude $5n + 1 = 2Q$.

Done Proof.

## Lecture 15:

The goal of today is to focus on Proof By Cases as opposed to Direct Proofs.
