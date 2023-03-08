---
title: What is the method to determine the position of an item in a list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the index() method to get the position of an item in a list in Python.
---

**Contents**

[TOC]

## Introduction

Knowing the position of an item in a list is important when working with list objects. Python provides several methods to get the position of an item in a list, ranging from simple methods like `index()` to more complex methods like using list comprehension. In this tutorial, we will look at some of the methods to get the position of an item in a list in Python.


## Using index() method

The `index()` method can be used to get the index of an item in a list. The method takes an argument, which is the value to be searched, and returns the index of the first occurrence of the value in the list.

```python
# Example
my_list = ['apple', 'banana', 'cherry', 'banana', 'apple']
position = my_list.index('banana')
print(position)
```

The above example will output `1`.

If the value is not present in the list, the method will raise a `ValueError`.


## Using enumerate() function

The `enumerate()` function is used to iterate over a list while keeping track of the index of the current item being processed. This function returns a tuple that contains the index of the current item and the value of the current item.

```python
# Example
my_list = ['apple', 'banana', 'cherry']
for index, value in enumerate(my_list):
    if value == 'banana':
        print(index)
```

The output of the above example will be `1`, which is the index position of the value 'banana'.



## Using list comprehension

List comprehension is a compact way of creating a list from another iterable while applying a filter condition. It can also be used to get the position of an item in a list. 

```python
# Example
my_list = ['apple', 'banana', 'cherry']
position = [i for i in range(len(my_list)) if my_list[i] == "banana"]
print(position)
```

The above example will output `[1]`.


## Conclusion

In conclusion, getting the position of an item in a list is a vital task when working with Python lists. Python provides multiple ways to find the position of an item in a list, with some of the most common being the `index()` method, using the `enumerate()` function, and list comprehension. Based on your use case, you can choose the method which suits you best.
