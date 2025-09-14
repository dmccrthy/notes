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

Given: $A = \{1, 2, 3\}$ and $B = \{m \in Z: 0 < m < 5\}$

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
