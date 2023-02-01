---
title: What is the process for generating a random number within a given decimal range?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the random.uniform() function to get a random number between a float range in Python.
---

**Contents**

[TOC]

# Using the random.uniform() Function

## Syntax
The syntax for the random.uniform() function is:

`random.uniform(a, b)`

where a is the lower bound of the range and b is the upper bound of the range.

## Example
Here is an example of how to use this function to generate a random number between 0.0 and 1.0:

`import random
random_number = random.uniform(0.0, 1.0)
print(random_number)`

## Output
The output of the above code will be a random float number between 0.0 and 1.0.

# Using the random.randrange() Function

## Syntax
The syntax for the random.randrange() function is:

`random.randrange(start, stop[, step])`

where start is the lower bound of the range, stop is the upper bound of the range, and step is the step size.

## Example
Here is an example of how to use this function to generate a random number between 0.0 and 1.0:

`import random
random_number = random.randrange(0, 1000, 0.1)
print(random_number)`

## Output
The output of the above code will be a random float number between 0.0 and 1.0.
