---
title: Divide the list into more compact lists, by halving it
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use slicing to split a list in half in Python, such as myList[len(myList)//2] and myList[len(myList)//2].
---

**Contents**

[TOC]

## Introduction
Splitting a list into smaller lists is a common operation in Python. There are many ways to split a list into smaller lists, but one of the most common ways is to split the list in half. In this article, we will discuss two ways to split a list in half in Python.

## Using slicing
One way to split a list into halves is to use slicing. The basic idea is to find the middle index of the list and use it to slice the list into two halves. Here is an example:

```python
my_list = [1,2,3,4,5,6,7,8,9,10]
middle_index = len(my_list) // 2
first_half = my_list[:middle_index]
second_half = my_list[middle_index:]
```

In this code snippet, `my_list` is the list we want to split in half. `middle_index` is the index of the middle element in the list. We use integer division `//` to ensure that `middle_index` is an integer value. Then we use slicing to split the list into halves. `first_half` contains the elements from the beginning of the list up to the `middle_index`. `second_half` contains the elements from the `middle_index` to the end of the list.

## Using list comprehension
Another way to split a list in half is to use list comprehension. List comprehension allows us to create a new list based on an existing list. Here is an example of how to split a list in half using list comprehension:

```python
my_list = [1,2,3,4,5,6,7,8,9,10]
middle_index = len(my_list) // 2
first_half = [my_list[i] for i in range(middle_index)]
second_half = [my_list[i] for i in range(middle_index, len(my_list))]
```

In this code snippet, we use list comprehension to create new lists `first_half` and `second_half`. We loop through the indices of the original list using `range()`. For `first_half`, we loop through indices 0 to `middle_index - 1`. For `second_half`, we loop through indices `middle_index` to the end of the list. We use the square bracket notation to access the elements in the original list and add them to the new lists.


## Conclusion
Splitting a list into halves is a common operation in Python. In this article, we discussed two ways to split a list into halves: using slicing and using list comprehension. Both methods are easy to use and can be adapted to split a list into any number of smaller lists.
