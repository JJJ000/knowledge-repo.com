---
title: What is the difference between an iterator, an iterable, and an iteration?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: An iterator is an object that can be used to iterate through an iterable, which is an object that can be used in a for loop, and iteration is the process of looping through the iterable.
---

**Contents**

[TOC]

### Iterator

An iterator is an object that contains a countable number of values. It implements the iterator protocol, which consists of the methods `__iter__()` and `__next__()`. An iterator is an object that can be iterated upon, meaning it can be looped over with a for loop.

### Iterable

An iterable is an object that can return an iterator. It implements the iterable protocol, which consists of the method `__iter__()`. Examples of iterables include lists, tuples, and dictionaries.

### Iteration

Iteration is the process of looping over an iterable object. During each iteration, the iterator returns a value, which can then be used in the loop. For example, you can use a for loop to iterate over a list and print out each item in the list.

### Examples

Here is an example of iteration using a for loop:

```python
my_list = [1, 2, 3, 4]

for item in my_list:
    print(item)

# Output:
# 1
# 2
# 3
# 4
```
