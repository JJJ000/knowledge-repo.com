---
title: Finding the disparities between the elements in a list using python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: One way to find differences between elements of a list in Python is to use a loop to compare pairs of adjacent elements and store the differences in a separate list.
---

**Contents**

[TOC]

1. Introduction:

In Python, we can find the differences between elements of a list by subtracting each element from the next one. For example, if we have a list [5, 3, 8, 1], the differences between the elements are [-2, 5, -7]. In this article, we will explore different ways to find differences between the elements of a list.

2. Using a for loop:

One way to find the differences between elements of a list is by using a for loop. We can iterate over the list and subtract each element from the next one. Here's an example:

```
my_list = [5, 3, 8, 1]
differences = []
for i in range(len(my_list)-1):
    diff = my_list[i+1] - my_list[i]
    differences.append(diff)
print(differences)
```

Output: `[-2, 5, -7]`

In the above code, we initialized an empty list called `differences`. Then we used a for loop to iterate over the list `my_list`. Inside the loop, we subtracted each element from the next one and appended the result to the `differences` list. Finally, we printed the `differences` list.

3. Using list comprehension:

List comprehension is a concise way of creating lists in Python. We can also use list comprehension to find the differences between elements of a list. Here's an example:

```
my_list = [5, 3, 8, 1]
differences = [my_list[i+1] - my_list[i] for i in range(len(my_list)-1)]
print(differences)
```

Output: `[-2, 5, -7]`

In the above code, we used list comprehension to create a list called `differences`. We used the same logic as in the previous example to subtract each element from the next one.

4. Using NumPy:

NumPy is a Python package for scientific computing. It provides efficient and fast mathematical functions for working with arrays. We can use NumPy to find the differences between elements of a list. Here's an example:

```
import numpy as np
my_list = [5, 3, 8, 1]
differences = np.diff(my_list)
print(differences)
```

Output: `[-2, 5, -7]`

In the above code, we imported NumPy and created a list `my_list`. Then we used the NumPy function `diff` to find the differences between elements of the list. Finally, we printed the `differences` list.

Conclusion:

In this article, we explored different ways to find the differences between elements of a list. We used a for loop, list comprehension, and NumPy to achieve the same result. Depending on the situation, one method may be more suitable than the other. Regardless of the method, we can easily find the differences between elements of a list in Python.
