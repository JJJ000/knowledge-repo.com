---
title: Determining the distance between two points by using their latitude and longitude
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the Haversine formula to calculate the great-circle distance between two points on a sphere given their latitude and longitude in Python.
---

**Contents**

[TOC]

1. Introduction
Getting the distance between two points on a sphere, such as the Earth, is not as straightforward as calculating the distance between two points on a plane. This is because the Earth is not flat, but instead, it is curved. Therefore, we need to use a formula that takes into account the curvature of the Earth to calculate the distance between two points based on their latitude and longitude. In this article, we will explore two such formulas: the Haversine formula and the Vincenty formula.

2. The Haversine Formula
The Haversine formula is a popular formula for calculating distances between two points based on their latitude and longitude. The formula uses the Earth's radius to take into account the curvature of the Earth. Here is the formula:

```
from math import sin, cos, sqrt, atan2, radians

def haversine(lat1, lon1, lat2, lon2):
    R = 6371.0 # Radius of the Earth in kilometers
    lat1 = radians(lat1)
    lon1 = radians(lon1)
    lat2 = radians(lat2)
    lon2 = radians(lon2)
    
    dlon = lon2 - lon1
    dlat = lat2 - lat1
    
    a = sin(dlat / 2)**2 + cos(lat1) * cos(lat2) * sin(dlon / 2)**2
    c = 2 * atan2(sqrt(a), sqrt(1 - a))
    
    distance = R * c
    
    return distance
```

3. The Vincenty Formula
The Vincenty formula is another popular formula for calculating distances between two points based on their latitude and longitude. This formula is more accurate than the Haversine formula because it takes into account the flattening of the Earth at the poles. Here is the formula:

```
from math import sin, cos, sqrt, atan2, radians

def vincenty(lat1, lon1, lat2, lon2):
    a = 6378137 # The Earth's equatorial radius in meters
    b = 6356752.314245 # The Earth's polar radius in meters
    f = 1 / 298.257223563 # The Earth's flattening
    
    lat1 = radians(lat1)
    lon1 = radians(lon1)
    lat2 = radians(lat2)
    lon2 = radians(lon2)
    
    L = lon2 - lon1
    
    U1 = atan2((1 - f) * tan(lat1), cos(L))
    U2 = atan2((1 - f) * tan(lat2), cos(L))
    
    sinU1 = sin(U1)
    cosU1 = cos(U1)
    sinU2 = sin(U2)
    cosU2 = cos(U2)
    
    lambdaa = L
    
    i = 0
    while abs(lambdaa) > 1e-12 and i < 100:
        sinlambdaa = sin(lambdaa)
        coslambdaa = cos(lambdaa)
        
        sinSigma = sqrt((cosU2 * sinlambdaa)**2 + (cosU1 * sinU2 - sinU1 * cosU2 * coslambdaa)**2)
        cosSigma = sinU1 * sinU2 + cosU1 * cosU2 * coslambdaa
        Sigma = atan2(sinSigma, cosSigma)
        
        sinalpha = cosU1 * cosU2 * sinlambdaa / sinSigma
        cos2alpha = 1 - sinalpha**2
        cos2SigmaM = cosSigma - 2 * sinU1 * sinU2 / cos2alpha
        
        C = f / 16 * cos2alpha * (4 + f * (4 - 3 * cos2alpha))
        lambdaaold = lambdaa
        lambdaa = L + (1 - C) * f * sinalpha * (Sigma + C * sinSigma * (cos2SigmaM + C * cosSigma * (-1 + 2 * cos2SigmaM**2)))
        
        i += 1
    
    u2 = cos2alpha * (a**2 - b**2) / b**2
    A = 1 + u2 / 16384 * (4096 + u2 * (-768 + u2 * (320 - 175 * u2)))
    B = u2 / 1024 * (256 + u2 * (-128 + u2 * (74 - 47 * u2)))
    deltaSigma = B * sinSigma * (cos2SigmaM + B / 4 * (cosSigma * (-1 + 2 * cos2SigmaM**2) - B / 6 * cos2SigmaM * (-3 + 4 * sinSigma**2) * (-3 + 4 * cos2SigmaM**2)))
    
    distance = b * A * (Sigma - deltaSigma)
    
    return distance
```

4. Conclusion
In this article, we explored two formulas for calculating distances between two points based on their latitude and longitude: the Haversine formula and the Vincenty formula. Both of these formulas take into account the curvature of the Earth and are accurate for short to medium distances. The Haversine formula is simpler and faster, while the Vincenty formula is more accurate and works well for long distances. Depending on your needs, you can choose the appropriate formula for your project.
