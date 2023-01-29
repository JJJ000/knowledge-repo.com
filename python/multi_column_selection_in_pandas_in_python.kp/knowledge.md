---
title: Retrieving multiple columns from a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the DataFrame.loc or DataFrame.iloc methods to select multiple columns from a Pandas dataframe.
---

**Contents**

[TOC]

#### Section 1: Importing Packages

```python
import pandas as pd
```

#### Section 2: Creating Dataframe

```python
data = {'Name':['Tom', 'nick', 'krish', 'jack'],
        'Age':[20, 21, 19, 18]} 

df = pd.DataFrame(data) 
```

#### Section 3: Selecting Multiple Columns

```python
# Selecting multiple columns using a list of column names 
selected_columns = df[['Name', 'Age']] 

# Print dataframe 
print(selected_columns)
```

#### Section 4: Output

```
   Name  Age
0   Tom   20
1  nick   21
2  krish   19
3  jack   18
```
