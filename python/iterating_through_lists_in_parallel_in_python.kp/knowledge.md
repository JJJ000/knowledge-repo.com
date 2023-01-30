---
title: What is the best way to loop through two lists together?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: You can use the zip() function to iterate through two lists in parallel in Python.
---

**Contents**

[TOC]

**Using the zip() Function**

The zip() function is a built-in Python function that allows you to iterate through two lists in parallel. It takes two lists as arguments and returns an iterator of tuples, where the first item in each passed iterator is paired together, and then the second item in each passed iterator is paired together, etc.

For example, given two lists `list1` and `list2`, you can iterate through them in parallel using the zip() function as follows:

```python
for item1, item2 in zip(list1, list2):
    # Do something with item1 and item2
```

**Using the enumerate() Function**

The enumerate() function is another built-in Python function that allows you to iterate through two lists in parallel. It takes two lists as arguments and returns an iterator of tuples, where the first item in each tuple is the index of the item in the list, and the second item in each tuple is the item itself.

For example, given two lists `list1` and `list2`, you can iterate through them in parallel using the enumerate() function as follows:

```python
for index, (item1, item2) in enumerate(zip(list1, list2)):
    # Do something with item1, item2, and index
```

**Using a For Loop**

You can also iterate through two lists in parallel using a for loop. This approach is useful if you need to access the index of each item in the list.

For example, given two lists `list1` and `list2`, you can iterate through them in parallel using a for loop as follows:

```python
for index in range(len(list1)):
    item1 = list1[index]
    item2 = list2[index]
    # Do something with item1, item2, and index
```

**Using a While Loop**

You can also iterate through two lists in parallel using a while loop. This approach is useful if you need to access the index of each item in the list.

For example, given two lists `list1` and `list2`, you can iterate through them in parallel using a while loop as follows:

```python
index = 0
while index < len(list1):
    item1 = list1[index]
    item2 = list2[index]
    # Do something with item1, item2, and index
    index += 1
```
