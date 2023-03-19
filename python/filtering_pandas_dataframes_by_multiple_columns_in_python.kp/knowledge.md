---
title: What is the method to apply multiple column filters to pandas dataframes?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use boolean indexing with multiple conditions joined by `&` or `|` to filter pandas dataframes by multiple columns in Python.
---

**Contents**

[TOC]

### Introduction

When dealing with large data sets, it is often necessary to filter the data frames based on specific criteria. Pandas offer several options to filter data frames, including filtering by multiple columns. In this tutorial, we will demonstrate how to filter pandas data frames by multiple columns using various techniques.

### Filtering by Multiple Columns Using Boolean Operators

One of the ways to filter data frames by multiple columns is by using boolean operators. We can use logical operators such as ‘and’ and ‘or’ to implement the filter. For example, consider the following code:

``` python
import pandas as pd

data = {'Name': ['Adam', 'Bob', 'Carla', 'David', 'Emily'],
        'Age': [27, 21, 23, 25, 29],
        'Gender': ['Male', 'Male', 'Female', 'Male', 'Female'],
        'City': ['Boston', 'Chicago', 'New York', 'Los Angeles', 'Seattle']}

df = pd.DataFrame(data)

filtered_df = df[(df['Gender'] == 'Male') & (df['Age'] >= 25)]

print(filtered_df)
```

In this code, we have created a data frame containing information about individuals, including their name, age, gender, and city. We then filtered the data frame to include only males who are 25 or older using the boolean operators ‘&’ and ‘|’ to combine the conditions.

### Filtering by Multiple Columns Using the ‘query’ Function

Another way to filter data frames by multiple columns is by using the ‘query’ function. The ‘query‘ function is used to filter the data frame based on specific criteria. Here’s an example:

``` python
import pandas as pd

data = {'Name': ['Adam', 'Bob', 'Carla', 'David', 'Emily'],
        'Age': [27, 21, 23, 25, 29],
        'Gender': ['Male', 'Male', 'Female', 'Male', 'Female'],
        'City': ['Boston', 'Chicago', 'New York', 'Los Angeles', 'Seattle']}

df = pd.DataFrame(data)

filtered_df = df.query("Gender == 'Male' and Age >= 25")

print(filtered_df)
```

In this example, we have used the ‘query’ function to filter the data frame in a similar way to the previous example.

### Filtering by Multiple Columns Using the ‘loc’ Function

We can also filter data frames by multiple columns using the ‘loc‘ function, which is used to select rows and columns based on specific criteria. Here is an example code:

``` python
import pandas as pd

data = {'Name': ['Adam', 'Bob', 'Carla', 'David', 'Emily'],
        'Age': [27, 21, 23, 25, 29],
        'Gender': ['Male', 'Male', 'Female', 'Male', 'Female'],
        'City': ['Boston', 'Chicago', 'New York', 'Los Angeles', 'Seattle']}

df = pd.DataFrame(data)

filtered_df = df.loc[(df['Gender'] == 'Male') & (df['Age'] >= 25)]

print(filtered_df)
```

In this example, we have used the ‘loc’ function to filter the data frame in a similar way to the previous examples.

### Conclusion

In this tutorial, we have shown you various ways to filter pandas data frames by multiple columns using boolean operators, the ‘query’ function, and the ‘loc’ function. Filtering data frames by multiple columns can be useful in many data manipulation scenarios.
