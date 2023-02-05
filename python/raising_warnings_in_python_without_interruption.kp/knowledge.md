---
title: Issue a warning in Python without halting execution
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can use the `warnings` module to raise a warning without interrupting the program.
---

**Contents**

[TOC]

# Using Warnings Module

The Warnings module in Python provides a way to issue warnings to the user of your program. It allows you to raise a warning without interrupting the program.

## Warning Types

Warnings are categorized into two types:

* **UserWarning**: These warnings are generated when a user action or configuration may have unexpected results.

* **RuntimeWarning**: These warnings are generated when a program may be behaving in an unexpected way.

## Using Warnings

To raise a warning without interrupting the program, use the `warnings.warn()` function. This function takes two arguments: a warning message and the warning type.

For example, to raise a UserWarning, you can use the following code:

```python
import warnings
warnings.warn("This is a user warning!", UserWarning)
```

## Suppressing Warnings

If you want to suppress a warning, you can use the `warnings.filterwarnings()` function. This function takes two arguments: a warning message and the warning type.

For example, to suppress a UserWarning, you can use the following code:

```python
import warnings
warnings.filterwarnings("ignore", "This is a user warning!", UserWarning)
```
