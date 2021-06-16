---
layout: post
title: linear algebra notes
data: 2020-11-04
categories: Linear Algebra 
---
If the columns of $ A$ are linearly independent, then $Ax=b$ has exactly one solution for every $b$.

It’s false. That is because there may be a case that $rank(A)<m$ , which means the vector $b$ couldn’t be expressed by $A$. 

Given $n$ vectors $a_i$ with $m$ components, what are the shapes of $A,Q,R$ ?

The expression is $$A_{m\times n} = Q_{m\times n}R_{n\times n}$$

Suppose that $A=A_{m\times n}$, $B=B_{s\times t}$, $C=C_{s\times t}$ are matrices, then 
$$
rank \left[
    \begin{array}{cc}
    A & O \\
    C & B \\
    \end{array}
    \right]
    \geq rank(A)+rank(B)
$$

It’s true. Because if the rank of $A$ equals $1$ , the rank of $B$ equals $2$, this satisfies the expression. (Assume that $m=n=s=t=2$)

Give transformation to find the transform matrix.

We know that
$\mathscr{A}(\varepsilon_1 \varepsilon_2 \cdots \varepsilon_n)=(\eta_1 \eta_2 \cdots \eta_n)$

Hence
$$A=(\eta_1 \eta_2 \cdots \eta_n)^{-1} (\mathscr{A}\varepsilon_1 \mathscr{A}\varepsilon_2 \cdots \mathscr{A}\varepsilon_n)$$
Therefore, we got $A$.

If $A$ is an $m$ by $n$ matrix and $rank(A)=n$, show that $A^{T}A$ is invertible. Is $P=A(A^{T}A)^{-1}A^T$ invertible? Explain why.

Since $N(A^T A)=N(A), dimC(A^T)+dimN(A)=n$, also we have $rankA=dimC(A^T)$,

Since $rankA=0,\Rightarrow dimN(A)=0, \Rightarrow dimN(A^T A)=0$,

Therefore, $A^T A$ is invertible.

Suppose $A$ is $m$ by $n$, $B$ is $n$ by $p$, and $AB = 0$. Prove
$rankA+rankB\leq n$

We have $dimA=n$, and also $dim(C(A^T))+dim(N(A))=n, rankA=dimC(A^T)$
And 

$$
AB=0, C(B)\subset N(A), \Rightarrow dimC(B)\leq dimN(A)
$$

Therefore, we have $rankA+rankB\leq n$.

Show that an upper triangular matrix multipling another gives an upper
triangular matrix.

$$\begin{aligned}
\mathscr{A}(\varepsilon_1 \varepsilon_2 \cdots \varepsilon_n)&=(\varepsilon_1 \varepsilon_2 \cdots \varepsilon_n)A\\
\mathscr{A}(\eta_1 \eta_2 \cdots \eta_n)&=(\eta_1 \eta_2 \cdots \eta_n)B\\
(\eta_1 \eta_2 \cdots \eta_n)&=(\varepsilon_1 \varepsilon_2 \cdots \varepsilon_n)X\end{aligned}$$

It can be proved that: 
$$\begin{aligned}
\mathscr{A}(\eta_1 \eta_2 \cdots \eta_n)
&=[\mathscr{A}(\varepsilon_1 \varepsilon_2 \cdots \varepsilon_n)]X\\&=(\varepsilon_1 \varepsilon_2 \cdots \varepsilon_n)AX \\&=(\eta_1 \eta_2 \cdots \eta_n)X^{-1}AX\end{aligned}$$

We get $B=X^{-1}AX$

Additionally, we add
$$\mathscr{A}([\varepsilon_1 \varepsilon_2 \cdots \varepsilon_n]x)=\mathscr{A}(\alpha)=[\varepsilon_1 \varepsilon_2 \cdots \varepsilon_n]Ax$$
$$\mathscr{A}(\alpha)=Ax$$ 
If we let $[\varepsilon_1 \varepsilon_2 \cdots \varepsilon_n]=I$, $A$ is transforming effect. $x$ is the cofficient corrospond to the basis. $[\varepsilon_1 \varepsilon_2 \cdots \varepsilon_n]$ is the basis before transformation.

When we do some proves, it is easy to use the basis reprensenting all the matrices or vectors in space, which means we have to introduce the normal expression of them. Basis elements
$$A_{m\times n}=\sum_{i=1}^{m}\limits\sum_{j=1}^{n}\limits a_{ij}\alpha_i\beta_j  \Rightarrow A_{m\times n}=\sum_{i=1}^{m}\limits\sum_{j=1}^{n}\limits a_{ij} e_i e_j^T$$
After we choose the basis as identity basis. If $A=\pm A^T$, we have

