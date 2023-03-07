---
title: What is the functionality of model.eval() in pytorch?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: model.eval() sets the model to evaluation mode, where no gradients are computed and certain layers may be adjusted for inference.
---

**Contents**

[TOC]

## Overview
`model.eval()` is a PyTorch method that sets the model to evaluation mode. It changes the behavior of some layers, such as dropout and batch normalization, to work in a different way than during the training process.

### Dropout during Training vs. Testing
During training, `Dropout()` randomly sets some of the input tensor elements to zero, with a certain probability defined by the parameter p. This process helps to prevent overfitting, making our model more generalizable to unseen data. 

However, during testing, we want to use the entire network, without such amputation, because we do not want to drop any valuable information from the input.

### Batch Normalization during Training vs. Testing
Similarly, `BatchNorm()`, which normalizes the input tensor with its mean and variance statistics over a batch of samples, has different modes of operation during training and testing. During training, the statistics are computed for each batch separately. During testing, these statistics are averaged over all the training examples.

## Syntax
The `model.eval()` method can be called on the model object as shown below:
```python
model.eval()
```
This method has no input or output parameters.

## Example
Here is a simple example that shows how to make use of the `model.eval()` method to set the model to evaluation mode:
```python
import torch
import torch.nn as nn

class SimpleNet(nn.Module):
    def __init__(self):
        super(SimpleNet, self).__init__()
        self.fc1 = nn.Linear(784, 10)
        self.relu = nn.ReLU()
        self.dropout = nn.Dropout(0.5)

    def forward(self, x):
        x = x.view(-1, 784)
        x = self.fc1(x)
        x = self.relu(x)
        x = self.dropout(x)
        return x

net = SimpleNet()
output = net(torch.randn(1, 1, 28, 28))
print(output)

# Set the network to evaluation mode
net.eval()

output = net(torch.randn(1, 1, 28, 28))
print(output)
```

Notice that we are printing the output of the network before and after setting it to evaluation mode. Before, we are applying dropout to the tensor output, and after that, we are not applying it. This can have a significant impact on the final output depending on the value of p, as detailed before.
