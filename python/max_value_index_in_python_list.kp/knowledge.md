---
title: What is the method in Python to determine the highest value and its corresponding index in a list that follows Python conventions?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use the built-in function `max()` with the optional parameter `key` set to `list.index`.
---

**Contents**

[TOC]

Section 1: Using max() and index()
The simplest and most pythonic way to find the maximum value and its index in a list is to use the built-in max() and index() functions. Here's an example:

```python
numbers = [1, 5, 2, 10, 7]

max_value = max(numbers)
max_index = numbers.index(max_value)

print(f"Maximum value is {max_value} at index {max_index}")
```
Output: 

```
Maximum value is 10 at index 3
```
In this approach, we first find the maximum value in the list using the max() function. Then, we find the index of the maximum value using the index() function. 

One thing to keep in mind is that this approach assumes that the list has at least one element. If the list is empty, an error will be raised.

Section 2: Using enumerate() and max()
Another pythonic way to find the maximum value and its index is to use the enumerate() function together with the max() function. Here's how it works:

```python
numbers = [1, 5, 2, 10, 7]

max_index, max_value = max(enumerate(numbers), key=lambda x: x[1])

print(f"Maximum value is {max_value} at index {max_index}")
```
Output: 

```
Maximum value is 10 at index 3
```

In this approach, we use the enumerate() function to iterate over the list and get both the index and the value of each element. We then pass this to the max() function, which returns the tuple with the maximum value. Finally, we unpack the tuple into two separate variables (max_index and max_value) and print the result.

Section 3: Using numpy.argmax()
If you have numpy installed, you can use the argmax() function to find the index of the maximum value in a list. Here's an example:

```python
import numpy as np

numbers = [1, 5, 2, 10, 7]

max_index = np.argmax(numbers)
max_value = numbers[max_index]

print(f"Maximum value is {max_value} at index {max_index}")
```
Output: 

```
Maximum value is 10 at index 3
```

In this approach, we use the argmax() function from numpy to find the index of the maximum value in the list. We then use this index to get the value at that position in the list.

Section 4: Using sorted() and pop()
Another way to find the maximum value and its index is to use the sorted() function along with the pop() method. Here's an example:

```python
numbers = [1, 5, 2, 10, 7]

sorted_numbers = sorted(numbers)
max_value = sorted_numbers.pop()
max_index = numbers.index(max_value)

print(f"Maximum value is {max_value} at index {max_index}")
```
Output: 

```
Maximum value is 10 at index 3
```

In this approach, we first make a sorted copy of the list using the sorted() function. We then use the pop() method to remove and return the maximum value from the sorted list. Finally, we use the index() function to get the index of the maximum value in the original list.
