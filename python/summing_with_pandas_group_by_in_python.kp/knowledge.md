---
title: What is the syntax for using pandas group-by to calculate a sum?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: To get the sum of a group using Pandas, use the groupby() function followed by the sum() function.
---

**Contents**

[TOC]

### Step 1: Import Pandas

In order to use Pandas for group-by sum, you must first import it.

```python
import pandas as pd
```

### Step 2: Create DataFrame

Next, create a DataFrame with the data that you want to group-by and sum.

```python
data = {'name': ['John', 'John', 'John', 'Paul', 'Paul', 'Paul'],
        'score': [1, 2, 3, 4, 5, 6]}

df = pd.DataFrame(data)
```

### Step 3: Group-By and Sum

Finally, use the `groupby` and `sum` functions to group-by and sum the data in the DataFrame.

```python
df.groupby('name').sum()
```

### Step 4: View Results

The results of the group-by and sum will be shown in a new DataFrame.

```python
   score
name     
John    6
Paul   15
```
