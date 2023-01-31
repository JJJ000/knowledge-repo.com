---
title: What is the procedure for waiting for a key to be pressed?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the input() or raw\_input() functions to wait for a pressed key.
---

**Contents**

[TOC]

# Using the msvcrt Module
The msvcrt module can be used to wait for a pressed key in Python. This module provides access to the C Runtime Library functions.

## Steps
1. Import the msvcrt module
2. Use the msvcrt.getch() function to wait for a pressed key
3. Use the ord() function to get the ASCII code of the pressed key

## Example
```python
import msvcrt

key = msvcrt.getch()
key_code = ord(key)

print(key_code)
```
