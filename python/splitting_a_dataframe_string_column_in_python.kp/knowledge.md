---
title: What is the best way to divide a dataframe string column into two separate columns?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the str.split() method to split the string column into two separate columns.
---

**Contents**

[TOC]

**Section 1: Import Dependencies**

```python
import pandas as pd
```

**Section 2: Create Sample Dataframe**

```python
# Create a sample dataframe
df = pd.DataFrame({'Name': ['John Smith', 'Jane Doe', 'Joe Schmo'],
                   'Age': [30, 40, 50]})
```

**Section 3: Split Column**

```python
# Split the Name column into two columns
df[['First Name', 'Last Name']] = df.Name.str.split(' ', expand=True)
```

**Section 4: View Results**

```python
# View the resulting dataframe
df
```

```
      Name  Age First Name Last Name
0  John Smith   30       John     Smith
1    Jane Doe   40       Jane       Doe
2   Joe Schmo   50        Joe     Schmo
```
