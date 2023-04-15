---
title: The automatic reloading of modules in ipython
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: IPython has a built-in autoreload extension that allows modules to be reloaded automatically whenever changes are made to its code.
---

**Contents**

[TOC]

Section 1: Overview

Autoreload is a useful feature in IPython that automatically reloads updated Python modules. This feature saves time and hassle because you don't have to manually reload updated modules every time you make a new change.

Section 2: Enabling Autoreload in IPython

To enable autoreload in IPython, you can use the %autoreload magic command. This command has three possible values:

1. %autoreload 0: turn off autoreload
2. %autoreload 1: autoreload Python modules that are imported into IPython (useful for interactive work)
3. %autoreload 2: autoreload all Python modules, whether they are imported or not (useful for development work)

To use autoreload, you simply type the %autoreload magic command in IPython followed by the desired value. For example, to enable autoreload for all Python modules, you would type:

%autoreload 2

Section 3: Examples of Autoreload in IPython

Here is an example of how autoreload can be useful. Suppose you have a module called mymodule.py that contains a function called add_numbers. You import this module into IPython and use the function as follows:

import mymodule
mymodule.add_numbers(1, 2)

Now suppose you make a change to the add_numbers function in the mymodule module. Normally, you would have to reload the module before you can see the updated function. However, if you have autoreload enabled, you don't have to do this – the updated function will be automatically reloaded. For example:

%autoreload 1
mymodule.add_numbers(1, 2) # this will still use the old version
# make a change to add_numbers in mymodule
mymodule.add_numbers(1, 2) # this will now use the updated version

Section 4: Conclusion

Autoreload is a useful feature in IPython that can save time and hassle when working with Python modules. By using the %autoreload magic command, you can enable autoreload and specify which modules should be reloaded automatically. This feature is especially useful for interactive and development work where you need to quickly see the effects of changes to your code.
