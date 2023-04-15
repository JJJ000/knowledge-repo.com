---
title: If not specified, argparse will set the value to false
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: By default, argparse treats options that aren`t specified on the command line as False.
---

**Contents**

[TOC]

## Understanding the `argparse` Module in Python
Before we can understand how to store false if a command line argument is unspecified, we need to have an understanding of the `argparse` module in Python. This module provides a way for us to declare the arguments we're expecting for our program and parse them from the command line. We declare our arguments and their type and store them in a Namespace object to be used later in our program. 

## The `store_true` and `store_false` Action in `argparse`
`argparse` provides two actions to handle Boolean arguments: `store_true` and `store_false`. When an argument is declared with `store_true`, the value of the argument is set to `True` if the argument is specified on the command line. Similarly, if an argument is declared with `store_false`, the value of the argument is set to `False` if the argument is specified on the command line. 

## Storing False if Unspecified 
To store `False` if an argument is unspecified, we need to declare our argument with `store_true` and then negate the value when we want to use it. For example, let's say we have a program that takes a `--debug` flag to indicate whether to print debug information or not. We can declare this argument as follows:

```
parser.add_argument('--debug', dest='debug', action='store_true', help='turn on debug mode')
```
Now, when we parse our arguments, if `--debug` is specified, the value of `debug` will be set to `True`. To use this value as `False` when `--debug` is not specified, we would negate it when we use it in our program:
```
if not args.debug:
    # debug mode is off
else:
    # debug mode is on
```
This will handle the case where the `--debug` flag is not specified and set `debug` to `False`.
