---
title: Performing matplotlib plotting in a manner that does not block
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To plot in a non-blocking way with Matplotlib in Python, use the `ion()` function to turn on interactive mode and the `draw()` function to update the plot.
---

**Contents**

[TOC]

# Introduction

Matplotlib is a widely used Python library used for data visualization. When plotting data using Matplotlib, the default behavior is to block the execution of the program until the plot is closed. This can be inconvenient when working with large datasets or when automated plotting is needed. In this article, we will explore different ways to plot data in a non-blocking way using Matplotlib.


# Using the `show()` function and timers

One way to plot data in a non-blocking way is to use the `show()` function and timers. In this approach, the `show()` function is called to display the plot, and a timer is used to periodically update the plot data. Here is an example:

```python
import matplotlib.pyplot as plt
import numpy as np

# generate some data
x = np.linspace(0, 10, 100)
y = np.sin(x)

# create the figure and axes
fig, ax = plt.subplots()

# plot the initial data
line, = ax.plot(x, y)

# set the axis limits
ax.set_xlim(0, 10)
ax.set_ylim(-1, 1)

# display the plot and start the timer
plt.ion()
plt.show()

# update the plot data
for i in range(100):
    y = np.sin(x + i/10)
    line.set_ydata(y)
    plt.draw()
    plt.pause(0.1)
```

In this example, we generate some data, create the figure and axes, and plot the initial data. We then call the `plt.ion()` function to turn on interactive mode, which enables the non-blocking behavior. We then call the `plt.show()` function to display the plot and start the event loop. Finally, we enter a loop where we update the plot data, redraw the plot using `plt.draw()`, and pause for a short period of time using `plt.pause()`. The `plt.pause()` function is necessary to give Matplotlib time to process events and update the plot.


# Using the `FuncAnimation` class

Another way to plot data in a non-blocking way is to use the `FuncAnimation` class. This class creates an animation by repeatedly calling a function that updates the plot data. Here is an example:

```python
import matplotlib.pyplot as plt
import numpy as np
from matplotlib.animation import FuncAnimation

# generate some data
x = np.linspace(0, 10, 100)
y = np.sin(x)

# create the figure and axes
fig, ax = plt.subplots()

# plot the initial data
line, = ax.plot(x, y)

# set the axis limits
ax.set_xlim(0, 10)
ax.set_ylim(-1, 1)

# define the update function
def update(i):
    y = np.sin(x + i/10)
    line.set_ydata(y)

# create the animation
anim = FuncAnimation(fig, update, frames=100, interval=100)

# display the plot
plt.show()
```

In this example, we generate some data, create the figure and axes, and plot the initial data. We define an `update()` function that takes an index `i` as input and updates the plot data based on the value of `i`. We then create an instance of the `FuncAnimation` class, passing in the figure, the update function, the number of frames, and the interval between frames. Finally, we call `plt.show()` to display the plot.


# Using the `async` and `await` statements

Starting from version 3.7, Python supports asynchronous programming using the `async` and `await` statements. We can use this feature to plot data in a non-blocking way using Matplotlib. Here is an example:

```python
import asyncio
import matplotlib.pyplot as plt
import numpy as np

# create the figure and axes
fig, ax = plt.subplots()

# set the axis limits
ax.set_xlim(0, 10)
ax.set_ylim(-1, 1)

# define the async update function
async def update():
    x = np.linspace(0, 10, 100)
    for i in range(100):
        y = np.sin(x + i/10)
        ax.plot(x, y, 'b-')
        ax.set_title(f'Frame {i}')
        fig.canvas.draw()
        fig.canvas.flush_events()
        await asyncio.sleep(0.1)

# run the event loop
async def main():
    plt.ion()
    plt.show(block=False)
    await update()

asyncio.run(main())
```

In this example, we create the figure and axes, and set the axis limits. We define an async `update()` function that generates data and updates the plot in a loop. The `await asyncio.sleep()` function is used to pause the loop for a short period of time between updates. We then define an async `main()` function that turns on interactive mode, displays the plot, and awaits the result of the `update()` function. Finally, we call `asyncio.run()` to start the event loop and run the `main()` function. The `fig.canvas.flush_events()` function is used to process any pending events in the Matplotlib event queue.
