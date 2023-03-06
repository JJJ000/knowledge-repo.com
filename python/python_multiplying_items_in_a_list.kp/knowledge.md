---
title: What is the method to multiply all elements in a list using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the built-in Python function reduce() with a lambda function that multiplies its two arguments together.
---

**Contents**

[TOC]

Section 1: Introduction
In this task, we need to multiply all the items in a list using Python. This can be done by creating a for loop or by using the built-in reduce() function. In this article, we will discuss both approaches.

Section 2: Using a for loop
One way to multiply all items in a list is by using a for loop. We create a variable, say result, and initialize it to 1. Then we iterate through each item in the list, and multiply it with the result variable. After the loop completes, we return the final result.

Here's the code:

```python
lst = [1, 2, 3, 4, 5]
result = 1
for item in lst:
    result *= item
print(result)  # Output: 120
```

Section 3: Using the reduce() function
Another approach is to use Python's built-in reduce() function from the functools module. This function takes two arguments: a function that performs the operation and an iterable (list, tuple, etc.) to apply that function to.

Here's the code:

```python
from functools import reduce

lst = [1, 2, 3, 4, 5]
result = reduce(lambda x, y: x*y, lst)
print(result)  # Output: 120
```

In the above code, we imported the reduce() function from the functools module, created a list, and then passed it to the reduce() function along with a lambda function that multiplies two numbers.

Section 4: Conclusion
In this article, we have discussed two methods to multiply all items in a list in Python. We can either use a for loop or the built-in reduce() function from the functools module. Both approaches are simple and effective.
