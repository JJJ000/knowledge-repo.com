---
title: Refining a roster utilizing a record of true or false values
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use a list comprehension to filter the list based on a corresponding list of booleans.
---

**Contents**

[TOC]

### Introduction
Filtering a list based on a list of booleans is a common task in Python. Boolean values are often generated as a result of some condition checking when working with lists in Python, and filtering based on these boolean values is a useful technique for selecting only the desired elements of the list. In this tutorial, we will explore the various ways to filter a list based on a list of booleans.

### Method 1: Using a Loop
One way to filter a list based on a list of booleans is to use a loop to iterate over each element of the list and check the corresponding boolean value. If the boolean value is True, then the element is added to a new list. Here's an example:

```python
numbers = [1, 2, 3, 4, 5]
booleans = [True, False, True, False, True]

filtered_numbers = []
for i in range(len(numbers)):
    if booleans[i]:
        filtered_numbers.append(numbers[i])

print(filtered_numbers)  # Output: [1, 3, 5]
```

In this example, we have two lists `numbers` and `booleans` of the same length. We looped over the index values of `numbers`, and for each index, we checked the corresponding boolean value in `booleans`. If the value was `True`, we added the corresponding element from `numbers` to the new list `filtered_numbers`. Finally, we printed the filtered list.

### Method 2: Using a List Comprehension
Another way to filter a list based on a list of booleans is to use a list comprehension. A list comprehension is a way to create a new list by applying an expression to each element of an existing list. Here's an example:

```python
numbers = [1, 2, 3, 4, 5]
booleans = [True, False, True, False, True]

filtered_numbers = [numbers[i] for i in range(len(numbers)) if booleans[i]]

print(filtered_numbers)  # Output: [1, 3, 5]
```

In this example, we have used a list comprehension to create a new list `filtered_numbers`. We looped over the index values of `numbers`, and for each index, we checked the corresponding boolean value in `booleans`. If the value was `True`, we added the corresponding element from `numbers` to the new list `filtered_numbers`. Finally, we printed the filtered list.

### Method 3: Using the Zip Function
A third way to filter a list based on a list of booleans is to use the built-in `zip` function along with a list comprehension. The `zip` function takes two or more sequences and returns a new sequence of tuples, where the i-th tuple contains the i-th element from each of the input sequences. Here's an example:

```python
numbers = [1, 2, 3, 4, 5]
booleans = [True, False, True, False, True]

filtered_numbers = [num for num, boolean in zip(numbers, booleans) if boolean]

print(filtered_numbers)  # Output: [1, 3, 5]
```

In this example, we have used the `zip` function to create a new sequence of tuples, where each tuple contains an element from `numbers` and the corresponding boolean value from `booleans`. We looped over these tuples using a list comprehension, and for each tuple, we checked the boolean value. If the value was `True`, we added the corresponding element from `numbers` to the new list `filtered_numbers`. Finally, we printed the filtered list.

### Conclusion
In this tutorial, we explored three ways to filter a list based on a list of booleans in Python. These include using a loop, using a list comprehension, and using the `zip` function with a list comprehension. All of these methods will produce the same output when given the same input, and which method you choose may depend on personal preference or the requirements of your specific use case.
