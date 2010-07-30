Functional Analysis
===================

Linear space
------------

A simple way to test if a space $V$ is a **linear space** is to see if

#. the space is equipped with two operations

#. "+" called addition,

#. "$\cdot$" called scalar multiplication,

and satisfies the following two properties:

* $V$ contains a zero element $\left( 0+a=a\right)\,\forall a \in V$

* $V$ is closed under linear combination: $u,v\in V \Rightarrow au+bu\in V\quad \forall a,b\in \mathbb{R}$

Examples:

* $V=\left\{0\right\}$ is a linear space

* $V=\left\{ v\in \mathbb{R}^5;\quad v_1+v_3+v_4=0\right\}$ is a linear space

* $V=\left\{ v\in \mathbb{R}^5;\quad v_1+v_3+v_4=10\right\}$ is not a linear space

* $V=\left\{ M\in \mathbb{R}^{3\times 3};\quad \sum_{m=1}^n m_{ii}=0 \right\}$ is a linear space


If $V$ is a linear space, and $W\in V$, $W$ is a **subspace** of $V$ if $W \in W$ and it is a
linear space itself.
For instance, when $V=\mathbb{R}^3$ then  $W=\left\{w\in V;\quad w_3=0\right\}$ are all 3D vectors
that lay on x-y plane and $W$ is a subspace of $V$.

Union and intersection of subspaces
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Let $V$ be a linear space and $W_1$ and $W_2$ subspaces of $V$. 

**Intersection** 
 is $W_1\cap W_2$
 and it is never an empty set - contains at least the zero element. 
 Furthermore, intersection of two subspaces is always a linear space. 
| It is sufficient to show that $z_1,\: z_2\in W_1 \cap W_2 \Rightarrow az_1 + bz_2 \in W_1 \cap W_2$.  
| This is due to the linearity as $w_1$ and $w_2$ both belong to $W_1$ and $W_2$. 
| Therefore $az_1 + bz_2$ belong to the both of the subspaces as well and this results that $az_1 + bz_2 \in W_1 \cap W_2$.

At the same time, **union** of two subspaces $W_1 \cup W_2$ is not necessarily a subspace.

Linear combination
^^^^^^^^^^^^^^^^^^

Let $V$ be a linear space and $v_1,\, v_2\in V$ and $c_1,\, c_2\in \mathbb{R}$  then the element $v$

.. math::
	:label: linear combination

		v=\sum_{i=1}^n c_i v_i

of $V$ is a linear combination of the elements $v_1,\, v_2,\, \dots, \, v_n$ with the
coefficients $c_1,\, c_2,\, \dots, \, c_n$

Linear span, sum and direct sum of subspaces
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Let $V$ be a linear space and $v_1,\, v_2,\, \dots, \, v_n \in V$ then linear span
$\left[ v_1,\, v_2, \, \dots ,\, v_n\right]$ or $span\left\{ v_1,\, v_2, \, \dots ,\, v_n\right\}$
is the smallest subspace of $V$ containing $v_1,\, v_2,\, \dots \, v_n$.
In the other words, $v_1,\, v_2,\, \dots, \, v_n$ are said to span $V$ if every element $v \in V$
can be expressed as a linear combination of $v_1,\, v_2,\, \dots, \, v_n$

Let $S=\left\{ v_1,\, v_2,\, \dots , \, v_n\right\}\subset V$ then $\left[ S \right]$ is equal
to the set of all linear cobinations of elements of $S$.

Basic properites of linear span:
Let $V$ be a linear space and $S_1, \, S_2$ subsets uf $V$ then

#. $S_1 \subset \left[ S_1 \right]$,

#. $S_1 \subset S_2 \Rightarrow \left[ S_1 \right] \subset \left[ S_2 \right]$,

#. $\left[ \left[ S_1 \right] \right] = \left[ S_1 \right]$,

#. if $S_1 = 0$ then $\left[ S_1 \right] = \left\{ 0 \right\}$

#. if $S_1 \subset S_2 \subset \left[ S_1 \right] \Rightarrow \left[ S_1 \right] = \left[ S_2 \right]$.

Let $W_1$ and $W_2$ be subspaces  of a linear space $V$.
Then we define

.. math::
	:label: sum 

	        W_1+W_2=\left[W_1\cup W_2\right]

