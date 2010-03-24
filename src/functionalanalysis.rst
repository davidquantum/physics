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
-----------------------------------

Let $V$ be a linear space and $W_1$ and $W_2$ subspaces of $V$. Then the **intersection** is $W_1\cap W_2$
and it is never an empty set - contains at least the zero element. Furthermore, intersection
of two subspaces is always a linear space. It is sufficient to show that
$z_1,\: z_2\in W_1 \cap W_2 \Rightarrow az_1 + bz_2 \in W_1 \cap W_2$.  This is due to 
the linearity as $w_1$ and $w_2$ both belong to $W_1$ and $W_2$. Therefore $az_1 + bz_2$ belong to the
both of the subspaces as well and this results that $az_1 + bz_2 \in W_1 \cap W_2$.

At the same time, **union** of two subspaces $W_1 \cup W_2$ is not necessarily a subspace.


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