$$A_{m\times n}=\sum_{i=1}^{m}\limits\sum_{j>i}^{n}\limits a_{ij}( e_i e_j^T \pm e_j e_i^T)$$

The four possibilities for linear equations depend on the rank.

  ------- ----- ------- ----------------------- -------- ---------------------------
   $r=m$   and   $r=n$   Square and invertible   $Ax=b$         $1$ solution
   $r=m$   and   $r<n$      Short and wide       $Ax=b$      $\infty$ solutions
   $r<m$   and   $r=n$       Tall and thin       $Ax=b$      $0$ or $1$ solution
   $r<m$   and   $r<n$       Not full rank       $Ax=b$   $0$ or $\infty$ solutions
  ------- ----- ------- ----------------------- -------- ---------------------------

$ Ax=b $ is solvable if and only if $ y^T b=0 $ whenever $y^T A=0  $

$Ax=b$ is solvable if and only if $b\in C(A)$. Also $C(A)\perp N(A^T)$, and $b\in N(A^T)$ if and only if $ y^T b=0 $ whenever $y^T A=0  $

$$P_Q(b)=Q(Q^TQ)^{-1}Q^T=(\sum\limits_{i=1}^{n} \frac{q_iq_i^T}{q_i^Tq_i})b$$

If eigenvectors $x_1, x_2, \cdots x_k$ correspond to different eigenvalues $\lambda_1, \lambda_2 \cdots \lambda_k$ , then
$x_1, x_2, \cdots x_k$ is linearly independent.

Suppose $x_1, x_2, \cdots x_k$ is linearly dependent. Let $n$ be the smallest positive integer such that $x_1, x_2, \cdots x_n$ is independent.

$\exists a_1,a_2 \cdots a_n$ not all $0$, such that 
$$\begin{aligned}
 a_1x_1+a_2x_2+\cdots a_nx_n=0\end{aligned}$$ 
 
Apply both sides
,$a_1\lambda_1 x_1+a_2 \lambda_2 x_2+\cdots +a_n\lambda_nx_n=0$, which
minus $\lambda_n \cdot (1)$

$$\Rightarrow a_1(\lambda_1-\lambda_n) x_1+a_2 (\lambda_2-\lambda_n) x_2+\cdots +a_n(\lambda_{n-1}-\lambda_n)x_n=0$$

$x_1 , x_2, \cdots x_n$ is independent
$\Rightarrow a_1=a_2=\cdots=a_{n-1}=0$.

Back to the (1), $a_nx_n=0\Rightarrow a_n=0$
$$\Rightarrow a_1=a_2=\cdots=a_{n-1}=a_n=0 \Rightarrow$$ A Contradiction$$

Different Expressions:
$$|A|=\sum\limits_{j=1}^{n}(-1)^{i+1}a_{ij}|M_{ij}|
=\sum_{j} (-1)^{\tau (j_1j_2\cdots j_n)} a_{1 j_1} a_{2 j_2} \cdots  a_{n j_n}$$
There is a big fomula:
$$|A|=\sum_{j} det(P)  a_{1 j_1} a_{2 j_2} \cdots  a_{n j_n}$$ Also we
have a relation:$\displaystyle A^{-1}=\frac{ C^T}{|A|}$$

For a difference equation, connected to eigenvalues:
$$A=Q\Lambda Q^T \Rightarrow A^k = Q\Lambda ^k Q^T$$

$p(x)=\frac{1}{2} x^T Ax-b^Tx$, so we
have$\nabla p_1(x)=Ax, \nabla p_2(x)=b.$ Therefore,
$$\nabla p(x)=Ax-b=0 \Rightarrow Ax=b$$

When $Ax=b$, for any $y\in {\mathbb{R}}$, we have
$$p(y)-p(x)=\frac{1}{2} y^T Ay-b^Ty-(\frac{1}{2} x^T Ax-b^Tx)=
 \frac{1}{2} (y-x)^T A(y-x)\geqslant 0 $$ 
 
 if and only if $A$ is positive
definite.

$$L(x,y)=p(x)+y^T(Cx-d)=\frac{1}{2} x^T Ax-b^Tx+x^T C^Ty-y^T d,$$ 
and $y=(y_1, y_2, \cdots y_n) \in {\mathbb{R}}$ is given vector(*Lagrange multipliers*). So, it get the minimum value if and only if :

