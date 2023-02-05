---
title: Create 'n' distinct random numbers within a specified range
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use random.sample() to generate `n` unique random numbers within a range.
---

**Contents**

[TOC]

# Using the random module
The random module provides access to various useful functions to generate random numbers in python. 

## Generating a single random number
To generate a single random number within a range, use the `randint()` function. This function takes two arguments, a lower bound and an upper bound, and returns a random integer between those two bounds, inclusive.

For example, to generate a random number between 1 and 10:

```
import random

random_number = random.randint(1, 10)
print(random_number)
```

## Generating multiple unique random numbers
To generate multiple unique random numbers within a range, use the `sample()` function. This function takes two arguments, a population (i.e. a sequence of numbers) and a sample size, and returns a list of unique random numbers from the population of the given size.

For example, to generate 3 unique random numbers between 1 and 10:

```
import random

population = range(1, 11)
sample_size = 3

random_numbers = random.sample(population, sample_size)
print(random_numbers)
```
