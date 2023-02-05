---
title: Randomize the order of items in an array using python's random module
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: To shuffle an array with python, use the random.shuffle() function.
---

**Contents**

[TOC]

# Using the `random` Module

The `random` module provides functions that allow us to work with random numbers. We can use this module to shuffle an array.

## Step 1: Import the `random` Module

The first step is to import the `random` module.

```python
import random
```

## Step 2: Create a Function to Shuffle the Array

We can create a function that takes an array as an argument and shuffles it.

```python
def shuffle_array(arr):
    random.shuffle(arr)
    return arr
```

## Step 3: Call the Function

We can now call the function and pass in the array we want to shuffle.

```python
array = [1, 2, 3, 4, 5]
shuffled_array = shuffle_array(array)
print(shuffled_array) # [2, 5, 1, 3, 4]
```
