---
title: What is the syntax for assigning a default value if a variable is set to none in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Yes, the `or` operator can be used to return a default value if the value is None.
---

**Contents**

[TOC]

**Option 1:**

Using the Ternary Operator
--------------------------------
The ternary operator `x if c else y` provides a shorthand way to return a default value if `None` is encountered. The syntax is simple:

```
result = x if c else y
```

This statement evaluates to `x` if the condition (`c`) is `True` and evaluates to `y` if the condition is `False`. If `None` is encountered, it can be used to return a default value:

```
result = x if c is not None else y
```

**Option 2:**

Using the `or` Operator
------------------------
The `or` operator can also be used to return a default value if `None` is encountered. The syntax is as follows:

```
result = x or y
```

This statement evaluates to `x` if `x` is `True` and evaluates to `y` if `x` is `False`. Therefore, it can be used to return a default value if `None` is encountered:

```
result = x or y if x is not None else y
```
