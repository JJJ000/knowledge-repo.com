---
title: What is the syntax for continuing a string on multiple lines in python's coding convention?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: Use parentheses to continue strings over multiple lines in Python.
---

**Contents**

[TOC]

There are different ways to handle line continuation in Python when working with strings. In this response, we will explore two main approaches: using the backslash character and using parentheses.

Backslash character

One common way to handle line continuation with strings in Python is by using the backslash character (\). This special character allows us to split long strings over multiple lines. Here's an example:

```python
message = "Hello, this is a long string \
that continues on the next line."
```

In the above code, the backslash character at the end of the first line tells Python that the string continues on the next line. Note that there's no space between the backslash and the carriage return character (\n), which separates the lines.

Parentheses

Another way to handle line continuation with strings in Python is by using parentheses. This method offers more flexibility and can be used with multiple lines of code. Here's an example:

```python
message = ("Hello, this is a long string "
           "that continues on the next line. "
           "And here is another line.")

```

In the above code, we've created a tuple with three string elements. The parentheses allow us to split the strings over multiple lines, without using any special characters. This approach can be useful when we want to continue working with a multiline string in our code.

Conclusion

Overall, there are various ways to handle line continuation with strings in Python. The best approach depends on the specific requirements of your code and the preferred coding style. Both the backslash and parentheses methods offer practical ways to split long strings over multiple lines, depending on the situation.
