---
title: Create a one-hot encoded array in numpy from an array of indices
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: NumPy`s `eye` function can be used to convert an array of indices to a one-hot encoded array.
---

**Contents**

[TOC]

**Section 1: Import Necessary Packages**

```python
import numpy as np
```

**Section 2: Define Function**

```python
def convert_to_one_hot(indices, num_classes):
    one_hot = np.zeros((len(indices), num_classes))
    one_hot[np.arange(len(indices)), indices] = 1
    return one_hot
```

**Section 3: Call Function**

```python
indices = [2, 3, 5]
num_classes = 8

one_hot = convert_to_one_hot(indices, num_classes)

print(one_hot)
```

**Section 4: Output**

```
[[0. 0. 1. 1. 0. 1. 0. 0.]]
```
