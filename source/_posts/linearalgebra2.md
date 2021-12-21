---
layout: post
title: linear algebra notes 2
data: 2020-11-04
description: Eigenvalues
categories: Linear Algebra 
---

## Important

## Eigenvalues

Suppose the $n$ by $n$ matrix $A$ has $n$ linearly independent
eigenvectors. If these eigenvectors are the columns of a matrix $S ,$
then $S ^ { - 1 } A S$ is a diagonal matrix $\Lambda .$ The eigenvalues
of $A$ are on the diagonal of $\Lambda $

**Any matrix with distinct eigenvalues can be diagonalized.**

Not all matrices possess $n$ linearly independent eigenvectors, so not
all matrices are diagonalizable.

Diagonalizability of A depends on enough eigenvectors.\
Invertibility of A depends on nonzero eigenvalues.\
Diagonalization can fail only if there are repeated eigenvalues.

Diagonalizable matrices share the same eigenvector matrix $S$ if and
only if $A B = B A$

1. Every symmetric matrix (and Hermitian matrix) has real eigenvalues.

2. Its eigenvectors can be chosen to be orthonormal.

## complex

A real symmetric matrix can be factored into
$A = Q \Lambda Q ^ { \mathrm { T } } .$ Its orthonormal eigenvectors are
in the orthogonal matrix $Q$ and its eigenvalues are in $\Lambda .$

A complex matrix with orthonormal columns is called a unitary matrix.

If $A$ is Hermitian then $K = i A$ is skew-Hermitian.

Suppose that $B = M ^ { - 1 } A M .$ Then $A$ and $B$ have the same
eigenvalues. Every eigenvector $x$ of $A$ corresponds to an eigenvector
$M ^ { - 1 } x$ of $B .$

The matrices $A$ and $B$ that represent the same linear transformation
$T$ with respect to two different bases (the $v ^ { \prime }$ s and the
$V ^ { \prime }$ s) are similar:

There is a unitary matrix $M = U$ such that $U ^ { - 1 } A U = T$ is
triangular. The eigenvalues of $A$ appear along the diagonal of this
similar matrix $T .$

**Spectral Theorem** Every real symmetric $A$ can be diagonalized by an
orthogonal matrix $Q .$ Every Hermitian matrix can be diagonalized by a
unitary $U :$
$$\begin{aligned} Q ^ { - 1 } A Q = \Lambda \quad& \text { or } \quad A = Q \Lambda Q ^ { \mathrm { T } } \\ U ^ { - 1 } A U = \Lambda\quad & \text { or } \quad A = U \Lambda U ^ { \mathrm { H } } \end{aligned}$$
The columns of $Q ($ or $U )$ contain orthonormal eigenvectors of $A$

## Normal

The matrix $N$ is normal if it commutes with
$$N N ^ { \mathrm { H } } = N ^ { \mathrm { H } } N .$$
 For such matrices, and no others, the triangular $T = U ^ { - 1 } N U$ is the
diagonal $\Lambda$ Normal matrices are exactly those that have a
complete set of orthonormal eigenvectors.

1. $A$ is diagonalizable: The columns of $S$ are eigenvectors and
    $S ^ { - 1 } A S = \Lambda$

2. $A$ is arbitrary: The columns of M include “generalized
    eigenvectors” of $A ,$ and the Jordan form $M ^ { - 1 } A M = J$ is
    block diagonal.

3. $A$ is arbitrary: The unitary $U$ can be chosen so that
    $U ^ { - 1 } A U = T$ is triangular.

4. $A$ is normal, $A A ^ { \mathrm { H } } = A ^ { \mathrm { H } } A :$
    then $U$ can be chosen so that $U ^ { - 1 } A U = \Lambda$ *Special
    cases of normal matrices, all with orthonormal eigenvectors:*

    1. If $A = A ^ { H }$ is Hermitian, then all $\lambda _ { i }$ are
        real.

    2. If $A = A ^ { T }$ is real symmetric, then $\Lambda$ is real and
        $U = Q$ is orthogonal.

    3. If $A = - A ^ { H }$ is skew-Hermitian, then all
        $\lambda _ { i }$ are purely imaginary.

    4. If $A$ is orthogonal or unitary, then all
        $\left| \lambda _ { i } \right| = 1$ are on the unit circle.
