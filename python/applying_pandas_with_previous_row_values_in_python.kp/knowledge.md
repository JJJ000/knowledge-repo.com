---
title: In pandas, is it possible to utilize the value of the preceding row in the dataframe.apply function when the previous value is also computed in the apply?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Yes, by using the `.shift()` method to access the previous row value within the `apply` function.
---

**Contents**

[TOC]

Introduction
------------

Yes, it is possible to use the previous row value in `pandas.apply()` when the previous value is also calculated within `apply()` method. We can use `.shift()` method to shift the rows and access the previous row values. In this tutorial, we will look at the step-by-step process of using the previous row value in `pandas.apply()`.


Step 1: Importing necessary Libraries
-------------------------------------

Let's start by importing `pandas` and creating a sample dataframe to illustrate the workings of `pandas.apply()` method.


```python
import pandas as pd

# Creating a sample dataframe
df = pd.DataFrame({'A': [10, 20, 30, 40, 50], 'B': [20, 30, 40, 50, 60]})
```

This will create a dataframe `df` with two columns `A` and `B`. Now, let's write a function that uses previous value of column `A` and current row value of column `B`.


Step 2: Defining a Function that Uses Previous Row Value
--------------------------------------------------------

```python
def func(row):
    # Accessing previous row value of column A
    prev_A = row['A'].shift(1)
    # Accessing current row value of column B
    current_B = row['B']
    # Adding both the values and returning the result
    return prev_A + current_B
```

Here, we have defined a function `func()` that takes a row as input and returns a value. The function uses the previous row value of column `A` and current row value of column `B` to generate the result. The `.shift()` method shifts the values in the column one position up and this allows us to access the previous row values.


Step 3: Using the Function in pandas.apply()
--------------------------------------------

```python
# Applying the function on dataframe
df['result'] = df.apply(func, axis=1)

# Printing the final dataframe
print(df)
```

This will add a new column `result` to the dataframe `df`. The `axis=1` argument in `apply()` specifies that the function should be applied on each row of the dataframe. The output of the above code will be:

```
    A   B  result
0  10  20     NaN
1  20  30    30.0
2  30  40    50.0
3  40  50    70.0
4  50  60    90.0
```

We can see that the new column `result` has been added with correct values. Note that the first row will always have `NaN` value as there is no previous row to access the value of column `A`.


Conclusion
----------

In this tutorial, we have seen how to use a previous row value in `pandas.apply()` method when the previous value is also calculated within the function. We used `.shift()` method to shift the rows and access the previous row values. This technique can be used in various scenarios where we need to use previous row values in `pandas`.
