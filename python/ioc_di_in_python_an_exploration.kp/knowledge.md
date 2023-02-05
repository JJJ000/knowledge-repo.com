---
title: What are the reasons that inversion of control/dependency injection is not widely used in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Python`s dynamic nature makes it difficult to implement IoC/DI, since it requires static typing to be effective.
---

**Contents**

[TOC]

## Lack of Standardization
Python does not have a single standard for implementing IoC / DI. There are many different libraries and frameworks that can be used to achieve IoC / DI, but none of them are universally adopted. This lack of standardization makes it difficult for developers to make an informed decision about which library or framework to use.

## Lack of Popularity
IoC / DI is not a widely used concept in Python. Many developers are familiar with the concept, but it is not a popular technique in the Python community. This lack of popularity is likely due to the fact that Python is a dynamically typed language, which makes it easier to achieve the same results without using IoC / DI.

## Complexity
IoC / DI can be quite complex to implement in Python. This is because Python does not have a built-in mechanism for dependency injection, and requires the use of external libraries and frameworks. This complexity can be a barrier to entry for developers who are not familiar with the concept.

## Performance
IoC / DI can also have a negative impact on performance, as it adds an extra layer of complexity to an application. This can be especially problematic in Python, as the language is not optimized for performance.
