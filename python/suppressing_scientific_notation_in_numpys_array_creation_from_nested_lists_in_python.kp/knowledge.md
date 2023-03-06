---
title: Prevent the use of scientific notation in numpy when generating an array via a nested list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `float\_format` argument in the `np.array()` function to suppress scientific notation.
---

**Contents**

[TOC]

Section 1: Introduction
Numpy is a popular Python library used for scientific computing. In Numpy, scientific notation is used to represent very large or very small numbers. However, some users may prefer to suppress scientific notation in their output. This can be accomplished when creating an array from a nested list in Numpy.

Section 2: Using the set_printoptions function
One way to suppress scientific notation in Numpy is to use the set_printoptions function. This function allows you to set various printing options for arrays, including the precision and suppress options. The suppress option can be set to True to suppress scientific notation.

Example code:
```
import numpy as np
np.set_printoptions(suppress=True)

nested_list = [[1.2345678e+08, 2.3456789e-08],
               [3.456789e+07, 4.5678901e-07]]

arr = np.array(nested_list)
print(arr)
```
Output:
```
[[123456780.          0.        ]
 [ 34567890.         0.00000046]]
```

Section 3: Using the astype function to convert to int or float
Another way to suppress scientific notation in Numpy is to convert the array to integers or floats. This can be done using the astype function.

Example code:
```
import numpy as np

nested_list = [[1.2345678e+08, 2.3456789e-08],
               [3.456789e+07, 4.5678901e-07]]

arr = np.array(nested_list).astype(int)
print(arr)
```
Output:
```
[[123456780          0]
 [ 34567890          0]]
```

Section 4: Conclusion
Overall, there are various ways to suppress scientific notation when creating an array from a nested list in Numpy. The set_printoptions function can be used to set the suppress option, while the astype function can be used to convert the array to integers or floats. The best option will depend on the specific use case and desired output.
