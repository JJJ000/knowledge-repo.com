---
title: Can you describe the distinction between reshaping and viewing in pytorch?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Reshape creates a new tensor with a different shape while view creates a view of the original tensor with a different shape.
---

**Contents**

[TOC]

Introduction
------------
Pytorch is an open-source machine learning library that provides a range of tensors and mathematical operations for building neural networks. In Pytorch, tensors can have different dimensions and shapes, to perform different operations such as reshaping or viewing, Pytorch provides these two functions- `reshape` and `view`. They both work with tensors of same size, but there are certain differences. In this article, we will discuss the differences between reshape and view in pytorch with some examples.

Reshape
-------
Reshape is a function in PyTorch used to change the shape of the given tensor without modifying its content or underlying data. The size of the reshaped tensor should be equal to the size of the original tensor. The reshaped tensor’s underlying data is always the same as that of the original tensor. We can reshape a tensor using the `reshape()` function in PyTorch.

Example:

```
import torch
t = torch.tensor([[1,2,3,4], [5,6,7,8]])
# Shape of tensor
print(t.shape) # prints torch.Size([2, 4])
reshaped_t = t.reshape(4,2)
print(reshaped_t)
print(reshaped_t.shape) # prints torch.Size([4,2])
```
Output:
```
torch.Size([2, 4])
tensor([[1, 2],
        [3, 4],
        [5, 6],
        [7, 8]])
torch.Size([4, 2])
```
In the above example, the original tensor of shape `[2,4]` is reshaped using the reshape() function to a new tensor of shape `[4,2]`.

View
----
View is also a function in PyTorch used to change the shape of the given tensor without modifying its content or underlying data. Similar to reshape(), it requires that the size of the new tensor is the same as that of the original tensor. The difference is that with the `view()` function, the new tensor and the original tensor share the same underlying data. Pytorch will throw an error if the reshaping cannot be done because of the tensor’s size. We can reshape a tensor using the `view()` function in PyTorch.

Example:

```
import torch
t = torch.tensor([[1,2,3,4], [5,6,7,8]])
# Shape of tensor
print(t.shape) # prints torch.Size([2, 4])
view_t = t.view(4,2)
print(view_t)
print(view_t.shape) # prints torch.Size([4,2])
```
Output:
```
torch.Size([2, 4])
tensor([[1, 2],
        [3, 4],
        [5, 6],
        [7, 8]])
torch.Size([4, 2])
```
In the above example, the original tensor of shape `[2,4]` is reshaped using the view() function to a new tensor of shape `[4,2]`. 

Differences
-----------
The actual difference between reshape and view is that reshape() does not affect the tensor provided the new shape has the same number of elements as the initial tensor. But view() will throw an error at runtime if the new shape does not have the same number of elements as the initial tensor. 

Another difference is that reshape() creates a copy of the original tensor when the new shape is inconsistent with the original shape, whereas view() doesn’t make a copy of the original tensor till the data is from the same location.

Conclusion
----------
In this article, we discussed the differences between reshape and view in PyTorch. Both the functions are used to change the shape of the given tensor without affecting their underlying data but view checks the compatibility of the new shape with original shape and raises an error if they are incompatible.
