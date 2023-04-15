---
title: Modify the frame border of the legend using matplotlib by either eliminating it completely or adjusting its appearance
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To remove or adapt the border of the frame of legend using matplotlib in Python, use the `frameon` parameter and set it to `False` to remove the border or `True` to show the border.
---

**Contents**

[TOC]

Section 1: Introduction
In this section, we will provide a brief overview of the problem we are trying to solve and the library we are using to solve it.

We want to remove or adapt the border of the frame of a legend using Matplotlib in Python. Matplotlib is a powerful data visualization library for Python that provides a variety of graphing and plotting tools.

Section 2: Removing the border of the frame of the legend
In this section, we will show how to remove the border of a legend using Matplotlib.

To remove the border of the frame of the legend, we can use the `frameon` parameter of the `legend` method. This parameter controls whether or not the frame is drawn around the legend. We can set it to `False` to remove the border.

Here is an example code snippet that removes the border of the frame of the legend:

```
import matplotlib.pyplot as plt

data = [1, 2, 3, 4, 5]
labels = ['One', 'Two', 'Three', 'Four', 'Five']

fig, ax = plt.subplots()
ax.plot(data)
ax.legend(labels, loc='best', frameon=False)

plt.show()
```

Notice that we set the `frameon` parameter to `False` when creating the legend. When we run the code, we should see a graph with a legend that has no border around it.

Section 3: Adapting the border of the frame of the legend
In this section, we will show how to adapt the border of a legend using Matplotlib.

To adapt the border of the frame of the legend, we can use the `fancybox` parameter of the `legend` method. This parameter controls the style of the border, and we can set it to `True` to create a rounded border. We can also adjust the size and color of the border by providing the `edgecolor` and `linewidth` parameters.

Here is an example code snippet that adapts the border of the frame of the legend:

```
import matplotlib.pyplot as plt

data = [1, 2, 3, 4, 5]
labels = ['One', 'Two', 'Three', 'Four', 'Five']

fig, ax = plt.subplots()
ax.plot(data)
ax.legend(labels, loc='best', frameon=True, fancybox=True, edgecolor='red', linewidth=2)

plt.show()
```

In this example, we set the `frameon` parameter to `True` to enable the border, and we set the `fancybox` parameter to `True` to create a rounded border. We also set the `edgecolor` parameter to `'red'` to change the color of the border to red, and we set the `linewidth` parameter to `2` to increase the width of the border. When we run the code, we should see a graph with a legend that has a rounded, red border with a width of 2.

Section 4: Conclusion
In this tutorial, we learned how to remove or adapt the border of the frame of a legend using Matplotlib in Python. We showed how to use the `frameon` parameter to remove the border, and how to use the `fancybox`, `edgecolor`, and `linewidth` parameters to adapt the border. With these techniques, we can create customized legends that fit our data visualization needs.
