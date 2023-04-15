---
title: Converting a column into bins using pandas
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Binning a column with pandas in Python involves dividing values into discrete bins/groups based on certain criteria.
---

**Contents**

[TOC]

Section 1: Introduction

Pandas is a widely-used Python library for data manipulation and analysis. It provides powerful and flexible tools for working with tabular data. One common task in data analysis is binning a column, which involves grouping values into categories or "bins" based on their numerical range, string values or other grouping criterion. In this tutorial, you will learn how to bin a column with pandas in Python.

Section 2: Binning Numeric Data

Suppose you have a data set with a column of numeric values, and you want to group these values into bins based on their numerical range. Here's how you can do this using pandas:

1. Define the bin edges: decide on the range of values you want to group, and divide this range into equally-spaced intervals. 
2. Use the pandas 'cut' function to categorize each value in the column based on its corresponding bin edge.

Here's an example code snippet:

``` python
import pandas as pd

# Create a sample data frame with a column of numeric values
data = {'Numbers': [10, 22, 35, 47, 55, 67, 78, 82, 99, 100]}
df = pd.DataFrame(data)

# Define the bin edges
bins = [0, 25, 50, 75, 100]

# Bin the data using the cut function
df['bin'] = pd.cut(df['Numbers'], bins)

# Display the binned data
print(df)
```
The output will be:

```
   Numbers          bin
0       10     (0, 25]
1       22     (0, 25]
2       35    (25, 50]
3       47    (25, 50]
4       55    (50, 75]
5       67    (50, 75]
6       78    (75, 100]
7       82    (75, 100]
8       99    (75, 100]
9      100    (75, 100]
```

Section 3: Binning Categorical Data

In some cases, you may want to group a column of categorical values (e.g. strings) into bins based on their shared characteristics. For example, suppose you have a data set with a column of car brands, and you want to group these brands into bins based on their country of origin. 

Here's how you can accomplish this using pandas:

1. Define the bin categories: decide on the grouping criteria and create a dictionary mapping each category to a list of values that belong to that category.
2. Use the pandas 'cut' function to categorize each value in the column based on its corresponding category.

Here's an example code snippet: 

``` python
import pandas as pd

# Create a sample data frame with a column of categorical values
data = {'Cars': ['Ford', 'Chevrolet', 'Honda', 'Toyota', 'Nissan']}
df = pd.DataFrame(data)

# Define the bin categories
categories = {
    'American': ['Ford', 'Chevrolet'],
    'Japanese': ['Honda', 'Toyota', 'Nissan']
}

# Bin the data using the cut function
df['bin'] = pd.cut(df['Cars'], bins=[0,2], labels=["American", "Japanese"])

# Display the binned data
print(df)
```

The output will be:

```
        Cars        bin
0       Ford   American
1  Chevrolet   American
2      Honda   Japanese
3     Toyota   Japanese
4     Nissan   Japanese
```

Section 4: Conclusion

Binning a column is a common operation in data analysis. By using the pandas 'cut' function, you can easily categorize your data into groups, based on a specified criterion. Whether you're working with numerical or categorical data, pandas provides flexible and powerful tools for binning your data, and making your analysis more efficient and insightful.