$$\begin{aligned}
\frac{\partial L}{\partial x}=0 : Ax+C^T y=b \qquad
\frac{\partial L}{\partial y}=0 : Cx=d\end{aligned}$$

Consider $\displaystyle R(x)=\frac{x^TAx}{x^Tx}$, and we will solve
$\min R(x)$. So we have :
$$\lambda_{\min}(A)\leqslant R(x)=\frac{x^TAx}{x^Tx}=\frac{(Qy)^TA(Qy)}{(Qy)^T(Qy)}=
    \frac{y^T \Lambda y}{y^Ty}\leqslant \lambda_{\max}(A)$$ Therefore,
we have
$$\lambda_{\min}(A)\leqslant R(x)=\{ x^TAx|  \|x\|=1 \} \leqslant \lambda_{\max}(A)$$

$A_{m\times n}=U_{m\times m}\Sigma_{m\times n} V_{n\times n}^T$, and
$AV=U\Sigma$, is called SVD. We also have: 
$$\begin{aligned}
A^TA=(V\Sigma^T U^T)U\Sigma V^T=V\Sigma^T \Sigma U &\qquad
AA^T=(U\Sigma V^T)V\Sigma^T U^T=U\Sigma\Sigma^T U^T\\
A[V_r|V_{n-r}]=[U_r|U_{n-r}]\Sigma&= [\sigma_1u_1, \sigma_2u_2 \cdots \sigma_ru_r , 0 \cdots 0]\end{aligned}$$
and from this, we also have: 
$$\begin{aligned}
V_{n-r} \rightarrow N(A) &\qquad U_{m-r}\rightarrow N(A^T) \qquad
A^+ = U\Sigma^+ V^T\\
V_r \rightarrow C(A^T)&\qquad U_r \rightarrow C(A) \qquad x^+=A^+ b\end{aligned}$$

If $A_{s\times n}, B_{n\times m}$, show that
$rank(AB)\geqslant rank(A)+rank(B)-n$.

Since 
$rank(A)+rank(B)=rank\begin{bmatrix}
    A & O \\
    O & B
    \end{bmatrix}\geqslant rank\begin{bmatrix}
    A & I \\
    O & B
    \end{bmatrix}
    $.

    Also we have elementary transformations:

$$\begin{bmatrix}
        A & I \\
        O & B
    \end{bmatrix}\longrightarrow\begin{bmatrix}
    A & I \\
    -AB & O
    \end{bmatrix}\longrightarrow\begin{bmatrix}
    O& I \\
    -AB & O
    \end{bmatrix}$$ Therefore, $rank\begin{bmatrix}
    A & I \\
    O & B
    \end{bmatrix}=rank\begin{bmatrix}
    O& I \\
    -AB & O
    \end{bmatrix}=rank(AB)+rank(I)=rank(AB)+n$$

Let $R(A)=r_1, R(B)=r_2, R(AB)=r,$ We assume that
$b_1, b_2 \cdots b_{r_2}$ is the basic solutions of the column vectors
of $B$, so there must exists the largest number which satisfies
$Ab_j=0, j\in \{1,2\cdots r_2\}$ where $b_1, b_2 \cdots b_{r_2}$ is
$r_2-r$. Otherwise, it is contradictary to $R(AB)=r$.

It also means the $b_j$ of $Ab_j=0$ is in the $N(A)$, which means
$dim(N(A))=n-r_1$. Therefore, 
$r_2-r\leqslant n-r_1 \Rightarrow rank(AB)\geqslant rank(A)+rank(B)-n$.

Linear Calculation
==================

A $n$ by $n$ matrix multiplies an $n$ -dimensional vector and produces
an $m$ -dimensional vector.

$( E A$ times $x )$ equals $( E \operatorname { times } A x ) .$ We just
write $E A x$
$$A B = A \left[ \begin{array} { l } { b _ { 1 } } \\ { b _ { 2 } } \\ { b _ { 3 } } \end{array} \right] = \left[ \begin{array} { c } { A b _ { 1 } } \\ { A b _ { 2 } } \\ { A b _ { 3 } } \end{array} \right]$$
the number of columns in A has to equal the number of rows in $B .$ Then
$A$ can be multiplied into each column of $B .$

Each column of $A B$ is the product of a matrix and a column: column $j$
of $A B = A$ times (column $j$ of $B )$

