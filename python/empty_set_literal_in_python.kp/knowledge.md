---
title: What is an empty set?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: An empty set in Python is denoted by set(), or {}.
---

**Contents**

[TOC]

# Empty Set Literal
A set is a collection of unique elements. An empty set can be created in Python with the set literal `set()`.

## Usage
The empty set literal can be used to create an empty set, which can then be populated with elements.

```python
# Create an empty set
empty_set = set()

# Add elements to the set
empty_set.add(1)
empty_set.add(2)
empty_set.add(3)

# Print the set
print(empty_set)
# Output: {1, 2, 3}
```

## Empty Set vs Empty Dictionary
It is important to note that an empty set is not the same as an empty dictionary. An empty dictionary is created with the literal `{}`.

```python
# Create an empty dictionary
empty_dict = {}

# Print the dictionary
print(empty_dict)
# Output: {}
```
