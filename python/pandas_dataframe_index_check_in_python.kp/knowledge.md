---
title: Verify whether a value is present in the index of a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To check if a value exists in pandas dataframe index, use the following code `value in df.index`.
---

**Contents**

[TOC]

## Section 1: Introduction

Pandas is an open-source library in Python used for data analysis and manipulation. Data is typically represented in a pandas dataframe object. Dataframes consist of rows and columns, and each row and column has an associated label. The row labels are known as the index, and the column labels are known as the columns. In this tutorial, we will see how to check if a value exists in a pandas dataframe index in Python.


## Section 2: Checking if a value exists in pandas dataframe index

Pandas dataframe index is a special data structure that contains row labels. It can be used to select, filter, and sort rows in the dataframe. We can check if a value exists in the index using the "in" keyword. The "in" keyword checks if the value is present in the index labels and returns a boolean value.

Here's an example to demonstrate the same:


```python
import pandas as pd

# Create a new dataframe with index values
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]}, index=['X', 'Y', 'Z'])

# Check if 'Y' exists in the index
print('Y' in df.index) # True

# Check if 'W' exists in the index
print('W' in df.index) # False
```

Output:
```
True
False
```


## Section 3: Using the isin() method

We can also use the isin() method to check if a value exists in the index. The isin() method is a pandas dataframe method that returns a boolean mask, which can be used to filter out rows based on the specified values.

Here's an example to demonstrate the same:


```python
import pandas as pd

# Create a new dataframe with index values
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]}, index=['X', 'Y', 'Z'])

# Use isin() method to check if 'X' and 'Y' exist in the index
print(df.index.isin(['X', 'Y'])) # Output: [ True  True False]
```

Output:
```
[ True  True False]
```


## Section 4: Conclusion

In this tutorial, we have seen how to check if a value exists in a pandas dataframe index using the "in" keyword and the isin() method. The "in" keyword returns a boolean value, while the isin() method returns a boolean mask that can be used to filter rows.
