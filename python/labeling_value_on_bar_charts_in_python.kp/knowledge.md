---
title: What are the steps to include value labels in a bar chart?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can add value labels on a bar chart in Python using the text() function from the matplotlib library.
---

**Contents**

[TOC]

## Section 1: Required libraries

To add value labels on a bar chart, we need to use the following libraries:

- `matplotlib`: It is a plotting library for creating static, animated, and interactive visualizations in Python.
- `numpy`: It is a library for mathematical operations, which is used to generate random data.
- `pandas`: It is a library for data manipulation and analysis.

We can install these libraries using the following code:

```
!pip install matplotlib numpy pandas
```
## Section 2: Creating a basic bar chart

Before we add value labels on a bar chart, we need to create a basic bar chart using the `matplotlib` library. We can use the following code to create a basic bar chart:

```python
import matplotlib.pyplot as plt
import numpy as np

# Data
x = np.array(['A', 'B', 'C', 'D', 'E'])
y = np.array([10, 20, 15, 25, 30])

# Plotting the bar chart
plt.bar(x, y)

# Adding title to the chart
plt.title('Bar Chart')

# Displaying the chart
plt.show()
```

In this code, we first import the required libraries `matplotlib` and `numpy`. Then, we create an array `x` containing the labels for our bar chart and an array `y` containing the corresponding values. We then create a bar chart using the `plt.bar()` function and add a title to it using the `plt.title()` function. Finally, we display the chart using the `plt.show()` function.

The output of this code will be a basic bar chart with the x-axis labels A, B, C, D, E and the corresponding values on the y-axis.

## Section 3: Adding value labels on a bar chart

To add value labels on a bar chart, we need to loop through each bar in the chart and add the value label at the proper position. We can use the following code to add value labels on a bar chart:

```python
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np

# Data
x = np.array(['A', 'B', 'C', 'D', 'E'])
y = np.array([10, 20, 15, 25, 30])

# Plotting the bar chart
plt.bar(x, y)

# Adding value labels
for i in range(len(x)):
    plt.text(x[i], y[i], y[i], ha='center', va='bottom')

# Adding title to the chart
plt.title('Bar Chart')

# Displaying the chart
plt.show()
```

In this code, we import the required libraries `pandas`, `matplotlib`, and `numpy`. Then, we create an array `x` containing the labels for our bar chart and an array `y` containing the corresponding values. We then create a bar chart using the `plt.bar()` function. We then loop through each bar in the chart and add the value label at the proper position using the `plt.text()` function. Finally, we add a title to the chart using the `plt.title()` function and display it using the `plt.show()` function.

The output of this code will be a bar chart with the x-axis labels A, B, C, D, E, corresponding values on the y-axis, and the value labels on top of each bar.

## Section 4: Customizing the value labels

We can customize the value labels on a bar chart by changing the font size, color, and position. We can use the following code to customize the value labels on a bar chart:

```python
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np

# Data
x = np.array(['A', 'B', 'C', 'D', 'E'])
y = np.array([10, 20, 15, 25, 30])

# Plotting the bar chart
plt.bar(x, y)

# Adding value labels
for i in range(len(x)):
    plt.text(x[i], y[i]+1, str(y[i]), ha='center', va='bottom', fontsize=12, color='black')

# Adding title and axis labels to the chart
plt.title('Bar Chart')
plt.xlabel('X Axis')
plt.ylabel('Y Axis')

# Displaying the chart
plt.show()
```

In this code, we first import the required libraries `pandas`, `matplotlib`, and `numpy`. Then, we create an array `x` containing the labels for our bar chart and an array `y` containing the corresponding values. We then create a bar chart using the `plt.bar()` function. We then loop through each bar in the chart and add the value label at the proper position using the `plt.text()` function. We have customized the value labels by increasing the font size to 12 and changing the color to black. We have also added 1 unit to the y-coordinate of the value label so that the label appears above the bar. Finally, we add a title and axis labels to the chart using the `plt.title()`, `plt.xlabel()`, and `plt.ylabel()` functions and display it using the `plt.show()` function.

The output of this code will be a bar chart with the x-axis labels A, B, C, D, E, corresponding values on the y-axis, and the customized value labels on top of each bar.
