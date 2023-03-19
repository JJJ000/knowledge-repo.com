---
title: Why is it that "list.sort ()" returns none instead of returning the sorted list itself?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The sort() method of list in Python does not return anything or returns None by default.
---

**Contents**

[TOC]

## Understanding the sort() method

In Python, the `sort()` method is used to sort a list in ascending or descending order. It modifies the original list and does not return a new list.

Consider the following example:

```
my_list = [3, 1, 4, 2, 5]
my_list.sort()
print(my_list)
```

The output of this code will be `[1, 2, 3, 4, 5]`, which is the sorted version of the original list `my_list`.

## The return value of sort()

The `sort()` method does not return anything. It does not have a `return` statement in its implementation.

Therefore, if you try to do something like `result = my_list.sort()`, `result` will be `None`, not the sorted list. This is because the `sort()` method modifies the original list in place and does not return anything.

## The return statement in return x.sort()

If you try to return the result of `list.sort()`, like `return my_list.sort()`, the result will still be `None`. This is because the `sort()` method does not have a return value.

The `return` statement in `return my_list.sort()` will execute the `sort()` method first, which modifies the original list `my_list`, and then return `None`.

## Solutions and alternatives

If you want to return the sorted list, you can simply use the `sorted()` function instead of the `sort()` method. The `sorted()` function returns a new sorted list and does not modify the original list.

```
my_list = [3, 1, 4, 2, 5]
result = sorted(my_list)
print(result)
```

The output of this code will be `[1, 2, 3, 4, 5]`, which is the sorted list returned by `sorted()`. 

Alternatively, you can sort the list first and then return it:

```
my_list = [3, 1, 4, 2, 5]
my_list.sort()
return my_list
```

This will modify the original list and return it.
