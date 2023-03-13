---
title: The plot is not displayed on pycharm
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: You need to include the command plt.show() at the end of your code to show the plot in Pycharm.
---

**Contents**

[TOC]

Solution to PyCharm not showing plot in Python 

1. Check the backend used by matplotlib
The first thing to check is the backend used by matplotlib. If the backend is not set to a GUI backend, it is possible not to display the plot. You can do this by adding the following code to your script:

```
import matplotlib
print(matplotlib.get_backend())
```

If the output is ‘Agg’ or ‘Cairo’, then change the backend to a GUI backend. 

2. Add the plt.ion() command to your code
Another solution is to add the `plt.ion()` command to your code after importing matplotlib. This command will enable interactive mode in matplotlib and allow for plotting to the screen. 

```
import matplotlib.pyplot as plt
plt.ion()
```

3. Add the plt.show() command to your code
If the above solutions do not work, you can try adding the `plt.show()` command to the end of your code. This command will display the plot in a new window. 

```
import matplotlib.pyplot as plt 
<code to create plot>
plt.show()
```

4. Turn on “Scientific Mode”
Lastly, you can turn on “Scientific Mode” in PyCharm. This mode comes with a built-in support for scientific libraries like Numpy and Matplotlib. You can do this by going to File -> Settings -> Editor -> General -> Appearance, and then ticking the “Scientific Mode” checkbox. 

With one or more of the above solutions, you should be able to display plots in PyCharm with ease.
