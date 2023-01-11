---
title: What is the command to print colored text to the terminal?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-11 00:00:00
updated_at: 2023-01-11 00:00:00
tldr: You can use the ANSI escape codes to print colored text to the terminal in Python.
---

**Contents**

[TOC]

### Using ANSI Escape Codes

The simplest way to print colored text to the terminal in Python is to use ANSI escape codes. ANSI escape codes are special characters that can be used to change the formatting of text, including its color.

For example, to print the text "Hello World" in green, you could use the following code:

```python
print("\033[32mHello World\033[0m")
```

The "\033[32m" before the text sets the text color to green, and the "\033[0m" after the text resets the text color to the default.

### Using the Colorama Module

Another way to print colored text to the terminal in Python is to use the Colorama module. Colorama is a third-party module that provides support for ANSI escape codes in Python.

For example, to print the text "Hello World" in green, you could use the following code:

```python
from colorama import init
init()

print(Fore.GREEN + "Hello World" + Style.RESET_ALL)
```

The "Fore.GREEN" sets the text color to green, and the "Style.RESET_ALL" resets the text color to the default.

### Using the Termcolor Module

Another way to print colored text to the terminal in Python is to use the Termcolor module. Termcolor is a third-party module that provides an easy-to-use interface for printing colored text.

For example, to print the text "Hello World" in green, you could use the following code:

```python
from termcolor import colored

print(colored("Hello World", "green"))
```

The "colored" function takes two arguments: the text to print and the color to print it in.
