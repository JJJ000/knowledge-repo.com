---
title: What is the procedure for resetting the index in a pandas dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the DataFrame.reset\_index() method to reset the index of a pandas dataframe.
---

**Contents**

[TOC]

# Solution

## Section 1: Create a DataFrame

We can create a Pandas DataFrame by passing a NumPy array, a dictionary, a list, or a single value to the `pd.DataFrame()` constructor.

For example, we can create a DataFrame from a dictionary of lists:

```python
import pandas as pd

data = {
    'Name': ['John', 'Paul', 'George', 'Ringo'],
    'Age': [30, 31, 32, 33]
}

df = pd.DataFrame(data)
print(df)
```

Output:

```
    Name  Age
0   John   30
1   Paul   31
2  George   32
3  Ringo   33
```

## Section 2: Reset the Index

We can reset the index of a DataFrame using the `.reset_index()` method. This method will reset the index of the DataFrame to a range starting from 0.

For example, we can reset the index of the above DataFrame by calling the `.reset_index()` method:

```python
df = df.reset_index()
print(df)
```

Output:

```
   index   Name  Age
0      0   John   30
1      1   Paul   31
2      2  George   32
3      3  Ringo   33
```

## Section 3: Specify the Index

We can also specify the index when resetting the index of a DataFrame. This can be done by passing the desired index values to the `.reset_index()` method.

For example, we can reset the index of the above DataFrame to a range starting from 10 by passing a list of values to the `.reset_index()` method:

```python
df = df.reset_index(index=[10, 11, 12, 13])
print(df)
```

Output:

```
    index   Name  Age
10     10   John   30
11     11   Paul   31
12     12  George   32
13     13  Ringo   33
```

## Section 4: Drop the Old Index

By default, the `.reset_index()` method will create a new column which contains the old index values. We can prevent this by passing the `drop=True` argument to the `.reset_index()` method.

For example, we can reset the index of the above DataFrame and drop the old index column by passing the `drop=True` argument to the `.reset_index()` method:

```python
df = df.reset_index(drop=True)
print(df)
```

Output:

```
    Name  Age
0   John   30
1   Paul   31
2  George   32
3  Ringo   33
```
