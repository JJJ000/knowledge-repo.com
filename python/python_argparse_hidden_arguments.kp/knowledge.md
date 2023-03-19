---
title: Modifying python's argparse to include concealed arguments
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: Hidden arguments can be created with Python argparse by adding them as optional arguments with no explicit mention in the help message using the `add\_argument` method`s `dest` parameter.
---

**Contents**

[TOC]

Introduction:
Python argparse module is used to create command-line interfaces for Python applications. It allows parsing of command-line arguments and options into a user-friendly interface. Often times, we want to create hidden arguments in the command-line interface that the user won't see. These hidden arguments can be useful for internal functionalities or debugging purposes.

Defining hidden arguments in argparse:
The argparse module allows us to create hidden arguments by setting the "help" parameter to argparse.SUPPRESS. This will suppress the display of the argument in the help menu while keeping it functional. Here's an example:

``` python
import argparse

parser = argparse.ArgumentParser()
parser.add_argument('--visible_arg', help='This is a visible argument')
parser.add_argument('--hidden_arg', help=argparse.SUPPRESS)

args = parser.parse_args()
```

Here, the "--visible_arg" argument will be visible in the help menu, while the "--hidden_arg" argument will be hidden.

Using hidden arguments in Python:
Once we have created the hidden argument, we can use it in our code just like any other argument. Here's an example:

``` python
import argparse

parser = argparse.ArgumentParser()
parser.add_argument('--visible_arg', help='This is a visible argument')
parser.add_argument('--hidden_arg', help=argparse.SUPPRESS)

args = parser.parse_args()

# Use the hidden argument in code
if args.hidden_arg:
    print('This argument is hidden, but still functional')
```

Here, we are checking if the hidden argument "--hidden_arg" is set, and if so, we are printing a message.

Benefits of hidden arguments:
Using hidden arguments in the command-line interface can be helpful for many reasons. Here are a couple of benefits:

1. Debugging purposes: Hidden arguments can be used to enable debugging functionalities in the code, which can aid in debugging issues that may arise.

2. Internal functionalities: Hidden arguments can also be used to enable internal functionalities, such as configuration options or special modes, that the user doesn't need to see or access directly.

Conclusion:
Creating hidden arguments in the Python argparse module can be useful for many purposes. By setting the "help" parameter to argparse.SUPPRESS, we can create hidden arguments that are functional but don't appear in the help menu. We can then use these hidden arguments in our code for debugging purposes or internal functionalities.
