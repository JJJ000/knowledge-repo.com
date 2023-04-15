---
title: Rephrased Python code containing lengthy lines should be appropriately formatted by wrapping them
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: It is recommended to wrap long lines of code in Python to improve readability and avoid horizontal scrolling.
---

**Contents**

[TOC]

Section 1: Introduction

When writing code in Python, it is common to come across lines that are longer than the standard 79 character limit recommended by the PEP 8 style guide. These long lines can make code difficult to read and understand, and can also cause formatting issues when printing or sharing code.

In this article, we will explore several methods for wrapping long lines in Python, including splitting lines with parentheses, using backslashes, and utilizing triple quotes.

Section 2: Splitting Lines with Parentheses

One common approach to wrapping long lines in Python is to split them into multiple lines using parentheses to indicate continuation. This method is useful when a single expression or statement is too long to fit on one line.

For example, consider the following line of code:

```
result = (num1 + num2 + num3 + num4 + num5 + num6 + num7 + num8 + num9 + num10)
```

This line exceeds the recommended 79 character limit and could be difficult to read. To wrap this line, we can split it into multiple lines using parentheses:

```
result = (num1 + num2 + num3 + num4 + num5
          + num6 + num7 + num8 + num9 + num10)
```

By splitting the line in this way, we have made the code easier to read and understand while still maintaining its functionality.

Section 3: Using Backslashes

Another method for wrapping long lines in Python is to use backslashes to indicate continuation. This method works well for splitting long strings or multiple lines of code into manageable sections.

For example, consider the following long string:

```
message = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
```

This string exceeds the recommended character limit and could be difficult to read. To wrap this string, we can use backslashes to indicate continuation:

```
message = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, \
           sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. \
           Ut enim ad minim veniam, quis nostrud exercitation ullamco \
           laboris nisi ut aliquip ex ea commodo consequat."
```

By using backslashes to split this string into multiple lines, we have made it more readable and easier to edit.

Section 4: Utilizing Triple Quotes

A third method for wrapping long lines in Python is to take advantage of triple quotes. Triple quotes allow us to define a string literal that spans multiple lines without using backslashes or parentheses.

For example, consider the following long string:

```
message = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
```

To wrap this string using triple quotes, we can do the following:

```
message = """Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud
exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor
in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur
sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est
laborum."""
```

By utilizing triple quotes, we have created a string that spans multiple lines and is easy to read and maintain.
