---
title: Replace nan values in pandas with an empty string
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Pandas DataFrame`s replace() method can be used to replace NaN values with an empty string.
---

**Contents**

[TOC]

#Solution 1
##Using Pandas fillna()
Pandas fillna() function can be used to replace NaN values with empty strings. This function can take an argument of a scalar value, dict, Series, or DataFrame to replace the NaN values.

Example:

```
import pandas as pd

#Create a DataFrame
df = pd.DataFrame({'A':[1,2,3,4], 'B':[5,6,7,8], 'C':[9,10,11,None]})

#Replace NaN values with empty strings
df.fillna('')
```

#Solution 2
##Using Numpy where()
Numpy where() function can also be used to replace NaN values with empty strings. This function takes three arguments: condition, x and y. The condition argument is a boolean array which is used to select the elements from x and y which satisfy the condition.

Example:

```
import numpy as np

#Create a DataFrame
df = pd.DataFrame({'A':[1,2,3,4], 'B':[5,6,7,8], 'C':[9,10,11,None]})

#Replace NaN values with empty strings
df.where(pd.notnull(df), np.where(pd.isnull(df), '', df), axis=1)
```
