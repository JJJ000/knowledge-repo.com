---
title: Transform a numpy array into a Python list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the tolist() method to convert a NumPy array to a Python list.
---

**Contents**

[TOC]

#### Section 1: Import NumPy Library

```python
import numpy as np
```

#### Section 2: Create NumPy Array

```python
numpy_arr = np.array([1, 2, 3, 4, 5])
```

#### Section 3: Convert NumPy Array to Python List

```python
python_list = numpy_arr.tolist()
```

#### Section 4: Print Python List

```python
print(python_list)
```

Output: [1, 2, 3, 4, 5]
