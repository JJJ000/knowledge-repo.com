---
title: I need a basic example of using argparse with one argument that produces three results
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Using the argparse module, you can create a parser object with one argument and three results, and parse the argument to get the desired output.
---

**Contents**

[TOC]

# Section 1: Importing argparse

import argparse

# Section 2: Creating the Argument Parser

parser = argparse.ArgumentParser(description='Example argparse program')

# Section 3: Adding an Argument

parser.add_argument('-n', action='store', dest='name', help='Name of the user')

# Section 4: Parsing the Arguments

results = parser.parse_args()

print("Hello " + results.name + "!")
print("Welcome to the argparse example!")
print("Have a great day!")
