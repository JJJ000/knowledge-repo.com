---
title: Create a correlation matrix of the data using pandas
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Pandas can be used to plot a correlation matrix using the .corr() method on a DataFrame.
---

**Contents**

[TOC]

**Section 1: Set Up**

To create a correlation matrix using pandas, we need to first import the necessary packages and create a dataframe. 

```python
import pandas as pd
import numpy as np

df = pd.DataFrame({'A': [1,2,3,4,5],
                   'B': [2,3,4,5,6],
                   'C': [3,4,5,6,7],
                   'D': [4,5,6,7,8]})
```

**Section 2: Calculate Correlation Matrix**

Once the dataframe is created, we can calculate the correlation matrix using the corr() method.

```python
corrMatrix = df.corr()
```

**Section 3: Visualize Correlation Matrix**

We can then visualize the correlation matrix using the heatmap() method from the seaborn package.

```python
import seaborn as sns
sns.heatmap(corrMatrix, annot=True)
```

**Section 4: Output**

The output of the above code is a heatmap of the correlation matrix, which can be seen below.

![Correlation Matrix](correlation_matrix.png)
