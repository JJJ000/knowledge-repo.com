---
title: Remove/exclude any extra characters from all the strings in a dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the str.strip() method on the dataframe to strip all strings.
---

**Contents**

[TOC]

# Introduction

When working with data in Python, it is common to encounter situations where the strings in a dataframe contain extra white spaces at the beginning or end. These extra spaces can affect various data analysis tasks such as string matching, grouping, and aggregation. In this guide, we will learn how to strip or trim all strings of a dataframe in Python using various techniques.


# Section 1: The .strip() function

The `.strip()` function is a built-in Python function that removes leading and trailing whitespace characters from a string. We can use this function with the `applymap()` method to remove white spaces from all strings in a dataframe. Here's a code snippet that demonstrates this technique:

``` python
import pandas as pd

# Create a sample dataframe with some strings containing extra white spaces
df = pd.DataFrame({
    'name': [' John  ', ' Jane', 'Michael  '],
    'age': [28, 32, 24],
    'city': ['New York', 'San Francisco  ', 'Los Angeles'],
})

# Strip all strings in the dataframe
df = df.applymap(lambda x: x.strip() if isinstance(x, str) else x)

print(df)
```

Output:
```
      name  age           city
0     John   28       New York
1     Jane   32  San Francisco
2  Michael   24    Los Angeles
```

In this example, we created a sample dataframe with some strings containing leading and trailing white spaces. We then used the `applymap()` method with a lambda function to apply the `.strip()` function to all string values in the dataframe. The `isinstance()` function is used to apply the `.strip()` function only to string values, leaving numeric and boolean values unchanged.


# Section 2: The .apply() function

Another way to strip all strings in a dataframe is to use the `.apply()` function with a lambda function that applies the `.strip()` function to each cell of the dataframe. Here's an example:

``` python
import pandas as pd

# Create a sample dataframe with some strings containing extra white spaces
df = pd.DataFrame({
    'name': [' John  ', ' Jane', 'Michael  '],
    'age': [28, 32, 24],
    'city': ['New York', 'San Francisco  ', 'Los Angeles'],
})

# Define a function to strip all strings in a dataframe
def strip_all_cells(df):
    """
    Strip all white spaces from strings in a dataframe
    """
    df = df.apply(lambda x: x.str.strip() if x.dtype == "object" else x)
    return df

# Strip all strings in the dataframe
df = strip_all_cells(df)

print(df)
```

Output:
```
      name  age           city
0     John   28       New York
1     Jane   32  San Francisco
2  Michael   24    Los Angeles
```

In this example, we defined a custom function called `strip_all_cells()` that applies the `.strip()` function to all string values in a dataframe. We used the `.apply()` function with this custom function to strip all strings in the dataframe.


# Section 3: Using list comprehension

A third way to strip all strings in a dataframe is to use list comprehension. Here's a code snippet that demonstrates this technique:

``` python
import pandas as pd

# Create a sample dataframe with some strings containing extra white spaces
df = pd.DataFrame({
    'name': [' John  ', ' Jane', 'Michael  '],
    'age': [28, 32, 24],
    'city': ['New York', 'San Francisco  ', 'Los Angeles'],
})

# Strip all strings in the dataframe using list comprehension
df = pd.DataFrame([[val.strip() if type(val) == str else val for val in row] for row in df.values], columns=df.columns)

print(df)
```

Output:
```
      name  age           city
0     John   28       New York
1     Jane   32  San Francisco
2  Michael   24    Los Angeles
```

In this example, we used list comprehension to loop through each row and cell of the dataframe and apply the `.strip()` function to all string values. We then created a new dataframe with the stripped values.


# Conclusion

In this guide, we learned how to strip or trim all strings in a dataframe in Python. We covered three different techniques: using the `.strip()` function with the `applymap()` method, using the `.apply()` function with a custom function, and using list comprehension. These techniques can be useful when dealing with dataframes that contain strings with extra white spaces.
