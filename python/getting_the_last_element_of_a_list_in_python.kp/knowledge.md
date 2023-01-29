---
title: What is the method for accessing the final item in a list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: To get the last element of a list in Python, use the index -1.
---

**Contents**

[TOC]

**Using the [-1] Index**

The most straightforward way to access the last element of a list is to use the [-1] index. This index is used to access the element at the end of the list.

**Example**

```python
list = [1, 2, 3, 4]

last_element = list[-1]

print(last_element)
```

**Output**

```
4
```

**Using the len() Function**

Another way to access the last element of a list is to use the len() function. This function returns the length of the list, which can then be used to access the last element.

**Example**

```python
list = [1, 2, 3, 4]

last_element = list[len(list) - 1]

print(last_element)
```

**Output**

```
4
```
