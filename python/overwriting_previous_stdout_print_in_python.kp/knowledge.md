---
title: What is the method for replacing the previous output to stdout?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use `\r` at the beginning of the string to return the cursor to the beginning of the line and overwrite the previous output.
---

**Contents**

[TOC]

Introduction
------------
In Python, the `print()` function is used to output data to the console or terminal. However, there are situations where we might want to overwrite the previous print statement instead of printing a new line. In this article, we will explore different ways to achieve this in Python.

Using carriage return ('\r')
---------------------------
We can use the carriage return (`'\r'`) character to overwrite the previous print statement in Python. The carriage return character moves the cursor to the beginning of the line without advancing to the next line. This allows us to overwrite the previous print statement.

```python
import time

for i in range(10):
    print(i, end='\r')
    time.sleep(1)
```
In the above code, we used the `end` parameter of the `print()` function to set the string to be printed at the end of the line as `\r`. This causes the cursor to return to the beginning of the line after each iteration of the loop. We also use the `time.sleep()` function to pause the program for 1 second before printing the next iteration of the loop. This gives us the illusion that the previous print statement is being overwritten.

Using ANSI escape sequences
---------------------------
We can also use ANSI escape sequences to overwrite the previous print statement in Python. ANSI escape sequences are special codes that can be used to control the formatting of console output. In this case, we can use the CSI (Control Sequence Introducer) escape sequence to move the cursor to the beginning of the line and erase the previous line.

```python
import time

for i in range(10):
    print(f"\033[2K\033[1G{i}", end="")
    time.sleep(1)
```
In the above code, we used the `"\033[2K\033[1G"` sequence to erase the previous line and move the cursor to the beginning of the line. We then print the current iteration of the loop using an f-string. We also use the `end` parameter of the `print()` function to set the string to be printed at the end of the line as an empty string (`""`). This prevents the cursor from advancing to the next line after each iteration of the loop.

Using the `curses` module
-------------------------
The `curses` module in Python provides a way to create interactive console applications with support for keyboard input, colors, and cursor movement. We can use the `curses` module to overwrite the previous print statement by moving the cursor to the beginning of the line and printing over the previous text.

```python
import curses
import time

stdscr = curses.initscr()

for i in range(10):
    stdscr.addstr(0, 0, str(i))
    stdscr.refresh()
    time.sleep(1)
```
In the above code, we use the `curses.initscr()` function to initialize the curses library and create a window for our program. We then use the `stdscr.addstr()` function to print the current iteration of the loop at coordinates `(0, 0)` (top-left corner of the window). We also use the `stdscr.refresh()` function to update the contents of the window. Finally, we use the `time.sleep()` function to pause the program for 1 second before printing the next iteration of the loop.

Conclusion
----------
In this article, we explored different ways to overwrite the previous print statement in Python. We saw that we can use the carriage return character, ANSI escape sequences, or the `curses` module to achieve this. Knowing these techniques can be useful when building console applications that require updating the output in real-time.
