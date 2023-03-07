---
title: Could you phrase "clear cell output in code on ipython notebook?"
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: To clear cell output in code, use the IPython.display.clear\_output() method.
---

**Contents**

[TOC]

Section 1: Introduction
In this tutorial, we will discuss how to clear cell output in the code using the IPython Notebook. Sometimes, when we run a code cell, it generates a lot of output, and we may want to clear it to focus on the essential parts of the code. In the IPython notebook, we can clear the output of a cell using built-in functions or keyboard shortcuts. Let's dive into it.

Section 2: Clearing output using built-in functions
To clear the output of a cell, we can use the `IPython.display.clear_output` function. This function takes three arguments: `wait`, `stdout`, and `stderr`. The `wait` argument tells the function whether to wait for new output before clearing the cell. If set to `True`, the function will not clear the cell until new output is generated. The `stdout` and `stderr` arguments tell the function which output streams to clear. By default, both streams are cleared.

Here is an example of how to use the `IPython.display.clear_output` function:

```
from IPython.display import clear_output

# Some code generating output
print("Hello World!")

# Clear output
clear_output(wait=True)
```

In this example, we first generate some output with the `print` function. Then, we call the `clear_output` function with the `wait` argument set to `True`. This tells the function to wait for new output before clearing the cell.

Section 3: Clearing output using keyboard shortcuts
In addition to using the `clear_output` function, we can also clear the output of a cell using keyboard shortcuts. To clear the output, we need to select the cell and press `Shift + O`. This will toggle the output visibility, and the output will disappear. 

If we want to clear the output and keep the output area closed, we can press `Esc` to go into command mode and then press `Shift + O`. This will clear the output and leave the output area closed.

Section 4: Conclusion
In this tutorial, we discussed how to clear the output of a cell in the IPython Notebook using built-in functions and keyboard shortcuts. Clearing the output of a cell is useful when we want to focus on the essential parts of the code, or when the output is too cluttered. By using these techniques, we can keep the notebook clean and organized.
