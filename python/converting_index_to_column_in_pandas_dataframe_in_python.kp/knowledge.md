---
title: What is the process for transforming an index of a pandas dataframe into a column?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: Use the `reset\_index` method to convert the index of a pandas dataframe into a column.
---

**Contents**

[TOC]

# Section 1: Importing Necessary Libraries

```python
import pandas as pd
```

# Section 2: Creating a Sample DataFrame

```python
# Create a sample dataframe
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})

# Print the dataframe
print(df)
```

Output:

|  A |  B |
|---:|---:|
|  1 |  4 |
|  2 |  5 |
|  3 |  6 |

# Section 3: Converting Index to Column

```python
# Convert the index to a column
df.reset_index(inplace=True) 

# Print the dataframe
print(df)
```

Output:

| index |  A |  B |
|-----:|---:|---:|
|     0 |  1 |  4 |
|     1 |  2 |  5 |
|     2 |  3 |  6 |

# Section 4: Renaming the Column

```python
# Rename the column
df.rename(columns={'index':'new_column'}, inplace=True)

# Print the dataframe
print(df)
```

Output:

| new_column |  A |  B |
|----------:|---:|---:|
|          0 |  1 |  4 |
|          1 |  2 |  5 |
|          2 |  3 |  6 |
