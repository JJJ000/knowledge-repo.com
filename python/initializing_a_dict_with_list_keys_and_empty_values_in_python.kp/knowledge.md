---
title: What is the syntax for creating a dictionary with keys from a list and empty values in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: dict.fromkeys(list, ``) can be used to initialize a dict with keys from a list and empty value in Python.
---

**Contents**

[TOC]

## 1. Using dict comprehension

The following code snippet can be used to initialize a dict with keys from a list and empty value in Python using dict comprehension:

```python
my_list = [1,2,3]
my_dict = {key: None for key in my_list}
```

## 2. Using dict.fromkeys()

The following code snippet can be used to initialize a dict with keys from a list and empty value in Python using dict.fromkeys():

```python
my_list = [1,2,3]
my_dict = dict.fromkeys(my_list, None)
```

## 3. Using for loop

The following code snippet can be used to initialize a dict with keys from a list and empty value in Python using for loop:

```python
my_list = [1,2,3]
my_dict = {}
for key in my_list:
    my_dict[key] = None
```

## 4. Using dict()

The following code snippet can be used to initialize a dict with keys from a list and empty value in Python using dict():

```python
my_list = [1,2,3]
my_dict = dict((key, None) for key in my_list)
```
