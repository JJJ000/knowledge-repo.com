---
title: Debugging with ipython in a systematic manner
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: IPython allows for step-by-step debugging through the use of the %debug and %pdb commands.
---

**Contents**

[TOC]

Section 1: Introduction to IPython and Debugging

IPython is an enhanced interactive Python shell that offers many useful features, including advanced debugging tools. With IPython's debugger, you can step through code one line at a time, examine variables, and interactively evaluate expressions to quickly find and fix errors in your code. In this tutorial, we'll walk through the process of debugging code using IPython's built-in debugger.

Section 2: Setting up Debugging with IPython

To start debugging with IPython, you need to set a breakpoint in your code by adding the "set_trace()" function from the "pdb" module. You can add this function to any line of code where you want to pause the execution and start the debugger.

```
import pdb

def my_function(x, y):
    z = x + y
    pdb.set_trace()  # set breakpoint
    return z

result = my_function(2, 3)
print(result)
```

When your program reaches the breakpoint, it will pause the execution and start the IPython debugger.

Section 3: Debugging with IPython commands

Once the code is paused at the breakpoint, you can use IPython commands to interact with the code and inspect its state. Some useful IPython commands for debugging include:

- **n**: execute the current line and continue to the next line
- **s**: step into a function call
- **c**: continue running the program until the next breakpoint is hit
- **p varName**: print the value of a variable
- **q**: quit the debugger and abort the program

Here's an example of using these commands to debug the "my_function" function:

```
> <ipython-input-1-2d64284c40f5>(5)my_function()
      4     z = x + y
----> 5     pdb.set_trace()  # set breakpoint
      6     return z

ipdb> p x
2
ipdb> n
> <ipython-input-1-2d64284c40f5>(6)my_function()
      5     pdb.set_trace()  # set breakpoint
----> 6     return z
      7
ipdb> p y
3
ipdb> c
5
```

In this example, we use the "p" command to print the values of the "x" and "y" variables. We then use the "n" command to execute the current line of code and move to the next line. Finally, we use the "c" command to continue running the program until the next breakpoint is hit.

Section 4: Conclusion

Debugging with IPython can be a powerful tool for quickly identifying and fixing errors in your code. With IPython's advanced debugging tools and intuitive command interface, you can easily step through code one line at a time, inspect variable values, and evaluate expressions to troubleshoot and fix issues in your code.
