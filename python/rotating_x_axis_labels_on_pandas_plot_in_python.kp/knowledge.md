---
title: What is the process for rotating the x-axis tick labels in a pandas plot?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: You can rotate x-axis tick labels in a pandas plot in Python by using the `rotation` parameter and specifying the angle of rotation, such as `rotation=90`.
---

**Contents**

[TOC]

## 1. Import necessary libraries

Before we start rotating the x-axis tick labels in a pandas plot, we need to import some necessary libraries. The following code block imports pandas library for data manipulation, matplotlib library for data visualization, and numpy library for computational functions.


```python
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np
```

## 2. Create pandas DataFrame and plot data

We will create a simple pandas DataFrame to illustrate how to rotate x-axis tick labels in a pandas plot in Python. We will create a DataFrame with two columns - 'Year' and 'Sales'. The 'Year' column will have years from 2010 to 2019, and the 'Sales' column will have random sales data. We will then plot the data using pandas plot function.


```python
data = {'Year': list(range(2010, 2020)), 
        'Sales': np.random.randint(1000, 10000, size=10)}
df = pd.DataFrame(data)
df.plot(x='Year', y='Sales')
plt.show()
```

## 3. Rotate x-axis tick labels

By default, x-axis tick labels are horizontal in a pandas plot. However, sometimes it may be useful to rotate the x-axis tick labels to make them more readable. We can rotate x-axis tick labels using the 'xticks' function of matplotlib library.

First, we will get the current x-axis tick labels using 'get_xticklabels' function of matplotlib. We will then create a 'rotation' variable and set it to the desired rotation angle in degrees. Finally, we will call 'set_rotation' function of matplotlib to apply the rotation to x-axis tick labels.


```python
labels = plt.gca().get_xticklabels()
rotation = 45
plt.setp(labels, rotation=rotation)
plt.show()
```

## 4. Complete code


```python
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np

data = {'Year': list(range(2010, 2020)), 
        'Sales': np.random.randint(1000, 10000, size=10)}
df = pd.DataFrame(data)
df.plot(x='Year', y='Sales')

labels = plt.gca().get_xticklabels()
rotation = 45
plt.setp(labels, rotation=rotation)
plt.show()
```


This code will create a pandas plot with rotated x-axis tick labels.
