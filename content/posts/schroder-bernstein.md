---
title: The Schröder–Bernstein theorem
date: 2020-08-10
lastmode: 2020-08-10
author: Janaky Murthy

description: Explanation of the proof of the Schröder–Bernstein theorem
categories: [Basic Math]
tags: [Math]

draft: false
enableDisqus : true
enableMathJax: true
disableToC: false
disableAutoCollapse: true
---

I decided that my first blog post should be about something that gave me the 'wow' feeling - and I immediately knew that it has to be the **Schröder–Bernstein theorem**. The proof of this theorem was skipped in the lecture (as an exercise :P) and I was waiting for the lecture to get over to try the proof. After hours of failed attempt, I thought I might be missing something trivial and decided to google it. I am a fan of elegant proofs and this theorem has been close to my heart ever since. Okay, lets cut the drama and jump straight into the theorem.

### The Schröder–Bernstein theorem

**Theorem:** Let $A,B$ be any sets. If there are [injective functions](https://en.wikipedia.org/wiki/Injective_function)  $f:A \rightarrow B$ and $g:B \rightarrow A$ then there exists a [bijection](https://en.wikipedia.org/wiki/Bijection#:~:text=In%20mathematics%2C%20a%20bijection%2C%20bijective,element%20of%20the%20first%20set.) $h: A \rightarrow B$.

![](/blog_docs/schroder_bernstein/sets_A_B.png)


Before going into the proof, I would like to introduce you to an alternate restatement of this theorem. This is not used in the proof and can be skipped.

Let us first fix the following terminologies.

- |A| denotes the **cardinality** of set $A$.
- $|\{1,\ldots,n \}|=n$.
- If there exists an injection $f: A \rightarrow B$, we say $|A| \leq |B|$.
- We say that $|A| = |B|$ if there exists a bijection $f: A \rightarrow B$.
- As an example for infinite sets, $|\mathbb{N}| = |2\mathbb{N}|$ ($2\mathbb{N}$ is the set of all even natural numbers).


The Schröder–Bernstein theorem can now be restated as follows:

**Theorem (restated):** For any sets $A,B$, if $|A| \leq |B|$ and $|B| \leq |A|$ then $|A| = |B|$.

### Proof (Finite Case)

Let us do an easy special case first. Say $A = \{a_1, \ldots, a_n\}$ and $B=\{b_1,\ldots,b_k \}$ be finite sets with injections $f: A \rightarrow B$ and $g: B \rightarrow A$. If $f(A) = B$, we are done as $f$ is a bijection as well. We now argue that if $f(A) \subsetneq B$ then there can not exist any injection from $B$ to $A$ which is a contradiction. Since $f$ is an injection $f(a_i) \neq f(a_j)$ for $i \neq j$, meaning $B$ can be written as $B = \{f(a_1), \ldots, f(a_n), b_{n+1}, \ldots, b_k \}$. As $k >n$, by [pigeonhole principle](https://en.wikipedia.org/wiki/Pigeonhole_principle) there can not exist an injection from $B \rightarrow A$.

### Proof (Infinite Case)

The above proof idea does not carry over to the case when $A$ and $B$ are not finite. There are various proofs of this theorem. The proof presented in this post is based on what I read from <a href="https://artofproblemsolving.com/wiki/index.php/Schroeder-Bernstein_Theorem">here</a> (although I have used my own terminologies and visualized this as a graph).

Construct a **directed graph** $G(V,E)$ as follows:

- $V = A \cup B$.
- $E = \{(a,f(a)) : \forall a \in A\} \cup \{(b,g(b)) : \forall b \in B\}$.

![](/blog_docs/schroder_bernstein/graph_G.png)


It follows from the injectivity of $f$ and $g$, that both the **indegree and outdegree of any vertex in this graph is atmost 1**. So chains that have branches (as shown in the following diagrams) can not exist.

![](/blog_docs/schroder_bernstein/f_injectivity.png)

![](/blog_docs/schroder_bernstein/g_injectivity.png)

Hence the graph $G$ consists of **disjoint componenets** each of which is either a **cycle** or an **infinite chain**.

![](/blog_docs/schroder_bernstein/cycles.png)


![](/blog_docs/schroder_bernstein/infinite_chains.png)

An infinite chain can either start with a vertex from set $A$ (that is a blue vertex) or a vertex from set $B$ (a pink vertex). Let us call them **blue chains** and **pink chains** respectively. Observe that the first element of each pink chain do not have an incoming edge and these are precisely those elements in B that does not have a pre-image with respect to $f$. **The idea is to modify the pink chains so that all pink elements in this chain has exactly one incoming edge while preserving the number of outgoing edges of the blue elements**.

We are now ready to define our bijection $h: A \rightarrow B$.

Since all pink elements in cycles and blue chains have an incoming edge, **$h$ mimics $f$ for the blue elements in these components.**

![](/blog_docs/schroder_bernstein/h1.png)

However on pink chains, **$h$ maps each blue element to its parent vertex in the graph $G$.**  

![](/blog_docs/schroder_bernstein/h2.png)


More formally $h: A \rightarrow B$ is defined as:

$
  h(a) = \begin{cases}f(a) ; a \in \text{blue chain or a cycle}\cr
  g^{-1}(a) ; a \in \text{pink chain}\end{cases}
$

Let us verify that $h$ is a bijection. First of all $h$ is a valid function as $h$ is defined on all blue vertices and each blue vertex has outdegree 1. Further each pink vertex has indegree exactly equal to 1 implying $h$ is a bijection. That's all - we are done :)

**Aside:** Observe that if $A$ and $B$ were finite sets then all the components are cycles!

**Remarks**

1. There are various proofs of this theorem and the ideas used in this version are very similar to Konig's proof of this theorem.
2. This theorem is also referred to as **Cantor–Schröder–Bernstein theorem**.
3. **Any mistakes - technical, typos or any other mistake are solely my own**. Please let me know if you spot any. Thanks!
