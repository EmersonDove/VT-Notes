---
title: Exam 3
position: 3
category: MATH 2114 - Linear Algebra
---

# Exam 3

## Fast Determinant

If *A* is an upper triangle, lower triangle or diagonal matrix then
$det(A) = A_{11}A_{22} \cdots A_{nn}$

To do this you also need to make sure:

1. Switching any two rows of a matrix reverses the sign of the determinant
2. If the matrix has two identical rows or columns, then det(*A*) $=0$
3. If *B* is a matrix obtained by multiplying a row or column of *A* by a scalar *k*, then $det(B) = k\ det(A)$
4. If *B* is a matrix obtained from *A* by adding a multiple of row *I* to row *j* or a multiple of column *I* to column *j* for $i\neq j,$ then $det(B) = det(A)$.

### Properties

$det(AB) = det(A)det(B)$

$det(A^T) = det(A)$

If *A* is not invertible, then $det(A) = 0$

*A* is invertible if and only if $det(A) \neq 0$

## Eigenvalues

You can find characteristic equation with $det(A- \lambda I) =0$

The eigenvectors are vectors in $null(A - \lambda I)$

The algebraic multiplicity is how many times the eigenvalue shows up in the diagonal of a reduced matrix.

The geometric multiplicity can never exceed the algebraic multiplicity.

Find geometric multiplicity by looking for the dimension of the null space of $A-\lambda I$. This is the dimension of the eigenspace of $\lambda$

### Dominant Eigenvalue

Eigenvalue with the highest magnitude, $-10$ is dominant over $3$.

## Matrix Powers

To calculate $A^k x$ for any $x$ we need a basis for $R^n$ consisting of eigenvectors of *A*.

This works because $A\vec{v} = \lambda \vec{v}$

So $A^3\vec{v} = A(A(A\vec{v})) \rarr A(A(\lambda \vec{v}))$ 

You can also decompose linear combinations and use the process above to sum: $A^4(a\bold{v_1}+b\bold{v_2}) = A^4a \vec{v_1}+bA^4\vec{v_2}$

## Diagonalization

$A=PDP^{-1}$

Also $A^k = PD^k P ^{-1}$

If there exists an interpretable matrix *P* and a diagonal matrix *D* such that $A=PDP^{-1}$, we say that *A* is diagonalizable.

To diagonalize:

1. Find eigenvalues of matrix 
2. Find eigenspace (basis) from each eigenvalue
3. This may need to occur multiple times
4. The geometric multiplicity must be equal to the algebraic multiplicity for both eigenvalues
5. Create a matrix from these eigenvalues as *P*
6. Put the eigenvalues corresponding with each eigenvector into the diagonal of another matrix
7. Multiply by $P^{-1}$

If a *n x n* matrix has *n* distinct eigenvalues, then *A* **is** diagonalizable

If the same matrix does not have *n* eigenvalues the matrix could be diagonalizable

Matrixes are similar (~) if there exists an invertible *n x n* matrix *P* such that $B=P^{-1}AP$. 

1. A~A
2. If A~B, then B~A
3. If A~B and B~C then A~C

Two similar matrices have the properties:

1. det(A) = det(B)
2. A is invertible if and only if B is invertible
3. rank(A) = rank(B)
4. A and B have same characteristic polynomial
5. A and B have same eigenvalues
6. $A^m$ ~ $B^m$ For all positive integers *m*
7. If *A* is invertible, then $A^m$ ~ $B^m$ for all integers *m*

## Perp & Orthogonality

$(col(A))^\perp = null(A^T)$

$dim(W) + dim(W^{\perp}) = n$ in $\R^n$

$perp_{w}(v) = v-proj_w(v)$

$W^\perp = null(A^T)$

## Normal Equations

$A^T Ax = A^T b$

You can find the projection of *b* by multiplying the normal solution back to the original matrix.