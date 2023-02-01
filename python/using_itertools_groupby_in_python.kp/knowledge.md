---
title: What is the proper syntax for using itertools.groupby()?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Itertools.groupby() can be used to group items in an iterable based on a key function or condition.
---

**Contents**

[TOC]

# Introduction
The itertools.groupby() function is a powerful tool for grouping data in Python. It is used to group iterable objects together based on a key function. This function can be used to group data into categories, such as alphabetical or numerical ranges, or to group data into logical collections.

# Syntax
The syntax for the itertools.groupby() function is as follows:

```
itertools.groupby(iterable, key=None)
```

Where:
- iterable is the list of items to be grouped
- key is a function that returns a value on which the grouping will be based

# Examples
Here are some examples of how to use the itertools.groupby() function:

## Grouping Strings

To group a list of strings by their first letter, you can use the following code:

```
from itertools import groupby

words = ['apple', 'banana', 'carrot', 'dog', 'elephant']

for letter, items in groupby(words, lambda x: x[0]):
    print(letter)
    for item in items:
        print(' ', item)
```

This will output the following result:

```
a
 apple
b
 banana
c
 carrot
d
 dog
e
 elephant
```

## Grouping Numbers

To group a list of numbers by their range, you can use the following code:

```
from itertools import groupby

numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

for range, items in groupby(numbers, lambda x: x // 3):
    print(range)
    for item in items:
        print(' ', item)
```

This will output the following result:

```
0
 1
 2
 3
1
 4
 5
 6
2
 7
 8
 9
3
 10
```

# Conclusion
The itertools.groupby() function is a powerful tool for grouping data in Python. It can be used to group data into logical collections, such as alphabetical or numerical ranges, or to group data into logical collections based on a key function. Examples of how to use the itertools.groupby() function have been provided above.
