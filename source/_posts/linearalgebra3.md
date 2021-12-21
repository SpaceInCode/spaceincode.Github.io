---
layout: post
title: linear algebra notes 3
data: 2020-11-04
description: Positive definite
categories: Linear Algebra 
---

## Positive definite

$ a x ^ { 2 } + 2 b x y + c y ^ { 2 }$ is positive definite if and only
if $a > 0$ and $a c > b ^ { 2 } .$ Any $f ( x , y )$ has a minimum at a
point where $\partial F / \partial x = \partial F / \partial y = 0$ with

$$\frac { \partial ^ { 2 } F } { \partial x ^ { 2 } } > 0 \quad \qquad \left[ \frac { \partial ^ { 2 }F  } { \partial x ^ { 2 } } \right] \left[ \frac { \partial  ^ { 2 }F } { \partial y ^ { 2 } } \right] > \left[ \frac { \partial ^ { 2 } F } { \partial x \partial y } \right] ^ { 2 }$$

$$F ( x ) = F ( 0 ) + x ^ { \mathrm { T } } ( \text{ grad } F ) + \frac { 1 } { 2 } x ^ { \mathrm { T } } A x +\text{higher order terms}$$

At a stationary point,
$\nabla F = \left( \partial F / \partial x _{ 1 } , \ldots , \partial F / \partial x_ { n } \right)$
is a vector of zeros.

$$a x ^ { 2 } + 2 b x y + c y ^ { 2 } = a \left( x + \frac { b } { a } y \right) ^ { 2 } + \frac { a c - b ^ { 2 } } { a } y ^ { 2 }$$

Each of the following tests is a necessary and sufficient condition for
the real symmetric matrix $A$ to be positive definite:

1. $x ^ { \mathrm { T } } k x > 0$ for all nonzero real vectors $x$ .

2. All the eigenvalues of $A$ satisfy $\lambda _ { i } > 0$

3. All the upper left submatrices $A _ { k }$ have positive
    determinants.

4. All the pivots (without row exchanges) satisfy $d _ { k } > 0 .$

5. There is a matrix $R$ with independent columns such that
    $A = R ^ { \mathrm { T } } R .$

The key is to recognize $x ^ { \mathrm { T } } A x$ as
$x ^ { \mathrm { T } } R ^ { \mathrm { T } } R x = ( R x ) ^ { \mathrm { T } } ( R x )$

symmetric matrix $A$ to be positive semidefinite:

1. $x ^ { \mathrm { T } } A x \geq 0$ for all vectors $x$ (this defines
    positive semidefinite)

2. All the eigenvalues of $A$ satisfy $\lambda _ { i } \geq 0$

3. No principal submatrices have negative determinants.

4. No pivots are negative.

5. There is a matrix $R ,$ possibly with dependent columns, such that
    $A = R ^ { \mathrm { T } } R$

$$5 u ^ { 2 } + 8 u v + v ^ { 2 } = \left( \frac { u } { \sqrt { 2 } } - \frac { v } { \sqrt { 2 } } \right) ^ { 2 } + 9 \left( \frac { u } { \sqrt { 2 } } + \frac { v } { \sqrt { 2 } } \right) ^ { 2 } = 1$$

Any ellipsoid $x ^ { \mathrm { T } } A x = 1$ can be simplified in the
same way. The key step is to diago- nalize
$A = Q \Lambda Q ^ { \mathrm { T } } .$ We straightened the picture by
rotating the axes. Algebraically, the change to $y = Q ^ {T} x$ produces
a sum of squares:
$$x ^ { \mathrm { T } } A x = \left( x ^ { \mathrm { T } } Q \right) \Lambda \left( Q ^ { \mathrm { T } } x \right) = y ^ { \mathrm { T } } \Lambda y = \lambda _{ 1 } y_ { 1 } ^ { 2 } + \cdots + \lambda _{ n } y_ { n } ^ { 2 } = 1$$

Suppose $A = Q \Lambda Q ^ { \mathrm { T } }$ with
$\lambda _{ i } > 0 .$ Rotating $y = Q ^ { \mathrm { T } } x$
simplifies $x ^ { \mathrm { T } } A x = 1 :$
$$x ^ { \mathrm { T } } Q \Lambda Q ^ { \mathrm { T } } x = 1  \qquad y ^ { \mathrm { T } } \Lambda y = 1 ,\qquad \lambda_ { 1 } y _{ 1 } ^ { 2 } + \cdots + \lambda_ { n } y _ { n } ^ { 2 } = 1$$

Congruence transformation $ A \rightarrow C ^ { \mathrm { T } } A C$ for
some nonsingular $C .$

$C ^ {T } A C $ has the same number of positive eigenvalues, negative
eigenvalues, and zero eigenvalues as $A .$

For any symmetric matrix $A ,$ the signs of the pivots agree with the
signs of the eigenvalues. The eigenvalue matrix $\Lambda$ and the pivot
matrix $D$ have the same number of positive entries, negative entries,
and zero entries.

The graph of $$P ( x ) = \frac { 1 } { 2 } A x ^ { 2 } - b x$$ has zero
slope when $$\frac { d P } { d x } = A x - b = 0$$

If $A$ is symmetric positive definite, then
$$P ( x ) = \frac { 1 } { 2 } x ^ { \mathrm { T } } A x - x ^ { T } b$$
reaches its minimum at the point where $A x = b .$ At that point
$$P _ { \min } = - \frac { 1 } { 2 } b ^ { \mathrm { T } } A ^ { - 1 } b$$

$$P _ { \min } = \frac { 1 } { 2 } \left( A ^ { - 1 } b \right) ^ { \mathrm { T } } A \left( A ^ { - 1 } b \right) - \left( A ^ { - 1 } b \right) ^ { \mathrm { T } } b = - \frac { 1 } { 2 } b ^ { \mathrm { T } } A ^ { - 1 } b$$

$$L ( x , y ) = P ( x ) + y ^ { \mathrm { T } } ( C x - d ) = \frac { 1 } { 2 } x ^ { \mathrm { T } } A x - x ^ { \mathrm { T } } b + x ^ { \mathrm { T } } C ^ { \mathrm { T } } y - y ^ { \mathrm { T } } d$$

$$\quad P _{ C / \min } = P_ { \min } + \frac { 1 } { 2 } y ^ { \mathrm { T } } \left( C A ^ { - 1 } b - d \right) \geq P _ { \min }$$
