---
title: Disregard unacknowledged arguments in python's argparse
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Set the `allow\_abbrev` attribute of the `ArgumentParser` object to `True` to ignore unrecognised arguments in Python argparse.
---

**Contents**

[TOC]

Section 1: Introduction 
`argparse` is a standard Python library used for parsing command-line arguments. It provides several features like automatically generating help messages, checking argument types, and handling errors. One common problem that users face when using `argparse` is that it raises an error when an unrecognised argument is passed to it. 

Section 2: Solution 
There is a way to make `argparse` ignore unrecognised arguments. You can define a special argument parser called `ArgumentParser(allow_abbrev=False, argument_default=None, conflict_handler='error', prog=None, usage=None, description=None, epilog=None, parents=[], formatter_class=<class 'argparse.HelpFormatter'>, prefix_chars='-', fromfile_prefix_chars=None, argument_default=None)` and set the `allow_abbrev` parameter to `True`. This instructs the parser to ignore any arguments that it doesn't recognize. 

Section 3: Code Snippet
Here is an example of how to create an argument parser that ignores unrecognised arguments. 


```python 
import argparse

# Create an ArgumentParser object, set allow_abbrev to True
parser = argparse.ArgumentParser(allow_abbrev=True)

# Add arguments to the parser
parser.add_argument('--input', type=str, help='Input file')
parser.add_argument('--output', type=str, help='Output file')
parser.add_argument('--verbose', action='store_true', help='Verbose mode')

# Parse the arguments
args, unknown = parser.parse_known_args()

# Print the values of the parsed arguments
print(args)

# Print any unknown arguments
if unknown:
    print(f"Ignored arguments: {unknown}")
``` 

Section 4: Explanation 
In the code above, we first create an `ArgumentParser` object and set the `allow_abbrev` parameter to `True`. Then, we add three arguments to the parser: `--input`, `--output`, and `--verbose`. We then parse the arguments using `parse_known_args()`, which returns two values: the parsed arguments and any unknown arguments. Finally, we print the values of the parsed arguments and any unknown arguments. If there are any unknown arguments, we print a message indicating that they were ignored.
