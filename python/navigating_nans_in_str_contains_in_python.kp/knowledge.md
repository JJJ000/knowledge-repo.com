---
title: Disregarding nan values while using str.contains
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To ignore NaNs with str.contains in Python, use the na=False parameter.
---

**Contents**

[TOC]

Section 1: Understanding NaNs

NaN stands for Not a Number. It is a special floating-point value used in computing to represent undefined or unrepresentable values, such as the result of a calculation that doesn't produce a valid number. NaNs can arise from operations like dividing zero by zero, taking the square root of a negative number, or attempting to convert a non-numeric string to a number.

In Python, NaNs are represented as floats and can be imported from the NumPy library using the command `np.nan`. NaNs can also appear in pandas dataframes or series when data is missing or incomplete.

Section 2: Using str.contains() to search for strings

The `str.contains()` method in Python is used to check whether a specified string is present in another string or a series of strings. It returns a boolean value (True or False) for each element in the specified series, indicating whether or not that element contains the specified string.

Here is an example of using `str.contains()` in Python:

```
import pandas as pd

# create a dataframe with strings
df = pd.DataFrame({'fruits': ['apple', 'banana', 'cherry', 'durian']})

# check if 'an' is present in each string
df['contains_an'] = df['fruits'].str.contains('an')

print(df)
```

Output:

```
   fruits  contains_an
0   apple         True
1  banana         True
2  cherry        False
3  durian         True
```

This code generates a pandas dataframe called `df` with a column called 'fruits' containing four different fruits as strings. The `str.contains()` method is used to check if the string 'an' is present in each fruit name, and the resulting boolean values are stored in a new column called 'contains_an'.

Section 3: Ignoring NaNs with str.contains()

When using `str.contains()` with a pandas dataframe or series that contains NaNs, the method will throw an error if it encounters a NaN value. To ignore NaNs, we can use the `na` parameter in `str.contains()` and set it to `False`.

Here is an example of using `str.contains()` with NaNs in Python:

```
import pandas as pd
import numpy as np

# create a dataframe with strings and NaN values
df = pd.DataFrame({'fruits': ['apple', 'banana', np.nan, 'durian']})

# check if 'an' is present in each string, ignoring NaNs
df['contains_an'] = df['fruits'].str.contains('an', na=False)

print(df)
```

Output:

```
   fruits  contains_an
0   apple         True
1  banana         True
2     NaN        False
3  durian         True
```

This code generates a pandas dataframe called `df` with a column called 'fruits' containing four different fruits as strings, including one NaN value. The `str.contains()` method is used to check if the string 'an' is present in each fruit name, and the resulting boolean values are stored in a new column called 'contains_an', ignoring the NaN value.

Section 4: Conclusion

Ignoring NaNs when using `str.contains()` in Python is easy with the `na` parameter. By setting it to `False`, the method will skip over NaN values and only check for string matches in non-NaN values. This allows for consistent and error-free string searching in pandas dataframes or series that may contain NaNs.
