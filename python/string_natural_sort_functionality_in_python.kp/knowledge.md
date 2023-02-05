---
title: Is there a native function for string sorting in a natural order?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: No, there is not a built-in function for string natural sort in Python.
---

**Contents**

[TOC]

#No

##Explanation

Unfortunately, Python does not have a built-in function for string natural sort. Natural sort is a sorting algorithm that compares strings in a natural way, taking into account the fact that numbers embedded in strings should be sorted in numerical order.

##Alternative Solutions

There are a few third-party libraries that can be used to achieve natural sorting in Python. The most popular are `natsort` and `natsorted`. Both of these libraries provide functions that can be used to sort strings in a natural way.

##Example

For example, using `natsort` you can sort a list of strings like this:

```
import natsort

strings = ["file1.txt", "file2.txt", "file10.txt"]

sorted_strings = natsort.natsorted(strings)

print(sorted_strings)
# Output: ['file1.txt', 'file2.txt', 'file10.txt']
```
