---
title: What is the procedure for identifying the columns in a pandas dataframe that have nan values?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the `isna().any()` method on the dataframe to identify which columns contain any NaN value.
---

**Contents**

[TOC]

# Introduction
Pandas is a widely used data manipulation library in Python. A dataframe is the primary Pandas object used for data manipulation. Pandas provides many functions and methods to explore and manipulate data including finding which columns contain any NaN values.

# Step 1: Create a sample dataframe with NaN values
To demonstrate how to find which columns contain any NaN values in Pandas, we first create a sample dataframe.

```python
import pandas as pd
import numpy as np

data = {'A': [1, 2, np.nan, 4, 5],
        'B': [1, 2, 3, 4, 5],
        'C': [np.nan, 2, 3, 4, np.nan],
        'D': [1, 2, 3, 4, 5],
        }
df = pd.DataFrame(data)

print(df)
```

Output:

|     |   A |   B |   C |   D |
|----:|----:|----:|----:|----:|
|  0 |   1 |   1 | NaN |   1 |
|  1 |   2 |   2 |   2 |   2 |
|  2 | NaN |   3 |   3 |   3 |
|  3 |   4 |   4 |   4 |   4 |
|  4 |   5 |   5 | NaN |   5 |

The above code snippet creates a simple dataframe with NaN values in columns 'A' and 'C'.

# Step 2: Use isna() to find which columns have NaN values
The isna() function returns a boolean dataframe where each element is True if the corresponding element in the original dataframe is NaN; otherwise, False. We can use this to identify which columns contain NaN values.

```python
nan_cols = df.isna().any()

print(nan_cols)
```

Output:

|     |   A |     B |     C |   D |
|----:|----:|------:|------:|----:|
|   0 | 1   | False | True  | 1   |

The above output shows that columns 'A' and 'C' contain NaN values.

# Step 3: Extract the columns with NaN values into a list
We can extract the column names with NaN values into a list using the following code.

```python
nan_cols_list = nan_cols[nan_cols == True].index.tolist()

print(nan_cols_list)
```

Output:

['A', 'C']

# Conclusion
In this tutorial, we demonstrated how to find which columns contain any NaN values in a Pandas dataframe. This involves creating a sample dataframe with NaN values, using the isna() function to find which columns have NaN values, and then extracting the column names with NaN values into a list.
