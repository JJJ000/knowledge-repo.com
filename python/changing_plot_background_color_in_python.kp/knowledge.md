---
title: What is the process for altering the background color of a plot?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: In Python, you can change the plot background color using the set\_facecolor() method.
---

**Contents**

[TOC]

# Section 1: Import Libraries

The first step is to import the necessary libraries. This includes Matplotlib and Seaborn.

```python
import matplotlib.pyplot as plt
import seaborn as sns
```

# Section 2: Set the plot background Color

Once the libraries are imported, the plot background color can be set using the ```set_style()``` function from Seaborn. This function takes a string argument which can be used to set the plot background color.

```python
sns.set_style("dark")
```

# Section 3: Create the Plot

Next, create the plot using the ```plot()``` function from Matplotlib.

```python
plt.plot(x, y)
```

# Section 4: Show the Plot

Finally, use the ```show()``` function to display the plot.

```python
plt.show()
```
