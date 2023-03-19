---
title: What is the method to ensure Python lists have only unique elements?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the set() function to convert the list into a set, then convert it back to a list.
---

**Contents**

[TOC]

## Using set()

One way to make a list contain only distinct elements is by converting the list to a set and then back to a list. The set data type contains only unique elements, so any duplicates will be removed during the conversion process.

```python
my_list = [1, 2, 2, 3, 4, 4, 5]
unique_list = list(set(my_list))
print(unique_list) # [1, 2, 3, 4, 5]
```


## Using for loop

Another way to make a list contain only distinct elements is by using a for loop to compare each element in the list to the rest of the elements and removing duplicates.

```python
my_list = [1, 2, 2, 3, 4, 4, 5]
unique_list = []

for element in my_list:
    if element not in unique_list:
        unique_list.append(element)

print(unique_list) # [1, 2, 3, 4, 5]
```

## Using dictionary

Another way to make a list contain only distinct elements is by using a dictionary. We can add elements from the list to the dictionary as the keys, and since dictionary keys must be unique, any duplicates will be removed automatically.

```python
my_list = [1, 2, 2, 3, 4, 4, 5]
my_dict = {}

for element in my_list:
    my_dict[element] = None

unique_list = list(my_dict.keys())
print(unique_list) # [1, 2, 3, 4, 5]
```


## Using defaultdict

We can also use defaultdict in Python's collections module to make a list contain only distinct elements. We can set the default value of this dictionary to 0, so any new keys that are added will have a value of 0. We can then add elements from the list to the dictionary as keys, and since dictionary keys must be unique, any duplicates will be removed automatically.

```python
from collections import defaultdict

my_list = [1, 2, 2, 3, 4, 4, 5]
my_dict = defaultdict(int)

for element in my_list:
    my_dict[element] = 0

unique_list = list(my_dict.keys())
print(unique_list) # [1, 2, 3, 4, 5]
```
