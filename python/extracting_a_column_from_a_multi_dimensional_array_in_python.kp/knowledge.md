---
title: What is the process for retrieving an individual column from a multi-dimensional array?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can extract a column from a multi-dimensional array in Python by indexing the array with the desired column index.
---

**Contents**

[TOC]

**Using Numpy Array Indexing**

1. Create a Numpy array from the multi-dimensional array: 
   `import numpy as np`
   `arr = np.array(multi-dimensional_array)`

2. Select the desired column: 
   `column = arr[:,index]`

**Using List Slicing**

1. Create a list of lists from the multi-dimensional array: 
   `list_of_lists = [list(row) for row in multi-dimensional_array]`

2. Select the desired column: 
   `column = [row[index] for row in list_of_lists]`
