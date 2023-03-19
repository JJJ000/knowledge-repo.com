---
title: Reworded python's f-string feature allows for multiline strings
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Multiline f-strings are possible in Python by enclosing them with triple quotes and using curly braces to insert variables or expressions.
---

**Contents**

[TOC]

Introduction
------------
f-strings are a powerful feature in Python that enable string formatting by directly embedding expressions inside string literals. While f-strings can span over multiple lines, the syntax can become tricky when dealing with complex expressions or template strings. This article explores various ways to create multiline f-strings in Python.

Using Backslashes
------------------
One way to create multiline f-strings is by using backslashes. Consider the following example:

```python
name = "Alice"
age = 30

greeting = f"Hello, \
{name}! \
You are {age} years old."
```

This f-string takes advantage of the backslash character to escape the newline character and join the multiple strings together into a single line. The output would be:

```python
Hello, Alice! You are 30 years old.
```

Using Parentheses
------------------
Another way to create multiline f-strings is by using parentheses. Consider the following example:

```python
name = "Bob"
age = 40

greeting = (
    f"Hello, "
    f"{name}! "
    f"You are {age} years old."
)
```

This f-string uses parentheses to group multiple f-strings as a single expression. Each f-string can be on a separate line and indented as needed for readability. The output would be the same as the previous example.

Using Triple Quotes
-------------------
A third way to create multiline f-strings is by using triple quotes. Consider the following example:

```python
name = "Charlie"
age = 50

greeting = f"""Hello, 
{name}! 
You are {age} years old."""
```

This f-string uses triple quotes to create a multiline string literal. The expressions inside the f-string can span multiple lines as needed. Note the use of a newline character at the end of the first line to properly separate the f-string from the plain text. The output would be the same as the previous examples.

Conclusion
----------
In conclusion, there are several ways to create multiline f-strings in Python. Depending on the context, using backslashes, parentheses, or triple quotes can help make your code more readable and maintainable. Use whichever method suits your coding style and preferences.
