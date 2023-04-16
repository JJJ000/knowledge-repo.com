---
title: Create a single chart using matplotlib that displays two histograms
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, it is possible to plot two histograms on a single chart using matplotlib in Python by using the `plt.hist` function twice with different parameters.
---

**Contents**

[TOC]

**Section 1: Import Libraries**

```python
import matplotlib.pyplot as plt
import numpy as np
```

**Section 2: Create Data**

```python
# Create data for two histograms

data1 = np.random.randn(1000)
data2 = np.random.randn(1000)
```

**Section 3: Plot Histograms**

```python
# Plot the histograms
plt.hist(data1, bins=20, color='b', alpha=0.5)
plt.hist(data2, bins=20, color='r', alpha=0.5)

# Add labels
plt.xlabel('Data Values')
plt.ylabel('Frequency')

# Show the plot
plt.show()
```

**Section 4: Customize Plot**

```python
# Plot the histograms
plt.hist(data1, bins=20, color='b', alpha=0.5, label='Data 1')
plt.hist(data2, bins=20, color='r', alpha=0.5, label='Data 2')

# Add labels
plt.xlabel('Data Values')
plt.ylabel('Frequency')

# Add a legend
plt.legend(loc='upper right')

# Show the plot
plt.show()
```
