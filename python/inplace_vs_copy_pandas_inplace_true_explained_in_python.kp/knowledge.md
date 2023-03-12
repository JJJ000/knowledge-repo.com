---
title: Rewording a comprehensive comprehension of the concept of inplace=true in pandas
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Inplace=True in pandas modifies the original DataFrame instead of creating a new one.
---

**Contents**

[TOC]

## Introduction
The pandas library in Python is a powerful tool for data analysis, manipulation, and visualization. One of the key features of pandas is its ability to modify data in place using the inplace parameter. In this article, we will explore the concept of inplace=True in pandas and discuss its uses.

## What is inplace=True in pandas?
By default, when we apply any method in pandas, it returns a new DataFrame or a new Series. It means that the original DataFrame/Series is not modified. However, the inplace parameter allows us to modify the original DataFrame or Series directly. Setting inplace=True tells pandas to modify the original object instead of returning a new one. 

## Example
Let's demonstrate the use of inplace=True with an example. Consider the following DataFrame:

```
import pandas as pd
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})
df
```

Output:
```
   A  B
0  1  4
1  2  5
2  3  6
```

Suppose we want to add a new column 'C' to this DataFrame. We could do this by creating a new column and assigning it to the DataFrame, like this:

```
df['C'] = df['A'] + df['B']
df
```

Output:
```
   A  B  C
0  1  4  5
1  2  5  7
2  3  6  9
```

Alternatively, we can use inplace=True to modify the original DataFrame directly:

```
df['C'] = df['A'] + df['B']
df.drop(columns=['C'], inplace=True)
df
```

Output:
```
   A  B
0  1  4
1  2  5
2  3  6
```

Note that we first added a new column 'C' and then dropped it using inplace=True. This modified the original DataFrame directly.

## Conclusion
In summary, the inplace parameter in pandas is used to modify the original DataFrame or Series directly instead of creating a new one. This can be useful for performance reasons or when we want to chain multiple operations in a single line of code. However, we need to be careful when using inplace=True to avoid accidentally modifying the original data.
