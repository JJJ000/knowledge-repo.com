---
title: First, use pandas groupby to group the data, then sort the data within each group
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To sort a pandas groupby object within each group, use the apply() method along with a lambda function that sorts the group based on a particular column.
---

**Contents**

[TOC]

## Introduction
Pandas is a popular data manipulation library in Python that provides functionalities for data analysis and manipulation such as merging, filtering, sorting, and grouping. One of the most common operations in data analysis is grouping data by a criterion and then sorting the groups. In this tutorial, we will explore how to use pandas groupby to group data, and then sort the groups using various methods.

## Setup
Before we start, let us install pandas and create some sample data to work with. Open your terminal or command prompt and run the following commands:

```
pip install pandas
```

Next, create a new Python script and import pandas:

```python
import pandas as pd
import numpy as np
```

We will also generate some sample data by creating a DataFrame with three columns: `Group`, `Value`, and `Rank`.

```python
data = {
    'Group': ['A'] * 5 + ['B'] * 5,
    'Value': np.arange(10),
    'Rank': np.random.randint(1, 6, 10)
}

df = pd.DataFrame(data)
print(df)
```

This creates a DataFrame that looks like this:

```
  Group  Value  Rank
0     A      0     3
1     A      1     1
2     A      2     2
3     A      3     2
4     A      4     1
5     B      5     4
6     B      6     1
7     B      7     3
8     B      8     3
9     B      9     4
```

## Sorting within groups using the sort_values() method
To sort within groups using pandas groupby, we can use the sort_values() method along with the groupby() method. The sort_values() method takes a column(s) along which to sort the data. To sort within groups, we need to specify the column(s) to sort by as well as the column(s) to group by. 

```python
sorted_df = df.sort_values(['Group', 'Value'])
grouped_df = sorted_df.groupby('Group')
grouped_df.apply(lambda x: x.sort_values('Rank'))
```

This will sort the DataFrame by the 'Group' and 'Value' columns, group it by the 'Group' column, and apply the sort_values() method on each group based on the 'Rank' column. 

Note that we need to use the apply() method to apply the sort_values() method within each group.

The resulting DataFrame will look like this:

```
  Group  Value  Rank
1     A      1     1
4     A      4     1
2     A      2     2
3     A      3     2
0     A      0     3
6     B      6     1
7     B      7     3
8     B      8     3
5     B      5     4
9     B      9     4
```

## Sorting within groups using groupby() and apply()
Another way to sort within groups is to use groupby() and apply(). In this method, we group the DataFrame by the 'Group' column, apply a custom function to each group, and sort the resulting DataFrame.

```python
def sort_group(group):
    return group.sort_values(['Rank'])

sorted_df = df.groupby('Group').apply(sort_group)
```

This will group the DataFrame by the 'Group' column, and for each group, apply the sort_group() function that sorts the group by the 'Rank' column. The resulting sorted DataFrame will look like this:

```
          Group  Value  Rank
Group                      
A     1      A      1     1
      4      A      4     1
      2      A      2     2
      3      A      3     2
      0      A      0     3
B     6      B      6     1
      7      B      7     3
      8      B      8     3
      5      B      5     4
      9      B      9     4
```

Note that the resulting DataFrame has an additional level of indexing, as we are using a multi-level index. We can remove this by resetting the index of the DataFrame:

```python
sorted_df = sorted_df.reset_index(drop=True)
```

This will remove the additional level of indexing and output a DataFrame with the same structure as the previous example:

```
  Group  Value  Rank
0     A      1     1
1     A      4     1
2     A      2     2
3     A      3     2
4     A      0     3
5     B      6     1
6     B      7     3
7     B      8     3
8     B      5     4
9     B      9     4
```

## Sorting within groups using groupby() and sort_values()
Lastly, we can sort within groups using groupby() and sort_values(). This approach is similar to the first method, but we do not need to use apply() here.

```python
sorted_df = df.groupby('Group').apply(lambda x: x.sort_values(['Rank']))
```

This will group the DataFrame by the 'Group' column, and for each group, sort the values by the 'Rank' column. The resulting DataFrame will look exactly the same as the first implementation.

```
  Group  Value  Rank
A  1     A      1     1
   4     A      4     1
   2     A      2     2
   3     A      3     2
   0     A      0     3
B  6     B      6     1
   7     B      7     3
   8     B      8     3
   5     B      5     4
   9     B      9     4
```

## Conclusion
In this tutorial, we have demonstrated how to group data and sort within groups using pandas groupby. We discussed different ways to achieve this, including using the sort_values() method, groupby() and apply(), and groupby() and sort_values(). These methods allow us to manipulate and analyze data in a powerful and flexible way, making pandas an invaluable tool for data analysis and manipulation.
