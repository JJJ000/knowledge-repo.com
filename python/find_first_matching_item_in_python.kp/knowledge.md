---
title: Retrieve the initial element from an iterable that fulfills a requirement
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the built-in function next() and pass it a generator expression to get the first item from an iterable that matches a condition in Python.
---

**Contents**

[TOC]

**Section 1: Using List Comprehension**

List comprehension is a powerful tool for quickly filtering and mapping lists in Python. To get the first item from an iterable that matches a condition, we can use the following syntax:

```
first_item = [item for item in iterable if condition][0]
```

**Section 2: Example**

For example, let's say we have a list of numbers and we want to get the first number that is greater than 5:

```
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9]
first_number_greater_than_5 = [number for number in numbers if number > 5][0]
```

The value of `first_number_greater_than_5` will be 6.

**Section 3: Using next()**

We can also use the `next()` function to get the first item from an iterable that matches a condition. The syntax for this is as follows:

```
first_item = next(item for item in iterable if condition)
```

**Section 4: Example**

For example, let's say we have a list of words and we want to get the first word that is longer than 5 letters:

```
words = ["cat", "dog", "elephant", "giraffe", "hippo"]
first_word_longer_than_5 = next(word for word in words if len(word) > 5)
```

The value of `first_word_longer_than_5` will be "elephant".
