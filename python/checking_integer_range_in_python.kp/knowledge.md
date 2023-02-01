---
title: Figure out if an integer is between two other integers
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Yes, you can use the comparison operators (>, <, >=, <=) to determine if an integer is between two other integers.
---

**Contents**

[TOC]

# Answer

## Using Comparison Operators
We can use comparison operators to determine whether an integer is between two other integers. To do this, we need to compare the integer with the two other integers to determine if it is greater than or equal to the lower integer and less than or equal to the higher integer.

## Syntax
The syntax for using comparison operators to determine whether an integer is between two other integers is as follows:

```
lower_int <= int <= higher_int
```

## Example
For example, if we wanted to determine if the integer 5 is between the integers 3 and 7, we could use the following comparison operator:

```
3 <= 5 <= 7
```

## Output
The output of the comparison operator in this example would be `True`, since 5 is indeed between 3 and 7.
