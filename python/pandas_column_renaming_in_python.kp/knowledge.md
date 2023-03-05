---
title: Change the name of particular column(s) in pandas
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: To rename specific column(s) in pandas in Python, use the `rename()` method with a dictionary of old and new column names.
---

**Contents**

[TOC]

**Section 1: Introduction**

In Pandas, we can easily rename specific columns of a DataFrame. Renaming columns is essential when we need to replace the default column names with something more meaningful, or when we need to change the names of columns to fit our analysis needs.



**Section 2: Renaming a Single Column using rename() method**

The `rename()` method in Pandas provides a straightforward way to rename columns. Here's how we can use it to rename a single column:

```
# Import pandas
import pandas as pd

# Create a sample DataFrame
df = pd.DataFrame({'name': ['John', 'Sara', 'Peter'], 'age': [25, 28, 19]})

# Rename the 'name' column to 'full_name'
df = df.rename(columns={'name': 'full_name'})
```

In the above example, `rename(columns={'name': 'full_name'})` renames the column `name` to `full_name`. The `columns` parameter takes a dictionary where the keys are the old column names, and the values are the new column names.



**Section 3: Renaming Multiple Columns using rename() method**

We can also rename multiple columns in Pandas using the `rename()` method. We pass a dictionary with the old and new column names as key-value pairs to the `rename()` method. Here's an example:

```
# Import pandas
import pandas as pd

# Create a sample DataFrame
df = pd.DataFrame({'first_name': ['John', 'Sara', 'Peter'], 'last_name': ['Doe', 'Smith', 'Jones'], 'age': [25, 28, 19]})

# Rename the 'first_name' and 'last_name' columns to 'name' and 'surname'
df = df.rename(columns={'first_name': 'name', 'last_name': 'surname'})
```

In the above example, `rename(columns={'first_name': 'name', 'last_name': 'surname'})` renames the column `first_name` to `name` and `last_name` to `surname`.



**Section 4: inplace Parameter**

The `rename()` method in Pandas returns a new DataFrame with the new column names. If we want to modify the original DataFrame, we can use the `inplace` parameter. Here's an example:

```
# Import pandas
import pandas as pd

# Create a sample DataFrame
df = pd.DataFrame({'first_name': ['John', 'Sara', 'Peter'], 'last_name': ['Doe', 'Smith', 'Jones'], 'age': [25, 28, 19]})

# Modify the 'first_name' and 'last_name' columns to 'name' and 'surname' inplace
df.rename(columns={'first_name': 'name', 'last_name': 'surname'}, inplace=True)
```

In the above example, `rename(columns={'first_name': 'name', 'last_name': 'surname'}, inplace=True)` modifies the original DataFrame with the new column names. We set `inplace=True`, so the original DataFrame gets modified, and there's no need to assign the result back to the DataFrame.
