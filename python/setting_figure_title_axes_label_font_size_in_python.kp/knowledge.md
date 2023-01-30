---
title: What is the procedure for changing the font size of the figure title and axes labels?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: You can set the figure title and axes labels font size in Python by using the set\_size() method.
---

**Contents**

[TOC]

#### Setting Font Size for Figure Title

To set the font size of the figure title in Python, use the `set_size()` method from the `matplotlib.pyplot.title` class. This method takes a single argument, which is the desired font size in points. For example:

```
import matplotlib.pyplot as plt

plt.title("Figure Title", fontsize = 18)
```

#### Setting Font Size for Axes Labels

To set the font size of the axes labels in Python, use the `set_size()` method from the `matplotlib.pyplot.xlabel` and `matplotlib.pyplot.ylabel` classes. This method takes a single argument, which is the desired font size in points. For example:

```
import matplotlib.pyplot as plt

plt.xlabel("X Label", fontsize = 18)
plt.ylabel("Y Label", fontsize = 18)
```

#### Setting Font Size for All Figure Elements

To set the font size of all figure elements in Python, use the `rcParams` dictionary from the `matplotlib.pyplot` module. This dictionary contains all of the figure's parameters and can be used to set the font size for all elements. For example:

```
import matplotlib.pyplot as plt

plt.rcParams['font.size'] = 18
```

#### Setting Font Size for Specific Figure Elements

To set the font size of specific figure elements in Python, use the `set_size()` method from the appropriate class. For example, to set the font size for the figure title, use the `matplotlib.pyplot.title` class, and to set the font size for the axes labels, use the `matplotlib.pyplot.xlabel` and `matplotlib.pyplot.ylabel` classes. The `set_size()` method takes a single argument, which is the desired font size in points. For example: 

```
import matplotlib.pyplot as plt

plt.title("Figure Title", fontsize = 18)
plt.xlabel("X Label", fontsize = 18)
plt.ylabel("Y Label", fontsize = 18)
```
