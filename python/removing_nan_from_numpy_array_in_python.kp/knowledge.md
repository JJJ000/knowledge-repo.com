---
title: What is the best way to eliminate nan values from a numpy array?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the NumPy function np.nan\_to\_num() to replace NaN values with zeros.
---

**Contents**

[TOC]

**Section 1: Importing Necessary Libraries**

```python
import numpy as np
```

**Section 2: Removing NaN Values**

```python
# Remove NaN values from an array
arr = np.array([1, 2, np.nan, 3, 4, np.nan])
arr = arr[~np.isnan(arr)]
```

**Section 3: Verifying Results**

```python
# Verify results
print(arr)
# Output: [1. 2. 3. 4.]
```

**Section 4: Replacing NaN Values**

```python
# Replace NaN values with a specific value
arr = np.array([1, 2, np.nan, 3, 4, np.nan])
arr = np.where(np.isnan(arr), 0, arr)
```
