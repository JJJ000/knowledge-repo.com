---
title: What are the benefits of using __slots__?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: \_\_slots\_\_ allows for the optimization of memory usage in Python by limiting the attributes that can be added to an object.
---

**Contents**

[TOC]

## What are __slots__?

__slots__ are a way of limiting the attributes that can be added to an object in Python. They are used to reduce the memory usage of an object by preventing the dynamic creation of attributes.

## How do __slots__ work?

When an object is created with __slots__, the attributes that can be set on the object are limited to those specified in the __slots__ declaration. This prevents the dynamic creation of attributes, which can be memory intensive.

## Benefits of __slots__

Using __slots__ can reduce the memory usage of an object by preventing the dynamic creation of attributes. This can be particularly useful in situations where memory usage is a concern, such as in embedded systems or when dealing with large datasets.

## Drawbacks of __slots__

Using __slots__ can make it difficult to add new attributes to an object, as they must be specified in the __slots__ declaration. Additionally, __slots__ are not inherited, so any subclasses of an object with __slots__ will not be able to access the attributes specified in the __slots__ declaration.
