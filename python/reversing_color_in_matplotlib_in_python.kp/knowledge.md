---
title: Invert the color scheme in matplotlib
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: To reverse a colormap in matplotlib, use the reversed() function to invert the colors of the colormap.
---

**Contents**

[TOC]

**Option 1: Using the LinearSegmentedColormap**

1. Create a LinearSegmentedColormap: 
   Create a LinearSegmentedColormap instance with the name of the desired colormap and the reversed keyword set to True.

```python
import matplotlib.pyplot as plt
from matplotlib.colors import LinearSegmentedColormap

cmap = LinearSegmentedColormap("my_cmap_name", reversed=True)
```

2. Set the Colormap:
   Use the set_cmap() method of the pyplot module to set the colormap.

```python
plt.set_cmap(cmap)
```

**Option 2: Using the reversed() Function**

1. Create a Colormap: 
   Create a colormap instance with the name of the desired colormap.

```python
import matplotlib.pyplot as plt

cmap = plt.cm.my_cmap_name
```

2. Reverse the Colormap:
   Use the reversed() function to reverse the colormap.

```python
cmap_r = reversed(cmap)
```

3. Set the Colormap:
   Use the set_cmap() method of the pyplot module to set the colormap.

```python
plt.set_cmap(cmap_r)
```
