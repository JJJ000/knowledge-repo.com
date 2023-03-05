---
title: Choose specific rows in a pandas dataframe that has a multiindex
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: We can select rows in pandas MultiIndex DataFrame in Python using .loc method with either single or multiple labels/indices.
---

**Contents**

[TOC]

# Section 1: Creating a MultiIndex DataFrame

In order to demonstrate how to select rows in a pandas MultiIndex DataFrame, let's first create an example dataset with a hierarchical index.

We can do this by creating two lists of data, one for each level of the index, and passing them to the `pd.MultiIndex.from_arrays()` method. We can then use this index along with a dictionary of data to create our DataFrame.

```python
import numpy as np
import pandas as pd

# create sample data
data1 = np.random.rand(6)
data2 = np.random.rand(6)
data_dict = {'data1': data1, 'data2': data2}

index_array = [['group1', 'group1', 'group1', 'group2', 'group2', 'group2'], 
               ['A', 'B', 'C', 'A', 'B', 'C']]
index = pd.MultiIndex.from_arrays(index_array, names=['Group', 'Label'])

# create DataFrame
df = pd.DataFrame(data_dict, index=index)
```

This creates a DataFrame that looks like this:

```
              data1     data2
Group  Label                
group1 A      0.766  0.211411
       B      0.200  0.121598
       C      0.871  0.448830
group2 A      0.629  0.986540
       B      0.709  0.104900
       C      0.799  0.266276
```

# Section 2: Selecting rows using .loc[]

One way to select rows in a MultiIndex DataFrame is to use the `.loc[]` accessor. This allows you to select rows based on the values of the index levels.

For example, to select all the rows where the Group is "group1", you would use the following code:

```python
df.loc['group1']
```

This would produce the following output:

```
       data1     data2
Label                
A      0.766  0.211411
B      0.200  0.121598
C      0.871  0.448830
```

You can also specify multiple index levels to select by passing a tuple to `.loc[]`. For example, to select all the rows where the Group is "group1" and the Label is "A", you would use the following code:

```python
df.loc[('group1', 'A')]
```

This would produce the following output:

```
data1    0.766000
data2    0.211411
Name: (group1, A), dtype: float64
```

# Section 3: Selecting rows using boolean indexing

Another way to select rows in a pandas DataFrame is to use boolean indexing. This allows you to select rows based on a condition, such as whether a value is greater than a certain threshold.

To do this with a MultiIndex DataFrame, you can use the `.loc[]` accessor along with a boolean condition. For example, to select all the rows where the data in the "data1" column is greater than 0.5, you would use the following code:

```python
df.loc[df['data1'] > 0.5]
```

This would produce the following output:

```
              data1     data2
Group  Label                
group1 C      0.871  0.448830
group2 A      0.629  0.986540
       C      0.799  0.266276
```

# Section 4: Conclusion

In this tutorial, we learned how to select rows in a pandas MultiIndex DataFrame using two different methods: `.loc[]` and boolean indexing. These methods allow you to select rows based on the values of the index levels or based on a boolean condition. By mastering these techniques, you'll be able to extract exactly the information you need from your MultiIndex DataFrames.
