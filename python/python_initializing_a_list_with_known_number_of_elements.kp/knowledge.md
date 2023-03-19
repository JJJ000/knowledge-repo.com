---
title: In python, how to set up a list with a predefined number of elements
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: One way to initialize a list with a known number of elements in Python is to use a list comprehension or the built-in `range()` function.
---

**Contents**

[TOC]

# Introduction
In Python, lists are used for storing multiple values in a single variable. Sometimes, we need to create a list with a fixed number of elements. Initializing a list to a known number of elements can be achieved by various methods in Python. In this article, we will discuss some of the methods to initialize a list to a known number of elements.

# Using a for loop and append()
One of the simplest ways to initialize a list to a known number of elements is by using a for loop and appending the elements to the list. Here's an example:

```
my_list = []
for i in range(10):
    my_list.append(0)
print(my_list)
```

In the above code, we have created an empty list `my_list` and used a for loop to append the value `0` to the list 10 times. The output of the code will be:

```
[0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
```

# Using a list comprehension
Another way to initialize a list to a known number of elements is by using a list comprehension. Here's an example:

```
my_list = [0 for i in range(10)]
print(my_list)
```

In the above code, we have used a list comprehension to create a list with 10 elements and set each element to `0`. The output of the code will be:

```
[0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
```

# Using the * operator
Python provides a way to initialize a list to a known number of elements using the * operator. Here's an example:

```
my_list = [0] * 10
print(my_list)
```

In the above code, we have used the * operator to initialize a list with 10 elements and set each element to `0`. The output of the code will be:

```
[0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
```

# Conclusion
In this article, we have discussed some of the methods to initialize a list to a known number of elements in Python. We can use a for loop and append(), a list comprehension, or the * operator to achieve this. These methods can help us to create lists with a fixed number of elements which can be useful in various programming tasks.
