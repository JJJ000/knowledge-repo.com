---
title: Price of len() function
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The cost of the len() function in Python is a constant time operation, so it has a time complexity of O(1).
---

**Contents**

[TOC]

### Cost
The cost of the len() function in Python is free.

### Time Complexity
The time complexity of the len() function is O(1). This means that the time it takes to run the len() function is constant, regardless of the size of the passed argument.

### Memory Complexity
The memory complexity of the len() function is O(1). This means that the amount of memory used by the len() function is constant, regardless of the size of the passed argument.

### Examples
The following example shows the use of the len() function to get the length of a string:

```
string = "Hello World"

string_length = len(string)

print(string_length)
# Output: 11
```
