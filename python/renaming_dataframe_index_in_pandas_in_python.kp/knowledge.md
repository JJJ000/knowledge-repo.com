---
title: Reworded change the index labels of a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To rename the index of a Pandas DataFrame in Python, use the rename\_axis() method.
---

**Contents**

[TOC]

# Introduction

In Pandas DataFrame, an index is used to identify and locate rows. Sometimes, we may want to change the names of the index columns for clarity or consistency with other data frames. This tutorial will demonstrate how to rename the index of a Pandas DataFrame in Python.

# Creating a Sample DataFrame

Before we begin, let's create a small sample DataFrame that we will use throughout the tutorial:

``` python
import pandas as pd

data = {'Name': ['John', 'Mary', 'Peter', 'Sam', 'Ivy'],
        'Age': [28, 45, 33, 52, 35],
        'Country': ['USA', 'Canada', 'UK', 'Australia', 'USA']}

df = pd.DataFrame(data)
```

The DataFrame looks like this:

```
    Name    Age    Country
0   John    28     USA
1   Mary    45     Canada
2   Peter   33     UK
3   Sam     52     Australia
4   Ivy     35     USA
```

# Renaming the Index Using set_index() Method

The simplest way to rename the index column in a Pandas DataFrame is to use the `set_index()` method with the `inplace=True` parameter.

``` python
df.set_index('Name', inplace=True)
```

This will rename the index column from the default numeric values `[0, 1, 2, 3, 4]` to the `Name` column.

The resulting DataFrame looks like this:

```
        Age    Country
Name                
John    28     USA
Mary    45     Canada
Peter   33     UK
Sam     52     Australia
Ivy     35     USA
```

# Renaming the Index Column Using rename_axis() Method

Sometimes, we may want to change the name of the index column without changing the actual index values. For this, we can use the `rename_axis()` method.

``` python
df.rename_axis('Customer', inplace=True)
```

This will rename the index column to `Customer`. The actual index values are not changed.

The resulting DataFrame looks like this:

```
          Age    Country
Customer                
John       28     USA
Mary       45     Canada
Peter      33     UK
Sam        52     Australia
Ivy        35     USA
```

# Renaming the Index Values Using rename() Method

Finally, if we want to change the names of the index values themselves, we can use the `rename()` method.

``` python
df = df.rename(index={'John': 'Johnny', 'Mary': 'Marianne'})
```

This will rename the index value `John` as `Johnny` and `Mary` as `Marianne`. We can add as many key-value pairs as we need to this dictionary.

The resulting DataFrame looks like this:

```
           Age    Country
Customer                
Johnny     28     USA
Marianne   45     Canada
Peter      33     UK
Sam        52     Australia
Ivy        35     USA
```

# Conclusion

In this tutorial, we have covered three ways to rename the index of a Pandas DataFrame in Python. The first method is to use the `set_index()` method with the `inplace=True` parameter. The second method is to use the `rename_axis()` method to change the name of the index column. The third method is to use the `rename()` method to change the names of the index values themselves. All three methods are very easy to use and can be adapted to any DataFrame.
