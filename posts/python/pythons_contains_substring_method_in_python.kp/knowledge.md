---
title: Is there a "contains" substring method available in Python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-08 00:00:00
updated_at: 2023-01-08 00:00:00
tldr: Yes, Python has a built-in `in` operator to check if a substring is present in a string.
---

**Contents**

[TOC]

### Yes
Python does have a string 'contains' substring method. This method is called the `in` operator and it can be used to check if a substring is present in a string.

### How to Use
The `in` operator can be used to check if a substring is present in a string. The syntax is as follows:

```python
if substring in string:
    # Do something
```

### Examples
Here are some examples of how to use the `in` operator:

```python
# Check if 'Python' is present in the string
if 'Python' in 'I love programming with Python':
    print('Python is present in the string')

# Check if 'Java' is present in the string
if 'Java' in 'I love programming with Python':
    print('Java is present in the string')
```

The output of the above code would be:

```python
Python is present in the string
```
