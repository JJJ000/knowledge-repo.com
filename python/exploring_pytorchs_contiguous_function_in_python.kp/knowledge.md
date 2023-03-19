---
title: What is the purpose of .contiguous() in pytorch?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: The .contiguous() function in PyTorch reshapes a tensor so that its data is stored in contiguous chunks of memory.
---

**Contents**

[TOC]

## PyTorch and Tensor Objects

PyTorch is an open-source machine learning library written in Python. It is primarily used for building deep neural networks and supports both CPU and GPU computation using simplified tensor objects.

## Tensor Memory Allocation

When tensors are created in PyTorch, they are usually allocated on the machine's memory in a non-linear fashion. This means that the data in the tensor may not be stored in contiguous memory locations. However, certain PyTorch functions like matrix multiplication and convolution operations require the input tensors to be in contiguous memory locations.

## The .contiguous() Method

The .contiguous() method in PyTorch returns a tensor with contiguous memory allocation. If the tensor is already contiguous, the .contiguous() method simply returns the tensor. However, if the tensor is non-contiguous, the .contiguous() method creates a contiguous copy of the tensor's data and returns a new tensor object with the same data.

## Example Usage

```python
import torch

# create a tensor with non-contiguous memory allocation
x = torch.randn(2, 3, 4)  # size: 2x3x4

# check if the tensor is contiguous
print(x.is_contiguous())

# create a contiguous copy of the tensor using .contiguous()
y = x.contiguous()

# check if the new tensor is contiguous
print(y.is_contiguous())
```

In the above example, we first create a tensor with non-contiguous memory allocation using the `torch.randn()` function. We then use the `.is_contiguous()` method to check if the tensor is contiguous. Since the tensor is non-contiguous, we create a contiguous copy of the tensor using the `.contiguous()` method and store it in the variable `y`. Finally, we use the `.is_contiguous()` method to check if the new tensor `y` is now contiguous, which returns `True`.
