---
title: What is the syntax for converting all elements of a list to floats in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the map() function to apply the float() function to each item in the list.
---

**Contents**

[TOC]

### Using a For Loop 

The following code will loop through each item in a list and convert it to a float:

```
my_list = [1, 2, 3, 4]

for i in range(len(my_list)):
    my_list[i] = float(my_list[i])
```

### Using List Comprehension

The following code will convert all items in a list to floats using list comprehension:

```
my_list = [1, 2, 3, 4]

my_list = [float(i) for i in my_list]
```

### Using Map Function

The following code will use the map function to convert all items in a list to floats:

```
my_list = [1, 2, 3, 4]

my_list = list(map(float, my_list))
```

### Using Numpy

The following code will use NumPy to convert all items in a list to floats:

```
import numpy as np

my_list = [1, 2, 3, 4]

my_list = np.array(my_list, dtype=float)
```
