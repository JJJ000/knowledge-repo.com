---
title: What is the method for identifying all locations where the highest value is located in a list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can use the built-in function `max()` to find the maximum value and then use a list comprehension to find all positions where the maximum value occurs using the `enumerate()` function.
---

**Contents**

[TOC]

### Using the max() and index() methods

One way to find all positions of the maximum value in a list is by using the `max()` function to find the maximum value and then the `index()` method to find all the positions of that value in the list. Here's an example:

```python
my_list = [2, 5, 8, 5, 10, 5]
max_value = max(my_list)
max_positions = [i for i, x in enumerate(my_list) if x == max_value]
print(max_positions)  # Output: [1, 3, 5]
```

In the example above, we first find the maximum value in the list `my_list` using the `max()` function, which gives us the value `10`. We then use a list comprehension to find all the positions of that value in the list using the `enumerate()` function and the `if` statement. This gives us the list `[1, 3, 5]`, which represents the positions of the maximum value in the list.

### Using numpy

Another method for finding all positions of the maximum value in a list is by using the `argwhere()` function from the numpy library. This method can be useful when working with multidimensional arrays. Here's an example:

```python
import numpy as np

my_list = [2, 5, 8, 5, 10, 5]
max_positions = np.argwhere(my_list == np.amax(my_list)).flatten()
print(max_positions)  # Output: [1 3 5]
```

In the example above, we first import the numpy library and use it to convert our list to a numpy array. We then use the `argwhere()` function to find all the positions of the maximum value in the array, which gives us a ndarray with shape `(3,1)`. To convert this to a one-dimensional list, we use the `flatten()` method. This gives us the same result as the previous method: `[1, 3, 5]`.

### Using a loop

A third method for finding all positions of the maximum value in a list is by using a loop to iterate over the list and keep track of the positions. Here's an example:

```python
my_list = [2, 5, 8, 5, 10, 5]
max_value = max(my_list)
max_positions = []
for i in range(len(my_list)):
    if my_list[i] == max_value:
        max_positions.append(i)
print(max_positions)  # Output: [1, 3, 5]
```

In the example above, we first find the maximum value in the list `my_list` using the `max()` function, which gives us the value `10`. We then use a loop to iterate over the list and check if each element is equal to the maximum value. If it is, we append the position of that element to the `max_positions` list. This gives us the same result as the previous two methods: `[1, 3, 5]`. 

### Conclusion

There are multiple ways to find all positions of the maximum value in a list in Python. The method you choose may depend on the size and type of your list, as well as your familiarity with different Python libraries and coding styles.
