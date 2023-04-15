---
title: What is the way to inform matplotlib that my plot is completed?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Call plt.show() to display the plot and once closed, the plot is finished.
---

**Contents**

[TOC]

Section 1: Ending a Plot in Matplotlib
To end a plot in Matplotlib, you need to execute a function that saves or displays the current figure. It is possible to save the figure to a file or display it on-screen depending on your needs. 

Section 2: Saving a Figure in Matplotlib 
Saving a figure in Matplotlib involves calling the savefig() function. The function takes a filename argument and an optional DPI (dots per inch) argument that specifies the resolution of the output file. For example, the code below saves the current figure as a PNG file with a DPI of 300 pixels.

```
import matplotlib.pyplot as plt
plt.plot([1, 2, 3, 4])
plt.ylabel('some numbers')
plt.savefig('myplot.png', dpi=300)
```

Section 3: Displaying a Figure in Matplotlib
To display a figure in Matplotlib, you can use the show() function. The show() function is a blocking function that displays the current figure until the user closes the window manually. If you have already saved the figure to a file or do not want to display the figure, you can skip calling show(). Here's an example of how to use show():

```
import matplotlib.pyplot as plt
plt.plot([1, 2, 3, 4])
plt.ylabel('some numbers')
plt.show()
```

Section 4: Closing a Figure in Matplotlib
Once you have finished with a plot, it is best to close the figure. You can close a figure by calling the close() function. By default, close() will close the current figure, but you can also close a specific figure by passing a reference to it. Here's an example of how to close the current figure:

```
import matplotlib.pyplot as plt
plt.plot([1, 2, 3, 4])
plt.ylabel('some numbers')
plt.show()
plt.close()
```

By calling close() after show(), you can free up memory and ensure that no additional changes are made to the figure.
