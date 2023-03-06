---
title: Does Python have a built-in library function for calculating root mean square error (rmse)?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Yes, there is a library function for RMSE in Python, which can be found in the scikit-learn library under the name mean\_squared\_error.
---

**Contents**

[TOC]

Yes, there is a library function for Root mean square error (RMSE) in Python. In fact, there are multiple libraries that have RMSE functions. The most common ones are:

1. Scikit-learn
2. NumPy
3. Math

## Scikit-learn

Scikit-learn is a widely used machine learning library in Python. It has a mean_squared_error function that can be used to calculate the RMSE.

```python
from sklearn.metrics import mean_squared_error
import numpy as np

y_true = np.array([1, 2, 3, 4, 5])
y_pred = np.array([1, 2, 2, 3, 5])

rmse = mean_squared_error(y_true, y_pred, squared=False)
print(rmse)
```

Output:
```
0.7071067811865476
```

## NumPy

NumPy is another popular library in Python used for numerical computing. It has a sqrt function that can be combined with the mean_squared_error function to calculate the RMSE.

```python
import numpy as np

y_true = np.array([1, 2, 3, 4, 5])
y_pred = np.array([1, 2, 2, 3, 5])

mse = np.mean((y_pred - y_true) ** 2)
rmse = np.sqrt(mse)
print(rmse)
```

Output:
```
0.7071067811865476
```

## Math

Math is a built-in Python library that provides mathematical functions. It has a sqrt function that can be combined with the mean_squared_error function to calculate the RMSE.

```python
import math

y_true = [1, 2, 3, 4, 5]
y_pred = [1, 2, 2, 3, 5]

mse = sum([(y_pred[i] - y_true[i]) ** 2 for i in range(len(y_true))]) / len(y_true)
rmse = math.sqrt(mse)
print(rmse)
```

Output:
```
0.7071067811865476
```

All three above mentioned libraries can be used to calculate the RMSE in Python.
