---
title: If 'x' is present, argument 'y' is mandatory in argparse
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the `required` attribute in argparse for argument `y` and add a custom condition in the `if` block for argument `x` to achieve the required behavior.
---

**Contents**

[TOC]

## Introduction
Argparse is a Python library that allows the creation of command-line interfaces with easy-to-understand commands and options. Sometimes, we want to specify conditions for the command-line arguments, such as requiring one argument to be present if another is. In this case, we want to require the argument "y" to be present if the argument "x" is present. 

## Defining Arguments
First, we need to define our arguments using argparse. We can add the "x" and "y" arguments using the `add_argument()` method. The `add_argument()` method takes several arguments such as the name of the argument, the type of the argument, the short and long forms of the argument, a help text, etc.

```python
import argparse

parser = argparse.ArgumentParser(description='Argument parser example')

parser.add_argument('-x', '--x', type=str, help='Argument x')
parser.add_argument('-y', '--y', type=str, help='Argument y')
```

## Adding Conditions
Then we can define our condition using the `add_argument_group()` method, which allows us to create a group of related arguments. We can add an argument group using the `add_mutually_exclusive_group(required=True)` method, which enforces that only one argument from this group is used. We add the condition using the `add_argument()` method.

```python
condition_group = parser.add_argument_group('condition group')

condition = condition_group.add_mutually_exclusive_group(required=True)
condition.add_argument('-x', '--x', help='Argument x', required=True)
condition.add_argument('-y', '--y', help='Argument y', required=False)
```

In this case, we add the "x" and "y" arguments to the "condition" group and require that one of them be present, but not both. 

## Checking for Conditions
Finally, we can check for our condition using the `parse_args()` method, which returns a Namespace object containing the values of the arguments. We can then check if "x" is present and "y" is not, and raise an error if this is the case.

```python
args = parser.parse_args()

if args.x and not args.y:
    parser.error("Argument '--y' is required when '--x' is present.")
```

This code checks if "x" is present and "y" is not. If this is the case, an error is raised stating that "--y" is required when "--x" is present.

## Conclusion
In conclusion, we can add conditions to argparse using an argument group with mutually exclusive arguments, and then check for the condition using the `parse_args()` method. In this case, we required the argument "y" to be present if the argument "x" is present, and raised an error if this condition was not met.
