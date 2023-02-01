---
title: What is the process for utilizing a function on two columns of a pandas dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the DataFrame.apply() method to apply a function to two columns of a Pandas dataframe.
---

**Contents**

[TOC]

**Section 1: Importing pandas library**

We need to import the pandas library to use the dataframe object.

```python
import pandas as pd
```

**Section 2: Creating the dataframe**

We can create a dataframe with two columns using the following code:

```python
df = pd.DataFrame({'col1':[1,2,3], 'col2':[4,5,6]})
```

**Section 3: Defining the function**

We can define a function that we want to apply to the dataframe:

```python
def my_func(x, y):
    return x + y
```

**Section 4: Applying the function**

We can apply the function to the two columns of the dataframe using the following code:

```python
df['result'] = df.apply(lambda row: my_func(row['col1'], row['col2']), axis=1)
```
