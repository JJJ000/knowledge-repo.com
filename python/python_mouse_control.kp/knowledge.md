---
title: Manipulating the mouse using python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Yes, it is possible to control a mouse using Python using libraries such as pyautogui and pynput.
---

**Contents**

[TOC]

## Introduction

Python is a high-level programming language that is widely used for diverse purposes, including web development, data analysis, machine learning, and automation. One interesting application of Python is its ability to control the mouse pointer and simulate user-inputs. In this article, we will explore some ways to control the mouse using Python.


## Using the pyautogui module

The easiest way to control the mouse with Python is to use the pyautogui module. This module provides a set of functions that allow us to control the mouse pointer's movement and simulate mouse clicks and scrolling. Here is an example code that moves the mouse pointer to the center of the screen and clicks the left button:

```
import pyautogui

# move the mouse to the center of the screen
width, height = pyautogui.size()
pyautogui.moveTo(width/2, height/2)

# click the left button
pyautogui.click()
```

The `moveTo()` function moves the mouse pointer to the specified coordinates, and the `click()` function simulates a left-click. We can also specify the x and y coordinates of the mouse pointer relative to its current position using the `moveRel()` function.


## Using the pynput module

Another way to control the mouse with Python is to use the pynput module. This module provides a class called `Controller` that allows us to control the mouse pointer's movement and simulate mouse events such as clicks, scrolling, and drag-and-drop operations. Here is an example code that moves the mouse pointer to the center of the screen and clicks the left button:

```
from pynput.mouse import Controller, Button

# create an instance of the mouse controller
mouse = Controller()

# move the mouse to the center of the screen
width, height = mouse.position
mouse.position = (width/2, height/2)

# click the left button
mouse.press(Button.left)
mouse.release(Button.left)
```

The `Controller` class creates an instance of the mouse controller that we can use to control the mouse pointer. We can move the mouse pointer to the specified coordinates using the `position` attribute, and we can simulate mouse events such as clicks using the `press()` and `release()` methods.


## Using the ctypes module

Finally, we can also control the mouse with Python using the ctypes module, which allows us to call low-level C functions from Python. Here is an example code that moves the mouse pointer to the center of the screen and clicks the left button:

```
import ctypes

# define the ctypes structures and functions
class POINT(ctypes.Structure):
    _fields_ = [("x", ctypes.c_long), ("y", ctypes.c_long)]

def set_mouse_position(x, y):
    ctypes.windll.user32.SetCursorPos(x, y)

def left_click():
    ctypes.windll.user32.mouse_event(2, 0, 0, 0, 0)
    ctypes.windll.user32.mouse_event(4, 0, 0, 0, 0)

# move the mouse to the center of the screen
width = ctypes.windll.user32.GetSystemMetrics(0)
height = ctypes.windll.user32.GetSystemMetrics(1)
set_mouse_position(width//2, height//2)

# click the left button
left_click()
```

The `SetCursorPos()` function moves the mouse pointer to the specified coordinates, and the `mouse_event()` function simulates mouse events such as clicks, scrolling, and drag-and-drop operations. Since this method involves calling low-level C functions, we have to define the necessary structures and functions using the ctypes module.
