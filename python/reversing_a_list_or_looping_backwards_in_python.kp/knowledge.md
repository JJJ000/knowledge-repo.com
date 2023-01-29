---
title: What is the process for looping through a list in reverse order?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: To reverse a list or loop over it backwards in Python, use the reversed() or reversed for loop.
---

**Contents**

[TOC]

# Using reversed()

The `reversed()` built-in function allows you to iterate over a sequence in reverse order. It takes an iterable object and returns an iterator object that can be used in a for loop to iterate over the sequence in reverse order.

Example:
```python
my_list = [1, 2, 3, 4, 5]

for item in reversed(my_list):
    print(item)

# Output:
5
4
3
2
1
```

# Using a for loop

You can also use a for loop to iterate over a sequence in reverse order. The for loop should start at the end of the list and decrement the index until it reaches the beginning of the list.

Example:
```python
my_list = [1, 2, 3, 4, 5]

for i in range(len(my_list)-1, -1, -1):
    print(my_list[i])

# Output:
5
4
3
2
1
```

# Using slicing

You can also use slicing to reverse a list. The syntax for slicing is `list[start:stop:step]`. By specifying a negative step size of `-1`, the list will be reversed.

Example:
```python
my_list = [1, 2, 3, 4, 5]

print(my_list[::-1])

# Output:
[5, 4, 3, 2, 1]
```

# Using reversed() and a for loop

You can combine the two methods to iterate over a sequence in reverse order. The `reversed()` built-in function can be used to get an iterator object that can be used in a for loop to iterate over the sequence in reverse order.

Example:
```python
my_list = [1, 2, 3, 4, 5]

for item in reversed(my_list):
    print(item)

# Output:
5
4
3
2
1
```
