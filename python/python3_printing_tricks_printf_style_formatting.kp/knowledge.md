---
title: What is the equivalent of printf in python3 for printing?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the print() function with the format string.
---

**Contents**

[TOC]

Section 1: Introduction to Python's print() function

In Python programming, the print() function is used to display output on the screen. This function allows us to display text and numbers in the console or terminal window. In its simplest form, you can call the print() function with a string argument to display it on the console.

Section 2: Formatting output using string interpolation

Python provides several ways to format output using print(). One of the most common approaches is string interpolation. This technique allows you to embed variables and format strings into other strings.

For example, you can use the following code to insert a variable into a string:

```python
name = "John"
age = 30
print("My name is %s and I am %d years old." % (name, age))
```

You can also format a string using the format() method:

```python
name = "John"
age = 30
print("My name is {} and I am {} years old.".format(name, age))
```

Both of these methods allow you to format output in a similar way to printf() in C.

Section 3: Using f-strings for string interpolation

Since Python 3.6, f-strings have become an increasingly popular way to format output. An f-string is a special type of string literal that allows you to evaluate expressions inside curly braces. You can use f-strings to format output in a concise and readable way.

Here is an example:

```python
name = "John"
age = 30
print(f"My name is {name} and I am {age} years old.")
```

As you can see, the f-string syntax is similar to a regular string, but with an "f" prefix. Inside the string, you can embed expressions inside curly braces. These expressions are evaluated at runtime and their value is inserted into the string.

Section 4: Conclusion

In conclusion, Python's print() function provides a flexible and user-friendly way to display output on the screen. Whether you are formatting strings using string interpolation or f-strings, there are many ways to make your output look just the way you want it.
