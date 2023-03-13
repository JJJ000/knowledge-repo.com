---
title: What is the procedure to eliminate nan values from a list in python/numpy?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: You can use the NumPy method `numpy.isnan()` to create a boolean mask of the array and then pass this mask to the original array to remove any NaN values.
---

**Contents**

[TOC]

## Identify the NaN values

The first step in removing NaN values from a list in Python/NumPy is to identify them. We can use the isna() function from the pandas library to check if a value is NaN or not. Alternatively, if we are working with arrays, we can use the isnan() function from the NumPy library.


## Remove the NaN values

Once we have identified the NaN values, we can remove them from the list using various methods. One common approach is to use the dropna() function provided by pandas. This function removes all the rows or columns with NaN values based on the axis parameter. We can also use the fillna() function to replace NaN values with a specific value.


## Example code

Here is an example code that demonstrates how to remove NaN values from a list using the pandas library:

```
import pandas as pd 

# create a list with NaN values
mylist = [1, 2, 3, float('nan'), 5, 6, float('nan'), 8]

# convert the list to a pandas series
s = pd.Series(mylist)

# identify and remove the NaN values
clean_list = s.dropna()

print(clean_list)
```

Output:
```
0    1.0
1    2.0
2    3.0
4    5.0
5    6.0
7    8.0
dtype: float64
```

In this example, we used the dropna() function to remove the NaN values from the list. We converted the list to a pandas series first and then applied the dropna() function on it. The function removed two NaN values from the list, and the resulting series had six elements.


## Conclusion

Removing NaN values from a list in Python/NumPy is a simple task that can be achieved using various methods. We first need to identify the NaN values and then remove them using appropriate functions. The choice of function depends on the type of data structure we are working with and the specific requirements of the problem.
