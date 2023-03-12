---
title: Obtain the chosen subcommand using argparse
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the `parse\_known\_args()` method in argparse to get the selected subcommand.
---

**Contents**

[TOC]

## Introduction
`argparse` is a module that provides a user-friendly way to parse command-line arguments in Python. It provides an easy way to define the expected arguments and options while executing the Python script from the command line. In this article, we will see how to get the selected subcommand with `argparse` in Python.

## Defining subcommands
One of the advantages of using `argparse` is that we can define subcommands that add functionality to our program. Subcommands are specified by a prefix argument followed by a string argument. Here is an example of how to define subcommands using the `add_subparsers()` method:

```python
import argparse

parser = argparse.ArgumentParser()

# Create a subparsers object
subparsers = parser.add_subparsers(dest='command')

# Create a parser for the 'foo' command
foo_parser = subparsers.add_parser('foo')

# Create a parser for the 'bar' command
bar_parser = subparsers.add_parser('bar')

# Parse the arguments
args = parser.parse_args()
```

In this example, we define two subcommands: `foo` and `bar`. The `dest` argument specifies the name of the variable that will hold the selected subcommand.

## Getting the selected subcommand
Once we have defined our subcommands, we can get the selected subcommand by accessing the `command` attribute of the parsed arguments. Here is an example:

```python
import argparse

parser = argparse.ArgumentParser()

# Create a subparsers object
subparsers = parser.add_subparsers(dest='command')

# Create a parser for the 'foo' command
foo_parser = subparsers.add_parser('foo')

# Create a parser for the 'bar' command
bar_parser = subparsers.add_parser('bar')

# Parse the arguments
args = parser.parse_args()

# Print the selected subcommand
print(args.command)
```

When we execute this script with the `foo` subcommand (`python example.py foo`), it will output:

```
foo
```

And when we execute it with the `bar` subcommand (`python example.py bar`), it will output:

```
bar
```

## Conclusion
In this article, we saw how to define subcommands using `argparse` and how to get the selected subcommand by accessing the `command` attribute of the parsed arguments. This is a powerful feature that allows us to create complex command-line interfaces with ease.
