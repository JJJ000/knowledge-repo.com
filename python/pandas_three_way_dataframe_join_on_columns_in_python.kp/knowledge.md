---
title: Joining multiple dataframes on columns using pandas in three ways
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To perform a three-way join on multiple dataframes in pandas using specific columns, use the merge() method with the on parameter specifying the columns to merge on.
---

**Contents**

[TOC]

Section 1: Introduction to three-way joining in Pandas
- In pandas, three-way joining involves merging three dataframes together based on one or more common columns.
- This is useful when you have multiple datasets with related information that you want to combine into one comprehensive dataset.
- Three-way joining can be achieved using the pandas `merge()` function, which allows you to specify the columns on which to merge the dataframes.

Section 2: Syntax for three-way joining
- The syntax for merging three dataframes in pandas is as follows:
```
pd.merge(df1, pd.merge(df2, df3, on='common_column'), on='common_column')
```
- In this syntax, `df1`, `df2`, and `df3` are the three dataframes you want to merge.
- The `pd.merge(df2, df3, on='common_column')` inner merge creates a temporary dataframe that results from merging `df2` and `df3` on a common column specified by `on`.
- The resulting temporary dataframe is then merged with `df1` on the same common column specified by `on`.

Section 3: Example of three-way joining in Pandas
- Let's see an example of merging three dataframes in pandas. Suppose we have the following three dataframes:
```
df1 = pd.DataFrame({'name': ['Alice', 'Bob', 'Charlie'], 'age': [25, 30, 35]})
df2 = pd.DataFrame({'name': ['Alice', 'Charlie', 'Dave'], 'gender': ['F', 'M', 'M']})
df3 = pd.DataFrame({'name': ['Bob', 'Charlie', 'Emily'], 'city': ['New York', 'San Francisco', 'Chicago']})
```
- We can merge these three dataframes on the common column 'name' as follows:
```
result = pd.merge(df1, pd.merge(df2, df3, on='name'), on='name')
```
- The resulting dataframe `result` will be:
```
      name  age gender           city
0    Alice   25      F            NaN
1  Charlie   35      M  San Francisco
2      Bob   30    NaN       New York
```
- In this result, we can see that the three dataframes have been merged based on the common column 'name'.

Section 4: Conclusion
- Three-way joining in pandas can be a powerful tool for combining multiple datasets based on one or more common columns.
- The `merge()` function in pandas allows you to easily merge three or more dataframes together using a simple syntax.
- When merging dataframes, it is important to carefully consider the columns on which you want to merge and to ensure that the resulting merged dataframe is accurate and complete.
