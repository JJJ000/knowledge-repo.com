---
title: What is the procedure for determining if a string is contained within a list of strings?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: Use the `in` operator to check if the string is a substring of any items in the list of strings.
---

**Contents**

[TOC]

## Using `in` Operator

The simplest way to check if a string is a substring of items in a list of strings is to use the `in` operator. This operator returns `True` if the substring is found in any of the strings in the list, and `False` otherwise.

For example,

```
list_of_strings = ['abc', 'def', 'ghi']
substring = 'de'

if substring in list_of_strings:
    print('Substring found')
else:
    print('Substring not found')
```

The above code will print `Substring found`.

## Using `any()` Function

Another way to check if a string is a substring of items in a list of strings is to use the `any()` function. This function takes a predicate (function that returns `True` or `False`) as an argument and returns `True` if the predicate returns `True` for any of the items in the list.

For example,

```
list_of_strings = ['abc', 'def', 'ghi']
substring = 'de'

def check_substring(string):
    return substring in string

if any(check_substring, list_of_strings):
    print('Substring found')
else:
    print('Substring not found')
```

The above code will print `Substring found`.

## Using List Comprehension

A third way to check if a string is a substring of items in a list of strings is to use list comprehension. This allows us to create a new list containing only the strings that contain the substring.

For example,

```
list_of_strings = ['abc', 'def', 'ghi']
substring = 'de'

filtered_list = [string for string in list_of_strings if substring in string]

if len(filtered_list) > 0:
    print('Substring found')
else:
    print('Substring not found')
```

The above code will print `Substring found`.

## Using `filter()` Function

A fourth way to check if a string is a substring of items in a list of strings is to use the `filter()` function. This function takes a predicate (function that returns `True` or `False`) as an argument and returns a list containing only the items in the list for which the predicate returns `True`.

For example,

```
list_of_strings = ['abc', 'def', 'ghi']
substring = 'de'

def check_substring(string):
    return substring in string

filtered_list = filter(check_substring, list_of_strings)

if len(filtered_list) > 0:
    print('Substring found')
else:
    print('Substring not found')
```

The above code will print `Substring found`.
