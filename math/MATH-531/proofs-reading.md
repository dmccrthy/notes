# MATH 531: Proofs Reading

Book: [Mathematical Proofs:
A Transition to
Advanced Mathematics](https://www.amazon.com/Mathematical-Proofs-Transition-Advanced-Mathematics/dp/0134746759)

## Section 0: Communicating Mathematics

### Intro

-   Proofs are the basis for most regular math.
-   This book will teach you proofs

### 0.2 Symbol Best Practices

-   Don't start sentences with symbols
-   Try not to list symbols in your writing (avoid x, y, z, etc.)
-   Avoid using math symbols outside of there application
-   Try not to use i.e or e.g if you have variables with those letters
-   Write out integers in words if they aren't applicable to an equation.
-   Try not to mix symbols, where you could just write it out.
-   Explain what a symbol is when used (ex. x is a rational number)
-   Be consistent with the symbols/variables you use.

### 0.5 Writing Equations

When we write equations in our proofs we will typically add a line break and center the equation. If we need multiple lines we can do that. **Make sure the = signs are lined up**.

```
Bac,
    x = 1 + 2 + 3
      = 3 + 3
      = 6
```

### 0.6 Common Words

I, We, One, Lets - Avoid I. You really only use **We, or Lets**

-   Avoid Clearly, Obviously, Of Course, or Certainly (these make assumptions)
-   That, Which (Sometimes interchangeable)

## Section 1: Sets

### 1.2 Subsets

A set B is called a subset of A if all elementsof B are in A. So:

$A = \{1, 2, 3\}$

$B = \{1\}$

$B \subseteq A$

We also have this concept of **universal sets** which are just sets that contain an infinite number of elements. An example of this would be $\mathbb{R}$ which is the set of all real numbers (See def. for more of them).

Using the definition of a subset we can then prove that 2 sets are equal if:

$A = B$

$B \subseteq A$

$A \subseteq B$

### 1.3 Set Operations

The basic idea is, we can use a number of operations to create new sets from existing sets.

One example of this is the **Union** operations. This is pretty much addition; just combining 2 sets together.

$A = \{1, 2, 3\}$

$B = \{4\}$

$A \cup B = \{1, 2, 3, 4\}$

The opposite of a union is an **Intersection**. This finds the shared elements of 2 sets.

$A = \{1, 2, 3\}$

$B = \{2, 4\}$

$A \cap B = \{2\}$

We can also do some traditional subtraction on sets. This can be used to find **the unique elements of a set**

$A = \{1, 2, 3\}$

$B = \{2, 3\}$

$A - B = \{1\}$

**THE DIFFERENCE OPERATION CHANGES BASED ON ORDER**

$A - B \neq B - A$

The first element is the one you want to find unique values of.

Theres also this idea of sets being **Disjoint**. All this means is that 2 sets have no overlapping values. More formally this is written as:

$A \cap B = \emptyset$

Finally, we can take the **compliment** of a set. A compliment is simple everything thats not in the set. This can be described as:

$\overline A = U - A = \{x:  x \in U \ and \ x \notin A\}$

In this case $U$ could be many different things. Typically they will give the definition of $U$ as something like this:

$U = \mathbb{Z}$

### 1.4 Indexed Collections of Sets

Often times we will be asked to combine multiple sets using **unions** and **intersections**. When dealing with larger combinations of sets it can be difficult to write it all out in the regular notation (ie. $A \cup B$) which is why we have a different notation for this:

$\bigcup^N_{n=1} A_n = \{x: x \in A_n \ for \ some \ n, 1 \leq n \leq N\}$

For an element to be within this union it must be within one of the set $A_n$. This notation is very similiar to summation notation from calculus, but for unions instead.

Additional this same notation can be used for intersection as shown below:

$\bigcap^N_{n=1} A_n = \{x: x \in A_n \ for \ EVERY \ n, 1 \leq n \leq N \}$

The only real distinction here is that for the value to be within this intersection it must be in all sets, as opposed to the union which it can be in any.

**This chapter also cover index sets, but that is outside the scope of this course.**

### 1.6 Cartesian Products

When discussing sets we know that the order of elements in a set doesn't matter. There is another type of value called an **Ordered Pair** where this does matter. It is written as $(x, y)$. For ordered pairs to be equal their first elements must be equal and their second elements must be equal.

The **Cartesian Product** written as $A \times B$ is defined as a set containing ordered pairs where the first element $x$ belongs to $A$, and the second element $y$ belongs to $B$.

$A \times B = \{(a, b): a \in A \ and \ b \in B\}$

So for example we might write something like this:

$A = \{1, 2\}$

$B = \{4, 5\}$

$A \times B = \{(1, 4), (1, 5), (2, 4), (2, 5)\}$

Its important to note that the order of operations matters with Cartesian Products. This means that:

$A \times B \neq B \times A$

## Section 2: Logic

### 2.1 Statements

A **statement** is a declarative sentence or assertion that is either true or false (a boolean). Examples of this would be:

> 3 is odd.

> 12 is prime.

There sentence with a definitive true or false answer. When we talk about statements we sometimes us the term **Truth Value** to describe the answer to a statement. This value is either **T** for true, or **F** for false.

Statements can be more than just basic sentences like above. Often times we will refer to **Open Sentences** which are SENTENCES that include a variable of some kind, that when substituted out can give us a statement with a truth value.

$3x = 12$

This is an open statement. The statement here is only actually true when $x = 4$; in all other cases it is false. When dealing with these kinds of statements we will often use a **Truth Table** to right out the truth value for each given case. (we'll go into truth tables more in the following sections)

### 2.2 Negations

The negation of a statement $X$, is $not \ X$. This is written as:

$\neg X$ or ~$X$

In written form we can describe the negation of a statement like so:

> The integer 3 is odd.

> The integer 3 is **not** odd.

Thats it. This section is really short.

### 2.3 Disjunctions and Conjunctions

Often times we will combine statements with a logical "and" or "or". We describe the **disjunction** of 2 statements as:

> P **or** Q

Additionally we describe the **conjunction** as:

> P **and** Q

In math terms we can describe these 2 conditions as follows:

**Disjunction** - $P \lor Q$

**Conjunction** - $P \land Q$

A disjunction is defined as true, when **either** of the statements is true. Conjunctions are defined as true, when **both** statements are true.

### 2.4 Implications

The implication (or conditional) of 2 statements is described as:

> If P, then Q.

We write this as math like this:

$P \Rightarrow Q$

The truth table for an implication is described below.

| $P$ | $Q$ | $P \Rightarrow Q$ |
| --- | --- | ----------------- |
| T   | T   | T                 |
| T   | F   | F                 |
| F   | T   | T                 |
| F   | F   | T                 |

### 2.5 Further Implications

### 2.6 Biconditionals

### 2.7 Tautologies and Contradictions

### 2.8 Logical Equivalence

### 2.9 More Logical Equivalence

### 2.10 Quantified Statements
