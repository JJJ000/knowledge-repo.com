---
title: What is the method to obtain the count of columns present in a pandas dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The number of columns in a Pandas data frame can be retrieved using the `shape` attribute and indexing the second element of the tuple (i.e., `df.shape[1]`).
---

**Contents**

[TOC]

# Step 1: Import necessary libraries
To retrieve the number of columns in a Pandas dataframe in Python, you need to import the Pandas library. You can achieve that through the line of code below.

```python
import pandas as pd
```


# Step 2: Create Dataframe
After importing your libraries, you can create a Pandas dataframe. In this illustration, we will create a dataframe 'df'.

```python
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})
```

# Step 3: Retrieve Number of Columns
To retrieve the number of columns in the Pandas dataframe, we can utilize the shape attribute available to any dataframe in Pandas. The .shape attribute returns the number of rows and columns in a dataframe as a tuple. To retrieve the number of columns, we access the shape attribute like df.shape[1].

```python
number_cols = df.shape[1]
print(f"The dataframe has {number_cols} columns.")
```

# Example: Putting it all together:
```python
import pandas as pd

df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})

number_cols = df.shape[1]
print(f"The dataframe has {number_cols} columns.")
```
