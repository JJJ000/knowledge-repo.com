---
title: What is the syntax for adding default parameters to functions when using type hinting?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Default parameters can be added to functions using type hinting by specifying the parameter name followed by an equal sign and the default value.
---

**Contents**

[TOC]

## Syntax

The syntax for adding default parameters to functions when using type hinting in Python is as follows:

```python
def function_name(parameter_name: type = default_value) -> return_type:
    # Function body
```

## Example

As an example, we can create a function called `add_numbers` that takes two numbers and returns their sum, with a default value of 0 for the second parameter:

```python
def add_numbers(num1: int, num2: int = 0) -> int:
    return num1 + num2
```

## Usage

We can then call the function with or without a second parameter:

```python
add_numbers(1) # returns 1
add_numbers(1, 2) # returns 3
```

## Benefits

Using default parameters with type hinting allows us to ensure that the function is always called with the correct types and to provide sensible defaults for optional parameters.
