[TOC]

# Linear Algebra Exam 1

# Unit 1

## Length and Dot Products

### Length Definition

The <u>length</u> or <u>magnitude</u> of a vector **x** in $\R^m$ is defined to be
$$
||x|| = \sqrt{x^2_1+x^2_2+ \cdot\cdot\cdot+x_n^2} = \sqrt{x\cdot x}
$$

### Theorem 1

For any vector **x** in $\R^n$ and scalar *c* in $\R$ we have

1. $||x|| = 0$ If and only if $x=0$
2. $||cx||=|c|||x||$

### Unit Vector Definition

A vector **u** is called a <u>unit vector</u> if $||u||=0$

### Distance Definition

The <u>distance</u> $d(x,y)$ between vectors **x** and **y** in $\R^n$ is defined by $d(x,y) = ||x-y||$

### Dot Product Definition

The <u>dot product</u> of vectors **x, y** in $\R^n$ is the scalar in $\R$ defined by $x\cdot y = x_1y_1 + x_2v_2 + \cdots + x_n y_n$

## Matrices and Matrix Operations

### Theorem 1

If *A* is a $m\times k$ matrix, $B$ is a $k \times n $ matrix, *C* is a $n\times p$ matrix, then $(AB)C=A(BC)$

### Theorem 2

If *A* is a $m\times k$ matrix and *B* is a $k\times n $ matrix then $(AB)^T=B^TA^T$

### Consequence of Linearity

Let *A* be a $m\times n$ matrix and **b** a vector in $\R^m$. Then *exactly one* of the following is true.

1. $Ax=b$ has no solution
2. $Ax=b$ has exactly one unique solution
3. $Ax=b$ has an infinite number of solutions

### Properties

In general: **AB $\neq$ BA**
$$
A(B+C) = AB +AC\\
\text{it is associative}\\
(A+B)C=AC+BC = ABC\\
$$
The transpose $A^T$ of A is the matrix obtained by flipping the rows and columns of A
$$
\begin{bmatrix}
1 & 2 & 3\\
4 & 5 & 6\\
\end{bmatrix}^T=
\begin{bmatrix}
1 & 4\\
2 & 5\\
3 & 6
\end{bmatrix}\\

A^T=A\\
(AB)^T=B^TA^T
$$
A is symmetric if $A^T=A$, example::
$$
\begin{bmatrix}
1 & 2 & 3\\
2 & 0 & 4\\
3 & 4 & 5
\end{bmatrix}
$$
Suppose $\vec{v_1}\ and\ \vec{v_2}$
$$
A\vec{v_1} = \begin{bmatrix}2\\ 3 \end{bmatrix},\ 
A\vec{v_2} = \begin{bmatrix}5\\ 0 \end{bmatrix}\\
\text{then}\\ A(3\vec{v_1} + 2\vec{v_2}) =
3A\vec{v_1} + 2A\vec{v_2} = 3\begin{bmatrix}2\\ 3 \end{bmatrix} + 2 \begin{bmatrix}5\\ 0 \end{bmatrix} = \begin{bmatrix}16\\ 9 \end{bmatrix}
$$

### Matrix-Vector Products

$$
Ax=\begin{bmatrix}
a_{11} & a_{12} & \cdots & a_{1n}\\
a_{21} & a_{22} & \cdots & a_{2n}\\
\vdots & \vdots & \ddots & \vdots\\
a_{m1} & a_{m2} & \cdots & a_{mn}\\
\end{bmatrix}
\begin{bmatrix}
x_1\\
x_2\\
\vdots\\
x_n
\end{bmatrix}=
x_1
\begin{bmatrix}
a_11\\
a_21\\
\vdots\\
a_{m1}
\end{bmatrix}+
x_2
\begin{bmatrix}
a_12\\
a_22\\
\vdots\\
a_{m2}
\end{bmatrix}
+
\cdots
+
x_n
\begin{bmatrix}
a_{1n}\\
a_{2n}\\
\vdots\\
a_{mn}
\end{bmatrix}
$$

# Unit 2

## Solving Linear Systems

### Augmented Matrix Definition

