---
title: The recommended approach for duplicating a tensor in pytorch is to use
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: In PyTorch, the preferred way to copy a tensor in Python is to use the clone() method.
---

**Contents**

[TOC]

## Using the clone() method 

PyTorch provides clone() method to copy a tensor. The clone() method creates a new tensor with the same data as the original tensor but with a completely different memory location. Any changes made to the cloned tensor do not affect the original tensor. 

```python
import torch

# create a tensor
x = torch.tensor([1, 2, 3])

# create a copy of the tensor using clone() method
y = x.clone()

# print both tensors
print(x)
print(y)
```

Output:

```
tensor([1, 2, 3])
tensor([1, 2, 3])
```


## Using the copy_() method

The copy_() method, which is another way to copy a tensor in PyTorch, creates a copy of the original tensor and stores it in a new memory location. Any changes made to the copied tensor do not affect the original tensor. 

```python
import torch

# create a tensor
x = torch.tensor([1, 2, 3])

# create a copy of the tensor using copy_() method
y = torch.Tensor(x.size()).copy_(x)

# print both tensors
print(x)
print(y)
``` 

Output:

```
tensor([1, 2, 3])
tensor([1., 2., 3.])
```


## Using the detach() method

The detach() method in PyTorch is used to get a new tensor with the same data as the original tensor but with no gradients. detaching is useful when you want to detach a tensor from a computation graph, but you still want to use the tensor's values. 

```python
import torch

# create a tensor
x = torch.tensor([1, 2, 3])

# create a new tensor using detach() method
y = x.detach()

# print both tensors
print(x)
print(y)
```

Output:

```
tensor([1, 2, 3])
tensor([1, 2, 3])
```


## Using the Tensor() constructor

The Tensor() constructor is also another way to copy a tensor in PyTorch. It's similar to the copy_() method in creating a new memory location for the copied tensor. 

```python
import torch

# create a tensor
x = torch.tensor([1, 2, 3])

# create a copy of the tensor using Tensor() constructor
y = torch.Tensor(x.size()).copy_(x)

# print both tensors
print(x)
print(y)
```

Output:

```
tensor([1, 2, 3])
tensor([1., 2., 3.])
```
