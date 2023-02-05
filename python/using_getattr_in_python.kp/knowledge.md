---
title: Could you explain to me in detail what getattr() is and how to utilize it?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: getattr() is a built-in function in Python that is used to access the attribute of an object, and can be used by passing in the object and the attribute name as arguments.
---

**Contents**

[TOC]

### Definition

getattr() is a built-in function in Python that returns the value of a specified attribute from an object. It takes three arguments: an object, a string (the attribute name), and an optional default value, which is returned if the attribute doesn't exist.

### Usage

getattr() is used to access the value of an attribute of an object. This can be useful when you don't know the name of the attribute ahead of time, or when you want to avoid writing a lot of if-else statements to check for the existence of an attribute.

For example, let's say you have a class called `Person` that has an attribute called `name`. You could use getattr() to get the value of the `name` attribute like this:

```python
person = Person()
name = getattr(person, 'name', 'John Doe')
```

If the `name` attribute exists, it will be returned. If it doesn't exist, the default value `John Doe` will be returned instead.

### Further Information

For more information about getattr(), see the [official Python documentation](https://docs.python.org/3/library/functions.html#getattr).
