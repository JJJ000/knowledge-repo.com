---
title: Adding characters to the beginning and end of a string
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: We can use string concatenation or string formatting methods to insert characters at the start and end of a string in Python.
---

**Contents**

[TOC]

Section 1: Introduction

In Python, we can insert characters at the start and end of a string by utilizing a few string manipulation methods. In this tutorial, we will explore the different methods that you can use to add characters to the beginning and end of a string.

Section 2: Adding characters to the start of a string

To add characters to the start of a string, we can use the concatenation operator (+) or the string formatting method. Here’s an example using the concatenation operator:

```python
string = "world"
new_string = "hello " + string
print(new_string) # Output: hello world
```

Alternatively, we can use the string formatting method to achieve the same result:

```python
string = "world"
new_string = "hello {}".format(string)
print(new_string) # Output: hello world
```

Section 3: Adding characters to the end of a string

To add characters to the end of a string, we can use the concatenation operator (+) or the string formatting method. Here’s an example using the concatenation operator:

```python
string = "hello"
new_string = string + " world"
print(new_string) # Output: hello world
```

Alternatively, we can use the string formatting method to achieve the same result:

```python
string = "hello"
new_string = "{} world".format(string)
print(new_string) # Output: hello world
```

Section 4: Conclusion

In this tutorial, we have explored the different methods that we can use to add characters at the start and end of a string in Python. By using either the concatenation operator or the string formatting method, we can easily manipulate strings to fit our needs.
