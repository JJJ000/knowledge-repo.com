---
title: What is a 'named tuple' in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: Named tuples are a type of object that allows you to access elements using both numerical indices and string labels.
---

**Contents**

[TOC]

## Definition
Named tuples are a type of object in Python that are similar to tuples, but with named fields instead of numerical indexes. They are immutable, meaning they cannot be changed once created.

## Usage
Named tuples are useful for organizing data in a more meaningful way. For example, instead of a regular tuple like (1, 2, 3), you could have a named tuple like (name="Bob", age=25, occupation="Engineer"). This makes it easier to understand what each value represents.

## Benefits
Named tuples provide a more readable and maintainable way to store data. They are also more efficient than dictionaries, since they use less memory and are faster to access. Additionally, they are immutable, so once created, they cannot be modified.

## Limitations
Named tuples cannot contain duplicate field names, and they cannot be changed once created. Additionally, they are not as flexible as dictionaries, since they cannot contain different types of data.