Each row of $A B$ is the product of a row and a matrix: row $i$ of
$A B = ($ row $i$ of $A )$ times $B$

Matrix multiplication is associative: $( A B ) C = A ( B C ) .$ Just
write $A B C .$

Triangular factorization $A = L U$ with no exchanges of rows. $L$ is
lower triangular, with 1’s on the diagonal. The multipliers
$\ell _ { i j } ($ taken from elimination $)$ are below the diagonal.
$U$ is the upper triangular matrix which appeats after forward
elimination, The diagonal entries of $U$ are the pivots.

$$\left[ \begin{array} { c c c } { 1 } & { 0 } & { 0 } \\ { \ell _ { 21 } } & { 1 } & { 0 } \\ { \ell _ { 31 } } & { \ell _ { 32 } } & { 1 } \end{array} \right] \left[ \begin{array} { l l } { \text { row } 1 \text { of } U } \\ { \text { row } 2 \text { of } U } \\ { \text { row } 3 \text { of } U } \end{array} \right] =\mathrm{ original }A$$

$P A = L U$ $P ^ { - 1 }$ is always the same as
$P ^ { \mathrm { T } }$. With the rows reordered in advance, $P A$ can
be factored into $L U$

The inverse exists if and only if elimination produces n pivots (row
exchanges allowed). Elimination solves $A x = b$ without explicitly
finding $A ^ { - 1 } .$

Suppose there is a nonzero vector $x$ such that $A x = 0 .$ Then $A$
cannot have an inverse. To repeat: No matrix can bring 0 back to $x$ .
If $A$ is invertible, then $A x = 0$ can only have the zero solution
$x = 0$

$$\left[ \begin{array} { l l } { a } & { b } \\ { c } & { d } \end{array} \right] ^ { - 1 } = \frac { 1 } { a d - b c } \left[ \begin{array} { c c } { d } & { - b } \\ { - c } & { a } \end{array} \right]$$

$x = A ^ { - 1 } b$ separates into $L c = b $ and $ U x = c$ Invertible
$=$ Nonsingular ($n$ pivots)

The transpose of $A ^ { - 1 }$ is
$\left( A ^ { - 1 } \right) ^ { \mathrm { T } } = \left( A ^ { \mathrm { T } } \right) ^ { - 1 }$

Suppose $A = A ^ {T }$ can be factored into $A = L D U$ without row
exchanges. Then $U$ is the transpose of $L$ . The symmetric
factorization becomes $A = L D L ^ { T }$

The number of free variables consist of the basic solutions of $N(A)$.
The expression is normally:
$$N(A)= \left\lbrace x|x=k_1x_1+k_2x_2+k_3x_3 \right\rbrace$$

For a rectangular matrix, there dosen’t exist full inverse matrix.
However, there exist one-side matrix.

1.  Full row rank. $r=m\leqslant n$. There exists a right-side inverse
    matrix.

2.  Full column rank. $r=n\leqslant m$. There exists a left-side inverse
    matrix.

Linear Space
============

A *Vector space* is a set $V$ along with an additiont on $V$ and a
scalar multiplication on $V$ such that the following properties hold:

1.  **commutativity**\
    $u+v=v+u$ for all $u,v \in V$ ;

2.  **associativity**\
    $(u+v)+w=u+(v+w) $ and $(ab)v=a(bv)$ for all $u,v,w  \in V $ and all
    $a,b \in \textbf{F}$;

3.  **addictive identity**\
    there exists an element $0\in V$ such that $v+0=v$ for all $v\in V$;

4.  **addicyive inverse**\
    for every $v\in V$ ,there exists $w \in V$ such that $v+w=0$;

5.  **multiplicative identity** $1v=v$ for all $v \in V$

6.  **distributive properties** $a(u+v)=au+av$ and $(a+b)v=av+bv$ for
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

$A x _ { p } = b$ and $A x _ { n } = 0 \quad$ produce
$\quad A \left( x _ { p } + x _ { n } \right) = b$

$$R x = \left[ \begin{array} { l l l l } { 1 } & { 3 } & { 0 } & { - 1 } \\ { 0 } & { 0 } & { 1 } & { 1 } \\ { 0 } & { 0 } & { 0 } & { 0 } \end{array} \right] \left[ \begin{array} { l } { u } \\ { v } \\ { w } \\ { y } \end{array} \right] = \left[ \begin{array} { l } { 0 } \\ { 0 } \\ { 0 } \end{array} \right]$$
The unknowns $u , v , w , y$ go into two groups. One group contains the
pivot variables, those that correspond to columns with pivots.

