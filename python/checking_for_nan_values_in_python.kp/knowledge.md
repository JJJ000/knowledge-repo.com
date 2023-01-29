---
title: What is the best way to identify nan values?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can check for NaN values in Python using the pandas.isnull() or numpy.isnan() functions.
---

**Contents**

[TOC]

**Using the isnan() Function**

The `isnan()` function is a built-in function in Python that allows you to check for NaN values. It is a part of the math module and can be used as follows:

```python
import math

x = math.nan

if math.isnan(x):
    print("x is NaN")
```

**Using the isnull() Function**

The `isnull()` function is a built-in function in Python that allows you to check for NaN values. It is a part of the pandas module and can be used as follows:

```python
import pandas as pd

x = pd.NaT

if pd.isnull(x):
    print("x is NaN")
```

**Using the == Operator**

The `==` operator can also be used to check for NaN values in Python. This method is not as reliable as the `isnan()` and `isnull()` functions, but it can be used as follows:

```python
x = float('nan')

if x == float('nan'):
    print("x is NaN")
```

**Using the isna() Method**

The `isna()` method is a built-in method in Python that allows you to check for NaN values. It is a part of the pandas module and can be used as follows:

```python
import pandas as pd

x = pd.NaT

if x.isna():
    print("x is NaN")
```
