---
title: What are the steps to use tensorflow on a cpu?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To run Tensorflow on CPU in Python, you can simply install Tensorflow and import it, and it will automatically use CPU by default.
---

**Contents**

[TOC]

## Introduction

Tensorflow is an open-source library dedicated to numerical computation and machine learning. It has achieved wide popularity among data scientists, and for a good reason. Tensorflow provides support for deep learning and other algorithms, making it one of the ultimate machine learning libraries available today. In this tutorial, we demonstrate how to use Tensorflow on a CPU in Python. 

## Check for Tensorflow Installation

Before running Tensorflow on a CPU, you need to ensure that Tensorflow is installed on your machine. Tensorflow can be installed using the following command:

```
!pip install tensorflow
``` 

Make sure that you have the necessary dependencies installed to use Tensorflow. 

Once you’ve installed Tensorflow, you can verify the installation in Python using the following code snippet:

```python
import tensorflow as tf
print("TensorFlow version:", tf.__version__)
```

## Run Tensorflow on a CPU

To run Tensorflow on a CPU, you need to configure the code to use the CPU instead of the GPU. Tensorflow is designed to automatically detect hardware configurations and choose the appropriate processor to use by default. To force Tensorflow to use a CPU instead, use the following code:

```python
import os
os.environ['CUDA_VISIBLE_DEVICES'] = '-1'
```

By setting `CUDA_VISIBLE_DEVICES` to `-1`, you explicitly tell Tensorflow to use the CPU instead of the GPU. You can then continue to write your Tensorflow code as you would normally.

## Verify CPU Usage

After running Tensorflow on a CPU, you may want to verify that the CPU is being used instead of the GPU. You can check which device is being used by Tensorflow by using the following command:

```python
sess = tf.Session(config=tf.ConfigProto(log_device_placement=True))
```

This code snippet will print out the device that Tensorflow is using to perform the computations. If the output displays `/CPU:0`, that means Tensorflow is running on a CPU.

## Conclusion

In this tutorial, we have demonstrated how to run Tensorflow on a CPU in Python. By setting `CUDA_VISIBLE_DEVICES` to `-1`, you can force Tensorflow to use a CPU instead of a GPU. You can then proceed to write your Tensorflow code as usual. We hope this tutorial was informative and helpful in your use of Tensorflow.
