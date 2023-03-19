---
title: What is the method to print bold text in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can print bold text in Python by printing ANSI escape sequences using the format `\033[1m` and `\033[0m`.
---

**Contents**

[TOC]

# Introduction

When it comes to printing text in Python, you may sometimes want to emphasize certain words or phrases by making them bold. This can be useful for visualizing headings, important information or distinguishing certain aspects of output. In this guide, we will explore how to print bold text in Python using various methods.

# Using ANSI Escape Codes

One simple method to print bold text in Python is by using **ANSI escape codes**. These codes can modify the output of text by changing the color, style, or position of the text. To print bold text, we can use the `'\033[1m'` escape code before our desired text, and the `'\033[0m'` code after it, like so:

```python
print("\033[1m" + "This text is bold!" + "\033[0m")
```

This will produce the output:

```
This text is bold!
```

# Using Console Fonts

Another option to print bold text in Python is to use **console fonts**. Console fonts are pre-designed fonts that are supported by the terminal or command prompt. To access and use these fonts in your Python code, we will need to install and import a third-party library like **consolemd**, which provides various fonts to choose from. Here is an example:

```python
# Install consolemd library
!pip install consolemd

# Import the consolemd library
from consolemd import ConsoleMD

# Set the font style to bold
print(ConsoleMD("This text is bold!", style="bold"))
```

This will produce the output:

```
This text is bold!
```

# Using ASCII Art

Finally, an unconventional method to print bold text in Python is by using **ASCII art**. ASCII art is a form of illustration created by arranging characters to form images. By using ASCII characters, we can create bold text that is visually distinct. Here is an example:

```python
# Print a bold text message using ASCII art
print("""
888       888 d8b888 888   d8b 
888   o   888 Y8P888 888   Y8P 
888  d8b  888     888 888      
888 d888b 888 888 888 88888 
888d88888b888 888 888 888      
88888P Y88888 888 888 888      
8888P   Y8888 Y88b888 888      
                      v{0}
""".format(1))
```

This will produce the output:

```
888       888 d8b888 888   d8b 
888   o   888 Y8P888 888   Y8P 
888  d8b  888     888 888      
888 d888b 888 888 888 88888 
888d88888b888 888 888 888      
88888P Y88888 888 888 888      
8888P   Y8888 Y88b888 888      
                      v1
```

# Conclusion

There are several ways to print bold text in Python using ANSI escape codes, console fonts, and ASCII art. Each method has its own advantages and limitations, and you should choose the one that best suits your needs. With these techniques, you can enhance the readability and visual appeal of your Python scripts and applications.
