---
title: How to obtain user input and manipulate it as a string without using quotes in Python 2.7?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-15 00:00:00
updated_at: 2023-03-15 00:00:00
tldr: To get user input and manipulate it as a string in Python 2.7 without quotations, use the raw\_input() function.
---

**Contents**

[TOC]

# Section 1: Getting User Input in Python 2.7

To get user input in Python 2.7, we use the `raw_input()` function. Here's an example:

```
name = raw_input("Enter your name: ")
```

This will prompt the user to enter their name and store the input as a string in the `name` variable.


# Section 2: Manipulating User Input as a String

Once we have the user input as a string, we can manipulate it using various string methods. For example, we can convert the string to all uppercase or lowercase using the `upper()` or `lower()` method, respectively:

```
name_uppercase = name.upper()
name_lowercase = name.lower()
```

We can also extract specific characters or substrings using indexing and slicing. For example, to get the first letter of the name, we can do:

```
first_letter = name[0]
```

And to get the first three letters, we can do:

```
first_three_letters = name[:3]
```

There are many more string methods available in Python, so be sure to check the documentation for more information.


# Section 3: Using User Input Without Quotations

If we want to use user input as a variable without having to wrap it in quotes, we can use the `eval()` function. For example:

```
name = raw_input("Enter your name: ")
eval("print " + name)
```

This will print the value of the `name` variable without the quotes.


# Section 4: Beware of Security Risks with `eval()`

Note that using `eval()` to execute arbitrary code can be dangerous, as it can allow an attacker to execute malicious code. So be sure to only use `eval()` on trusted input, or find alternative solutions that don't involve executing user input as code.
