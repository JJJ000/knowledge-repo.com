---
title: Changing the visibility of axis labels in matplotlib plots
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use plt.xticks([]) and plt.yticks([]) to hide the axis text.
---

**Contents**

[TOC]

**Section 1: Hiding the x-axis Text**

To hide the x-axis text in a matplotlib plot in Python, use the following code:

```python
import matplotlib.pyplot as plt

plt.xticks([])
```

This will hide the x-axis text, but the x-axis labels will still be visible.

**Section 2: Hiding the y-axis Text**

To hide the y-axis text in a matplotlib plot in Python, use the following code:

```python
import matplotlib.pyplot as plt

plt.yticks([])
```

This will hide the y-axis text, but the y-axis labels will still be visible.

**Section 3: Hiding Both x- and y-axis Text**

To hide both the x- and y-axis text in a matplotlib plot in Python, use the following code:

```python
import matplotlib.pyplot as plt

plt.xticks([])
plt.yticks([])
```

This will hide both the x- and y-axis text, but the axis labels will still be visible.

**Section 4: Hiding All Axis Text**

To hide all axis text in a matplotlib plot in Python, use the following code:

```python
import matplotlib.pyplot as plt

plt.xticks([])
plt.yticks([])
plt.axis('off')
```

This will hide all axis text, including the axis labels.
