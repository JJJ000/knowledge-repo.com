---
title: Execute a function from the command prompt
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Run a Python script from the command line by typing `python <scriptname>.py` into the terminal.
---

**Contents**

[TOC]

# Section 1: Set up Command Line Arguments

In order to run a function from the command line in Python, the first step is to set up the command line arguments. This is done by importing the `argparse` module and creating an `ArgumentParser` object. This object will be used to parse the command line arguments.

# Section 2: Define Function

The next step is to define the function that will be run from the command line. This function should take in the command line arguments as parameters and should contain the code that needs to be executed.

# Section 3: Add Arguments to ArgumentParser

The third step is to add the command line arguments to the ArgumentParser object. This is done by calling the `add_argument()` method and specifying the name, type, and help message for the argument.

# Section 4: Execute Function

The final step is to execute the function with the command line arguments. This is done by calling the `parse_args()` method on the ArgumentParser object, which will return the parsed arguments. These arguments can then be passed to the function, which will be executed with the given arguments.
