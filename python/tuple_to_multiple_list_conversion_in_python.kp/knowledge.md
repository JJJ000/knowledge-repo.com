---
title: What is the method for transforming a list of tuples into numerous lists?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: Use the `zip()` and `*` operator to unpack the tuples and convert them to multiple lists.
---

**Contents**

[TOC]

## Section 1: Introduction
In Python, a list of tuples can be converted to multiple lists by making use of the `zip` function. The `zip` function takes multiple iterables and returns a tuple with corresponding elements from each iterable.

## Section 2: Example
Suppose we have a list of tuples as follows:
``` python
list_of_tuples = [(1, 'a'), (2, 'b'), (3, 'c')]
```
To convert this list of tuples to multiple lists, we can make use of the `zip` function as follows:

``` python
x, y = zip(*list_of_tuples)
```

Now the variable `x` will contain the first element of each tuple, while the variable `y` will contain the second element of each tuple. Thus, `x` and `y` will be:
``` python
# x contains the first element of each tuple
(1, 2, 3)

# y contains the second element of each tuple
('a', 'b', 'c')
```

## Section 3: Explanation
In the code `x, y = zip(*list_of_tuples)`, the `*` symbol is used to unpack the list of tuples. This means that each tuple is passed to the `zip` function as a separate argument. Essentially, this is equivalent to calling the following:

``` python
x, y = zip((1, 'a'), (2, 'b'), (3, 'c'))
```

The `zip` function then takes the corresponding elements from each tuple and returns a tuple that contains those elements. Thus, `x` will contain the first element of each tuple `(1, 2, 3)`, while `y` will contain the second element of each tuple `('a', 'b', 'c')`.

## Section 4: Conclusion
Using the `zip` function, we can easily convert a list of tuples to multiple lists. This can be useful in situations where we want to manipulate the elements of the tuples separately.
