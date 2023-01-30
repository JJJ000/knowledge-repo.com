---
title: Merge two columns of text in a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: You can use the str.cat() function to combine two columns of text in a pandas dataframe.
---

**Contents**

[TOC]

**Section 1: Import Libraries**

```python
import pandas as pd
```

**Section 2: Create Dataframe**

```python
data = {'Name':['John','Paul','George','Ringo'],
        'City':['London','Liverpool','Liverpool','London']}

df = pd.DataFrame(data)

print(df)
```

**Section 3: Combine Two Columns**

```python
df['Name_City'] = df['Name'] + '_' + df['City']

print(df)
```

**Section 4: Output**

```python
    Name      City      Name_City
0   John     London    John_London
1   Paul     Liverpool Paul_Liverpool
2   George   Liverpool George_Liverpool
3   Ringo    London    Ringo_London
```
