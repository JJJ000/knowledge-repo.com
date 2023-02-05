---
title: Python's list of zeros
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: A list of zeros in Python can be created using the syntax `[0] * n`, where `n` is the desired length of the list.
---

**Contents**

[TOC]

### Option 1:

**Using List Comprehension:**

```python
zeros_list = [0 for i in range(n)]
```

### Option 2:

**Using Numpy:**

```python
import numpy as np

zeros_list = np.zeros(n)
```

### Option 3:

**Using List:**

```python
zeros_list = [0] * n
```

### Option 4:

**Using For Loop:**

```python
zeros_list = []
for i in range(n):
    zeros_list.append(0)
```
