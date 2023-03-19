---
title: What is the method to verify the intersection of two segments?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the Shapely library`s intersects() function to check for intersection between two LineString objects representing the two segments.
---

**Contents**

[TOC]

Section 1: Introduction

One common problem in computer science and geometry is determining whether two line segments intersect. This problem can be solved using the equations of the lines that connect the endpoints of each segment. In Python, there are several algorithms that can be used to solve this problem. In this tutorial, we will explore some of the most popular algorithms and their implementation in Python.

Section 2: Method 1 - Using the cross product

One popular method for determining whether two segments intersect is by using the cross product. This method involves calculating the cross product of the vectors that represent the two segments. If the cross product is zero, the two segments are parallel, and there is no intersection. If the cross product is nonzero, the two segments intersect at some point.

Here is an implementation of this method in Python:
```python
def intersect(segment1, segment2):
    x1, y1 = segment1[0]
    x2, y2 = segment1[1]
    x3, y3 = segment2[0]
    x4, y4 = segment2[1]

    det = (x1 - x2) * (y3 - y4) - (y1 - y2) * (x3 - x4)
    if det == 0: # The segments are parallel
        return False

    # Calculate the intersection point
    px = ((x1*y2 - y1*x2) * (x3 - x4) - (x1 - x2) * (x3*y4 - y3*x4)) / det
    py = ((x1*y2 - y1*x2) * (y3 - y4) - (y1 - y2) * (x3*y4 - y3*x4)) / det

    # Check if the intersection point is on both segments
    if min(x1, x2) <= px <= max(x1, x2) and min(y1, y2) <= py <= max(y1, y2) and min(x3, x4) <= px <= max(x3, x4) and min(y3, y4) <= py <= max(y3, y4):
        return True
    else:
        return False
```
This function takes two segments as input, where each segment is represented as a tuple of two points. The function first calculates the determinant of the two segments using the formula:

$det = (x_1 - x_2)*(y_3 - y_4) - (y_1 - y_2)*(x_3 - x_4)$

If the determinant is zero, the two segments are parallel, and there is no intersection. Otherwise, the function calculates the intersection point using the formulas:

$px = ((x_1*y_2 - y_1*x_2) * (x_3 - x_4) - (x_1 - x_2) * (x_3*y_4 - y_3*x_4)) / det$

$py = ((x_1*y_2 - y_1*x_2) * (y_3 - y_4) - (y_1 - y_2) * (x_3*y_4 - y_3*x_4)) / det$

Finally, the function checks whether the intersection point is on both segments using simple boundary checks.

Section 3: Method 2 - Using the slope of the lines

Another method for determining whether two segments intersect is by using the slope of the lines that connect the endpoints of each segment. This method involves calculating the slope, intercept, and y-coordinate of the intersection point for each line, and then checking whether the intersection point falls within the bounds of each segment.

Here is an implementation of this method in Python:
```python
def intersect(segment1, segment2):
    x1, y1 = segment1[0]
    x2, y2 = segment1[1]
    x3, y3 = segment2[0]
    x4, y4 = segment2[1]

    # Calculate the slopes and intercepts of the lines
    slope1 = (y2 - y1) / (x2 - x1) if x2 - x1 != 0 else float('inf')
    slope2 = (y4 - y3) / (x4 - x3) if x4 - x3 != 0 else float('inf')
    intercept1 = y1 - slope1 * x1 if x2 - x1 != 0 else x1
    intercept2 = y3 - slope2 * x3 if x4 - x3 != 0 else x3

    # Calculate the y-coordinate of the intersection point
    if slope1 == slope2:
        return False
    elif slope1 == float('inf'):
        ix = x1
        iy = slope2 * ix + intercept2
    elif slope2 == float('inf'):
        ix = x3
        iy = slope1 * ix + intercept1
    else:
        ix = (intercept2 - intercept1) / (slope1 - slope2)
        iy = slope1 * ix + intercept1

    # Check if the intersection point is on both segments
    if min(x1, x2) <= ix <= max(x1, x2) and min(y1, y2) <= iy <= max(y1, y2) and min(x3, x4) <= ix <= max(x3, x4) and min(y3, y4) <= iy <= max(y3, y4):
        return True
    else:
        return False
```
This function works similar to the first method, but instead calculates the slope and intercept of each line using the formulas:

$slope = (y_2 - y_1) / (x_2 - x_1)$

$intercept = y_1 - slope * x_1$

If the lines are parallel, there is no intersection, and the function returns False. Otherwise, the function calculates the y-coordinate of the intersection point using the formula:

$iy = slope_1 * ix + intercept_1$

Here, the function checks if the intersection point falls within the bounds of both segments and returns True if it does.

Section 4: Conclusion

In this tutorial, we have explored two popular methods for determining whether two line segments intersect in Python. The first method involves using the cross product of the vectors that represent the segments, while the second method involves calculating the slope and intercept of each line that connects the endpoints of the segments. Both methods are viable solutions to this problem, and which one to use depends on personal preference and specific use cases.
