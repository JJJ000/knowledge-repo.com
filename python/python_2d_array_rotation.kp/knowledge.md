---
title: How to perform a 2d array rotation using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: To rotate a two-dimensional array in Python, we can use the numpy library`s rot90() method.
---

**Contents**

[TOC]

Section 1: Introduction

In Python, we can easily rotate a two-dimensional array using a few simple techniques. A two-dimensional array consists of multiple rows and columns, and we can rotate the array either clockwise or anti-clockwise.

Section 2: Rotating a two-dimensional array clockwise

To rotate a two-dimensional array clockwise, we can first transpose the array, which involves exchanging the rows and columns. After transposing, we can reverse the rows to obtain the desired rotation.

Here's an example of rotating a 3x3 array clockwise:

```
arr = [[1, 2, 3],
       [4, 5, 6],
       [7, 8, 9]]

# Transpose the array
for i in range(len(arr)):
    for j in range(i, len(arr)):
        arr[i][j], arr[j][i] = arr[j][i], arr[i][j]

# Reverse the rows
for i in range(len(arr)):
    arr[i] = arr[i][::-1]

```

After executing the above code, the `arr` array will be rotated clockwise by 90 degrees.

Section 3: Rotating a two-dimensional array anti-clockwise

To rotate a two-dimensional array anti-clockwise, we can perform the reverse steps of rotating clockwise. We can first reverse the rows and then transpose the array.

Here's an example of rotating a 3x3 array anti-clockwise:

```
arr = [[1, 2, 3],
       [4, 5, 6],
       [7, 8, 9]]

# Reverse the rows
for i in range(len(arr)):
    arr[i] = arr[i][::-1]

# Transpose the array
for i in range(len(arr)):
    for j in range(i, len(arr)):
        arr[i][j], arr[j][i] = arr[j][i], arr[i][j]
```

After executing the above code, the `arr` array will be rotated anti-clockwise by 90 degrees.

Section 4: Conclusion

In this article, we learned how we can easily rotate a two-dimensional array in Python. We looked at two different methods - rotating clockwise and anti-clockwise - and saw how we can implement them using simple techniques like transposing and reversing rows.
