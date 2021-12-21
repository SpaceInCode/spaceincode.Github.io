---
layout: post
title: linear algebra notes 1-2
data: 2020-11-04
description: Linear space
categories: Linear Algebra 
---


## Linear Space

A *Vector space* is a set $V$ along with an additiont on $V$ and a
scalar multiplication on $V$ such that the following properties hold:

1. **commutativity**\
    $u+v=v+u$ for all $u,v \in V$ ;

2. **associativity**\
    $(u+v)+w=u+(v+w) $ and $(ab)v=a(bv)$ for all $u,v,w  \in V $ and all
    $a,b \in \textbf{F}$;

3. **addictive identity**\
    there exists an element $0\in V$ such that $v+0=v$ for all $v\in V$;

4. **addicyive inverse**\
    for every $v\in V$ ,there exists $w \in V$ such that $v+w=0$;

5. **multiplicative identity** $1v=v$ for all $v \in V$

6. **distributive properties** $a(u+v)=au+av$ and $(a+b)v=av+bv$ for
    all $a,b\in \textbf{F}$ and all $u,v\in V$.

A subset $U$ of $V$ is called a *subspace* of $V$ if $U$ is also a
vector space (using the same addition and scalar multiplication as on
$V$).

A *subspace* of a vector space is a nonempty subset that satisfies the
requirements for a vector space: Linear combinations stay in the
subspace.

The system $A x = b$ is solvable if and only if the vector $b$ can be
expressed as a combination of the columns of $A .$ Then $b$ is in the
column space. We can describe all combinations of the two columns
geometrically: $A x = b$ can be solved if and only if b lies in the
plane that is spanned by the two column vectors.

The nullspace of a matrix consists of all vectors $x$ such that
$A x = 0 .$ It is denoted by $N ( A ) .$ It is a subspace of
$\mathbf { R } ^ { n } ,$ just as the column space was a subspace of
$\mathbf { R } ^ { m } .$

$A x _{ p } = b$ and $A x_ { n } = 0 \quad$ produce
$\quad A \left( x _{ p } + x_ { n } \right) = b$

$$R x = \left[ \begin{array} { l l l l } { 1 } & { 3 } & { 0 } & { - 1 } \\ { 0 } & { 0 } & { 1 } & { 1 } \\ { 0 } & { 0 } & { 0 } & { 0 } \end{array} \right] \left[ \begin{array} { l } { u } \\ { v } \\ { w } \\ { y } \end{array} \right] = \left[ \begin{array} { l } { 0 } \\ { 0 } \\ { 0 } \end{array} \right]$$
The unknowns $u , v , w , y$ go into two groups. One group contains the
pivot variables, those that correspond to columns with pivots.

If $A x = 0$ has more unknowns than equations $( n > m ) ,$ it has at
least one special solution: There are more solutions than the trivial
$x = 0$

$x _{ \mathrm{complete} } = x_ { \mathrm{particular} } + x _ {\mathrm{  nullspace }}$

The columns of A are independent exactly when $N ( A ) = \{$ zero vector
$\}$

## Basis

Suppose $c _{ 1 } v_ { 1 } + \cdots + c _{ k } v_ { k } = 0$ only
happens when $c _{ 1 } = \cdots = c_ { k } = 0 .$ Then the vectors
$v _{ 1 } , \ldots , v_ { k }$ are linearly independent. If any
$c ^ { \prime }$ are nonzero, the $v ^ { \prime } \mathrm { s }$ are
linearly dependent. One vector is a combination of the others.

To check any set of vectors $v _{ 1 } , \ldots , v_ { n }$ for
independence, put them in the columns of $A .$ Then solve the system
$A c = 0 ;$ the vectors are dependent if there is a solution other than
$c = 0 .$ With no free variables ( rank is $n$) , there is no nullspace
except $c = 0 ;$ the vectors are independent. If the rank is less than
$n ,$ at least one free variable can be nonzero and the columns are
dependent.

A set of n vectors in $\mathbf { R } ^ { m }$ must be linearly dependent
if $n > m$

A basis for $\mathrm { V }$ is a sequence of vectors having two
properties at once:

1. The vectors are linearly independent (not too many vectors).

2. They span the space V (not too few vectors).

Any two bases for a vector space $\mathbf { V }$ contain the same number
of vec- tors. This number, which is shared by all bases and expresses
the number of $\cdot$ degrees of freedom" of the space, is the dimension
of $\mathbf { V } .$

If $v _{ 1 } , \ldots , v_ { m }$ and $w _{ 1 } , \ldots , w_ { n }$
are both bases for the same vector space, then $m = n .$ The number of
vectors is the same.

Suppose there are more $w ^ { \prime }$ s than
$v ^ { \prime } \mathrm { s } ( n > m ) .$ We will arrive at a
contradiction. Since the $v ^ { \prime }$ s form a basis, they must span
the space. Every $w _{ j }$ can be written as a combination of the v’s:
If $w_ { 1 } = a _{ 11 } v_ { 1 } + \cdots + a _{ m 1 } v_ { m } ,$
this is the first column of a matrix multiplication $V A :$
$$W = \left[ \begin{array} { l l l l } { w _ { 1 } } & { w _ { 2 } } & { \cdots } & { w _ { n } } \end{array} \right] = \left[ \begin{array} { c c c } { v _ { 1 } } & { \cdots } & { v _ { m } } \end{array} \right] \left[ \begin{array} { c } { a _ { 11 } } \\ { \vdots } \\ { a _ { m 1 } } \end{array} \right] = V A$$
We don’t know each $a _{ i j } ,$ but we know the shape of $A$ (it is
$m$ by $n ) .$ The second vector $w_ { 2 }$ is also a combination of
the $v ^ { \prime }$ . The coefficients in that combination fill the
second column of $A .$ The key is that $A$ has a row for every $v$ and a
column for every $w . A$ is a short, wide matrix, since $n > m .$ There
is a nonzero solution to $A x = 0 .$ Then $VA x = 0$ which is $Wx = 0 .$
A combination of the $w$ ’s gives zero! The $w ^ { \prime }$ s could not
be a basis $-$ so we cannot have $n > m$

If $m > n$ we exchange the $v ^ { \prime }$ s and $w ^ { \prime }$ and
repeat the same steps. The only way to avoid a contradiction is to have
$m = n .$ This completes the proof that $m = n .$ To repeat: The
dimension of a space is the number of vectors in every basis.

The row space of $A$ has the same dimension $r$ as the row space of
$U ,$ and it has the same bases, because the row spaces of $A$ and $U ($
and $R )$ are the same.

The dimension of the column space $C ( A )$ equals the rank $r ,$ which
also equals the dimension of the row space: The number of independent
columns equals the number of independent rows. A basis for $C ( A )$ is
formed by the $r$ columns of $A$ that correspond, in $U ,$ to the
columns containing pivots.

Roughly speaking, an inverse exists only when the rank is as large as
possible.
