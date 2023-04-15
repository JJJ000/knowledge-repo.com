---
title: Can you explain how to use matplotlib in Python to create a histogram from a data list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the plt.hist() function from Matplotlib and pass your list of data as the first argument.
---

**Contents**

[TOC]

## Section 1: Importing Libraries

We need to import two libraries to plot a histogram using Matplotlib in Python, namely NumPy and Matplotlib. NumPy is a powerful library for mathematical operations and Matplotlib is a plotting library.

```python
import numpy as np
import matplotlib.pyplot as plt
```

## Section 2: Preparing Data

We need to prepare the data in the form of a list or numpy array. Let us assume we have a list of ages of 50 people.

```python
ages = [25, 30, 42, 19, 28, 38, 22, 18, 31, 28, 29, 19, 22, 24, 23, 28, 26, 20, 27, 29, 34, 26, 23, 21, 35, 33, 23, 27, 30, 18, 21, 26, 29, 19, 31, 24, 20, 22, 28, 27, 30, 25, 23, 19, 21, 22, 26, 20, 19, 32, 24]
```

## Section 3: Plotting the Histogram

Now, we can use the `plt.hist()` function to plot the histogram. 

```python
plt.hist(ages, bins=10, color='green',edgecolor='black')
plt.title('Age Distribution')
plt.xlabel('Age')
plt.ylabel('Frequency')
plt.show()
```

Here, we specified the number of bins as 10, color as green and edge color as black. We also set the title of the plot, and the x-axis and y-axis labels. Finally, we display the plot using the `plt.show()` function.

## Section 4: Complete Code

The complete code for plotting a histogram using Matplotlib in Python with a list of data is shown below.

```python
import numpy as np
import matplotlib.pyplot as plt

ages = [25, 30, 42, 19, 28, 38, 22, 18, 31, 28, 29, 19, 22, 24, 23, 28, 26, 20, 27, 29, 34, 26, 23, 21, 35, 33, 23, 27, 30, 18, 21, 26, 29, 19, 31, 24, 20, 22, 28, 27, 30, 25, 23, 19, 21, 22, 26, 20, 19, 32, 24]

plt.hist(ages, bins=10, color='green',edgecolor='black')
plt.title('Age Distribution')
plt.xlabel('Age')
plt.ylabel('Frequency')
plt.show()
```
