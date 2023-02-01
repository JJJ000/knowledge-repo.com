---
title: What are the differences between a list and a tuple, and when should each be used?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Tuples are immutable and should be used when the data is not expected to change, while lists are mutable and should be used when the data is expected to change.
---

**Contents**

[TOC]

### Usage

A list is a collection of objects that are ordered and mutable. Lists are typically used when the order of elements is important and when elements need to be changed. Tuples are also collections of objects, but they are immutable and the order of elements is important. Tuples are typically used when the order of elements is important and when elements should not be changed.

### Creation

Lists are created by enclosing elements in square brackets and separating them with commas. Tuples are created by enclosing elements in parentheses and separating them with commas.

### Accessing Elements

Lists and tuples can be accessed by indexing. To access an element in a list, use square brackets and the index of the element. To access an element in a tuple, use parentheses and the index of the element.

### Modifying Elements

Lists can be modified by adding, removing, and replacing elements. Tuples cannot be modified; any attempt to modify a tuple will result in an error.
