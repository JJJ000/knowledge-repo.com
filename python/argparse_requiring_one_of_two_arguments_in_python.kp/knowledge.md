---
title: Use argparse to demand one of two arguments
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the `nargs=`?`` argument in argparse to allow for either of two arguments to be inputted.
---

**Contents**

[TOC]

## Introduction
`argparse` is a standard Python module for creating command-line interfaces. It greatly simplifies the process of parsing command-line options and arguments for your Python scripts. There are cases when you need to require either of two arguments to pass during the script execution. This can be achieved by creating mutually exclusive groups of arguments. In this tutorial, we will see how to require either of two arguments using `argparse` in Python.

## Creating mutually exclusive groups
A mutually exclusive group is a way to specify that only one of a set of mutually exclusive arguments can be used at a time. This is often used to ensure that only one of two options is chosen. In `argparse`, a mutually exclusive group is created by calling the `add_mutually_exclusive_group()` method on an `ArgumentParser` object.

## Example Code
Here is an example code that shows how to require either of two arguments using `argparse` in Python:

```python
import argparse

parser = argparse.ArgumentParser()

group = parser.add_mutually_exclusive_group(required=True)
group.add_argument('-a', '--arg1', help='Option 1')
group.add_argument('-b', '--arg2', help='Option 2')

args = parser.parse_args()

if args.arg1:
    print("Option 1 was chosen")
else:
    print("Option 2 was chosen")
```

In this code, we create a mutually exclusive group by calling `add_mutually_exclusive_group()` on the `ArgumentParser` object. The `required=True` parameter specifies that at least one argument from the group is required. We then add two arguments to the group using `add_argument()`. The `-a`/`--arg1` and `-b`/`--arg2` options represent two mutually exclusive options. Finally, we parse the arguments using `parse_args()` and print the result depending on which argument was passed.

## Conclusion
In conclusion, `argparse` is a powerful tool for creating command-line interfaces in Python. The `add_mutually_exclusive_group()` method can be used to require either of two arguments by creating a mutually exclusive group of arguments. This ensures that only one of the two specified arguments is used at runtime.
