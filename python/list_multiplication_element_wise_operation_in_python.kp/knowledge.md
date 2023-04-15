---
title: What is the process to multiply each element of two lists individually?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use a list comprehension or numpy to perform element-wise multiplication of two lists in Python.
---

**Contents**

[TOC]

## Introduction

Python is a powerful and easy-to-learn programming language used for many applications like data analytics, machine learning, and software development. One of the important applications of python is in numerical operations. In this tutorial, we will learn how to perform element-wise multiplication of two lists in Python.


## Creating Lists

The first step to perform element-wise multiplication of two lists is to create two lists with equal lengths. We can use the bracket notation to create lists in Python.

```python
# create two lists
list1 = [1, 2, 3]
list2 = [4, 5, 6]
```

## Element-wise Multiplication

Once we have two lists, we can perform element-wise multiplication by iterating over the elements of both lists and multiplying them. We can do this using a for loop and the * operator.

```python
# element-wise multiplication
result = []
for i in range(len(list1)):
    result.append(list1[i] * list2[i])
print(result)  # Output: [4, 10, 18]
```

Alternatively, we can also use list comprehension to perform element-wise multiplication in a more concise way.

```python
# element-wise multiplication using list comprehension
result = [list1[i] * list2[i] for i in range(len(list1))]
print(result)  # Output: [4, 10, 18]
```

## Conclusion

In this tutorial, we have learned how to perform element-wise multiplication of two lists in Python. We first created two lists using the bracket notation, and then we used a for loop and the * operator to iterate over the elements of both lists and multiply them. Finally, we learned how to use list comprehension to perform element-wise multiplication in a more concise way.
