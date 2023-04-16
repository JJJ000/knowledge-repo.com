---
title: Identifying the highest points in a two-dimensional array
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The scipy.signal.find\_peaks\_2d function can be used to detect peaks in a 2D array in Python.
---

**Contents**

[TOC]

# Section 1: Overview

Peak detection in a 2D array is a process of finding local maxima in an array. A local maximum is a value in the array that is greater than its neighbors. It is a useful technique for finding areas of interest in an array, such as the location of a peak. 

# Section 2: Algorithm

The peak detection algorithm is fairly straightforward. It begins by iterating over the elements of the array, starting from the top left corner. For each element, the algorithm checks if it is greater than its neighbors. If it is, then it is considered a local maximum. The algorithm then moves on to the next element until it has examined all elements in the array. 

# Section 3: Implementation

The peak detection algorithm can be implemented in Python using a simple for loop. The following code shows an example of how it can be implemented:

```
# Initialize an empty list to store the local maxima
maxima = []

# Iterate over the elements of the array
for i in range(len(array)):
    for j in range(len(array[0])):
        # Check if the element is a local maximum
        if array[i][j] > array[i-1][j] and array[i][j] > array[i][j-1]:
            # If it is, add it to the list of maxima
            maxima.append((i,j))

# The list of maxima contains the coordinates of all local maxima
```

# Section 4: Conclusion

Peak detection in a 2D array is a useful technique for finding areas of interest in an array. The algorithm is fairly straightforward and can be easily implemented in Python using a simple for loop.
