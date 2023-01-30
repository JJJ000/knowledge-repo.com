---
title: What is the syntax for using a decimal step value in the range() function?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: To use a decimal step value for range() in Python, specify the step argument as a float.
---

**Contents**

[TOC]

#### Section 1: Definition

The range() function in Python is used to generate a sequence of numbers. It can accept three parameters: start, stop, and step. The start parameter is the starting number of the sequence. The stop parameter is the ending number of the sequence. The step parameter is the difference between each number in the sequence. It is usually an integer, but it can also be a decimal.

#### Section 2: Syntax

The syntax for using a decimal step value for range() is as follows:

```python
for x in range(start, stop, step):
    # code block
```

Where "start" is the starting number of the sequence, "stop" is the ending number of the sequence, and "step" is the difference between each number in the sequence.

#### Section 3: Example

For example, if you wanted to generate a sequence of numbers from 0 to 10 with a step value of 0.5, you could use the following code:

```python
for x in range(0, 10, 0.5):
    print(x)
```

This would generate the following sequence:

0.0
0.5
1.0
1.5
2.0
2.5
3.0
3.5
4.0
4.5
5.0
5.5
6.0
6.5
7.0
7.5
8.0
8.5
9.0
9.5

#### Section 4: Considerations

It is important to note that the range() function only works with integers, so if you are using a decimal step value, the sequence will be rounded to the nearest integer. Additionally, the step value must be positive; you cannot use a negative decimal step value.
