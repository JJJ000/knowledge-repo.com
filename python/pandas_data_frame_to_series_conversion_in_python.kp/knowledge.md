---
title: Transform a data frame in pandas into a series
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: To convert a pandas dataframe to a series in Python, select the desired column from the dataframe using indexing.
---

**Contents**

[TOC]

## Section 1: Introduction
Pandas is a popular data manipulation library in Python. Pandas data frame is a two-dimensional size-mutable, tabular data structure with columns of potentially different types. It is designed for working with table-like or structured data. On the other hand, Pandas series is a one-dimensional size-mutable, array-like object that can hold any data type such as integers, strings, floating-point numbers, Python objects, etc. Sometimes, we may need to convert a Pandas data frame to series to perform some operations or to feed input to a function that expects a Pandas series as input. In this tutorial, we will see how to convert a Pandas data frame to series in Python.


## Section 2: Converting Pandas data frame to series
Pandas data frame has two main components: index and columns. When we convert it to series, we must specify which column or index we want to convert to a series. In Python, we can use the `iloc`, `loc`, or column indexing operator [] to select the desired column or index. Then, we can use `squeeze()` method on the selected column or index to convert it to a Pandas series. 

**Example:**

Consider the following data frame:

```
import pandas as pd

data = {'name': ['John', 'Smith', 'Paul'],
        'age': [30, 25, 40],
        'sex': ['M', 'M', 'M']}

df = pd.DataFrame(data)
print(df)
```

Output:

```
    name  age sex
0   John   30   M
1  Smith   25   M
2   Paul   40   M
```

To convert the `name` column to a Pandas series, we can use the following code:

```
series = df['name'].squeeze()
print(series)
```

Output:

```
0     John
1    Smith
2     Paul
Name: name, dtype: object
```

Similarly, to convert the index to a Pandas series, we can use the following code:

```
series = df.index.squeeze()
print(series)
```

Output:

```
RangeIndex(start=0, stop=3, step=1)
```


## Section 3: Converting multiple columns to a series
We can also convert multiple columns of a data frame to a single Pandas series by concatenating them using the `concat()` function. We can specify the axis along which we want to concatenate the columns. We can concatenate the columns of the data frame by setting the axis parameter to 0. Then, we can use the `squeeze()` method on the concatenated column to convert it to a Pandas series.

**Example:**

Consider the following data frame:

```
import pandas as pd

data = {'name': ['John', 'Smith', 'Paul'],
        'age': [30, 25, 40],
        'sex': ['M', 'M', 'M']}

df = pd.DataFrame(data)
print(df)
```

Output:

```
    name  age sex
0   John   30   M
1  Smith   25   M
2   Paul   40   M
```

To convert the `name` and `age` columns to a single Pandas series, we can use the following code:

```
series = pd.concat([df['name'], df['age']], axis=0).squeeze()
print(series)
```

Output:

```
0     John
1    Smith
2     Paul
0       30
1       25
2       40
dtype: object
```


## Section 4: Conclusion
In this tutorial, we have seen how to convert a Pandas data frame to series in Python. We can use the `iloc`, `loc`, or column indexing operator [] to select the desired column or index. Then, we can use `squeeze()` method on the selected column or index to convert it to a Pandas series. We can also concatenate multiple columns of the data frame to a single Pandas series using the `concat()` function.