Consider the linear system $Ax=b$ where *A* is a $m\times n$ matrix and **b** is in $\R^m$. We call the matrix *A* the corresponding <u>coefficient matrix</u> and the $m \times (n+1)$ matrix $\begin{bmatrix}A & | & b \end{bmatrix}$ the corresponding <u>augmented matrix.</u>

### Elementary Row Operations Definition

The following three operations on the rows of any matrix are called <u>elementary row operations.</u>

1. Interchange any two rows.
2. Multiply any row by a <u>nonzero</u> scalar.
3. Add any scalar multiple of a row to another row

### Row Equivalence Definition

We call two matrices with the same number of rows and columns <u>row equivalent</u> if there is a sequence of elementary row operations that converts one matrix into the other.

Two $m\times n$ linear systems with corresponding augmented matrices that are *row equivalent* have *exactly the same set of solutions.*

## Matrix Rank and General Solution

### Matrix Rank Definition

The rank of matrix A, denoted rank($A$), is the number of nonzero rows in any matrix *B* in row echelon form that is row equivalent to *A*.

### General Solution Definition

The <u>general solution</u> of a linear system is a formula for each variable (possibility containing parameters) that generates *all* solutions of the linear system.

### Theorem 1:

If *A* is a $m\times n$ matrix, then the linear system $Ax=b$ has a solution for all **b** in $\R^m$ if and only if rank(*A*) = $m$.

## RREF

### RREF Definition

A matrix is said to be in reduced row echelon form if

1. It is in *row echelon form*
2. The first nonzero entry in each row is 1.
3. The first nonzero entry one each row is the only nonzero entry in its column

### Theorem 1

Ever matrix is row equivalent to a *unique* matrix in reduce row echelon form (RREF).

## Homogeneous Linear System

### Homogeneous Linear System Definition

A $m\times n$ linear system is called <u>homogeneous</u> if $b_1 = b_2=\cdots=b_m=0$:
$$
a_{11}x_1+a_{12}x_2+\cdots+a_{1n}x_n=b_1\\
a_{21}x_1+a_{22}x_2+\cdots+a_{2n}x_n=b_2\\
\vdots\\
a_{m1}x_1+a_{m2}x_2+\cdots+a_{mn}x_n=b_m\\
$$

## Span

### Span Definition

We call the <u>set</u> of all <u>linear combinations</u> of the vectors $v_1,v_2,...,v_n$ in $\R^m$ the <u>span</u> of the vectors $v_1,v_2,...,v_n$ which we denote $span(v_1,v_2,...,v_n)$. We say that the vectors $v_1,v_2,...,v_n$ <u>span</u> $\R^m$ if $span(v_1,v_2,...,v_n) = \R^m$ 

### Theorem 1

Let A be a $m\times n$ matrix with column vectors $v_1,v_2,...,v_n$ and **b** be a vector in $\R^m$. The linear system $Ax=b$ is consistent if and only if **b** is in $span(v_1,v_2,...,v_n)$.

### Theorem 2

Let A be a $m\times n$ matrix with column vectors $v_1,v_2,...,v_n$, then the following three statements are equivalent (all true or false):

1. $rank(A) = m$
2. The linear system $Ax=b$ has a solution for all **b** in $\R^m$
3. $span(v_1,v_2,...,v_n) = \R^m$

## Linear Independence

### Linear Independence Definition

The vectors $v_1,v_2...,v_n$ in $\R^m$ are called <u>linearly independent</u> if the homogeneous linear system $x_1 v_1 + x_2v_2 +...+x_nv_n=0$ has only the *trivial solution* **x=0** and <u>linearly dependent</u> if the equation has a *nonzero solution*.

### Theorem 1

Vectors $v_1,v_2,...,v_n$ in $\R^m$ are linearly dependent if and only if one of the vectors $v_i$ is in $span(v_1,...,v_{i-1},v_{i+1},...,v_n)$ 

### Theorem 2

Let A be a $m\times n$ matrix with column vectors $v_1,v_2,...,v_n$. Then the following three statements are equivalent (all true or false):

1. $rank(A)=n$
2. The homogeneous linear system $Ax=0$ has the *unique* solution **x=0**
3. The vectors $v_1,v_2,...,v_n$ are linearly independent

Interpretation, if the number of filled rows is equal to the number of columns, all vectors are linearly dependent.

## Note on Rank:

$Rank(A)= dim(Col(A))$

