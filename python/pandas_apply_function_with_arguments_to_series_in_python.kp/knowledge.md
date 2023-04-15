---
title: How can a function with arguments be applied to a series in Python pandas?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the `apply()` method on the series and pass the function name and arguments as arguments to the `apply()` method.
---

**Contents**

[TOC]

## Introduction
In python pandas, `apply()` is a powerful function that is used to apply a function to a series or a dataframe. In this tutorial, we will learn how to apply a function with arguments to a pandas series.

## Creating Function with Arguments
To apply a function with arguments to a pandas series, we need to first create the function with the arguments. Here is an example of a function that takes two arguments:

```python
def square_sum(x, y):
    return (x**2) + (y**2)
```

## Applying Function with Arguments to a Series
Once you have defined the function with arguments, you can apply it to a pandas series using the `apply()` function. Here is an example:

```python
import pandas as pd
df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})
df['C'] = df.apply(lambda x: square_sum(x['A'], x['B']), axis=1)
print(df)
```

Output:
```
   A  B  C
0  1  4  17
1  2  5  29
2  3  6  45
```

In this example, we first create a pandas dataframe with two columns `A` and `B`. We then use the `apply()` function to apply the `square_sum()` function to each row of the dataframe. The `axis=1` argument tells pandas to apply the function row-wise. The resulting output is a new column `C` added to the dataframe.

## Conclusion
In this tutorial, we learned how to apply a function with arguments to a pandas series using the `apply()` function. First, we created a function with arguments and then we applied it to a pandas series using the `apply()` function. We also saw how to apply the function row-wise using the `axis=1` argument.
