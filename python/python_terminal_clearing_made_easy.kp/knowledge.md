---
title: How to empty the Python terminal window?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To clear the terminal in Python, you can use the os module and call the system function with the clear command.
---

**Contents**

[TOC]

Clear Terminal in Python

There are several ways to clear the terminal in Python, depending on your operating system and the capabilities of your console or terminal emulator. Here are some possible approaches:

1. Using the os module

You can use the os module to execute a system command that clears the terminal. Here is an example code snippet that works on Windows, Linux, and macOS:

```python
import os

def clear_terminal():
    os.system('cls' if os.name == 'nt' else 'clear')
```

This code checks the value of os.name to determine whether the operating system is Windows ('nt') or not (e.g., 'posix' on Linux and macOS). It then executes the appropriate command ('cls' for Windows or 'clear' for other systems) using os.system(), which runs the command in a system shell.

2. Using the subprocess module

Alternatively or in addition to the os module, you can use the subprocess module to spawn a new process that runs the system command for clearing the terminal. Here is an example code snippet that uses subprocess.call():

```python
import subprocess

def clear_terminal():
    subprocess.call('cls' if os.name == 'nt' else 'clear', shell=True)
```

This code is similar to the previous one, but it passes shell=True to subprocess.call(), which tells it to use a system shell to execute the command. This can be useful if you need to chain multiple commands or use shell-specific features.

3. Using ANSI escape sequences

If you want a more low-level and cross-platform solution, you can use ANSI escape sequences to manipulate the terminal output. Here is an example code snippet that uses the 'clear screen' control sequence:

```python
def clear_terminal():
    print('\033[2J\033[1;1H', end='')
```

This code uses the escape sequence \033 (also known as the ESC character) followed by the [ character to start a control sequence. The sequence \033[2J is the 'clear screen' control sequence, which erases the entire terminal window. The sequence \033[1;1H is the 'move cursor' control sequence, which positions the cursor at the top-left corner of the screen. The end='' argument to print() avoids printing a newline character ('\n') after the escape sequences, which could cause additional blank lines to appear.

4. Using a third-party library

Finally, you can use a third-party library like curses or blessings to create more complex and interactive terminal applications that can clear the screen and manipulate text and colors with more granularity. However, this approach requires more advanced knowledge of terminal programming and may not be necessary for simple scripts or console utilities.
