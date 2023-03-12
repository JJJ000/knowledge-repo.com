---
title: Verify whether the optional argument in argparse has been configured or not
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use `args.<argument>` to access the value of an optional argument parsed by argparse, which will return the default value specified in `parser.add\_argument` if the argument was not provided at runtime.
---

**Contents**

[TOC]

## Introduction
In Python, argparse is a module that is used for parsing command-line arguments. It makes it easy to write user-friendly command-line interfaces for your programs. It allows you to specify both required and optional arguments, and take actions based on those arguments. 

In this tutorial, we will see how to check if an optional argument is set or not using argparse in Python.

## Defining the argument parser
Firstly, we need to define our argument parser using the `argparse` module. We can do this by creating an instance of ArgumentParser and setting the required arguments and the optional arguments with their default values.

```python
import argparse

parser = argparse.ArgumentParser()
parser.add_argument("required_argument", help="This is a required argument.")
parser.add_argument("--optional_argument", help="This is an optional argument.", default=None)

args = parser.parse_args()
```

In the above code, we have defined two arguments, `required_argument` and `optional_argument`. The former is a required argument, which means it must be passed when the script is run. The latter is optional and has a default value of `None`.

## Checking if an optional argument is set
Once the arguments are defined and parsed, we can then check if the optional argument is set or not. If the optional argument is set, its value will not be `None`. 

```python
if args.optional_argument is not None:
    print("The optional argument is set to:", args.optional_argument)
else:
    print("The optional argument is not set.")
```

In the above code, we are checking if the optional argument is `None` or not. If it is not `None`, that means it has been set, and its value is printed.

## Using `default` argument
We have already set a `default` value for the optional argument. If the user does not provide a value for the optional argument, the `default` value will be used.

```python
if args.optional_argument == parser.get_default('optional_argument'):
    print("The optional argument is not set and is using the default value.")
else:
    print("The optional argument is set to:", args.optional_argument)
```

In the above code, we are checking if the optional argument is set to the `default` value or not. If it is set to the `default` value, that means it has not been set explicitly and is using the default value.

## Conclusion
In this tutorial, we have seen how to check if an optional argument is set or not in Python using argparse module. We have also seen how to use the `default` argument to set a default value for the optional argument.
