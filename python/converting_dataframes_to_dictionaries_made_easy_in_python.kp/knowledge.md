---
title: What is the process of transforming a dataframe into a dictionary?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the to\_dict() method on the dataframe object to convert the dataframe to a dictionary.
---

**Contents**

[TOC]

## Convert Dataframe to Dictionary using pandas

The easiest way to convert a pandas DataFrame to a dictionary is to use the `to_dict()` method. This method will return a dictionary where keys are column names and values are lists of values for each column.

``` python
import pandas as pd

# create a sample DataFrame
df = pd.DataFrame({'a': [1, 2, 3], 'b': [4, 5, 6], 'c': [7, 8, 9]})

# convert DataFrame to dictionary
my_dict = df.to_dict()

print(my_dict)
```

Output:

```
{'a': {0: 1, 1: 2, 2: 3}, 'b': {0: 4, 1: 5, 2: 6}, 'c': {0: 7, 1: 8, 2: 9}}
```


## Convert Dataframe to Dictionary using zip()

Another way to convert a DataFrame to a dictionary is to use the `zip()` function. This method will allow you to create a dictionary with keys and values from the DataFrame.

``` python
import pandas as pd

# create a sample DataFrame
df = pd.DataFrame({'a': [1, 2, 3], 'b': [4, 5, 6], 'c': [7, 8, 9]})

# convert DataFrame to dictionary
my_dict = dict(zip(df.columns, [df[col].tolist() for col in df.columns]))

print(my_dict)
```

Output:

```
{'a': [1, 2, 3], 'b': [4, 5, 6], 'c': [7, 8, 9]}
```


## Convert Dataframe to Dictionary with Nested Dictionary

If you want to create a nested dictionary from a DataFrame, where one column is the key and the other columns are values, you can use the `set_index()` and `to_dict()` methods.

``` python
import pandas as pd

# create a sample DataFrame
df = pd.DataFrame({'key': ['A', 'B', 'C'], 'value_1': [1, 2, 3], 'value_2': [4, 5, 6]})

# convert DataFrame to dictionary
my_dict = df.set_index('key').T.to_dict('list')

print(my_dict)
```

Output:

```
{'A': [1, 4], 'B': [2, 5], 'C': [3, 6]}
```


## Convert Dataframe to Dictionary with Custom Formats

Finally, if you want to create a dictionary with custom formats or data types, you can use the `map()` method to convert the values.

``` python
import pandas as pd

# create a sample DataFrame
df = pd.DataFrame({'a': [1, 2, 3], 'b': [4, 5, 6], 'c': [7, 8, 9]})

# convert DataFrame to dictionary with custom format
my_dict = df.to_dict()
my_dict = {k: list(map(float, v.values())) for k, v in my_dict.items()}

print(my_dict)
```

Output:

```
{'a': [1.0, 2.0, 3.0], 'b': [4.0, 5.0, 6.0], 'c': [7.0, 8.0, 9.0]}
```
