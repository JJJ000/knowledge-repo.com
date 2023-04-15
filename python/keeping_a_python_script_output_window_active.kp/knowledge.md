---
title: What is the way to prevent a Python script output window from closing?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the input() function at the end of the script to prompt the user to press enter before closing the window.
---

**Contents**

[TOC]

## Introduction

When running a Python script in the terminal, the output window typically closes before you have a chance to read the output. In this tutorial, we will go through different approaches you can take to keep the Python script output window open, allowing you to read or analyze the output before exiting.

## Using the input() Function

One way to ensure that the script output window stays open is to use the built-in input() function. This function waits for the user to press the Enter key before continuing to the next line, thereby keeping the window open. 

Here is an example code snippet:

``` python
# your Python code here
print("Hello World!")
input("Press Enter to exit...")
```

In this example, the print() function displays "Hello World!" in the output window, and then the input() function waits for the user to press Enter to exit the window.

## Using a Command-Line Argument

Another approach you can take to keep the output window open is to pass a command-line argument when launching the script. The argument can then be used to keep the window alive even after the script has completed executing.

You can achieve this as shown below:

``` python
import sys

# your Python code here

if len(sys.argv) < 2 or sys.argv[1] != "exit":
    input("Press Enter to exit...")
```

In this example, we check if there are any command-line arguments passed when launching the script. If no argument is passed or the argument is not "exit", the input() function waits for the user to press Enter before exiting the window.

You can then launch the script using the CLI command `python script.py stay-open` to keep the output window open.

## Using a Third-Party Tool

Alternatively, you can use third-party tools such as PyInstaller and py2exe to create a standalone executable file. These tools have an option to keep the output window open after the script has completed executing, which can be enabled during the packaging process.

For example, using PyInstaller, you can add the following command to keep the window open:

`pyinstaller --noconsole --onefile --name=my_script my_script.py`

The `--noconsole` option removes the console window, and the `--onefile` option creates a single-file executable. The executable will run silently, but you can add the `--wait-for-process-exit` flag to keep the window open after the script has executed.

## Conclusion

In this tutorial, we have explored different approaches you can take to keep a Python script output window open. Whether using built-in functions such as input(), command-line arguments, or third-party tools, you can easily keep the window open to read or analyze the output.
