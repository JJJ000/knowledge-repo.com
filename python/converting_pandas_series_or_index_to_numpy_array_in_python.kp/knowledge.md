---
title: What is the process of transforming a pandas series or index to a numpy array?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: To convert a Pandas series or index to a NumPy array in Python, use the `.to\_numpy()` method.
---

**Contents**

[TOC]

## Convert Pandas Series to NumPy array

To convert a Pandas Series to a NumPy array, you can simply use the `values` attribute of the Pandas Series.

``` python
import pandas as pd
import numpy as np

# create a Pandas Series
s = pd.Series([1, 2, 3, 4, 5])

# convert the Pandas Series to a NumPy array
arr = s.values

print(arr)
```

Output:
```
[1 2 3 4 5]
```

## Convert Pandas Index to NumPy array

To convert a Pandas Index to a NumPy array, you can also use the `values` attribute of the Pandas Index.

``` python
import pandas as pd
import numpy as np

# create a Pandas Index
idx = pd.Index([1, 2, 3, 4, 5])

# convert the Pandas Index to a NumPy array
arr = idx.values

print(arr)
```
Output:
```
[1 2 3 4 5]
```

## Convert Pandas DataFrame column to NumPy array

To convert a Pandas DataFrame column to a NumPy array, you can use the `values` attribute of the DataFrame column.

``` python
import pandas as pd
import numpy as np

# create a Pandas DataFrame
df = pd.DataFrame({'A': [1, 2, 3, 4, 5], 'B': [6, 7, 8, 9, 10]})

# convert column 'A' of the DataFrame to a NumPy array
arr = df['A'].values

print(arr)
```

Output:
```
[1 2 3 4 5]
```

## Convert Pandas DataFrame to NumPy array

If you want to convert a whole Pandas DataFrame to a NumPy array, you can use the `values` attribute of the DataFrame.

``` python
import pandas as pd
import numpy as np

# create a Pandas DataFrame
df = pd.DataFrame({'A': [1, 2, 3, 4, 5], 'B': [6, 7, 8, 9, 10]})

# convert the DataFrame to a NumPy array
arr = df.values

print(arr)
```

Output:
```
[[ 1  6]
 [ 2  7]
 [ 3  8]
 [ 4  9]
 [ 5 10]]
```
