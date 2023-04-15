---
title: Using argparse to process boolean values
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: Argparse can parse boolean values using the action argument with the value `store\_true` or `store\_false`.
---

**Contents**

[TOC]

# Section 1: Overview

Argparse is a popular Python module that provides a simple way to parse command line arguments. It can also be used to parse boolean values, which are values that represent true or false. Boolean values can be used to control the behavior of a program or to enable or disable certain features.

# Section 2: Parsing Boolean Values

Parsing boolean values with argparse is relatively straightforward. All that needs to be done is to specify the type of the argument as a boolean when adding it to the argument parser. This can be done using the `add_argument` method, which takes the argument’s name, type, and other optional parameters. For example, to add a boolean argument called “verbose”, the following code can be used:

```python
parser.add_argument("--verbose", type=bool, default=False)
```

# Section 3: Accessing the Argument

Once the argument has been added to the argument parser, it can be accessed by using the `parse_args` method. This method returns an object that contains the values of all the arguments that were specified. To access the value of the “verbose” argument, the following code can be used:

```python
args = parser.parse_args()
if args.verbose:
    print("Verbose mode enabled")
```

# Section 4: Conclusion

Parsing boolean values with argparse is a simple and straightforward process. By specifying the type of the argument as a boolean when adding it to the argument parser, the value of the argument can be accessed and used to control the behavior of a program.
