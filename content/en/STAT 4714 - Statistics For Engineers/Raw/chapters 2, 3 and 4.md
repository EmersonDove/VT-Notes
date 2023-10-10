---
title: Chapters 2 and 3
position: 1
category: STAT 4714
---

# Lecture 2

The first 1 & 2 chapters are basically all garbage. Come on. You know that stuff get over it. I'm going to talk about chapters 3+

## Laws

$$
\text{Commutative}\\
A \cup B = B\cup A\\
A\cap B=B\cap A\\
\text{Associativity}\\
(A\cup B) \cup C = A\cup (B\cup C)\\
(C \cap B) \cap C = A \cap (B \cap C)\\
\text{Distributive}\\
A\cap (B\cup C) = (A \cap B) \cup (A\cap C)\\
A \cup (B \cap C) = (A \cup B) \cap (A \cup C)\\
\text{DeMorgan's}
(A\cup B)^c = A^c \cap B^c\\
(A \cap B) ^ c = A^c \cup B^c
$$

## Pemutations

$n! = n \times (n-1) \times (n - 2) \times ...$

## Laws Of Probability

### Addition Rules

For mutually exclusive sets (like for example hair color) then $P(A \cup B) = P(A) + P(B)$

If A and B are **not** mutually exclusive (like a worm, virus or both) then $P(A\cup B) = P(A) + P(B) - P(A \cap B)$.

### Complement Rule

For any event $A, P(A^C) = 1 - P(A)$

### Fun Bonus Rules

$P(B \cup A ^C) = P(B) - P(A \cup B)$

If A is a subset of B, then $P(A) \leq P(B)$

### Examples

Let V be the event that a computer has a virus. Let W be the event that a computer has a worm. Suppose P(V) = 0.15, P(W) = 0.05, and $P ( V\cup W) = 0.17$.

1. Probability of both a worm and a virus: $P(V \cap W)$?

   1. $$
      P(A \cup B) = P(A) +P(B) - P(A \cap B)\\
      \text{So}\\
      P(V \cup W) = P(V) + P(W) - P(V \cup W)\\
      = 0.15 + 0.05 +0.17\\
      =0.03
      $$

   2. $$
      =1-0.37 = 0.97
      $$

# Lecture 3

"If B, then what I the probability of A" this also means "A given B"

$P(A | B) = \frac{P(A \cap B)}{P(B)}$ and of course $P(B) > 0$

This is for quantifying the relationship between two events.

## Marginal Distribution

Uhhhhhh just add together all the irrelevant variables. Like in the total column we're marginalizing the hair color

|           | Brown Eyes | Black Eyes | Total    |
| --------- | ---------- | ---------- | -------- |
| Red har   | 5          | 6          | 11       |
| Blue hair | 6          | 5          | 11       |
|           |            |            | 22 total |

So $P(\text{Hair Color} == \text{red}) = 11/22$

So $P(\text{Hair Color} == \text{blue}) = 11/22$

## Independent Events

Just make sure that the probability of one thing given another is the same as initial probability. Is the probability of red hair given brown eyes the same as the probability of red hair? If so then the brown eyes have no influence.

## Multiplicative Law of Probability

If A and B are two events with $P(B) > 0$ and $P(A) > 0 $, then
$$
P(B|A) = \frac{P(A \cap B)}{P(A)} \implies P(A \cap B) = P(B | A)P(A).
$$
Similarly we can have
$$
P(A|B) = \frac{P(A\cap B)}{P(B)}\implies P(A \cap B) = P(A|B)P(B)
$$
If A and B are independent:
$$
P(A \cap B) = P(A) P(B)
$$
Now given the multiplicative rules we have three way to check for independence:

1) $P(B) = P(B|A)$
2) $P(A) = P(A|B)$
3) $P(A \cap B) = P(A) P(B)$

If any of the above are true then they're all true.

## Total Law of Probability

Really intuitively (if I had the diagram here). If $P(A) \neq 0, P(A^C) \neq 0, P(B) \neq 0$. Then 

$P(B) = P(B|A) \times P(A) + P(B | A^C) \times P(A^C)$

## Gigachad Bayes' Rule

Combine total law of probability with the multiplicative rule.
$$
P(A|B) = \frac{P(A \cap B)}{P(B)} = \frac{P(B|A)P(A)}{P(B|A)\times P(A) + P(B | A^C)P(A^C)}
$$
This is important, notice the denominator of the rule is just the probability of B directly.

## General Bayes' Rule
Let $A_1,...,A_n$ be mutally exclusive and exhaustive events with $P(A_i)\neq 0$ for each $A_i$. Furthermore, let B be any event with $P(B_i)\neq 0$. Then
$$
P(A_k | B) = \frac{P(B|A)P(A_k)}{\sum_{i=1}^K P(B|A_i)P(A_i)}
$$
Basically the same thing as above but you sum all the denominators it's dependent on. Intersect the denominators as all the bases.
