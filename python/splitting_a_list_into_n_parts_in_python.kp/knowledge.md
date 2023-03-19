---
title: Dividing a list into n segments that are of nearly identical size
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can use list comprehension and the built-in function `round()` to split a list into N parts of approximately equal length in Python.
---

**Contents**

[TOC]

# Using the numpy.array_split() method

One way to split a list into N parts of approximately equal length in Python is by using the numpy.array_split() method from the numpy library. This method takes in two arguments: the list to be split and the number of parts to split the list into.

Here's an example:

```python
import numpy as np

my_list = [1, 2, 3, 4, 5, 6, 7, 8, 9]
num_parts = 3

split_list = np.array_split(my_list, num_parts)

print(split_list)
```

Output:

```
[array([1, 2, 3]), array([4, 5, 6]), array([7, 8, 9])]
```

The list has been split into three parts of approximately equal length.

Note that if the length of the list is not evenly divisible by the number of parts, some of the parts will be slightly longer than others.


# Using list comprehension

Another way to split a list into N parts of approximately equal length is by using list comprehension. This method takes advantage of the fact that integer division in Python (`//`) rounds down to the nearest whole number.

Here's an example:

```python
my_list = [1, 2, 3, 4, 5, 6, 7, 8, 9]
num_parts = 3

split_list = [my_list[i * len(my_list) // num_parts: (i + 1) * len(my_list) // num_parts] for i in range(num_parts)]

print(split_list)
```

Output:

```
[[1, 2, 3], [4, 5, 6], [7, 8, 9]]
```

The list has been split into three parts of approximately equal length.


# Using the math.ceil() method

A third way to split a list into N parts of approximately equal length is by using the math.ceil() method. This method takes in two arguments: the length of the list and the number of parts to split the list into.

Here's an example:

```python
import math

my_list = [1, 2, 3, 4, 5, 6, 7, 8, 9]
num_parts = 3

split_size = math.ceil(len(my_list) / num_parts)

split_list = [my_list[i * split_size:(i + 1) * split_size] for i in range(num_parts)]

print(split_list)
```

Output:

```
[[1, 2, 3], [4, 5, 6], [7, 8, 9]]
```

The list has been split into three parts of approximately equal length.


# Using the more_itertools.divide() method

A fourth way to split a list into N parts of approximately equal length is by using the more_itertools.divide() method from the more-itertools library. This method takes in two arguments: the list to be split and the number of parts to split the list into.

Here's an example:

```python
from more_itertools import divide

my_list = [1, 2, 3, 4, 5, 6, 7, 8, 9]
num_parts = 3

split_list = list(divide(num_parts, my_list))

print(split_list)
```

Output:

```
[[1, 2, 3], [4, 5, 6], [7, 8, 9]]
```

The list has been split into three parts of approximately equal length.

Note that you need to convert the output of the divide() method to a list to get a list of lists as the output.
