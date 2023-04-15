---
title: The action of using ctrl+c to end or terminate python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Pressing Ctrl+C sends a signal to the Python interpreter to interrupt and stop the current program execution.
---

**Contents**

[TOC]

## Introduction

When running a Python program in a terminal or shell, it is possible to stop or interrupt the program using a keyboard shortcut. This can be useful when a program is taking too long to execute or if you need to stop it for any other reason. In this article, we will learn how to stop a Python program using the `ctrl+c` keyboard shortcut.

## Using Ctrl+C to Stop a Python Program

The `ctrl+c` keyboard shortcut is a common way to stop a running program in a Unix/Linux shell environment. When this shortcut is pressed, a keyboard interrupt signal is sent to the running program, which allows it to gracefully exit the execution.

In Python, you can use `ctrl+c` to stop a program if it is running in a terminal or console window. When you press `ctrl+c`, the `KeyboardInterrupt` exception is raised in the program, which can be used to gracefully exit the program.

Here is an example Python program that can be used to demonstrate how to stop a program using `ctrl+c`:

```
import time
 
try:
    while True:
        print("Hello, World!")
        time.sleep(1)
except KeyboardInterrupt:
    print("Stopping the program...")
```

In this example, we have created an infinite loop that prints the message `Hello, World!` every second. However, we have wrapped this loop in a `try` block and included an `KeyboardInterrupt` exception handler. If you run this program in a terminal or console window, you can stop it at any time by pressing `ctrl+c`.

## Conclusion

In this article, we have learned how to stop a Python program using the `ctrl+c` keyboard shortcut. When you press `ctrl+c`, a `KeyboardInterrupt` exception is raised, which can be used to gracefully exit the program. This technique is useful when a program is taking too long to execute, or if you need to stop it for any reason. Remember to always include an exception handler in your code when using this technique to avoid abrupt program termination.
