---
title: Transforming an integer column in a pandas dataframe into a string format
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the astype() function with str as the parameter to convert a column from int to string in a pandas dataframe.
---

**Contents**

[TOC]

Section 1: Introduction
In this tutorial, we will discuss how to convert a column within pandas dataframe from int to string in Python.

Section 2: Sample Data
As a first step, let's create a sample dataframe to demonstrate the conversion process.

```
import pandas as pd

# sample data
data = {'A': [1, 2, 3, 4, 5],
       'B': [10, 20, 30, 40, 50]}

df = pd.DataFrame(data)
print(df)
```
Output:
```
   A   B
0  1  10
1  2  20
2  3  30
3  4  40
4  5  50
```

Section 3: Converting Column from int to string
Now, let's convert column 'A' from int to string.

```
df['A'] = df['A'].astype(str)
```

The astype() method is used to cast a pandas object to a specified dtype. In this case, we are converting the column 'A' to a string data type.

Section 4: Output
Finally, let's print the updated dataframe to see the conversion.

```
print(df)
```
Output:
```
   A   B
0  1  10
1  2  20
2  3  30
3  4  40
4  5  50
``` 

As we can see from the output, column 'A' has been successfully converted from int to string.
