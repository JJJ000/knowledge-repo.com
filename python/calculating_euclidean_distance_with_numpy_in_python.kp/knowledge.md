---
title: What is the method for calculating the euclidean distance using numpy?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: The Euclidean distance can be calculated with NumPy in Python using the np.linalg.norm() function.
---

**Contents**

[TOC]

**Section 1: Importing NumPy**

The first step is to import the NumPy library. This is done by using the following command:

```python
import numpy as np
```

**Section 2: Calculating Euclidean Distance**

Once NumPy is imported, the Euclidean distance between two points can be calculated with the following command:

```python
dist = np.linalg.norm(point1 - point2)
```

Where `point1` and `point2` are the two points whose distance is to be calculated. 

**Section 3: Example**

For example, to calculate the Euclidean distance between the points (2, 3) and (4, 6), the following command can be used:

```python
dist = np.linalg.norm(np.array([2, 3]) - np.array([4, 6]))
```

**Section 4: Output**

The output of this command will be the Euclidean distance between the points, in this case 3.605551275463989.
