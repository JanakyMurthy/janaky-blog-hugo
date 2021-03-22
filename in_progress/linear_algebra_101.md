---
title: Linear Algebra 101
date: 2020-12-12
lastmode: 2020-12-12
author: Janaky Murthy

description: Linear Algebra 101
categories: [Linear Algebra, Basic Math]
tags: [Math,la]

draft: false
enableDisqus : true
enableMathJax: true
disableToC: false
disableAutoCollapse: true
---

This post will have some preliminaries for the sake of completeness. Let us start at the beginning. 

## Vector Spaces
The story begins with **vector spaces**. Rather than defining them straight away, let me start with my favourite example. Consider the set of all polynomials of degree at most $2$ with real coefficients.
$$
\mathcal{P} = \lbrace a_0 + a_1x + a_2x^2 : a_0,a_1,a_2 \in \mathbb{R} \rbrace\ .
$$

Let us call the polynomials in $\mathcal{P}$ as ***vectors*** and the numbers in $\mathbb{R}$ as ***scalars***. Consider the following **operations**:

1. **(Vector addition)** For any two vectors $p = a_0 + a_1x + a_2x^2$ and $q = b_0 + b_1x + b_2x^2$ in $\mathcal{P}$, define the sum of $p$ and $q$ as

$$p+q := (a_0+b_0) + (a_1+b_1)x + (a_2+b_2)x^2\ .$$ 

Clearly $p+q$ is a polynomial of degree at most 2 and hence belongs to $\mathcal{P}$.

2. **(Scalar Multiplication)** Any vector $p = a_0 + a_1x + a_2x^2 \in \mathcal{P}$ can be multiplied by a scalar $k \in \mathbb{R}$ to obtain a new vector $kp \in \mathcal{P}$ defined as follows:
$$
kp :=  ka_0 + (ka_1)x + (ka_2)x^2
$$.

You can verify that the vector addition and scalar multiplication operations as defined above satisfy the following properties:

1. **(Properties of vector addition)**  The vector space $\mathcal{P}$ forms a ***commutative group*** with respect to the vector addition operation. i.e, it satisfies the following properties:
	-  For all vectors $p,q,r \in \mathcal{P}$, $p + (q+r) = (p+q) + r$ **(Associativity)** 
	- There exists $0 \in \mathcal{P}$ (a.k.a the zero polynomial) such that for all $p \in \mathcal{P}$,  $p + 0 = 0 + p = p$ **(Additive Identity)**.
	-  For all $p \in \mathcal{P}$, there exists $q \in P$ such that $p + q = q + p = 0$ **(Additive Inverse)**
	-  For all vectors $p,q \in \mathcal{P}$, $p + q = q + p$ **(Commutativity)** 

2. **(Multiplicative identity)** 
3. **(Distributive properties)** 
4. **(Associativity of scalar multiplication)**

We say that $\mathcal{P}$ along with the vector addition ($+$) and scalar multiplication $(\cdot)$ is a **vector space over the field $\mathbb{R}$**. 

If vector spaces still look somewhat abstract to you, let us visualize them. Consider a polynomial $p = a_0 + a_1x + a_2x^2 \in \mathcal{P}$. You can view this as the point $\tilde{p} = (a_1, a_2, a_3) \in \mathbb{R}^3$. Each polynomial in $\mathcal{P}$ maps to a unique point in $\mathbb{R}^3$ and vice-versa. What more? The polynomial $p+q$ maps to the point $\tilde{p} + \tilde{q}$ and the polynomial $kp$ maps to the point $k\tilde{p}$.  Also the properties of vector addition and scalar multiplication which we observed for the polynomials holds true for the points in $\mathbb{R}^3$ as well.

![](/blog_docs/matrix_dec/r_cube.png)


 *Thus whenever you find it hard to visualize $\mathcal{P}$ you can work with $\mathbb{R}^3$ instead.*

### Linear independence, basis and dimension
## Linear Maps (aka) Matrices