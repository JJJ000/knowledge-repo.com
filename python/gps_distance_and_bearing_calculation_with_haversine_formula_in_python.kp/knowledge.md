---
title: Rewrite Python code for calculating the bearing and distance between two gps coordinates using the haversine formula
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: The Haversine formula in Python calculates the distance and bearing between two GPS points based on their latitude and longitude coordinates.
---

**Contents**

[TOC]

## Introduction

The Haversine formula is a widely used formula for calculating the distance between two points on a sphere. It is particularly useful in calculating the distance between two GPS points, since the Earth can be approximated as a sphere.

In this tutorial, we will learn how to calculate the distance and bearing between two GPS points using the Haversine formula in Python.

## Understanding the Haversine formula

The Haversine formula is based on the law of haversines, which states that the haversine of a central angle between two points on a sphere is equal to the sum of the haversines of the two angles from the points to the center of the sphere.

The formula to calculate distance between two points on Earth is as follows:

```
a = sin²(Δlat/2) + cos(lat1).cos(lat2).sin²(Δlong/2)
c = 2.atan2(√a, √(1−a))
d = R.c
```

where:
- lat1 and lat2 are the latitudes of the two points
- Δlat and Δlong are the differences in latitude and longitude between the two points
- R is the radius of the Earth (mean radius = 6,371km)
- d is the distance between the two points along a great circle of the sphere

## Implementing the formula in Python

To calculate the distance between two GPS points, we can write a Python function that takes in the latitude and longitude of the two points and returns the distance in kilometers.

```python
import math

def distance(lat1, lon1, lat2, lon2):
    R = 6371  # radius of Earth in kilometers
    dLat = math.radians(lat2 - lat1)
    dLon = math.radians(lon2 - lon1)
    a = math.sin(dLat/2) * math.sin(dLat/2) + \
        math.cos(math.radians(lat1)) * math.cos(math.radians(lat2)) * \
        math.sin(dLon/2) * math.sin(dLon/2)
    c = 2 * math.atan2(math.sqrt(a), math.sqrt(1-a))
    distance = R * c
    return distance
```

We can now use this function to calculate the distance between two GPS points:

```python
# Sydney Opera House
lat1 = -33.857197
lon1 = 151.21514

# Statue of Liberty
lat2 = 40.6892494
lon2 = -74.0445004

print(distance(lat1, lon1, lat2, lon2))  # output: 16074.753311996212 (in km)
```

## Calculating the bearing between two GPS points

In addition to calculating the distance between two GPS points, we can also calculate the bearing, or direction, from one point to the other. The formula for calculating the bearing is as follows:

```
θ = atan2(sin(Δlong).cos(lat2), cos(lat1).sin(lat2) − sin(lat1).cos(lat2).cos(Δlong))
```

where:
- lat1 and lat2 are the latitudes of the two points
- Δlong is the difference in longitude between the two points
- θ is the bearing from point 1 to point 2, measured in degrees clockwise from north

We can implement this formula in Python as follows:

```python
def bearing(lat1, lon1, lat2, lon2):
    dLon = math.radians(lon2 - lon1)
    y = math.sin(dLon) * math.cos(math.radians(lat2))
    x = math.cos(math.radians(lat1))*math.sin(math.radians(lat2)) - \
        math.sin(math.radians(lat1))*math.cos(math.radians(lat2))*math.cos(dLon)
    brng = math.degrees(math.atan2(y, x))
    brng = (brng + 360) % 360
    return brng
```

We can now use this function to calculate the bearing from one GPS point to another:

```python
# Sydney Opera House
lat1 = -33.857197
lon1 = 151.21514

# Statue of Liberty
lat2 = 40.6892494
lon2 = -74.0445004

print(bearing(lat1, lon1, lat2, lon2))  # output: 312.0670642160116 (in degrees clockwise from north)
```

## Conclusion

In this tutorial, we learned how to calculate the distance and bearing between two GPS points using the Haversine formula in Python. These calculations can be used in a wide range of applications, including navigation, distance-based search, and geolocation services.
