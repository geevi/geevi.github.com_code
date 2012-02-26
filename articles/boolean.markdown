---
layout: page
title: "Generalized Harmonic Analysis over Abelian Group"
mqathjax: enable
---

\newcommand{\Int}{\mathbb{Z}}
\newcommand{\Real}{\mathbb{R}}
\newcommand{\Cmplx}{\mathbb{C}}
\newcommand{\pmone}{\{\pm 1\}}
\newcommand{\Exp}{\mathbb{E}}

Consider $\Int_2 = \{0,1\}$, an abelian group under $mod~2$ addition.
We will be viewing this group as $\pmone$ under the operation of 
multiplication. These two are isomorphic by the following mapping 
$0 \mapsto +1, 1 \mapsto -1$. The following is a well known theorem:

> **Theorem** Any function of the form $f:\pmone^n \rightarrow\Real$ 
> can be written as a multilinear polynomial:
> $$ f(x) = \sum_{S \subseteq [n]} \hat{f}_S \prod_{i\in S}x_i $$
> This representation is unique. 

Another way of saying this is that the functions
$\{\prod_{i\in S}x_i \}_{S\subseteq [n]}$ form an orthogonal basis for the 
$2^n$ dimensional real vector space of functions from $\pmone^n$ to 
$\Real$. In this article we will be exploring the generalizations of 
this theorem to arbitrary finite (and some infinite) abelian groups.

It is well known by the [structure theorem for finitely generated modules](http://en.wikipedia.org/wiki/Fundamental_theorem_of_finitely_generated_abelian_groups#Classification), 
that any finite abelian group is isomorphic to a direct sum of cyclic groups with 
prime order. Hence we will first analyze cyclic groups of prime order $\Int_p$.

Harmonic analysis of $\Int_p$
------------------------------------

Let 

--------------- -----------------------------------------------------
            $p$ be a prime
       $\Int_p$ be the cyclic group of order $p$
         $\Phi$ be the set of homomorphisms from $\Int_p$ to $\Cmplx$
--------------- -----------------------------------------------------

> **Claim :** 
> 1. $\forall \chi \in \Phi, \chi(0)=1$
>
> 2. $|\Phi| = p$
>
> 3. $\Phi = \{ \chi_k(x) = \omega^{kx \mod p} \}$, where $\omega$ is the $p$th
> root of unity.


*Proof :* 
Since $\forall a \in \Int_p, a+0=a \Rightarrow \chi(a)\chi(0) = \chi(a)$
, then $\chi(0)$ should be $1$. Let $1$ be a generator then 
$b=k\times1 \Rightarrow \chi(b)=\chi(a)^k$^[$k\times1$ refers to repeated 
addition of $1$, $k$ times]. Hence $\chi$ is completely determined by its 
value on the generator $1\in \Int_p$. Since $\chi(0)=\chi(p\times 1)=\chi(1)^p$,
we have that $\chi(1)$ must be one of the $p$ roots of unity. Hence the last
statement follows. **QED**


> **Claim :**
> $\Phi$ forms an orthonormal basis for the complex vector space of functions 
> from $\Int_p$ to $\Cmplx$ under the inner product 
> $$\langle f, g \rangle = \Exp_{x\leftarrow \mu}f(x)\overline{g(x)} .$$

*Proof :* 

**QED**

Handling Product Groups $\Int_p\times \Int_q$
---------------------------------------------------------



Consider the functions 
$$\{ \chi_{j,k}(x,y) = \omega^{jx+ky}  \}_{j\in \Int_p, k\in \Int_q}$$
These again form an orthonormal basis.

Term 1
:   Definition 1

Term 2 with *inline markup*
:   Definition 2

  Right     Left     Center     Default
-------     ------ ----------   -------
     12     12        12            12
    123     123       123          123
      1     1          1             1

Table:  Demonstration of simple table syntax.

: Sample grid table.

+---------------+---------------+--------------------+
| Fruit         | Price         | Advantages         |
+===============+===============+====================+
| Bananas       | $1.34         | - built-in wrapper |
|               |               | - bright color     |
+---------------+---------------+--------------------+
| Oranges       | $2.10         | - cures scurvy     |
|               |               | - tasty            |
+---------------+---------------+--------------------+

What is the difference between `>>=` and `>>`?

Here is a footnote reference,[^1] and another.[^longnote]

[^1]: Here is the footnote.

[^longnote]: Here's one with multiple blocks.

