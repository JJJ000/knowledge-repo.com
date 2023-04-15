---
title: Provide a lambda expression that triggers an exception
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: lambda raise Exception(`Error message`)
---

**Contents**

[TOC]

## Introduction
A lambda expression is an anonymous function in Python. It is defined using the keyword `lambda`, followed by a colon and the function's body. It can take any number of arguments but can only have one expression. In this article, we will see how to define a lambda expression that raises an Exception in Python.

## Using lambda to raise an Exception
To raise an Exception using a lambda expression, we need to define the lambda expression so that it returns an Exception. We can define an Exception using the `raise` keyword followed by a new instance of the Exception class. Here is an example:

```python
raise Exception("This is an exception raised from a lambda expression")
```

To define a lambda expression that raises this Exception, we can simply put this code inside a lambda function. Here is an example:

```python
raise_exception_lambda = lambda: raise Exception("This is an exception raised from a lambda expression")
```

Now we can call this lambda expression to raise the Exception:

```python
raise_exception_lambda()
```

## Example code
Here is the full example code that defines the lambda expression and calls it to raise an Exception:

```python
raise_exception_lambda = lambda: raise Exception("This is an exception raised from a lambda expression")
raise_exception_lambda()
```

When we run this code, it will raise the following Exception:

```
Exception: This is an exception raised from a lambda expression
```
