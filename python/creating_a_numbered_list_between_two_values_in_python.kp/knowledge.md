---
title: What is the process for creating a list of numbers between two given values?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the range() function to create a list with numbers between two values in Python.
---

**Contents**

[TOC]

# Section 1: Using a For Loop

Using a for loop to create a list with numbers between two values is a simple and straightforward approach.

```
# Create a list of numbers between two values
start = 5
end = 10

# Create a list
numbers_list = []

# Use a for loop to add numbers to the list
for i in range(start, end+1):
    numbers_list.append(i)

# Print the list
print(numbers_list)
```

# Section 2: Using List Comprehension

Using list comprehension is a more concise way to create a list with numbers between two values.

```
# Create a list of numbers between two values
start = 5
end = 10

# Use list comprehension to create a list
numbers_list = [i for i in range(start, end+1)]

# Print the list
print(numbers_list)
```

# Section 3: Using Numpy Arrays

Using NumPy arrays is another way to create a list with numbers between two values.

```
# Import the NumPy library
import numpy as np

# Create a list of numbers between two values
start = 5
end = 10

# Use the arange() function to create an array
numbers_list = np.arange(start, end+1)

# Print the list
print(numbers_list)
```

# Section 4: Using the Range Function

Using the range() function is yet another way to create a list with numbers between two values.

```
# Create a list of numbers between two values
start = 5
end = 10

# Use the range() function to create a list
numbers_list = list(range(start, end+1))

# Print the list
print(numbers_list)
```
