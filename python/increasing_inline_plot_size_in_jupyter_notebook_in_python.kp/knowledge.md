---
title: What is the best way to increase the size of inline plots in jupyter notebook?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `figsize` parameter in the `plt.figure()` function to set the size of the plot.
---

**Contents**

[TOC]

# 1. Using Matplotlib
Matplotlib is a Python library used to create plots. It can be used to create inline plots in Jupyter Notebook. The size of the plot can be adjusted by setting the figure size using the figsize parameter.

```
import matplotlib.pyplot as plt

# Set plot size
plt.figure(figsize=(10,10))

# Create plot
plt.plot(x, y)

# Show plot
plt.show()
```

# 2. Using Seaborn
Seaborn is another Python library used for creating plots. It can also be used to create inline plots in Jupyter Notebook. The size of the plot can be adjusted by setting the figure size using the figsize parameter.

```
import seaborn as sns

# Set plot size
sns.set(rc={'figure.figsize':(10,10)})

# Create plot
sns.scatterplot(x, y)

# Show plot
plt.show()
```

# 3. Using Plotly
Plotly is a Python library used to create interactive plots. It can also be used to create inline plots in Jupyter Notebook. The size of the plot can be adjusted by setting the width and height parameters.

```
import plotly.express as px

# Set plot size
fig = px.scatter(x=x, y=y, width=1000, height=1000)

# Show plot
fig.show()
```

# 4. Using Bokeh
Bokeh is another Python library used to create interactive plots. It can also be used to create inline plots in Jupyter Notebook. The size of the plot can be adjusted by setting the plot_width and plot_height parameters.

```
from bokeh.plotting import figure

# Set plot size
p = figure(plot_width=1000, plot_height=1000)

# Create plot
p.circle(x, y)

# Show plot
show(p)
```
