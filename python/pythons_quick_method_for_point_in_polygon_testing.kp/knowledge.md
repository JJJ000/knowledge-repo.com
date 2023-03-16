---
title: How can I check whether a point is contained within a polygon in Python most quickly?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: The shapely library provides a quick and efficient way of checking if a point is inside a polygon in Python.
---

**Contents**

[TOC]

Section 1: Introduction

Checking if a point is within a polygon is a common problem in various fields. There are many algorithms to solve this problem, and some are more efficient than others. In this article, we will explore some of the fastest ways to check if a point is inside a polygon in Python.

Section 2: Using the Shapely Library

The Shapely library provides an efficient and easy-to-use way to check if a point is within a polygon. Shapely is a Python library for handling and analyzing geometric objects such as points, lines, polygons, and more. To use the Shapely library, we must first install it. We can install it using the pip command:

```python
pip install Shapely
```

Once installed, we can use the Point and Polygon objects to check if a point is within a polygon. Here's an example:

```python
from shapely.geometry import Point, Polygon

# define the polygon
polygon = Polygon([(0, 0), (0, 10), (10, 10), (10, 0)])

# define the point
point = Point(5, 5)

# check if the point is within the polygon
if polygon.contains(point):
    print("The point is within the polygon")
else:
    print("The point is outside the polygon")
```

This method is efficient and easy to use, especially when dealing with complex polygons.

Section 3: Using the PyGeos Library

PyGeos is a Python library that provides fast and memory-efficient operations on geometries. It is built on top of the GEOS library, which is a C++ library for performing geometric operations. To use the PyGeos library, we must first install it. We can install it using the pip command:

```python
pip install pygeos
```

Once installed, we can use the contains function of the Polygon object to check if a point is within a polygon. Here's an example:

```python
import pygeos

# define the polygon
polygon = pygeos.box(0, 0, 10, 10)

# define the point
point = pygeos.points(5, 5)

# check if the point is within the polygon
if pygeos.contains(polygon, point):
    print("The point is within the polygon")
else:
    print("The point is outside the polygon")
```

This method is faster than the previous method and is suitable for larger datasets.

Section 4: Using the Ray Casting Algorithm

The Ray Casting Algorithm is a classic algorithm for determining if a point is within a polygon. The algorithm works by casting a ray from the point to the right and counting the number of intersections with the edges of the polygon. If the number of intersections is odd, the point is within the polygon; otherwise, it is outside. Here's an example implementation of the Ray Casting Algorithm:

```python
def point_in_poly(x, y, poly):
    n = len(poly)
    inside = False
    p1x, p1y = poly[0]
    for i in range(n + 1):
        p2x, p2y = poly[i % n]
        if y > min(p1y, p2y):
            if y <= max(p1y, p2y):
                if x <= max(p1x, p2x):
                    if p1y != p2y:
                        x_inters = (y - p1y) * (p2x - p1x) / (p2y - p1y) + p1x
                    if p1x == p2x or x <= x_inters:
                        inside = not inside
        p1x, p1y = p2x, p2y
    return inside
```

To use this function, we can pass in the x and y coordinates of the point and a list of vertices of the polygon. Here's an example:

```python
# define the polygon vertices
poly = [(0, 0), (0, 10), (10, 10), (10, 0)]

# define the point coordinates
x = 5
y = 5

# check if the point is within the polygon
if point_in_poly(x, y, poly):
    print("The point is within the polygon")
else:
    print("The point is outside the polygon")
```

This method is suitable for simple polygons and small datasets. However, it can become slow and inefficient when dealing with larger datasets or polygons with many vertices.
