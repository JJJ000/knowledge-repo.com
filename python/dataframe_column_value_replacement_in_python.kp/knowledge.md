---
title: Substituting values in a dataframe column using pandas
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To replace column values in a pandas DataFrame in Python, use the `.loc` accessor to select the rows and columns where the replacement is necessary and assign the new values to them.
---

**Contents**

[TOC]

Section 1: Introduction to pandas DataFrame
-------------------------------------------
Pandas is a powerful Python library used for data manipulation and analysis. One of the main data structures provided by pandas is the DataFrame. A DataFrame is a two-dimensional table with rows and columns, similar to a spreadsheet.

A DataFrame can store multiple data types and is great for performing various operations on data such as filtering, grouping, merging, and sorting.


Section 2: Replacing column values in a pandas DataFrame
-------------------------------------------------------
Sometimes you may need to replace the values in a specific column of a pandas DataFrame. This can be done using the `replace()` function of pandas.

The `replace()` function takes two parameters: the value to replace and the new value to replace it with. You can replace a single value or multiple values at once by passing a dictionary of the values to replace and their new values.

Here's an example of how to replace a single value in a DataFrame:

```
import pandas as pd

# create a sample DataFrame
df = pd.DataFrame({
    'A': [1, 2, 3, 4, 5],
    'B': ['a', 'b', 'c', 'd', 'e']
})

# replace the value 'b' in column 'B' with 'f'
df['B'] = df['B'].replace('b', 'f')

print(df)
```

Output:
```
   A  B
0  1  a
1  2  f
2  3  c
3  4  d
4  5  e
```

Section 3: Replacing multiple values in a pandas DataFrame
-----------------------------------------------------------
If you want to replace multiple values in a DataFrame, you can pass a dictionary to the `replace()` function. The keys of the dictionary should be the values to replace and the values should be their corresponding new values.

Here's an example of how to replace multiple values in a DataFrame:

```
import pandas as pd

# create a sample DataFrame
df = pd.DataFrame({
    'A': [1, 2, 3, 4, 5],
    'B': ['a', 'b', 'c', 'd', 'e']
})

# replace the values 'b' and 'e' in column 'B' with 'f'
df['B'] = df['B'].replace({'b': 'f', 'e': 'f'})

print(df)
```

Output:
```
   A  B
0  1  a
1  2  f
2  3  c
3  4  d
4  5  f
```

Section 4: Conclusion
----------------------
In this tutorial, we've learned how to replace column values in a pandas DataFrame using the `replace()` function. We've seen how to replace a single value as well as multiple values at once using a dictionary. Replacing column values is an essential operation in data manipulation and analysis, and pandas provides an easy and efficient way to perform this operation.
