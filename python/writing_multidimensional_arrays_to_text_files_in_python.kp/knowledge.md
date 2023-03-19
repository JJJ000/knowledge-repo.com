---
title: What is the process for saving a multidimensional array to a text file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-15 00:00:00
updated_at: 2023-03-15 00:00:00
tldr: Use the `numpy.savetxt()` function to write a multidimensional array to a text file in Python.
---

**Contents**

[TOC]

# Introduction
In Python, we can easily store values in a multidimensional array using the NumPy library. However, writing a multidimensional array to a text file can be a bit tricky. In this tutorial, we will discuss how to write a multidimensional array to a text file in Python.

# Method 1: Using the numpy.savetxt() Method

One of the easiest ways to write a multidimensional array to a text file is by using the numpy.savetxt() method. This method takes in the filename that we want to save the array to, followed by the actual array that we want to save.

``` python
import numpy as np

# Create a multidimensional array
my_array = np.array([[1, 2], [3, 4], [5, 6]])

# Save the array to a text file
np.savetxt('my_array.txt', my_array)
```

In this example, we created a 3x2 multidimensional array and saved it in a text file named 'my_array.txt'. The default delimiter used by the numpy.savetxt() method is a space (' ') but we can also set a different delimiter by specifying the 'delimiter' parameter.

``` python
import numpy as np

# Create a multidimensional array
my_array = np.array([[1, 2], [3, 4], [5, 6]])

# Save the array to a text file with a comma delimiter
np.savetxt('my_array.txt', my_array, delimiter=',')
```

# Method 2: Using the open() and write() methods

Another way to write a multidimensional array to a text file is by using the open() method to create a file object and then using the write() method to write the array to the file object. 

``` python
# Create a multidimensional array
my_array = [[1, 2], [3, 4], [5, 6]]

# Create a file object and write the array to the file
with open('my_array.txt', 'w') as file:
    for row in my_array:
        file.write(' '.join([str(elem) for elem in row]) + '\n')
```

In this example, we used a for loop and the join() method to concatenate all the elements in each row of the array using a space (' ') delimiter. We converted all elements to strings using the str() method since the write() method only accepts strings. We also added a newline character at the end of each row so that each row is written on a new line in the text file.

# Conclusion

In this tutorial, we discussed two methods to write a multidimensional array to a text file in Python. We learned that the numpy.savetxt() method is the easiest way to write a multidimensional array to a text file if we are already using NumPy in our project. However, if we are not using NumPy, we can use the open() and write() methods to write the array to a text file.
