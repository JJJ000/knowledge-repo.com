---
title: What is the reason that the range function does not include the value of 'end' as part of its output?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Range(start, end) does not include end because range() is exclusive of the end value.
---

**Contents**

[TOC]

# Reason

The main reason for the range() function not including the end value is because it is designed to be used in conjunction with the for loop. The range() function returns a sequence of numbers starting from the given start number up to the end number, but not including the end number. This allows the for loop to iterate over the items in the sequence and stop when it reaches the end number.

# Example

For example, if we use the range() function to create a sequence of numbers from 0 to 5, the sequence will be 0, 1, 2, 3, 4. Notice that the number 5 is not included in the sequence. This is because the range() function is designed to create a sequence of numbers that are used to control the number of iterations in a for loop.

# Benefits

This design decision has several benefits. For one, it allows for more efficient code. Since the range() function does not have to include the end value, it can be computed more quickly. Additionally, it makes code easier to read and understand. When a for loop is used with the range() function, it is immediately apparent what the loop is doing and how many times it will iterate.
