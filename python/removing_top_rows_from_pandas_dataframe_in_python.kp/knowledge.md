---
title: Remove the first three rows of a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `drop()` method with `index` parameter set to a list of row indices to drop the first three rows of a dataframe in pandas `df.drop(index=[0,1,2], inplace=True)`
---

**Contents**

[TOC]

## 1. Creating a sample dataframe
First, we need to create a sample dataframe to demonstrate how to delete the first three rows.

```python

import pandas as pd

# Creating a sample dataframe
df = pd.DataFrame({'Name':['John', 'Mike', 'Sara', 'Emily', 'Jessica'],
                   'Age':[25, 30, 21, 27, 29],
                   'City':['New York', 'Chicago', 'Los Angeles', 'San Francisco', 'Seattle']})

print(df)


   Name  Age           City
0   John   25       New York
1   Mike   30        Chicago
2   Sara   21    Los Angeles
3  Emily   27  San Francisco
4  Jessica 29       Seattle

```

## 2. Delete the first three rows
Now that we have a sample dataframe, we can delete the first three rows using the `drop()` method in pandas. We can specify the range of rows we want to delete and set the `inplace` parameter to `True` to modify the original dataframe.

```python

df.drop(df.index[:3], inplace=True)

print(df)


      Name  Age           City
3     Emily   27  San Francisco
4  Jessica   29        Seattle

```

## 3. Explanation
In the code above, we used the `drop()` method to delete the first three rows of the dataframe. The `df.index[:3]` specifies the first three rows and the `inplace=True` parameter modifies the original dataframe. The resulting dataframe only contains the last two rows after we delete the first three rows.

## 4. Conclusion
In conclusion, using the `drop()` method with the `df.index[:3]` parameter allows us to easily delete the first three rows of a dataframe in pandas. We can also use this method to delete any range of rows in a dataframe.
