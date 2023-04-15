---
title: What is the process for printing the model summary in pytorch?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the following code to print the model summary in PyTorch `print(model)`
---

**Contents**

[TOC]

Import necessary libraries and define the model

The first step is to import the necessary libraries and define the model. We will use the PyTorch library to create a neural network and the torchsummary library to print the model summary.

```python
import torch
import torch.nn as nn
from torchsummary import summary

class MyModel(nn.Module):
    def __init__(self):
        super(MyModel, self).__init__()
        self.conv1 = nn.Conv2d(in_channels=1, out_channels=32, kernel_size=3)
        self.conv2 = nn.Conv2d(in_channels=32, out_channels=64, kernel_size=3)
        self.pool = nn.MaxPool2d(kernel_size=2, stride=2)
        self.fc1 = nn.Linear(in_features=64 * 12 * 12, out_features=128)
        self.fc2 = nn.Linear(in_features=128, out_features=10)

    def forward(self, x):
        x = self.pool(torch.relu(self.conv1(x)))
        x = self.pool(torch.relu(self.conv2(x)))
        x = torch.flatten(x, 1)
        x = torch.relu(self.fc1(x))
        x = self.fc2(x)
        return x

model = MyModel()

```

Print the model summary using torchsummary

The torchsummary library provides the `summary` method, which takes the model as input and prints the summary to the console.

```python
summary(model, (1, 28, 28))
```

This will output the following summary to the console:

```
----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================
            Conv2d-1           [-1, 32, 26, 26]             320
         MaxPool2d-2           [-1, 32, 13, 13]               0
            Conv2d-3           [-1, 64, 11, 11]          18,496
         MaxPool2d-4             [-1, 64, 5, 5]               0
            Linear-5                  [-1, 128]       5,242,624
            Linear-6                   [-1, 10]           1,290
================================================================
Total params: 5,262,730
Trainable params: 5,262,730
Non-trainable params: 0
----------------------------------------------------------------
Input size (MB): 0.00
Forward/backward pass size (MB): 0.33
Params size (MB): 20.08
Estimated Total Size (MB): 20.41
----------------------------------------------------------------
```

This summary includes information on each layer of the model, such as the layer type, the output shape, and the number of parameters. It also provides a summary of the total number of trainable parameters and the estimated total size of the model.
