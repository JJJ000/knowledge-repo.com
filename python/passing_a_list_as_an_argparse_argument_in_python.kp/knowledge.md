---
title: What is the syntax for passing a list as a command-line argument using argparse?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the action=`append` argument in argparse to allow a list of command-line arguments.
---

**Contents**

[TOC]

### 1. Create a parser

First, create a parser object using the `argparse.ArgumentParser()` constructor.

```
import argparse

parser = argparse.ArgumentParser()
```

### 2. Define a list argument

Next, define a list argument using the `add_argument()` method.

```
parser.add_argument('--list', nargs='+', type=str, help='A list of strings')
```

The `nargs` parameter specifies that the argument should be a list, and the `type` parameter specifies that the elements of the list should be strings.

### 3. Parse the arguments

Finally, parse the command-line arguments using the `parse_args()` method.

```
args = parser.parse_args()
```

### 4. Access the list

You can access the list argument from the `args` object.

```
list_arg = args.list
```
