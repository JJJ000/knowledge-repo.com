---
title: Retrieve several columns using pandas apply()
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: To return multiple columns from pandas apply(), return a pandas Series with multiple values separated by commas.
---

**Contents**

[TOC]

Section 1: Introduction
Pandas apply() function is a powerful tool for manipulating data in a DataFrame. It allows you to apply a function to each row or column of the DataFrame, and return a single value. However, there are times when you may want to return multiple values from the applied function. In this guide, we will explore how to return multiple columns from pandas apply() in Python.

Section 2: Using pandas apply() to return multiple columns
The first step to returning multiple columns from pandas apply() is to create a function that returns a Series object. The Series object will contain the values for each of the columns you want to return. Here's an example function that returns the square and cube of a number:

```
import pandas as pd

def square_cube(x):
    return pd.Series([x**2, x**3])
```

Once you have your function that returns a Series object, you can use apply() to apply the function to each row or column of your DataFrame. Here's an example of applying the function to a column in a DataFrame:

```
df = pd.DataFrame({'numbers': [1, 2, 3, 4, 5]})
df[['square', 'cube']] = df['numbers'].apply(square_cube)
```

In this example, we create a new DataFrame with a 'numbers' column that contains the numbers 1-5. We then use apply() to apply the square_cube() function to each value in the 'numbers' column. We assign the resulting Series object to two new columns in the DataFrame, 'square' and 'cube'. 

Section 3: Using pandas apply() with lambda functions
Another way to return multiple columns from pandas apply() is to use lambda functions. Lambda functions are anonymous functions that can be defined in one line of code. Here's an example of a lambda function that returns the square and cube of a number:

```
square_cube = lambda x: pd.Series([x**2, x**3])

df = pd.DataFrame({'numbers': [1, 2, 3, 4, 5]})
df[['square', 'cube']] = df['numbers'].apply(square_cube)
```

In this example, we define the square_cube lambda function in one line of code. We then use apply() to apply the lambda function to each value in the 'numbers' column of our DataFrame. We assign the resulting Series object to two new columns in the DataFrame, 'square' and 'cube'. 

Section 4: Conclusion
In this guide, we've explored how to return multiple columns from pandas apply() in Python. We've shown examples of using apply() with functions that return a Series object, as well as using lambda functions. With these techniques, you can add new columns to your DataFrame based on the values in existing columns.
