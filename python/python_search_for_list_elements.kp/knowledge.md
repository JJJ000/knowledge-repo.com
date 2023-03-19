---
title: Searching for an item within a list using python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To find an element in a list in Python, use the index method or the `in` operator.
---

**Contents**

[TOC]

## Introduction

In Python, finding an element in a list is a very common task. Whether we want to check if an element exists in the list, or we want to know its index or count, Python provides several built-in methods to make it easy for us. In this article, we will go through some of these methods and learn how to find an element in a list.

## Using the `in` operator

One of the easiest ways to check if an element exists in a list is to use the `in` operator. The `in` operator returns `True` if the element is present in the list and `False` otherwise. Here is an example:

``` python
>>> my_list = [1, 2, 3, 4, 5]
>>> 3 in my_list
True
>>> 6 in my_list
False
```

Here, we have a list `my_list` containing five elements. We use the `in` operator to check if the element `3` exists in the list (which it does), and if the element `6` exists in the list (which it does not).

It is important to note that the `in` operator is case-sensitive. If the list contains string elements, we need to make sure that the case of the element we are checking matches the case of the element in the list. For example:

``` python
>>> my_list = ['apple', 'banana', 'pear', 'orange']
>>> 'banana' in my_list
True
>>> 'Banana' in my_list
False
```

Here, we have a list `my_list` containing four string elements. We use the `in` operator to check if the element `banana` (in lowercase) exists in the list (which it does), and if the element `Banana` (in uppercase) exists in the list (which it does not).

## Using the `index()` method

If we want to find the index of an element in a list, we can use the `index()` method. The `index()` method takes an element as an argument and returns the index of the first occurrence of the element in the list. Here is an example:

``` python
>>> my_list = [1, 2, 3, 4, 5, 4]
>>> my_list.index(4)
3
```

Here, we have a list `my_list` containing six elements. We use the `index()` method to find the index of the first occurrence of the element `4` in the list, which is `3`.

If the element is not present in the list, the `index()` method raises a `ValueError`. To avoid this error, we can check if the element exists in the list using the `in` operator before calling the `index()` method.

## Using the `count()` method

If we want to know how many times an element appears in a list, we can use the `count()` method. The `count()` method takes an element as an argument and returns the number of times the element appears in the list. Here is an example:

``` python
>>> my_list = [1, 2, 3, 4, 5, 4]
>>> my_list.count(4)
2
```

Here, we have a list `my_list` containing six elements. We use the `count()` method to find how many times the element `4` appears in the list, which is `2`.

If the element is not present in the list, the `count()` method returns `0`.

## Conclusion

In this article, we have learned how to find an element in a list in Python. We have seen that we can use the `in` operator to check if an element exists in a list, the `index()` method to find the index of an element, and the `count()` method to find how many times an element appears in a list. These methods are very useful for working with lists in Python.
