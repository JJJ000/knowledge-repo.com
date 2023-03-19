---
title: What is the equivalent of foreach in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: The Python equivalent of foreach is the for loop which iterates over a sequence or iterable.
---

**Contents**

[TOC]

## Section 1: Introduction

Python does not have a built-in `foreach` loop. However, there are several ways to achieve the same functionality using different approaches.


## Section 2: Using a for loop

The most common way to iterate over a collection of elements in Python is by using a for loop. For example, let's say we have a list called `numbers` which contains some integer values. We can iterate over the list and perform a certain operation on each item as follows:

```
numbers = [1, 2, 3, 4, 5]

for num in numbers:
    print(num)
```

This will output the following:

```
1
2
3
4
5
```

This is equivalent to a foreach loop in other programming languages.


## Section 3: Using map

Another way to achieve the same functionality is by using the `map` function. The `map` function takes a function and an iterable as arguments and returns a new iterable object with the function applied to each item in the original iterable. Here's an example:

```
numbers = [1, 2, 3, 4, 5]

def print_number(num):
    print(num)

map(print_number, numbers)
```

This will output the following:

```
1
2
3
4
5
```

This is also equivalent to a foreach loop in other programming languages.


## Section 4: Using list comprehension

Finally, we can use list comprehension to achieve the same functionality as a foreach loop. List comprehension allows us to create a new list by iterating over an existing iterable and applying some logic to each item. Here's an example:

```
numbers = [1, 2, 3, 4, 5]

[print(num) for num in numbers]
```

This will output the following:

```
1
2
3
4
5
```

This is a concise and readable way of achieving the same functionality as a foreach loop.
