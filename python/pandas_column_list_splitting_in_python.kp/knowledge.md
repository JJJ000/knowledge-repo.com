---
title: Divide a pandas column containing lists into separate columns
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the `explode` function to split a Pandas column of lists into multiple columns.
---

**Contents**

[TOC]

#### Section 1: Creating the DataFrame

We can create a DataFrame in pandas using the `pd.DataFrame()` method. This method takes a dictionary of lists as an argument.

```python
import pandas as pd

data = {'name':['John', 'Jane', 'Jack'], 
        'age':[[20, 21], [22, 23], [24, 25]],
        'score':[[90, 95], [80, 85], [70, 75]]}

df = pd.DataFrame(data)
```

#### Section 2: Exploring the DataFrame

The DataFrame we have created looks like this:

```
    name    age        score
0   John    [20, 21]   [90, 95]
1   Jane    [22, 23]   [80, 85]
2   Jack    [24, 25]   [70, 75]
```

#### Section 3: Splitting the Column

We can use the `pd.DataFrame.explode()` method to split the column of lists into multiple columns.

```python
df_split = df.explode('age')
```

The `explode()` method takes the name of the column of lists as an argument.

#### Section 4: Examining the Result

The resulting DataFrame looks like this:

```
    name    age    score
0   John    20     90
0   John    21     95
1   Jane    22     80
1   Jane    23     85
2   Jack    24     70
2   Jack    25     75
```

The column of lists has been split into multiple columns.
