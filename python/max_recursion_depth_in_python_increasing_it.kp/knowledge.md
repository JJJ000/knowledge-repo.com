---
title: What is the deepest level of recursion that can be reached in python, and how can it be increased?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The maximum recursion depth in Python is typically 1000, but it can be increased by setting the sys.setrecursionlimit() function to a higher number.
---

**Contents**

[TOC]

## Maximum Recursion Depth

The default maximum recursion depth in Python is 1000. This means that the maximum number of nested function calls that can be made before reaching the maximum recursion depth is 1000.

## How to Increase

The maximum recursion depth can be increased by using the `sys.setrecursionlimit()` method. This method takes an integer argument which is the new maximum recursion depth. For example, to increase the maximum recursion depth to 2000, the following code can be used:

```
import sys
sys.setrecursionlimit(2000)
```

## Considerations

It is important to note that increasing the maximum recursion depth may have an impact on the performance of the program. A higher maximum recursion depth may lead to increased memory usage and slower execution. Therefore, it is important to consider the trade-offs before increasing the maximum recursion depth.
