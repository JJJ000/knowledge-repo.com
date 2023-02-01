---
title: What is the procedure for locating all instances of an item in a list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the list.count() method to find all occurrences of an element in a list.
---

**Contents**

[TOC]

## Using for loop

The most common and straightforward way to find all occurrences of an element in a list is to use a for loop. The following code demonstrates this approach:

```python
my_list = [1,2,3,4,5,6,7,8,9]

# element to find
element = 4

# list to store all occurrences
occurrences = []

# iterate through the list
for i in my_list:
    # check if current element is equal to element
    if i == element:
        # append element to occurrences
        occurrences.append(i)

# print all occurrences
print(occurrences)
```

## Using list comprehension

Another approach to find all occurrences of an element in a list is to use list comprehension. The following code demonstrates this approach:

```python
my_list = [1,2,3,4,5,6,7,8,9]

# element to find
element = 4

# use list comprehension to find all occurrences
occurrences = [i for i in my_list if i == element]

# print all occurrences
print(occurrences)
```

## Using the count() method

The count() method can also be used to find all occurrences of an element in a list. The following code demonstrates this approach:

```python
my_list = [1,2,3,4,5,6,7,8,9]

# element to find
element = 4

# use the count() method to find all occurrences
occurrences = [element] * my_list.count(element)

# print all occurrences
print(occurrences)
```
