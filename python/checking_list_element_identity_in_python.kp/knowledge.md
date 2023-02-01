---
title: See if all items in the list are the same
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Yes, you can use the all() function to check if all elements in a list are identical.
---

**Contents**

[TOC]

**Solution 1: Using a Set**

```python
def is_identical(lst):
    return len(set(lst)) <= 1
```

**Solution 2: Using a Counter**

```python
from collections import Counter

def is_identical(lst):
    return len(Counter(lst).items()) == 1
```

**Solution 3: Using All()**

```python
def is_identical(lst):
    return all(x == lst[0] for x in lst)
```

**Solution 4: Using Numpy**

```python
import numpy as np

def is_identical(lst):
    return np.all(lst == lst[0])
```
