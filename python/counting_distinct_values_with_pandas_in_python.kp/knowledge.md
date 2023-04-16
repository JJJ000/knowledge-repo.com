---
title: Pandas 'nunique()'
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The closest equivalent to Pandas` count(distinct) in Python is to use the set() function to convert the list to a set and then use len() to count the number of unique elements in the set.
---

**Contents**

[TOC]

**Option 1: Using Set**

```python
unique_values = set(list_of_values)
count = len(unique_values)
```

**Option 2: Using Counter**

```python
from collections import Counter

unique_values = Counter(list_of_values)
count = len(unique_values)
```

**Option 3: Using Numpy**

```python
import numpy as np

unique_values = np.unique(list_of_values)
count = len(unique_values)
```

**Option 4: Using Pandas**

```python
import pandas as pd

unique_values = pd.unique(list_of_values)
count = len(unique_values)
```
