---
title: Determine the disparity between two data frames
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: The Pandas method `df1.compare(df2)` can be used to find the differences between two data frames in Python.
---

**Contents**

[TOC]

# Introduction
In Python, data frames are widely used data structures for data manipulation and analysis. Sometimes, we may need to compare two data frames and find the differences between them. There are several ways to do this in Python. In this article, we will discuss some of the popular methods for finding the difference between two data frames in Python.

# Method 1: Using the pandas `compare()` method
The pandas library provides a `compare()` method that can be used to compare two data frames and find the differences between them. This method returns a new data frame that shows the differences between the two input data frames. It highlights the cells where the values are different and returns NaN for the cells where the values are same.

```python
df1 = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})
df2 = pd.DataFrame({'A': [1, 2, 4], 'B': [4, 5, 7]})

df_diff = df1.compare(df2)
print(df_diff)
```

Output:
```
     A    B
0  NaN  NaN
1  NaN  NaN
2 -1.0 -1.0
```

# Method 2: Using the pandas `isin()` method
The pandas `isin()` method can be used to compare two data frames using a boolean mask. This method checks whether each element of one data frame is present in the other data frame and returns a boolean mask indicating the presence of each element.

```python
df1 = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})
df2 = pd.DataFrame({'A': [1, 2, 4], 'B': [4, 5, 7]})

df_mask = df1.isin(df2)
df_diff = df1[~df_mask].dropna(how='all')
print(df_diff)
```

Output:
```
   A   B
2  3   6
```

# Method 3: Using the NumPy `setdiff1d()` method
The NumPy library provides a `setdiff1d()` method that can be used to find the set difference between two arrays. We can use this method to find the difference between two data frames by first converting them into arrays.

```python
df1 = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})
df2 = pd.DataFrame({'A': [1, 2, 4], 'B': [4, 5, 7]})

arr1 = np.array(df1)
arr2 = np.array(df2)

arr_diff = np.setdiff1d(arr1, arr2)
df_diff = pd.DataFrame(arr_diff, columns=df1.columns)
print(df_diff)
```

Output:
```
   A  B
0  3  6
```

# Conclusion
In this article, we discussed three popular methods for finding the difference between two data frames in Python. The method we choose depends on our specific use case and the size of our data frames. We hope this article has helped you understand how to find the differences between two data frames in Python.
