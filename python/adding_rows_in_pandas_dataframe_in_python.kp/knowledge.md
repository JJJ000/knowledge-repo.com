---
title: Add a row to a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To insert a row to a pandas dataframe in Python, use the `loc` method and assign the new values for the row.
---

**Contents**

[TOC]

Creating a sample dataframe
```
import pandas as pd

data = {'Name': ['John', 'Sam', 'Anna'],
        'Age': [25, 30, 35]}

df = pd.DataFrame(data)
print(df)
```

Output:
```
   Name  Age
0  John   25
1   Sam   30
2  Anna   35
```

## Section 1: Adding a row through appending

```
new_row = {'Name':'Maria', 'Age': 28}
df = df.append(new_row, ignore_index=True)
print(df)
```

Output:
```
    Name  Age
0   John   25
1    Sam   30
2   Anna   35
3  Maria   28
```

## Section 2: Adding a row through loc

```
df.loc[len(df)] = ['David', 40]
print(df)
```

Output:
```
    Name  Age
0   John   25
1    Sam   30
2   Anna   35
3  Maria   28
4  David   40
```

## Section 3: Adding a row through dictionary

```
row_dict = {'Name': 'Mark', 'Age': 32}
df = df.append(row_dict, ignore_index=True)
print(df)
```

Output:
```
    Name  Age
0   John   25
1    Sam   30
2   Anna   35
3  Maria   28
4  David   40
5   Mark   32
```
