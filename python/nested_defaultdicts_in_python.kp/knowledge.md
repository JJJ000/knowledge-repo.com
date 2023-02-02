---
title: A nested defaultdict
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: A defaultdict of defaultdict is a dictionary that contains keys that point to other dictionaries, each of which can have its own default value.
---

**Contents**

[TOC]

## What is a defaultdict?
A defaultdict is a type of Python dictionary that provides a default value for a key that does not exist. It is a subclass of the built-in dict class. It takes a single argument which is used to provide the default value for a nonexistent key.

## How is it different from a regular dict?
Unlike a regular dict, a defaultdict will never raise a KeyError when the key does not exist. Instead, it will return the default value specified in the constructor. This makes it easier to use defaultdicts when the default value is known.

## What is a defaultdict of defaultdict?
A defaultdict of defaultdict is a type of dictionary that contains another defaultdict as its value. This allows for nested dictionaries to be easily created and accessed.

## How is it used?
A defaultdict of defaultdict is often used when dealing with nested data structures. It provides an easy way to access and manipulate the data without having to manually create the nested dictionaries. It can also be used to store complex data structures such as graphs or trees.
