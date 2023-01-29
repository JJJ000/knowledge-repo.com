---
title: Instead of displaying a plot using matplotlib, save it as an image file
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the plt.savefig() function to save the plot to an image file.
---

**Contents**

[TOC]

**Section 1: Import Necessary Libraries**

```python
import matplotlib.pyplot as plt
import numpy as np
```

**Section 2: Create the Plot**

```python
x = np.linspace(0, 10, 100)
y = np.sin(x)

plt.plot(x, y)
```

**Section 3: Save the Plot**

```python
plt.savefig('plot.png')
```

**Section 4: Display the Plot**

```python
plt.show()
```
