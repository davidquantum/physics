Functional Analysis
===================

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
