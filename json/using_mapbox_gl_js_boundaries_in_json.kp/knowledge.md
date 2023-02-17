---
title: Mapbox gl js functions to retrieve and adjust the boundaries of a map
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: The getBounds() and fitBounds() methods return and accept a LngLatBounds object, which is an array of two LngLat objects in JSON format.
---

**Contents**

[TOC]

## getBounds()

The `getBounds()` method of Mapbox GL JS returns the current geographical bounds of the map view in the form of a LngLatBounds object. This object contains the southwest and northeast corners of the map view, represented as two LngLat objects.

## fitBounds()

The `fitBounds()` method of Mapbox GL JS takes a LngLatBounds object and sets the map view to contain the given geographical bounds. This method is useful for zooming the map view to fit a given set of coordinates.

## JSON Format

The JSON format for both `getBounds()` and `fitBounds()` is the same. The object consists of two keys: `sw` and `ne`. `sw` refers to the southwest corner of the bounds, and `ne` refers to the northeast corner. Each of these keys is an object containing the `lng` and `lat` keys, which refer to the longitude and latitude of the respective corner.

An example of the JSON format for a LngLatBounds object is as follows:

```json
{
  "sw": {
    "lng": -122.45,
    "lat": 37.78
  },
  "ne": {
    "lng": -122.40,
    "lat": 37.81
  }
}
```
