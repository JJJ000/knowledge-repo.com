---
title: Select rows from a pandas dataframe using a list of values
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the `.loc` method to select rows from a Pandas dataframe by passing in a list of values.
---

**Contents**

[TOC]

**Section 1: Create a Dataframe**

We can create a Pandas dataframe from a dictionary of lists.

```
import pandas as pd

data = {'Name':['John', 'Paul', 'George', 'Ringo'],
        'Age':[25, 26, 27, 28],
        'Location':['London', 'Liverpool', 'Manchester', 'Birmingham']}

df = pd.DataFrame(data)
print(df)
```

**Section 2: Create a List**

We can create a list of values to select rows from the dataframe.

```
values = ['John', 'Manchester']
```

**Section 3: Select Rows**

We can use the list of values to select rows from the dataframe.

```
selected_rows = df[df['Name'].isin(values) | df['Location'].isin(values)]
print(selected_rows)
```

**Section 4: Result**

The result of the code is the following dataframe.

```
   Name  Age   Location
0  John   25     London
2  George   27  Manchester
```
