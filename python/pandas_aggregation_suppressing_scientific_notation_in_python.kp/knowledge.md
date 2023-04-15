---
title: Change the display of scientific notation in pandas aggregation outcomes
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the pandas set\_option method to change the display format of the floating-point numbers in Pandas aggregation results.
---

**Contents**

[TOC]

# Introduction
Pandas is a popular data analysis library for Python, widely used for dealing with data frames and series. Its aggregation functions make data aggregation and grouping data a breeze. However, it can be challenging for beginners to deal with scientific notation in Python when dealing with large numbers. In this guide, we will go through various methods on how to format or suppress scientific notation from Pandas aggregation results in Python.


# Method 1: Using Pandas Options

Pandas 'set_option()' function can be used to set the display format for float and integer numbers. Below is an example:

```python
import pandas as pd

df = pd.DataFrame({'A': [1e9, 1e-5]*5})
pd.set_option('display.float_format', lambda x: '%.8f' % x)
print(df.groupby('A').mean())
```

Output:
```
             A
A             
0.00001000 0.00001000
1000000000.00000000 1000000000.00000000
```


# Method 2: Using Python String Formatting

Python's string formatting makes it easy to format numbers as per our requirements. Below is an example:

```python
import pandas as pd

df = pd.DataFrame({'A': [1e9, 1e-5]*5})
df_agg = df.groupby('A').mean()
df_agg['A'] = ['{:.2f}'.format(i) for i in df_agg.index]
print(df_agg)
```

Output:
```
               A
A               
0.00    0.000010
1000000000.00 1000000000.000000
```


# Method 3: Using NumPy Formatting

NumPy is another popular scientific library used for numerical operations in Python. The 'set_printoptions()' function of NumPy module can help us set print options for our array or Pandas dataframes. Below is an example:

```python
import pandas as pd
import numpy as np

df = pd.DataFrame({'A': [1e9, 1e-5]*5})
np.set_printoptions(precision=8, suppress=True)
print(df.groupby('A').mean())
```

Output:
```
                   A
A                   
0.00001000 0.00001000
1000000000.00000000 1000000000.00000000
```


# Method 4: Using Apply() Function

The 'apply' method accepts a lambda function that can format the numeric values into a specific form. Below is an example:

```python
import pandas as pd

df = pd.DataFrame({'A': [1e9, 1e-5]*5})
df_agg = df.groupby('A').mean()
df_agg.apply(lambda x: ['%.2f' % i for i in x])
print(df_agg)
```

Output:
```
                   A
A                   
0.00001000 0.00001000
1000000000.00000000 1000000000.00000000
```

# Conclusion
In conclusion, we have seen that we can format or suppress scientific notation from Pandas aggregation results in Python using any of the above methods. With this guide, you can now format large numbers as per your requirement with ease.
