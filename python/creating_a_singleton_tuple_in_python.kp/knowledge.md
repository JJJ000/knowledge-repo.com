---
title: How can a tuple with only one element be created that behaves like a 'singleton'?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use a comma after the element, then enclose it in parenthesis.
---

**Contents**

[TOC]

## What is a "singleton" tuple?

A "singleton" tuple is a tuple that contains only one element. In Python, tuples are typically created by enclosing their elements in parentheses. However, if there is only one element in the tuple, it is not enough to simply use parentheses. You need to use a special syntax to create a "singleton" tuple.

## Using a comma

The most common way to create a "singleton" tuple is by using a comma after the only element. This is because Python considers a single element inside parentheses to be of that element's data type. By adding a comma after the element, Python recognizes it as a 1-element tuple. For example: 

```
t = ("apple",)  # This is a "singleton" tuple
```

## Using the tuple() function

Another way to create a "singleton" tuple is by using the `tuple()` function. This method can be used for any number of elements, including one. To create a "singleton" tuple with the `tuple()` function, simply pass a single element as a parameter, like this:

```
t = tuple(["apple"]) # This is a "singleton" tuple
```

## Using indexing

Finally, it's worth noting that a "singleton" tuple can also be created using indexing. If you have a list or other iterable with only one element, you can access that element and create a tuple at the same time using indexing. Here's an example:

```
l = ["apple"]
t = (l[0],) # This is a "singleton" tuple
``` 

This method is not recommended, however, as it is less clear and requires additional code. 

In summary, the easiest and most widely used way to create a "singleton" tuple in Python is to use a comma after the single element.
