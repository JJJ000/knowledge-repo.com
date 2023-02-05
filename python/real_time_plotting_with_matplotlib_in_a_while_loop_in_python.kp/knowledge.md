---
title: What is the most effective way to use matplotlib to plot data in real-time within a while loop?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the Matplotlib FuncAnimation function to plot in real-time in a while loop.
---

**Contents**

[TOC]

**Section 1: Setting Up the Plot**

The first step to plotting in real-time using matplotlib is to set up the plot. This includes importing the necessary libraries, creating the figure, and setting up the axes.

The following code imports the necessary libraries and creates a figure with two axes:

```python
import matplotlib.pyplot as plt
import numpy as np

fig, ax = plt.subplots(2, 1)
```

**Section 2: Creating the Loop**

The next step is to create the loop that will be used to generate the data and plot it in real-time. This loop should be an infinite while loop that runs until the user exits the program.

The following code creates an infinite while loop that runs until the user exits the program:

```python
while True:
    # Generate data and plot it in real-time
```

**Section 3: Generating Data**

Inside the while loop, the data needs to be generated and plotted in real-time. This can be done by generating random numbers and plotting them on the axes.

The following code generates random numbers and plots them on the axes:

```python
# Generate random numbers
x = np.random.rand(50)
y = np.random.rand(50)

# Plot the data
ax[0].plot(x, y)
ax[1].plot(x, y)
```

**Section 4: Updating the Plot**

Finally, the plot needs to be updated in real-time. This can be done by using the `plt.draw()` and `plt.pause()` functions.

The following code updates the plot in real-time:

```python
# Update the plot
plt.draw()
plt.pause(0.05)
```
