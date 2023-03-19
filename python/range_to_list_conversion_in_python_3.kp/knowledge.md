---
title: How can the range in Python 3 be converted to a list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the list() function to turn a range into a list in Python 3.
---

**Contents**

[TOC]

# Introduction
Python 3 has a built-in function range() that creates a sequence of numbers. When we want the sequence of numbers to be in list format, we can turn the range into a list. In this article, we will discuss the different ways to turn a range into a list.

# Using list()
One way to turn a range into a list is by using the built-in list() function. We can pass the range object as an argument to the function, and it will return the list of numbers.

```python
numbers = list(range(1, 6))
print(numbers)
```

Output:
```python
[1, 2, 3, 4, 5]
```

In the code above, we created a variable named numbers and assigned the list object returned by the list() function. The function took the range object as an argument, which starts at 1 and ends at 6, but excludes 6.

# Using a list comprehension
Another way to turn a range into a list is by using a list comprehension. We can use the range() function in the list comprehension and iterate over its values.

```python
numbers = [num for num in range(1, 6)]
print(numbers)
```

Output:
```python
[1, 2, 3, 4, 5]
```

In the code above, we created a variable named numbers and assigned the list object using a list comprehension. The list comprehension iterates over the values of the range object, starting at 1 and ending at 6, but excluding 6.

# Using * expression
We can also use the * expression to unpack the range object and create a list of its values.

```python
numbers = [*range(1, 6)]
print(numbers)
```

Output:
```python
[1, 2, 3, 4, 5]
```

In the code above, we created a variable named numbers and assigned the list object using the * expression. The expression unpacks the range object starting at 1 and ending at 6, but excluding 6, and creates a list of its values.

# Conclusion
Turning a range into a list is a common operation in Python. We discussed three ways to achieve this: by using the list() function, list comprehension, and the * expression. It's important to note that all three ways are equally valid, and it depends on personal preference and specific situations to use any of them.
