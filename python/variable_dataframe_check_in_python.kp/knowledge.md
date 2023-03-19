---
title: Verify whether the variable is a dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the `isinstance()` function and check if the variable is an instance of the `pandas.DataFrame` class.
---

**Contents**

[TOC]

# Section 1: Introduction
In Python, a dataframe is a common data structure used in data analysis and manipulation. It is a two-dimensional table-like structure with rows and columns, where each column can be of a different data type. In this tutorial, we will discuss how to check if a variable is a dataframe in Python.

# Section 2: Using isinstance() function
One of the easiest ways to check if a variable is a dataframe is by using the isinstance() function. This function takes two arguments: the variable to check and the class or type to compare it to. If the variable is an instance of the given class or type, it returns True; otherwise, it returns False.

Here's an example:

```python
import pandas as pd

# create a dataframe
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6], 'C': [7, 8, 9]})

# check if the variable is a dataframe
if isinstance(df, pd.DataFrame):
    print("Variable is a dataframe")
else:
    print("Variable is not a dataframe")
```

Output:
```
Variable is a dataframe
```

# Section 3: Using type() function
Another way to check if a variable is a dataframe is by using the type() function. This function returns the type of the given object. We can compare this type to the pandas DataFrame type to check if the variable is a dataframe.

Here's an example:

```python
import pandas as pd

# create a dataframe
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6], 'C': [7, 8, 9]})

# check if the variable is a dataframe
if type(df) == pd.DataFrame:
    print("Variable is a dataframe")
else:
    print("Variable is not a dataframe")
```

Output:
```
Variable is a dataframe
```

# Section 4: Using pandas.api.types.is_dataframe() function
Pandas provide a function is_dataframe() in pandas.api.types module for checking whether the given object is a pandas dataframe or not.

Here's an example:

```python
import pandas as pd
from pandas.api.types import is_dataframe

# create a dataframe
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6], 'C': [7, 8, 9]})

# check if the variable is a dataframe
if is_dataframe(df):
    print("Variable is a dataframe")
else:
    print("Variable is not a dataframe")
```

Output:
```
Variable is a dataframe
```

# Conclusion
In this tutorial, we have discussed how to check if a variable is a dataframe in Python using different methods such as isinstance() function, type() function, and pandas.api.types.is_dataframe() function. The use of any of these methods will give you a boolean value indicating whether the variable is a dataframe or not.
