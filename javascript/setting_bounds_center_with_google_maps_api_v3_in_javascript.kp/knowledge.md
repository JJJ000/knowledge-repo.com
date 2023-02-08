---
title: Set the boundaries and center point for the google maps API v3
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: The bounds and center of a map can be set using the setCenter() and fitBounds() methods of the Google Maps API v3.
---

**Contents**

[TOC]

**Section 1: Setting Bounds**

Bounds can be set in the Google Maps API v3 by creating a LatLngBounds object and passing in the coordinates of the south-west and north-east corners of the desired area. This can be done using the following code:

`var bounds = new google.maps.LatLngBounds(
  new google.maps.LatLng(southWestLat, southWestLng),
  new google.maps.LatLng(northEastLat, northEastLng)
);`

**Section 2: Setting the Map Bounds**

Once the bounds have been set, they can be applied to the map by using the `fitBounds` method of the map object. This can be done using the following code:

`map.fitBounds(bounds);`

**Section 3: Setting the Map Center**

The center of the map can be set by using the `setCenter` method of the map object. This can be done using the following code:

`map.setCenter(new google.maps.LatLng(lat, lng));`

**Section 4: Setting the Map Zoom Level**

The zoom level of the map can be set by using the `setZoom` method of the map object. This can be done using the following code:

`map.setZoom(zoomLevel);`
