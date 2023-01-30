---
title: Transform a list of dictionaries into a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the pandas DataFrame constructor and pass in the list of dictionaries as the data parameter.
---

**Contents**

[TOC]

### Section 1: Import pandas library

Before you can convert a list of dictionaries to a pandas DataFrame, you must first import the pandas library.

```python
import pandas as pd
```

### Section 2: Create list of dictionaries

Next, create a list of dictionaries. For example:

```python
data = [{'name': 'John', 'age': 20},
        {'name': 'Jane', 'age': 30},
        {'name': 'Bob', 'age': 40}]
```

### Section 3: Convert to DataFrame

Now, you can convert the list of dictionaries to a pandas DataFrame using the `pd.DataFrame()` method.

```python
df = pd.DataFrame(data)
```

### Section 4: View DataFrame

Finally, you can view the DataFrame using the `df.head()` method.

```python
df.head()
```

This will return the following DataFrame:

| name | age |
|------|-----|
| John | 20  |
| Jane | 30  |
| Bob  | 40  |
