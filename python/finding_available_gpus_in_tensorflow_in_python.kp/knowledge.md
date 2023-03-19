---
title: What is the method to obtain the presently accessible gpus in tensorflow?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use `tf.config.list\_physical\_devices(`GPU`)` to get the list of available GPUs in TensorFlow.
---

**Contents**

[TOC]

## Importing Tensorflow library

First, we need to import the TensorFlow library in Python.


```python
import tensorflow as tf
```

## Detecting available GPUs

TensorFlow provides a utility function called `tf.config.list_physical_devices('GPU')` to detect the available GPUs in the system. This function returns a list of PhysicalDevice objects representing the available GPUs.


```python
gpus = tf.config.list_physical_devices('GPU')
print(gpus)
```

This will print a list of PhysicalDevice objects representing the available GPUs.

## Getting the names of available GPUs

We can extract the names of the available GPUs from the PhysicalDevice objects using the `name` attribute.


```python
gpu_names = [gpu.name for gpu in gpus]
print(gpu_names)
```

This will print a list of strings, where each string represents the name of an available GPU.

## Checking if the GPUs are available

We can check whether the GPUs are available or not by using the `is_initialized` attribute of the PhysicalDevice object. If the attribute is `True`, the GPU is available.


```python
gpu_availabilities = [gpu.is_initialized() for gpu in gpus]
print(gpu_availabilities)
```

This will print a list of Boolean values representing the availability of the available GPUs. `True` means the GPU is available.
