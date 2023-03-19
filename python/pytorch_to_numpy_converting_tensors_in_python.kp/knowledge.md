---
title: Transform pytorch tensor into a numpy array
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: Use the `.numpy()` function to convert a Pytorch tensor to a numpy array in Python.
---

**Contents**

[TOC]

Converting Pytorch Tensor to Numpy Array

Pytorch tensor and numpy array are two important data types used in machine learning and scientific computing. Pytorch tensor is used in deep learning frameworks, while numpy array is used in scientific computing. Sometimes it may be necessary to convert a Pytorch tensor to a numpy array to perform certain operations. This article discusses how to convert a Pytorch tensor to a numpy array in Python.

Section 1: Introduction

In this section, we discuss the differences between Pytorch tensor and numpy array and why you may need to convert Pytorch tensor to numpy array.

Section 2: Converting Pytorch Tensor to Numpy Array

In this section, we discuss the steps involved in converting a Pytorch tensor to a numpy array using the `numpy()` method.

Section 3: Example

In this section, we provide an example of how to convert a Pytorch tensor to a numpy array.

Section 4: Conclusion

In this section, we summarize the article and highlight the key takeaways.

## Section 1: Introduction

Pytorch tensor and numpy array are two popular data types in machine learning and scientific computing. Pytorch tensor is used in deep learning frameworks such as Pytorch, while numpy array is used in scientific computing libraries such as NumPy, Scipy, and Pandas. Pytorch tensors are similar to numpy arrays, but they can be used on GPUs for faster computation. 

Sometimes, you may need to perform operations on a Pytorch tensor that are not supported by the Pytorch library, but are supported by numpy. In such situations, you may need to convert a Pytorch tensor to a numpy array.

## Section 2: Converting Pytorch Tensor to Numpy Array

To convert a Pytorch tensor to a numpy array, you can use the `numpy()` method. This method is available in the Pytorch library and can be used to convert a Pytorch tensor to a numpy array. Here are the steps involved:

1. Import the Pytorch and NumPy libraries.

   ```python
   import torch
   import numpy as np
   ```

2. Create a Pytorch tensor.

   ```python
   x = torch.rand(3, 3)
   ```

3. Convert the Pytorch tensor to a numpy array.

   ```python
   y = x.numpy()
   ```

   The resulting `y` variable is a numpy array that contains the same data as the original Pytorch tensor.

## Section 3: Example

Here is an example of converting a Pytorch tensor to a numpy array:

```python
# import libraries
import torch
import numpy as np

# create tensor
x = torch.randn(2, 2)

# convert tensor to numpy array
y = x.numpy()

# print tensor and numpy array
print(f"Pytorch tensor:\n{x}")
print(f"Numpy array:\n{y}")
```

Output:
```
Pytorch tensor:
tensor([[ 1.8431,  0.6357],
        [-0.3705, -2.0016]])
Numpy array:
[[ 1.8430986   0.63573444]
 [-0.37048206 -2.001549  ]]
```

## Section 4: Conclusion

In this article, we discussed how to convert a Pytorch tensor to a numpy array in Python. We explained the differences between Pytorch tensor and numpy array and why you may need to convert Pytorch tensor to numpy array. We also provided an example of how to convert a Pytorch tensor to a numpy array using the `numpy()` method.
