# Discrete Math Test 1

## Number Symbols

$\Z$ - integers

$\Q$ - rationals

$\R$ - reals

$\C$ - complex numbers

And of course this where $\sub$ means subset of.

$\Z \sub \Q \sub \R \sub \C$

Tautology: Something that's always true regardless of truth values

Contradiction: Something that is always false regardless of truth values

## Table of Crazy Equivalence

| Law              | 1                                                  | 2                                                  |
| ---------------- | -------------------------------------------------- | -------------------------------------------------- |
| Distributive Law | $p \and (p \or r)\equiv (p\and q) \or (p  \and r)$ | $p \or (q \and r) \equiv (p \or q) \and (p \or r)$ |
| Demorgan's Law   | $\sim (p \and q) \equiv \sim p \or \sim q$         | $\sim (p \or q) \equiv \sim p \and \sim q$         |
| Absorption Law   | $p \or (p \and q) \equiv p$                        | $p \and (p \or q) \equiv p$                        |



## Equivalence

$\neg \or q  \equiv p \implies q$

$\neg (p \implies q) \equiv p \and \neg q$

|      |      |      |      | conditional   | Contrapositive          | Converse       | Inverse                  |
| ---- | ---- | ---- | ---- | ------------- | ----------------------- | -------------- | ------------------------ |
| p    | q    | ~p   |      | $p\implies q$ | $\sim q\implies \sim p$ | $q \implies p$ | $\sim p \implies \sim q$ |
|      |      |      |      |               |                         |                |                          |
|      |      |      |      |               |                         |                |                          |
|      |      |      |      |               |                         |                |                          |
|      |      |      |      |               |                         |                |                          |

- The **conditional** and its **contrapositive** are logically equivalent. That is, "If P, then Q" is logically equivalent to "If not Q, then not P".
- The **converse** and **inverse** are also logically equivalent to each other. However, they are not necessarily logically equivalent to the original conditional statement.

The negation of a **conditional** is $p \implies q \equiv p \and \sim q$

These two groups being logically equivalent is somewhat obvious if you think about it, because they're both doing the same thing - taking a statement than then flipping and negating the terms wow.

## Biconditional Statements

This is an underrated equivalence:

$(p \iff q) \equiv (p \implies q) \and (q \implies p)$

Breaking it down more

$r \iff q \equiv (r \and p) \or (\sim r \and \sim p)$

Obviously though right, this is just breaking down what if and only if means.

## Predicate and Quantifier and the Quantified Statement

A predicate is a statement that contains a variable and becomes either  true or false depending on the value that you assign to the variable. In essence, a predicate asserts something about the subject, often  specifying a property or relation. For example, in the statement "x is  even", "is even" is a predicate. Depending on the value of x, this  statement will be true or false. Predicates can be more complex and  involve multiple variables, e.g., "x is greater than y".

A quantifier specifies the quantity or scope of the elements for which a predicate holds within a certain domain. There are two primary types of quantifiers like universal and existential quantifier.

Quantified statements are formed by attaching quantifiers to predicates, which specify how many or which elements of the domain satisfy the  predicate. This is the whole statement together.

### Contrapositive of a Conditional Statement

$\forall x, P(x) \implies Q(x)$

then

$\forall x, \sim Q(x) \implies \sim P(x)$

## Negating Statements

Negation of

$\forall x \in D, Q(x)$

Is 

$\exists x \in D | \sim Q(x)$

The negation of

$\exists x \in D | Q(x)$

Is

$\forall x \in D, \sim Q(x)$

## Negating Conditional Statements

$\sim (\forall x , if\ P(x), \ then \ Q(x))\equiv \exists x\  such \ that\ \sim (P(x) \implies x)$

$\equiv \exists x\ such\ that\ P(x) \and \sim Q(x)$

# Proof Lore

### Closure

The integers are closed under addition, subtraction and multiplication

### Even

An integer $n$ is even if and only if n equals twice some integer.

### Odd

An integer $n$ is odd if and only if $n$ equals twice some integer plus 1

### Prime

An integer is prime if and only if $n>1$ and for all positive integers $r$ and $s$, if $n=rs$, then either $r$ or $s$ equals $n$

An integer $n$ is composite if and only if $n>1$ and $n=rs$ for some integers $r$ and $s$ with $1<r<n$ and $1<s<n$.

### Rational

A real number $r$ is rational if and only if it can be expressed as a quotient of two integers with nonzero denominator.

### Divisibility

Let $n$ and $d$ be integers such that  $d\neq 0$/ Then we say that $n$ is divisible by $d$ if and only f, $n$ equals $d$ times some integer.

$d|n$ reads divisible by.

Or $d|n \iff k \in \Z$ such that $n=dk$.