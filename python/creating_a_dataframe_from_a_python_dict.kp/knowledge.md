---
title: Transform a Python dictionary into a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can convert a Python dict into a dataframe by using the pandas DataFrame() constructor.
---

**Contents**

[TOC]

##### Section 1: Import Libraries

```python
import pandas as pd
```

##### Section 2: Create Dictionary

```python
data = {'Name': ['John', 'Paul', 'George', 'Ringo'], 
        'Age': [30, 33, 31, 28],
        'Occupation': ['Engineer', 'Doctor', 'Musician', 'Musician']}
```

##### Section 3: Convert Dictionary to DataFrame

```python
df = pd.DataFrame(data)
```

##### Section 4: View DataFrame

```python
df
```

|    | Name   | Age  | Occupation |
|---:|:-------|:-----|:-----------|
|  0 | John   | 30   | Engineer   |
|  1 | Paul   | 33   | Doctor     |
|  2 | George | 31   | Musician   |
|  3 | Ringo  | 28   | Musician   |
