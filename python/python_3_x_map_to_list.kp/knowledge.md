---
title: Retrieving a list from a map() function in Python 3.x
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the list() function to convert the map object to a list.
---

**Contents**

[TOC]

**Section 1 - Introduction**

The map() function in Python 3.x allows you to apply a function to each element of an iterable object (such as a list, tuple, or string) and return a list of the results. This can be useful for performing operations on a list of values, such as calculating the square of each element in a list.

**Section 2 - Syntax**

The syntax for the map() function is as follows:

```python
map(function, iterable)
```

Where function is the function to be applied to each element of the iterable and iterable is the iterable object (such as a list, tuple, or string).

**Section 3 - Example**

Let's say we have a list of numbers, and we want to calculate the square of each element in the list. We can use the map() function to do this:

```python
# Create a list of numbers
numbers = [1, 2, 3, 4, 5]

# Use map() to calculate the square of each element
squares = list(map(lambda x: x**2, numbers))

# Print the result
print(squares)

# Output: [1, 4, 9, 16, 25]
```

**Section 4 - Conclusion**

In this article, we discussed how to use the map() function to return a list in Python 3.x. We saw how to use the map() function with a lambda expression to apply a function to each element of an iterable object and return a list of the results.
