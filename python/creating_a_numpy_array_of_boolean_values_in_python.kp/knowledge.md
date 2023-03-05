---
title: What is the method to produce a numpy array consisting entirely of true or false values?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the np.ones() function with dtype=bool to create an array of all True or np.zeros() function with dtype=bool to create an array of all False.
---

**Contents**

[TOC]

# Using np.ones() and np.zeros() functions
You can create a numpy array of all True or all False by using the np.ones() and np.zeros() functions that create arrays of all ones or zeros respectively. By casting them to boolean dtype, the arrays will become arrays of all True or all False.

```python
import numpy as np

# creating a numpy array of all True
arr_true = np.ones((5,), dtype=bool)
print(arr_true)

# creating a numpy array of all False
arr_false = np.zeros((5,), dtype=bool)
print(arr_false)
```

Output:
```
[ True  True  True  True  True]
[False False False False False]
```


# Using np.full() function
Another way to create a numpy array of all True or all False is by using the np.full() function which fills the array with a scalar value. 

```python
import numpy as np

# creating a numpy array of all True
arr_true = np.full((5,), True, dtype=bool)
print(arr_true)

# creating a numpy array of all False
arr_false = np.full((5,), False, dtype=bool)
print(arr_false)
```

Output:
```
[ True  True  True  True  True]
[False False False False False]
```


# Using np.array() with Python's Boolean data type
You can create a numpy array of all True or all False by simply creating a Python list of all True or all False and passing it to the np.array() function. 

```python
import numpy as np

# creating a numpy array of all True
arr_true = np.array([True] * 5)
print(arr_true)

# creating a numpy array of all False
arr_false = np.array([False] * 5)
print(arr_false)
```

Output:
```
[ True  True  True  True  True]
[False False False False False]
```


# Using np.tile() and np.bool_() functions
Finally, you can create a numpy array of all True or all False by using the np.tile() function to construct a 1D array filled with True/False values and then by casting it to boolean data type using np.bool_() function.

```python
import numpy as np

# creating a numpy array of all True
arr_true = np.tile(np.bool_(True), 5)
print(arr_true)

# creating a numpy array of all False
arr_false = np.tile(np.bool_(False), 5)
print(arr_false)
```

Output:
```
[ True  True  True  True  True]
[False False False False False]
```
