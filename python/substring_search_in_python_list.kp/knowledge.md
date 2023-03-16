---
title: Locating a portion of a string within a Python list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: Use the `in` keyword followed by the list to check if a substring is present in the list.
---

**Contents**

[TOC]

## Introduction

Python provides various ways to find a substring within a list. We can use loops, list comprehension, and built-in functions such as `in` and `index`.

## Using Loop

We can iterate over each element in the list and use the `in` operator to check whether the substring exists in the element. Here's the code:

```python
def find_substring(lst, substring):
    result = []
    for item in lst:
        if substring in item:
            result.append(item)
    return result
```

This function takes two arguments: `lst` is the list we want to search within, and `substring` is the string we want to search for. The function iterates over each item in the list and checks if the substring exists in that item. If it does, the item is added to the `result` list. Finally, the function returns the `result` list.

## Using List Comprehension

We can use list comprehension to achieve the same result as the previous section in a more concise way. Here's the code:

```python
def find_substring(lst, substring):
    return [item for item in lst if substring in item]
```

This function is nearly identical to the previous one, except that it uses list comprehension instead of a loop. The list comprehension builds a new list containing only the items that contain the substring, and this new list is immediately returned.

## Using index() method

Another method to find a substring within a list is to use the `index()` method. The `index()` method returns the index of the first occurrence of a substring in a string. Here's the code:

```python
def find_substring(lst, substring):
    result = []
    for item in lst:
        if item.find(substring) != -1:
            result.append(item)
    return result
```

This function takes two arguments: `lst` is the list we want to search within, and `substring` is the string we want to search for. The function iterates over each item in the list and checks if the substring exists in that item using the `find()` method. If it does, the item is added to the `result` list. Finally, the function returns the `result` list.

## Conclusion

In this tutorial, we learned different methods to find a substring within a list in Python. We can use loops, list comprehension, and built-in functions such as `in` and `index()`. Depending on our specific requirements, we can choose the most suitable method for our application.
