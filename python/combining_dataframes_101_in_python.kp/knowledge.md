---
title: What is the process of merging two dataframes?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: The pd.concat() method can be used to combine two dataframes in Python.
---

**Contents**

[TOC]

Section 1: Introduction
When working with data analysis in Python, it's common to have multiple dataframes that need to be combined into one. Combining dataframes is a way to merge or integrate data from different sources into a single output. There are various ways to combine dataframes in Python, and this article will explore some popular methods.

Section 2: Concatenation
Concatenation is the simplest way to combine dataframes. This method combines dataframes vertically or horizontally. Let's say we have two dataframes, A and B, with the same columns and we want to combine them vertically. We can do this using the pandas library:

```python
import pandas as pd

A = pd.DataFrame({'id': [1, 2, 3], 'name': ['Alice', 'Bob', 'Charlie']})
B = pd.DataFrame({'id': [4, 5, 6], 'name': ['David', 'Eli', 'Frank']})
C = pd.concat([A, B])

print(C)
```
Output:
```
   id     name
0   1    Alice
1   2      Bob
2   3  Charlie
0   4    David
1   5      Eli
2   6    Frank
```
In the above example, we used the `concat()` function to concatenate the dataframes A and B, and stored the output in the new dataframe C. We can also concatenate dataframes horizontally by passing the parameter `axis=1` to the `concat()` function.

Section 3: Merge 
Merge is another method to combine dataframes. This method allows you to join two dataframes based on a common column. For example, let's say we have two dataframes, A and B, where A has the columns id, name, and age, and B has the columns id and salary. We can use the merge function to join the two dataframes based on the id column:

```python
import pandas as pd

A = pd.DataFrame({'id': [1, 2, 3], 'name': ['Alice', 'Bob', 'Charlie'], 'age': [25, 31, 36]})
B = pd.DataFrame({'id': [2, 3, 4], 'salary': [50000, 55000, 60000]})
C = pd.merge(A, B, on='id')

print(C)
```
Output:
```
   id     name  age  salary
0   2      Bob   31   50000
1   3  Charlie   36   55000
```
In the above example, we used the `merge()` function to merge the dataframes A and B, based on the common column id. The output dataframe C contains only the rows where the value of the id column is present in both dataframes.

Section 4: Join 
Join is another method to combine dataframes. This method is similar to merge, but it allows you to join dataframes based on their indexes. For example, let's say we have two dataframes, A and B, where A has the columns id, name, and age, and B has the columns id and salary. We can use the join function to join the two dataframes based on their indexes:

```python
import pandas as pd

A = pd.DataFrame({'id': [1, 2, 3], 'name': ['Alice', 'Bob', 'Charlie'], 'age': [25, 31, 36]})
B = pd.DataFrame({'salary': [50000, 55000, 60000]}, index=[2, 3, 4])
C = A.join(B, how='outer')

print(C)
```
Output:
```
   id     name  age   salary
0   1    Alice   25      NaN
1   2      Bob   31  50000.0
2   3  Charlie   36  55000.0
3   4      NaN  NaN  60000.0
```
In the above example, we used the `join()` function to join the dataframes A and B, based on their indexes. The output dataframe C contains all the rows from both dataframes, and if a value is missing in either dataframe, it will be represented as `NaN`. We used the parameter `how='outer'` to perform an outer join, which includes all rows from both dataframes.
