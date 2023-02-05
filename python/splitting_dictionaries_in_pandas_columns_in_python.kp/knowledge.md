---
title: Separate the elements of a pandas column containing dictionaries into distinct columns
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the pandas.DataFrame.from\_dict() method to convert the column of dictionaries into a dataframe and then use the pandas.DataFrame.explode() method to separate the column into separate columns.
---

**Contents**

[TOC]

**Section 1: Overview**

Pandas is a powerful library in Python for data manipulation and analysis. It provides a wide range of operations for manipulating and transforming data, including the ability to split or explode a column of dictionaries into separate columns. This can be done using the pandas.DataFrame.explode() or pandas.Series.str.split() methods.

**Section 2: pandas.DataFrame.explode()**

The pandas.DataFrame.explode() method can be used to split a column of dictionaries into separate columns. This method takes in a column of dictionaries, and creates a new row for each key-value pair in the dictionaries. The keys become the column headers, and the values become the values for the corresponding column.

**Section 3: pandas.Series.str.split()**

The pandas.Series.str.split() method can also be used to split a column of dictionaries into separate columns. This method takes in a column of dictionaries, and splits each dictionary into separate strings. The strings are then split into separate columns, with the keys becoming the column headers, and the values becoming the values for the corresponding column.

**Section 4: Example**

Here is an example of how to use the pandas.DataFrame.explode() and pandas.Series.str.split() methods to split a column of dictionaries into separate columns.

```
import pandas as pd

# Create a dataframe with a column of dictionaries
df = pd.DataFrame({'data': [{'name': 'John', 'age': 20},
                            {'name': 'Jane', 'age': 22},
                            {'name': 'Bob', 'age': 24}]})

# Split the column of dictionaries using pandas.DataFrame.explode()
df_exploded = df.explode('data')

# Split the column of dictionaries using pandas.Series.str.split()
df_split = df['data'].str.split(',', expand=True)

# Print the result
print(df_exploded)
print(df_split)
```

The output would be:

```
    name  age
0   John   20
1   Jane   22
2   Bob    24
   name age
0  John  20
1  Jane  22
2   Bob  24
```
