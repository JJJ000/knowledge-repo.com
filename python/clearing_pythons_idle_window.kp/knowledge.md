---
title: Is there a method to erase the Python idle window?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: You can clear Python`s IDLE window by using the shortcut Ctrl + Shift + F6.
---

**Contents**

[TOC]

## Using built-in functions

Python's IDLE window has a built-in function called `clear()` which clears the screen by moving the cursor to the top left corner. However, this function does not work on all platforms. To use it, simply type `clear()` and hit enter on the IDLE window.

## Using keyboard shortcuts

Another way to clear the IDLE window is by using keyboard shortcuts. On Windows, you can press `Ctrl+Shift+L` to clear the screen. On a Mac, you can press `Cmd+Shift+K`.

## Running a system command

You can also clear the IDLE window by running a system command from within Python. To do this, you can use the `os` module. 

```python
import os
os.system('clear')
```

This will clear the IDLE window by running the `clear` command in the terminal.

## Writing a custom function

If none of the above methods work, you can write a custom function to clear the IDLE window. Here's an example:

```python
def clear():
    import os
    os.system('cls' if os.name == 'nt' else 'clear')
```

This function first checks the operating system and uses the appropriate command to clear the screen. You can then call this function anytime you want to clear the IDLE window.
