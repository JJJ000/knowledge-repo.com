---
title: What is the way to obtain monitor resolution using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: You can use the `win32api` module to get the monitor resolution in Python on Windows, while on other platforms you can use the `Xlib` or `pyobjc` modules.
---

**Contents**

[TOC]

## Using the `pyautogui` module

The `pyautogui` module has a function called `size()` which can be used to get the screen resolution of the monitor. 

```python
import pyautogui

width, height = pyautogui.size()
print("Monitor Resolution: {} x {}".format(width, height))
```

This will output the monitor resolution in pixels in the format `Monitor Resolution: <width> x <height>`.

## Using the `Tkinter` module 

The `Tkinter` module is used to create GUI applications in Python. It also has a `winfo_screenwidth()` and `winfo_screenheight()` method which can be used to get the screen resolution in pixels.

```python
import tkinter

root = tkinter.Tk()
screen_width = root.winfo_screenwidth()
screen_height = root.winfo_screenheight()
print("Monitor Resolution: {} x {}".format(screen_width, screen_height))
```

## Using the `win32api` module 

The `win32api` module provides access to many of the low-level APIs in Windows. One of its functions is `GetSystemMetrics()` which can be used to get the resolution of the primary monitor in pixels.

```python
import win32api

width = win32api.GetSystemMetrics(0)
height = win32api.GetSystemMetrics(1)
print("Monitor Resolution: {} x {}".format(width, height))
```

## Using the `screeninfo` module

The `screeninfo` module is a cross-platform Python library for getting monitor information. It includes a easy-to-use Monitor class for accessing information on different monitors, as well as tools for working with monitor resolution.

```python
import screeninfo

monitors = screeninfo.get_monitors()
for m in monitors:
    print("Monitor Resolution: {} x {}".format(m.width, m.height))
```

This will output the resolution of all connected monitors. If there is only one monitor connected, it will output its resolution.