If $A x = 0$ has more unknowns than equations $( n > m ) ,$ it has at
least one special solution: There are more solutions than the trivial
$x = 0$

$x _ { \mathrm{complete} } = x _ { \mathrm{particular} } + x _ {\mathrm{  nullspace }}$

The columns of A are independent exactly when $N ( A ) = \{$ zero vector
$\}$

Basis
-----

Suppose $c _ { 1 } v _ { 1 } + \cdots + c _ { k } v _ { k } = 0$ only
happens when $c _ { 1 } = \cdots = c _ { k } = 0 .$ Then the vectors
$v _ { 1 } , \ldots , v _ { k }$ are linearly independent. If any
$c ^ { \prime }$ are nonzero, the $v ^ { \prime } \mathrm { s }$ are
linearly dependent. One vector is a combination of the others.

To check any set of vectors $v _ { 1 } , \ldots , v _ { n }$ for
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

1.  The vectors are linearly independent (not too many vectors).

2.  They span the space V (not too few vectors).

Any two bases for a vector space $\mathbf { V }$ contain the same number
of vec- tors. This number, which is shared by all bases and expresses
the number of $\cdot$ degrees of freedom" of the space, is the dimension
of $\mathbf { V } .$

If $v _ { 1 } , \ldots , v _ { m }$ and $w _ { 1 } , \ldots , w _ { n }$
are both bases for the same vector space, then $m = n .$ The number of
vectors is the same.

Suppose there are more $w ^ { \prime }$ s than
$v ^ { \prime } \mathrm { s } ( n > m ) .$ We will arrive at a
contradiction. Since the $v ^ { \prime }$ s form a basis, they must span
the space. Every $w _ { j }$ can be written as a combination of the v’s:
If $w _ { 1 } = a _ { 11 } v _ { 1 } + \cdots + a _ { m 1 } v _ { m } ,$
this is the first column of a matrix multiplication $V A :$
$$W = \left[ \begin{array} { l l l l } { w _ { 1 } } & { w _ { 2 } } & { \cdots } & { w _ { n } } \end{array} \right] = \left[ \begin{array} { c c c } { v _ { 1 } } & { \cdots } & { v _ { m } } \end{array} \right] \left[ \begin{array} { c } { a _ { 11 } } \\ { \vdots } \\ { a _ { m 1 } } \end{array} \right] = V A$$
We don’t know each $a _ { i j } ,$ but we know the shape of $A$ (it is
$m$ by $n ) .$ The second vector $w _ { 2 }$ is also a combination of
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

Important
=========

Eigenvalues
-----------

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

1.  Every symmetric matrix (and Hermitian matrix) has real eigenvalues.

2.  Its eigenvectors can be chosen to be orthonormal.

complex
-------

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

Normal
------

The matrix $N$ is normal if it commutes with
$$N N ^ { \mathrm { H } } = N ^ { \mathrm { H } } N .$$
 For such matrices, and no others, the triangular $T = U ^ { - 1 } N U$ is the
diagonal $\Lambda$ Normal matrices are exactly those that have a
complete set of orthonormal eigenvectors.

1.  $A$ is diagonalizable: The columns of $S$ are eigenvectors and
    $S ^ { - 1 } A S = \Lambda$

2.  $A$ is arbitrary: The columns of M include “generalized
    eigenvectors” of $A ,$ and the Jordan form $M ^ { - 1 } A M = J$ is
    block diagonal.

3.  $A$ is arbitrary: The unitary $U$ can be chosen so that
    $U ^ { - 1 } A U = T$ is triangular.

4.  $A$ is normal, $A A ^ { \mathrm { H } } = A ^ { \mathrm { H } } A :$
    then $U$ can be chosen so that $U ^ { - 1 } A U = \Lambda$ *Special
    cases of normal matrices, all with orthonormal eigenvectors:*

    1.  If $A = A ^ { H }$ is Hermitian, then all $\lambda _ { i }$ are
        real.

    2.  If $A = A ^ { T }$ is real symmetric, then $\Lambda$ is real and
        $U = Q$ is orthogonal.

    3.  If $A = - A ^ { H }$ is skew-Hermitian, then all
        $\lambda _ { i }$ are purely imaginary.

    4.  If $A$ is orthogonal or unitary, then all
        $\left| \lambda _ { i } \right| = 1$ are on the unit circle.

Positive definite
=================

