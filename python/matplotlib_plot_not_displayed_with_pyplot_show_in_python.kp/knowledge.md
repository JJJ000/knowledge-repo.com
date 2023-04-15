---
title: Although I call pyplot.show(), my plot is not displayed by matplotlib
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: It is possible that the plot window is being blocked by an anti-virus software or a firewall.
---

**Contents**

[TOC]

Possible Solution 1: Check your backend

Matplotlib has different backends for generating plots, and sometimes the one you are using may not work properly. To check if this is the case, you can try setting a different backend before creating the plot:

```python
import matplotlib
matplotlib.use('tkagg')  # replace with a different backend
import matplotlib.pyplot as plt

# create your plot here

plt.show()  # display the plot
```

If this solves the problem, you can make the backend change permanent by setting it in your `matplotlibrc` file, which is located in your `matplotlib` directory. This way, you don't need to include the `matplotlib.use()` line in every script that uses `matplotlib`.

Possible Solution 2: Use interactive mode

Sometimes, calling `pyplot.show()` is not enough to display the plot, especially if you have multiple plots or complex plots that require user interaction. In this case, you can try using interactive mode:

```python
import matplotlib.pyplot as plt

# create your plot here

plt.ion()  # turn on interactive mode
plt.show()  # display the plot
```

This will open a window with the plot and allow you to interact with it (e.g., zoom in/out, pan, etc.). If this works, you can turn off interactive mode by calling `plt.ioff()`.

Possible Solution 3: Check for errors/warnings

Sometimes, the plot may fail to display due to errors or warnings that are not displayed in the console or notebook. To check for them, you can try running the following code after calling `plt.show()`:

```python
import matplotlib.pyplot as plt
import matplotlib as mpl

# create your plot here

plt.show()  # display the plot

if mpl.get_backend() != 'agg':
    for i, msg in enumerate(mpl.get_backend().errorbar):
        print('Error/Warning {}: {}'.format(i+1, msg))
```

This will print any errors or warnings related to the backend in the console, which may give you a clue about what went wrong.

Possible Solution 4: Update matplotlib and/or your environment

Finally, you may want to update `matplotlib` to the latest version or make sure your environment is properly configured (e.g., dependencies, path, etc.). You can do this using your package manager or virtual environment tools, depending on how you installed `matplotlib` and your Python distribution. Make sure you follow the instructions for your specific platform and version to avoid compatibility issues.
