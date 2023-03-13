---
title: What is the method for synchronizing the x-axes of two subplots that have already been generated?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the plt.subplots function to create both subplots at once and set sharex=True.
---

**Contents**

[TOC]

## Section 1: Creating two subplots

To create two subplots with a shared x-axis, we can use the `plt.subplots()` method. For example, the following code creates two subplots with `fig` as the figure object and `ax1` and `ax2` as the axis objects of the two subplots:

```python
import matplotlib.pyplot as plt

fig, (ax1, ax2) = plt.subplots(2, 1, sharex=True)
```

The `sharex=True` argument ensures that the two subplots share the same x-axis.

We can now plot data on these subplots using the `plot()` method.

## Section 2: Sharing x-axes of pre-existing subplots

If we already have two subplots that we want to share the x-axis of, we can use the `get_shared_x_axes()` method from the `matplotlib` library. For example, suppose we have two subplots `ax1` and `ax2` that we want to share the x-axis:

```python
import matplotlib.pyplot as plt

# create two subplots
fig, ax1 = plt.subplots()
ax2 = ax1.twinx()

# share x-axis of the subplots
ax1_share, ax2_share = ax1.get_shared_x_axes(), ax2.get_shared_x_axes()
ax1_share.join(ax1, ax2)
```

In the above code, we create two subplots `ax1` and `ax2`. We then create two new axis objects `ax1_share` and `ax2_share` that represent the shared x-axis of the subplots.

Finally, we use the `join()` method to join the subplots on their shared x-axis.

## Section 3: Example code

```python
import matplotlib.pyplot as plt

# create two subplots
fig, ax1 = plt.subplots()
ax2 = ax1.twinx()

# share x-axis of the subplots
ax1_share, ax2_share = ax1.get_shared_x_axes(), ax2.get_shared_x_axes()
ax1_share.join(ax1, ax2)

# plot on ax1
x_data = [1, 2, 3]
y_data = [10, 20, 30]
ax1.plot(x_data, y_data)

# plot on ax2
x_data = [2, 3, 4]
y_data = [15, 25, 35]
ax2.plot(x_data, y_data)

plt.show()
```

In the above code, we first create two subplots `ax1` and `ax2`. We then use the `get_shared_x_axes()` method to create two shared axis objects `ax1_share` and `ax2_share`.

We then use the `join()` method to join the subplots on their shared x-axis.

Finally, we plot data on the two subplots using the `plot()` method.

## Section 4: Conclusion

In this tutorial, we have shown how to share the x-axis of two subplots in Python using the `plt.subplots()` method and the `get_shared_x_axes()` method. By sharing the x-axis, we can ensure that the subplots have the same range and tick marks on the x-axis, which can make it easier to compare data across the subplots.
