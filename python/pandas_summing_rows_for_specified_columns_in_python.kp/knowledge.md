---
title: How to calculate the total of dataframe rows for specified columns in pandas?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use the `sum()` method with `axis=1` parameter to calculate the sum of rows for given columns in Pandas DataFrame.
---

**Contents**

[TOC]

## 1. Introduction

Pandas is a popular data manipulation and analysis library for Python. It provides functionality to work with tabular data, such as rows and columns, and perform operations on them. One of the common tasks when working with data is to sum rows for certain columns. This can be done using various pandas functions, and we will look at some of them in this tutorial.


## 2. Summing rows with the `sum` function

The `sum` function in pandas can be used to sum rows of a DataFrame along a certain axis. By default, it sums columns (axis=0), but we can specify axis=1 to sum rows. Here's an example:

```python
import pandas as pd

df = pd.DataFrame({
    'A': [1, 2, 3],
    'B': [4, 5, 6],
    'C': [7, 8, 9]
})

# sum rows for columns A and B
total = df[['A', 'B']].sum(axis=1)

print(total)
```

Output:
```
0     5
1     7
2     9
dtype: int64
```

In this example, we create a DataFrame with three columns: A, B, and C, and three rows of data. We select the columns A and B using the double square bracket notation (this returns a new DataFrame), and call the `sum` function with axis=1 to sum the rows. The resulting Series contains the sum for each row.


## 3. Summing rows with a lambda function

Another way to sum rows of a DataFrame is to use a lambda function along with the `apply` function. This allows us to specify a custom operation for each row. Here's an example:

```python
import pandas as pd

df = pd.DataFrame({
    'A': [1, 2, 3],
    'B': [4, 5, 6],
    'C': [7, 8, 9]
})

# sum rows for columns A and B using a lambda function
total = df.apply(lambda row: row['A'] + row['B'], axis=1)

print(total)
```

Output:
```
0     5
1     7
2     9
dtype: int64
```

In this example, we create a DataFrame similar to the previous example. We then call the `apply` function with a lambda function that sums columns A and B for each row. The resulting Series contains the sum for each row.


## 4. Conclusion

Summing rows for certain columns in a DataFrame is a common and useful operation in data analysis. Pandas provides various functions for this, including the `sum` function and the `apply` function with a lambda function. By knowing how to use these functions, you can easily sum rows for given columns in Python with pandas.
