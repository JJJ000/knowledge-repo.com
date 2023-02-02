---
title: What is the best way to alter the font size of a legend using matplotlib.pyplot?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the plt.legend() function with the fontsize parameter to change the legend fontsize in matplotlib.pyplot.
---

**Contents**

[TOC]

# Section 1: Importing Libraries

In order to change the font size of the legend, we will need to import the `matplotlib.pyplot` library. 

```
import matplotlib.pyplot as plt
```

# Section 2: Adding the Legend

Before we can change the font size of the legend, we will need to add the legend to the plot. This can be done using the `plt.legend()` command. 

```
plt.legend(loc='upper left')
```

# Section 3: Changing the Font Size

Once we have added the legend to the plot, we can then change the font size of the legend using the `fontsize` argument. 

```
plt.legend(loc='upper left', fontsize=12)
```

# Section 4: Displaying the Plot

Finally, we can display the plot with the legend font size changed by using the `plt.show()` command. 

```
plt.show()
```
