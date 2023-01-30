---
title: Find the distinct elements in a list in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the set() function to get unique values from a list in Python.
---

**Contents**

[TOC]

**Section 1: Using Sets**

Sets are a data structure in Python that stores only unique values. To get the unique values from a list, we can convert the list to a set.

```python
# Create a list
my_list = [1, 2, 3, 1, 2, 3]

# Convert the list to a set
unique_list = set(my_list)

# Print the set
print(unique_list) # {1, 2, 3}
```

**Section 2: Using List Comprehension**

We can also use a list comprehension to get the unique values from a list.

```python
# Create a list
my_list = [1, 2, 3, 1, 2, 3]

# Use a list comprehension to get the unique values
unique_list = [x for x in my_list if my_list.count(x) == 1]

# Print the list
print(unique_list) # [1, 2, 3]
```

**Section 3: Using Dictionary**

We can also use a dictionary to get the unique values from a list.

```python
# Create a list
my_list = [1, 2, 3, 1, 2, 3]

# Create an empty dictionary
unique_dict = {}

# Iterate through the list and add each element to the dictionary
# If the element is already in the dictionary, it will be ignored
for x in my_list:
    unique_dict[x] = 0

# Get the keys of the dictionary
unique_list = unique_dict.keys()

# Print the list
print(unique_list) # [1, 2, 3]
```

**Section 4: Using Set Operations**

We can also use set operations to get the unique values from a list.

```python
# Create two lists
list_1 = [1, 2, 3]
list_2 = [1, 2, 3, 1, 2, 3]

# Get the difference between the two lists
unique_list = set(list_2) - set(list_1)

# Print the list
print(unique_list) # set()
```
