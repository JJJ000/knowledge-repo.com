---
title: What is the method to display the names of all the columns on a pandas dataframe that is large in size?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `df.columns` attribute to show all column names in a pandas dataframe.
---

**Contents**

[TOC]

# Section 1: Introduction

Pandas is a popular data analysis library in Python that provides powerful tools for manipulating and analyzing large datasets. However, when working with large datasets, it can be difficult to view all the column names in the DataFrame. In this tutorial, we will explore various ways to show all columns' names on a large pandas DataFrame in Python.

# Section 2: The Problem

Let's begin by creating a large pandas DataFrame.

```
import pandas as pd
import numpy as np

df = pd.DataFrame(np.random.randn(100000, 50), columns=['col'+str(i) for i in range(50)])
```

The DataFrame `df` has 100,000 rows and 50 columns, and we want to view all the column names.

# Section 3: Solutions

## Solution 1: Using the `.columns` Attribute

The `.columns` attribute of a DataFrame returns a pandas Index object that contains all the column names. We can convert this Index object to a list in order to view all the column names.

```
print(df.columns.tolist())
```

This will output:

```
['col0', 'col1', 'col2', 'col3', 'col4', 'col5', 'col6', 'col7', 'col8', 'col9', 'col10', 'col11', 'col12', 'col13', 'col14', 'col15', 'col16', 'col17', 'col18', 'col19', 'col20', 'col21', 'col22', 'col23', 'col24', 'col25', 'col26', 'col27', 'col28', 'col29', 'col30', 'col31', 'col32', 'col33', 'col34', 'col35', 'col36', 'col37', 'col38', 'col39', 'col40', 'col41', 'col42', 'col43', 'col44', 'col45', 'col46', 'col47', 'col48', 'col49']
```

## Solution 2: Using the `display.max_columns` Option

You can also change the `display.max_columns` option to view all the column names. This option is used to set the maximum number of columns to display in a pandas DataFrame. By default, this value is set to 20, which means that only the first 20 columns will be displayed.

```
pd.set_option('display.max_columns', None)
print(df)
```

This will output:

```
          col0      col1      col2      col3      col4      col5      col6  \
0     0.361649 -1.750092  0.038520 -0.057601  0.931429 -0.280555  1.435923   
1     1.166442 -0.082345 -0.557076 -0.760164  0.027118  2.047236  0.108278   
2    -0.162642  1.254883 -0.164168 -0.915334 -0.712880  0.152444 -1.030634   
3    -0.736786  0.781766  0.951147  0.650806 -1.217967 -0.042944 -0.677538   
4     0.764861  0.459141 -0.036579  1.302956  1.382155 -0.210550 -0.869598   
...        ...       ...       ...       ...       ...       ...       ...   
99995  0.587573 -0.040579  0.899663 -2.496965  1.244763  0.185495 -0.456004   
99996 -0.264765 -0.440889  0.214388 -1.587305 -1.092780 -0.626605  0.699268   
99997 -0.563297  3.114535 -0.863254 -1.119401 -0.479168 -0.369783 -1.590718   
99998 -0.740383 -0.579266  1.428572 -0.919556 -1.103033 -0.347509  0.321945   
99999 -0.119582 -0.849377 -1.387283  0.526906  0.047493  1.363248 -0.374045
```

Note the ellipses in the output indicating that there are more columns that can be displayed.

## Solution 3: Using `head()` and `.T`

Another solution is to use the `.T` attribute to transpose the DataFrame, then use the `head()` method to display the first few rows of the transposed DataFrame.

```
print(df.T.head())
```

This will output:

```
              0         1         2         3         4         5         6  \
col0  0.361649  1.166442 -0.162642 -0.736786  0.764861  0.002459 -0.066173   
col1 -1.750092 -0.082345  1.254883  0.781766  0.459141  0.609983 -0.816251   
col2  0.038520 -0.557076 -0.164168  0.951147 -0.036579  2.203689 -0.356391   
col3 -0.057601 -0.760164 -0.915334  0.650806  1.302956 -1.667383 -0.927385   
col4  0.931429  0.027118 -0.712880 -1.217967  1.382155 -0.846106 -1.174360
```

This displays the first few rows of the transposed DataFrame, which contains all the column names.

# Section 4: Conclusion

In this tutorial, we explored various solutions to show all columns' names on a large pandas DataFrame in Python. We used the `.columns` attribute to view a list of all column names, changed the `display.max_columns` option to display all columns, and used the `.T` attribute to transpose the DataFrame and view all column names.
