---
title: What is the process of printing a groupby object?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can print a groupby object in Python by iterating over it or by using the `groups` attribute.
---

**Contents**

[TOC]

# Introduction

A `groupby` object in Python is created by grouping rows of a Pandas DataFrame based on a specified column or set of columns. Grouping data allows us to perform operations on subsets of the data, such as aggregations or transformations. In this tutorial, we will discuss how to print a groupby object in Python.

# Sample Dataset

Let's create a sample dataset to demonstrate how to print a groupby object:

```python
import pandas as pd

data = {
    'Name': ['Alice', 'Bob', 'Charlie', 'David', 'Eric', 'Frank', 'Alice', 'David', 'Charlie', 'Bob'],
    'City': ['Seattle', 'Portland', 'Seattle', 'Miami', 'Portland', 'Miami', 'Seattle', 'Miami', 'Seattle', 'Portland'],
    'Amount': [100, 200, 300, 400, 500, 600, 700, 800, 900, 1000]
}

df = pd.DataFrame(data)
```

In this example, we have a DataFrame with three columns: `Name`, `City`, and `Amount`.

# Using the `get_group()` Method

One way to print a groupby object is to use the `get_group()` method. This method allows us to select a specific group from the groupby object and return it as a DataFrame. Here's how to use it:

```python
grouped = df.groupby('City')

seattle_group = grouped.get_group('Seattle')
print(seattle_group)
```

Output:
```
       Name     City  Amount
0     Alice  Seattle     100
2   Charlie  Seattle     300
6     Alice  Seattle     700
8   Charlie  Seattle     900
```

In this example, we grouped the DataFrame by the `City` column and selected the group for `'Seattle'`. The resulting DataFrame contains only the rows from the original DataFrame where the `City` column equals `'Seattle'`.

# Using a For Loop

Another way to print a groupby object is to use a for loop. This method allows us to iterate over the groups and print each group as a DataFrame. Here's an example:

```python
grouped = df.groupby('City')

for name, group in grouped:
    print(name)
    print(group)
```

Output:
```
Miami
     Name    City  Amount
3   David   Miami     400
5   Frank   Miami     600
7   David   Miami     800
Portland
     Name      City  Amount
1     Bob  Portland     200
4    Eric  Portland     500
9     Bob  Portland    1000
Seattle
      Name     City  Amount
0    Alice  Seattle     100
2  Charlie  Seattle     300
6    Alice  Seattle     700
8  Charlie  Seattle     900
```

In this example, we grouped the DataFrame by the `City` column and used a for loop to iterate over each group. For each group, we printed the name of the group (the city) and the DataFrame containing the rows from the original DataFrame that belong to that group.

# Using the `groups` Attribute

Finally, we can use the `groups` attribute to print a dictionary that maps each group name to the indices of the rows in the original DataFrame that belong to that group. Here's an example:

```python
grouped = df.groupby('City')

print(grouped.groups)
```

Output:
```
{'Miami': Int64Index([3, 5, 7], dtype='int64'), 'Portland': Int64Index([1, 4, 9], dtype='int64'), 'Seattle': Int64Index([0, 2, 6, 8], dtype='int64')}
```

In this example, we grouped the DataFrame by the `City` column and printed the `groups` attribute of the groupby object. The resulting dictionary maps each unique value in the `City` column to the indices of the rows in the original DataFrame that belong to that group.

# Conclusion

In this tutorial, we discussed how to print a groupby object in Python. We covered three methods: using the `get_group()` method, using a for loop, and using the `groups` attribute. These methods allow us to inspect and work with the groups created by the `groupby()` function, which is a powerful tool for manipulating and analyzing data in Python.
