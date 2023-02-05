---
title: What is the process for converting and displaying a numpy array as an image?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the imshow() function from the matplotlib library to display a numpy array as an image.
---

**Contents**

[TOC]

## Using Matplotlib
1. Use the `imshow` function from the `matplotlib` library to display the numpy array as an image. 
2. Import the `matplotlib.pyplot` library. 
3. Convert the numpy array to a `uint8` array using the `astype` method. 
4. Call the `imshow` function with the numpy array as an argument. 

## Using PIL
1. Use the `fromarray` method from the `PIL` library to convert the numpy array to an image. 
2. Import the `PIL` library. 
3. Convert the numpy array to a `uint8` array using the `astype` method. 
4. Call the `fromarray` method with the numpy array as an argument. 
5. Call the `show` method to display the image.
