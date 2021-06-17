---
layout: post
title: linear algebra notes 1
data: 2020-11-04
description: Linear calculations
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
