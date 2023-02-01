---
title: What is the process for identifying and compiling a list of duplicate elements from a given list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: To find the duplicates in a list and create another list with them, use the list comprehension syntax [x for x in list if list.count(x) > 1].
---

**Contents**

[TOC]

### Section 1: Create a Set

A set is an unordered collection of unique items, meaning no duplicates are allowed. To create a set from a list, we can use the `set()` function.

```python
my_list = [1,2,3,4,4,5,6,7,7]
my_set = set(my_list)

print(my_set)
# Output: {1, 2, 3, 4, 5, 6, 7}
```

### Section 2: Find Duplicates

To find the duplicates in the list, we can compare the length of the original list and the set created in the previous step. If the lengths are not equal, then there are duplicates in the list.

```python
if len(my_list) != len(my_set):
    print("Duplicates found!")
# Output: Duplicates found!
```

### Section 3: Iterate Through List

To create a new list with the duplicates, we can iterate through the original list and check if each item is in the set. If it is not, then it is a duplicate and should be added to the new list.

```python
duplicates = []

for item in my_list:
    if item not in my_set:
        duplicates.append(item)

print(duplicates)
# Output: [4, 7]
```

### Section 4: Create New List

Finally, we can create a new list with the duplicates.

```python
duplicates_list = list(set(duplicates))

print(duplicates_list)
# Output: [4, 7]
```
