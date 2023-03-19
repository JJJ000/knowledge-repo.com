---
title: Is there a sorted list in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Yes, Python has a built-in sorted() function that can sort lists.
---

**Contents**

[TOC]

Python has a built-in sorted() function that can sort any iterable. However, it does not have a specific data structure called a "sorted list". 

#### 1. Using the built-in `sorted()` function:

Python provides a built-in `sorted()` function, which returns a new list that is sorted.

```python
my_list = [5, 1, 3, 2, 4]
sorted_list = sorted(my_list)
print(sorted_list)   # Output: [1, 2, 3, 4, 5]
```

#### 2. Using the `list.sort()` method:

Python lists also have a `sort()` method that can sort a list in-place. This means that the original list is modified instead of returning a new sorted list.

```python
my_list = [5, 1, 3, 2, 4]
my_list.sort()
print(my_list)    # Output: [1, 2, 3, 4, 5]
```

#### 3. Using third-party libraries:

Python has third-party libraries, such as NumPy and Pandas, that provide specialized data structures like sorted arrays and data frames that can be used to mimic sorted lists. 

#### 4. Creating a sorted list from scratch:

In Python, there is no specific data structure called a "sorted list". However, we can create a class and implement the methods ourselves.

```python
class SortedList:
    def __init__(self):
        self.data = []
    
    def add(self, item):
        index = 0
        while index < len(self.data) and self.data[index] < item:   # find the correct index
            index += 1
        self.data.insert(index, item)   # insert the item at the correct index
    
    def __str__(self):
        return str(self.data)
```

Now, we can create an instance of the `SortedList` class and add items to it.

```python
my_list = SortedList()
my_list.add(5)
my_list.add(1)
my_list.add(3)
my_list.add(2)
my_list.add(4)
print(my_list)    # Output: [1, 2, 3, 4, 5]
```
