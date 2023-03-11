---
title: Which one is preferable in urls.py for django 2.0 path() or url()?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: It is better to use path() as it is simpler and more readable compared to url().
---

**Contents**

[TOC]

Introduction
------------

When working with URLs in Django, there are two functions that can be used to define URL patterns in `urls.py`: `path()` and `url()`. In this article, we will explore the differences between the two functions and when it is better to use one over the other.

Overview of path() and url()
-----------------------------

Both `path()` and `url()` are functions that are defined in the `django.urls` module in Django. They are used to create URL patterns that can be matched to incoming requests to your Django application. 

`path()` was introduced in Django 2.0 as a more modern and Pythonic way of defining URL patterns. It uses the syntax of matching patterns to functions that are more like Python's built-in regular expressions. `url()` is the older version of the function that was available in earlier versions of Django.

Differences between path() and url()
------------------------------------

There are a few key differences between `path()` and `url()` that are important to consider when deciding which one to use.

### Regular Expressions

`path()` uses a simpler syntax than `url()` for matching regular expressions. In `path()`, the syntax used for matching patterns is similar to regular expressions in Python, but somewhat simplified.

On the other hand, `url()` requires that you use the full regular expression syntax, which can be more cumbersome to work with.

### Namespacing

`path()` allows you to create namespaces for your URL patterns, which can be useful for organizing your code and preventing naming conflicts. This is not possible with `url()`.

### Reverse URL Lookup

`path()` makes it easier to do reverse URL lookups in your templates by using a simpler syntax. With `path()`, you can define a name for each URL pattern and then use the name in your template code to generate links. This makes it easier to maintain your code.

On the other hand, `url()` requires that you use a more complicated syntax to reverse URL lookups in your templates.

### Required Arguments

`path()` allows you to define required arguments for your URL patterns using angle brackets (`<` and `>`). These arguments are then passed to the view function defined for the URL pattern.

With `url()`, you can also define required arguments, but the syntax is more complicated and uses regular expressions.

Conclusion
----------

In general, it is better to use `path()` for defining URL patterns in Django 2.0 and later versions of Django. `path()` has a simpler syntax for regular expressions, allows for namespacing, and makes it easier to do reverse URL lookups in templates. However, if you are working with an older version of Django that does not support `path()`, using `url()` is still a viable option.
