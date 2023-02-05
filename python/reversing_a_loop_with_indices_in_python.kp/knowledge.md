---
title: Iterate through the indices in reverse order
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: To loop backwards using indices in Python, start with the highest index and iterate with a decrementing step size.
---

**Contents**

[TOC]

### Using a For Loop

The most straightforward way to loop backwards using indices in Python is to use a `for` loop. This loop will iterate through the indices in reverse order, starting at the highest index and ending at the lowest.

```python
my_list = [1, 2, 3, 4]

for i in range(len(my_list)-1, -1, -1):
    print(my_list[i])
```

The `range` function takes three arguments: the starting index, the ending index, and the step size. In this example, we start at the highest index (`len(my_list)-1`) and count backwards in steps of -1.

### Using a While Loop

Another way to loop backwards using indices in Python is to use a `while` loop. This loop will also iterate through the indices in reverse order, starting at the highest index and ending at the lowest.

```python
my_list = [1, 2, 3, 4]

i = len(my_list) - 1
while i >= 0:
    print(my_list[i])
    i -= 1
```

In this example, we start at the highest index (`len(my_list)-1`) and decrement the index by 1 each time through the loop. The loop will continue until the index is less than 0.

### Using a List Comprehension

A third way to loop backwards using indices in Python is to use a list comprehension. This is a concise way to create a new list from an existing list.

```python
my_list = [1, 2, 3, 4]

new_list = [my_list[i] for i in range(len(my_list)-1, -1, -1)]
```

The `range` function takes three arguments: the starting index, the ending index, and the step size. In this example, we start at the highest index (`len(my_list)-1`) and count backwards in steps of -1. The new list will contain the elements of the original list in reverse order.

### Using a Reverse Function

Finally, another way to loop backwards using indices in Python is to use the `reversed` function. This function takes an iterable object and returns an iterator that yields the elements of the object in reverse order.

```python
my_list = [1, 2, 3, 4]

for element in reversed(my_list):
    print(element)
```

This is a simple and concise way to loop through the elements of a list in reverse order.
