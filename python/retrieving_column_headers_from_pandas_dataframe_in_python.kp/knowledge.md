---
title: Retrieve the column names from a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can get a list from Pandas DataFrame column headers in Python by using the DataFrame`s `columns` attribute.
---

**Contents**

[TOC]

**Section 1: Getting the Column Headers**

The column headers can be retrieved from a Pandas DataFrame by using the `columns` attribute. The `columns` attribute returns a list of the column names in the DataFrame. 

```python
import pandas as pd

# Create a DataFrame
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6], 'C': [7, 8, 9]})

# Get the column headers
column_headers = df.columns

# Print the column headers
print(column_headers)

# Output: Index(['A', 'B', 'C'], dtype='object')
```

**Section 2: Accessing the List Values**

Once the column headers have been retrieved, the list values can be accessed using the `list` method. The `list` method returns a list of the column names in the DataFrame. 

```python
import pandas as pd

# Create a DataFrame
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6], 'C': [7, 8, 9]})

# Get the column headers
column_headers = df.columns

# Get the list of column headers
column_headers_list = column_headers.tolist()

# Print the list of column headers
print(column_headers_list)

# Output: ['A', 'B', 'C']
```

**Section 3: Iterating through the List**

The list of column headers can also be iterated through using a `for` loop. This allows for the values to be accessed individually. 

```python
import pandas as pd

# Create a DataFrame
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6], 'C': [7, 8, 9]})

# Get the column headers
column_headers = df.columns

# Iterate through the list of column headers
for header in column_headers:
    print(header)

# Output:
# A
# B
# C
```

**Section 4: Sorting the List**

The list of column headers can be sorted using the `sorted` function. This allows for the values to be sorted in alphabetical or numerical order. 

```python
import pandas as pd

# Create a DataFrame
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6], 'C': [7, 8, 9]})

# Get the column headers
column_headers = df.columns

# Sort the list of column headers
sorted_column_headers = sorted(column_headers)

# Print the sorted list of column headers
print(sorted_column_headers)

# Output: ['A', 'B', 'C']
```
