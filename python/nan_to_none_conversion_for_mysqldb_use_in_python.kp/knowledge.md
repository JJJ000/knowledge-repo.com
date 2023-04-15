---
title: To utilize with mysqldb, switching out nan from pandas or numpy with none
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: You can use the pandas.DataFrame.where() method with a condition to replace Nan with None for MySQLDB compatability in Python.
---

**Contents**

[TOC]

Introduction

In Python, the NaN (Not a Number) value is used to represent invalid or missing data in numerical arrays. Pandas and Numpy libraries use NaNs extensively to facilitate data analysis and manipulation. However, when working with databases like MySQL, NaNs can pose a challenge since they are not compatible with databases' NULL values. One solution is to convert NaNs to Python's None object, which can be mapped to NULL in MySQL. In this article, we will discuss how to replace NaNs with None in Pandas or Numpy arrays to facilitate working with MySQL in Python.

Using Pandas to Replace NaNs with None

Pandas is a widely used library for handling data in Python. It provides tools for data analysis, manipulation, and visualization, and it is widely used in scientific computing and data-intensive applications. To replace NaNs with None in a Pandas dataframe, we can use the .fillna() method. 

Here's an example:

```
import pandas as pd

# create a dataframe with NaN values
df = pd.DataFrame({
    'col1': [1.0, 2.0, 3.0, 4.0, float('nan')],
    'col2': ['A', 'B', 'C', 'D', 'E']
})

# Replace NaNs with None
df.fillna(value=None, inplace=True)

print(df)
```

In this code, we create a Pandas dataframe with a column containing NaN values. We then use the .fillna() method to replace NaNs with None. The value=None argument tells Pandas to replace NaNs with None. The inplace=True argument specifies that the changes should be made to the original dataframe, rather than creating a new one. 

Using Numpy to Replace NaNs with None

Like Pandas, Numpy also provides tools for working with numerical arrays in Python. To replace NaNs with None in a Numpy array, we can use the .astype() method. 

Here's an example:

```
import numpy as np

# create a numpy array with NaN values
arr = np.array([1.0, 2.0, 3.0, 4.0, np.nan])

# replace NaNs with None
arr = arr.astype(object)
arr[np.isnan(arr)] = None

print(arr)
```

In this code, we create a Numpy array with NaN values. We then change the data type of the array to 'object' using .astype(). This is necessary because NaNs are not supported in numerical arrays, but they are supported in object arrays. We then use np.isnan() to identify the NaN values in the array and replace them with None. Finally, we print the modified array to verify that NaNs have been replaced.

Conclusion

In this article, we discussed how to replace NaNs with None in Pandas or Numpy arrays to facilitate working with MySQL in Python. We demonstrated how to use the .fillna() method in Pandas and the .astype() method in Numpy to replace NaNs with None. These techniques can be useful in a variety of applications where NaNs are incompatible with other systems that require NULL values.
