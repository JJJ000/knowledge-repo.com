---
title: What is the method for obtaining the magnitude of a vector in numpy?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the numpy.linalg.norm() function to get the magnitude of a vector in Numpy in Python.
---

**Contents**

[TOC]

Section 1: Import Numpy package
Before we can use any of the functions in Numpy package, we need to first import it. We can do that using the import statement.

```python
 import numpy as np
```

Section 2: Define the vector
We can define our vector using the np.array() function. In this example, we will define a vector with x, y and z components. 

```python
v = np.array([4, 3, 2])
```

Section 3: Calculate the magnitude of vector
We can use the np.linalg.norm() function to calculate the magnitude, also known as the norm of the vector. This function takes the vector v as the input argument and returns the magnitude of the vector. 

```python
magnitude = np.linalg.norm(v)
```

Section 4: Print the magnitude of vector
Finally, we can print the magnitude of the vector to the console using the print() function.

```python
print(magnitude)
```

The complete code snippet would look like:


```python
import numpy as np

v = np.array([4, 3, 2])
magnitude = np.linalg.norm(v)

print(magnitude)
```
