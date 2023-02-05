---
title: Retrieving the exception value in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The exception value can be retrieved by using the `as` keyword in the except statement, followed by an exception variable name.
---

**Contents**

[TOC]

# Using try/except

The try/except block is a common way to handle exceptions in Python. The try block allows you to test a block of code for errors. The except block lets you handle the error.

## Syntax

The syntax for the try/except block in Python is:

```
try:
   # code block
except ExceptionName as e:
   # code block
```

## Example

Here is an example of a try/except block in Python:

```
try:
   a = int(input("Enter a number: "))
except ValueError as e:
   print("Not a valid number! Error:", e)
```

## Getting the Exception Value

The exception value can be accessed using the `e` variable in the except block. For example, in the above example, the `e` variable holds the exception value which is the error message.
