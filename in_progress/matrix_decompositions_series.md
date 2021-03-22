---
title: Notes on Basic Matrix Decompositions
date: 2020-12-08
lastmode: 2020-12-08
author: Janaky Murthy

description: Notes on basic matrix decompositions
categories: [Linear Algebra, Basic Math]
tags: [Math]

draft: false
enableDisqus : true
enableMathJax: true
disableToC: false
disableAutoCollapse: true
---

I was revising some basic matrix decomposition methods last week and I realised that I hadn't understood it well enough when I read it for the first time. Undoubtedly, I might have understood the bits and pieces but do I know what the big picture looks like? A good way to test this is to explain the concepts to someone. With the COVID lockdown keeping me at home, the best (and only) option I have is to explain it to myself. I tried doing this and realised that I was handwaving at some parts when I thought things were ***obvious***. This is exactly what leads to incomplete understanding!

Writing is another alternative to technical discussions. I can see few shortcomings though: it takes more time to write and you receive delayed and usually limited (in my case zero) feedback. However it is useful in other ways, you have time to organise your thoughts. Once you have written something, you can use it as a resource later (I like to read my own write-ups after a while and cringe about how I have written it. If you want to know how it feels, try reading your diaries from your teens when you get older).

 I have decided to write a series of short blogs on basic matrix decomposition methods for the benefit of **my own understanding**. The materials in these blog posts can be found in any standard Linear Algebra textbook. The goal of these blog posts is to convey the big picture as well as sketch details of some basic matrix decomposition methods. Here is the plan for this series.

 ## Plan

 1. [**Linear Algebra 101: (optional)**]()
 2. [**What is Matrix Decomposition**](matrix_decomposition.md)
 3. [**LU Decomposition**]()
 4. [**Chloesky Decomposition**]()
 5. [**QR Decomposition**]()
 6. [**Eigen stuff...(optional)**]()
 7. [**Eigen Decomposition**]()
 8. [**Jordan Decomposition**]()
 9. [**Positive semidefinite matrices**]()
 10. [**Singular value decomposition**]()

  I intend to write these posts in my free time and hence may update this blog series very infrequently.

**Remarks**:
1. I am an extremely **verbose** writer. I don't optimise my posts for length. Please read the posts at your own risk.
2. Most of these posts will have a good mix of formal and informal writing style.
3. If you spot any error, please let me know in the comments. Thanks!

**References:**

I have used the following resources while I was learning Linear Algebra. I will cite other particular references (if any) on individual posts.

1. [Linear Algebra Done Right, Sheldon Axler](https://linear.axler.net/)
2. Some parts of these [lecture notes](http://math.iisc.ac.in/~patil/web_courses/e0-219-laa11/e0-219-laa11-lecturenotes.html) from a course taught by [Prof. D.P. Patil](http://math.iisc.ac.in/~patil/index.html).
