---
title: Use pandas to prepend a string prefix to all values in a column that contains strings
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: You can use the str accessor with the string prefix to concatenate it with the values in a Pandas DataFrame string column.
---

**Contents**

[TOC]

## Load Data

First, we need to import the required libraries and load the data that we want to process.

```python
import pandas as pd

# Load data from CSV file
data = pd.read_csv('file.csv')
```

## Add Prefix to Column

Next, we can use the `apply` method of the Pandas DataFrame to add a prefix to each value in a string column.

```python
# Function to add prefix to a string
def add_prefix(string, prefix):
    return prefix + str(string)

# Add prefix to column 'column_name'
data['column_name'] = data['column_name'].apply(add_prefix, prefix='prefix_')
```

This will add the prefix "prefix_" to each value in the column 'column_name'.

## Save Data

Finally, we can save the updated data to a new file, using the `to_csv` method of the Pandas DataFrame.

```python
# Save updated data to CSV file
data.to_csv('updated_file.csv', index=False)
```

This will save the updated data to a new file called "updated_file.csv", without including the index column.
