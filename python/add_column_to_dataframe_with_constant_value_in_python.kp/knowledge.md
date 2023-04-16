---
title: Create a new column in the dataframe with a fixed value
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can add a column to a dataframe with a constant value by using the df.assign() method.
---

**Contents**

[TOC]

**Section 1: Creating the Dataframe**

We can create a dataframe from a dictionary of lists, like so:

```python
import pandas as pd 

data = {'Name':['John', 'Paul', 'George', 'Ringo'], 
        'Age':[20, 21, 22, 23]
       }
 
df = pd.DataFrame(data) 

print(df)
```

This will produce the following output:

| Name | Age |
|------|-----|
| John | 20  |
| Paul | 21  |
| George | 22 |
| Ringo | 23  |

**Section 2: Adding the Column**

We can add a column to the dataframe with a constant value using the ```assign()``` method, like so:

```python
df = df.assign(Gender='Male')

print(df)
```

This will produce the following output:

| Name | Age | Gender |
|------|-----|--------|
| John | 20  | Male   |
| Paul | 21  | Male   |
| George | 22 | Male   |
| Ringo | 23  | Male   |

**Section 3: Using a List**

Alternatively, we can use a list to add a column with a constant value, like so:

```python
df['Gender'] = ['Male'] * len(df)

print(df)
```

This will produce the same output as before:

| Name | Age | Gender |
|------|-----|--------|
| John | 20  | Male   |
| Paul | 21  | Male   |
| George | 22 | Male   |
| Ringo | 23  | Male   |

**Section 4: Using a Dictionary**

We can also use a dictionary to add a column with a constant value, like so:

```python
df['Gender'] = {'Gender': 'Male'}

print(df)
```

This will again produce the same output:

| Name | Age | Gender |
|------|-----|--------|
| John | 20  | Male   |
| Paul | 21  | Male   |
| George | 22 | Male   |
| Ringo | 23  | Male   |
