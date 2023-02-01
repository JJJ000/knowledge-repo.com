---
title: What is the method for determining if a pandas dataframe is empty?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: To check if a pandas DataFrame is empty, use the .empty attribute.
---

**Contents**

[TOC]

### Using the `empty` Attribute

Pandas DataFrames have an `empty` attribute that can be used to determine whether the DataFrame is empty or not. This attribute returns a boolean value (True or False) depending on whether the DataFrame is empty or not.

Example:

```python
import pandas as pd

# Create an empty DataFrame
df = pd.DataFrame()

# Check if the DataFrame is empty
print(df.empty)
```

Output:

`True`

### Using the `shape` Attribute

The `shape` attribute of a Pandas DataFrame can also be used to determine whether the DataFrame is empty or not. If the DataFrame is empty, then the `shape` attribute will return a tuple of (0, 0).

Example:

```python
import pandas as pd

# Create an empty DataFrame
df = pd.DataFrame()

# Check if the DataFrame is empty
print(df.shape == (0, 0))
```

Output:

`True`

### Using the `size` Attribute

The `size` attribute of a Pandas DataFrame can also be used to determine whether the DataFrame is empty or not. If the DataFrame is empty, then the `size` attribute will return 0.

Example:

```python
import pandas as pd

# Create an empty DataFrame
df = pd.DataFrame()

# Check if the DataFrame is empty
print(df.size == 0)
```

Output:

`True`

### Using the `len` Function

The built-in `len` function can also be used to determine whether the DataFrame is empty or not. If the DataFrame is empty, then the `len` function will return 0.

Example:

```python
import pandas as pd

# Create an empty DataFrame
df = pd.DataFrame()

# Check if the DataFrame is empty
print(len(df) == 0)
```

Output:

`True`