$ a x ^ { 2 } + 2 b x y + c y ^ { 2 }$ is positive definite if and only
if $a > 0$ and $a c > b ^ { 2 } .$ Any $f ( x , y )$ has a minimum at a
point where $\partial F / \partial x = \partial F / \partial y = 0$ with

$$\frac { \partial ^ { 2 } F } { \partial x ^ { 2 } } > 0 \quad \qquad \left[ \frac { \partial ^ { 2 }F  } { \partial x ^ { 2 } } \right] \left[ \frac { \partial  ^ { 2 }F } { \partial y ^ { 2 } } \right] > \left[ \frac { \partial ^ { 2 } F } { \partial x \partial y } \right] ^ { 2 }$$

$$F ( x ) = F ( 0 ) + x ^ { \mathrm { T } } ( \text{ grad } F ) + \frac { 1 } { 2 } x ^ { \mathrm { T } } A x +\text{higher order terms}$$

At a stationary point,
$\nabla F = \left( \partial F / \partial x _ { 1 } , \ldots , \partial F / \partial x _ { n } \right)$
is a vector of zeros.

$$a x ^ { 2 } + 2 b x y + c y ^ { 2 } = a \left( x + \frac { b } { a } y \right) ^ { 2 } + \frac { a c - b ^ { 2 } } { a } y ^ { 2 }$$

Each of the following tests is a necessary and sufficient condition for
the real symmetric matrix $A$ to be positive definite:

1.  $x ^ { \mathrm { T } } k x > 0$ for all nonzero real vectors $x$ .

2.  All the eigenvalues of $A$ satisfy $\lambda _ { i } > 0$

3.  All the upper left submatrices $A _ { k }$ have positive
    determinants.

4.  All the pivots (without row exchanges) satisfy $d _ { k } > 0 .$

5.  There is a matrix $R$ with independent columns such that
    $A = R ^ { \mathrm { T } } R .$

The key is to recognize $x ^ { \mathrm { T } } A x$ as
$x ^ { \mathrm { T } } R ^ { \mathrm { T } } R x = ( R x ) ^ { \mathrm { T } } ( R x )$

symmetric matrix $A$ to be positive semidefinite:

1.  $x ^ { \mathrm { T } } A x \geq 0$ for all vectors $x$ (this defines
    positive semidefinite)

2.  All the eigenvalues of $A$ satisfy $\lambda _ { i } \geq 0$

3.  No principal submatrices have negative determinants.

4.  No pivots are negative.

5.  There is a matrix $R ,$ possibly with dependent columns, such that
    $A = R ^ { \mathrm { T } } R$

$$5 u ^ { 2 } + 8 u v + v ^ { 2 } = \left( \frac { u } { \sqrt { 2 } } - \frac { v } { \sqrt { 2 } } \right) ^ { 2 } + 9 \left( \frac { u } { \sqrt { 2 } } + \frac { v } { \sqrt { 2 } } \right) ^ { 2 } = 1$$

Any ellipsoid $x ^ { \mathrm { T } } A x = 1$ can be simplified in the
same way. The key step is to diago- nalize
$A = Q \Lambda Q ^ { \mathrm { T } } .$ We straightened the picture by
rotating the axes. Algebraically, the change to $y = Q ^ {T} x$ produces
a sum of squares:
$$x ^ { \mathrm { T } } A x = \left( x ^ { \mathrm { T } } Q \right) \Lambda \left( Q ^ { \mathrm { T } } x \right) = y ^ { \mathrm { T } } \Lambda y = \lambda _ { 1 } y _ { 1 } ^ { 2 } + \cdots + \lambda _ { n } y _ { n } ^ { 2 } = 1$$

Suppose $A = Q \Lambda Q ^ { \mathrm { T } }$ with
$\lambda _ { i } > 0 .$ Rotating $y = Q ^ { \mathrm { T } } x$
simplifies $x ^ { \mathrm { T } } A x = 1 :$
$$x ^ { \mathrm { T } } Q \Lambda Q ^ { \mathrm { T } } x = 1  \qquad y ^ { \mathrm { T } } \Lambda y = 1 ,\qquad \lambda _ { 1 } y _ { 1 } ^ { 2 } + \cdots + \lambda _ { n } y _ { n } ^ { 2 } = 1$$

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

$$\quad P _ { C / \min } = P _ { \min } + \frac { 1 } { 2 } y ^ { \mathrm { T } } \left( C A ^ { - 1 } b - d \right) \geq P _ { \min }$$
