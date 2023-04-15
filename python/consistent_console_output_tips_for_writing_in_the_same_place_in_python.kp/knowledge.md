---
title: What is the way to write output in the same location on the console?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Using a combination of carriage return and print statements, you can overwrite the previous output and write in the same place on the console in Python.
---

**Contents**

[TOC]

# Introduction

When working with console output in Python, it is often desirable to write output in the same place on the console, rather than having new output overwrite old output. This can be especially useful for long-running processes or programs that require live feedback.

There are a few different techniques that can be used to achieve this effect, depending on the specific use case and requirements. In this article, we will explore some of the most common approaches to writing output in the same place on the console in Python.

# Using Carriage Returns

One simple way to write output in the same place on the console in Python is to use carriage returns (`\r`) to overwrite the previous output. The basic idea behind this technique is to construct a string containing the new output and any necessary control characters (such as carriage returns), and then write that string to the console using the `print()` function.

For example, consider the following code:

```
import time

for i in range(10):
    print(f"Counting: {i}\r", end="")
    time.sleep(1)
```

In this code, we use a `for` loop to count from 0 to 9, printing the current count to the console each second. However, instead of printing each count on a new line, we use a carriage return (`\r`) to overwrite the previous output. This causes the output to be printed in the same place on the console, giving the illusion of live updating.

# Using the Tqdm Library

Another useful tool for writing output in the same place on the console in Python is the `tqdm` library. This library provides a progress bar widget that can be used to display live updates for long-running processes.

To use the `tqdm` library, you first need to install it using pip:

```
pip install tqdm
```

Once you have installed the library, you can use it to wrap your existing code and generate a progress bar. For example:

```
import time
from tqdm import tqdm

for i in tqdm(range(10)):
    time.sleep(1)
```

In this code, we use the `tqdm` function to wrap our `for` loop, creating a progress bar that updates in real time. Each iteration of the loop is displayed as a new segment on the progress bar, and the bar itself is updated in place on the console each time a new segment is added.

# Using ANSI Escape Codes

Finally, it is also possible to use ANSI escape codes to write output in the same place on the console in Python. ANSI escape codes are special control sequences that can be used to perform various formatting and text manipulation operations, such as changing the color of text or moving the cursor around the console.

To write output in the same place on the console, we can use the ANSI escape sequence "\033[F", which moves the cursor up one line. By combining this with other formatting and manipulation codes, we can create complex visual displays that update in real time.

For example:

```
import time

for i in range(10):
    print("\033[F\033[K", end="")
    print(f"Counting: {i}")
    time.sleep(1)
```

In this code, we first use the escape sequence "\033[F" to move the cursor up one line, and then "\033[K" to clear that line. We then print the current count on the cleared line, effectively overwriting the previous output. Thanks to the use of escape codes, the display updates in real time, giving the impression of live updating.
