---
title: Changing numpy data types to standard Python data types
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Numpy dtypes can be converted to native Python types using the `.item()` method.
---

**Contents**

[TOC]

# Section 1: Converting Numpy dtypes to Native Python Types

Numpy dtypes are the data types used in the numpy library for scientific computing. These data types are used to represent numerical values, strings, and other objects. Numpy dtypes can be converted to native Python types using the `.astype()` method.

# Section 2: Examples

For example, to convert a Numpy array of integers to a Python list of integers, use the following code: 

```python
import numpy as np

# Create a Numpy array
x = np.array([1, 2, 3, 4, 5])

# Convert Numpy array to Python list
y = x.astype(list)

print(y)
# Output: [1, 2, 3, 4, 5]
```

Similarly, to convert a Numpy array of floats to a Python list of floats, use the following code:

```python
import numpy as np

# Create a Numpy array
x = np.array([1.1, 2.2, 3.3, 4.4, 5.5])

# Convert Numpy array to Python list
y = x.astype(list)

print(y)
# Output: [1.1, 2.2, 3.3, 4.4, 5.5]
```

# Section 3: Other Data Types

It is also possible to convert other Numpy data types to native Python types. For example, to convert a Numpy array of strings to a Python list of strings, use the following code:

```python
import numpy as np

# Create a Numpy array
x = np.array(['a', 'b', 'c', 'd', 'e'])

# Convert Numpy array to Python list
y = x.astype(list)

print(y)
# Output: ['a', 'b', 'c', 'd', 'e']
```

# Section 4: Conclusion

In conclusion, the `.astype()` method can be used to convert Numpy dtypes to native Python types. This is a useful tool for data manipulation and data analysis.
