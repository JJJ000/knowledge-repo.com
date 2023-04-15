---
title: What is the method to limit a value obtained through argparse (e.g., confine an integer to only positive values)?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use the `type` parameter in `add\_argument` method to define a custom function that validates and converts the argument value.
---

**Contents**

[TOC]

## Introduction

The `argparse` module in Python is a module that makes it easy to write user-friendly command-line interfaces. It allows developers to specify expected command-line arguments and options in a way that is both human-readable and machine-parsable. Moreover, in order to avoid entering wrong values, the `argparse` module provides ways to constrain values parsed with it. This can be done by setting limits on the values which can be entered by the user. In this article, we will discuss how to constrain values parsed with argparse in Python.


## Restricting integers to positive values

One simple way to constrain a value parsed with `argparse` is to place a limit on the values that the user can enter. For example, we can restrict an integer to positive values as shown in the code below. 

```python
import argparse

parser = argparse.ArgumentParser()
parser.add_argument('--value', type=int, metavar='N', required=True, help='an integer value greater than zero')
args = parser.parse_args()

if args.value <= 0:
    raise argparse.ArgumentTypeError('Value "{}" must be greater than zero.'.format(args.value))
```

Here, we have used the `add_argument()` method to define an argument named `value`. The `type` parameter is set to `int`, which means that the value entered by the user will be parsed as an integer. We have also added a `metavar` parameter to specify the name of the argument in the help message. The `required` parameter is set to `True` to ensure that the user enters a value for this argument. Finally, we have included a `help` message to describe what this argument is for.

After parsing the command-line arguments using `parse_args()`, we can check if the value of `args.value` is less than or equal to zero. If it is, we can raise an error with a custom message using `ArgumentTypeError()`.


## Restricting floats to a range of values

We can also restrict floats to a range of values using the `add_argument()` method. We can specify the minimum and maximum values using the `type` parameter and the `metavar` parameter. For example, we can restrict a float to values between 0.0 and 1.0 as shown in the code below.

```python
import argparse

def float_range(value):
    fvalue = float(value)
    if fvalue < 0.0 or fvalue > 1.0:
        raise argparse.ArgumentTypeError('Value "{}" must be between 0.0 and 1.0.'.format(value))
    return fvalue

parser = argparse.ArgumentParser()
parser.add_argument('--value', type=float_range, metavar='N', required=True, help='a float value between 0.0 and 1.0')
args = parser.parse_args()
```

Here, we have used a custom function `float_range` to constrain the value of the `value` argument to a range between 0.0 and 1.0. This function takes the argument value as input, and returns the same value as a float if it is within the range. If it is not within the range, it raises an error with a custom message using `ArgumentTypeError()`.

We have then included this function as the `type` parameter in the `add_argument()` method, which means that the input value will be passed through the `float_range()` function and checked for validity.


## Restricting strings to a list of choices

We can also restrict a string to a list of choices using the `choices` parameter in the `add_argument()` method. This parameter takes a list of valid choices for the argument. If the user enters a value that is not in the list of choices, an error will be raised.

```python
import argparse

parser = argparse.ArgumentParser()
parser.add_argument('--color', choices=['red', 'green', 'blue'], required=True, help='choose a color')
args = parser.parse_args()
```

Here, we have created an argument named `color` using the `add_argument()` method. We have included a list of valid choices for this argument using the `choices` parameter. If the user enters a value that is not in this list, an error will be raised.


## Conclusion

In this article, we have discussed how to constrain values parsed with `argparse` in Python. We have seen how to restrict an integer to positive values, restrict a float to a range of values, and restrict a string to a list of choices. By setting limits on the values that can be entered by the user, we can ensure that the input values are valid and within a specified range.
