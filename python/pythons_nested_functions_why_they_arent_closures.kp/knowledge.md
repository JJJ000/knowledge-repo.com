---
title: What is the reason for not calling Python nested functions as closures?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Python nested functions are not directly called closures because they do not necessarily have access to variables in the outer function`s scope, which is a defining characteristic of closures.
---

**Contents**

[TOC]

Introduction
Python is a dynamic high-level programming language with powerful features, which include the ability to create nested functions or functions within functions. There are some terminologies related to nested functions, such as closures, but Python nested functions are not called closures. In this article, we will look at the reasons behind it.

What is Nested Function?
Before going into why Python nested functions are not called closures, let us first discuss what a nested function is. A nested function is a function defined inside another function. It has access to the variables and names declared in the enclosing function, as well as to the global names.

What is Closure?
A closure is a function object that has access to the variables in the enclosing lexical scope, even after the outer function has completed execution. In other words, a closure is a nested function that remembers the values of the variables in the outer function even after the outer function has returned.

Why Python Nested Functions are not called Closures?
There are two reasons why Python nested functions are not called closures.

Firstly, in Python, all functions are closures. This means that all nested functions in Python have access to the enclosing lexical scope, making them closures. Hence, specifically calling nested functions closures in Python is redundant.

Secondly, in Python, a closure must have a free variable that is bound in the enclosing lexical scope. In other words, the variable must have a value that is not defined in the nested function but is instead defined in the enclosing function. Python nested functions do not always have free variables, and so calling them closures would be inaccurate.

Conclusion
Python nested functions are not called closures since all functions in Python are closures. Besides, Python nested functions do not always have free variables, which is a requirement for a closure. Hence, it can be said that calling nested functions closures in Python is not necessary.
