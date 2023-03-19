---
title: In python, extract the initial component of each tuple contained in a list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use a list comprehension with indexing to retrieve the first element of each tuple in a list `[t[0] for t in list\_of\_tuples]`.
---

**Contents**

[TOC]

# Section 1: Introduction
  
A tuple is a collection of immutable elements. We can create a list of tuples in Python. We may need to access the first element of each tuple in such lists to perform some operations. In this tutorial, we will explore different ways to get the first element of each tuple in a list.


# Section 2: Using loop

One of the simplest ways to get the first element of each tuple in a list is to use a loop. We can iterate through the tuples in the list and access the first element using indexing. Here’s an example:

```python
my_list = [(1, 2), (3, 4), (5, 6)]
first_elements = []

for tup in my_list:
    first_elements.append(tup[0])
    
print(first_elements) # Output: [1, 3, 5]
```

In the above code, we created a list of tuples called `my_list`. Then, we created an empty list called `first_elements`. We then used a `for` loop to iterate through each tuple in `my_list`. In each iteration, we accessed the first element of the tuple using `tup[0]` and appended it to the `first_elements` list. Finally, we printed the `first_elements` list.


# Section 3: Using list comprehension

We can also use list comprehension to get the first element of each tuple in a list. Here’s an example:

```python
my_list = [(1, 2), (3, 4), (5, 6)]

first_elements = [tup[0] for tup in my_list]

print(first_elements) # Output: [1, 3, 5]
```

In the above code, we used list comprehension to create a new list of the first elements of each tuple in the `my_list` list. We accessed the first element of each tuple using `tup[0]` and added it to the list comprehension. Finally, we printed the `first_elements` list.


# Section 4: Using the map() function

Another way to get the first element of each tuple in a list is to use the `map()` function. Here’s an example:

```python
my_list = [(1, 2), (3, 4), (5, 6)]

first_elements = list(map(lambda x: x[0], my_list))

print(first_elements) # Output: [1, 3, 5]
```

In the above code, we used the `map()` function to apply the `lambda` function to each tuple in the `my_list` list. The `lambda` function accessed the first element of each tuple using `x[0]`. We then converted the result into a list using the `list()` function and stored it in the `first_elements` variable. Finally, we printed the `first_elements` list.
