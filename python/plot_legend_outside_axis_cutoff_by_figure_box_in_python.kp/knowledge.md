---
title: If you move the legend of matplotlib outside the axis, it will be truncated by the figure box
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the bbox\_to\_anchor parameter in the legend function to adjust the legend position and prevent it from being cut off by the figure box.
---

**Contents**

[TOC]

Introduction
-----------

When plotting graphs with the `matplotlib` library in Python, it is often useful to add a legend to make the plot more informative. However, when the legend is placed outside of the plot area, it can get cut off by the figure box. This occurs because the figure box only extends to the edge of the axes and does not take into consideration any elements that are placed outside of it. In this guide, we will discuss the steps that can be taken to prevent this from happening.

Creating a sample plot
----------------------

Before we dive into the solution, let's create a simple plot to demonstrate the issue:

``` python
import matplotlib.pyplot as plt
import numpy as np

x = np.arange(0, 2*np.pi, 0.1)
y = np.sin(x)

fig, ax = plt.subplots()
ax.plot(x, y, label='sin(x)')
ax.legend(loc='center left', bbox_to_anchor=(1, 0.5))
plt.show()
```

The `bbox_to_anchor` parameter in the `legend` function places the legend outside of the axis at the specified location. In this case, we are placing it on the right-hand side of the plot.

![Cut off legend](https://i.imgur.com/ZLILSxN.png)


Moving the legend outside of the figure box
-------------------------------------------

To prevent the legend from getting cut off, we need to move it outside of the figure box. This can be achieved by using the `tight_layout` function and adjusting the `w_pad` and `h_pad` parameters. These parameters add padding between the subplots and the figure edge, giving the legend more room to be displayed.

``` python
import matplotlib.pyplot as plt
import numpy as np

x = np.arange(0, 2*np.pi, 0.1)
y = np.sin(x)

fig, ax = plt.subplots()
ax.plot(x, y, label='sin(x)')
ax.legend(loc='center left', bbox_to_anchor=(1, 0.5))

plt.tight_layout(pad=1.5, w_pad=1, h_pad=1)
plt.show()
```

The `pad` parameter sets the padding between the figure edge and the plot area, while the `w_pad` and `h_pad` parameters set the padding between adjacent subplots. By increasing the padding, we give the legend more space to be displayed without being cut off.

![Legend outside figure](https://i.imgur.com/miRZn1V.png)


Conclusion
----------

When plotting graphs with `matplotlib`, it is important to ensure that all components are visible and informative. Placing the legend outside of the axis can be an effective way to achieve this, but it can also result in the legend getting cut off by the figure box. To prevent this from happening, we can adjust the padding using the `tight_layout` function. By increasing the padding between the subplots and the figure edge, we can give the legend more room to be displayed without being cut off.
