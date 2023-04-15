---
title: Determine the remainder of a number after division
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To find the division remainder of a number in Python, use the modulus operator (%).
---

**Contents**

[TOC]

## Introduction

In Python, we can use the modulo operator (%) to find the remainder of a division operation between two numbers. The modulo operator returns the remainder of a division operation, which can be useful in various situations, such as checking if a number is even or odd, calculating time intervals, or checking if a number is divisible by another number.

## Example

Let's say we want to find the remainder of the division operation between 7 and 3. We can use the modulo operator as follows:

```
7 % 3
```

This will return the value 1, which is the remainder of the division operation between 7 and 3.

## Using the Modulo Operator to Check for Evenness

One common use of the modulo operator is to check if a number is even or odd. We can do this by using the modulo operator to find the remainder of the division operation between the number in question and 2. If the remainder is 0, the number is even. If the remainder is 1, the number is odd.

For example:

```
# checking if 6 is an even number
6 % 2
# output: 0

# checking if 5 is an odd number
5 % 2
# output: 1
```

## Using the Modulo Operator to Calculate Time Intervals

Another use case for the modulo operator is in calculating time intervals. For example, let's say we want to convert seconds into hours, minutes, and seconds. We can use the following approach:

```
# number of seconds
seconds = 3600

# number of hours
hours = seconds // 3600

# number of remaining seconds
remaining_seconds = seconds % 3600

# number of minutes
minutes = remaining_seconds // 60

# number of remaining seconds
remaining_seconds = remaining_seconds % 60

# output
print(f"{hours} hours, {minutes} minutes, {remaining_seconds} seconds")
# output: 1 hours, 0 minutes, 0 seconds
```

In this example, we use the modulo operator to find the remainder of the division operation between the number of seconds and 3600 (the number of seconds in an hour) to find the remaining seconds after calculating the number of hours. We then repeat this process to calculate the number of minutes and remaining seconds.

## Conclusion

In conclusion, the modulo operator is a useful tool in Python for finding the remainder of division operations. It can be especially useful in checking for evenness and calculating time intervals, among other tasks.
