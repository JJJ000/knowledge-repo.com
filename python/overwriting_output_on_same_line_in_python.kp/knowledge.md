---
title: Can you produce output on the same line by replacing previous output?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the carriage return (\r) character to return the cursor to the beginning of the line and overwrite the previous output.
---

**Contents**

[TOC]

I'm sorry, as an AI language model, I do not have the capability to display outputs in an interactive or graphical user interface such as overwriting previous output in Python. However, I can provide you with some possible ways on how to achieve this.

1. Using the Carriage Return character (\r)
One way to output to the same line and to overwrite the previous output in Python is by using the carriage return character (\r). The carriage return character moves the cursor to the beginning of the current line without advancing to the next line, allowing you to rewrite what was previously printed.

```python
import time

for i in range(100):
    # Print the current value of i on the same line
    print(f"Value of i is: {i}\r", end="")
    time.sleep(0.1)
```
2. Using the end parameter
Another way is to use the end parameter of the print function. By default, the end parameter value is set to "\n", which means that the output will be printed on a new line. But you can change it to a space " " or an empty string "" to output on the same line.

```python
import time

for i in range(100):
    # Print the current value of i on the same line
    print(f"Value of i is: {i}", end="\r")
    time.sleep(0.1)
```

3. Using the built-in library, Tqdm
The Tqdm library can be used to output to the same line overwriting existing output with a progress bar. This library can be used to track the progress of a process such as downloading or uploading files.

```python
from tqdm import tqdm
import time

for i in tqdm(range(100)):
    time.sleep(0.1)
```

4. Using Backspace character (\b) 
Another way is by using the backspace character (\b) along with the `\r` character. The backspace removes the character just printed and the `\r` moves the cursor back to the beginning of the line.

```python
import time

for i in range(10):
    print("Loading" + "." * i, end="\r")
    time.sleep(1)
print("\nDone!")
```

I hope one of these methods helps you achieve what you want to do.
