---
title: Counting the items in a list with the use of a dictionary
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use a dictionary comprehension and iterate over the list, using each item as a key and incrementing its value by one each time it appears.
---

**Contents**

[TOC]

## Introduction
Dictionary is an essential data structure in Python that is used to store and organize data in key-value pairs. In Python, we can use a dictionary to count the items in a list. This approach offers a simple and efficient way to count the number of occurrences of each item in a list.

## Using a Dictionary to count items in a List
To count the items in a Python list using a dictionary, we will follow the steps listed below.

1. We start by creating an empty dictionary that will be used to store the results of counting the items in the list.
2. We loop through the items in the list.
3. For each item, we check if it exists in the dictionary as a key.
4. If it exists, we increment the value associated with the key in the dictionary.
5. If it does not exist, we add the item as a new key with a value of 1.
6. After looping through all items in the list, the dictionary contains the count of each item in the list.

Here's a code snippet that illustrates this:

```
my_list = ['apple', 'banana', 'apple', 'orange', 'banana', 'apple']
count_dict = {}

for item in my_list:
    if item in count_dict:
        count_dict[item] += 1
    else:
        count_dict[item] = 1

print(count_dict)
```

This code will output the following dictionary:

```
{'apple': 3, 'banana': 2, 'orange': 1}
```

## Conclusion
Using a dictionary to count the items in a list in Python is a simple and efficient approach. By storing the results in a dictionary, we can easily access the count of each item using its key.