which is the linear span of the union of $W_1$ and $W_2$.
For instance, let $V=P^3$, and 
$W_1=\left\{v\in V;\quad v=a+bx;\quad a,b\in \mathbb{R}\right\}$
and $W_2=\left\{v\in V;\quad v=cx^2;\quad c\in\mathbb{R}\right\}$
then $W_1+W_2=\left\{v\in V;\quad v=a+bx+cx^2;\quad a,b,c\in \mathbb{R}\right\}$.
$V$ is a direct sum of $W_1+W_2$ ($V=W_1\oplus W_2$) if

#. $V=W_1+W_2$,

#. $W_1 \cap W_2 = \left\{0\right\}$.

Also, $V=W_1+W_2\iff$ every element of $v\in V$ can be **uniquely**
expressed as $v=w_1+w_2$ where $w_1\in W_1$ and $w_2\in W_2$.

For instance, consider $V=\mathbb{R}^{3\times 3}$ with the following
subspaces:
$W_1=\left\{M\in V;\quad m_{ij}=0,\quad i\neq j\right\}$,
$W_2=\left\{M\in V;\quad m_{ij}=0,\quad j \geq i\right\}$,
$W_3=\left\{M\in V;\quad m_{ij}=0,\quad j\leq i\right\}$.

Then clearly $W_1\cap W_2=\left\{0\right\}$, $W_2 \cap W_3=\left\{0\right\}$,
and $W_3 \cap W_1 = \left\{0\right\}$.
Therefore $V=W_1\oplus W_2 \oplus W_3$.

Linear independence, basis, dimension
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Let $V$ to be a linear space and $v_1,v_2,v_3,\dotsc ,v_n\in V$, 
then these elements are linearly independent 
if $\alpha_1v_1+\alpha_2v_2+\dotsb +\alpha_nv_n=0\implies \alpha_1=\alpha_2=\dotsb =\alpha_n=0$.
Whenever we can find a linear combination  such that at least
one $\alpha_i\neq 0$ then these elements are linearly dependent.

| For instance, let $V=\mathbb{R}^2$ and $v_1=\begin{pmatrix}1\\0\end{pmatrix}$, and $v_2=\begin{pmatrix}1\\1\end{pmatrix}$. 
| To find if $v_1$ and $v_2$ are linearly independent, let's check 
| $\alpha_1v_1+\alpha_2v_2=\begin{pmatrix}0\\0\end{pmatrix}$
| $\alpha_1\begin{pmatrix}1\\0\end{pmatrix}+\alpha_2\begin{pmatrix}1\\1\end{pmatrix}=\begin{pmatrix}0\\0\end{pmatrix}$
| This results in
| $\left\{\begin{array}{l}\alpha_1 + \alpha_2 = 0\\ \alpha_2=0\end{array}\right.$,
| so necessarily $\alpha_1=\alpha_2=0$ and $v_1$ and $v_2$ are linearly independent.

**Basis**
 Let $V$ be a linear space. Then any set $S\subset V$ that is
 linearly independent and $\left[S\right]=V$ is a basis of $V$.

A linear space $V$ is separable if it has a finite basis, or a
countable infinite one.

All bases in a linear space have the same cardinality - number of elements
in set. Furthermore, cardinality of any basis of a linear space
$V$ is said to be the **dimension** of $V$, denoted $dim\left( V \right)$.

**Expansion coefficients**
 Let $V$ be a linear space and $B$ any basis of $V$ with $dim\left( V \right) = n < \infty$
 Any element $v\in V$ can be uniquely expressed in the form

.. math::
        :label: expansion coefficients 

                v=\sum_{i=1}^n \alpha_iv_i,

where $B=\left\{v_1,\ v_2,\dotsc,v_n\right\}$ and $\alpha_i$ are expansion coefficients.

Determinants, eigenvalues, and eigenvectors
-------------------------------------------

First, a permutation of a finite set ${1,2,...,n}$ is an arrangement of its 
elements. For instance, if $S={1,2,3}$, then 123 312, 321 are three different
permutations of $S$. The number of permutations of a set with n elements is $n!$.
Permutations can be defined also as $P\in S_{n}$ where $S_{n}$ is a set of 
all bijections of the set ${1,2,...n}$ into itself, e.g. a permutation $123\rightarrow 312$
is a function $f:{1,2,3}\rightarrow {1,2,3}$ that assigns:

.. math::
	:label: bijection

		f\left( 1 \right) = 3,\ \ \ f\left( 2 \right) = 1,\ \ \ f\left(3 \right) = 2.

For a permutation $P \in S_{n}$ let $m$ be a number of pairs $(i,j)\ \set {1,2,...,n},\ i<j$
such that $P(i)>P(j)$.

Normed spaces
-------------

Definition of norm
^^^^^^^^^^^^^^^^^^


