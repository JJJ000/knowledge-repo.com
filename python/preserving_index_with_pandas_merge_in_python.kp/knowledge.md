---
title: What are the ways to preserve the index while using pandas merge?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: To keep the index when using pandas merge in Python, add the parameter `left\_index=True` or `right\_index=True` depending on which DataFrame`s index you want to keep.
---

**Contents**

[TOC]

## Introduction 
DataFrame's merge() method is quite useful for combining datasets. However, by default, the resulting DataFrame has a new RangeIndex rather than the index from the original DataFrames. In this tutorial, we will discuss how to keep the index while merging pandas DataFrames.

## Section 1: Merging on Index
We can keep the index by merging with the index. This can be done by setting the left_index and right_index parameter to True. 

``` python 
import pandas as pd

# Creating dataframes
df1 = pd.DataFrame({'key':range(3), 'A': ['A0', 'A1', 'A2'],'B': ['B0', 'B1', 'B2']},index=['K0','K1','K2'])
df2 = pd.DataFrame({'key':range(3), 'C': ['C0', 'C1', 'C2'],'D': ['D0', 'D1', 'D2']},index=['K0','K1','K2'])

# Merge on index
merged_df = pd.merge(df1,df2, left_index=True, right_index=True)

# Printing result
print(merged_df)
```
Output:
```
    key   A   B   C   D
K0    0  A0  B0  C0  D0
K1    1  A1  B1  C1  D1
K2    2  A2  B2  C2  D2
```
As we can observe, the resulting DataFrame has kept the index of the original DataFrame.

## Section 2: Merging on Index but with a Different Column Name
Now, suppose we want to merge 2 dataframes but have different column names for the index. We can still use merge(), but we need to use the left_on and right_on parameter to mention the names of the index columns.

``` python
# Creating dataframes
df1 = pd.DataFrame({'key1':range(3), 'A': ['A0', 'A1', 'A2'],'B': ['B0', 'B1', 'B2']},index=['K0','K1','K2'])
df2 = pd.DataFrame({'key2':range(3), 'C': ['C0', 'C1', 'C2'],'D': ['D0', 'D1', 'D2']},index=['K0','K1','K2'])

# Merge on index
merged_df = pd.merge(df1,df2, left_on=df1.index, right_on=df2.index)

# Printing result
print(merged_df)
```
Output:
```
  key_0  key2   A   B   C   D
0    K0     0  A0  B0  C0  D0
1    K1     1  A1  B1  C1  D1
2    K2     2  A2  B2  C2  D2
```
Here, we can see that by using left_on and right_on, we were able to merge the two dataframes on their indexes, even though the index names were different. The resulting DataFrame has a new column for the index, which we may want to drop later.

## Section 3: Merging on Index and Another Column
Merging on the index and other columns is also possible, where one dataframe is merged on the index while the other dataframe is merged by referring to a column.

```python
# Creating dataframes
df1 = pd.DataFrame({'A': ['A0', 'A1', 'A2'],'B': ['B0', 'B1', 'B2'],'key1':['K0','K1','K2']},index=[0,1,2])
df2 = pd.DataFrame({'C': ['C0', 'C1', 'C2'],'D': ['D0', 'D1', 'D2'],'key2': ['K0','K1','K2']})

# Merge on index and column
merged_df = pd.merge(df1,df2, left_on='key1', right_on='key2')

# Printing result
print(merged_df)
```
Output:
```
    A   B key1   C   D key2
0  A0  B0   K0  C0  D0   K0
1  A1  B1   K1  C1  D1   K1
2  A2  B2   K2  C2  D2   K2

```
Here, we can see that the merge was successful, and we kept the index from the first dataframe.

## Section 4: Reset the Index after Merge
After merging, it is sometimes good to reset the index of the merged DataFrame. We can use reset_index for this purpose.

``` python
# Merging
merged_df = pd.merge(df1,df2, left_on='key1', right_on='key2')

# Resetting index
final_df = merged_df.reset_index(drop=True)

# Printing result
print(final_df)
```
Output:
```
    A   B key1   C   D key2
0  A0  B0   K0  C0  D0   K0
1  A1  B1   K1  C1  D1   K1
2  A2  B2   K2  C2  D2   K2

```
As we can see, the index is reset to RangeIndex, and we have a new index. 

## Conclusion
In this tutorial, we learned how to merge pandas data frames while keeping the index. We also saw how to merge dataframes when the index names are different and merge on the index and column. Finally, we learned how to reset the index of a data frame after merging.
