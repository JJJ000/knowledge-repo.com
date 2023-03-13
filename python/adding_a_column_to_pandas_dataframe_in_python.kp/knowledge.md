---
title: Add a new column to a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the `df[`new\_column`] = values` syntax to append a new column to a pandas dataframe in Python.
---

**Contents**

[TOC]

Section 1: Introduction
Pandas is one of the most widely used libraries when it comes to data manipulation. It is particularly useful when it comes to dealing with structured data in the form of a table or a spreadsheet. In many cases, we might want to add a new column to an existing pandas dataframe. In this tutorial, we will explain how to append a column to a pandas dataframe in Python. 

Section 2: Adding a single column
Adding a single column to a pandas dataframe is straightforward. We can use the following syntax: 

``` df['new_column_name'] = new_column_values ```

where `df` is the pandas dataframe and `new_column_values` are the values we want to add to the dataframe. 

For example, let's say we have the following pandas dataframe: 

```
import pandas as pd

# create a dataframe
df = pd.DataFrame({'name': ['Alice', 'Bob', 'Charlie', 'David'], 'age': [25, 30, 35, 40]})

print(df)
```

Output:

```
       name  age
0     Alice   25
1       Bob   30
2   Charlie   35
3     David   40
```

We can add a new column called `gender` as follows:

```
# add a new column to the dataframe
df['gender'] = ['F', 'M', 'M', 'M']

print(df)
```

Output:
```
       name  age gender
0     Alice   25      F
1       Bob   30      M
2   Charlie   35      M
3     David   40      M
```

Section 3: Adding multiple columns
To append multiple columns to a pandas dataframe, we can use the same approach as for a single column, but we need to provide a list of column values instead of a single value. 

For example, let's say we want to add two new columns `city` and `country` to the existing pandas dataframe. We can do this as follows:

```
# add two new columns to the dataframe
df['city'] = ['New York', 'Paris', 'London', 'Sydney']
df['country'] = ['USA', 'France', 'UK', 'Australia']

print(df)
```

Output:
```
       name  age gender      city    country
0     Alice   25      F  New York        USA
1       Bob   30      M     Paris     France
2   Charlie   35      M    London         UK
3     David   40      M    Sydney  Australia
```

Section 4: Conclusion
In this tutorial, we have learned how to add a new column or multiple columns to an existing pandas dataframe in Python. We hope this tutorial has been helpful!
