---
title: What is the method for determining the angle between a line and the horizontal axis?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the arctangent function (math.atan) to find the angle in radians and convert to degrees (math.degrees) if necessary.
---

**Contents**

[TOC]

Introduction

Calculating the angle between a line and the horizontal axis is a common operation in geometry and computer vision. In this tutorial, we will show you how to do this in Python using the arctangent function from the math module.

Section 1: Finding the slope of the line

The first step in finding the angle between a line and the horizontal axis is to find the slope of the line. The slope of a line is defined as the change in the y-coordinate divided by the change in the x-coordinate. In Python, we can calculate the slope of a line given two points (x1, y1) and (x2, y2) as follows:

```
def slope(x1, y1, x2, y2):
    return (y2 - y1) / (x2 - x1)
```

Section 2: Calculating the angle

Once we have the slope of the line, we can use the arctangent function to calculate the angle between the line and the horizontal axis. This is done using the formula:

```
angle = arctan(slope)
```

In Python, we can calculate the arctangent of a number using the math.atan function. Here is an example using the slope function defined in Section 1:

```
import math

def angle(x1, y1, x2, y2):
    slope = (y2 - y1) / (x2 - x1)
    return math.atan(slope)
```

This function calculates the angle between the line that passes through the points (x1, y1) and (x2, y2) and the horizontal axis.

Section 3: Converting radians to degrees

The angle calculated in Section 2 is in radians. If we want to convert the angle to degrees, we can use the math.degrees function. Here is an updated version of the angle function that returns the angle in degrees:

```
def angle(x1, y1, x2, y2):
    slope = (y2 - y1) / (x2 - x1)
    radians = math.atan(slope)
    return math.degrees(radians)
```

Section 4: Putting it all together

Here is an example of how to use the angle function:

```
x1, y1 = 0, 0
x2, y2 = 1, 1

degrees = angle(x1, y1, x2, y2)
print(degrees)
```

This code defines two points (0,0) and (1,1), and calculates the angle between the line that passes through these points and the horizontal axis. The output will be approximately 45 degrees.
