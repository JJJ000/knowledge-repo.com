---
title: Verify the overall count of parameters present in a pytorch model
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: To check the total number of parameters in a PyTorch model in Python, use the command `sum(p.numel() for p in model.parameters())`.
---

**Contents**

[TOC]

Section 1: Introduction
In PyTorch, a model's parameters are stored in its `state_dict` attribute, which is essentially a dictionary of parameter names and their corresponding tensors. In order to compute the total number of parameters in a PyTorch model, we can simply sum up the number of elements in all the tensors in the `state_dict`.

Section 2: Code
To compute the total number of parameters in a PyTorch model, we can use the following code snippet:

```python
import torch

def count_parameters(model):
    return sum(p.numel() for p in model.parameters() if p.requires_grad)

# example usage
model = torch.nn.Linear(784, 10)
num_params = count_parameters(model)
print(f"Number of trainable parameters: {num_params}")
```

In this example, we define the `count_parameters` function, which takes a PyTorch model as input and returns the total number of trainable parameters in the model. We iterate over all the trainable parameters in the model by calling `model.parameters()` and filtering out the ones that don't require gradients (e.g., fixed biases). We then calculate the number of elements in each trainable parameter tensor by calling `p.numel()` and sum them up using the `sum` function. Finally, we return the total number of parameters.

Section 3: Example
As an example, we create a simple linear model with a 784-dimensional input and 10-dimensional output, and print the number of trainable parameters:

```python
model = torch.nn.Linear(784, 10)
num_params = count_parameters(model)
print(f"Number of trainable parameters: {num_params}")
```

This should output:

```
Number of trainable parameters: 7850
```

Section 4: Conclusion
In this tutorial, we discussed how to compute the total number of parameters in a PyTorch model using the `state_dict` attribute and the `numel` function. We also provided an example implementation of the `count_parameters` function for computing the number of trainable parameters in a PyTorch model, and demonstrated its usage on a simple linear model.
