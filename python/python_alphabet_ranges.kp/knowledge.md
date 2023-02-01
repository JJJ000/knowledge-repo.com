---
title: Creating a sequence of letters using the Python alphabet range function
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The range of the alphabet in Python is from `a` to `z`.
---

**Contents**

[TOC]

#### Range Function
The range() function in Python returns a sequence of numbers, starting from 0 by default, and incrementing by 1 (by default), and stops before a specified number.

#### Syntax
range(start, stop, step)

#### Parameters
- start: Starting number of the sequence.
- stop: Generate numbers up to, but not including this number.
- step: Difference between each number in the sequence.

#### Example
The following example generates a sequence of numbers from 0 to 9:

```python
for x in range(10):
  print(x)
```
Output:
```
0
1
2
3
4
5
6
7
8
9
```
