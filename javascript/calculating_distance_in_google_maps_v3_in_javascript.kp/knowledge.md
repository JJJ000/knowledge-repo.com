---
title: Find the distance between two points in google maps version 3
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the Google Maps JavaScript API v3`s DistanceMatrixService to calculate the distance between two points.
---

**Contents**

[TOC]

# Section 1 - Preparation

Before calculating the distance between two points in Google Maps V3, the necessary preparation must be done. This includes loading the Google Maps API and creating two `LatLng` objects from the two points.

# Section 2 - Calculating the Distance

Once the preparation is complete, the distance between the two points can be calculated by using the `google.maps.geometry.spherical.computeDistanceBetween()` method. This method takes in two `LatLng` objects and returns the distance in meters.

# Section 3 - Converting to Other Units

If the distance in meters is not desired, it can be converted to other units such as kilometers, miles, or feet. This can be done by multiplying the distance in meters by the appropriate conversion factor.

# Section 4 - Example

Below is an example of how to calculate the distance between two points in Google Maps V3 using Javascript.

```javascript
// Load the Google Maps API
<script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY"></script>

// Create two LatLng objects from the two points
var point1 = new google.maps.LatLng(lat1, lng1);
var point2 = new google.maps.LatLng(lat2, lng2);

// Calculate the distance in meters
var distanceInMeters = google.maps.geometry.spherical.computeDistanceBetween(point1, point2);

// Convert the distance to kilometers
var distanceInKilometers = distanceInMeters * 0.001;
```
