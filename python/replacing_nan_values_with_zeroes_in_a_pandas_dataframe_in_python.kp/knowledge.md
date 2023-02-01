---
title: What is the best way to replace nan values with zeroes in a column of a pandas dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the Dataframe.fillna() method and specify 0 as the value to replace NaN values with 0.
---

**Contents**

[TOC]

### Section 1: Import Necessary Libraries

In order to replace NaN values by zeroes in a column of a Pandas Dataframe, we need to first import the necessary libraries. 

```python
import pandas as pd
```

### Section 2: Create Dataframe

We can create a sample dataframe with NaN values in one of its columns. 

```python
df = pd.DataFrame({'A':[1,2,3,4,5], 'B':[6,7,8,9,np.nan]})
```

### Section 3: Replace NaN Values

We can use the `fillna()` method to replace the NaN values in the column with zeroes. 

```python
df['B'] = df['B'].fillna(0)
```

### Section 4: Result

The resulting dataframe will look like this: 

```python
   A    B
0  1  6.0
1  2  7.0
2  3  8.0
3  4  9.0
4  5  0.0
```
