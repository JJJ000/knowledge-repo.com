---
title: Identify the name of the column that contains the highest value for every row
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use the pandas method `idxmax(axis=1)` to find the column name with the maximum value for each row in a dataframe.
---

**Contents**

[TOC]

# Introduction
In this task, we will learn how to find the column name which has the maximum value for each row in Python. This is a common task in data analysis when working with large datasets. We will use the pandas library for this purpose.

# Solution
The solution to this problem involves finding the column name with the maximum value for each row in a pandas DataFrame. Here are the steps involved:

## Step 1: Importing the Required Libraries
The first step is to import the pandas library, which we will use to work with data frames in Python. We will also import numpy library which is a dependency for pandas library.

```python
import pandas as pd
import numpy as np
```

## Step 2: Creating a Sample DataFrame
We will create a sample DataFrame for illustration purposes. This can be done using the pandas ```DataFrame()``` function. We will create a 3x3 matrix containing random integers between 1 and 10.

```python
np.random.seed(42)
df = pd.DataFrame(np.random.randint(1, 10, size=(3, 3)), columns=['A', 'B', 'C'])
```

This will create a DataFrame object called df with the following values:

```
   A  B  C
0  7  4  8
1  5  7  3
2  7  8  5
```

## Step 3: Finding the Column with the Maximum Value
We will use the pandas ```idxmax()``` function to find the column with the maximum value for each row. This function returns the index of the maximum value for each row.

```python
df.idxmax(axis=1)
```

This will return the following result:

```
0    C
1    B
2    B
dtype: object
```

This indicates that the maximum values in the first, second and third rows are in columns C, B and B respectively.

## Step 4: Outputting the Results
We can store the results in a new column of the DataFrame or in a separate list or series. Here, we will add a new column to the DataFrame called ```Max_Column``` to store the column with the maximum value for each row.

```python
df['Max_Column'] = df.idxmax(axis=1)
```

This will add a new column to the DataFrame with the following values:

```
   A  B  C Max_Column
0  7  4  8          C
1  5  7  3          B
2  7  8  5          B
```

# Conclusion
In this task, we learned how to find the column name which has the maximum value for each row in Python using pandas library. We used the ```idxmax()``` function to identify the column name with the maximum value and added a new column to the DataFrame to store these values. The ability to find the column name with the maximum value for each row is an important tool for data analysis and can be used to identify relevant features or variables in a large dataset.
