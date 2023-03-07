---
title: Reformulate determine the subparser that was utilized using argparse
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: You can identify which subparser was used in Python by accessing the `dest` attribute of the subparser object returned by `parse\_known\_args()`.
---

**Contents**

[TOC]

## Introduction
The `argparse` module in Python makes it easy to parse command-line arguments and options. It provides a way to define arguments and options, and parse them from the command-line input provided by the user. `argparse` also provides support for sub-commands, which adds another level of option and argument parsing for complex command-line interfaces. In this tutorial, we'll look at how to identify which sub-parser was used in Python using `argparse`.

## Step 1: Define sub-parsers
To identify which sub-parser was used in Python, we first need to define our sub-parsers using the `add_subparsers` method. This method creates a new sub-parsers object which can be used to add parsers for different sub-commands. Here is an example:

```python
import argparse

parser = argparse.ArgumentParser()
subparsers = parser.add_subparsers()
 
parser_foo = subparsers.add_parser('foo')
parser_bar = subparsers.add_parser('bar')
```

In this example, we define two sub-parsers, `foo` and `bar`.

## Step 2: Parse the command-line arguments
After defining the sub-parsers, we need to parse the command-line arguments using `parse_args` method of the parent parser (`parser.parse_args()`). 

```python
args = parser.parse_args()
```

`args` is an object that holds the parsed arguments, and we can access each argument through its name.

## Step 3: Identify which sub-parser was used
Once we have parsed the command-line arguments and stored them in the `args` object, we can identify which sub-parser was used by checking which attribute was set.

```python
if hasattr(args, 'foo'):
    print("foo sub-parser was used")
    
if hasattr(args, 'bar'):
    print("bar sub-parser was used")
```

Here, we use the built-in `hasattr()` function to check whether the `foo` or `bar` attribute is set in `args`. If the attribute is set, then we know that the corresponding sub-parser was used.

## Conclusion
In this tutorial, we looked at how to identify which sub-parser was used in Python using `argparse`. We first defined our sub-parsers, then parsed the command-line arguments using `parse_args()` method, and finally used the `hasattr()` method to identify which sub-parser was used. Understanding this concept will be useful in developing complex command-line interfaces using Python.
