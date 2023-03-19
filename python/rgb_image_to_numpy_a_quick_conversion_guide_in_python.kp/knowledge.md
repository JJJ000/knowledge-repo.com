---
title: What is the process of converting an rgb image to a numpy array?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the `numpy.asarray()` function to convert an RGB image to a numpy array in Python.
---

**Contents**

[TOC]

## Introduction
To work with images in Python, one common format is the numpy array. Numpy is a package for scientific computing in Python and it provides an easy way to manipulate arrays. In this tutorial, we will show how to convert an RGB image to numpy array using Python. 

## Step 1: Importing the required libraries
We will start by importing two libraries: matplotlib.pyplot and numpy.

```python
import matplotlib.pyplot as plt
import numpy as np
```

## Step 2: Reading the RGB image
To read the RGB image, we will use the imread() function from the matplotlib library.

```python
image = plt.imread('image_name.png')
plt.imshow(image)
```

## Step 3: Converting the RGB image to numpy array 
Once we have an RGB image, we can convert it to a numpy array by using the astype() method. This method is used to cast a numpy array to a specified type. In this case, we will cast the RGB image to a numpy array with a data type of 'float32'.

```python
image_array = np.array(image, dtype='float32')
```

## Conclusion
We have shown how to convert an RGB image to numpy array using Python. It is a useful skill to have when working with images in Python.
